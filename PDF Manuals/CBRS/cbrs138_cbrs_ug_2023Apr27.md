---
title: "Cost Basis Reporting Service (CBRS) User Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cbrs138_cbrs_ug_2023Apr27.pdf"
pages: 166
size: "6549.5 KB"
category: "CBRS"
ingested_on: "2026-06-05"
---

# Cost Basis Reporting Service (CBRS) User Guide

**Original File:** [cbrs138_cbrs_ug_2023Apr27.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cbrs138_cbrs_ug_2023Apr27.pdf)  
**Category:** CBRS  
**Total Pages:** 166  
**File Size:** 6549.5 KB  

---

## Page 1

 
 
COST BASIS REPORTING SERVICE 
(CBRS) 
CBRS USER GUIDE 
VERSION 9.2 
APRIL 27, 2023 
 


---

## Page 2

 
 
© 2023 The Depository Trust & Clearing Corporation. All rights reserved.   
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.  
 
Doc Info: April 27, 2023 
Publication Code: CBRS138 
Service: Cost Basis Reporting Service (CBRS) 
Title: CBRS User Guide 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
1. About This User Guide .................................................................................................................................. 10 
Getting Answers to Your CBRS Questions ...................................................................................................... 11 
2. General Information ....................................................................................................................................... 12 
Scope of the System: Transfer of Information Only .......................................................................................... 12 
[[BASIC]] Feature: Input .......................................................................................................................................... 12 
Input Record Content Indicator Types ............................................................................................................ 15 
Original [[Asset]] and Tax Lot Records Form a Package .................................................................................... 15 
Package Rule Applies to Corrected Records .................................................................................................. 15 
Exceptions to Package Rule: Firm Reject and Request Records ................................................................... 16 
Association of [[Asset]] and Tax Lot Records ..................................................................................................... 16 
[[BASIC]] Feature: Output ....................................................................................................................................... 18 
Output Available Through Both Automated Connection and [[DTCC]] Web Portal ............................................ 18 
3. Eligibility for CBRS ........................................................................................................................................ 19 
User Eligibility ................................................................................................................................................... 19 
Cost Basis User Master File ............................................................................................................................ 19 
Cost Basis User Master File Record Layout Fields ....................................................................................... 20 
Active/Inactive Feature .................................................................................................................................. 21 
[[Asset]] Eligibility .................................................................................................................................................. 26 
4. Application Input and Output ........................................................................................................................ 27 
General Record Layout Information .................................................................................................................. 27 
Filler Fields ...................................................................................................................................................... 29 
Using CBRS for Cost Basis Information in Non-US Currency .......................................................................... 29 
Input General Information ................................................................................................................................. 30 
Transfer Control Number ................................................................................................................................. 30 
Firm Reject Record ......................................................................................................................................... 31 
Firm Number and Type Versus Customer Account Number Fields ................................................................ 32 
Contra Firm Number ........................................................................................................................................ 33 
Contra Firm Type ............................................................................................................................................ 33 

---

## Page 4

 
 
Numeric Fields ................................................................................................................................................ 37 
[[Asset]] Category Field ....................................................................................................................................... 37 
Sum of the Tax Lot Quantities Must Match the [[Asset]] Quantity ...................................................................... 37 
Optional Fields ................................................................................................................................................ 38 
Borrowed Position Code .................................................................................................................................. 38 
ACATS [[Asset]] Sequence Number ................................................................................................................... 39 
Output General Information .............................................................................................................................. 39 
Distribution Side .............................................................................................................................................. 40 
Cost Basis Control Number ............................................................................................................................. 40 
System Rejects ............................................................................................................................................... 41 
System Action Field ......................................................................................................................................... 41 
System Reject Reason Field ........................................................................................................................... 41 
Status Fields .................................................................................................................................................... 42 
Example of System Changed .......................................................................................................................... 42 
Example of System Rejected .......................................................................................................................... 43 
Output Dropped Records ................................................................................................................................ 43 
LPA Number and LPA Type ............................................................................................................................ 43 
5. Best Practices................................................................................................................................................. 45 
Resolving Issues with the Contra Party ............................................................................................................ 45 
Firms Submit and Receive Records ................................................................................................................. 45 
When Should a Firm Send the CBRS Record? ................................................................................................ 45 
Corrected Record .............................................................................................................................................. 46 
Some Scenarios About Corrected Records .................................................................................................... 46 
Firm Reject and Request Records .................................................................................................................... 47 
[[DO]] Not Request Basis for Lots Received With Unknown Basis ....................................................................... 48 
Submitting and Receiving Noncovered Accounts and Noncovered Security Types ........................................ 49 
Covered Fixed Income Assets Transferred in 2014 ......................................................................................... 49 
CBRS Quantity Should Equal the Original [[Asset]] Transfer Quantity - Avoid Fractional [[shares]] ....................... 49 
Populating CBRS Records for ACATS Reclaim or Fail Reversal Transactions ............................................... 50 
Sending a CBRS Record for an [[Asset]] Held in Multiple Currencies ................................................................. 51 

---

## Page 5

 
 
Sending Cost Basis for an Invalid Certificate ................................................................................................... 51 
Field Specific Best Practices ............................................................................................................................ 52 
Transaction Type (A/T) .................................................................................................................................... 52 
Transfer Control Number (A/T) ....................................................................................................................... 52 
Alternate Control Number (A/T) ...................................................................................................................... 53 
[[Asset]] Description (A/T) ................................................................................................................................... 53 
[[Asset]] Category (A) .......................................................................................................................................... 53 
Transferring Basis on Rights or [[Warrants]] ....................................................................................................... 53 
Receiver Customer Account Number (A/T) ..................................................................................................... 53 
Deliverer Customer Account Number (A/T) .................................................................................................... 53 
Total Position Quantity/Tax Lot Quantity (A/T) ................................................................................................ 54 
Date Transfer was Initiated and [[settlement]] Date of Transfer (A) ................................................................... 54 
Disposition Method Used (A)........................................................................................................................... 54 
[[shares]] to Cover Short Indicator (A) ................................................................................................................ 54 
Noncovered/Pending Indicator (T) .................................................................................................................. 55 
Taxes Reported by [[issuer]]/[[transfer agent]] (T) ................................................................................................. 56 
Gifted or Inherited Indicator (T) ....................................................................................................................... 56 
Fair Market Value as of Date of Gift (T) .......................................................................................................... 56 
Position Code (T) ............................................................................................................................................ 57 
Position Code for Options (T) .......................................................................................................................... 57 
Populating Acquisition Date of Tax Lot field when Date is Unknown (T) ........................................................ 57 
Original Acquisition Date for Wash Sale Adjustment (T) ................................................................................ 57 
Wash Sale Adjustment Amount (T) ................................................................................................................. 58 
Exchange Rate (T) .......................................................................................................................................... 58 
Tax Lot Original Cost (T) ................................................................................................................................. 58 
Tax Lot Current Cost (T) ................................................................................................................................. 59 
Zero Basis Indicator (T) ................................................................................................................................... 59 
Tax Lot Original Unit Price (T) ......................................................................................................................... 60 
Employee Plan [[shares]] Indicator (T) ............................................................................................................... 60 
Fields for Fixed Income Elections (T) .............................................................................................................. 60 

---

## Page 6

 
 
Purchase/ [[Dividend]] Reinvestment Indicator (T).............................................................................................. 60 
Market Discount (T) ......................................................................................................................................... 61 
Bond [[Premium]] (T) ........................................................................................................................................... 62 
Acquisition [[Premium]] (T) .................................................................................................................................. 63 
Accrued OID (T) .............................................................................................................................................. 63 
Last Adjustment Date (T) ................................................................................................................................ 64 
Carryover Offset (T) ........................................................................................................................................ 65 
Prior Year Mark to Market (T).......................................................................................................................... 66 
[[settlement]] Date (T) ......................................................................................................................................... 66 
Accrued Unrealized Market Discount (T) ........................................................................................................ 66 
6. File Input and Output Through Common Data Transfer Service (CDTS) ................................................. 67 
File Input ........................................................................................................................................................... 67 
File Output: Transaction MRO .......................................................................................................................... 69 
File Output: Cost Basis User Master File MRO ................................................................................................ 69 
Limits on When Output Files and Data are Available ....................................................................................... 69 
Input and Output Timing ................................................................................................................................... 70 
Extension Guidelines ........................................................................................................................................ 70 
CBRS Application Output Header ..................................................................................................................... 71 
CBRS Application Output Trailer ...................................................................................................................... 72 
7. Accessing CBRS Through the [[DTCC]] Web Portal ....................................................................................... 73 
Logging on to the System ................................................................................................................................. 73 
Creating CBRS Transactions ............................................................................................................................ 74 
Working With Pending CBRS Transactions ..................................................................................................... 77 
Adding Assets to CBRS Transactions ............................................................................................................. 77 
Adding More Tax Lots to an Existing Transaction .......................................................................................... 80 
Listing Pending Transactions .......................................................................................................................... 83 
Searching Pending Transactions .................................................................................................................... 84 
Deleting Transactions ....................................................................................................................................... 86 
Deleting Transactions From the Transfer List ................................................................................................. 86 
Deleting Transactions From the Transfer Information Update Page .............................................................. 88 

---

## Page 7

 
 
Editing Transfer Information, [[Asset]] Records, and Tax Lot Records ................................................................ 89 
Viewing and Updating Transfer Information .................................................................................................... 89 
Viewing and Updating Assets.......................................................................................................................... 91 
Deleting Assets ............................................................................................................................................... 94 
Viewing and Updating Tax Lots ...................................................................................................................... 98 
Deleting Tax Lots ..........................................................................................................................................100 
Working With CBRS Batches .........................................................................................................................104 
Sending a Batch to [[DTCC]] .............................................................................................................................104 
Viewing Sent Batches ...................................................................................................................................107 
Verifying the File Sent Successfully Using the Confirms Utility ....................................................................108 
Resending Batches .......................................................................................................................................109 
Uploading Records to CBRS ..........................................................................................................................110 
Overview of the CBRS Upload Process ........................................................................................................111 
Downloading CBRS Spreadsheet Templates ...............................................................................................114 
For Earlier Versions of Microsoft Excel .........................................................................................................115 
Spreadsheet Template Column Headers ......................................................................................................115 
Spreadsheets at a Glance .............................................................................................................................117 
Adding an [[Asset]] With One Tax Lot ...............................................................................................................119 
Adding Assets With Multiple Tax Lots ...........................................................................................................120 
Adding Multiple [[Asset]] Records .....................................................................................................................121 
Adding an [[Asset]] Without a Tax Lot (Firm Reject and Request Records Only) ............................................123 
CBRS Spreadsheet Examples ......................................................................................................................123 
Example One: An [[Asset]] With One Tax Lot .................................................................................................123 
Example Two: An [[Asset]] With Multiple Tax Lots ..........................................................................................124 
Example Three: Multiple [[Asset]] Records .....................................................................................................125 
Uploading the CBRS Spreadsheet ................................................................................................................127 
Viewing and Modifying Records After Uploading ..........................................................................................128 
Modifying Uploaded Information ...................................................................................................................129 
Verifying the File Sent Successfully (Using the Confirms Utility) ..................................................................129 
Reviewing and Correcting Spreadsheet Errors .............................................................................................130 

---

## Page 8

 
 
Errors That You See Immediately Upon Submission ..................................................................................130 
Errors That You See After End-of-Day Processing .....................................................................................131 
Searching CBRS Transactions .......................................................................................................................133 
Using Quick Search .......................................................................................................................................133 
Using Advanced Search ................................................................................................................................137 
Displaying [[Asset]] and Tax Lot Details ............................................................................................................139 
Searching for CBRS Users .............................................................................................................................140 
Searching for Active CBRS Accounts ...........................................................................................................140 
Searching for Inactive CBRS Accounts .........................................................................................................141 
Downloading and Viewing Cost Basis Files and Reports ...............................................................................144 
Downloading Cost Basis Files .......................................................................................................................144 
Viewing Cost Basis Files Using Microsoft Excel ...........................................................................................147 
Size Limit for Transaction Download Files ....................................................................................................149 
Time Frames for Files and Data Availability ..................................................................................................149 
[[DTCC]] Web Portal Data Entry on Weekends and Holidays ..........................................................................149 
8. CBRS Statistical Reports ............................................................................................................................ 150 
Requesting CBRS Statistical Report Access ...................................................................................................150 
Accessing CBRS Statistical Reports from the CBRS Web Portal .....................................................................151 
Understanding the Submitter of Assets Report .............................................................................................153 
Understanding the Receiver of Assets Report ..............................................................................................155 
9. Joining the Service ...................................................................................................................................... 157 
Multiple Output File Set-up .............................................................................................................................157 
CBRS Billing ...................................................................................................................................................158 
10. User Testing ................................................................................................................................................ 159 
Testing Data Input...........................................................................................................................................159 
Testing Data Output ........................................................................................................................................160 
Testing the Daily Deposit File for Transfer Agents .......................................................................................160 
Canned Transaction Output File ...................................................................................................................161 
Appendix A: List and Description of File Identification Numbers .............................................................. 162 
CBRS Input SYS [[ID]] Numbers ........................................................................................................................162 

---

## Page 9

 
 
List of CBRS Output File Identification Numbers ............................................................................................162 
CBRS Output Files and Reports .....................................................................................................................163 
Appendix B: List of Valid Characters for CBRS ............................................................................................ 165 
 

---

## Page 10

CBRS User Guide 
About This User Guide 10 
1. ABOUT THIS USER GUIDE 
The enhanced Cost Basis Reporting Service (CBRS) mitigates potential endless paper trails, added costs and 
more operational risk associated with transferring cost basis information manually. The previous version of 
CBRS allowed financial firms to pass customer cost basis information about assets transferred through the 
Automated Customer Account Transfer Service (ACATS). The current service extends its efficiencies and 
capabilities to [[Equity]] transfer agents and issuers, [[Mutual Funds]], custodian banks and [[Broker]]/dealers to pass 
cost basis information—from one financial firm to another—for all [[Asset]] transfers.  
This user guide provides details of CBRS and its functionality. Included in this user guide are general 
descriptions of businesses processes and information flow in CBRS. The guide assumes that you have prior 
[[securities]] industry experience, a [[BASIC]] knowledge of cost basis terminology and processing, and knowledge of 
Microsoft Excel. 
Version Date Author Notes – Sections Edited 
3.0   September 
2013 
Lydia Midwood Source document 
4.0 September 
2014 
Janice DiTore Additions to Sections 3 (p.15); 4 (p.25); 5 (p.43), (p.45); 7 
(p.134-141) 
4.1 March 2015 Janice DiTore Section 3 (p.21); Section 5 (p.43), (p.54-59) 
5.0 April 2015 Janice DiTore Section 5 (p.46), 5 (p.52-53), 5 (p.55-58) 
5.1 May 2015 Janice DiTore Section 5 (p.52) 
5.2 August 2015 Janice DiTore Section 5 (p.52), (p.53-59) 
5.3  October 
2015 
Janice DiTore Section 5 (p.57) 
5.4 November 
2015 
Janice DiTore Section 5 (p.58) 
6.0 December 
2016 
Korosh Major Section 5 - Accrued Market Discount 
7.0 January 
2018 
Korosh Major Section 3 (NSCAIP); Section 4 (Contra Firm Type); Section 5 
(Transaction Type), (ALT Control Number), (Added Note) 
8.0 August 2019 Korosh Major • Setting up Inactive Records 
• Populating CBRS Records for ACATS Reclaim or Fail 
Reversal Transactions 
• Downloading and Viewing Cost Basis Files and Reports 
o Downloading Cost Basis Files 
o Viewing Cost Basis Files Using Microsoft Excel 
• CBRS Statistical Reports 
o Requesting CBRS Statistical Report Access 
o Accessing CBRS Statistical Reports from the CBRS 
Web Portal 

---

## Page 11

CBRS User Guide 
About This User Guide 11 
Version Date Author Notes – Sections Edited 
• List of CBRS Output File Identification Numbers 
• CBRS Output Files and Reports 
9.0 April 15, 
2020 
Casey Sorochen • Contact Us 
• Extension Guidelines 
9.1 January 6, 
2022 
Korosh Major System Reject Reason Field 
9.2 April 27, 
2023 
Korosh Major/Jackie Gude Enables firms to pass Mortgage-Backed Security (MBS) last 
factor and last factor date information using repurposed fields. 
See Last Factor. 
 
Getting Answers to Your CBRS Questions 
Use the following [[NSCC]] contacts for information about CBRS. You can also contact your [[DTCC]] Relationship 
Manager or obtain general assistance by visiting the [[DTCC]] Client Center. 
For… Contact… 
General questions and product support [[NSCC]] Support by email at NSCCSupport@[[DTCC]].com 
Setup and testing [[NSCC]] Integration by email at NSCCIntegration@[[DTCC]].com 
Issues with logging on to the system [[DTCC]] Client Support. Call the following number, and then follow 
the prompt for product support. 
• For US and Canada, call 1 888–382–2721. 
• For the UK, Europe, and Asia, call +1 212–855–8099. 
 

---

## Page 12

CBRS User Guide 
General Information 12 
2. GENERAL INFORMATION 
The Depository Trust & Clearing Corporation ([[DTCC]]) initially launched the Cost Basis Reporting Service 
(CBRS) in 2003 to enable firms to pass cost basis on assets transferred through the Automated Customer 
Account Transfer Service (ACATS). In October 2008, the United States Congress passed a law requiring firms 
to not only report cost basis information to investors and the U.S. Internal Revenue Service, but to also pass 
cost basis information between financial intermediaries when assets move from one firm to another.  
As a result, [[DTCC]] enhanced CBRS to help firms comply with this legislation. [[DTCC]] works with a cross 
functional committee with members from different segments of the industry: [[Broker]]-dealers, banks, transfer 
agents, mutual fund [[Companies]], and service bureaus to define the system’s functionality and record layouts. 
Since many different parties are affected by the legislation, [[DTCC]] seeks the input of these parties to make 
sure the system meets their cost basis passage needs. 
CBRS supports the passage of cost basis in many different types of [[Asset]] transfers, such as Depository Trust 
Company ([[DTC]]) deliver orders, [[DTC]] deposits and withdrawals, and ACATS/FundSERV and Networking 
transactions, in addition to supporting basis transfers for ACATS transfers as it did in the previous version of 
the system. System capabilities include enhanced functionality over the internet: firms can perform the same 
tasks through [[DTCC]] Web Portal that are available through the computer-to-computer connection.  
Scope of the System: Transfer of Information Only 
CBRS supports the transfer of cost basis information from one financial [[intermediary]] to another. CBRS does 
not tell users what transactions trigger the need to pass cost basis, or when to send the basis. CBRS does not 
provide any reconciliation capabilities between expected and received records. Also, CBRS does not calculate 
cost basis.  
[[BASIC]] Feature: Input 
CBRS has two input record types: [[Asset]] records and Tax Lot records. A firm submits an [[Asset]] record for each 
[[Asset]] for which it needs to pass cost basis information. The [[Asset]] record must have at least one, but can have 
many, associated Tax Lot records. Tax Lot records contain detailed cost basis information for each [[Asset]] 
record. There are four types of CBRS input records: original, corrected, firm reject, and request. [[Asset]] 
records can be any of the four types; tax lot records can only be original or corrected. 
CBRS receives the cost basis records from a computer-to-computer automated connection or through data 
input through the internet-based [[DTCC]] Web Portal.  
For the most part, the record types correspond to the deliverer and receiver of the security in the transaction 
that triggered the need to pass cost basis. The deliverer of the security submits an Original or Corrected 
record, and the receiver of the security submits a Firm Reject or a Request record, as needed. The one 
exception is the transfer of a [[short position]] (See Figure 2 for the information flow on the transfer of a short 
position). 

---

## Page 13

CBRS User Guide 
General Information 13 
The following figure shows how cost basis information flows through CBRS when the original transfer is the 
transfer of a long position:  
 
  
Deliverer 
of security 
Original [[Asset]] 
Record 
Original Tax Lot 
Record 
Corrected [[Asset]] 
Record 
Corrected Tax 
Lot Record 
Receiver 
of security 
Firm Reject 
[[Asset]] Record 
Request [[Asset]] 
Record 

---

## Page 14

CBRS User Guide 
General Information 14 
When a [[short position]] moves from one firm to another, the deliverer of the [[short position]] is the receiver of the 
security, and the receiver of the [[short position]] is the deliverer of the security. Also, the deliverer of the short 
position passes the cost basis to the receiver of the [[short position]].  The following figure shows the information 
flow of the transfer of cost basis for a [[short position]].
 
  
Deliverer of 
short 
position = 
Receiver of 
security 
Receiver of 
short 
position = 
Deliverer of 
security 
Original [[Asset]] 
Record 
Original Tax Lot 
Record 
Corrected [[Asset]] 
Record 
Corrected Tax 
Lot Record 
Firm Reject 
[[Asset]] Record 
Request [[Asset]] 
Record 

---

## Page 15

CBRS User Guide 
General Information 15 
Input Record Content Indicator Types 
CBRS input records have four different types: original, corrected, firm reject, and request. The [[Asset]] record 
includes all four types, and the Tax Lot record has only original and corrected record types.  
• Original [[Asset]] record/Original tax lot record: the primary record used to transfer the cost basis 
information. 
• Corrected [[Asset]] record/Corrected tax lot record: a submitter can use the corrected record type to tell 
the receiver the cost basis information has changed since the original record was sent. 
• Firm reject record ([[Asset]] level only): the receiver of the cost basis can use this type of record to let the 
submitter of the cost basis know that there is a problem with the information. The firm reject record is 
different from a system reject—a system reject occurs when some of the submitted information is rejected 
by the CBRS software. For example, if the submitter populates one of the date fields with 01/35/2012, 
CBRS will reject the record because a date of January 35, 2012 is not possible.  
• Request record ([[Asset]] level only): the [[Asset]] receiver can use this type of record to request cost basis 
from the [[Asset]] deliverer. 
The following table summarizes the relationship between the [[Asset]] deliverer and receiver for a long position 
and the CBRS record submitter and receiver. 
Record Content Type Record Submitter Record Receiver 
Original [[Asset]] deliverer [[Asset]] receiver 
Corrected [[Asset]] deliverer [[Asset]] receiver 
Firm reject [[Asset]] receiver [[Asset]] deliverer 
Request [[Asset]] receiver [[Asset]] deliverer 
Original [[Asset]] and Tax Lot Records Form a Package 
The [[Asset]] record and its corresponding Tax Lot records are a package. The Original and Corrected [[Asset]] 
data in the input file must consist of the [[Asset]] record followed by at least one Tax Lot record. CBRS rejects 
back to the submitter any [[Asset]] record not followed by a Tax Lot record(s). Tax Lot records that [[DO]] not follow 
an [[Asset]] record are assigned a separate Cost Basis Control Number and rejected by the system. The sum of 
the tax lot quantities must equal the quantity of the [[Asset]] record, or CBRS rejects the package. 
Package Rule Applies to Corrected Records 
A submitter must send all the tax lots for a corrected record, even if only one tax lot is corrected. For original 
and corrected records, the submitter must always send an [[Asset]] record with all its corresponding tax lot 
records. CBRS looks at the [[Asset]] and tax lot records as a package. If the package is not intact, CBRS rejects 
it. 
  

---

## Page 16

CBRS User Guide 
General Information 16 
Exceptions to Package Rule: Firm Reject and Request Records 
The Firm Reject and Request record content types exist only at the [[Asset]] level, not the tax lot level. For these 
two record content types, there are no corresponding tax lot records. 
Association of [[Asset]] and Tax Lot Records 
For all types of assets except options ([[Asset]] Category = OPT) and for all Transaction Types except 41 = 
Direct Presentation, CBRS establishes the association between the [[Asset]] and the Tax Lot record when the 
contents of these fields on the two records are equal: 
• Transfer Control Number 
• Contra Firm Number 
• Contra Firm Type 
• Submitting Firm Number 
• Submitting Firm Type 
• Receiver Customer Account Number 
• Deliverer Customer Account Number 
• ISIN Country Code 
• ISIN Security Issue [[ID]] 
• ISIN Security Check Digit 
For [[Option]] assets, CBRS establishes the association between the [[Asset]] and the Tax Lot record when the 
contents of these fields on the two records are equal: 
• Transfer Control Number 
• Contra Firm Number 
• Contra Firm Type 
• Submitting Firm Number 
• Submitting Firm Type 
• Receiver Customer Account Number 
• Deliverer Customer Account Number 
• Put/Call Indicator 
• [[Option]] Symbol 
• [[Option]] Expiration Date 
• [[Option]] Strike Price Integer 
• [[Option]] Strike Price Decimal  
  

---

## Page 17

CBRS User Guide 
General Information 17 
For Transaction Type 41 = Direct Presentation when the [[Asset]] is not an [[Option]], CBRS establishes the 
association between the [[Asset]] and the Tax Lot record when the contents of these fields on the two records are 
equal: 
• Transfer Control Number 
• Contra Firm Number 
• Contra Firm Type 
• Submitting Firm Number 
• Submitting Firm Type 
• Receiver Customer Account Number 
• Deliverer Customer Account Number 
• ISIN Country Code 
• ISIN Security Issue [[ID]] 
• ISIN Security Check Digit, unless ISIN Security Issue [[ID]] is blank. In this case, CBRS uses the [[Asset]] 
Description instead of the ISIN Country Code, ISIN Security Issue [[ID]], and ISIN Security Check Digit to 
associate the [[Asset]] and Tax Lot record. 
  

---

## Page 18

CBRS User Guide 
General Information 18 
[[BASIC]] Feature: Output 
CBRS edits the input data, runs an end-of-day batch process to validate, produce output files, and returns the 
validated data to the appropriate firms. CBRS takes the following steps to produce its output: 
• Four times a day, CBRS collects all the input files available at that time and runs a preliminary data edit 
process. During this cycle processing the system performs the following tasks: 
o Assigns a unique Cost Basis Control Number to each [[Asset]] and its tax lots 
o Validates that the contra firm is a valid CBRS user 
o Validates that the submitting firm is a valid CBRS user 
o Performs other [[BASIC]] validation of the input fields, such as editing of the input record length, and 
verifying that each field value contains valid and printable characters 
o Based on this validation, the system may preliminarily accept the records, reject them, or drop them  
• After 4:00 PM, CBRS runs an end-of-day batch process. Next, the system performs an in-depth edit of 
cost basis data received today by applying all established validation rules. 
• CBRS sends accepted cost basis records to the submitting and contra firm. 
• CBRS sends rejected cost basis records to the submitting firm only. 
Output Available Through Both Automated Connection and [[DTCC]] Web Portal 
Output files are available through both the automated computer-to-computer connection and/or through [[DTCC]] 
Web Portal. Regardless of how a submitter enters data into the system, the entire receiver’s data is in one file 
that is available for retrieval through either of the methods.  
Note 
The data is not automatically available through both methods. You must subscribe to either. 

---

## Page 19

CBRS User Guide 
Eligibility for CBRS 19 
3. ELIGIBILITY FOR CBRS 
This section describes the user and [[Asset]] eligibility for CBRS 
User Eligibility 
Each user that participates in CBRS is assigned a CBRS Account Number. [[DTCC]] will link existing [[DTC]], [[NSCC]] 
or [[transfer agent]] numbers to the CBRS account number. CBRS data submitted by or to an ineligible user is 
rejected.  
All financial intermediaries subject to the new IRS regulations are eligible to apply to use CBRS, including 
users who are not currently members of any service offered by one of [[DTCC]]’s affiliate [[Companies]]. 
Cost Basis User Master File 
To assist firms in identifying eligible users, the Cost Basis User Master File is available daily by 11 P.M. 
Eastern Time. This file lists eligible CBRS counterparties: by referring to this file before submitting a record, 
CBRS users can significantly reduce the number system rejects caused by cost basis records sent to ineligible 
counterparties. 
The record layout for the Cost Basis User Master File is located in the CBRS Technical Resources section of 
the [[DTCC]] Learning website. You must log in to access the file. 
The machine-readable output (MRO) file is a flat file. The [[DTCC]] Web Portal download file is a *.csv file. 
The Cost Basis User Master File has a CDTS header. It does not have a CBRS application header or CBRS 
application trailer. 
  

---

## Page 20

CBRS User Guide 
Eligibility for CBRS 20 
Cost Basis User Master File Record Layout Fields 
The following table shows the fields for the record layout for the Cost Basis User Master file. For more 
information about how to use the various fields in the User Master file, see Active/Inactive Feature. 
Field Description 
CBRS User Account Number Each user who signs up for CBRS is assigned a CBRS User Account Number. 
However, in most cases this is not the primary number that identifies a firm. The 
Active Firm Number, which corresponds to a firm’s [[DTC]] [[participant]] Number, [[NSCC]] 
[[participant]] Number, or [[transfer agent]] Number, is the number to use in the 
Receiving and Submitting Firm Number fields in CBRS data input and output. The 
only time the CBRS User Account Number is the primary identification number of a 
firm is when that firm is not a [[DTC]] [[participant]], nor an [[NSCC]] [[participant]], nor a 
[[transfer agent]].   
CBRS Account Name Contains the name of the user. 
Active Firm Number Number of the CBRS user who is the active user of the system (the user’s [[DTC]], 
[[NSCC]], or [[transfer agent]] (TA) number; or CBRS account number if the user does 
not have a [[DTC]], [[NSCC]], or TA number). 
This is the primary number that identifies 
the Receiving and Submitting Firms in CBRS data input and output (See 
Receiving and Submitting Firm Numbers). The Cost Basis Steering Committee, 
who advises [[DTCC]] on the design on the system, recommended that firms can use 
their existing [[DTC]] [[participant]], [[NSCC]] [[participant]], or [[transfer agent]] Numbers when 
processing data in CBRS. This number varies based on Active Firm Type: 
• When Active Firm Type is NSCPRT, this number is the [[NSCC]] [[participant]] 
Number 
• When Active Firm Type is DTCPRT, this number is the [[DTC]] [[participant]] Number 
• When Active Firm Type is AGTNBR, this number is the [[transfer agent]] Number 
• When Active Firm Type is CBRACT, this number is the CBRS User Account 
Number 
Active Firm Type: Type that corresponds to the Active Firm Number. Because there is some overlap 
between [[NSCC]] [[participant]] Numbers, [[DTC]] [[participant]] Numbers, and [[transfer agent]] 
Numbers, this file includes an Active Firm type so that the system can determine the 
type of number populated in the Active Firm Number field. Values: 
• AGTNBR = [[transfer agent]] 
• DTCPRT = [[DTC]] [[participant]] 
• NSCPRT = [[NSCC]] [[participant]] 
• CBRACT = CBRS-only user 
CBRS Account Start Date Date that the firm is eligible to participate in CBRS in the production environment. 
Exempt Recipient Accounts 
Indicator 
Allows CBRS users to indicate whether they want retirement accounts excluded from 
the basis they receive. This field contains the following two values: 
• Y:  Exclude retirement accounts from basis sent to this user 
• N:  [[DO]] not exclude retirement accounts from basis sent to this user. ‘N’ is the 
[[default]] value for this field.  
Search Firm Number Number of the CBRS user associated with the Active Firm Number. In most cases, 
this number is the same as the Active Firm Number. In the instances when an active 
CBRS user has assumed cost basis responsibility for a CBRS user who has become 
inactive, this number is the number of the inactive Firm (the inactive user’s [[DTC]], 

---

## Page 21

CBRS User Guide 
Eligibility for CBRS 21 
Field Description 
[[NSCC]], or [[transfer agent]] (TA) number; or CBRS account number if the user does 
not have a [[DTC]], [[NSCC]], or TA number).  
Search Firm Type Type that corresponds to the Search Firm Number. Values: 
• AGTNBR = [[transfer agent]] 
• DTCPRT = [[DTC]] [[participant]] 
• NSCPRT = [[NSCC]] [[participant]] 
• CBRACT = CBRS-only user 
• DTCOCC = [[DTC]] [[participant]] who is also an OCC [[Member]] 
• DTCFED = [[DTC]] [[participant]] who is also a FED [[Member]] 
• NSCAIP=AIP [[participant]] who is also a [[NSCC]] [[Member]] 
In the instances when an active CBRS user has assumed cost basis responsibility 
for another CBRS user who has become inactive, this type is the type of the inactive 
Firm. 
Active/Inactive Indicator Indicates whether the record corresponds to an active or inactive CBRS user.  
• If the user is active, a CBRS user can populate the Contra Firm Number and 
Contra Firm Type fields with either the Active Firm Number and Active Firm Type 
or the Search Firm Number and Search Firm Type.  
• If the user is inactive, a CBRS user must populate the Contra Firm Number and 
Contra Firm Type fields with the Active Firm Number and Active Firm Type. CBRS 
system rejects records sent to the Search Firm Number and Search Firm Type in 
this scenario. 
 
Active/Inactive Feature 
The CBRS User Master File’s active/inactive feature helps to reduce the manual processing that occurs when 
a user becomes ineligible for CBRS when its CBRS account closes as the result of events such as a merger or 
bankruptcy. 
When a user becomes ineligible for CBRS and another user assumes the ineligible user’s accounts, the 
active/inactive functionality allows an active CBRS user to indicate that it should receive CBRS records on 
behalf of an inactive user. This feature works where one user assumes complete responsibility for another 
user’s accounts. It does not work in the case where one user’s business goes to two or more users.  
A CBRS user can use the Search Firm Number/Type combination as the first place to look for the number of a 
CBRS contra party. Once a user locates the contra party’s number, that user looks to the Active/Inactive 
indicator. If the contra party is active, a user can send the CBRS record either to the Search Firm Number and 
Type combination, or to the Active Firm Number/Type combination. If the contra party is inactive, the user 
must send the CBRS record to the Active Firm Number/Type. 
For an active CBRS user, the value in the CBRS Account Effective Date field corresponds to the date the 
account becomes eligible for processing in the production environment. 
  

---

## Page 22

CBRS User Guide 
Eligibility for CBRS 22 
For an inactive CBRS user, the value in the CBRS Account Effective Date field corresponds to the first date 
that the inactive record is valid. For example, Firm A goes out of business, and Firm B assumes all of Firm A’s 
accounts. Because Firm A has gone out of business, it is removed from the CBRS User Master File. Once this 
new functionality is in place, Firm A can become an “Inactive” record, and Firm B is the associated “Active” 
record. For each inactive record, a contra party should send CBRS records to the active user. 
The following examples show the different scenarios that can occur in the new version of the Master File. In 
these examples, as for all CBRS users, type AGTNBR = [[transfer agent]] (TA), type DTCPRT = [[DTC]] [[participant]], 
type NSCPRT = [[NSCC]] [[participant]], and type CBRACT indicates a CBRS user who does not have a [[DTC]], 
NSCCPRT, or TA number, such as CBRS-only user. 
CBRS 
User 
Account 
Number 
CBRS 
Account 
Name 
Active 
Firm 
Number 
Active Firm 
Type 
CBRS 
Account 
Effective Date 
Exempt 
Recipient 
Accounts 
Search 
Firm 
Number 
Search 
Firm Type 
Active/ 
Inactive 
000ZZZZ1 Example 1 AAA DTCPRT 1/1/2011 N AAA DTCPRT A 
000ZZZZ2 Example 2 BBBB NSCPRT 1/2/2011 Y BBBB NSCPRT A 
000ZZZZ3 Example 3 CCCCC AGTNBR 1/3/2011 N CCCCC AGTNBR A 
000ZZZZ4 Example 4 DDDD DTCPRT 1/4/2011 N DDDD DTCPRT A 
000ZZZZ4 Example 4 DDDD DTCPRT 8/1/2012 N EEE DTCPRT I 
000ZZZZ5 Example 5 FFFF NSCPRT 1/5/2011 Y FFFF NSCPRT A 
000ZZZZ5 Example 5 FFFF NSCPRT 8/5/2012 Y YYYY1 CBRACT I 
000ZZZZ6 Example 6 ZZZZ6 CBRACT 1/6/2011 N ZZZZ6 CBRACT A 
000ZZZZ6 Example 6 ZZZZ6 CBRACT 8/6/2012 N XXXX2 CBRACT I 
000ZZZZ7 Example 7 ZZZZ7 CBRACT 1/7/2011 N ZZZZ7 CBRACT A 
000ZZZZ7 Example 7 ZZZZ7 CBRACT 8/7/2012 N GGG NSCPRT I 
000ZZZZ8 Example 8 HHHHH AGTNBR 1/8/2011 N HHHHH AGTNBR A 
000ZZZZ8 Example 8 HHHHH AGTNBR 8/8/2012 N JJJ AGTNBR I 
000ZZZZ9 Example 9 LLL NSCPRT 1/9/2011 N LLL NSCPRT A 
000ZZZZ9 Example 9 LLL NSCPRT 8/9/2012 N MMM NSCPRT I 
000ZZZZ9 Example 9 LLL NSCPRT 8/10/2012 N NNN NSCPRT I 
 
Examples 1 - 3 are CBRS users who [[DO]] not have a relationship with an inactive Firm Number. They are Active 
records only with no corresponding inactive records. The expectation is that most CBRS users will only have 
Active records. 
Example 4 is a CBRS user who is a [[DTC]] [[participant]], DDDD, who has assumed the cost basis responsibility for 
a retired CBRS user who is a [[DTC]] [[participant]], number EEE. DDDD is the active user, and ‘EEE’ is the inactive 
user. All CBRS records intended for EEE should be sent to DDDD. 

---

## Page 23

CBRS User Guide 
Eligibility for CBRS 23 
Example 5 is a CBRS user who is an [[NSCC]] [[participant]], FFFF, who has assumed the cost basis responsibility 
for a retired user who is a CBRS-only user, YYYY1. FFFF is the active user, and YYYY1 is the inactive user. 
All CBRS records intended for YYYY1 should be sent to FFFF. 
Example 6 is a CBRS-only user, ZZZZ6, who has assumed the cost basis responsibility for a retired user who 
is a CBRS-only user, XXXX2. ZZZZ6 is the active user, and XXXX2 is the inactive user. All CBRS records 
intended for XXXX2 should be sent to ZZZZ6. 
Example 7 is a CBRS-only user, ZZZZ7, who has assumed the cost basis responsibility for a retired user who 
is a [[NSCC]] [[participant]], GGG. ZZZZ7 is the active user, and GGG is the inactive user. All CBRS records 
intended for GGG should be sent to ZZZZ7. 
Example 8 is a CBRS user who is a [[transfer agent]], HHHHH, who has assumed the cost basis responsibility 
for a retired user who is a [[transfer agent]], JJJ. HHHHH is the active user, and JJJ is the inactive user. All 
CBRS records intended for JJJ should be sent to HHHHH. 
Example 9 is a CBRS user who is an [[NSCC]] [[participant]], LLL, who has assumed the cost basis responsibility 
for two [[NSCC]] participants—MMM and NNN. LLL is the active user, and MMM and NNN are the inactive users. 
All CBRS records intended for MMM or NNN should be sent to LLL. 
To set up an inactive record: 
The active [[Member]] must instruct [[DTCC]] to set up a new inactive record, for example Alternative Account. 
Active users should review the instructions about setting up an inactive record. See CBRS New and Existing 
Account Instructions available in the New Accounts, Instructions and Forms section at: 
http://www.[[DTCC]].com/clearing-services/equities-clearing-services/cbrs/client-center/public-documents.aspx  
By [[default]], an inactive record expires 18 months after it is set up, unless the [[Member]] specifies an end 
date. In its instructions to [[DTCC]], an active user can request the inactive record to remain on the Master File for 
a longer amount of time, if necessary. 
Note  
The account numbers in the User Master file output have leading zeroes. 
Q If a fund has a Y in the Exempt Recipient Accounts Indicator, which means the fund does not 
want to receive basis for retirement accounts, but a firm sends a record with basis for a 
retirement account to the fund, does CBRS pass system reject the record back to the firm?   
A CBRS does not reject a record in this scenario. CBRS does not have any system edits based on the 
Exempt Recipient Accounts Indicator. In the case described in this question, CBRS passes the record to 
the fund. 
Q If I send a CBRS record to an inactive user, what will happen?   
A CBRS system rejects a record sent to a user designated as Inactive on the CBRS User Master File.  
Q What System Reject Reason does CBRS use in this case?  

---

## Page 24

CBRS User Guide 
Eligibility for CBRS 24 
A From the Transaction Machine Readable Output (MRO), CBRS populates the System Reject Reason 
field with the value 01 = Invalid Field and populates the AO Contra Firm Number Status field with the 
value   2 = Error. The combination of these values indicates that the submitter has populated a field with 
an invalid value, and the status field indicates which field contains the invalid value (in this case, the 
Contra Firm Number on the [[Asset]] record). 
Q Is it possible for a CBRS only user to be the active user for an inactive [[NSCC]], [[DTC]], or TA 
number?   
A The CBRS User Master File has been designed to allow an active CBRS only user (type CBRACT) to 
have corresponding inactive records that are [[NSCC]] participants, [[DTC]] participants, or Transfer Agents 
(types NSCPRT, DTCPRT, and AGTNBR, respectively).  
N
ote: 
The type CBRACT is a receiver on a limited number of Transaction Types, so a CBRS only user may not be able to 
receive a record sent to it on behalf of the inactive [[DTC]], [[NSCC]], or TA number. 
Q I only know the OCC number of my contra. How [[DO]] I find the CBRS active user number? 
A The CBRS User Master file has been designed to allow an active CBRS user to have corresponding 
inactive record user identifiers for their OCC account numbers. Use the Search Firm Type DTCOCC to 
find the active CBRS user number. 
Q I only know the FED number and short name combination of my contra. How [[DO]] I find the CBRS 
active user number? 
A The CBRS User Master File has been designed to allow an active CBRS user to have corresponding 
inactive record user identifiers for their FED account number and associated short names. Use the 
Search Firm Type, DTCFED, to find the active CBRS user number. 
Q I’m looking for a CBRS user who was on the CBRS User Master file last week, but they are not 
there today. What happened? How can I send cost basis to this user?  
A If a user is no longer on the CBRS User Master file, they are ineligible to send and receive records 
through CBRS. A variety of things could have happened; maybe the firm went out of business or merged 
with another firm. If the contra firm or fund is not on the CBRS User Master File, you cannot send CBRS 
records to them: you need to send cost basis through an alternate, manual method. 
  

---

## Page 25

CBRS User Guide 
Eligibility for CBRS 25 
Receiving and Submitting Firm Numbers 
Notes  
If a firm has a [[DTC]] [[participant]] Number, [[NSCC]] [[participant]] Number, or a [[transfer agent]] Number, that number is the 
number to use in the Submitting or Contra Firm Number field in CBRS. If a firm has none of the numbers above, the CBRS 
User Account Number is the number to use in the Submitting or Contra Firm Number field. 
Each firm that participates in CBRS is assigned a CBRS User Account Number. As mentioned earlier, for most 
users the CBRS User Account Number is not the primary number used to identify the firm in CBRS data input 
and output. As applicable, the CBRS User Account Number is related to an existing [[DTC]] [[participant]] Number, 
[[NSCC]] [[participant]] Number, or [[transfer agent]] Number based on the logic below. This relationship allows users 
to identify themselves and other firms using numbers with which they are already familiar.  
The Contra and Submitting Firm Number must follow the following logic: 
• A user who is a [[DTC]] [[participant]] uses its [[DTC]] [[participant]] Number. 
• A user who is an [[NSCC]] [[participant]] uses its [[NSCC]] [[participant]] Number. 
• A user who is both a [[DTC]] [[participant]] and [[NSCC]] [[participant]] uses its [[DTC]] [[participant]] Number. 
• An [[Equity]] [[transfer agent]]/[[issuer]] who has a [[transfer agent]] Number uses this number. 
• All other firms use their CBRS User Account Number. 
 
While the CBRS User Account Number is not often the number used to identify the firm as a submitter and 
receiver of CBRS records, users are advised to make a note of their CBRS User Account Number to 
communicate with [[DTCC]] about system and billing inquiries. 
 
Q If a user has a [[DTC]] number or [[transfer agent]] number, can I send records to it using its CBRS 
number?  
A No. For users who have [[DTC]] or [[transfer agent]] (TA) numbers, you must send basis to the [[DTC]] or TA 
number and the appropriate firm type. 
Q Some transfer agents (TAs) have multiple TA numbers. If I am sending a CBRS record to a TA, 
does the TA number must be the specific TA number assigned to that ISIN Security Issue [[ID]] 
([[CUSIP]])?  
A No. For CBRS records to or from a [[transfer agent]], CBRS does not check that the Submitting or Contra 
Firm Number is the correct TA number for the [[CUSIP]] on the record.  
While CBRS does not perform an edit between the TA number and the [[CUSIP]] number, it does on some 
occasions populate the TA number in the Contra Firm Number field based on the [[CUSIP]]. For Original and 
Corrected records where a TA is the receiver (Transaction Types 36 = [[DWAC]] Withdrawal and 37 = Withdrawal 
by Transfer (WT)), and Firm Reject and Request records where a TA is the receiver (Transaction Types 26 = 
[[DWAC]] Deposit, 27 = Certificate Deposit, and 28 = [[DRS]] Profile/[[DO]]), CBRS automatically populates the Contra 
Firm Number field with the number for the [[transfer agent]] who corresponds to the ISIN Security Issue [[ID]] 
([[CUSIP]]) number on the record.  

---

## Page 26

CBRS User Guide 
Eligibility for CBRS 26 
If this [[transfer agent]] number is eligible for CBRS, CBRS passes the record to the agent (assuming the record 
passes all other system rules and edits). If the [[transfer agent]] number is not eligible for CBRS, CBRS populates 
the number on the output back to the submitting [[Broker]]-dealer, so the [[Broker]] knows where to send the cost 
basis using some other method. 
Q I work at a [[Broker]]-dealer and have had some rejects in CBRS records that I’ve sent to a transfer 
agent (TA) who I know is eligible for CBRS. Why are these rejects happening?   
A Some TAs have multiple TA numbers. There are some cases where not all TA numbers for a given TA 
are eligible for CBRS. For example, a TA has three numbers: 12345, 23456, and 34567. The TA has 
made numbers 12345 and 23456 eligible for CBRS, but not 34567. A [[Broker]]-dealer sends a request 
record for cost basis on a deposit on [[CUSIP]] 123456789. The [[Broker]]-dealer populates the ISIN Security 
Issue [[ID]] ([[CUSIP]]) field with 123456789, which happens to correspond to TA number 34567. CBRS 
automatically populates the Contra Firm Number field with TA number 34567, and then rejects the record 
because 34567 is not eligible for CBRS—even though the same TA has two other numbers that are 
CBRS eligible. Best Practices suggest that TAs should make all their TA numbers eligible for CBRS, to 
prevent this system reject. 
[[Asset]] Eligibility 
All assets are eligible for the submission of cost basis information. CBRS supports the passage of cost basis 
on both covered and noncovered [[securities]]. The Tax Lot Input record includes a Noncovered/Pending Indicator 
field that the submitter can use to indicate that a lot is noncovered.  
Note: 
If the Noncovered/Pending indicator is left blank, the lot is considered covered. 

---

## Page 27

CBRS User Guide 
Application Input and Output 27 
4. APPLICATION INPUT AND OUTPUT 
The following information relates to input and output timing: 
• Input: for today’s processing date, firms can submit CBRS records between 8 P.M. Eastern Time 
yesterday (the previous processing day) and 4 P.M. Eastern Time today.  
o Files submitted between 8 P.M. Eastern Time yesterday and 4 P.M. Eastern Time today should have 
today’s date in the header 
o Files with today’s header date, submitted between 4 PM and 8 PM today, are processed with 
tomorrow’s processing date 
o Files with tomorrow’s header date, submitted between 4 PM and 8 PM today, are rejected by CDTS. 
• Output: for today’s processing date, CBRS transaction output and the Daily Deposit File for Transfer 
Agents is available by 9 P.M. Eastern Time today. The Cost Basis User Master File is available by 11 
P.M. Eastern Time today. 
Note: 
This schedule applies to input and output through both the automated computer-to-computer connection and through 
[[DTCC]] Web Portal. 
General Record Layout Information 
The CBRS record layouts, both input and output, are located in the CBRS Technical Resources section of the 
[[DTCC]] Learning website. You must login to access the file. 
The following table shows the column headings for the record layouts: 
Heading Definition 
Field Name The name of the field 
Length The length of the field, in bytes 
Start The position where the field starts 
End The position where the field ends 
Type The type of the field: 
• A/N = Alphanumeric • NUM = Numeric 
 
Opt/Req/Cond Indicator that specifies whether the field is optional, required, or conditionally required: 
• OPT = optional field • REQ = required field 
• COND = conditionally required, depending upon values in other fields 
 
Comments A brief field description, possibly including format, valid values, conditional requirements, general 
use rules, and/or best practices 
 
  

---

## Page 28

CBRS User Guide 
Application Input and Output 28 
Notes about the record layouts: 
• All input fields must contain printable and allowed characters; otherwise CBRS will overlay the input with 
asterisks, ‘*’, and reject the record. The CBRS printable and allowed characters are all lower/upper case 
letters and numbers, and certain symbols. 
• Alphanumeric fields may contain any character in the EBCDIC computer character set except for 
unprintable characters such as Low-Value, High-Value, COMP-3 fields, etc. See Appendix B for the list of 
valid characters for CBRS. 
• Numeric fields include only digits (0-9). 
• When a field is required: 
o If a list of values is provided, the field must contain a value from that list 
o An alphanumeric field without a specified list of possible values may have any alphanumeric value, 
except spaces 
o A numeric field without a specified list of possible values may contain any digit except zero (0)  
• When a field is optional: 
o An alphanumeric field with a specific list of possible values must have one of those values or blank 
o An alphanumeric without a specific list of possible values may have any value including spaces 
o A numeric field without a specific list of possible values may contain numeric digits (0-9) or spaces 
• All dates in the layouts have the format CCYYMMDD (except where otherwise indicated), where: 
o CC = Century 
o YY = Year 
o MM = Month 
o DD = Day  
For example, December 31, 2011 is 20111231 in CBRS format. 
The Quantity fields support up to four decimal places. Decimals greater than four places in the quantity fields 
are truncated. 
Notes  
The position of the decimal point can float. The record layouts state: "Position of decimal denoted by a ',' (comma). Up to 
four decimal places will be supported before truncation occurs."   
The following list shows examples of how the share quantity fields can look on the CBRS output file: 
• 000000000001234,5 
• 00000000001234,56 
• 0000000001234,567 
• 000000001234,5678 
The Cost fields support up to two decimal places. Decimals greater than two places in the cost fields are 
truncated. 
  

---

## Page 29

CBRS User Guide 
Application Input and Output 29 
Filler Fields 
Filler fields are required because the filler tells the system the position of the fields in the record. Also, when 
fields are marked as “optional,” this means that the value in the field is optional, but the submitter is required to 
provide spaces in place of the value to keep the position of the other fields in the correct place. The filler at the 
end of the record is required as well: the filler at the end of the record layout extends the length of the record to 
the required 1,000 bytes. A submitted record that is more or less than 1,000 bytes in length is rejected by the 
system. 
Q When [[DTCC]] removes a field from the CBRS record layouts and turn it into filler, what happens if 
a submitter populates this field? 
A After a field has been removed from the record layouts, and turned into a filler field, the CBRS 
application does not look at this field. The data populated in this field by the submitter is not included in 
the CBRS output. [[DTCC]] recommends that the submitter space out these bytes: a submitter who does 
not space out these bytes may encounter a problem in the future if the bytes are reused for a different 
field.  
Using CBRS for Cost Basis Information in Non-US Currency 
All cost fields in CBRS are denominated in US Dollars only. However, on the Tax Lot level, there are two 
fields—ISO Currency Code and Exchange Rate—that allow a submitter to tell the receiver that the submitter 
held the cost basis on its system in a different currency, and they converted the cost basis to US Dollars to 
transfer it. 
When transferring basis for a lot purchased in a foreign currency, note the following: 
• For lots whose acquisition date has been adjusted as the result of a wash sale, the exchange rate should 
be the rate as of the date in the “Original Acquisition Date for Wash Sale Adjustment” field.  
• The exchange rate is the rate that the delivering firm captured on the date the security was purchased. 
The currency that the trade settled in is the currency that the cost basis should be recorded in. 
• The deliverer provides the exchange rate so that the receiver can calculate the gain/loss in the currency 
separately from the gain/loss in the security. 
 
 

---

## Page 30

CBRS User Guide 
Application Input and Output 30 
Input General Information 
This section explains the general input information. 
Transfer Control Number 
You must enter a Transfer Control Number for each CBRS transaction submitted to the system. This Transfer 
Control Number should be the same as the control number used to identify the [[Asset]] transfer that triggered the 
need to pass cost basis. All cost basis output includes this Transfer Control Number for reference. CBRS 
rejects any cost basis record that does not have a Transfer Control Number. 
Note:  
In the [[Asset]] Input and Tax Lot Input records, the value in the Transfer Control Number field is left justified.  
Q If the transfer control number has less than 30 bytes, does the submitter must follow the transfer 
control number with spaces or zeros?   
A CBRS accepts either one. 
Q For some CBRS transaction types, I should use the IMS TID number as the Transfer Control 
Number. I know this number is available on the DTFPART file, but is there a way to manually look 
up the IMS TID number?   
A You can look up a [[DTC]] transaction’s IMS TID number through the ART function in [[PBS]]. Begin by 
selecting a transaction. After you click on the transaction, the following figure appears. The IMS TID is 
located at the bottom of the Activity Details section. The IMS TID is not available in [[PTS]]. 
 
Figure 1. Activity Details 


---

## Page 31

CBRS User Guide 
Application Input and Output 31 
For Transaction Type 01 = ACATS, the Transfer Control Number should be populated with the 14-byte ACATS 
control number from the original transfer. However, the ACATS Control Number that we receive in positions 
683-702 on the Fund/SERV 018 record (an ACATS Transfer) is 20 bytes.  
Q Should I truncate the field down to 14 bytes? How [[DO]] I know what the ACATS Control Number is?   
A The first fourteen bytes of the ACATS Control Number on the Fund/SERV record are the ACATS Control 
Number. The last six bytes are the ACATS [[Asset]] Sequence Number, which is used to identify that 
mutual fund [[Asset]] in the ACATS transfer. 
Notes about populating the Transfer Control Number for [[transfer agent]] Transactions: 
• For deposit Transaction Type 27 = Certificate Deposit, a [[transfer agent]] can choose to receive the CBRS Daily 
Deposit File. The Transfer Control Number is the Reference [[ID]], ARF, or CID number that was submitted on the 
original deposit. 
• For deposit Transaction Type 26 = [[DWAC]] Deposit, use the 26-byte Reference [[ID]] that you see on [[CDWC]] as the 
CBRS Transfer Control Number. 
• For Transaction Type 37 = Withdrawal by Transfer (WT), use the first 30 bytes of the 37-byte reference number 
on the RSATFX file (for [[FAST]]) or on the upper right had corner of the Transfer Assignment Control Form (TACF) 
(for non-[[FAST]]). 
• For Transaction Type 28 = [[DRS]] Profile/[[DO]], use the first 30 characters of the customer account number received 
through the DRSPRO file. 
Firm Reject Record 
A firm sends a Firm Reject record when, for various reasons, the firm cannot apply the received cost basis to 
its books. This situation is different from a system reject. A system reject occurs when the CBRS system 
rejects a record because it does not comply with the system’s rules, such as when a date field has a value of 
1/35/2012, which is not a valid calendar date.  
Information flow for a firm reject record: 
1. You receive a CBRS record that you cannot apply to your books.  
2. Submit an [[Asset]] record, with the value 03 = Firm reject record in the Record Content Indicator field. 
3. At this point the receiver of the firm reject record decides whether to respond. CBRS does not require 
a response to a firm reject. If the receiver of the reject chooses to respond, the information flow 
continues with step 3. 
4. To correct the error, the receiver of the reject responds with an [[Asset]] record with the value 02 = 
Corrected [[Asset]] record in the Record Content Indicator field, and its corresponding tax lots. At least 
one of these tax lots must also be corrected (value 02 = Corrected tax lot record in the Record Content 
Indicator field). 
  

---

## Page 32

CBRS User Guide 
Application Input and Output 32 
Firm Number and Type Versus Customer Account Number Fields 
The Submitting Firm Number and Submitting Firm Type fields should always correspond to the user sending 
the CBRS record. The Receiving Firm Number and Receiving Firm Type should always correspond to the user 
receiving the CBRS record. The Deliverer Customer Account Number should always correspond to the user 
who delivered the [[Asset]] transfer, and the Receiver Customer Account Number should always correspond to 
the user who received the [[Asset]] transfer. Another way to think of it is the Deliverer Customer Account Number 
corresponds to the user who is delivering the cost basis, and the Receiver Customer Account Number 
corresponds to the user who is receiving the cost basis. 
Notes for the transfer of a [[short position]]:  
The Deliverer Customer Account Number is the account from which the [[short position]] is being transferred.  
The Receiver Customer Account Number is the account that is adding the [[short position]] to its books and is thus 
receiving the Proceeds as required by the regulations. Therefore, in this context, the fields deliverer and receiver account 
numbers correspond to the account delivering and receiving the [[short position]], not the account delivering or receiving the 
long [[shares]]. 
This example shows how an original record is sent after the transfer of a long position. Scenario: customer’s 
long position is transferred from Firm A to Firm B.  
1. Firm A delivers [[shares]] to Firm B. 
2. Firm B establishes the customer’s long position on its books.  
3. Firm A sends cost basis to firm B (Original [[Asset]] and tax lot(s) records). 
This example shows how a request record, followed by an original record, are sent after the transfer of a short 
position. Scenario: customer’s [[short position]] is transferred from Firm A to Firm B. 
1. Firm B delivers [[shares]] to Firm A. 
2. Firm B establishes the customer’s [[short position]] on its books. 
3. Firm A accepts the [[shares]]. 
4. Firm B sends Firm A the borrow Request record (a Request [[Asset]] record with the value of B = Borrowed 
in the Position Code field). 
5. In response to the borrow request record, Firm A should send the proceeds to Firm B (Original [[Asset]] and 
Tax Lots records). 
You can send through CBRS the following types of records: 
• Original record – used to initially send cost basis to the contra-firm 
• Corrected record – used to send corrected basis when previously sent basis is deemed to be incorrect 
• Firm Reject record – used in cases where the contra-firm receives basis for which it cannot match to a 
received [[Asset]] 
• Request record – used to request basis if it was not received on an [[Asset]] transfer within 15 days or as a 
borrow request for long [[shares]] delivered to cover the transfer of a [[short position]] 
  

---

## Page 33

CBRS User Guide 
Application Input and Output 33 
The following table shows how these fields should be filled out for each record type. This table applies to both 
long and short positions. 
Record Type Submitting 
Firm Number 
Submitting 
Firm Type 
Contra Firm 
Number 
Contra Firm 
Type 
Deliverer 
Customer 
Account 
Number 
Receiver 
Customer 
Account 
Number 
Original  Firm A Firm A Firm B Firm B Firm A Firm B 
Corrected Firm A Firm A Firm B Firm B Firm A Firm B 
Firm Reject Firm B Firm B Firm A Firm A Firm A Firm B 
Request Firm B Firm B Firm A Firm A Firm A Firm B 
Contra Firm Number 
For Original and Corrected records where an [[issuer]]/[[Equity]] [[transfer agent]] (TA) is the receiver (Transaction 
Types 36 = [[DWAC]] Withdrawal and 37 = Withdrawal by Transfer (WT)), and Firm Reject and Request records 
where a TA is the receiver (Transaction Types 26 = [[DWAC]] Deposit, 27 = Certificate Deposit, and 28 = [[DRS]] 
Profile/[[DO]]), CBRS automatically populates the Contra Firm Number field with the number for the [[transfer agent]] 
who corresponds to the ISIN Security Issue [[ID]] ([[CUSIP]]) number on the record. If this [[transfer agent]] number is 
eligible for CBRS, CBRS passes the record to the agent (assuming the record passes all other system rules 
and edits). If the [[transfer agent]] number is not eligible for CBRS, CBRS populates the number on the output 
back to the submitting [[Broker]]-dealer, so the [[Broker]] knows where to send the cost basis using some other 
method. 
Q If a [[Broker]]-dealer has received a deposit from a [[transfer agent]], does CBRS automatically solicit 
the cost basis information from the [[transfer agent]]? 
A No, CBRS does not automatically solicit the cost basis information. Instead, when the [[Broker]]-dealer 
sends the [[transfer agent]] a request [[Asset]] record for the cost basis on the deposit, CBRS follows the 
process described. 
Contra Firm Type 
CBRS needs the Submitting and Contra Firm Type fields because of the occasional overlap between [[DTC]], 
[[NSCC]], and [[transfer agent]] numbers. For firms to use their existing [[participant]] numbers, and not a CBRS 
Account Number, as an identifier in CBRS input and output records, the CBRS application needs the Firm 
Type to be able to properly identify the submitting and contra users where an overlap exists. The following 
tables clarifies the relationship between the Contra Firm Type and the various Transaction Types. These rules 
are in the input record layouts. 
  

---

## Page 34

CBRS User Guide 
Application Input and Output 34 
For the Original and Corrected Records: 
If the Transaction Type is… Contra Firm Type must be… 
01 = ACATS DTCPRT; NSCPRT; CBRACT 
02 = Free [[DTC]] Deliver Order (non-ACATS) DTCPRT; NSCPRT; CBRACT 
03 = Valued [[DTC]] Deliver Order DTCPRT; NSCPRT; CBRACT 
04 = Conversion DTCPRT; NSCPRT; CBRACT 
05 = Mutual Fund Transfer (non-ACATS) [change of [[Broker]]-dealer] DTCPRT; NSCPRT; CBRACT 
06 = FED  DTCPRT; NSCPRT; CBRACT 
07 = Physical Movement [[settlement]] DTCPRT; NSCPRT; CBRACT 
08 = OCC Transfer (non-ACATS) DTCPRT; NSCPRT; CBRACT 
09 = Non-Domestic Depository (Foreign) DTCPRT; NSCPRT; CBRACT 
10 = Other DTCPRT; NSCPRT; CBRACT 
26 = [[DWAC]] Deposit DTCPRT 
27 = Certificate Deposit DTCPRT 
28 = [[DRS]] Profile/[[DO]] DTCPRT 
36 = [[DWAC]] Withdrawal AGTNBR 
37 = Withdrawal by Transfer (WT) AGTNBR 
41 = Direct Presentation AGTNBR; CBRACT; DTCPRT 
46 = Fund to Firm Mutual Fund Transfer DTCPRT; NSCPRT 
51 = Firm to Fund Mutual Fund Transfer DTCPRT; NSCPRT 
56 = Networking Transaction DTCPRT; NSCPRT 
57 = Manual Mutual Fund Transfer CBRACT; DTCPRT; NSCPRT 
58= AIP DTCPRT; NSCPRT; CBRACT 
59= Alternative Investment (Non-AIP) DTCPRT; NSCPRT; CBRACT 
 
  

---

## Page 35

CBRS User Guide 
Application Input and Output 35 
For the Firm Reject and Request Records: 
If the Transaction Type is… Contra Firm Type must be… 
01 = ACATS DTCPRT; NSCPRT; CBRACT 
02 = Free [[DTC]] Deliver Order (non-ACATS) DTCPRT; NSCPRT; CBRACT 
03 = Valued [[DTC]] Deliver Order DTCPRT; NSCPRT; CBRACT 
04 = Conversion DTCPRT; NSCPRT; CBRACT 
05 = Mutual Fund Transfer (non-ACATS) [change of [[Broker]]-dealer] DTCPRT; NSCPRT; CBRACT 
06 = FED (non-ACATS) DTCPRT; NSCPRT; CBRACT 
07 = Physical Movement [[settlement]] DTCPRT; NSCPRT; CBRACT 
08 = OCC Transfer (non-ACATS) DTCPRT; NSCPRT; CBRACT 
09 = Non-Domestic Depository (Foreign) DTCPRT; NSCPRT; CBRACT 
10 = Other DTCPRT; NSCPRT; CBRACT 
26 = [[DWAC]] Deposit AGTNBR; DTCPRT; NSCPRT; CBRACT 
27 = Certificate Deposit AGTNBR; DTCPRT; NSCPRT; CBRACT 
28 = [[DRS]] Profile/[[DO]] AGTNBR; DTCPRT; NSCPRT; CBRACT 
36 = [[DWAC]] Withdrawal DTCPR; NSCPRT; CBRACT 
37 = Withdrawal by Transfer (WT) DTCPRT; NSCPRT; CBRACT 
41 = Direct Presentation AGTNBR; CBRACT; DTCPRT 
46 = Fund to Firm Mutual Fund Transfer DTCPRT; NSCPRT 
51 = Firm to Fund Mutual Fund Transfer DTCPRT; NSCPRT 
56 = Networking Transaction DTCPRT; NSCPRT 
57 = Manual Mutual Fund Transfer CBRACT; DTCPRT; NSCPRT 
58= AIP DTCPRT; NSCPRT; CBRACT 
59= Alternative Investment (Non-AIP) DTCPRT; NSCPRT; CBRACT 
 
  

---

## Page 36

CBRS User Guide 
Application Input and Output 36 
Transaction Types 
The comments in the record layouts explain the roles of the submitter and contra firms by dividing the 
transaction types into the following categories: 
• Firm to Firm: 
01 = ACATS  
02 = Free [[DTC]] Deliver Order (Non-ACATS) 
03 = Valued [[DTC]] Deliver Order 
04 = Conversion 
05 = Mutual Fund Transfer (Non-ACATS) [change of [[Broker]]-dealer] 
06 = FED (Non-ACATS) 
07 = Physical Movement [[settlement]] (Non-ACATS) 
08 = OCC Transfer (non-ACATS) 
09 = Non-Domestic Depository (Foreign) 
10 = Other 
• Firm & [[transfer agent]]: 
o Agent submits/firm receives CBRS original/corrected record: 
26 = [[DWAC]] Deposit 
27 = Certificate Deposit 
28 = [[DRS]] Profile/[[DO]] 
o Firm submits/agent receives CBRS original/corrected record: 
36 = [[DWAC]] Withdrawal 
37 = Withdrawal by Transfer (WT) 
o Either the Agent submits/firm or Firm submits/agent receives the CBRS original/corrected record: 
41 = Direct Presentation 
• Firm & Fund (In-kind Mutual Fund Transfers): 
o Fund submits/firm receives CBRS original/corrected record: 
46 = Fund to Firm Mutual Fund Transfer [through ACATS Fund/SERV interface; also known as PTF, 
Position Transfer Fund ACATS transfer type] 
o Firm submits/fund receives CBRS original/corrected record: 
51 = Firm to Fund Mutual Fund Transfer [through ACATS Fund/SERV interface; also known as PTF, 
Position Transfer Fund ACATS transfer type] 
o Either the fund submits/firm or firm submits/fund receives the CBRS original/corrected record: 
56 = Networking Transaction 
58= AIP (Alternative Investment Product) 
59=Alternative Investment (Non-AIP) 
  

---

## Page 37

CBRS User Guide 
Application Input and Output 37 
Q In the case when an [[Equity]] [[transfer agent]]/[[issuer]] is either the submitter or receiver of CBRS 
records, does the system verify that Submitting or Contra Firm Type and Number is the right 
[[transfer agent]] for that [[CUSIP]], or just verify that the firm is an eligible CBRS User?   
A CBRS checks that the [[transfer agent]] is an eligible CBRS user; it does not confirm that the Firm Number 
is the correct number for the [[CUSIP]] in that record. However, CBRS does populate the Contra Firm 
Number in most cases when a [[transfer agent]] is the receiver. See the [[Asset]] and Tax Lot Input record 
layouts in the CBRS Technical Resources section for the rules for when CBRS populates the Contra 
Firm Number. 
Numeric Fields 
Q In numeric fields, [[DO]] I have to zero fill all the bytes before the actual number?  For example, in the 
Total Position Quantity field, if I send an [[Asset]] record for 45.53 [[shares]] should I send 
‘00000000000045,53’ or can I send spaces instead of zeroes?   
A You can send either one. You can send 45,53 and CBRS adds leading zeroes; or you can send 
00000000000045,53. 
[[Asset]] Category Field 
Q Should the value in the [[Asset]] Category field be left justified with a space to the right if it is a 
three-letter code? In other words, the field is four bytes long, but for [[Asset]] Category EQU, should 
the EQU be left justified with a space after the value or right justified with a space before the 
value?   
A The three-letter value should be left justified, otherwise CBRS rejects the record. For EQU, the submitter 
should populate the [[Asset]] Category field with ‘EQU_’ where the underscore represents a space. 
Sum of the Tax Lot Quantities Must Match the [[Asset]] Quantity 
As discussed in an earlier section, an [[Asset]] record and its corresponding Tax Lot record(s) are a package. The 
sum of the tax lot quantities must equal the quantity of the corresponding [[Asset]] record, or CBRS rejects the 
package. 
CBRS sums the tax lot quantities and compares this sum to the value in the Total Position Quantity field in 
the associated [[Asset]] record. When calculating the total tax lot quantity, CBRS adds the quantity of each long 
tax lot (value L = Long in the Position Code field) and subtracts the quantity of each short tax lot (value S = 
Short in the Position Code field).  
The number in the Total Position Quantity field on the [[Asset]] record is positive when the value in the [[Asset]] 
record’s Position Code field is L = Long. The number in the Total Position Quantity field on the [[Asset]] record 
is negative when the value in the [[Asset]] record’s Position Code field is S = Short.  
CBRS compares the Total Position Quantity on the [[Asset]] record to the sum of the values in the Tax Lot 
Quantity fields for the corresponding tax lot records, and then rejects the record if the quantities [[DO]] not match.  

---

## Page 38

CBRS User Guide 
Application Input and Output 38 
Optional Fields 
Q If an optional field is not filled in on the [[Asset]] or tax lot input, what will be in that field on the 
transaction output?   
A The quantity and price fields will have zeros in them, other fields will be blank. 
Borrowed Position Code 
The value Borrowed is only valid for a request record (Record Content Indicator = 04). This is a rare situation 
that can occur when a [[short position]] is delivered outside of a standard ACATS transfer. The following figure 
shows the information flow when a Borrowed value is used. 
 
Figure 2. Information Flow with a Borrowed Position Code 
In step 4, when the Blue firm sends the proceeds of the short to the Yellow firm, he/she can use either the Tax 
Lot Current Cost field or the Tax Lot Original Cost field, depending on the type of [[Asset]]. The Tax Lot Input 
record layout lists the rules for which cost field should be used for which [[Asset]] Category type. 
  


---

## Page 39

CBRS User Guide 
Application Input and Output 39 
ACATS [[Asset]] Sequence Number 
CBRS includes the ACATS [[Asset]] Sequence Number on the [[Asset]] Input record layout because of industry 
discussions about how to match cost basis to an [[Asset]] transferred through ACATS which is identified by a User 
[[CUSIP]]. A submitter and receiver may use a different User [[CUSIP]] to identify an [[Asset]], such as a restricted 
security. The ACATS [[Asset]] Sequence Number is another data element to help the receiver match an [[Asset]] 
transferred through ACATS to the cost basis received through CBRS.  
The date 07/26/2012 in the rule in this field is based on the day before this field was added to the CBRS code 
in the Production environment. The ACATS [[Asset]] Sequence Number is not required for ACATS transfers 
whose ‘Date Transfer was Initiated’ or ‘[[settlement]] Date of Transfer’ occurred before the field was available in 
Production because some CBRS users may not have stored this number in the past. 
Q What happens if I populate the ACATS [[Asset]] Sequence Number field for a transfer whose 
[[settlement]] date is before 7/26/2012?   
A If you populate the ACATS [[Asset]] Sequence Number for a transfer whose [[settlement]] date is before 
7/26/2012, CBRS validates that the field is a six-byte numeric field. If the value in the field passes that 
validation (and there are no other problems with the record), CBRS passes the record to the receiver. If 
the value in the field does not pass the validation, CBRS system rejects the record. 
Q What should I populate in the ACATS [[Asset]] Sequence Number field for transaction types other 
than 01 = ACATS?   
A For transaction types other than 01 = ACATS, the submitter leaves this field blank. If you populate this 
field for a transaction type other than 01 = ACATS, CBRS spaced out the field and passes the record. 
Output General Information 
Firms receive a variable length Transaction Machine Readable Output (MRO) file through CDTS (Output 
Product [[ID]] #02400264). A download of CBRS MRO files is available through [[DTCC]] Web Portal. Firms using 
the [[DTCC]] Web Portal CBRS Inquiry function can download the CBRS transaction output file to Excel (Output 
Product [[ID]] #02401663). Firms can download a daily end-of-day CBRS transaction output file that will be 
available on [[DTCC]] Web Portal (Output Product [[ID]] #02401664). 
The Cost Basis Transaction MRO output record layout is 1,500 bytes, which is 500 bytes longer than the [[Asset]] 
and Tax Lot input record layouts. The output is longer because of several fields that CBRS adds to the output 
after it processes the input.  
CBRS sends all accepted cost basis data to eligible recipients. CBRS validates each field to ensure that it 
meets the established validation rules. CBRS passes the cost basis data to the receiving firms and does not 
verify the accuracy of the data submitted.  
The Cost Basis Transaction MRO has three main components. The first component is a set of CBRS system-
generated output fields. The second component is a set of status fields for the [[Asset]] and Tax Lot records 
received from the input file. The third component is the actual [[Asset]] and Tax Lot data fields that contain the 
cost basis information validated by the CBRS system. CBRS returns the [[Asset]] and Tax Lot records to firms in 
the same sequence it received them: [[Asset]] record first, and then all the associated Tax Lot records.  

---

## Page 40

CBRS User Guide 
Application Input and Output 40 
The CBRS output includes both the records that a user submits, and the records that it receives from other 
users. In the output, users can also view the submitted records that CBRS rejected. Each record in the Cost 
Basis Transaction MRO file has a System Action field that labels the record as Accepted, Modified, or 
Rejected.  
Q What are the primary keys for the Transaction MRO file? 
A There is no primary key on the file. The Cost Basis Control Number uniquely identifies a CBRS transfer 
which consists of one to many records (one [[Asset]] record plus zero to many Tax Lot records that 
correspond to the [[Asset]]). To create uniqueness in your database you need to add a column, such as a 
sequence number. The combination of these two columns creates a unique key within the table. For 
information stored in more than one table, you need to identify your self-created keys in a manner 
consistent with your database structure. 
Distribution Side 
The Distribution Side field on the MRO file corresponds to whom CBRS is sending the file. For system 
rejected records, this field has a value of S = Submitting [[participant]], because only the submitter receives 
system rejected records. For records successfully processed through CBRS, this field has a value of B = Both 
Receiving and Submitting [[participant]], because CBRS sends successfully processed records to both the 
submitting and receiving firm. The Cost Basis Transaction MRO file also has a Distribution Firm Number and 
Distribution Firm Type. These fields have the firm number and type for the user receiving the file. 
Cost Basis Control Number 
CBRS assigns a Cost Basis Control Number that uniquely identifies each [[Asset]] and associated Tax Lot 
record(s). This number appears only on the Cost Basis Output sent to each firm. The Cost Basis Control 
Number format is CCYYDDDCBNNNNNNNN (date + CB + eight-digit number). CBRS assigns the Cost Basis 
Control Number to each submitted [[Asset]].  
All tax lot records associated with an [[Asset]] have the same cost basis control number as that [[Asset]].  
The only exception is when a firm submits Tax Lot record(s) without a corresponding [[Asset]] record. In this case 
CBRS assigns a separate Cost Basis Control Number to each Tax Lot record, and then rejects it. Also, CBRS 
assigns a unique Cost Basis Control Number to rejected Cost Basis records ([[Asset]] and their associated tax lot 
records) for identification purposes.  
  

---

## Page 41

CBRS User Guide 
Application Input and Output 41 
System Rejects 
CBRS validates each field to ensure that it meets the established validation rules. If a record does not pass 
these rules, CBRS rejects the record. CBRS returns rejected transactions, both [[Asset]] and tax lot records, only 
to the submitting firm. The intended receiver of the cost basis information does not know the submitter 
attempted to deliver the information if the transaction is system rejected.  
Note: 
If CBRS rejects an [[Asset]] record, it also rejects all corresponding Tax Lot records. If CBRS rejects one Tax Lot record, it 
also rejects all the Tax Lot records and the associated [[Asset]] record.  
CBRS uses two fields to identify the error on a record: System Action Code and System Reject Reason. For 
more information, review the field descriptions.  
System Action Field 
The System Action field is in the beginning section of the output record of both the [[Asset]] and Tax Lot record. 
The System Action field indicates if each record on the input file was accepted, rejected, or modified. The 
values for the field are: 
• 1 = System Accepted - Transaction submitted correctly 
• 2 = System Modified - Transaction submitted correctly and modified by CBRS 
• 3 = System Rejected - Transaction submitted incorrectly 
Successfully passed records have a value of either 1 = System Accepted or 2 = System Modified in the 
System Action field. System Modified means CBRS has changed a field in the record. For more information, 
see the bullet below on the System Changed value in the Status field. 
System Reject Reason Field 
The System Reject Reason field specifies the reason that CBRS rejected the record(s). If the System Action 
code is a 3, the System Reject Reason field indicates the applicable reason. 
The following list shows the system reject reasons and their explanations: 
• 01 = Invalid Field – One or more fields in the record has violated system rules. 
• 02 = Associated Record is Invalid1 – For an [[Asset]] record, this code indicates that one or more of the 
associated tax lot records has violated system rules. For a Tax Lot record, this code indicates that the 
associated [[Asset]] record has violated system rules. 
• 03 = Invalid Length Record –Record does not conform to the 1,000-byte length required by the record 
layout. 
• 04 = Invalid Physical Sequence – [[Asset]] record not present –Tax Lot record does not have an 
associated [[Asset]] record. 
 
1  If a system reject occurs and the Firm Contra Number displays Firm 0008 and Transaction Types 26- [[DWAC]] Deposit, 27- Certificate Deposit, 28-[[DRS]] 
Profile/[[DO]], 36-[[DWAC]] Withdrawal, 37-Withdrawal by Transfer (WT), and 41- Direct Presentation, [[DTCC]] cannot identify the agent. To send the record, 
populate the correct contra firm and send as a corrected record (02). 

---

## Page 42

CBRS User Guide 
Application Input and Output 42 
• 05 = Invalid Physical Sequence – tax lot record(s) not present –[[Asset]] record does not have an 
accompanying Tax Lot record. 
• 07 = Invalid Accumulated Quantity –Sum of the Tax Lot Quantity fields does not equal the Total 
Position Quantity field on the associated [[Asset]] record. 
• 09 = No Corrected Tax Lot present for corrected [[Asset]] Input –[[Asset]] Record with the value ‘02 = 
Corrected [[Asset]] record’ in the Record Content Indicator field does not have at least one associated Tax 
Lot record with the value ’02 = Corrected tax lot record’ in its Record Content Indicator field. 
• 10 = Invalid Physical Sequence – Tax Lot invalid with [[Asset]] Input reject or request –[[Asset]] record 
with either ‘03 = Firm reject record’ or ’04 = Request record’ in the Record Content Indicator field has an 
associated Tax Lot record. 
• Space = Not rejected – CBRS has not rejected the record. 
Note  
Numbers ‘06’ and ‘08’ are not currently in use. 
Status Fields 
From the output, each submitted field has a corresponding status field. This field indicates if the value in the 
submitted field is valid, system changed, or error. A space is also a possible value for this field: the space 
occurs if the field is an optional field, the submitter does not populate the field, and the field does not have a 
[[default]] value. 
CBRS populates the status fields for all records on the Transaction MRO file. For the records where you are 
the contra party, the status is 0 = Valid, 1 = System Changed, or [space] which indicates that this field was 
not populated by the submitter. If a submitted field does not pass CBRS system rules, the status for that field is 
populated with a value of 2 = Error. When you are the contra party, you [[DO]] not receive a status field which has 
a value of 2 = Error, because CBRS rejects a record that has an error in it and returns it to the submitter. 
CBRS does not pass a system rejected record to the contra party. 
Q What is the System Reject Reason if a submitter sends a corrected tax lot with an original [[Asset]] 
record?  
A The System Reject Reason is 01 = Invalid Field, and the TO Record Content Indicator status value is 2 = 
Error. 
Example of System Changed 
System Changed appears in a Status field when CBRS changes a submitted value in a field.  
For example, on the Tax Lot Input record, there is a Certificate Number field. This field is allowed for only two 
transactions: 27 = Certificate Deposit and 41 = Direct Presentation. If a submitter populates this field for any 
other transaction type, CBRS replaces the submitted value with spaces and continues to process the record. In 
this case, the TO Certificate Number Status field has a value of 1 = System Changed. Access the record 
layouts to view the various occasions where CBRS might modify submitted data.  
  

---

## Page 43

CBRS User Guide 
Application Input and Output 43 
Example of System Rejected 
When an [[Asset]] or tax lot record is rejected, CBRS rejects the [[Asset]] record and all its accompanying tax lots. 
CBRS treats an [[Asset]] record and its tax lots as a package: when one piece is rejected, the entire package is 
rejected. The example shows what the MRO can contain when an [[Asset]] record is rejected, but the tax lot 
record conforms to system rules: 
• In this example, the CBRS “package” has one [[Asset]] record and one accompanying tax lot record. The 
[[Asset]] record is rejected because the submitting firm populated the [[settlement]] Date of Transfer field with 
20110135 (20110135 is the CBRS format for January 35, 2011). CBRS rejects the record because 
January 35, 2011 is not a valid calendar date. The tax lot record passes system rules and edits with no 
errors. 
• From the Cost Basis Transaction MRO file for the [[Asset]] record, the System Action field has a value of 3 = 
System Rejected. The System Reject Reason field has a value of 01 = Invalid Field. The AO [[settlement]] 
Date of Transfer Status has a value of 2 = Error. This combination of fields tells the submitter that the 
record is rejected, and why. (Other fields on the MRO are populated as well, this example highlights fields 
related to the reject.) 
• From the Cost Basis Transaction MRO file for the accompanying tax lot record, the System Action field 
has a value of 3 = System Rejected. The System Reject Reason field has a value of 02 = Associated 
Record is Invalid. There are no 2 = Error values for the tax lot record Status fields because it passes 
system rules and edits. This combination of fields tells the submitter that record is rejected because of a 
problem with the associated record. (Other fields on the MRO are populated as well, this example 
highlights fields related to the reject.) 
Output Dropped Records 
CBRS drops a transaction in the rare occasion when a submitter enters their firm number incorrectly, and 
CBRS does not recognize the submitter. In this case, CBRS rejects the record because the submitter is invalid. 
However, CBRS cannot return the record to the submitter because the incorrect submitter number does not 
match the submitter’s actual number, so CBRS does not know where to return the record. 
LPA Number and LPA Type 
A [[transfer agent]] uses its LPA number as the deliverer of the [[DRS]] [[DO]], and its [[transfer agent]] number as the 
Submitting Firm Number on the CBRS record. [[Broker]]-dealers and banks who receive cost basis from a 
[[transfer agent]] for Transaction Type 28 = [[DRS]] Profile/[[DO]] benefit from having the LPA number on the 
transaction output because they can use the LPA number to more easily match the [[DRS]] Profile/[[DO]] [[Asset]] 
transfer to the CBRS record for that transfer.  
From the MRO file, CBRS provides the Limited [[participant]] Account (LPA) number for cost basis passed on 
[[Direct Registration]] System ([[DRS]]) Profile/Deliver Order ([[DO]]) transactions. There are two fields on the 
Transaction MRO file, LPA Number and LPA Type. ‘LPA Type’ is always ‘DTCPRT’. The LPA Number is the 
LPA number that a [[transfer agent]] uses to send [[DRS]] [[DO]] transactions through [[DTC]]. CBRS populates these two 
fields only for original and corrected [[Asset]] and tax lot records, for Transaction Type 28 = [[DRS]] Profile/[[DO]]. 
Otherwise, both fields will contain spaces.  

---

## Page 44

CBRS User Guide 
Application Input and Output 44 
For CBRS to populate the LPA Number in this field, the [[DTCC]] Account Administration department sets up a 
relationship between a [[transfer agent]]’s [[transfer agent]] (TA) number that is currently eligible for CBRS, and it’s 
LPA number. This functionality applies only to Transfer Agents who are eligible for CBRS and have a Limited 
[[participant]] Account number.  
Transfer Agents who would like to opt out of this functionality should contact the Client Account Representative 
Team at RMsupport@[[DTCC]].com. 

---

## Page 45

CBRS User Guide 
Best Practices 45 
5. BEST PRACTICES 
This section contains Best Practices for CBRS as defined by various industry groups. These Best Practices are 
not enforced by system rules, but instead are guidance to the users of CBRS on how to handle certain 
situations and populate certain fields. While CBRS cannot enforce these Best Practices with system rules, 
these guidelines help all CBRS users process the submitted and received data in a consistent way. 
Resolving Issues with the Contra Party 
If a firm has received cost basis data from a submitting firm that it cannot apply or did not expect, the firm 
should contact the contra party directly. Similarly, if a firm does not receive cost basis information that it is 
expecting, the firm should contact the contra party directly. [[DTCC]] is not able to access firm data to respond to 
inquiries.  
Firms Submit and Receive Records 
If a firm is a CBRS user, the firm should submit cost basis information, not just receive cost basis information. 
CBRS users are expected to participate on both sides and for all transaction types. 
While CBRS users are expected to participate on both sides, some firms may have limitations on which 
transaction types they can submit. Firms with these limitations are expected to receive all transaction types 
supported by CBRS, either through an automated computer-to-computer connection or through [[DTCC]] Web 
Portal. 
When Should a Firm Send the CBRS Record? 
Send an Original record on the day after the item settles. If it is not possible to send the CBRS records the day 
after [[settlement]], send them as soon as possible after [[settlement]]. 
Send a Corrected record within fifteen days of knowing that the record needs to be corrected. 
Send a Firm Reject record within two business days, except for a certificate deposit. For a certificate deposit, if 
a firm receives partial [[shares]] from the [[transfer agent]], wait to send the reject. 
A receiver of an [[Asset]] should wait at least fifteen days after the [[Asset]] has been received before sending a 
Request record to the deliverer of the [[Asset]]. 
  

---

## Page 46

CBRS User Guide 
Best Practices 46 
Corrected Record 
From the submitter’s point of view, the first time it sends basis, the submitter should send an original record. If 
the basis on a Lot changes after the original record is sent, the submitter should send a corrected record. From 
the receiver’s point of view, if a contra party receives corrected basis but has not first received original basis for 
the lot, it should treat the basis as original and apply the basis appropriately. For example, a contra party 
should not firm reject a corrected record that does not have a corresponding original record.  
Q Which fields, when changed, should prompt the submitter to send a corrected record?   
A Any field that has been changed should be sent as a correction. If the data element is important enough 
to be changed, it is important enough to re-send. 
Note: 
If you replay the basis on your books, and everything stays the same, [[DO]] not send a corrected record to the receiver. If you 
replay the basis on your books and anything is different, send a corrected record to the receiver. 
Some Scenarios About Corrected Records 
Q Example: A fund sends a CBRS record that is system rejected by CBRS. When the fund 
resubmits the record, marked as corrected, does CBRS accept the record?  In other words, does 
CBRS have any edits in place to check that an original record passed through successfully 
before a corrected record can be sent?   
A No. CBRS does not confirm that a corrected record has a corresponding preceding original record. In 
that case, would a firm reject a corrected record back to the fund because it hasn’t received an original 
record?  
Best practices suggest that a receiver should not firm reject a corrected record that does not have a 
corresponding original record. A receiver should be prepared to accept either an original or corrected 
record.  
Q What about this scenario: a fund sends a CBRS record, it passes CBRS edits and is sent to the 
receiving firm, and then the firm responds with a firm reject record. When the fund responds with 
a corrected record, would the firm accept the corrected record, even though they did not accept 
the original record?   
A Yes. The receiving firm should accept the corrected record. These Best Practices hold true regardless of 
what type of CBRS user is the submitter or receiver: these same Best Practices apply to [[Broker]]-dealers, 
funds, banks, and [[Equity]] transfer agents/issuers. 
 
 

---

## Page 47

CBRS User Guide 
Best Practices 47 
Firm Reject and Request Records 
The scenarios describe the Best Practices for the different Record Content types. In each example, Firm A has 
transferred an [[Asset]] to Firm B, and now needs to pass the cost basis for that transferred [[Asset]]. 
• Firm A sends an original record to Firm B. Some of the data is incorrect, so Firm B sends a firm reject 
record to Firm A. Firm A responds with a corrected record. 
• Firm B has not received cost basis from Firm A. Firm B sends a request record to Firm A. Firm A 
responds with an original record. 
• Firm A sends an original record to Firm C. Firm C is not the correct receiving firm for this record, so it 
sends a firm reject record to Firm A. Firm A responds by sending an original record to Firm B. 
Note: 
In the example, while CBRS does not require Firm C to send a Firm Reject, it would be helpful for Firm C to Firm Reject 
the record so Firm A knows there is a problem. CBRS does not reject the record if it passes all the system rules and edits, 
so the only way Firm A knows there is a problem with the record is if Firm C rejects it. 
You can also firm reject corrected records. Let’s look at an example, using the same Firm A, Firm B, and Firm 
C: 
• Firm A sends a corrected record to Firm C. Firm C is not the correct receiving firm for this record, so it 
sends a firm reject record to Firm A. Firm A responds by sending a corrected record to Firm B. 
A firm reject is not an appropriate response to a firm reject record or a request record. Best Practices 
recommend that a firm disregard a firm reject or request record that it has received in error. 
Q Can a CBRS user send a corrected record without first sending an original record?   
A CBRS does not reject a corrected record that was not preceded by an original record, but the contra 
party may not accept the corrected record in this scenario. Best Practices say [[DO]] not send a corrected 
record unless you have first sent an original record. 
The following Best Practices apply to many of the fields in the Firm Reject and Request record content types 
(full list below): 
• If Record content indicator is 03 = Firm reject record, the fields should be populated with the value on the 
Original [[Asset]] record or Corrected [[Asset]] record received. 
• If Record content indicator is 04 = Request record, the fields should be populated with the value on the 
original transfer that triggered the need to pass cost basis. 
  

---

## Page 48

CBRS User Guide 
Best Practices 48 
List of fields where these two best practices apply: 
• Receiver Customer Account Number 
• Deliverer Customer Account Number 
• ISIN Country Code 
• ISIN Security Issue [[ID]] ([[CUSIP]] number) 
• ISIN Security Check Digit 
• Put - Call Indicator 
• [[Option]] Symbol  
• [[Option]] Expiration Date  
• [[Option]] Strike Price Integer  
• [[Option]] Strike Price Decimal  
• [[Asset]] Description 
• [[Asset]] Category 
• Total Position Quantity 
• Date Transfer was Initiated 
• [[settlement]] Date of Transfer 
• Position Code 
• [[shares]] to Cover Short Indicator 
[[DO]] Not Request Basis for Lots Received With Unknown Basis 
A receiving firm should not request basis from a submitting firm if the receiver receives lots that have unknown 
basis. Here are two examples: 
• Firm A sends cost basis to Firm B on a transfer of 300 [[shares]] of XYZ.  Firm A sends an [[Asset]] record for 
300 [[shares]], and two tax lots, one for 100 [[shares]] and one for 200 [[shares]]. The tax lot for 100 [[shares]] has a 
cost amount associated with it, but the 200-share lot has an unknown cost amount. The records pass 
CBRS processing, so Firm B receives all this information. 
o Best Practices say that Firm B should not request information about the 200-share lot that has 
unknown cost. A firm should use a request record only when it has not received any information at 
all. 
• Firm A sends an ACATS transfer to Firm B that contains 10 assets. Firm A sends CBRS records to Firm 
B, but only for 9 assets. 
o In this case, Firm B should send a request record for the one [[Asset]] for which it did not receive a 
CBRS record. 
  

---

## Page 49

CBRS User Guide 
Best Practices 49 
Submitting and Receiving Noncovered Accounts and Noncovered 
Security Types 
Here are the Best Practices about submitting and receiving data for noncovered accounts and noncovered 
security types: 
From the submitter’s perspective: 
• If you have cost basis, send it. 
• If you [[DO]] not have cost basis, [[DO]] not send anything. For example., [[DO]] not send a record that says the lot is 
noncovered and has unknown cost basis. 
From the contra party’s perspective: 
• [[DO]] not send a request record for a noncovered account or noncovered security type. 
• If you receive basis for an account that is noncovered, [[DO]] not reject it. 
• If you receive basis for a security that you think is noncovered, [[DO]] not reject it. 
Covered Fixed Income Assets Transferred in 2014 
The regulations for the transfer of fixed income assets became effective on January 1, 2015. However, a 
CBRS user may receive basis on a fixed income [[Asset]] in 2014 which the submitter has marked as covered. 
When a CBRS user receives cost basis for fixed income assets in 2014 which are marked as covered, the 
receiver needs to determine whether to consider those assets covered. 
CBRS Quantity Should Equal the Original [[Asset]] Transfer Quantity - 
Avoid Fractional [[shares]] 
In the previous version of CBRS, some firms sent an [[Asset]] transfer for a round lot, and then follow up in CBRS 
with a quantity that includes fractional [[shares]]. To avoid this discrepancy, the quantity transferred through 
CBRS should equal the quantity of the original [[Asset]] transfer that triggered the need to pass cost basis. If the 
original [[Asset]] transfer did not have fractional [[shares]], neither should the CBRS record. 
Q If there is a corporate action during an ACATS transfer, what happens in CBRS?   
A Scenario: 100 [[shares]] of an [[Asset]] are transferred through ACATS. During the ACATS transfer, there is a 
[[Stock]] [[Dividend]] for 2 [[shares]]. In ACATS, the deliverer should send a residual balance of 2 [[shares]]. In 
CBRS, the deliverer should send a CBRS record for 100 [[shares]], and then another CBRS record for 2 
[[shares]]. This answer follows the best practice that the CBRS quantity should always equal the quantity of 
the [[Asset]] transfer. 
  

---

## Page 50

CBRS User Guide 
Best Practices 50 
Populating CBRS Records for ACATS Reclaim or Fail Reversal 
Transactions 
Follow these steps for populating the Submitting Firm, Contra Firm, Deliverer Customer Account Number, and 
Receiver Customer Account Number fields for ACATS reclaim (RCL) or fail reversal (FRV) transactions: 
The Submitting Firm is the firm submitting the CBRS record (and is the delivering firm of the [[Asset]] in ACATS). 
The Contra Firm is the firm receiving the CBRS record (and is the receiving firm of the [[Asset]] in ACATS). The 
Deliverer Customer Account Number is the account number at the firm delivering assets in the "original" 
ACATS transfer, and the Receiver Customer Account Number is the account number at the firm receiving 
assets in the "original" ACATS transfer. Both customer account number fields [[DO]] not correspond to the "new" 
Deliverer/Receiver Customer Account Number for the FRV or RCL. 
For example, Firm 789 submits a TIF for a full transfer to Firm 123. Firm 123 delivers the assets to Firm 789. 
(For this example, the transfer contains only long assets.)  Later, Firm 123 submits a reclaim to Firm 789. Firm 
789 sends the [[Asset]] to 123 in response. The customer account number at Firm 123 is 10203, and the 
customer account number at Firm 789 is 70809. The following table shows how CBRS records should be 
populated for the full transfer and the reclaim. 
ACATS CBRS 
Transfer 
Type 
TIF 
Submitter 
[[Asset]] 
Deliver 
[[Asset]] 
Receiver 
Deliverer 
Customer 
Account 
Number 
Receiver 
Customer 
Account 
Number 
Record 
Type 
Submitting 
Firm 
Contra 
Firm 
Deliverer 
Cust. 
Account 
Number 
Receiver 
Cust. 
Account 
Number 
FUL 789 123 789 10203 70809 Original 123 789 10203 70809 
FUL 789 123 789 10203 70809 Corrected 123 789 10203 70809 
FUL 789 123 789 10203 70809 Firm 
Reject 
789 123 10203 70809 
FUL 789 123 789 10203 70809 Request 789 123 10203 70809 
RCL 123 789 123 10203 70809 Original 789 123 10203 70809 
RCL 123 789 123 10203 70809 Corrected 789 123 10203 70809 
RCL 123 789 123 10203 70809 Firm 
Reject 
123 789 10203 70809 
RCL 123 789 123 10203 70809 Request 123 789 10203 70809 
 
  

---

## Page 51

CBRS User Guide 
Best Practices 51 
The following best practice explains what firms should [[DO]] in the event of an ACATS Fail Reversal or Reclaim: 
• Fail Reversals: The ACATS request went to the 310-Settle Close status, but the delivering firm is telling 
the receiving firm that the assets will not be delivered. Firms should unwind the FRV and not send or 
expect basis. If the firm initiating the FRV receives basis back, they should ignore it.  
• Reclaims: ACATS went to the 310-Settle Close status and the assets were delivered and are in the 
clients account before the RCL is initiated. Firms should send basis back to the firm reclaiming the [[shares]]. 
For partial reclaims, the basis sent back should still be from the [[shares]] received, but they should be based 
on the disposal method for that clients account. 
Sending a CBRS Record for an [[Asset]] Held in Multiple Currencies 
Q [[DO]] I send multiple [[Asset]] records for the same security if I hold the security in different 
currencies?   
A Remember that the quantity of the [[Asset]] record should correspond to the quantity of the original transfer 
that triggered the need to pass cost basis. You can indicate at the tax lot level which lots are held in a 
currency other than US Dollars. 
Sending Cost Basis for an Invalid Certificate 
Q If a [[transfer agent]] receives a deposit for 100 [[shares]] consisting of two 50 [[shares]] certificates and 
only one certificate can be processed, for example, one of the certificates is invalid, how should 
cost basis be returned?   
A Best Practices suggest that, since in this case a [[transfer agent]] can only re-register 50 [[shares]], it would 
only pass basis on the 50 [[shares]] that are re-registered. 
  

---

## Page 52

CBRS User Guide 
Best Practices 52 
Field Specific Best Practices 
After each field name (A) indicates a field on the [[Asset]] Input; (T), a field on the Tax Lot Input; and (A/T), a field 
on both the [[Asset]] and Tax Lot Input. 
Transaction Type (A/T) 
CBRS users should not firm reject a record based solely on a mismatched Transaction Type. If a user receives 
a record with a Transaction Type it does not recognize, examine other criteria in the record to match an [[Asset]] 
transfer 
Transaction type 05 = Mutual Fund Transfer (non-ACATS) [change of [[Broker]]-dealer] is for [[Broker]]-to-[[Broker]] 
transfers, and requests for this transaction type should not be sent to a fund. 
Transfer Control Number (A/T) 
If transaction type is 02 = Free [[DTC]] Deliver Order (Non-ACATS) or 03 = Valued [[DTC]] Deliver Order; this field 
should be the IMS Transaction [[ID]] number (16 bytes) as specified on the original transaction processed at [[DTC]]. 
If transaction type is 26 = [[DWAC]] Deposit, 27 = Certificate Deposit, 28 = [[DRS]] Profile/[[DO]], 36 = [[DWAC]] 
Withdrawal, 37 = Withdrawal by Transfer (WT); this field contains a reference [[ID]] number whose values and 
number of bytes changes depending on the original transaction processed at [[DTC]].  The CBRS Transfer 
Control Number should equal the reference [[ID]] for DAMP Deposits at [[DTC]]. 
If transaction type is 41 = Direct Presentation, this field should be 26 characters: 
Julian Date (3 bytes: DDD) + [[participant]] Number (5 bytes) + Customer Account Number (18 bytes) 
If transaction type is 46 = Fund to Firm Mutual Fund Transfer or 51 = Firm to Fund Mutual Fund Transfer; this 
field is the FundSERV control number. To match the number that Funds should provide in this field, firms 
should use the Fund/SERV Control # from the ACATS Fund/SERV Statistics file and add CATS to the front of 
it. 
If transaction type is 56 = Networking Transaction, then the control number is the Networking control number 
For all other transaction types, 04 = Conversion, 05 = Mutual Fund Transfer (Non-ACATS), 06 = FED (non-
ACATS), 07 = Physical Movement [[settlement]], 08 = OCC transfer, 09 = Non-Domestic Depository, 10 = Other, 
57 = Manual Mutual Fund Transfer; this field is the control number agreed upon by the contraparties involved in 
the original [[securities]] transaction. 
If Transaction Type is 58=AIP, this field should follow be: ‘D’ Direct Transfer Indicator (1 byte) +Julian Date (3 
bytes: DDD) + Submitting [[participant]] Number (8 bytes) + Receiving Customer Account Number (15 bytes) + 
Unique sequential number (3 bytes) 
If Transaction Type is 59=Alternative Investments (Non-AIP), this field should be ‘D’ for Direct Transfer 
Indicator (1 byte) + [[NSCC]] [[participant]] Number for the Fund or CBRS [[Member]] Number (8 bytes) + Last Digit of 
Current Year (1 byte) + Julian Date (3 bytes) + Unique sequential number (5 bytes). 

---

## Page 53

CBRS User Guide 
Best Practices 53 
Alternate Control Number (A/T) 
For Transaction Types 46 = Fund to Firm Mutual Fund Transfer or 51 = Firm to Fund Mutual Fund Transfer, 
populate this field with the ACATS Control Number. 
For Transaction Type 58=AIP, populate this field with the AIP SIN Number ([[NSCC]] Security Identifier). 
[[Asset]] Description (A/T) 
Populate this field for all records. 
[[Asset]] Category (A) 
Notes: 
Take care to populate this field accurately. This value should correspond to the [[Asset]] category for the transferred security. 
This is an important field that drives validation rules for the rest of the record. 
Use the Options [[Asset]] category for reporting 1256 Options. 
Transferring Basis on Rights or [[Warrants]]  
A deliverer should only pass basis for [[Warrants]] or rights that were purchased for cash. Cost Basis allocated 
under rule 305 or 307 should not be transferred; instead, it should be re-allocated back to the underlying 
security. 
Receiver Customer Account Number (A/T) 
If a firm does not have a receiver customer account number, Best Practices suggest entering the words “not 
provided” in this field. For ACATS items this Best Practice does not apply—a submitting firm does have a 
receiver customer account number for assets transferred through ACATS. 
Deliverer Customer Account Number (A/T) 
The submitter should populate this field for Transaction Type 04 = Conversion. 
  

---

## Page 54

CBRS User Guide 
Best Practices 54 
Total Position Quantity/Tax Lot Quantity (A/T) 
Q How [[DO]] I populate the quantity fields for fixed income and options?  For example, if I transfer 10 
[[Option]] contracts at 100 [[shares]] per contract, should I populate the quantity field with 10 or 100?   
A For an [[Option]], the submitter should populate the quantity field with the number of contracts. So, in this 
example, the submitter should populate the quantity field with ‘10’.  
Q For fixed income, if I transfer 10 [[Bonds]] with a total face value of 10,000, should I populate the 
quantity field with 10 or 10,000?  
A For a fixed income [[Asset]], the submitter should populate the quantity field with the [[Asset]]’s face value. In 
this example, the submitter should populate the quantity field with 10,000. 
Date Transfer was Initiated and [[settlement]] Date of Transfer (A) 
Best Practices define the [[settlement]] Date of Transfer, in general, as the day the position leaves the 
submitter’s books. 
Note: 
For options transferred through ACATS, the submitter should populate the [[settlement]] Date of Transfer with the ACATS 
[[settlement]] date. For options transferred at the Options Clearing Corporation (OCC) outside of ACATS, the submitter should 
populate the [[settlement]] Date of Transfer with the date the [[Option]] settled at the OCC. 
For covered fixed income transferred through the Federal Reserve, the submitter should use the date the transfer settled at 
the Fed to populate the [[settlement]] Date of Transfer. 
While the Date Transfer was Initiated may not be known for the underlying transfer, the [[settlement]] Date of 
Transfer should be known. One or the other of these dates is required. Best Practices suggest that the 
[[settlement]] Date of Transfer will be used for most records. 
Disposition Method Used (A) 
The field has a limited list of values of potential disposition methods. As it states in the record layouts, the list of 
values for this field are not exhaustive—there are other methods that firms use. The field is also Optional, and 
not all firms use it. For firms who [[DO]] use it, the field could provide value-added information for the underlying 
customer. Best Practices suggest that firms should try to use the field on a best-efforts basis. 
[[shares]] to Cover Short Indicator (A) 
This field is used in the following example: 
A customer moves to Firm A, and requests that Firm A delivers [[shares]] to Firm B to cover a short at Firm B. 
When Firm A sends the cost basis, populating the [[shares]] to Cover Short Indicator with the Y value tells Firm 
B that the intent is to [[Close Out]] the short.  
Sometimes in this situation, Firm B establishes a new position, has both a short account and a long position on 
its books, and awaits customer instructions. This field eliminates this last step. 

---

## Page 55

CBRS User Guide 
Best Practices 55 
Noncovered/Pending Indicator (T) 
If field is left blank, the receiver will consider the lot covered if the Position Code is L = Long. If the Position 
Code is S = Short, the covered status of the position is not determined until the [[shares]] are acquired. Examples 
of when a submitter would use the Noncovered account value or the Pending value: 
• Noncovered account: Account belonging to an exempt recipient (such as a C corporation) or an exempt 
account (such as a retirement account). 
• Pending: Account can be pending because the [[Asset]] is a part of an Employee [[Stock]] Plan, or because the 
submitter is waiting for cost basis information from a prior firm 
Certificate in Customer Name: Use this field to indicate that a certain tax lot is restricted or physical. 
These [[shares]] are always noncovered from the [[Broker]]-dealer’s perspective. The [[transfer agent]] has 
responsibility for the cost basis. The [[Broker]] may have the basis on its books, but if so, it has been 
provided by the customer. For example, a [[Broker]]-dealer receives a transfer of 1,000 [[shares]] of ABC, 300 
restricted [[shares]] 700 cash [[shares]]. The [[Broker]]-dealer segregates the restricted [[shares]] from the cash 
[[shares]]. When the contra party sends cost basis to the [[Broker]]-dealer through CBRS, it uses this new 
indicator to mark the 300 [[shares]] as noncovered using the “Certificate in Customer name” value. When the 
[[Broker]]-dealer receives the cost basis, it knows to apply the basis for these 300 [[shares]] to the 300 
restricted [[shares]] in the transfer. Without this indicator, the receiver would not know what basis to apply to 
the restricted [[shares]].  
Note: 
The submitter should not use the 01 = Noncovered lot value in this situation. [[shares]] may be noncovered for other 
reasons. If the [[shares]] are noncovered because they are restricted or physical, the submitter needs to use the value 
“Certificate in Customer Name”. 
Q What are some examples of when different values in the Noncovered/Pending Indicator are used?   
A Here are some examples: 
o Noncovered lot – A noncovered lot could occur in this scenario: a customer transfers 300 [[shares]] of 
[[Equity]] XYZ, containing two tax lots, one lot of 100 [[shares]], purchased on 05/29/2009, and one lot of 
200 [[shares]] purchased on 06/01/2011. The lot of 100 [[shares]] was purchased before the IRS 
regulations came into effect for equities so this lot is uncovered. The lot of 200 [[shares]] was purchased 
after the IRS regulations came into effect for equities, so this lot is covered. When passing cost basis 
on this customer transfer, the record for the lot of 100 [[shares]] would have a value of “Noncovered lot” 
in the “Noncovered/Pending Indicator”. 
o Noncovered account – An example of a Noncovered account is a retirement account. 
o Pending – Pending could occur in this scenario:  A customer transfers an [[Asset]] from Firm A to Firm 
B. A month later, the same customer transfers an [[Asset]] from Firm B to Firm C. Firm B is obligated to 
send cost basis to Firm C, but they have not yet received the basis from Firm A. Firm B sends the 
lots to Firm C, marked as Pending. Firm B sends corrected records to Firm C once it has received the 
cost basis from Firm  
Scenario: I send a CBRS transaction to a contra party that includes a lot that is pending (for example, has a 03 
= Pending value in the Noncovered/Pending Indicator) because I am waiting for basis from the prior firm. When 
I received that basis, and then send it on to the contra party, [[DO]] I send an original record or a corrected record? 
In this scenario, you should send a corrected record.  

---

## Page 56

CBRS User Guide 
Best Practices 56 
Taxes Reported by [[issuer]]/[[transfer agent]] (T) 
In some cases, the [[issuer]]/[[transfer agent]] does the 1099-B reporting. To avoid both parties reporting the 
information, the [[issuer]]/[[transfer agent]] uses this field to inform the [[Broker]]-dealer that it has already done the 
1099-B reporting for a given tax lot. 
Q Does the Taxes Reported by [[issuer]]/[[transfer agent]] field apply only to the current year’s tax 
reporting?   
A No. There can be circumstances where the reorg event affects multiple years. 
Gifted or Inherited Indicator (T) 
The gifted and/or inherited information in CBRS cannot be cross-referenced with the value in the Gift/Donation 
Indicator in ACATS. The gifted and/or inherited information in CBRS is used to establish the value of the tax 
lot. The gift indicator in ACATS is used to tell the receiver that the deliverer is sending a transfer where the 
account titles [[DO]] not match, and the deliverer or requestor is aware of this discrepancy. 
It is always recommended to deliver gifted or inherited [[securities]] and not request them through ACATS. 
However, if you [[DO]] not abide by this rule and request an inherited or gifted security, it is the obligation of the 
receiver to step up the basis. 
Q What is the significance of the 03 = Inherited, then Gifted value in the Gifted or Inherited Indicator 
on the Tax Lot Input record layout?   
A This value exists because of its impact on the holding period for the lot. Gifted [[shares]] have a short-term 
holding period, inherited [[shares]] have a long-term holding period. If an [[investor]] gifts inherited [[shares]], the 
lot should keep its long-term holding period. For example, an [[investor]] inherits [[shares]]. The same [[investor]] 
then gives these [[shares]] to his daughter. In this case, populate the Gifted or Inherited Indicator field with 
the value 03 = Inherited, the Gifted, to inform the receiver of the CBRS record that the lot should keep its 
long-term holding period. 
Q Where on CBRS can I indicate the date of inheritance?   
A The submitter does not enter the date of inheritance, as in the date the [[shares]] were inherited. Instead, 
the submitter should enter the date of death of the decedent in the Acquisition Date of Tax Lot field. 
Fair Market Value as of Date of Gift (T) 
The submitter should populate this field if the value is known for a gifted security. 
Note: 
For [[Bonds]], should be unadjusted for amortization or accretion. Basis adjustments should be made for all other security 
types. 
  

---

## Page 57

CBRS User Guide 
Best Practices 57 
Position Code (T) 
In this field, transfer agents and [[Mutual Funds]] should [[default]] to L = Long position. 
Position Code for Options (T) 
Q When I am submitting a record to CBRS, how [[DO]] I differentiate between writing the call and 
buying the call? 
A You can indicate whether you bought the call or wrote the call using the ‘Position Code’ field to label the 
tax lot as either Long or Short. 
Populating Acquisition Date of Tax Lot field when Date is Unknown (T) 
How a submitter populates the Acquisition Date of Tax Lot field varies depending on the following scenarios: 
When the acquisition date and the cost basis are both unknown: 
1. Populate the Noncovered/Pending Indicator field with the appropriate value for the lot. Populating this field 
tells the receiver that the lot is noncovered or pending. 
2. [[DO]] not populate any date or cost fields. 
3. Populate the Zero Basis Indicator with the value 02 = Unknown. 
When the acquisition date is unknown, but the cost basis is known: 
1. Populate the Noncovered/Pending Indicator field with the appropriate value for the lot. Populating this field 
informs the receiver that the lot is noncovered or pending.  
2. Best Practices suggest you can a date of 01/01/1901* (19010101 in CBRS record layout format) to signify 
an unknown date.  
*The date 01/01/1901 can mean different things: 
o If the lot is noncovered, 01/01/1901 can mean various dates or unknown date 
o If the lot is covered, 01/01/1901 means various dates 
3. Populate the cost field(s) as applicable 
 
Q When can 01/01/1901 mean various? 
A The best practice suggest that IRS regulations allow the grouping of lots (covered lots into one group, 
noncovered lots into another group) for lots older than five years for [[Mutual Funds]] and [[shares]] in a DRP 
plan. In this context, when lots are grouped together, the 01/01/1901 date can mean various. 
Original Acquisition Date for Wash Sale Adjustment (T) 
The submitter should populate this field if the tax lot is the result of a wash sale. If the Original Acquisition Date 
for Wash Sale Adjustment is submitted, then the Wash Sale Adjustment Amount must also be populated.  
  

---

## Page 58

CBRS User Guide 
Best Practices 58 
Wash Sale Adjustment Amount (T) 
The Wash Sale Adjustment Amount is commonly referred to as the Disallowance Amount. The Wash Sale 
Adjustment Amount represents the disallowed loss from a wash sale, which has been added to the Tax Lot 
Current Cost.  If the Wash Sale equals zero for a fixed income security, then the Wash Sale Adjustment 
Amount field must be populated with zero, blanks are not accepted in this scenario. 
• Neither the Tax Lot Original Cost, nor Tax Lot Current Cost basis of a fixed income security should be 
adjusted for the disallowed loss resulting from a wash sale. 
• The Wash Sale Adjustment Amount should be applied to the Tax Lot Original Cost, and Tax Lot Current 
Cost basis for the disallowed amount when assets are not fixed income. 
Exchange Rate (T) 
This field should be the spot exchange rate used while converting the Tax Lot Current Cost. The rate is the 
amount of local currency equal to one dollar. For example, if ISO Currency Code = JPY, the value in this field is 
86.4428 for the acquisition date 12/01/2009. 
Last Factor 
When the [[Asset]] Category field is set to MBS = Mortgage Backed [[securities]], you can, optionally, 
repurpose this field to input the last factor for mortgage-backed [[securities]]. You can then repurpose the 
[[Option]] Expiration Date field to input the last factor date.  
Tax Lot Original Cost (T) 
In this field, the submitter should include total original cost for [[Asset]] backed [[securities]]. 
• In the event of a wash sale for an [[Equity]] security, the Tax Lot Original Cost should be adjusted for the 
Wash Sale Adjustment Amount. 
• For covered fixed income [[securities]], [[DO]] not adjust the Tax Lot Original Cost for corporate actions. 
• The Tax Lot Original Cost should be populated for [[Asset]] backed [[securities]]. 
• If you are not amortizing or accreting a bond, the original cost and current cost for that bond could be the 
same. 
  

---

## Page 59

CBRS User Guide 
Best Practices 59 
Tax Lot Current Cost (T) 
If Position Code is S = Short and the security is covered by the legislation, this field should equal the gross 
proceeds of the [[short position]]. For lots using average cost, populate this field with the [[Pro-Rata]] average cost. 
This field includes this Best Practice: “For a noncovered average cost mutual fund position with at least one lot 
with unknown basis, populate this field with the actual current cost for each lot with known basis.”   
This means that the submitter should populate this field with the actual current cost for the lot without 
consideration for averaging. For example, a submitter has three lots. The submitter should populate the Tax 
Lot Current cost fields for the lots as follows: 
Tax Lot Quantity Tax Lot Cost Value in the Tax Lot Current Cost Field 
100 $700 $700 
200 $2,000 $2,000 
50 unknown $0, with a value of  
02 = Unknown in the  
Zero Basis Indicator field 
 
The submitter should not average all three lots together, and then populate the Tax Lot Current Cost field for 
each lot with its corresponding portion of the average.  
Best Practices indicate that a submitter should send the cost of the individual lot. However, sometimes the 
average cost is the only value that is known. In that case the submitter should send the average cost value in 
the Tax Lot Current Cost field. If neither the individual cost of the lot nor the average cost of the lot is known, 
the submitter should send the lot with unknown cost. 
Q How [[DO]] I indicate a negative value in the Tax Lot Current Cost field?  
A CBRS does not accept negative numbers. 
Note: 
• If you are not amortizing or accreting a bond, the original cost and current cost for that bond could be the same. 
• Adjust the Tax Lot Current Cost field for fixed income [[securities]] in the event of corporate actions, return of principal, 
OID, accretion, amortization as of the [[settlement]] date of the transfer. 
• Populate the Tax Lot Current Cost field when reporting Section 1256 Options. 
Zero Basis Indicator (T) 
Q When would a firm use the value 01 = True Zero?  
A A submitter could use the value 01 = True Zero in dealing with rights, or the return of capital. 
  

---

## Page 60

CBRS User Guide 
Best Practices 60 
Tax Lot Original Unit Price (T) 
Populate for a mortgage-backed security, if known. 
Employee Plan [[shares]] Indicator (T) 
If this field is populated, a third party—not the submitter—should provide the cost basis for the tax lot. 
Fields for Fixed Income Elections (T) 
The following table describes how a submitter should fill out the five fields related to fixed income elections, if 
the submitter is following the defaults outlined in the IRS regulations. 
Note  
[[default]] refers to the regulations, and not to a CBRS system [[default]]. CBRS does not automatically populate any of these 
fields. 
Election [[default]] per 
IRS Regulations 
Election to Accrue Market Discount using a constant yield 
*If lot was acquired prior to 1/1/2015 when IRS changed [[default]] election this should be 
reported as N. 
 Y* 
Election to Include Market Discount in Income currently N 
Election to Amortize [[Premium]] Y 
Spot Rate election for interest accruals with respect to a covered debt instrument 
denominated in a currency other than the U.S. dollar. (Y is only a valid value for 
[[securities]] denominated in foreign currency) 
N 
Purchase/ [[Dividend]] Reinvestment Indicator (T) 
The IRS [[default]] value for the Purchase / [[Dividend]] Reinvestment Indicator is P= purchase. 
  

---

## Page 61

CBRS User Guide 
Best Practices 61 
Market Discount (T) 
Market Discount information if applicable, should be included in the cost basis submissions for only CD’s, 
Commercial Paper, Corporates, Foreign Debt, Governments, Mortgage Backed [[securities]], Municipals and 
Zeroes. The following table provides a summary of Best Practices applicable to populating the Market Discount 
and Accrued Unrealized Market Discount (pg. 60) field. 
Market Discount 
Situation  Include 
Market 
Discount in 
Income 
Election  
Market Discount 
Reported on the 
Transfer Statement 
Current Cost  
Note: Should not 
include wash sale 
adjustments or 
carryover amount  
Accrued Unrealized 
Market Discount 
Reported on the 
Transfer Statement 
Election to include 
market discount in 
income currently is 
not made  
No  Amount should be 
0.00 Market Discount 
is deferred.  
Current Cost should not 
include any accretion of 
Market Discount  
Report the amount of 
Market Discount that 
has accrued from 
acquisition date through 
the transfer date. 
Election to include 
market discount in 
income currently is 
made  
Yes  Amount should reflect 
the accreted Market 
Discount from 
acquisition date to 
[[settlement]] date of 
transfer.  
Current Cost should 
include the amount of 
accreted Market Discount 
from acquisition date to 
the [[settlement]] date of 
transfer  
Report 0.00. All accrued 
market discount has 
been realized and 
applied to cost.  
Election to include 
market discount in 
income has been 
made and 
subsequently revoked 
 
No  Report the amount of 
market discount 
accrued for the years 
where the election to 
include market 
discount was in force. 
Current Cost should 
include the accreted 
Market Discount from 
[[settlement]] date of 
acquisition to the date of 
revocation  
Report the amount of 
market discount 
accrued for years where 
the election include 
market discount in 
income was not in 
force.  
[[default]] of debt 
instrument purchased 
at a market discount 
Current Inclusion 
election is not made  
No  Amount should be 
0.00  
Current Cost should not 
include any accretion of 
Market Discount  
Report the amount of 
Market Discount that 
has accrued from 
acquisition date through 
the transfer date.  
[[default]] of debt 
instrument purchased 
at a market discount - 
Current Inclusion 
election is made  
Yes  Amount should reflect 
the accreted Market 
Discount through the 
[[settlement]] date of the 
transfer  
Current cost should 
reflect the Market 
Discount amount 
accreted through the 
[[settlement]] date of the 
transfer  
Report 0.00. All market 
discount accrued has 
been realized and 
applied to cost.  
 
  

---

## Page 62

CBRS User Guide 
Best Practices 62 
Bond [[Premium]] (T) 
Bond [[Premium]] information, if applicable, should be included in the cost basis submissions for only CD’s, 
Commercial Paper, Corporates, Foreign Debt, Governments, Mortgage Backed [[securities]], Municipals and 
Zeroes. The following table shows a summary of Best Practices applicable to populating the Bond [[Premium]] 
field. 
Bond [[Premium]] 
Situation Amortize 
Bond 
[[Premium]] 
Election 
Bond [[Premium]] Current Cost 
Note: Should not include wash sale 
adjustments or carryover amount 
[[Broker]] [[default]] to 
Amortize 
Yes Amount should reflect amortized 
Bond [[Premium]] from acquisition date 
to the date of the last interest 
payment (last interest payment date 
since amortization is only allocable to 
interest payments) 
Current Cost adjusted for amortized 
Bond [[Premium]] from acquisition date to 
the date of last interest payment, for 
example, the last interest payment date 
since amortization is only allocable to 
interest payments. 
Client Notification 
to not amortize 
No For [[Bonds]] purchased in the year the 
election is made or thereafter, this 
amount should be 0.00. 
 
For [[Bonds]] purchased in a year prior 
to the election, this amount should be 
the amount of amortized Bond 
[[Premium]] from the [[settlement]] date of 
acquisition to the date of the 
notification to not amortize 
For [[Bonds]] purchased in the year the 
election is made or thereafter, Current 
Cost should be unadjusted for any Bond 
[[Premium]] 
For [[Bonds]] purchased in a year prior to 
the election, Current Cost should be 
adjusted by the amount of amortized 
[[Premium]] from the date of acquisition to 
the date of the notification to not 
amortize. 
Revocation of 
notification to not 
amortize 
Yes Amount of amortization from the date 
of revocation to the [[settlement]] date of 
transfer 
Current Cost adjusted for the amount of 
Bond [[Premium]] amortized from the date 
of revocation to the [[settlement]] date of 
transfer. 
[[default]] of debt 
purchased at a 
Bond [[Premium]] with 
the [[default]] to 
amortize 
Yes Amount of amortized Bond [[Premium]] 
from [[settlement]] date of acquisition to 
the date of the last interest payment 
received 
Cost adjusted for the amount of 
amortized Bond [[Premium]] from date of 
acquisition to the date of the last interest 
payment received. 
  

---

## Page 63

CBRS User Guide 
Best Practices 63 
Acquisition [[Premium]] (T) 
Acquisition [[Premium]] information if applicable, should be included in the cost basis submissions for only CD’s, 
Commercial Paper, Corporates, Foreign Debt, Governments, Mortgage Backed [[securities]], Municipals and 
Zeroes. The following table provides a summary of Best Practices applicable to populating the Acquisition 
[[Premium]] field. 
Acquisition [[Premium]] 
Situation Acquisition [[Premium]] Current Cost 
Note: Should not include wash sale 
adjustments or carryover amount 
No Applicable 
Election 
Amount of acquisition [[Premium]] accreted 
from the [[settlement]] date of acquisition 
through the [[settlement]] date of transfer, 
For OID [[Bonds]] purchased at par or at a 
bond [[Premium]], this amount should be 0.00 
or equal to the amount of accrued OID 
Cost adjusted for the amount of acquisition 
[[Premium]] accreted from the [[settlement]] date of 
acquisition through the [[settlement]] date of 
transfer. 
For OID [[Bonds]] purchased at par or at a bond 
[[Premium]], this amount should be 0.00 or equal to 
the amount of accrued OID 
[[default]] of debt 
purchased at an 
acquisition [[Premium]] 
Amount of acquisition [[Premium]] accreted 
from the [[settlement]] date of acquisition 
through the [[settlement]] date of transfer 
Cost adjusted for the amount of acquisition 
[[Premium]] accreted from the [[settlement]] date of 
acquisition through the [[settlement]] date of 
transfer 
Accrued OID (T) 
Accrued OID information, if applicable, should be included in the cost basis submissions for only CD’s, 
Commercial Paper, Corporates, Foreign Debt, Governments, Mortgage Backed [[securities]], Municipals and 
Zeroes. The following table provides a summary of Best Practices applicable to populating the Accrued OID 
field. 
Accrued Original Issue Discount (OID) 
Situation Accrued OID 
(Cost basis is not adjusted down for Payment in 
Kind payments) 
Current Cost 
Note: Should not include wash sale 
adjustments or carryover amount 
[[default]] of debt issued 
at an Original Issue 
Discount 
Amount of OID accreted from the [[settlement]] date of 
acquisition through the [[settlement]] date of transfer 
Original cost basis plus amount of OID 
accreted from the [[settlement]] date of 
acquisition through the [[settlement]] date 
of transfer. 
Complex Debt with 
Original issue 
discount payments of 
NQSI 
Amount of OID accreted from the [[settlement]] date of 
acquisition through the [[settlement]] date of transfer 
minus either the amount of NQSI or the projected 
payment, whichever is applicable.  
Original cost plus OID minus either the 
NQSI or projected payment, whichever 
is applicable.  
  

---

## Page 64

CBRS User Guide 
Best Practices 64 
Last Adjustment Date (T) 
The Last Adjustment Date occurs when the last basis adjustment was made to account for Bond [[Premium]], 
Acquisition [[Premium]], Market Discount or OID, Examples of how the fields would be populated are described. 
This is meant to provide further descriptive information and is not meant to be an exhaustive list or include all 
possible scenarios.  
Notes  
You should consider the requirements of each of the defaults and elections, how they may interact, the cost paid by the 
client and considerations for the potential for an election to be made in a calendar year after the [[Asset]] is acquired and for 
the potential that an election may be revoked. 
The adjustment happens on the last coupon date, not on the [[settlement]] date.   
• For OID [[Bonds]] neither purchased at a bond [[Premium]] or market discount, such as either at an acquisition 
[[Premium]] or at the adjusted issue price, the Last Adjustment Date should be the [[settlement]] date of the 
transfer as this is the last date, as of which OID was accreted or amortized, and there is no other type of 
cost basis adjustments due to premiums or discounts.  
• For [[Bonds]] purchased at a bond [[Premium]] (OID or non-OID)  
o If the lot is not being amortized, the Last Adjustment Date would be the acquisition date of the lot 
since no amortization has occurred. 
o If the position is being amortized, the Last Adjustment Date would generally be the date of the last 
interest payment because that would have been the last date the cost basis was adjusted for the 
amortization of bond [[Premium]].  
» Acquisition [[Premium]] offsets the OID for OID [[Bonds]] purchased at a bond [[Premium]]  
» Note that if interest is not paid on a scheduled interest payment date (for example, because the 
bond is in [[default]]), any accrued amortized bond [[Premium]] accrued since the last actual interest 
payment would generally not be applied to the cost basis.  
o If an election to amortize bond [[Premium]] has been revoked, the Last Adjustment Date would be the 
date of the last interest payment in the year prior to the date of the revocation. This is because 
elections apply to a full year; therefore, a revocation made during the year would apply for that full 
calendar year. 
• For [[Bonds]] purchased at a market discount (non-OID) 
o If market discount is being deferred, the Last Adjustment Date would be the acquisition date of the 
lot since no accreted market discount has been applied to the cost basis. 
o If market discount is being included in current income, the Last Adjustment Date would be the 
[[settlement]] date of the transfer since accrued market discount is applied to basis daily and the 
delivering firm will report market discount through the [[settlement]] date of the transfer. 
o If the election to include accrued market discount in current income is revoked, the Last Adjustment 
Date would be December 31 of the year prior to the date of the revocation. This is because elections 
apply to a full year; therefore, a revocation made during the year would apply for that full calendar 
year. 
  

---

## Page 65

CBRS User Guide 
Best Practices 65 
• For OID [[Bonds]] purchased at a market discount, the Last Adjustment Date should be the last date as of 
which the cost basis for that lot was adjusted for a market discount. This is because OID accrues daily 
and the date the basis was last adjusted for OID is always the [[settlement]] date of the transfer. However, 
the date the bond was last adjusted for the market discount could be different under certain 
circumstances. 
o OID bond purchased at a bond [[Premium]] – Last Adjustment Date is the date of the last interest 
payment, as of which the basis was last adjusted for bond [[Premium]] (Acquisition [[Premium]] and OID 
nets to 0.00 so the relevant date is the last interest payment date used for amortization of bond 
[[Premium]])  
o OID bond purchased at a market discount - Last Adjustment Date is the last date the cost basis was 
adjusted for market discount. If market discount is deferred, Last Adjustment Date is the Acquisition 
Date.  
» If market discount is included in income currently, the Last Adjustment Date is the [[settlement]] 
date of the transfer since market discount accrues daily.  
» If the market discount election to include the discount in income currently was revoked, the Last 
Adjustment Date is December 31 of the year prior to the revocation (since elections always 
apply to a full calendar year). 
Carryover Offset (T) 
The amount of Amortized Bond [[Premium]] to be carried over to the date of disposition (The Current Cost basis 
should NOT be adjusted by this amount).  The Carryover Offset amount must be carried over until the 
disposition of the [[Asset]]. 
Note: 
This occurs in the instance where debt purchased at a Bond [[Premium]] is not amortized and then in a later year, the client 
revokes the decision. For example, if a client elects to not amortize in year 1, then subsequently changes their election to 
amortize going forward, the year 1 amortization would be placed in the Carryover Offset field. 
  

---

## Page 66

CBRS User Guide 
Best Practices 66 
Prior Year Mark to Market (T) 
The Prior Year Mark to Market field is exclusively used for Section 1256 options. Beginning January 1, 2016, 
cost basis for Section 1256 options must be submitted on the transfer statements. 
• If the 1256 [[Option]] was acquired prior to 12/31of the prior year, then report the prior year end fair-market 
value used in reporting unrealized profit or (loss) on open contracts in box 10 of the 1099-B   
• If the 1256 [[Option]] was acquired in the same year as the transfer, then submit zero in the Prior Year Mark 
to Market field. 
• For all assets other than 1256 options, leave this field blank. The CBRS output will show the blank on the 
output file. 
For example, a 1256 [[Option]] was acquired last year and transferred today. The original cost was $10, the 
year-end value was $12, and the current market value is $15. When reporting the cost basis for the 
transfer, populate as follows: 
Tax Lot Original Cost: $ 10 (optional) 
Tax Lot Current Cost: $ 10 
Prior Year Mark to Market: $ 12 
[[settlement]] Date (T) 
[[settlement]] date of the original acquisition for the Tax Lot being transferred.  
Best Practice: If [[settlement]] Date is unknown, this field should be populated with the date the accrual 
calculations began.  
The [[settlement]] Date field is conditionally required for covered fixed income. CBRS will reject the transaction if 
not populated for covered fixed income.  
Accrued Unrealized Market Discount (T) 
The amount of market discount on the fixed income security that has been accrued but not realized. 
Best Practice: This field should be populated for debt [[securities]] purchased at a market discount where the 
market discount has been deferred. The value should be the amount of the deferred market discount through 
the [[settlement]] date of the transfer.  
The Accrued Unrealized Market Discount is an optional field. 
Note: 
Below the Market Discount section (pg. 54) is a summary of scenarios and Best Practices applicable to populating the 
Accrued Unrealized Market Discount field. 

---

## Page 67

CBRS User Guide 
File Input and Output Through Common Data Transfer Service (CDTS) 67 
6. FILE INPUT AND OUTPUT THROUGH COMMON DATA 
TRANSFER SERVICE (CDTS)  
The Common Data Transfer Service (CDTS) is the [[DTCC]] proprietary file input and output management 
system. It enables [[DTCC]] and its participants to automate the exchange of files securely and reliably over a 
network link. Once a secure network connection is configured, minimal set-up is required to automate inbound 
and outbound file transfers. Two industry standard file transfer protocols are supported, FTP and Connect:  
Direct (NDM). [[DTCC]] operations staff actively monitors these systems and addresses any failed transmissions. 
Both systems are available in the test and production environments. 
• Input: The transaction input has a CDTS input header and CDTS input trailer. 
• Output: The transaction output has a CDTS output header, and a CBRS application output header, and a 
CBRS application output trailer. There is no CDTS output trailer. 
The following table shows the order of the header, transaction records, and trailer in the file: 
Input Output 
CDTS input header CDTS output header 
CBRS records CBRS application header 
CDTS input trailer CBRS records 
 CBRS application trailer 
 
For questions about CDTS, call the Customer Support Hotline at 1 888-382-2721, [[Option]] 5, and then [[Option]] 1. 
File Input  
CBRS uses only variable length input files. There are no fixed length input files. The CBRS input cut-off time is 
4:00 P.M. Eastern Time.  
Note: 
The Input SYSID for CBRS input files is 36708 for Production.  
A CDTS input header record is required. It is the first record in any file transmitted. The CDTS input trailer 
record is also required, and it is the last record in any file transmitted.  The record layouts for the CDTS input 
header and trailer records (named DATATRAK Header and Trailer in the layout) is available from the CBRS 
Technical Resources section in the [[DTCC]] Learning Center at:  
https://dtcclearning.com/products-and-services/equities-clearing/cbrs/cbrs-technical-resources.html 
  

---

## Page 68

CBRS User Guide 
File Input and Output Through Common Data Transfer Service (CDTS) 68 
Q The [[Asset]] and tax lot input records are always 1,000 bytes. The transaction output is always 
1,500. Why are these records “variable?”   
A While it may not be apparent in the current record layouts, the records have variable functionality built 
into them for future expansion. For now, the [[Asset]] and tax lot input records are always 1,000 bytes long, 
and the transaction output record is always 1,500 bytes long. In the future, the record layouts can be 
expanded to as large as 4,000 bytes. This extra room allows for more fields in case they become 
necessary in future versions of the system. This possible expansion gives the records the “variable” 
designation. We [[DO]] not make the records 4,000 bytes today because we [[DO]] not want to take up disk 
space that we [[DO]] not need. 
[[NSCC]]’s Automated Customer Account Transfer Service (ACATS) uses this feature. As an example, here 
is the Record Length field in the variable ACATS [[Asset]] Input record layout: 
Field 
Name 
Length Start End Type Opt/Req/Cond Comments 
Record 
Length 
4 3 6 NUM REQ [[Asset]] Type Record Length 
[[Option]] 497 
Mutual Fund 550 
Insurance 1700 
Foreign 831 
All Others 431 
 
 
These different lengths illustrate the use of a variable record. The length of the record varies based on the type 
of [[Asset]] in the record. CBRS is not currently using this feature, but the [[Option]] to use it in the future, if the need 
arises, is available. 
Q Can a firm send multiple files to CBRS during the day?   
A Yes. You can send multiple files each day, through both the computer-to-computer connection and 
WebDirect. CBRS combines all the input and processes it at the end of the day and sends the output in 
one file. 
Q If my firm does not have any CBRS transactions to submit to [[DTCC]] on a given day, can I send an 
empty file?   
A Yes, you can send an empty file with only a CDTS header. You can also not send any file at all. 
  

---

## Page 69

CBRS User Guide 
File Input and Output Through Common Data Transfer Service (CDTS) 69 
File Output: Transaction MRO 
A CBRS application header record is the first record in the CBRS transaction MRO file.  For the CBRS 
application header and trailer record layouts, see CBRS Header and CBRS Trailer. 
Note: 
The Output Product [[ID]] for the CBRS Transaction MRO is 02400264. 
The record layout for the CDTS output header record (named the AutoRoute Header in the layout) is available 
from the CBRS Technical Resources section in the [[DTCC]] Learning Center.  
Q If my firm does not have any CBRS transaction output for a given day (meaning my firm is not the 
submitter or receiver of any CBRS records), will I receive a transaction output file?   
A The answer is yes if you are set up to receive an empty file. When you set up your access to CBRS, you 
can ask to receive an empty CBRS transaction output file in this situation. The file will contain only a 
CDTS header. 
File Output: Cost Basis User Master File MRO 
The Cost Basis User Master File MRO does not have an application header. The file has a CDTS header. The 
record layout for the CDTS output header record (named the AutoRoute Header in the layout) is available from 
the CBRS Technical Resources section in the [[DTCC]] Learning Center.  
Note: 
The Output Product [[ID]] for the Cost Basis User Master File MRO is 02561666. 
Limits on When Output Files and Data are Available 
Files are stored in [[DTCC]] Web Portal for four business days. [[DTCC]] can retransmit files for fourteen calendar 
days.  
Data is available for viewing from the [[DTCC]] Web Portal from the Cost Basis Inquiry page. You can download 
these files in the Microsoft Excel (.xls) format for twenty-five business days.  
Note:  
After the twenty-five-business day window has passed, [[DTCC]] cannot be able to provide CBRS data to users. You are 
responsible for storing your data on a long-term basis. 
  

---

## Page 70

CBRS User Guide 
File Input and Output Through Common Data Transfer Service (CDTS) 70 
Input and Output Timing 
• Input: for today’s processing date, firms can submit CBRS records between 8 P.M. Eastern Time 
yesterday and 4 P.M. Eastern Time today.  
o Files submitted between 8 P.M. Eastern Time yesterday and 4 P.M. Eastern Time today should have 
today’s date in the header 
o Files with today’s header date, submitted between 4 PM and 8 PM today, are processed with 
tomorrow’s processing date 
o Files with tomorrow’s header date, submitted between 4 PM and 8 PM today, are rejected by CDTS 
• Output: for today’s processing date, CBRS transaction output and the Daily Deposit File for Transfer 
Agents is available by 9 P.M. Eastern Time today. The Cost Basis User Master File is available by 11 
P.M. Eastern Time today. 
Note: 
This schedule applies to input and output through both the automated computer-to-computer connection, and through 
[[DTCC]] Web Portal. 
Extension Guidelines 
If an extension is needed for any input submission, firms should use one of the following methods to obtain 
support:  
• Email [[NSCC]] Support at NSCCSupport@[[DTCC]].com. 
• Telephone [[DTCC]] Client Support at 1-888-382-2721 and follow the prompt for production support. 
If [[DTCC]], at its sole discretion, extends a deadline that would significantly impact reporting times, a 
communication is sent out.  
  

---

## Page 71

CBRS User Guide 
File Input and Output Through Common Data Transfer Service (CDTS) 71 
CBRS Application Output Header 
A CBRS application header record is the first record in any CBRS MRO file transmitted. The following table 
shows the layout of this application header: 
CBRS APPLICATION OUTPUT HEADER 
Description Length Start End Type Comments 
Record Type 1 1 1 A/N H 
Record Length 4 2 5 A/N 61 – Variable Length 
AutoRoute Product [[ID]] 8 6 13 A/N 02400264 
File Description 30 14 43 A/N Cost Basis Transaction MRO 
Distribution Side 4 44 47 A/N Last four digits of the distribution firm’s 
CBRS Account [[ID]] number 
Processing Date 8 48 55 A/N CCYYMMDD 
Multicycle Indicator 1 56 56 A/N Single Cycle = [space] 
Multicycle Number 4 57 60 A/N Zeroes  
Variable-Length Record 
Indicator 
1 61 61 A/N Variable Length = * 
Future Use 19 62 80 A/N Spaces 
End of Record 
  

---

## Page 72

CBRS User Guide 
File Input and Output Through Common Data Transfer Service (CDTS) 72 
CBRS Application Output Trailer 
A CBRS application trailer record is the last record in any CBRS MRO file transmitted. The following table 
shows the layout of this application trailer: 
CBRS APPLICATION OUTPUT TRAILER 
Description Length Start End Type Comments 
Record Type 1 1 1 A/N T 
Record Length 4 2 5 A/N 70 – Variable Length 
AutoRoute Product [[ID]] 8 6 13 A/N 02400264 
File Description 30 14 43 A/N Cost Basis Transaction MRO 
Distribution Side 4 44 47 A/N Last four digits of the distribution firm’s 
CBRS Account [[ID]] number 
Processing Date 8 48 55 A/N CCYYMMDD 
Multicycle Indicator 1 56 56 A/N Single Cycle = [space] 
Multicycle Number 4 57 60 A/N Zeroes  
Variable-Length Record 
Indicator 
1 61 61 A/N Variable Length = * 
Item Count 9 62 70 A/N Transmission count (includes Header and 
Trailer) 
Future Use 10 71 80 A/N Spaces 
End of Record 

---

## Page 73

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 73 
7. ACCESSING CBRS THROUGH THE [[DTCC]] WEB 
PORTAL 
You can access CBRS through the [[DTCC]] Web portal, a secure internet portal. After accessing CBRS, you 
can: 
• Create transactions. 
• Submit transactions in a batch. 
Note:  
Transactions submitted to a batch have not yet been sent to [[DTCC]]. 
• Send your batches of transactions to [[DTCC]]. 
• Download files. 
You can also edit data, search, or delete transactions, and upload a spreadsheet. This guide contains 
information about these steps, as well as all CBRS features available through the [[DTCC]] Web Portal. 
Logging on to the System 
To access CBRS through the [[DTCC]] Web Portal: 
1. Go to https://portal.[[DTCC]].com 
2. Enter your user [[ID]] and password, and then click Login. 
3. From Applications, click COST Basis to use CBRS in the production environment.  
 
Note 
To use CBRS in the testing environment, click Cost Basis PSE from the Available PSE, PSE2, and PTE Products section: 
  
If you have trouble logging on to the system, contact Client Support at 1-888-382-2721 or 1-212-855-8099 
and follow the prompt for support. 
  


---

## Page 74

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 74 
Creating CBRS Transactions 
You can create either an [[Asset]] or a tax lot record. An [[Asset]] record can be one of the four possible record 
content types: original, corrected, firm reject, or request. A tax lot record can be either an original record or a 
corrected record.  
A transaction refers to all assets that have the same transfer control number. Some transfer types, such as an 
ACATS transfer, can have multiple assets per transfer control number. Other transfer types, such as a free 
deliver order, have one [[Asset]] per transfer control number. Each [[Asset]] can include one or more tax lots. 
Assets are required for all transactions. Tax lots are required for transactions with a record content type of 
either original or corrected. 
To create transactions: 
Notes: 
• When you submit transactions in CBRS (after creating new transactions or modifying existing transactions), you are 
creating or modifying pending transactions that must then be sent to [[DTCC]]. For more information, see Sending a 
Batch to [[DTCC]]. 
• You can also create transactions through spreadsheet upload. For more information, see The Spreadsheet Upload 
Process. 
1. From the Transaction Inputs section of the CBRS home page, click Cost Basis Input. 
 
 
  


---

## Page 75

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 75 
2. From the Cost Basis Reporting Service page that appears, enter all the information you have regarding 
the transaction.  
The following figure shows the Transfer Information section of the Cost Basis Reporting Service page. 
Note:  
Required fields are identified with a red asterisk (*). 
 
 
3. In the [[Asset]] Information section, enter information for the first [[Asset]] for this transaction. 
Note:  
The tax lot input screen automatically appears when, in the [[Asset]] Record Content Indicator field, you choose 01 = 
Original [[Asset]] record or 02 = Corrected [[Asset]] record. If you choose 03 = Firm reject record or 04 = Request record, the 
tax lot input screen will not appear. No tax lots are associated with the Firm Reject or Request record types.  
 
 


---

## Page 76

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 76 
 
4. If you have more than one tax lot for this [[Asset]], click More Tax Lots, and then click Submit. 
The transaction page reappears, with the transaction and the [[Asset]] information already populated. 
5. Enter the additional tax lot information. Repeat the steps for each tax lot associated with this [[Asset]]. 
6. If you have more than one [[Asset]] for this transaction, finish entering the tax lot information. Next, click 
More Assets, and then click Submit. 
The transaction page reappears with the transaction information already populated. 
7. Enter the additional [[Asset]] information. 
8. Enter the tax lot information for the next [[Asset]]. 
9. Repeat the steps, as needed, until you have entered all the [[Asset]] and tax lot information for this 
transaction. 
Note: 
You must finish entering all the [[Asset]] and tax lot information associated with the transaction before clicking Submit 
the final time. You cannot add additional [[Asset]] or tax lot information for a transaction by editing an existing Cost Basis 
record. For information about adding additional [[Asset]] or tax lot to a transaction, see Adding More Assets to a 
Transaction or Adding More Tax Lots to a Transaction. 
10. Click Submit. 
The Previous transaction was processed successfully message appears. After you submit the transaction, 
CBRS adds it to the previously submitted transactions (if any exist). After you are finished entering all the 
transactions, follow the steps to send the batch to [[DTCC]]. For more information, see Sending a Batch to 
[[DTCC]]. CBRS processes all the files at the same time at the end of the day. 
  


---

## Page 77

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 77 
Working With Pending CBRS Transactions 
There are multiple ways to work with a transaction that is pending. In this section, learn about adding 
more assets, adding more tax lots, displaying transactions you have submitted, viewing all existing 
transactions, and using the search criteria to display a specific transaction. 
Adding Assets to CBRS Transactions 
To add more assets to a transaction: 
Follow these steps if you have already entered a transaction and need to enter another [[Asset]]. 
Note:  
When you submit transactions in CBRS (after creating new transactions or modifying existing transactions), you are 
creating or modifying pending transactions that must then be sent to [[DTCC]]. For more information, see Sending a Batch to 
[[DTCC]]. 
1. From the Transaction Inputs section of the CBRS home page, click Cost Basis Input. 
 
 
2. From the Cost Basis Reporting Service page that appears, enter the same Transfer Information that you 
entered previously. 
Note: 
Required fields are identified with a red asterisk (*). 


---

## Page 78

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 78 
 
  


---

## Page 79

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 79 
3. Enter information for the additional [[Asset]] for this transaction. 
 
4. Enter information for the first tax lot for this [[Asset]]. 
Note: 
The tax lot input screen automatically appears when, in the [[Asset]] Record Content Indicator field, you choose  
01 = Original [[Asset]] record or 02 = Corrected [[Asset]] record. If you choose 03 = Firm reject record or 04 = Request 
record, the tax lot input section does not appear. No tax lots are associated with the Firm reject or Request record 
types. 
 
5. If you have more than one tax lot for this [[Asset]], click the More Tax Lots radio button and click Submit. 
The transaction page reappears, with the transaction and the [[Asset]] information already populated. 
6. Enter the additional tax lot information. 
Repeat the steps for each tax lot associated with this [[Asset]]. 
7. If you have more than one [[Asset]] to add to this transaction, finish entering the tax lot information. Next, 
click More Assets, and then click Submit. 
The transaction page reappears, with the transaction information already populated. 
8. Enter the additional [[Asset]] information. 
9. Enter the tax lot information for the next [[Asset]]. 
  


---

## Page 80

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 80 
10. Repeat the steps, as needed, until you have entered all the additional [[Asset]] and tax lot information for this 
transaction. 
Note: 
You must finish entering all the [[Asset]] and tax lot information associated with the transaction before clicking Submit 
the final time. 
11. Click Submit. 
Adding More Tax Lots to an Existing Transaction 
To add more tax lots to an existing transaction: 
1. From the Transaction Input section of the CBRS home page, click Cost Basis Input. 
 
  


---

## Page 81

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 81 
2. From the Cost Basis Reporting Service page that appears, enter the same transfer information that you 
entered previously. 
Note: 
Required fields are identified with a red asterisk (*). 
 
3. Enter the [[Asset]] Information that you already entered for this [[Asset]]. 
 
  


---

## Page 82

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 82 
4. Enter the additional tax lot information for this [[Asset]]. 
Note:  
The tax lot input screen automatically appears when, in the [[Asset]] Record Content Indicator field, you choose  
01 = Original [[Asset]] record or 02 = Corrected [[Asset]] record. If you choose 03 = Firm reject record or 04 = 
Request record, the tax lot input section does not appear. No tax lots are associated with the Firm reject or Request 
record types. 
 
5. If you have more than one additional tax lot for this [[Asset]], click the More Tax Lots radio button and click 
Submit. 
The transaction page reappears, with the transaction and the [[Asset]] information already populated. 
6. Enter the additional tax lot information. 
Repeat the steps for each tax lot associated with this [[Asset]]. 
Note: 
You must finish entering all the [[Asset]] and tax lot information associated with the transaction before clicking Submit 
the final time. 
7. Click Submit. 
The Previous transaction was processed successfully. message appears. 
After you submit the transaction, CBRS adds it to the previously submitted transactions. After you are 
finished entering all transactions, follow the steps to send the batch to [[DTCC]]. For more information, see 
Sending a Batch to [[DTCC]]. CBRS processes all the files at the same time at the end of the day. 
  


---

## Page 83

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 83 
Listing Pending Transactions 
You can display transactions that you have submitted but have not yet sent to [[DTCC]]. You can either list all 
existing transactions or use search criteria to display specific transactions. After displaying a set of 
transactions, you can view, update, or delete transfer information, assets, and tax lots for those transactions. 
To list all pending CBRS transactions: 
1. From the Data Review/Send section of the CBRS home page, click Summary. 
 
2. From the Summary page that appears, click List. 
 
 
  


---

## Page 84

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 84 
3.  From the Transfer List page, view all of the current pending transactions. 
 
4. View Searching Pending Transactions. 
Searching Pending Transactions 
Display transactions that you have submitted but have not yet sent to [[DTCC]]. You can either list all 
existing transactions or use search criteria to display specific transactions. After displaying a set of 
transactions, you can view, update, or delete transfer information, assets, and tax lots for those 
transactions. 
To search pending transactions: 
1. From the Data Review/Send section of the CBRS home page, click Summary. 
 
  


---

## Page 85

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 85 
2. From the Summary page that appears, click Search. 
 
3. From the Cost Basis Search page that appears, type and select your search criteria. 
 
4. Click Search. 
The Transfer List page appears, displaying the transactions that match your selection criteria. 
 
Notes:  
To view, update, and delete transfer information for transactions displayed on the Transfer List page click the 
corresponding link in the Item Number column. For more information, see Viewing and Updating Transfer Information. 
To view, update, and delete [[Asset]] and tax lot information for transactions displayed on the Transfer List page click the 
corresponding link in the Number of Assets column. For more information, see Viewing and Updating Assets and Viewing 
and Updating Tax Lots. 


---

## Page 86

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 86 
Deleting Transactions 
You can delete transactions from the Transfer List page or the Transfer Information Update page. 
Deleting Transactions From the Transfer List 
To delete transactions from the transfer list: 
1. Display the transactions that you want to manage. 
You can use the search function to search for specific pending transactions or the list function to list all 
pending transactions. If you choose List, skip to step 3. If you use Search, continue to the next step. 
For more information, see Listing and Searching Pending Transactions. 
 
The Cost Basis Search page appears.  
2. From the Cost Basis Search page that appears, type and select your search criteria, and then click 
Search. 
 
  


---

## Page 87

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 87 
3. From the Transfer List page that appears, click the check box next to one or more transactions that you 
want to delete, and then click Delete. To select all transactions, click the Select All checkbox. 
Note:  
When you click Delete, the transfer information and all associated assets and tax lots are deleted. 
 
 
4. From the Cost Basis Transfer Information page that appears, click Delete. 
Note: 
When you click Delete, the transfer information and all associated assets and tax lots are deleted. 
 
  


---

## Page 88

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 88 
Deleting Transactions From the Transfer Information Update Page 
To delete transactions from the Transfer Information Update page: 
1. Display the transactions that you want to manage. 
You can use the search function to search for specific pending transactions or the list function to list all 
pending transactions. If you click List, skip to step 3. If you click Search, continue to the next step. 
For more information, see Listing and Searching Pending Transactions. 
 
 
2. From the Cost Basis Search page that appears, type and select your search criteria, and then click 
Search.  
 
 
3. From the Transfer List page that appears, click the Item Number for the transaction that you want to 
delete. To select all transactions, click Select All. 
 
  


---

## Page 89

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 89 
4. From the Cost Basis Transfer Information page that appears, click Delete. 
Note:  
When you click Delete, the transfer information, all associated assets, and tax lots are deleted. 
 
Editing Transfer Information, [[Asset]] Records, and Tax Lot Records 
There are multiple ways to update a transaction that you have submitted. View the following sections to 
manage transfer information and manage assets and tax lots. 
Viewing and Updating Transfer Information 
You can view and update the transfer information for transactions you have submitted but have not yet sent to 
[[DTCC]]. 
Note:  
When you submit transactions in CBRS (after creating new transactions or modifying existing transactions), you are 
creating or modifying pending transactions that must then be sent to [[DTCC]]. For more information, see Sending a Batch to 
[[DTCC]]. 
To view and update transfer information: 
1. Display the transaction that you want to manage. 
You can use the list function to list all pending transactions, or you can use the search function to search 
for specific pending transactions. For more information, see Listing and Searching Pending Transactions. 
If you choose List, skip to step 3. If you use Search, continue to the next step. 


---

## Page 90

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 90 
 
 
2. From the Cost Basis Search page that appears, type and select your search criteria, and then click 
Search. 
 
3. From the Transfer List page that appears, click the Item Number for the transaction that you want to 
manage. 
 
  


---

## Page 91

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 91 
4. From the Cost Basis Transfer Information page that appears, update the transfer information, and then 
click Submit. 
Note:  
You cannot modify the following fields on the Transfer Information Update page: 
• Submitting Firm 
• Contra Firm Type 
• [[Asset]] Record Content Indicator 
• Transaction Type 
 
Viewing and Updating Assets 
For transactions that you have submitted but have not yet sent to [[DTCC]], you can view and update the assets 
assigned to those transactions. 
Note:  
When you submit transactions in CBRS (after creating new transactions or modifying existing transactions), you are 
creating or modifying pending transactions that must then be sent to [[DTCC]]. For more information, see Sending a Batch to 
[[DTCC]]. 
  


---

## Page 92

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 92 
To view and update an [[Asset]]: 
1. Display the transaction that you want to manage. 
You can use the list function to list all pending transactions, or you can use the search function to [[Locate]] a 
specific pending transaction. For more information, see Listing and Searching Pending Transactions. 
If you choose List, skip to step 3. If you use Search, continue to the next step. 
 
 
2. From the Cost Basis Search page that appears, type and select your search criteria, and then click 
Search. 
 
3. From the Transfer List page that appears, click the link in the Number of Assets column for the 
transaction that you want to manage. 
 
  


---

## Page 93

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 93 
4. From the Assets List page that appears, click the [[Asset]] Number link for the [[Asset]] that you want to modify. 
 
 
5. From the Cost Basis [[Asset]] page that appears, modify the [[Asset]] details, as needed, and then click 
Submit. 
 
  


---

## Page 94

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 94 
Deleting Assets 
You can delete assets through the Assets List or Update [[Asset]] page. 
Notes  
• When you delete an [[Asset]], all tax lots associated with that [[Asset]] are also deleted. 
• You cannot delete the last [[Asset]] for a transaction. 
• When you submit transactions in CBRS (after creating new transactions or modifying existing transactions), you are 
creating or modifying pending transactions that you must then send to [[DTCC]]. For more information, see Sending a 
Batch to [[DTCC]]. 
To delete assets through the Assets List page: 
1. Display the transaction that you want to manage. 
You can use the list function to list all pending transactions, or you can use the search function to search 
for specific pending transactions. For more information, see Listing and Searching Pending Transactions. 
If you choose List, skip to step 3. If you use Search, continue to the next step. 
 
 
2. From the Cost Basis Search page that appears, type and select your search criteria, and then click 
Search. 
 
  


---

## Page 95

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 95 
3. From the Transfer List page that appears, click the link in the Number of Assets column for the 
transaction that you want to manage. 
 
 
4. From the Assets List page that appears, click the check box next to one or more assets.  
To select all assets, click the Select All checkbox. 
 
5. Click Delete. 
  


---

## Page 96

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 96 
To delete assets through the Update [[Asset]] page: 
1. Display the transaction that you want to manage. 
You can use the list function to list all pending transactions, or you can use the search function to search 
for specific pending transactions. For more information, see Listing and Searching Pending Transactions. 
If you choose List, skip to step 3. If you use Search, continue to the next step. 
 
2. From the Cost Basis Search page that appears, type and select your search criteria, and then click 
Search.  
 
 
3. From the Transfer List page that appears, click the Number of Assets link for the transaction that you 
want to manage. 
 
  


---

## Page 97

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 97 
4. From the Assets List page that appears, click the [[Asset]] Number link for the transaction that you want to 
delete 
 
5. The Cost Basis [[Asset]] page appears, click Delete. 
Note:  
When you click Delete, the transfer information and all associated assets and tax lots are also deleted. 
 
  


---

## Page 98

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 98 
Viewing and Updating Tax Lots 
For transactions that you have submitted but have not yet sent to [[DTCC]], you can view and update the tax lots 
assigned to assets for those transactions. 
To view and update the tax lots: 
Note:  
When you submit transactions in CBRS (after creating new transactions or modifying existing transactions), you are 
creating or modifying pending transactions that must then be sent to [[DTCC]]. For more information, see Sending a Batch to 
[[DTCC]]. 
1. Display the transaction that you want to manage. 
You can use the list function to list all pending transactions, or you can use the search function to search 
for specific pending transactions. For more information, see Listing and Searching Pending Transactions. 
If you choose List, skip to step 3. If you use Search, continue to the next step. 
 
 
2. From the Cost Basis Search page that appears, type and select your search criteria, and then click 
Search. 
 
 
  


---

## Page 99

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 99 
3. From the Transfer List page that appears, click the link in the Number of Assets column for the 
transaction that you want to manage. 
 The  
4. From the Assets List page, click the link in the Number of Tax Lots column for the [[Asset]] that you want to 
modify. 
 The  
5. From the Tax Lot List page that appears, click the link in the Tax Lot Number column for the tax lot that 
you want to manage. 
 
  


---

## Page 100

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 100 
6. From the Cost Basis Tax Lot page that appears, modify the tax lot details, as needed, and then click 
Submit. 
 
Deleting Tax Lots 
For transactions that you have created but have not yet sent to [[DTCC]], you can delete the tax lots assigned to 
assets for those transactions. 
You can delete tax lots through the Tax Lot List page or through the Cost Basis Tax Lot page. You cannot 
delete the last tax lot for a transaction. 
Note:  
When you submit transactions in CBRS (after creating new transactions or modifying existing transactions), you are 
creating or modifying pending transactions that must then be sent to [[DTCC]]. For more information, see Sending a Batch to 
[[DTCC]]. 
To delete tax lots through the Tax Lot List page: 
1. Display the transaction that you want to manage. 
You can use the list function to list all pending transactions, or you can use the search function to search 
for specific pending transactions. For more information, see Listing and Searching Pending Transactions. 
If you choose List, skip to step 3. If you use Search, continue to the next step. 
 
  


---

## Page 101

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 101 
2. From the Cost Basis Search page that appears, type and select your search criteria, and then click 
Search.  
 
 
3. From the Transfer List page that appears, click the Number of Assets link for the transaction that you 
want to delete. 
 
4. From the Assets List page that appears, click the Number of Tax Lots link for the [[Asset]] that you want to 
delete. 
 
  


---

## Page 102

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 102 
5. From the Tax Lot List page that appears, click the checkbox next to one or more tax lots.  
To select all of the tax lots, click Select All. 
 
6. Click Delete. 
 
To delete tax lots through the Cost Basis Tax Lot page: 
1. Display the transaction that you want to manage. 
You can use the list function to list all pending transactions, or you can use the search function to search 
for specific pending transactions. For more information, see Listing and Searching Pending 
Transactions. 
If you choose List, skip to step 3. If you use Search, continue to the next step. 
 
2. From the Cost Basis Search page, type and select your search criteria, and then click Search. 
 
  


---

## Page 103

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 103 
3. From the Transfer List page, click the Number of Assets link for the transaction that you want to manage. 
 
4. From the Assets List page, click the Number of Tax Lots link for the [[Asset]] that you want to modify. 
 
5. From the Tax Lot List page that appears, click the Tax Lot Number link for the tax lot that that you want to 
manage. 
 
 
  


---

## Page 104

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 104 
6. From the Cost Basis Tax Lot page, click Delete. 
 
Working With CBRS Batches 
When you submit transactions in CBRS (after creating new transactions or modifying existing 
transactions), you are creating pending transactions that must then be sent to [[DTCC]]. In this section we 
will show you how to send a batch to [[DTCC]], view a sent batch, verify that your file was sent successfully, 
and resend a batch. 
Sending a Batch to [[DTCC]] 
When you submit transactions in CBRS (after creating new transactions or modifying existing transactions), 
you are creating pending transactions that must then be sent to [[DTCC]]. You can send your pending 
transactions to [[DTCC]] as a single batch. 
To send a batch to [[DTCC]]: 
1. From the Data Review/Send section of the CBRS home page, click Send. 


---

## Page 105

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 105 
 
  

---

## Page 106

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 106 
2. From the Send page that appears, click the check box in the Select column next to the product that you 
want to send. 
Note:  
To display a list of transactions in a batch, click the Cost Basis link in the Product column. 
 
 
3. Click Submit. 
4. Wait for the message informing you that the batch was sent to DATATRAK. 
 
If you [[DO]] not receive the following message, resend the batch. For more information, see Resending a 
Batch. 
  


---

## Page 107

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 107 
Viewing Sent Batches 
You can view the transfer information, [[Asset]], and tax lot details for transactions that you have sent to [[DTCC]]. 
To view a sent batch: 
1. From the Data Review/Send section of the CBRS home page, click Sent Batches. 
 
 
2. From the Sent Batches page, click the Batch Number link for the batch that you want to view. 
 
3. From the Sent Batch page, view the list of products that were sent in that batch. Click the Cost Basis link 
to view the product. 
 
  


---

## Page 108

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 108 
4. From the Cost Basis List page, view the [[BASIC]] information about the transactions. 
 
5. Perform one of the following actions: 
o Click the link in the Item Number column for the Cost Basis Transfer Information page that you want 
to view. 
o Click the link in the Number of Assets column for the Cost Basis Search List Assets page that you 
want to view. 
Verifying the File Sent Successfully Using the Confirms Utility 
After sending data to [[DTCC]], you can use the Confirms utility to verify that the file was sent successfully. 
To confirm that your file was sent successfully: 
1. After sending your data, make a note of the batch number displayed on the page. 
For more information about sending batches, see Sending a Batch to [[DTCC]] and Uploading the 
Spreadsheet. 
2. Return to the portal page (that is, the page that displays the production products that are available to you). 
From Available Production Products, click Utilities. 
 
 
3. From the File and Report Utilities page that appears, click Confirms. 
You should see a link displaying the batch you have submitted. This tells you your batch was submitted. 
  


---

## Page 109

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 109 
4. To verify that your batch was accepted, click the link. 
The Confirm Display page appears, providing details about your data submission. 
 
CBRS displays either ACCEPTED or REJECTED in the lower-left corner. 
Resending Batches 
To resend a batch: 
1. From the Data Review/Send section of the CBRS home page, click Sent Batches. 
 
  


---

## Page 110

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 110 
2. From the Sent Batches page that appears, [[Locate]] the batch number that you want to resend. 
 
3. Click the appropriate check box in the Re-Send column. 
4. Click Re-send. 
The Sent Batches page appears with a Batch Number: xxxxxxxxx was resent message similar to the 
following figure: 
 
Uploading Records to CBRS 
As an alternative to using the Transaction Input pages of the CBRS web interface (see Creating Transactions), 
you can submit your cost basis records to CBRS by entering your [[Asset]] and tax lot records into a Microsoft 
Excel spreadsheet, and then uploading that spreadsheet to CBRS through the [[DTCC]] Web Portal. 
Notes  
• Your spreadsheet cannot exceed 1000 rows.  
• CBRS supports MS Excel 2007 or later (.xlsx). Spreadsheets created with earlier versions may not work. 
  


---

## Page 111

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 111 
Overview of the CBRS Upload Process 
To use CBRS uploaded spreadsheets: 
1. Download the most recent version of the spreadsheet template. See Using the Most Recent Spreadsheet 
Template. 
 
 
2. Enter your new assets and tax lots.  
See Preparing the Upload Spreadsheet and Example Spreadsheets. 
 
 
 


---

## Page 112

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 112 
3. Save the spreadsheet as an Excel Workbook file. 
 
 
4. From the CBRS Upload page, submit the upload spreadsheet you have created. See Uploading the 
Spreadsheet. 
 
  


---

## Page 113

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 113 
5. After choosing your spreadsheet, click Submit to upload it. 
• If the system rejects your spreadsheet, investigate the issue, correct the errors, and submit the 
spreadsheet again. See Reviewing and Correcting Upload Errors. 
• If the system accepts your spreadsheet, the Batch Confirm page appears. For future inquiries, make a 
note of the batch number assigned to your upload. See Verifying That Your File Was Sent Successfully 
(Using the Confirms Utility). 
 
  


---

## Page 114

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 114 
Downloading CBRS Spreadsheet Templates 
To prepare spreadsheets for upload, make sure you have the latest version of the spreadsheet 
template.  
1. From the CBRS Upload section of the Cost Basis Reporting Service home page, click CBRS Upload 
Tool. 
2. In the Spreadsheet Template section of the CBRS Upload page, click the Click to download 
Spreadsheet Template link. 
 
The response depends on which browser you are using and how that browser is configured. In the most 
typical setup, you are prompted to either open or save the file. 
 
3. Perform one of the following actions: 
o To open the file, click Open.  
o To save the file, click Save. 
After you have downloaded and saved the spreadsheet template, you are ready to create new 
spreadsheets containing new [[Asset]] and tax lot records.   


---

## Page 115

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 115 
For Earlier Versions of Microsoft Excel 
After you have downloaded and saved the spreadsheet template (see Downloading CBRS Spreadsheet 
Template), you are ready to create new spreadsheets containing new [[Asset]] and tax lot records. 
Notes  
CBRS supports Microsoft Excel 2007 or later (.xlsx). Spreadsheets created with earlier versions may not work. If you are 
using a pre-2007 version of Microsoft Excel to create your spreadsheet, you may see a message regarding Microsoft Excel 
versions when you open the template.  
From the following message page, click OK to continue and open the template: 
 
When you save your spreadsheet, save it in compatibility mode. Click Save As, and then choose the 
compatibility mode [[Option]]. 
Spreadsheet Template Column Headers 
After you open the spreadsheet template, you will notice that it is color-coded. The following table shows what 
each color signifies. 
 
Headings for [[Asset]] record fields have a blue 
background. 
 
Headings for required [[Asset]] record fields have 
a blue background with red text. 
 


---

## Page 116

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 116 
 
Headings for tax lot record fields have a beige 
background. 
 
To display hints for a column, move your mouse over any column heading with a red triangle in the upper-right 
corner. 
 
  


---

## Page 117

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 117 
Spreadsheets at a Glance 
Here are the key points you need to understand when setting up your spreadsheet: 
• Enter [[Asset]] details on the left side of the spreadsheet, from the blue column headings. Enter tax lot details 
on the right side of the spreadsheet, from the beige column headings. 
 
• Enter an [[Asset]] and the first tax lot for an [[Asset]] on the same row. 
 
 
  


---

## Page 118

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 118 
• Use the rows below an [[Asset]] to add any additional tax lots for that [[Asset]]. 
 
 
• Add additional assets and tax lots as needed. 
 


---

## Page 119

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 119 
Tips: 
• [[DO]] not insert rows above row 3 (the column headings). 
• [[DO]] not modify the order of the columns. 
• [[DO]] not modify the format of the columns. 
• Your spreadsheet can have a maximum of 1000 rows. 
• Use the drop-down menus where available.  
• For date fields, the required format is MM/DD/YYYY. For example, enter January 3, 2011, as "01/03/2011" 
(without the quotes). 
• For [[participant]] [[ID]] fields, leading zeros are not required. For example, you can enter 000000123 as simply 
123. 
• Not all fields are required. 
• Some fields are conditional; that is, data from one field may influence whether another field is required. 
For more information about required and conditional fields, see the CBRS Users section of the [[DTCC]] 
Learning website. 
Adding an [[Asset]] With One Tax Lot 
In this case, you'll enter both the [[Asset]] and tax lot details on the first row. The [[Asset]] information appears from 
the blue headings on the left half of the spreadsheet; the tax lot information appears from the beige headings 
on the right half of the spreadsheet. 
1. In the CBRS Record Type column of the first row, use the drop-down menu to select A (for [[Asset]]). 
2. Type all the applicable [[Asset]] information in the [[Asset]] columns, identified by the column headings with a 
blue background. 
 
  


---

## Page 120

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 120 
3. In the same row, scroll to the right and from the beige column headings, type the tax lot details. 
 
Adding Assets With Multiple Tax Lots 
When you are entering an [[Asset]] with more than one tax lot, you will enter the additional tax lot information 
below the first tax lot.  
1. Type the first [[Asset]] and tax lot in the first row. 
For more information, see Adding an [[Asset]] with One Tax Lot. 
2. For each additional tax lot, [[DO]] the following: 
a. In the CBRS Record Type column, use the drop-down menu to select T (for additional tax lots). 
 
Note:  
The [[Asset]] fields in this row now appear in blue. Because the [[Asset]] fields for the additional tax lots are the same as the 
original [[Asset]], you should not retype this information. 


---

## Page 121

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 121 
 
b. Scroll to the right side of the spreadsheet, and from the beige columns, type the information for the 
next tax lot. 
 
c. Repeat the steps for each additional tax lot. 
Adding Multiple [[Asset]] Records 
You may have several assets to upload, some with just one tax lot and others with multiple tax lots. 
To add multiple [[Asset]] records: 
1. Type the first [[Asset]] and tax lot in the first row. 
For more information, see Adding an [[Asset]] with One Tax Lot. 
2. For each additional [[Asset]], [[DO]] the following: 
a. In the CBRS Record Type column, use the drop-down menu to select A (for [[Asset]]). 
b. Type all the [[Asset]] information in the [[Asset]] columns, identified by the column headings with a blue 
background. 
c. In the same row, scroll to the right side of the spreadsheet, and from the beige column headings, 
type the information for the first tax lot. 
3. For each additional tax lot within a specific [[Asset]], [[DO]] the following: 
a. In the CBRS Record Type column, use the drop-down menu to select T (for additional Tax lots). 
Note: The [[Asset]] fields in this row now appear in blue. Because the [[Asset]] fields for the additional tax 
lots are the same as the original [[Asset]], you should not retype this information. 
b. Scroll to the right side of the spreadsheet, and from the beige columns, type the information for the 
next tax lot. 
c. Repeat these steps for each additional tax lot. 


---

## Page 122

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 122 
 
 


---

## Page 123

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 123 
Adding an [[Asset]] Without a Tax Lot (Firm Reject and Request Records Only) 
If you are submitting firm reject or request records, you can add an [[Asset]] record on the spreadsheet without a 
tax lot. For more information, see the CBRS Users section of the [[DTCC]] Learning website. 
1. Enter the first [[Asset]] record and tax lot in the first available row. 
2. In the CBRS Record Type column, use the drop-down menu to select A (for [[Asset]]). 
3. Type all the [[Asset]] information in the [[Asset]] columns, identified by the column headings with a blue 
background. 
CBRS Spreadsheet Examples 
The examples in this section demonstrate completed spreadsheets for various scenarios. 
Example One: An [[Asset]] With One Tax Lot 
The [[Asset]] information and tax lot information all appear on the same row. The blue headings indicate [[Asset]] 
fields while the beige headings indicate tax lot fields. This is the left side of the spreadsheet, with one [[Asset]] 
entered: 
 
This is the right side of the same spreadsheet, with the one tax lot entered: 


---

## Page 124

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 124 
 
Example Two: An [[Asset]] With Multiple Tax Lots 
The [[Asset]] and the first tax lot appear on one row, followed by the additional tax lots on subsequent rows. For 
the additional tax lots, the [[Asset]] fields are filled with blue, indicating this information is the same as the first 
[[Asset]] record and should not be retyped. The following figure shows the left side of the spreadsheet, with one 
[[Asset]] entered and multiple tax lots added: 
 
  


---

## Page 125

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 125 
The following figure shows the right side of the same spreadsheet, showing the tax lot details added from the 
beige column headings.  
Note  
The first tax lot appears on the same row as the [[Asset]]. Each additional tax lot displays in the next rows below. 
 
Example Three: Multiple [[Asset]] Records 
Each new [[Asset]] includes one tax lot record on the same row. Additional tax lot records appear on subsequent 
rows. Here is the [[Asset]] side of a spreadsheet with multiple assets: 
 


---

## Page 126

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 126 
Here is the tax lot side of a spreadsheet with multiple assets: 
 
  


---

## Page 127

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 127 
Uploading the CBRS Spreadsheet 
After you have prepared your spreadsheet (see Preparing the Upload Spreadsheet), you can upload it through 
the CBRS web interface. CBRS processes the records you upload at the end of the day. 
To upload the spreadsheet: 
1. From the CBRS Upload section of the Cost Basis Reporting Service home page, click CBRS Upload 
Tool. 
2. From the CBRS Upload page that appears, click Browse. 
3. [[Locate]] the spreadsheet on your computer and select it. 
4. Click Submit to upload your spreadsheet. 
 
CBRS validates your spreadsheet for the following: 
o File type (must be .xls or .xlsx) 
o Number of rows (must be less than 1000) 
o CBRS Record Type (must be A, for [[Asset]], or T, for tax lot) 
o Submitting Firm Number and Submitting Firm Type (must match your firm) 
If all the records on your spreadsheet [[DO]] not pass the validation described earlier, CBRS rejects your 
spreadsheet and displays a rejection error message. 
 
If the system accepts your spreadsheet, the Batch Confirm page appears. For future inquiries, make a 
note of the batch number assigned to your upload. 
 
  


---

## Page 128

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 128 
When your records reach CBRS, it performs additional validations and produces output to you at the end of the 
day. 
Note:  
After CBRS produces this output, you can use the Cost Basis Inquiry feature that evening or the next business day to view 
your records. You can also use this feature to research any errors that may have resulted from the validations performed at 
the end of the day. After you successfully submit your spreadsheet, you cannot view your records until the end-of-day 
processing has been completed. 
For more information, see Reviewing and Correcting Upload Errors. 
Viewing and Modifying Records After Uploading 
After end-of-day processing, CBRS produces its transaction output to various files, such as the Transaction 
End of Day ([[EOD]]) Download file. You can use this file to view the records you submitted, as well as the 
records you received. 
You can use the Cost Basis Inquiry search function to verify that the records you submit through spreadsheet 
upload have been added to the CBRS database. For example, you can create a search using System Rejected 
or System Accepted as selection criteria, as highlighted in the figure. For more information about how to search 
for records in the CBRS database, see Searching CBRS Transactions. 
 
Notes  
When you submit CBRS transactions through spreadsheet upload, those records go directly to the CBRS mainframe 
database. You cannot view or modify these records in pending status as you can with transactions that you enter through 
manual data entry on the Cost Basis Input page.  


---

## Page 129

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 129 
Modifying Uploaded Information 
To modify details for any records that you have already uploaded, simply resubmit those records on a new 
spreadsheet. You cannot use the Transaction Input pages of CBRS web interface to edit the records you have 
uploaded through spreadsheet. For more details, see Preparing the Upload Spreadsheet. 
Note  
Because these records have already been submitted to the CBRS mainframe database, you should resubmit your records 
using the code for corrected records (02) in the Record Content Indicator column. 
Verifying the File Sent Successfully (Using the Confirms Utility) 
After sending data to [[DTCC]], use the Confirms utility to verify that the file was sent successfully. 
To verify that the file was sent successfully using the Confirms utility: 
1. After sending your data, make a note of the batch number displayed on the page. 
For more information about sending batches, see: Sending a Batch to [[DTCC]] and Uploading the 
Spreadsheet. 
2. Return to the portal page (that is, the page that displays the production products that are available to you). 
3. From Available Production Products, click Utilities. 
 
4. From the File and Report Utilities page that appears, click Confirms. 
A link displaying the batch that you have submitted appears. 
 
  


---

## Page 130

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 130 
5. To verify that your batch was accepted, click the link. 
The Confirm Display page appears, providing details about your data submission. 
 
CBRS displays either ACCEPTED or REJECTED in the lower-left corner. 
Reviewing and Correcting Spreadsheet Errors 
Review and correct the errors that you see immediately and after the end of day processing. 
Errors That You See Immediately Upon Submission 
When you upload transactions through spreadsheet, CBRS immediately checks for the following: 
• File type (must be .xls or .xlsx) 
• Number of rows (must be less than 1000) 
• CBRS Record Type (must be A, for [[Asset]], or T, for tax lot) 
• Submitting Firm Number and Submitting Firm Type (must match your firm) 
When the errors are found, CBRS displays an error message on the web interface.  
 
To correct the errors, modify the information, as needed, on your spreadsheet and repeat the upload process.  
Note  
Because these records have not yet been submitted to the CBRS mainframe database, you should resubmit your records 
using the code for original records (01) in the Record Content Indicator column. 
  


---

## Page 131

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 131 
Errors That You See After End-of-Day Processing 
For transactions on spreadsheets that pass the initial validation, CBRS performs additional validations at the 
end of the day. During end-of-day processing, CBRS checks for badly formatted data, incorrect or missing 
data.  
To view any errors generated by end-of-day processing, you can look at the Transaction End of Day ([[EOD]]) 
download file. You can use this file to view the records that you submitted as well as the records that you have 
received.  
You can also use the Cost Basis Inquiry search to display errors generated by end-of-day processing. For 
example, to display all transactions that were system rejected, create a search that specifies a System Status 
of System Rejected, as shown in the following figure: 
 
When you display the CBRS [[Asset]] Detail or the CBRS Tax Lot Detail pages, CBRS provides details about the 
error condition that you need to correct. 


---

## Page 132

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 132 
Here is an example of the CBRS [[Asset]] Detail page for an [[Asset]] record with errors:
 
Here is an example of the CBRS Tax Lot Detail page for a tax lot record with errors: 
 
For more information about how to use the Cost Basis Inquiry, see Searching CBRS Transactions.  
To correct the errors, upload a spreadsheet containing the corrected records. You can upload only the 
transactions that you want to correct, or you can upload all your transactions. 
Note  
Because these records have already been submitted to CBRS, you should resubmit your records using the code for 
corrected records (02) in the Record Content Indicator column. 


---

## Page 133

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 133 
Searching CBRS Transactions 
You can perform cost basis transaction inquiries using one of the following methods: 
• Quick Search: Specify a CBRS control number. 
• Advanced Search: Enter a combination of search criteria. 
You can display only those transactions for which your firm is either the submitter or receiver. The transactions 
that match your search criteria appear on the bottom half of the page. When a transaction has more than one 
[[Asset]], CBRS displays each [[Asset]] on a separate row. 
After displaying your search results, you can display details for specific assets and for the tax lots associated 
with those assets. 
Cost Basis Inquiry screens, including the download function, may not be available when the application is 
processing records. This processing occurs four times per day, at approximately 9:15 A.M., 11:15 A.M., 
1:15 P.M., and 4:15 P.M. Eastern Time. At these times, you may not be able to use the inquiry or inquiry 
download functions. The screens automatically become available again when processing is complete. If you 
encounter an error at approximately these times, try your inquiry again later. 
Using Quick Search 
To perform a quick search: 
1. From the Data Inquiry section of the CBRS page, click Cost Basis Transaction Inquiry: 
 
  


---

## Page 134

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 134 
2. In the Quick Search section of the Cost Basis Transaction Inquiry page, type the CBRS Control Number. 
 
3. Click Search. 
The Cost Basis Transaction Inquiry page updates to display your search results, one row for each [[Asset]] 
found for the transactions that match your search criteria.  
 
4. To download data associated with the transaction displayed, click the selection boxes for specific assets 
and then click Download Selected Items. 
Your data becomes available for download through the Data Files page. For more information, see 
Viewing Cost Basis Files. 
  


---

## Page 135

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 135 
5. To view the data associated with a displayed transaction, click the CBRS Control Number link next to 
that transaction. 
The CBRS [[Asset]] page appears.  
 
6. From the CBRS [[Asset]] page, you can view either the detailed [[Asset]] record or the associated tax lots. 
o To view the detailed [[Asset]] record, click [[Asset]] Details. 
o To view the associated tax lots, click a link in the Tax Lot Sequence Number column.  
7. When you click [[Asset]] Details, the CBRS [[Asset]] Detail page appears. To export this data to Excel, click 
Export to Excel. 
 
  


---

## Page 136

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 136 
8. When you click a link in the Tax Lot Sequence Number column, the CBRS Tax Lot Detail page appears. To 
export this data to Excel, click Export to Excel. 
 
  


---

## Page 137

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 137 
Using Advanced Search 
To perform an advanced search: 
1. From the Transaction Inquiry section of the CBRS home page, click Cost Basis Transaction Inquiry. 
 
 
2. From the Cost Basis Transaction Inquiry page, use the fields provided in the Advanced Search section, 
enter your search selection criteria. 
 
  


---

## Page 138

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 138 
3. Click Search.  
CBRS displays your search results in the lower portion of the page. CBRS displays one row for each 
[[Asset]] found for the transactions that match your search criteria. 
 
4. To download data associated with the transaction displayed, click the selection boxes for specific assets, 
and then click Download Selected Items.  
 
Your data becomes available for download through the Data Files page. It takes approximately 15 to 60 
minutes to create the file, depending on the amount of data in the request. For more information, see 
Downloading Cost Basis Files. 
  


---

## Page 139

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 139 
Displaying [[Asset]] and Tax Lot Details 
To display [[Asset]] and tax lot details: 
1. Complete either a quick search or an advanced search. See Advanced Search and Quick Search. 
Note: 
CBRS displays one row for each [[Asset]] found for the transactions that match your search criteria. 
2. From the Cost Basis Transaction Inquiry page, in the search results section, in the row for the [[Asset]] that 
you are interested in, click the CBRS Control Number. 
The CBRS [[Asset]] page appears. The CBRS [[Asset]] page displays information for the [[Asset]] you chose, 
along with a list of tax lots submitted for that [[Asset]]. 
 
 
3. To download data associated with the tax lots displayed, click the selection boxes for specific tax lots, and 
then click Download Selected Items.  
Your data becomes available for download through the Data Files page. It takes approximately 15 to 60 
minutes to create the file, depending on the amount of data in the request. For more information, see 
Downloading Cost Basis Files. 
4. From the CBRS [[Asset]] page, you can display additional [[Asset]] details or tax lot details: 
» To display additional [[Asset]] details, click [[Asset]] Details. The CBRS [[Asset]] Detail page appears, 
displaying additional [[Asset]] details, including the edit status for each field.  
Note: To open an Excel spreadsheet displaying the information about the [[Asset]] Details page, 
click Export to Excel. 
» To display tax lot details, in the Tax Lot List section, click the link in the Tax Lot Sequence 
Number column for the tax lot that you are interested in. The CBRS Tax Lot Detail page 
appears, displaying additional tax lot details, including the edit status for each field.  
Note: To open an Excel spreadsheet displaying the information about the CBRS Tax Lot Detail 
page, click Export to Excel. 
  


---

## Page 140

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 140 
Searching for CBRS Users 
You can search for: 
• Searching for Active CBRS Accounts 
• Searching for Inactive CBRS Accounts 
Searching for Active CBRS Accounts 
To search for an active CBRS account: 
1. From the Data Inquiry section of the CBRS home page, click Cost Basis User Inquiry. 
 
 
2. From the Cost Basis User Inquiry page, type the Firm Number and select the Firm Type. 
 
  


---

## Page 141

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 141 
3. Click Search. 
The Cost Basis User Inquiry page updates to display your search results. The results display the Active 
Firm that matches your search criteria. 
 
Searching for Inactive CBRS Accounts 
To search for an inactive CBRS account: 
1. From the Data Inquiry section of the CBRS home page, click Cost Basis User Inquiry.  
 
2. From the Cost Basis User Inquiry page, type the Firm Number and select the Firm Type. If the Firm 
Number is not known, populate the Firm Number with the Inactive account number known and select the 
appropriate Firm Type. 


---

## Page 142

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 142 
 
3. If the inactive account is a FED number and short name combination being used to find the active CBRS 
Account number, populated the Account number with the Fed number and select one of the associated 
Fed Short Names from the drop-down menu. 
 
  


---

## Page 143

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 143 
4. Click Search. 
5. View the returned results for the CBRS account number. 
 
  


---

## Page 144

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 144 
Downloading and Viewing Cost Basis Files and Reports 
You can view and download reports. You can also download data sets that you have requested through the 
Cost Basis Inquiry page. For more information, see Searching CBRS Transactions. 
Downloading Cost Basis Files 
To download a cost basis file: 
Note  
If your firm subscribes to AutoRoute products for direct delivery of machine-readable output (MRO) files, you cannot take 
the Web MRO. 
1. From the CBRS Output section of the CBRS home page, click Cost Basis Output Files. 
 
The Data Files page appears. 
2. In the drop-down menu provided, select the firm number and firm type, as highlighted in the following 
figure, and then click Submit: 
2.  


---

## Page 145

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 145 
3. Click the link associated with the file name of the file or report that you want to download and view.  
 
CBRS displays the reports, depending on which files you have subscribed to receive. For a description of 
each report, see CBRS Technical Resources. For access to CBRS Stats reports, see CBRS Statistical 
Reports. 
Note:  
The CBRS Transaction Download on Request (Transaction Request WebDirect Download) file contains the data you 
downloaded using the quick search or advanced search functions (see Searching CBRS Transactions). After you 
request the download, it takes approximately 15 to 60 minutes to create the file, depending on the amount of data in 
the request. 
  


---

## Page 146

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 146 
4. Internet Explorer either automatically downloads the file or prompts you to open or save the file. 
To save the file locally: 
A. Click Save. The Internet Explorer Save As page appears. 
 
B. Use the navigation tools to select a location on your system for the file. 
C. In the Save As window, perform the following steps: 
a. Using the navigation tools provided, choose a location on your system to store the file. For 
example, you can choose to save the file on your desktop. 
b. In the File name field, you can leave the existing file name or enter a new one. 
c. In the Save as type field, leave the type set to the MRO (.mro) extension. 
d. Click Save. 
5. View the files. See Viewing Cost Basis Files Using Microsoft Excel. 
  


---

## Page 147

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 147 
Viewing Cost Basis Files Using Microsoft Excel 
After downloading the cost basis files, view them using Microsoft Excel. 
To view cost basis files using Microsoft Excel: 
1. Launch Microsoft Excel. 
2. Open the file in Microsoft Excel. 
a. Click File > Open > Browse. 
b. Navigate to the file location on your system. If the file downloaded automatically, go to the location on 
your local drive to open and view it. Otherwise, go to the location where you saved the file. 
Note: 
If the file does not appear, make sure all files are displayed. To ensure the MRO (.mro) output files display, select All 
Files (*.*), as highlighted in the figure.  
 
c. Select your file, and then click Open. 
  


---

## Page 148

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 148 
3. If you are opening a delimited report, import your file correctly by using the Text Import wizard. 
To select a data type: 
a. From Text Import Wizard - Step 1 of 3, choose Delimited from the Original data type section. Click 
Next. 
 
The Text Import Wizard - Step 2 of 3 window appears. 
b. In the Delimiters section, the Tab delimiter is selected by [[default]], and you must deselect it.  
c. Select one of the following delimiters depending on the report: 
• If you are opening a stats report, select Comma.  
• If you are selecting another type of report, select Other, and then type a ~ (tilde) in the space 
provided.  
The following figure shows the Tab deselected. Choose either Comma or Other with a tilde depending on 
the file that you are opening.  
 
d. Click Finish. 
The downloaded file opens in Microsoft Excel. You can save and rename the file. 


---

## Page 149

CBRS User Guide 
Accessing CBRS Through the [[DTCC]] Web Portal 149 
Size Limit for Transaction Download Files 
CBRS produces the Transaction Request and Transaction [[EOD]] (end of day) Download files only when the 
number of records (combined [[Asset]] and tax lot records both received and submitted) per file is less than 3,000.  
If a file exceeds the allocated size, CBRS cannot create it. 
Note  
Firms that expect to exceed this maximum need to be able to take in the Transaction Machine Readable Output (MRO) file 
(AutoRoute #02400264 in Production and #02980264 in Test). 
Time Frames for Files and Data Availability 
Files are stored in [[DTCC]] Web Portal for four days. Data is available for viewing on [[DTCC]] web screens, using 
the Cost Basis Inquiry screen, and downloading to an Excel spreadsheet, for twenty-five business days.  
Note: 
After the twenty-five-business day window has passed, [[DTCC]] cannot provide CBRS data. You are responsible for storing 
your data on a long-term basis. 
[[DTCC]] Web Portal Data Entry on Weekends and Holidays 
Data entered on a weekend or holiday is processed by CBRS on the next valid processing date. For example, 
a user submits CBRS records through [[DTCC]] Web Portal on Memorial Day, Monday, May 28. CBRS holds 
these submitted records, and processes them on Tuesday, May 29. The records submitted on Monday are a 
part of the output produced on Tuesday. 

---

## Page 150

CBRS User Guide 
CBRS Statistical Reports 150 
8. CBRS STATISTICAL REPORTS 
This section explains how to request access and view CBRS statistical reports. For information about 
downloading the statistical report, see Downloading and Viewing Cost Basis Files and Reports. 
Requesting CBRS Statistical Report Access 
Before receiving CBRS statistical reports, you must request access to reports by either AutoRoute files or 
downloading reports from the web using the Product Request Form provided by the [[DTCC]] Account 
Administration. 
To request access to CBRS statistical reports: 
4. Go to the User Documentation section of the [[DTCC]].com site for Cost Basis Reporting Services (CBRS) 
available at: 
http://www.[[DTCC]].com/clearing-services/equities-clearing-services/cbrs/support/public-documents 
2. From the New Accounts, Instructions and Forms section, [[Locate]] and download the CBRS New Account 
Instructions. 
3. Submit an email to [[DTCC]] Solutions requesting an update to the Product Request Form for your firm. The 
following figure shows the section that you should select in the Product Request Form:  
 
 
Request access to connectivity and delivery file information through the following options: 
o Smart Connection – Enables access to the MRO output that automatically sends the files through a 
computer-to-computer connection with [[DTCC]]. Ensure that you include the destination [[ID]] so that the 
files are sent to the correct location. 
o Web Direct Files – Enables access to the DATATRAK and AutoRoute files through the CBRS Web 
Portal (If you [[DO]] not select this [[Option]], your firm’s reports are not available through the CBRS Web 
Portal. 
o CBRS Web Portal Access – Enables access to the DATATRAK and AutoRoute files through the 
CBRS Web Portal. 
  


---

## Page 151

CBRS User Guide 
CBRS Statistical Reports 151 
4. Select the reports that you want to subscribe to and access. The following figure shows what you should 
select to obtain access to the CBRS statistical reports: 
 
5. Complete the remaining sections of the Product Request Form. 
6. Return the Product Request Form to the [[DTCC]] Account Administration. 
Accessing CBRS Statistical Reports from the CBRS Web Portal 
Note 
Ensure that you have requested CBRS Web Portal Access to the reports through the Product Request Form. See 
Requesting CBRS Statistical Report Access. 
You can download the Submitter of Assets and Receiver of Assets reports from the CBRS Web Portal. The 
Submitter of Assets report provides a breakdown of all your transaction types, including submissions, firm rejects 
received, reject percentage for your firm, and industry reject percentage. Use the Submitter of Assets report to 
compare your firm rejects received against the industry. Use the Receiver of Assets report  
The Receiver of Assets report provides a breakdown of all your transaction types, including all received 
transactions, firm rejects submitted, request submitted, industry average rejected submitted, and industry 
average request submitted. Use the Receiver of Assets report to compare your firm’s rejects and requests 
submitted to the industry average. 
  


---

## Page 152

CBRS User Guide 
CBRS Statistical Reports 152 
To access the CBRS Submitter of Assets or Receiver of Assets reports from the CBRS Web Portal: 
1. From the CBRS Web Portal, select CBRS Output > Cost Basis Output Files, as highlighted in the 
following figure: 
 
 
2. From the Data Files page, type your firm number, select the firm type, and then click Submit, as 
highlighted in the following figure: 
 
In the Data Files page, the machine-readable output (MRO), other end of day ([[EOD]]) output files, and stat 
reports appear. 
3. Select the file or report that you would like to view from the available list.  
Note: 
If you cannot [[Locate]] the end of day file, you may have exceeded the maximum file size; otherwise, your firm has not yet 
signed up to receive these files.  


---

## Page 153

CBRS User Guide 
CBRS Statistical Reports 153 
4. To open the report in Microsoft Excel, see Downloading and Viewing Cost Basis Files and Reports. 
5. View the report.  
See also:  
o Understanding the Submitter of Assets Report 
o Understanding the Receiver of Assets Report. 
Notes:  
• After generating a report, it is available in CBRS for four calendar days. 
• If a specific report does not appear at the expected time, check again later. 
Understanding the Submitter of Assets Report 
The Submitter of Assets report is available for download in the Microsoft Excel (.xls) file format for four days. Table 
8.1 shows a description of the fields available in the Submitter of Assets report. The top portion of the spreadsheet 
(row 6-28 in the following example spreadsheet) shows the statistics and details for your firm and the bottom portion 
(rows 31-53 in the example) shows the statistics and details for all submitting participants.  
 
  


---

## Page 154

CBRS User Guide 
CBRS Statistical Reports 154 
The following table describes the fields available in the Submitter of Assets report: 
Field Description 
Submitter Name of the submitter. 
Firm Name Name of your firm. For example, XYZ [[Broker]] 
Transaction Type Code associated with the transaction type. For more information, see transaction 
type.  
Description Description of the transaction type. 
Original Assets Shows the number of original assets submitted. 
Original Tax Lots Displays the number of original tax lots submitted. 
Corrected Assets Provides the number of corrected assets submitted.  
Corrected Tax Lots Displays the number of corrected tax lots submitted. . 
Firm Rejects Received Shows the number of rejects that your firm received. 
Reject % Calculates the reject percentage for your firm. 
Industry Reject % Displays the industry reject percentage so that you can compare you firm's reject 
percentage with the industry. 
Requests Received Shows the number of requests that your firm received. 
Request % Calculates the request percentage for your firm. 
Industry Request % Displays the industry request percentage so that you can compare you firm's 
reject percentage with the industry. 
Total Accepted Provides the totals for the original  assets, original tax lots, corrected assets, 
corrected tax lots, firm rejects submitted, and requests submitted. 
System Rejected Shows the number of items rejected by the system. 
Total Processed Calculates the total accepted and system rejected items. 
  

---

## Page 155

CBRS User Guide 
CBRS Statistical Reports 155 
Understanding the Receiver of Assets Report 
The Receiver of Assets report is available for download in the Microsoft Excel (.xls) file format for four days. Table 
8.2 shows a description of the fields available in the Receiver of Assets report. The top portion of the spreadsheet 
(row 6-29 in the example spreadsheet) shows the statistics and details for your firm and the bottom portion (rows 
33-56 in the example) shows the statistics and details for all receiving participants. An example of the report is 
shown in the following figure: 
 
Figure 8.6 Receiver of Assets Report 
  


---

## Page 156

CBRS User Guide 
CBRS Statistical Reports 156 
The following table describes the fields available in the Submitter of Assets report: 
Table 8.2 Receiver of Assets Field Descriptions 
Submitter Name of the submitter. 
Receiver Name of the receiver. 
Firm Name Name of your firm. For example, XYZ [[Broker]] 
Transaction Type Code associated with the transaction type. For more information, see transaction type.  
Description Description of the transaction type. 
Original Assets Shows the number of original assets received 
Original Tax Lots Displays the number of original tax lots received. 
Corrected Assets Provides the number of corrected assets received 
Corrected Tax Lots Displays the number of corrected tax lots received. 
Firm Rejects Submitted Shows the number of rejects that your firm submitted. 
Reject % Calculates the reject percentage for your firm. 
Industry Reject % Displays the industry reject percentage so that you can compare you firm's reject 
percentage with the industry. 
Requests Submitted Shows the number of requests that your firm submitted. 
Request % Calculates the request percentage for your firm. 
Industry Request % Displays the industry request percentage so that you can compare you firm's reject 
percentage with the industry. 
Total Accepted Provides the totals for the original  assets, original tax lots, corrected assets, corrected tax 
lots, firm rejects submitted, and requests submitted. 
System Rejected Shows the number of items rejected by the system. 
Total Processed Calculates the total accepted and system rejected items. 
 

---

## Page 157

CBRS User Guide 
Joining the Service 157 
9. JOINING THE SERVICE 
All financial intermediaries are eligible to apply to use CBRS, including firms who are not currently members of 
any [[DTCC]] subsidiary. CBRS New and Existing Account Instructions that explain how to open a CBRS account 
are available from the New Accounts, Instructions and Forms section of the User Documentation page at:  
http://www.[[DTCC]].com/clearing-services/equities-clearing-services/cbrs/client-center/public-documents.aspx 
The forms required to become an eligible user of CBRS depends on your firm’s existing relationship with 
[[DTCC]]. The instructions specify the forms that are required in each situation ([[DTC]] [[participant]], [[DTC]] Limited 
[[participant]] utilizing the [[Direct Registration]] Service, [[NSCC]] [[participant]], or no relationship to any [[DTCC]] 
subsidiary). 
Q What date should I put as the effective date in the Service Add letter?   
A The effective date in the Service Add letter is the date your firm will be ready to use CBRS in the 
production environment. This is not the date when your firm will start testing. After you complete the new 
account process, you will hear back from [[DTCC]] that you are eligible to use CBRS. As soon as you are 
eligible and have set up your access to the system, you can start testing. You can test any time up to 
when you start in Production and past that date as well. There is no end date for testing. As of the 
effective date, the user will be on the CBRS Master File in Production. Counterparties expect that if you 
are on that Master file, at a minimum, you can accept the records sent to you.  
Q I am a [[transfer agent]] and would like to make my LPA number eligible for CBRS. How [[DO]] I [[DO]] 
that?  
A You need to follow the CBRS New Account process to make the LPA number eligible for CBRS, even if 
you have one or more [[transfer agent]] numbers that are already eligible for CBRS. See the CBRS New 
and Existing Account Instructions available in the New Accounts, Instructions and Forms section at: 
http://www.[[DTCC]].com/clearing-services/equities-clearing-services/cbrs/client-center/public-documents.aspx 
Multiple Output File Set-up 
If your company has both a [[Broker]]-dealer side and a mutual fund company side, with different [[participant]] 
numbers, you can receive separate output files for the different numbers. The standard set-up is to receive one 
file. If you prefer to receive two files, contact your relationship manager, and [[DTCC]] will adjust the set-up 
accordingly. 
  

---

## Page 158

CBRS User Guide 
Joining the Service 158 
CBRS Billing 
Fees for CBRS records are charged per [[Asset]] record. There is no charge for Tax Lot records. 
Because CBRS is a service offering of [[DTCC]] Solutions LLC, the CBRS invoice is issued separately from an 
[[NSCC]] or [[DTC]] invoice. System users receive one invoice per CBRS account. If a firm has multiple CBRS 
accounts, it receives multiple CBRS invoices; for example, if a firm has three CBRS accounts, it receives three 
CBRS invoices.  
[[DTCC]] distributed CBRS invoices on the 7th business day of the month. 
Invoices are available through email and through [[DTCC]]’s online billing system. Contact your Relationship 
Manager for questions about your CBRS bill. 
Q How [[DO]] I pay for CBRS?   
A A company that has a [[settlement]] account uses its [[settlement]] account to pay the balance on its CBRS 
invoice. A company that does not have a [[settlement]] account pays by wire. Wire instructions are on the 
invoice. 

---

## Page 159

CBRS User Guide 
User Testing 159 
10. USER TESTING 
To become eligible for the service in both testing and production, complete the CBRS new account forms and 
return them to [[DTCC]]. See the New Accounts, Instructions, and Forms section available at: 
https://www.[[DTCC]].com/clearing-services/equities-clearing-services/cbrs/support/public-documents 
[[DTC]] Participants can expect to receive their new CBRS account in approximately three to five business days 
after [[DTCC]] has received the forms. All other firms are subject to additional compliance screening which 
extends the amount of time to establish a new account. In these cases, the [[DTCC]] Account Administration 
group contacts each firm as it moves through the approval process. 
Once a user establishes its CBRS account and connectivity to the system (either through computer-to-
computer connection, [[DTCC]] Web Portal, or both), there are multiple resources available to test data input and 
output to CBRS.  
Q How [[DO]] I know which CBRS users are eligible to test?  
A The version of the CBRS master file (whose technical name is the “Cost Basis User Master File”) that is 
available in the test environment lists all CBRS users who are eligible to test. The master file has a 
column named “CBRS Account Start Date.”  This date corresponds to the date the CBRS user is eligible 
to use the service in the production environment. All CBRS users who are on the master file in the 
testing environment are eligible to test. 
Testing Data Input 
A user can test data input by using three different counterparties: itself; test accounts, or a testing partner.  
To test with itself, a firm uses its Firm Account Number from the Cost Basis User Master File (or CBRS User 
Account Number if it does not have a Firm Account Number) as both the Submitting Firm Number and Type 
and Receiving Firm Number and Type in the CBRS input record layouts (both [[Asset]] and Tax Lot records). 
Some Transaction Types have requirements for Submitting Firm Type and Contra Firm Type, so if you test with 
yourself, you will only be able to test the Transaction Types that permit your Firm Type. 
To test with a test account, a firm uses its Firm Account Number from the Cost Basis User Master File (or 
CBRS User Account Number if it does not have a Firm Account Number) as the Submitting Firm Number and a 
test account number as the Receiving Firm Number in the CBRS input record layouts (both [[Asset]] and Tax Lot 
records).  
  

---

## Page 160

CBRS User Guide 
User Testing 160 
The CBRS test accounts are: 
• [[DTC]] [[participant]]: 00008608 DTCPRT 
• [[DTC]] [[participant]]: 00008610 DTCPRT 
• [[NSCC]] [[participant]]: 00000122 NSCPRT 
• [[NSCC]] [[participant]]: 00000123 NSCPRT 
• [[transfer agent]]: 00036165 AGTNBR 
• The test [[transfer agent]] account has two CUSIPs associated with it: 99999X037 and 99999Z024 
To test with a testing partner, a user can [[Locate]] a partner on the list of eligible CBRS users on the Cost Basis 
User Master File. Once a user has found a testing partner, it uses its Firm Account Number from the Cost 
Basis User Master File (or CBRS User Account Number if it does not have a Firm Account Number) as the 
Submitting Firm Number, and uses the testing partner’s Firm Account Number (or CBRS User Account 
Number if it does not have a Firm Account Number) as the Contra Firm Number in the CBRS input record 
layouts (both [[Asset]] and Tax Lot records). 
Firms can test the following [[DTC]] transactions in the testing environment (U region): 
• Deposits 
• Branch Deposits 
• [[DWAC]] (to test a [[DWAC]], a [[Broker]]-dealer should coordinate the test with a [[transfer agent]], so the agent can 
approve the test transactions) 
It is not possible to test [[DRS]] or Withdrawal by Transfer (NWT1 or RWT1) transactions in the U region. 
Testing Data Output 
CBRS transaction output and the Daily Deposit File for Transfer Agents are available by 9 P.M. Eastern Time. 
The Cost Basis User Master File is available by 11 P.M. Eastern Time. From the CBRS transaction output, a 
firm receives the records it submitted, and the records it received from a testing partner, if applicable.2   
Testing the Daily Deposit File for Transfer Agents 
When a [[transfer agent]] joins CBRS, it can request to receive the Daily Deposit File for Transfer Agents through 
DTF, by having signed on to the DPCBRS function using their M or N sign-on. Transfer agents will also be able 
to download this file through [[DTCC]] Web Portal. 
[[DTCC]] creates two different versions of the Daily Deposit File in the testing environment. From Mondays, the 
contents of the file will be the data submitted to Production on the previous Friday. From Tuesday through 
 
2 In this situation, a firm does not receive a submitted record on the transaction output file.  CBRS drops a 
transaction on the rare occasion when a submitter enters their firm number incorrectly, and CBRS does not 
recognize the submitter.  In this case, CBRS rejects the record because the submitter is invalid.  However, 
CBRS cannot return the record to the submitter because the incorrect submitter number does not match the 
submitter’s actual number; therefore, CBRS does not know where to return the record. 

---

## Page 161

CBRS User Guide 
User Testing 161 
Friday, the contents of the file will be the deposit transactions submitted through the testing environment over 
the course of the previous week, if any.  
Note:  
For a deposit to appear on the file on Tuesday through Friday, a [[DTC]] [[participant]] must enter a deposit through the testing 
environment. A [[transfer agent]] should arrange to have a [[DTC]] [[participant]] testing partner enter deposits into the testing 
environment for a [[CUSIP]] or CUSIPs specific to that agent. 
The following table shows the timing of the contents of the Daily Deposit file for testing: 
For Production Data 
 Monday Tuesday Wednesday Thursday Friday 
Week 1 [[DTC]] Participants 
enter deposits 
into Production 
[[DTC]] 
Participants 
enter deposits 
into Production 
[[DTC]] Participants 
enter deposits 
into Production 
[[DTC]] Participants 
enter deposits into 
Production 
[[DTC]] 
Participants 
enter deposits 
into Production 
Week 2 Deposits from the 
previous Friday 
(not the other four 
days in Week 1) 
are in the file 
No production 
data in file 
No production 
data in file 
No production data 
in file 
No production 
data in file 
For Test Data 
 Monday Tuesday Wednesday Thursday Friday 
Week 1 [[DTC]] Participants 
enter transactions 
into Test 
[[DTC]] 
Participants 
enter 
transactions into 
Test 
[[DTC]] Participants 
enter 
transactions into 
Test 
[[DTC]] Participants 
enter transactions 
into Test 
[[DTC]] Participants 
enter 
transactions into 
Test 
Week 2 No test data in file File contains test 
data from all five 
days in Week 1 
File contains test 
data from all five 
days in Week 1 
File contains test 
data from all five 
days in Week 1 
File contains test 
data from all five 
days in Week 1 
Canned Transaction Output File 
Four versions of a canned transaction output file are available in the testing environment. A canned file 
contains static data that firms can use for testing. The canned output file serves as a sample of what CBRS 
transaction output looks like. The four versions correspond to the kind of firm receiving the file: there is one file 
for a [[Broker]]-dealer, one for a [[transfer agent]], one for a bank, and one for a mutual fund company. The contents 
of the different versions, such as the Transaction Types, vary based on the kind of receiver. When requesting 
the canned file, indicate the number that corresponds to your user type: 
• 02991797 for a bank  
• 02991798 for a [[Broker]]-dealer 
• 02991119 for a mutual fund 
• 02991796 for a [[transfer agent]] 

---

## Page 162

CBRS User Guide 
User Testing 162 
APPENDIX A: LIST AND DESCRIPTION OF FILE 
IDENTIFICATION NUMBERS 
CBRS Input SYS [[ID]] Numbers 
The input SYS [[ID]] numbers for CBRS are # 36708 for Production and # 46708 for the [[participant]] Services 
Environment (PSE) for testing. 
List of CBRS Output File Identification Numbers 
The following table shows the CBRS and CBRS-related files and their file identification numbers or product 
numbers: 
Product Request Form File Name Cost Basis Output File Name in the CBRS 
Web Portal 
Production 
Number 
Test 
Number 
Transaction Machine Readable 
Output (MRO) 
CBRS Transaction MRO 02400264 02980264 
Transaction Request WebDirect 
Download 
CBRS Transaction Download on Request 02401663 02981663 
Transaction End of Day ([[EOD]]) 
WebDirect Download 
CBRS Transaction Download [[EOD]] 02401664 02981664 
CBI Stats MTD Submitter of Assets 
RPT 
CBRS Stats MTD Submitter of Assets RPT 02402928 02982928 
CBI Stats MTD Receiver of Assets 
RPT 
CBRS Stats MTD Receiver of Assets RPT 02402929 02982929 
Cost Basis User Master File Machine 
Readable Output (MRO) 
CBRS User Masterfile MRO 02561666 02981666 
Cost Basis User Master File 
WebDirect Download 
CBRS User Masterfile Download 02561667 02981667 
Daily Deposit File for Transfer Agents 
WebDirect Download 
CBRS Daily Deposit File for Transfer Agents 02401649 02981649 
Daily Reorg Deposit File for Transfer 
Agents WebDirect Download 
Daily Reorg Deposit File for Transfer Agents 
WebDirect Download 
02401912 N/A 
See also: CBRS Output Files and Reports 
  

---

## Page 163

CBRS User Guide 
User Testing 163 
The canned file for testing has different numbers depending on what type of user is receiving the file. When 
requesting the canned file, indicate the number that corresponds to your user type: 
• 02991797 for a bank  
• 02991798 for a [[Broker]]-dealer 
• 02991119 for a mutual fund 
• 02991796 for a [[transfer agent]] 
CBRS Output Files and Reports 
The following table provides a description for the CBRS files and reports. If you [[DO]] not see a file or report, 
make sure your firm has access. If not, request access. See also: Requesting CBRS Statistical Report Access. 
and List of CBRS Output File Identification Numbers.  
Note:  
The Transaction Request WebDirect Download or CBRS Transaction Download on Request file contains the data you 
downloaded using the quick search or advanced search functions (see Searching CBRS Transactions). After you request 
the download, it takes approximately 15 to 60 minutes to create the file, depending on the amount of data in the request. 
File or Report Name Description 
• Transaction Machine Readable Output 
(MRO) 
• CBRS Transaction MRO 
For computer-to-computer connection users. This file contains all 
CBRS transaction output for the firm for the current processing date. 
(While this file is intended for computer-to-computer connection users, 
it is also available for [[DTCC]] Web Portal users to download using the 
CBRS Output Files function.) 
• Transaction Request [[DTCC]] Web Portal 
WebDirect Download 
• CBRS Transaction Download on Request 
For [[DTCC]] Web Portal users. Firms can use the transaction inquiry 
function to search and view specific transactions using various 
criteria, such as ISIN, Transfer Control Number, or Transaction Type. 
They can then download these requested transactions to Excel. This 
file contains these specifically requested transactions in Excel format. 
• Transaction End of Day ([[EOD]]) WebDirect 
Download 
• CBRS Transaction Download [[EOD]] 
For [[DTCC]] Web Portal users. This file contains all transactions for 
the current processing day in Excel format. It contains the same 
information provided in Transaction Machine Readable Output (MRO) 
or CBRS Transaction MRO report for that day. 
• CBI Stats MTD Submitter of Assets RPT 
• CBRS Stats MTD Submitter of Assets RPT 
This report provides firms with a count of all [[Asset]] and Tax Lot 
records submitted to CBRS by their firm.  This report also provides 
firms with the total count of all CBRS transactions submitted by the 
entire CBRS community. The report also looks at the amount of 
submitted transactions and provides visibility to the number of rejects 
and request submitted against those original submissions and 
compares to the industry shown in percentage. 
• CBI Stats MTD Receiver of Assets RPT 
• CBRS Stats MTD Receiver of Assets RPT 
This report provides firms with a count of all Assets and Tax Lots 
records received from CBRS for their firm. This report also provides 
firms with the total count of all CBRS transactions received by the 
entire CBRS community. This report also looks at the amount of 
received transactions and provides visibility to the number of rejects 

---

## Page 164

CBRS User Guide 
User Testing 164 
File or Report Name Description 
and request received against those original submissions and 
compares to the industry shown in percentage.  
• Cost Basis User Master File Machine 
Readable Output (MRO) 
• CBRS User Masterfile MRO 
For computer-to-computer connection users. This file provides a 
listing of the firms that are active users of CBRS in MRO format.  
(While this file is intended for computer-to-computer connection users, 
it is also available for [[DTCC]] Web Portal users to download using the 
CBRS Output Files function.)  
• Cost Basis User Master File [[DTCC]] Web 
Portal WebDirect Download 
• CBRS User Masterfile Download 
For [[DTCC]] Web Portal users. This file provides a listing of the firms 
that are active users of CBRS in tilde-delimited format for converting 
to the Excel format. 
• Daily Deposit File for [[Equity]] Transfer Agents 
WebDirect Download 
• CBRS Daily Deposit File for Transfer Agents 
For [[Equity]] Transfer Agents only. This file contains the deposits for 
that [[transfer agent]] for that day, so they know for which deposits they 
can expect to send cost basis. The file is available through the [[DTCC]] 
Web Portal or from the mainframe for retrieval through the Data 
Transmission Facility (DTF) function DPCBRS. 
• Daily Reorg Deposit File for [[Equity]] Transfer 
Agents 
For [[Equity]] Transfer Agents only. This file contains the reorg 
deposits for that [[transfer agent]] for that day, so that they know for 
which reorg deposits they can expect to send cost basis. The file is 
available through the [[DTCC]] Web Portal, or from the mainframe for 
retrieval through Data Transmission Facility (DTF) function DRCBRS. 

---

## Page 165

CBRS User Guide 
User Testing 165 
APPENDIX B: LIST OF VALID CHARACTERS FOR CBRS 
        'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I',     
        'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R',     
        'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z',          
 
        'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i',     
        'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r',     
        's', 't', 'u', 'v', 'w', 'x', 'y', 'z',          
 
        '1', '2', '3', '4', '5', '6', '7', '8', '9',     
        '0',                                             
 
        '!', '@', '#', '$', '%', '&', '*', '(',          
        ')', '-', '_', '+', '=', '~', '{', '}',          
        '¢', '\', ':', ';', '"', '<', '>',               
        ',', '.', '?', '/', ' ', "'", '`'.             

---

## Page 166

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 