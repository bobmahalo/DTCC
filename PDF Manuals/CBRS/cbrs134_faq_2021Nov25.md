---
title: "CBRS Frequently Asked Questions"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cbrs134_faq_2021Nov25.pdf"
pages: 18
size: "347.9 KB"
category: "CBRS"
ingested_on: "2026-06-05"
---

# CBRS Frequently Asked Questions

**Original File:** [cbrs134_faq_2021Nov25.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cbrs134_faq_2021Nov25.pdf)  
**Category:** CBRS  
**Total Pages:** 18  
**File Size:** 347.9 KB  

---

## Page 1

 
 
COST BASIS REPORTING SERIVCE 
(CBRS) 
FREQUENTLY ASKED QUESTIONS 
NOVEMBER 25, 2021 
This document provides a list of Frequently Asked Questions about the Cost Basis Reporting Service (CBRS) . 
For more information about CBRS, see the Cost Basis Reporting Service (CBRS) section of the Learning 
Center. 
The questions are grouped by the following topics: 
• General Questions 
• New Accounts 
• Data Input 
• Data Output 
• Cost Basis User Master File 
• Testing 
  


---

## Page 2

Frequently Asked Questions 
CBRS Frequently Asked Questions 2 
General Questions 
Q What kinds of transactions does CBRS support?   
A CBRS supports the passage of cost basis on many different types of [[Asset]] transfers, such as transfers 
through the Automated Customer Account Transfer Service (ACATS), [[Depository Trust Company]] ([[DTC]]) 
deliver orders (DOs), [[DTC]] deposits and withdrawals, and transfers through ACATS-Fund/SERV and 
Networking.  For a full list of CBRS-supported transfers, see the CBRS Input Formats. 
Q Does CBRS support the passing of cost basis for both covered and noncovered [[securities]]?   
A Yes.  The Tax Lot Input record includes a Noncovered/Pending Indicator that the submitter can use to 
indicate that a lot is noncovered. If this field is left blank, the lot is considered covered. For all the rules 
for this field, see the CBRS Technical Resources. 
Q Does CBRS support the passing of cost basis in currencies other than U.S. Dollars?   
A All cost fields in CBRS are denominated in US Dollars only.  However, on the Tax Lot level, there are two 
fields—ISO Currency Code and Exchange Rate—that allow a submitter to tell the receiver that the 
submitter held the cost basis on its system in a different currency and converted the cost basis to US 
Dollars to transfer it. 
Q Does CBRS support the passing of cost basis on transactions that happen outside of [[DTCC]]?   
A Yes.  For example, Transaction Type 06 = Other Depository Deliveries includes [[Asset]] movements 
through the Fed, and Euroclear and other foreign depositories.  There is also a transaction type for 
manual mutual fund transfers, 57 = Manual Mutual Fund Transfer. 
Q Is there a difference in system functionality depending on whether I use CBRS through a 
computer to computer connection, or over WebDirect?  - 
A CBRS has the same functionality regardless of the connection: you can perform the same tasks via 
WebDirect that you can perform via the computer to computer connection.  You can input [[Asset]] and tax 
lot records into CBRS via WebDirect, and you can get the output files (transactions, the Master File, and 
the Daily Deposit File for Transfer Agents) via WebDirect as well.  When you set up your new account for 
CBRS, you need to specify which, or both, connection(s) you will use.  You can upload data to CBRS 
using an Excel spreadsheet, and also download your output to Excel. 
  

---

## Page 3

Frequently Asked Questions 
CBRS Frequently Asked Questions 3 
New Accounts 
For more information about the new account process, see CBRS New Account Instructions. 
Q Who at my company should sign the CBRS new account forms?   
A The CBRS forms need to be signed by an authorized signer who is officer level or above.  
Q What date should I put as the effective date in the Service Add letter?   
A The effective date in the Service Add letter is the date your company is ready to use CBRS in the 
production environment.  This is not the date when you start testing.  After you complete the new 
account process, [[DTCC]] contacts you to inform you that you are eligible to use CBRS.  As soon as you 
are eligible and have set up your access to the system, you can start testing.  You can test any time up 
to when you start in Production, and also past that date as well.  There is no end date for testing.  As of 
the effective date, the user will be on the CBRS Master File in Production.  Counterparties expect that if 
you are on that Master File, at a minimum you are able to accept the records sent to you.   
Q When [[DO]] I use my CBRS account number?   
A Make a note of your CBRS account number for the times when you communicate with [[DTCC]].  During 
the new account set-up process, you need it to fill out the Product Request Form and the Access 
Coordinator Form.  You will also need it in the future when contacting [[DTCC]] with questions about file 
submission, billing, and other issues.  In most cases this is not the primary number that identifies a 
[[participant]] in the CBRS transaction data input and output.  The Firm Account Number on the Cost Basis 
User Master File, which corresponds to a CBRS user’s [[DTC]] [[participant]] Number, [[NSCC]] [[participant]] 
Number, or [[transfer agent]] Number, is the number used in the Submitting and Contra Firm Number 
fields in data input and output.  The only time the CBRS User Account Number is the primary 
identification number of a user is when that user does not have a number in the Firm Account Number  
field on the Cost Basis User Master File. 
Q Am I required to send in an Access Coordinator Form?  What if I already have an Access 
Coordinator Form on file?  Does the CBRS Access Coordinator Form replace the existing form?   
A You need to submit a completed Access Coordinator Form if you want to access CBRS through  
WebDirect.  If you use only the computer to computer connection, you [[DO]] not need to fill out the Access 
Coordinator Form.  If you already have an Access Coordinator Form on file, you still need to send in the 
Access Coordinator Form for CBRS.  CBRS is offered by [[DTCC]]’s [[DTCC]] Solutions subsidiary, so you 
need to fill out the new form with [[DTCC]] Solutions even if you have an Access Coordinator for [[NSCC]] or 
[[DTC]] services.  The CBRS Access Coordinator Form does not replace your existing Access Coordinator 
Form.  You can have either the same Super Access Coordinator for CBRS as your other [[DTCC]] products 
or a different one—that's a decision each CBRS [[participant]] makes based on need.  After your company 
has made that decision, submit a request to entitlements@[[DTCC]].com to set up the correct users.  
  

---

## Page 4

Frequently Asked Questions 
CBRS Frequently Asked Questions 4 
Q How [[DO]] I set up access to CBRS through a service bureau?   
A Provide a letter to [[DTCC]], on your company’s letterhead, with the following information. For more 
information, see CBRS New Account Instructions. 
• Name of the Service (CBRS in this case) 
• Name of your Service Bureau 
• Technical contact at your company 
• Technical contact at the Service Bureau 
• Effective date (first date when the Service Bureau will send and receive files on your behalf)  
• Your CBRS Account Number 
• Your [[DTC]] or [[NSCC]] [[participant]] Number, if applicable 
Q [[DO]] I need to set up a separate CBRS account for each [[Equity]] [[transfer agent]] number?     
A Yes.  [[DTCC]] needs a signed User Agreement per legal entity, then an applicant can list multiple transfer 
agent numbers per legal entity on the Service Add letter.  Best Practices recommend that a transfer 
agent makes all its [[transfer agent]] numbers eligible for CBRS, to reduce system rejects. 
Q [[DO]] I receive separate files for each [[transfer agent]] number?   
A No.  An [[Equity]] [[transfer agent]] receives one file from [[DTCC]], and the [[transfer agent]] sends one file to 
[[DTCC]].  From the technical standpoint, there needs to be only one eligible CBRS account number in the 
CDTS Header: the Header tells [[DTCC]] who the file is coming from.  Within the file itself, there can be 
multiple submitting firm numbers.  If a [[transfer agent]] has multiple [[transfer agent]] numbers, combine the 
records for all the [[transfer agent]] numbers into one file for transmission to CBRS. 
Q Is there a charge per [[Asset]] record and Tax Lot record?   
A CBRS fees are charged per [[Asset]] record.  There is no charge for submitting or receiving a Tax Lot 
record. 
  

---

## Page 5

Frequently Asked Questions 
CBRS Frequently Asked Questions 5 
Data Input 
Q What [[DO]] the different Record Content Indicator values mean? 
A The following table explains the values: 
Value Description 
Original [[Asset]] 
record/Original tax lot 
record 
Primary record used to transfer the cost basis information. 
Corrected [[Asset]] 
record/Corrected tax 
lot record 
Submitter can use the corrected record type to tell the receiver that the cost basis information 
has changed since the original record was sent. 
Firm reject record 
([[Asset]] level only) 
Receiver of the cost basis can use this type of record to let the submitter of the cost basis know 
that there is a problem with the information.  The firm reject record is different from a system 
reject—a system reject occurs when some of the submitted information is rejected by the 
CBRS application.  For example, if the submitter populates one of the date fields with 
01/35/2011, CBRS reject the record because a date of January 35, 2011 is not possible. 
Request record ([[Asset]] 
level only) 
Transfer receiver can use this type of record to request cost basis from the transfer deliverer. 
 
Q Which fields, when changed, should prompt the submitter to send a Corrected record?   
A Any field that has been changed should be sent as a correction.  If the data element is important enough 
to be changed, it should be important enough to resend. 
Q What happens when a CBRS user sends a firm reject record?   
A CBRS users send a firm reject record when, for various reasons, they cannot apply the received cost 
basis to its books.  This situation is different from a system reject.  A system reject occurs  when the 
CBRS system rejects a record because it does not comply with the system’s rules, such as when a date 
field has a value of 1/35/2021, which is not a valid calendar date.   
The following information flow occurs for a reject record: 
1. A CBRS user receives cost basis information it cannot apply to its books.   
2. This user submits an [[Asset]] record, with the value 03 = Firm reject record in the Record Content 
Indicator field. 
At this point the receiver of the firm reject decides whether to respond.  CBRS does not require a 
response to a firm reject.  If the receiver of the reject chooses to respond, the information flow 
continues with step 3. 
3. To correct the error, the receiver of the reject responds with an [[Asset]] record with the value 02 = 
Corrected [[Asset]] record in the Record Content Indicator field, and its corresponding tax lots.  At least 
one of these tax lots must also be corrected (02 = Corrected tax lot record in the Record Content 
Indicator). 
  

---

## Page 6

Frequently Asked Questions 
CBRS Frequently Asked Questions 6 
Q How should I when I receive a Firm Reject record?   
A The scenarios below describe the Best Practices for the different Record Content types.  In each 
example, Firm A has already transferred an [[Equity]] to Firm B, and now needs to pass the cost basis for 
that transferred [[Asset]]. 
• Firm A sends an original record to Firm B.  Some of the data is incorrect, so Firm B sends a firm 
reject record to Firm A.  Firm A responds with a corrected record. 
• Firm B has not received cost basis from Firm A.  Firm B sends a request record to Firm A.  Firm A 
responds with an original record. 
• Firm A sends an original record to Firm C.  Firm C is not the correct receiving firm for this record, so it 
sends a firm reject record to Firm A.  Firm A responds by sending an original record to Firm B.  
Note  
In the last example above, while CBRS does not require Firm C to send a Firm Reject, it would be helpful for Firm C 
to Firm Reject the record so Firm A knows there is a problem.  CBRS does not reject the record if it passes all of the 
system rules and edits, so the only way Firm A knows there is a problem with the record is if Firm C sends a firm 
reject. 
Q Can I reject a corrected or request record?   
A You can firm reject corrected records.  For example, Firm A sends a corrected record to Firm C.  Firm C 
is not the correct receiving firm for this record, so it sends a firm reject record to Firm A.  Firm A 
responds by sending a corrected record to Firm B. 
A firm reject is not an appropriate response to a firm reject record or a request record.  Best Practices 
recommend that a firm disregard a firm reject or request record that it has received in error.  
Q Can I send a corrected record without first sending an original record?   
A CBRS does not system reject a corrected record that was not preceded by an original record, but the 
contra party may not accept the corrected record in this scenario.  Best Practices say [[DO]] not send a 
corrected record unless you have first sent an original record. 
Q In CBRS, is the transfer receiver required to wait the entire fifteen days after transfer [[settlement]] 
before sending a request through CBRS?   
A Best Practices recommend waiting fifteen days before sending a request.  However, the CBRS system 
allows a user to send a request record type at any time.  CBRS does not system reject a request sent 
before the fifteen days has passed.   
Q After a request has been sent, is the transfer receiver required to wait an additional fifteen days 
before marking the tax lot as noncovered?   
A This is a decision each CBRS user makes for itself.  Some users may choose to mark the lot noncovered 
as soon as the request is sent, others may wait for the contra user to respond.  The CBRS system is not 
involved in this decision. 
  

---

## Page 7

Frequently Asked Questions 
CBRS Frequently Asked Questions 7 
Q What are the Best Practices around noncovered accounts and noncovered lots?  When should I 
send basis?  When should I expect to receive basis?   
A Use the following best practices when submitting a receiving data for noncovered accounts and 
noncovered security types: 
• From the submitter’s perspective: 
o If you have cost basis, send it. 
o If you [[DO]] not have cost basis, [[DO]] not send anything. That is, [[DO]] not send a record that says 
the lot is noncovered and has unknown cost basis. 
• From the receiver’s perspective: 
o [[DO]] not send a request record for a noncovered account or a noncovered security type.  
o If you receive basis for an account that is noncovered, [[DO]] not reject it. 
o If you receive basis for a security that you think is noncovered, [[DO]] not reject it. 
Q I’m confused about what values belong in the Submitting Firm Number/Type and Contra Firm 
Number/Type fields versus the Receiver Customer Account Number and Deliverer Customer 
Account Number fields.   
A The Submitting Firm Number and Submitting Firm Type should always correspond to the user sending 
the CBRS record.  The Receiving Firm Number and Receiving Firm Type should always correspond to 
the user receiving the CBRS record.  The Deliverer Customer Account Number should always 
correspond to the user who delivered the [[Asset]] transfer, and the Receiver Customer Account Number 
should always correspond to the user who received the [[Asset]] transfer.    
For example, let’s say that Firm A sends an Original record to Firm B, and later follows up with a 
Corrected record.  Firm B sends a Firm Reject record to Firm A.  Firm B is looking for cost basis from 
Firm A for a separate [[Asset]] transfer, so Firm B also sends a Request record to Firm A.  This table shows 
how these fields should be filled out for each record type: 
Record 
Type 
Submitting 
Firm Number 
Submitting 
Firm Type 
Contra 
Firm 
Number 
Contra 
Firm 
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
 
Q I won’t have a receiving customer account number for non-ACATS items and deliver items, but 
the Receiver Customer Account Number is required.  What [[DO]] I enter in that field?   
A Best Practices suggest you enter the words not provided in the Receiver Customer Account Number 
field if you [[DO]] not know the number and it is required.  For ACATS, this best practice does not apply 
since you have a receiver customer account number for assets transferred through ACATS.  

---

## Page 8

Frequently Asked Questions 
CBRS Frequently Asked Questions 8 
Q What if I [[DO]] not know the cost basis for an [[Asset]] that I have transferred?  How [[DO]] I populate 
CBRS in this situation?   
A CBRS allows you to pass records on assets when you [[DO]] not know the cost basis.  The rules for the cost 
fields vary as far as when zero is a valid value, and when a blank is a valid value.  F or the various 
conditions, see the CBRS Technical Resources. 
Q Is a request record used to ask for basis after I have received a record where the cost basis has 
been marked as Pending?   
A No. A request record is used in the situation when a [[participant]] who has received an [[Asset]] transfer is 
expecting to receive cost basis from a prior firm but has not received anything. 
Q What happens if I receive tax lots that have unknown basis?  Should I request basis for these 
lots?   
A Best Practices say a receiver should not request basis from a submitter if the receiver receives  lots that 
have unknown basis.  Here are two examples: 
• Firm A sends cost basis to Firm B on a transfer of 300 [[shares]] of XYZ.   Firm A sends an [[Asset]] record for 
300 [[shares]], and two tax lots, one for 100 [[shares]] and one for 200 [[shares]].  The tax lot for 100 [[shares]] has a 
cost amount associated with it, but the 200 share lot has an unknown cost amount.  The records pass 
CBRS processing, so Firm B receives all of this information. 
Best Practices say that Firm B should not request information on the 200 share lot t hat has 
unknown cost.  A CBRS user should send a request record only when it has not received any 
information at all. 
• Firm A sends an ACATS transfer to Firm B that contains 10 assets.  Firm A sends CBRS records to Firm 
B, but only for 9 assets. 
In this case, Firm B should send a request record for the one [[Asset]] for which it did not receive a 
CBRS record. 
Q Why is the Tax Identification Number and other personal information not included in the CBRS 
record layouts?   
A Based on the input from the Steering Committee that helps [[DTCC]] design the system, CBRS has not 
included fields that would pass explicit personal information.  Instead, the customer account number and 
the transfer control number serve as codes that represent the owner of the transferred [[Asset]].   
Q Since the Transfer Control Number field is 30 bytes, can I populate the field with a 16 byte 
number?   
A The only requirement CBRS has for the Transfer Control Number field is that it cannot be blank.  You 
can provide the number with or without leading zeros.  CBRS does not modify the field, so the exact 
same value submitted in the input is on the output. 
Q How [[DO]] I capture the inventory management system (IMS) transaction [[ID]] (TID) number from 
[[DTCC]]?   
A This number is available on [[DTC]]’s DTF PART file.  For more information, see the [[DTC]] important notice 
# B6890-10 available at: https://www.[[DTCC]].com/-/media/Files/pdf/2010/8/19/6890-10.pdf 

---

## Page 9

Frequently Asked Questions 
CBRS Frequently Asked Questions 9 
Q Is there a way to manually look up the IMS TID number?   
A You can look up a [[DTC]] transaction’s IMS TID number through the ART function in [[PBS]].  Begin by 
selecting a transaction.  After you click on the transaction, you see the screen below.  The IMS TID is 
located at the bottom of the ‘Activity Details’ section of the screen.  The IMS TID is not available in [[PTS]].  
 
Q When a [[transfer agent]] is either the submitter or receiver of CBRS records, does the system verify 
that Submitting or Receiving Firm Number is the right [[transfer agent]] for that  [[CUSIP]]?   
A CBRS checks that the [[transfer agent]] is an eligible CBRS user. It does not confirm that the firm number is 
the correct [[transfer agent]] number for the [[CUSIP]] in that record.  However, CBRS does populate the 
Receiving Firm Number in most cases when a [[transfer agent]] is the receiver.  For the rules for when 
CBRS populates the Receiving Firm Number, see the [[Asset]] and Tax Lot Input in the CBRS Input 
Formats section. 
Q What is an example of when a submitter should use the 01 = True Zero value in the Zero Basis 
Indicator field?   
A Submitters use the 01 = True Zero value when dealing with the return of capital or rights.   
Q How is the Disposition Method Used field used?  
A This optional field indicates the lot disposition method used by the deliverer.  For some CBRS users, the 
field could provide value-added information for the underlying customer.  Best practices suggest that you 
should populate the field on a best-efforts basis.  The list of values is not an exhaustive list for all 
possible disposition methods. 
  


---

## Page 10

Frequently Asked Questions 
CBRS Frequently Asked Questions 10 
Q In the Noncovered/Pending Indicator field, how are the values Noncovered account and Pending 
used? 
A Noncovered accounts can either belong to an exempt entity, such as a C Corporation, or an exempt 
account, such as a retirement account.  Examples of when a submitter would use the Pending value 
include the situation when an [[Asset]] is a part of an Employee [[Stock]] Plan, or because the submitter is 
waiting for cost basis information from the prior user. 
Q When [[DO]] I use the Date Transfer was Initiated versus the [[settlement]] Date of Transfer?    
A The Date Transfer was Initiated may not often be known or populated.   CBRS users can decide 
individually whether they want to populate the Date Transfer was Initiated field.  While the Date Transfer 
was Initiated may not be known for the underlying transfer, the [[settlement]] Date of Transfer should be 
known.  One or the other of these dates is required.  Best Practices suggest that the [[settlement]]  Date of 
Transfer is used for most records. 
Q In the Position Code field, when would I use the value B=Borrowed?   
A The value B=Borrowed is only valid for a request record (Record Content Indicator = 04).  This is a rare 
situation that can occur when a [[short position]] is delivered outside of a standard ACATS transfer.  For 
more information about the borrowed position code, see the CBRS User Guide. 
Q Why does CBRS include the Taxes Reported by [[issuer]]/[[transfer agent]] field?   
A In some cases, the [[issuer]]/[[transfer agent]] does the 1099-B reporting.  This field allows the [[issuer]]/transfer 
agent to tell the [[Broker]]-dealer that it has already done the 1099-B reporting for a given tax lot, in order to 
avoid both parties reporting the information. 
Q What is the significance of the 03 = Inherited, then Gifted value in the Gifted or Inherited Indicator 
on the Tax Lot Input record layout?   
A This value exists because of its impact on the holding period for the lot.  Gifted [[shares]] have a short term 
holding period; inherited [[shares]] have a long term holding period.  If an [[investor]] gifts inherited [[shares]], the 
lot should keep its long term holding period.  For example, an [[investor]] inherits [[shares]], and then this 
same [[investor]] gives these [[shares]] to his daughter.  In this case, populate the Gifted or Inherited Indicator 
field with the value 03 = Inherited, then Gifted, in order to inform the receiver of the CBRS record that the 
lot should keep its long term holding period. 
Q If a [[transfer agent]] receives a deposit for 100 [[shares]] consisting of two 50 [[shares]] certificates, and 
only one certificate can be processed, for example, one of the certificates is invalid, how should 
cost basis be returned?   
A Best practice suggest that, since in this case a [[transfer agent]] can only re-register 50 [[shares]], it would 
only pass basis on the 50 [[shares]] that are re-registered. 
Q Why are the Filler fields required?   
A Filler fields are required because the filler tells the system the position of the fields in the record.  Also, 
for optional fields, the submitter should still provide spaces in place of the value to keep the position of 
the other fields in the correct place. 

---

## Page 11

Frequently Asked Questions 
CBRS Frequently Asked Questions 11 
Q When [[DTCC]] removes a field from the CBRS record layouts and turn it into filler, what happens if 
a submitter populates this field?   
A After a field has been removed from the record layouts, and turned into a filler field, the CBRS 
application does not look at this field.  The data populated in this field by the submitter does not get 
passed on to the output.  [[DTCC]] recommends that the submitter space out these bytes: a submitter who 
does not space out these bytes may encounter a problem in the future if the bytes are reused for a 
different field.   
Q [[DO]] I send multiple [[Asset]] records for the same security if I hold the security in different 
currencies?   
A Best Practices suggest that the quantity of the [[Asset]] record should equal the quantity of the original 
transfer that triggered the need to pass cost basis.  You can indicate at the tax lot level that  lots are held 
in a currency other than US Dollars.  
Q Can I send multiple files to CBRS during the day?   
A Yes.  You can send multiple files each day, through both the computer to comput er connection and 
WebDirect.  CBRS combines all the input, processes it at the end of the day, and returns the output to 
you in one file. 
Q If my company does not have any CBRS transactions to submit to [[DTCC]] on a given day, can I 
send an empty file?   
A Yes, you can send an empty file with only a CDTS header.  You can also not send any file at all.  
Q Does CBRS have the [[Asset]] category MFMM (Mutual Fund Money Market)?   
A No. The Steering Committee that advises [[DTCC]] on CBRS requested that the category MFMM be 
removed, because the IRS regulations [[DO]] not apply to money market funds.  
Q Does CBRS have a file input limit?   
A [[DTCC]] recommends that if a record count exceeds 8 million daily records, whether for conversion or 
standard transaction, to alert CBRS Product Management or your Relationship Manager. This reduces 
any processing delays. 
  

---

## Page 12

Frequently Asked Questions 
CBRS Frequently Asked Questions 12 
Data Output 
Q How [[DO]] I know I have successfully submitted records to CBRS?  
A CBRS output [named the Cost Basis Transaction MRO (Machine Readable Output) file] includes the 
records you submitted to the system, as well as the records other CBRS users sent to you.  The only 
exception is a record submitted with an invalid submitter number.  In this case, CBRS rejects the record, 
but does not know where to send the reject record to, since the submitter is invalid.  CBRS drops this 
record (see description of dropped record below). 
Q Why does CBRS drop a record?   
A CBRS drops a transaction in the rare occasion when a submitter enters their Submitting Firm Number 
incorrectly, and CBRS does not recognize the submitter.   In this case, CBRS rejects the record because 
the submitter is invalid.  However, CBRS cannot return the record to the submitter because the incorrect 
submitter number does not match the submitter’s actual number, so CBRS does not know where to 
return the record. 
Q If CBRS rejects a tax lot record, does it also reject the accompanying [[Asset]] record?   
A Yes.  CBRS treats the [[Asset]] and its tax lot record(s) as a package.  When CBRS rejects a tax lot, CBRS 
also rejects the [[Asset]] record and any other tax lot records in that package.  
Q [[DO]] I have to send all the tax lots for a corrected record, even if only one tax lot is corrected?   
A Yes.  For original and corrected records, the submitter must always send an [[Asset]] record with all its 
corresponding tax lot records.  CBRS looks at the [[Asset]] and tax lot records as a package.  If the package 
is not intact, CBRS rejects it.  
Q After I submit a record, can I see that CBRS has accepted and passed that record?   
A Yes, a submitter can see the records that CBRS has successfully passed on to the receiver on the Cost 
Basis Transaction MRO file.  
Q How [[DO]] I know I have submitted a record that CBRS has rejected, such as a system reject?   
A The Cost Basis Transaction MRO file includes all records that a CBRS user submits.  Each record has a 
System Action field, that labels the record as Accepted, Modified, or Rejected.  Also, each field on the 
output has a corresponding status field.  If a submitted field does not pass CBRS system rules and 
therefore is system rejected, the status for that field is populated with a value of 2 = Error.  
Q Can you clarify what I receive in the system reject situation versus the firm reject situation? 
A In a system reject, CBRS sends the rejected [[Asset]] and accompanying tax lot record(s), as a package, 
back to the submitter of the record.  In a firm reject, the submitter of the record (who is usually the 
receiver of the [[Asset]]) sends only an [[Asset]] record to the receiver of the record (who is usu ally the 
deliverer of the [[Asset]]).  
Q If an optional field is not filled in on the [[Asset]] or tax lot input, what is in that field on the 
transaction output?   
A The quantity and price fields have zeros in them, other fields are blank. 

---

## Page 13

Frequently Asked Questions 
CBRS Frequently Asked Questions 13 
Q If my company does not have any CBRS transaction output for a given day (meaning my 
company is not the submitter or receiver of any CBRS records), [[DO]] I receive a transaction output 
file?   
A Yes if you are set up to receive an empty file.  When you set up your access to CBRS, you can ask to 
receive an empty CBRS transaction output file in this situation.  The file contains only a CDTS header.  
Q My company has both a [[Broker]]-dealer side and a mutual fund side, with different [[participant]] 
numbers.  Can I receive separate CBRS files for these two entities?   
A If your company has both a [[Broker]]-dealer side and a mutual fund company side, with different [[participant]] 
numbers, you can receive separate output files for the different numbers.  The standard set -up is to 
receive one file. If you prefer to receive two files, contact your relationship manager so that [[DTCC]] can 
adjust the set-up accordingly. 
Q Can I pick up the output files through both the automated connection and WebDirect?   
A Yes, the files are available in both places.  Regardless of how a submitter enters data into the system, all 
the receiver’s data is in one file.  To retrieve both files, subscribe to both files when setting up your 
access to CBRS.   
Q How long are CBRS records available on WebDirect?   
A The files are stored in WebDirect for four days.  The data stored on the mainframe database is available 
for inquiry, viewing and downloading to an Excel spreadsheet for twenty-five days. 
Q Can I look up system rejected records using WebDirect?   
A Yes.  WebDirect has an inquiry function that allows CBRS users to look up the records using the System 
Status field, with the Reject value. 
Q On the output, how can I tell the difference between the records I submitted and the records I 
received?   
A Each record has a Receiving Firm Number and Submitting Firm Number.  Use these fields to distinguish 
between the records you submitted and the records you received. 
Q On the output, how [[DO]] I know which records are original [[Asset]] records, corrected [[Asset]] records, 
firm reject records, and request records?   
A The Cost Basis Transaction MRO includes the AO Record Content Indicator field, which tells you 
whether the submitter designated the record as original, corrected, firm reject, or request.  
Q Does the Transaction MRO contain all firm reject and request records, and all [[Asset]] and tax lot 
records, in one file?   
A Yes.  All records submitted and received by your company on the same day are in the same file.  
  

---

## Page 14

Frequently Asked Questions 
CBRS Frequently Asked Questions 14 
Q What are the status fields?   
A On the output, each submitted field has an accompanying status field.   This field indicates whether the 
value in the submitted field is valid, system changed, or error.  A space is also a possible value for this 
field: the space occurs if the field is optional field, the submitter does not populate the field, and the field 
does not have a [[default]] value. 
Q Are the status fields populated for the records when I am the receiver, or only when I am the 
submitter?   
A CBRS populates the status fields for all records on the Cost Basis Transaction MRO file.  For the records 
when you are the receiver, the status is 0 = Valid, 1 = System Changed, or [space] which indicates that 
this field was not populated by the submitter.  If a submitted field does not pass CBRS system rules, the 
status for that field is populated with a value of 2 = Error.  When your company is on the receiving side, 
you [[DO]] not receive a status field which has a value of 2 = Error, because CBRS rejects a record that has 
an error in it and returns it to the submitter. 
Q What is the System Action field?   
A The System Action field is in the beginning section of the output record of the [[Asset]] or Tax Lot record.  
The System Action field indicates if each record on the input file was accepted, rejected, or modified.  
The values for the field are: 
• 1 = System Accepted - Transaction submitted correctly 
• 2 = System Modified - Transaction submitted correctly and modified by CBRS 
• 3 = System Rejected - Transaction submitted incorrectly 
Successfully passed records have a value of either 1 = System Accepted or 2 = System Modified in the 
System Action field.  System Modified means CBRS has changed a field in the record.  For more 
information, see the next answer. 
Q What is an example of a System Changed situation?   
A The System Changed status occurs when CBRS changes a submitted value in a field.  For example, on 
the Tax Lot Input records, there are two fields pertaining to certificate numbers: Certificate Number Prefix 
and Certificate Number.  These two fields pertain to only two transactions: 27 = Certificate Deposit and 
41 = Direct Presentation.  If a submitter populates this field for any other transaction type, CBRS 
replaces the submitted value with spaces and continues to process the record.  In this case, the status 
on the output for this field has a value of 1 = System Changed.   To view the various occasions where 
CBRS might modify submitted data, see the CBRS Technical Resources.   
Q What is the System Reject Reason field?   
A The System Reject Reason field specifies the reason that caused CBRS to reject the record(s).   If  the 
System Action code is a ‘3’, the System Reject Reason field indicates the applicable reason.  For 
example, the 04 = Invalid Physical Sequence – [[Asset]] record not present code occurs when a tax lot 
record is submitted without an [[Asset]] record.  Users can find the complete list of System Reject Reasons 
in the Cost Basis Transaction MRO record layout.  
  

---

## Page 15

Frequently Asked Questions 
CBRS Frequently Asked Questions 15 
Q What does the Distribution Side field mean on the Cost Basis Transaction MRO?   
A The Distribution Side field on the MRO file corresponds to whom CBRS is sending the file.  For system 
rejected records, this field has a value of S = Submitting [[participant]], because only the submitter receives 
system rejected records.  For records successfully processed through CBRS, this field has a value of B = 
Both Receiving and Submitting [[participant]], because CBRS sends successfully processed records to 
both the submitting and receiving firm.  The Cost Basis Transaction MRO file also has a Distribution Firm 
Number and Distribution Firm Type.  These fields have the firm number and type for the user receiving 
the file. 
Cost Basis User Master File 
Q What is the Cost Basis User Master File?   
A The Cost Basis User Master file includes all users who are eligible to send and receive files through the 
system.  The file is updated daily.  For more information about this master file, see the CBRS User 
Guide. 
Q What time does [[DTCC]] produce the Cost Basis User Master File?   
A The Cost Basis User Master file is available by 11 PM Eastern Time. 
Q How [[DO]] I get access to the Cost Basis User Master File?   
A You are given access to the Cost Basis User Master file and other CBRS files during the new account 
set-up process. For more information about this set-up process, see the New Account Instructions. 
Q Can a company be a CBRS user and not a [[Member]] of [[DTC]] or [[NSCC]]?   
A Yes. 
Q Can I send records to a user that has a [[DTC]] number using its CBRS number?   
A No. For [[DTC]] participants, you must send basis to its [[DTC]] number, using the correct Firm Type. This 
information is available on the CBRS master file, which is distributed daily.  
  

---

## Page 16

Frequently Asked Questions 
CBRS Frequently Asked Questions 16 
Q On the CBRS [[participant]] file, if a user is a CBRS [[participant]], but not an [[NSCC]] or [[DTC]] [[participant]], 
what does the user have in the Firm Type field?   
A If a company is a CBRS only user, the Firm Account [[ID]] and Firm Account Type fields are blank in the 
CBRS User Master File, as shown in the following example:  
 
In this case, you should use the user’s CBRS Account [[ID]] as their Firm Number and type CBRACT as 
their Firm Type in CBRS.  For example, if this Test CBRS Only User is the user to which you are sending 
cost basis, populate the Contra Firm Number field with 1234ABCD and the Contra Firm Type field with 
CBRACT. 
Q What is the Exempt Recipient Accounts indicator?   
A The Exempt Recipient Accounts indicator allows a CBRS user to state whether it wants to receive basis 
for exempt accounts, which in this context are defined as retirement accounts.  For more information, 
see the Important Notice #CBRS006.11 that describes the indicator. 
CBRS is not performing an edit between this indicator on the master file and submitted CBRS records.  If 
a CBRS user sends basis for a retirement account to a contra user who has indicated that it does not 
want to receive the basis, CBRS does not system reject the record.  While CBRS is not systematically 
enforcing the indicator, it is an industry Best Practice to program to the indicator to determine whether a 
contra party would like to receive basis for retirement accounts. 
  


---

## Page 17

Frequently Asked Questions 
CBRS Frequently Asked Questions 17 
Testing 
Q How does testing work?  Is there a pilot group for testing?   
A All eligible users can test with CBRS—there is no specific testing pilot group.  Testing is available 
through both the computer-to-computer connections and the internet via [[DTCC]]’s WebDirect.  For more 
information, see Important Notice CBRS005.11, dated July 27, 2011. 
Q Are there test firm numbers that I can use as Receiving Firm Numbers?   
A Yes. As outlined in [[DTCC]] Solutions Important Notice CBRS005.11 dated July 27, 2011, a CBRS user 
can submit transactions to the following test accounts:  
• [[DTC]] [[participant]]: 00008608 DTCPRT 
• [[DTC]] [[participant]]: 00008610 DTCPRT 
• [[NSCC]] [[participant]]: 00000122 
• [[NSCC]] [[participant]]: 00000123 
• [[transfer agent]]: 00036165 AGTNBR for CUSIPs 99999X037 and 99999Z024 
Q Can I get an example of what the Transaction MRO looks like?   
A Yes.  Four versions of a canned transaction output file are available in the testing environment.  A 
canned file contains static data available to CBRS users for testing.  The canned output file serves as a 
sample of what CBRS transaction output looks like.  The four versions correspond to the kind of user 
receiving the file: there is one file for a [[Broker]]-dealer, one for a [[transfer agent]], one for a bank, and one 
for a mutual fund company.  For more details about testing, including information about the canned file, 
see Important Notice CBRS005.11, dated July 27, 2011.   
 
 

---

## Page 18

 
 
© 2021 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: April 5, 2022 
Publication Code: CBRS134 
Service: Cost Basis Reporting Service (CBRS) 
Title: Frequently Asked Questions 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 