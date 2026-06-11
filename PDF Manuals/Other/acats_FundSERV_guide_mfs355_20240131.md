---
title: "User Guide: ACATS-Fund/SERV"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/acats_FundSERV_guide_mfs355_20240131.pdf"
pages: 44
size: "604.2 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# User Guide: ACATS-Fund/SERV

**Original File:** [acats_FundSERV_guide_mfs355_20240131.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/acats_FundSERV_guide_mfs355_20240131.pdf)  
**Category:** Other  
**Total Pages:** 44  
**File Size:** 604.2 KB  

---

## Page 1

 
 
FUND/SERV® 
USER GUIDE: ACATS-FUND/SERV 
JANUARY 31, 2024 
 

---

## Page 2

 
 
 
 
 
REVISION HISTORY 
Date Revisions 
January 31, 2024 Rebranded document. Content reviewed. 
April 22, 2022 Learning upgrade caused some link(s) to break.  Links have been corrected. 
Effective 02/24/2020 The ACATS-Fund/SERV Transfer record (018) will be sent to the funds multiple times each 
day (changed from once per day).  For more information, please see Important Notices 
a8276 (10/27/2016), a8359 and a8736. 
Effective 02/29/2016 The T+2 080 reminder will no longer be sent to funds at 8:00 pm. Also, new reject codes 
were created. See Important Notice a8107, dated 10/27/2015. 
August 26, 2014 Updated to reflect timing of when Fund/SERV wil l delete a transfer request on T+2 
(previously T+4) if an 019 is not received from the mutual fund. 
Effective July 28, 2014 Please see Important Notices:   
a7700 P&S# 7370 Dated April 1, 2014 (Revised) &  
a7701 P&S# 7371 Dated May 15, 2014 (Revised)  
a7472 P&S# 7042 Dated August 16, 2012 and  
a7567 P&S# 7137 Dated January 9, 2013 
 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Introduction .......................................................................................................................................................... 4 
1.1 About ACATS-Fund/SERV ........................................................................................................................... 4 
1.2 Purpose of Document ................................................................................................................................... 4 
1.3. Background .................................................................................................................................................. 4 
1.4. Processing Times ........................................................................................................................................ 4 
Tips for [[Broker]]/dealers, banks, and [[Mutual Funds]] ............................................................................................ 6 
2.1 Tips for [[Broker]]/Dealers and Banks ............................................................................................................... 6 
2.2 Tips and Best Practices for Mutual Fund [[Companies]] .................................................................................. 7 
Walkthrough of a mutual fund transfer using ACATS-Fund/SERV ............................................................... 11 
The ACATS side ................................................................................................................................................. 12 
4.1 Requesting the Account Transfer ...............................................................................................................12 
4.2 Submitting the Assets .................................................................................................................................13 
4.3 Submitting Registration Information ...........................................................................................................13 
4.4 [[default]] Registration ....................................................................................................................................13 
The Fund/SERV side .......................................................................................................................................... 18 
5.1 Record Type 018 ACATS-Fund/SERV Transfer Re-Registration ..............................................................18 
5.2 Record Type 019 ACATS-Fund/SERV Transfer Acknowledgment/Rejection ............................................30 
5.3 Record Type 080 ACATS-Fund/SERV Transfer Reminder ........................................................................33 
5.4 ACATS Fund/SERV Statistics Report ........................................................................................................34 
Frequently Asked Questions ............................................................................................................................ 38 
For More Information ......................................................................................................................................... 41 
Appendix A: Glossary of ACATS Terms .......................................................................................................... 42 
 

---

## Page 4

USER GUIDE: ACATS-Fund/SERV 
Introduction 4 
INTRODUCTION 
1.1 About ACATS-Fund/SERV 
ACATS-Fund/SERV eliminates much of the manual, paper-intensive processing that occurs when an account 
is transferred from one [[Broker]] or bank to another. The number of errors associated with manual  account re-
registrations and the costs associated with failed re-registrations are significantly reduced. Shareholders 
experience a smooth and efficient transfer of their fund assets. 
1.2 Purpose of Document 
The purpose of this document is to describe the ACATS-Fund/SERV process and assist the [[Mutual Funds]], 
brokers-dealers, and banks in processing information transmitted from ACATS-Fund/SERV. This document 
also serves as a guide to help these entities determine what information is to be communicated back to 
ACATS-Fund/SERV. 
1.3. Background 
ACATS was implemented in 1985 to expedite the transfer of customer accounts from [[Broker]] to [[Broker]].  
The ACATS-Fund/SERV link was set up in 1989 to add the capability of transferring [[Mutual Funds]] from one 
account to another.  The receiving firm enters the transfer instructions into the ACATS systems.  When a 
mutual fund is involved, ACATS sends these instructions (via 018 records) to Fund/SERV.  Fund/SERV then 
transmits the 018 records to the fund.  These records provide the instructions of how to re-register the assets in 
a customer’s account held at that mutual fund.  
The following are the record types used to communicate information between ACATS and Fund/ SERV: 
• Record Type 018–ACATS-Fund/SERV Transfer Re-registration 
• Record Type 019–ACATS-Fund/SERV Transfer Acknowledgment/Rejection 
• Record Type 080–ACATS-Fund/SERV Transfer Reminder 
1.4. Processing Times 
The ACATS system functions as a multi-batch process. A [[participant]] has more than one opportunity during the 
day to request an account, submit assets, submit registrations, or make an adjustment. Cut -off for registration 
input to ACATS is 4 pm ET.  ACATS sends mutual fund re-registration instructions to Fund/SERV throughout 
the day, beginning in cycle 14.  
• Record Type 018 (transfer re-registration information) is passed to the funds beginning in cycle 14 
(approximately 12:00 noon ET) and will continue through cycle 22 (approximately 7:00 pm ET).   
 
• Record Type 019 (transfer acknowledgment/rejection) is expected back from the funds by 11:00 am ET 
on T+2.  If the transfer is acknowledged by 11:00 am ET on [[settlement]] day, ACATS reverses the incentive 
charge applied to that transfer. 
 
• Record Type 080 (transfer reminder) is passed to the funds between 8-9 pm ET. 
 

---

## Page 5

USER GUIDE: ACATS-Fund/SERV 
Introduction 5 
Note: Effective February 24, 2020, the process was enhanced to allow ACATS-Fund/SERV Transfer (018) records 
be sent to the funds multiple times a day (instead of once).   There were no changes to Fund/Acknowledgement 
(019) process or Reminder (080).  Below is an example of the timeline for 019 records: 
Acknowledgement 019 records received from funds prior to 11:00 am on T+1 will continue to be sent to ACATS 
that day. 
Acknowledgement 019 records received after 11:00 am on T+1 will continue to be sent to ACATS the next day.  
Example: Fund receives Transfer record 018 on Monday at 2:00 pm in cycle 16.  Fund sends Acknowledgement 
019 record in cycle 18 on same day.  Fund/SERV will pass 019 record to ACATS on T+1 (Tuesday) to be included in 
Fund/SERV statistics report. 
Funds will continue to have until 11:00 am on T+2 to acknowledge ACATS-Fund/SERV transfers.  
080 Reminder records will continue to be sent on all ACATS-Fund/SERV transfers that have not been responded to 
on T+1.    

---

## Page 6

USER GUIDE: ACATS-Fund/SERV 
Tips for [[Broker]]/dealers, banks, and [[Mutual Funds]] 6 
TIPS FOR [[Broker]]/DEALERS, BANKS, AND MUTUAL 
FUNDS 
2.1 Tips for [[Broker]]/Dealers and Banks 
Below are some useful tips that will help achieve the maximum benefits of ACATS-Fund/SERV. If you have 
any questions, please call your [[DTCC]] Relationship or Wealth Management Services at (212) 855-8877. 
1. Security Issue Ids (CUSIPs) that are eligible for mutual fund processing are not necessarily eligible for 
ACATS-Fund/SERV processing. Within [[NSCC]]’s Mutual Fund Security Master file (Autoroute #02112198) 
is an indicator showing if a mutual fund Security Issue [[ID]] is eligible for ACATS-Fund/SERV. You can use 
this weekly file (distributed every Friday) to identify Security Issue Ids that aren’t eligible. We suggest that 
you then contact the fund family to request that these Security Issue Ids be made eligible for ACATS-
Fund/SERV. 
 
2. Note: there is a timing difference between non-standard and full transfer types when submitting re-
registration info. The timeframe for submitting non-standard re-registrations is shorter than for full 
transfers. 
Further information can be obtained from ACATS reference manual located on the ACATS section of the 
[[DTCC]] Learning Center https://dtcclearning.com/products-and-services/equities-clearing/acats/acats-
users.html 
 
3. Verify that sales/trading agreements are in place between the receiving [[Broker]]/dealers, banks, and the 
mutual fund company. If there is no agreement in place, then, as a receiver, you would select the 
Receiver [[Asset]] Delete function in ACATS. This function enables the receiving firm to remove a specific 
mutual fund [[Asset]] from the [[Asset]] list submitted by the deliverer. Please note [[NSCC]] does not retain 
sales/trading agreements. To obtain agreement information, it will be necessary to c ontact the trading 
parties directly. 
 
4. Correct use of the BIN/FIN indicator on the re-registration form is critical to properly identify receiving and 
delivering firms and results in fewer fund rejects. 
 
5. Be certain that [[NSCC]] has the most up-to-date [[default]] registration information for your firm, specifically 
your firm’s complete address and current tax [[ID]]. In addition, please ensure that your tax [[ID]] on the [[DTC]] 
[[Broker]] Masterfile is current. 
 
6. Useful information about your ACATS-Fund/SERV re-registration activity is available on the ACATS 
Statistical Reports. These reports show the top funds by transaction volume that are rejecting your          
re-registrations, the most frequent reasons why funds are rejecting them and the firms that you either 
move accounts to or receive accounts from.  
To see this information, it is necessary to access the ACATS Transactional Inquiry application. Please 
contact your Super Access Coordinator for user access.  Below is the link to the [[DTCC]] Learning Center 
where the ACATS Statistical Reporting User Guide and ACATS Super Access Coordinator Guide are 
available under the ACATS Resources tab of Learning filtered for User Guides. 
 
7. Bank trust departments using ACATS-Fund/SERV must also be users of Fund/SERV. Eligibility for one 
service does not automatically mean eligibility for the other. Additionally, make sure that there is a trading 

---

## Page 7

USER GUIDE: ACATS-Fund/SERV 
Tips for [[Broker]]/dealers, banks, and [[Mutual Funds]] 7 
relationship already in place between your firm and the fund, as this facilitates the re- registration of mutual 
funds through ACATS-Fund/SERV. 
 
8. Be aware that the “New” or “Existing” indicator on the re-registration form determines how the fund 
registration is processed. Incorrect use of the indicator is a leading cause of items being rejected by funds.  
 
9. Firms should adopt the practice of submitting mutual fund transfer instructions to ACATS as early as 
possible.  This will provide funds additional time to identify accounts earlier and to ‘work’ pending transfers 
not in good order. 
2.2 Tips and Best Practices for Mutual Fund [[Companies]] 
1. When submitting a Fund/SERV Security Issue [[ID]] Change or Add form, review the ACATS-Fund/SERV 
Eligibility indicator to verify that the Security Issue [[ID]] is marked eligible for ACATS-Fund/SERV. The 
[[default]] for this field is YES, making all Security Issue Ids eligible for ACATS-Fund/SERV unless the field is 
changed to NO. If you select NO, please indicate the reason. 
 
2. To prevent transfers from being purged, either reject or acknowledge the ACATS fund re- registrations 
upon receipt. This reduces lag time and increases customer satisfaction. We also suggest that you 
establish a procedure within your firm that tracks [[NSCC]] reminders to ensure that items not initially acted 
upon are resolved in a timely manner. 
 
3. To minimize fund rejects, make certain that the ACATS-Fund/SERV eligibility code is the same on both 
your [[transfer agent]]’s files and the [[NSCC]] Masterfile for the Security Issue [[ID]]. 
 
4. If re-registration data is continually omitted, please contact your [[Broker]]/dealers, bank, or [[Mutual Funds]] 
Relationship or Wealth Management Services at (212) 855-8877 area for assistance. 
 
5. Secondary Social Security Number: 
If the secondary social security number is provided on the 018 record, it should be included as part of the 
search criteria when identifying accounts. This will assist funds in identifying the account to be transferred 
if multiple account owners are a party to the transfer. 
 
6. Fund [[settlement]] Date: 
Funds should populate this field with the trade date. This date represents the effective date that the 
transfer moved on the books of the Fund.  Funds that process as-of transfers should populate this field 
with the as-of date. This information should allow firms to synchronize their books with the fund’s 
[[settlement]] date and, based on the fund’s rules, assist in calculating the accrual for the account.  
 
7. Funds should begin to ‘work’ transfers that are not in good order (soft rejected) as soon as possible.   
 
 
 
 
 

---

## Page 8

USER GUIDE: ACATS-Fund/SERV 
Tips for [[Broker]]/dealers, banks, and [[Mutual Funds]] 8 
Below are scenarios that may occur and the recommended best practices for funds. 
 
Scenario 
(018 file received by fund company)  
Action  
Accept request 
Best Practice  
(For mutual fund [[Companies]])  
Same [[NSCC]] [[ID]] to Same [[NSCC]] [[ID]] 
(transfer within the same Omnibus 
fund/account)  
 
Accept request  
[[DO]] not reject the Fund/SERV ACATS (018) 
record. These are either transfers between a 
clearing firm and its underlying clients or 
between two clearing firm’s clients.  
 
New account not created for an ACAT to 
New  
 
Suspend request  
 
•  [[Option]] 1 - Make outcall to firm and   
request further information so that the     
018 record can be updated and accepted.  
• [[Option]] 2 – Request a B50 from the firm   
and accept 018 if new account is received   
and in good order. *Timing consideration:   
This [[Option]] is feasible when the 018 
ACATS-Fund/SERV record is received in a 
cycle prior to the Networking file, and the 
firm can submit the B50 so that it is 
delivered to the fund on that evenings 
networking cycle, which is Day 1 (or same 
day) that the ACAT 018  record was 
received.  
• [[Option]] 3 – Without successful completing   
[[Option]] 1, [[Option]] 2, or both options, reject  
request prior to the cutoff.  
 
 
Rejected Retail to [[Broker]]/PTF ACATS  
 
Reject request – 
Application of reject codes  
 
Utilize the appropriate reject code for 
Position Transfer Fund (PTF) rejects (see 
Reject Codes below).  
 
 
Omnibus firm versus Non-Omnibus firm 
ACAT  
 
Action determined by fund 
company’s internal 
practices  
 
Review system rules to understand how 
variances by relationship may be needed 
and/or could be supported.  
 
 
Share amount exceeds account balance/ 
Insufficient [[shares]]  
 
Suspend request – call 
firm and confirm amount  
 
Scenario is a partial transfer for a specific 
amount, where the available difference is 
minimal/fractional [[shares]].  
Outcall to verify amount/all [[shares]] through a 
telephone call or other verification method.  

---

## Page 9

USER GUIDE: ACATS-Fund/SERV 
Tips for [[Broker]]/dealers, banks, and [[Mutual Funds]] 9 
Update and process the 018 record or reject 
it depending on outcome.  
 
 
 
 
 
 
Reject Codes 
 
Below is a list of reject codes as well as the best practices and recommended actions pertaining to them:    
Reject 
Code Description Best Practice Recommended Action for 
Firm 
019 Money Amount/Number of 
[[shares]] missing/invalid 
For ACATS-Fund/SERV transfers, if 
account has $0 balance, use 712 (Zero 
Balance Account). 
 
If there are not enough [[shares]] in the 
account to satisfy the request on an 
ACATS-Fund/SERV transfer, use 713 
(Requested amount exceeds [[shares]] 
available) 
 
To be used only by [[NSCC]] when the 
money amount or number of [[shares]] is 
missing or invalid (i.e., format). 
Review if money amount or 
number of [[shares]] submitted were 
missing or an invalid format. 
Resubmit if can be corrected. 
060 [[liquidation]] exceeds book 
share balance 
[[DO]] not use for ACATS-Fund/SERV 
transfers. See reject code 713 
(Requested amount exceeds [[shares]] 
available) 
 
Only to be used for [[liquidation]] requests. 
NA–reject code 060 should not be 
used for ACATS-Fund/SERV 
transfers. 
098 Other error To be used only if error cannot be 
defined by an existing reject code. 
Contact fund or resubmit through 
manual channel 
099 Multiple Rejects To be used when there are multiple 
reasons for rejecting item. 
Contact fund or resubmit through 
manual channel 
712 Zero Balance Account To be used when an account has $0 
balance 
Contact client to determine 
necessary action. 
713 Requested amount 
exceeds [[shares]] available 
The account balance is greater than 
$0but there are not enough [[shares]] in the 
account to satisfy the request. 
Contact client and resubmit for 
correct amount 

---

## Page 10

USER GUIDE: ACATS-Fund/SERV 
Tips for [[Broker]]/dealers, banks, and [[Mutual Funds]] 10 
714 Not PTF (Position 
Transfer Fund) Eligible 
To be used when an account type or 
fund is not able to transfer through a 
PTF. Example: retirement account, etc. 
Paperwork is needed. 
Manual Transfer Request 
715 Simple IRA under 2 years To be used when a Simple IRA account 
has not satisfied the 2-year holding 
period. 
Review Fund Policy and contact 
client. 
716 Account not found Account cannot be found. Possible 
reason for reject is incorrect account 
number, etc. 
Contact Fund or clarify with client 
717 Duplicate Request To be used when a duplicate request is 
submitted. 
None-[[DO]] not call fund; [[DO]] not 
resubmit 
    
281 Purged ACATS-
Fund/SERV transfer 
[[NSCC]] generated reject code for purged 
transfers not acknowledged by funds 
(019 record) within the allotted 
timeframe. 
 
To be used only by [[NSCC]]. 
Contact Fund to determine reject 
reason or submit manually. 
 
 

---

## Page 11

USER GUIDE: ACATS-Fund/SERV 
Walkthrough of a mutual fund transfer using ACATS-Fund/SERV 11 
WALKTHROUGH OF A MUTUAL FUND TRANSFER 
USING ACATS-FUND/SERV 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
  
 
 
 
 
 
 
 
  
1 
2 3 
4 
5 
6 
7 
8 
TIF Record 
The receiver requests the 
account to be transferred by 
submitting a transfer initiation 
file (TIF) into ACATS and 
ACATS passes the file to the 
deliverer. The account is in 
Request status. See 
Requesting the Account 
Transfer12 
AT Record 
The deliverer, after receiving the TIF, submits to the receiver 
through ACATS an [[Asset]] transfer (AT) input record that lists the 
assets for that account, including mutual fund [[Asset]] information. 
The account is in Review status. See 
Submitting the Assets 
 
FR Record 
The receiver reviews 
the assets (ensuring 
the account meets 
with the receiver’s 
credit policy) and 
submits a mutual fund 
registration (FR) input 
record to ACATS 
before the end of the 
ACATS Review 
period. See 
Submitting 
Registration 
Information 
[[default]] Registration 
If, by the end of the review 
period, the receiver fails to 
submit a fund registration 
(FR) record for all eligible 
mutual fund assets due to be 
re-reregistered through the 
ACATS-Fund/SERV 
automatic link (ACATS 
settling location 10, ACATS-
Fund/SERV), ACATS 
generates a [[default]] account 
registration on behalf of the 
receiver and passes it to the 
ACATS-Fund/SERV link. See 
[[default]] Registration 
 
Record Type 018 
ACATS creates Record Type 
018 (a combination of fund 
registration (FR) input 
information from the receiver 
and pertinent fields from the 
deliverer’s [[Asset]] record) and 
passes it to Fund/SERV which 
passes it to the mutual fund. 
See 
Record Type 018–ACATS-
Fund/SERV Transfer Re-
Registration 
 
Record 019 
The mutual fund creates Record 019 (to 
either acknowledge or reject the transfer) 
and passes it to Fund/SERV which 
passes it to ACATS. See 
Record Type 
019–ACATS-Fund/SERV Transfer 
Acknowledgment/Rejection 
 
Mutual Fund Statistics Report 
The status of Record 019 is detailed in 
the ACATS-Fund/SERV mutual fund 
statistics report. ACATS creates this 
report and distributes it to both receiver 
and deliverer. See ACATS-Fund/SERV 
Statistics Report 
 
Record type 080 
If the mutual fund does not reply to 
the 018 record with a 019, one 
transfer reminder (Record type 
080) will be sent to the fund the 
first business day after Record 018 
has been sent. 
Fund/SERV will delete a transfer 
request on T+2 if 019 is not 
received by 11:00 am. ET. 019s 
submitted after 11:00 EST will be 
rejected back to the fund. See 
Record Type 080–ACATS-
Fund/SERV Transfer Reminder 
 
DELIVERING Bank/[[Broker]] 
 
RECEIVING Bank/[[Broker]] 
7 
 
Mutual Fund 
6 
5 
4 
 8 
Fund/SERV 
ACATS 
2 
1 
Request 
 Request 
Review 
 Review 
Settle Prep 
3 

---

## Page 12

USER GUIDE: ACATS-Fund/SERV 
The ACATS side 12 
THE ACATS SIDE 
The ACATS side of the ACATS- Fund/SERV process comprises the first half of transferring mutual fund assets 
from one owner to another through the ACATS-Fund/SERV system. The following records are transmitted: 
• Transfer Initiation (TI) Record 
Request for account transfer sent by the receiving bank/[[Broker]] to the delivering bank/[[Broker]]. When this 
record is transmitted, the account transfer process is in the Request stage. 
• [[Asset]] Transfer (AT) Record 
List of account assets, including mutual fund information, sent by the delivering bank/[[Broker]] to the 
receiving bank/[[Broker]]. When this record is transmitted, the account transfer process is in the Review  
stage. 
• Fund Registration (FR) Record 
Mutual fund [[Asset]] information sent by the receiving bank/[[Broker]] through ACATS and Fund/SERV to the 
mutual fund. When this record is transmitted, the account transfer process is in the Settle -Prep stage. 
• [[default]] Registration 
If no FR record has been submitted to ACATS, ACATS creates [[default]] mutual fund registration 
information and sends it to Fund/SERV. 
4.1 Requesting the Account Transfer 
The ACATS-Fund/SERV account transfer process begins when the new account holder (the receiver) submits a 
Transfer Initiation (TI) record through ACATS to the present account holder (the deliverer). At this point the 
account is in Request status. 
This Transfer Initiation File (TIF) requests [[BASIC]] account information and contains the following fields:  
Items marked with a red asterisk (*) are required. 
Field Name Field Value/Description 
Account Type* Choose the customer's account type from a list if you are the original receiver. 
Comments Type any additional notes or information about this full transfer not already covered by 
the entry fields. Create line breaks by pressing ENTER-otherwise your text consists of 
a single line. 
Customer Name* Type the customer's name. You can enter a maximum of 60 characters. 
Deliverer Customer Account 
Number* 
Type the deliverer's account number for the customer. You can enter a maximum of 20 
characters. 
Original Deliverer* View, choose, or type the 4-digit membership number of the [[NSCC]] [[participant]] 
originally delivering the transfer of assets. This field differs according to your user type: 
• If you are logged in as a [[participant]], your [[participant]] number appears in this field by 
[[default]]. 
• If you are logged in as a Service Bureau, this field becomes a drop-down list that 
contains all [[participant]] numbers to which you have access. 
• If you are logged in as an [[NSCC]] Branch Office, this field is empty. 
Original Receiver* Type the 4-digit membership number of the [[NSCC]] [[participant]] originally receiving the 
transfer of assets. 

---

## Page 13

USER GUIDE: ACATS-Fund/SERV 
The ACATS side 13 
Field Name Field Value/Description 
Primary SSN* Type the customer's Social Security number. Use a nine-digit numeric format without 
hyphens or spaces. 
Receiver Correspondent 
Number 
Type the 4-digit Receiver Correspondent number if the receiving [[participant]] is acting on 
behalf of another party. 
Receiver Customer Account 
Number* 
Type the receiver's customer account number. You can enter a maximum of 20 
characters. 
Receiver OCC [[Broker]] Number Type the five-character Receiver Options Clearing Corporation [[Broker]] number. This 
field is required only if the OCC clearing number is different from the [[NSCC]] clearing 
number. 
Secondary SSN Type the customer's secondary Social Security number. Use a nine-digit numeric 
format without hyphens or spaces. 
4.2 Submitting the Assets 
Once the receiver has submitted a Transfer Initiation (TI) record to the deliverer through ACATS, the deliverer 
responds to the TI by submitting an [[Asset]] Transfer (AT) record to the receiver. The AT record lists the assets 
for that account, including mutual fund [[Asset]] information. 
Once the receiver receives the [[Asset]] transfer record, the account has moved from Request status to Review 
status. 
4.3 Submitting Registration Information 
Once the receiver has reviewed the [[Asset]] record from the deliverer, the receiver submits a Mutual Fund 
Registration (FR) record to ACATS before the end of the Review period. Once the FR record is submitted, the 
account transfer has passed from Review status to Settle-Prep status. 
4.4 [[default]] Registration 
If the [[participant]] receiving a mutual fund [[Asset]] fails to input a fund re-registration (FR) record during the 
Review period, or if the re-registration is rejected by ACATS, the ACATS system creates a [[default]] mutual fund 
registration. The [[default]] registration is created from a combination of general [[default]] values and user -defined 
profile data. 
 
The ACATS system [[default]] mutual fund registration contains the following fields:  
Field Name Field Value/Description 
ACATS Control Number The ACATS control number is used to identify the account transfer in the ACATS-
Fund/SERV system. The number consists of the ACATS-generated control number 
combined with the [[Asset]] sequence number of the mutual fund [[Asset]]. The format is 
‘CCYYDDDNNNNNNNSSSSSS’ where: 
• CC Century when record was submitted 
• YY Year when the transfer is initiated 
• DDD Julian date when the transfer is initiated 
• NNNNNNN System assigned sequence number, beginning at ‘0000001’ for 
  each ‘CCYYDDD’ 
• SSSSSS [[Asset]] sequence number of that mutual fund 

---

## Page 14

USER GUIDE: ACATS-Fund/SERV 
The ACATS side 14 
Field Name Field Value/Description 
Account Representative 
Name 
The name of the account representative at the receiver. 
Account Representative 
Number 
The account number of the account number at the receiver. 
Account Type Indicator Required when transfer type is “A” (add) and requested settling location is “10” 
(Fund/SERV). 
1=Customer Name 
2=[[street name]] 
Book/Physical Share 
Indicator 
The format of the [[Asset]] being transferred. Values are: 
1=Transfer in and out Book (Record 018) 
0=Book [[shares]]-BIN provided (FR record) 
Branch Identification Number The number identifying the account representative’s branch office, the branch office 
of the firm submitting the FR record. 
CDSC Indicator Deliverer Indicates whether the Contingent Deferred Sales Charge (CDSC) is applicable 
and/or how the deliverer provides CDSC information to the receiver and the mutual 
fund (CDSC is known as Share Aging in Fund/SERV). Values are: 
0=Not Applicable 
1=Delivering firm will provide CDSC information within Networking 
2=Delivering firm will provide CDSC information outside Networking 
CDSC Indicator Receiver Indicates whether the Contingent Deferred Sales Charge (CDSC) is applicable and 
whether the receiver requires CDSC information (CDSC is known as Share Aging in 
Fund/SERV). Values are: 
0=Not Applicable 
1=Receiving firm requires CDSC information. If the user defined profile value is not 
provided, then this field defaults to spaces 
Check Writing Privileges 
Indicator 
Value is 0=No 
Currency Indicator Indicates the nationality of the currency involved in the account transfer. The ISO 
currency code is required when the [[Asset]] pricing category is in foreign currency. 
When not entered, the [[default]] currency code is USD 
Customer Account Number at 
Firm 
The account number of the customer at the receiving firm. 
Customer Account Number at 
Firm (Delivering Firm) 
The account number of the customer at the delivering firm. 
Customer Account Number at 
Fund (Delivering Firm) 
The account number of the customer at the mutual fund that corresponds to the 
customer’s account number at the deliverer. 
Customer Name The name of the customer for which the account is being transferred. 
Customer Name End Line The line number on which the customer’s name and address ends. 

---

## Page 15

USER GUIDE: ACATS-Fund/SERV 
The ACATS side 15 
Field Name Field Value/Description 
Customer Name/Address 
Lines 1–6 
The six lines used to record the customer’s name and address. 
Customer Zip Code Syntax is 5-digit Zip Code+4-digit Zip-Four+2 digits for future postal expansion. 
[[default]] Registration Value is 1=[[default]] Registration 
Delivering Firm Number The identification number of the firm from which the account is being transferred. 
[[Dividend]] Code (Optional) User Defined Profile. The [[default]] is the [[Dividend]] code on the mutual fund 
[[Asset]] from the deliverer. 
Firm Membership Indicator 
Deliverer 
Values are: 
Space=[[Broker]] 
01=Trust 
Firm Membership Indicator 
Receiver 
User defined profile value. If not provided, consists of spaces (implies [[Broker]]). 
Firm Number The identification number of the firm that is the receiver in the account transfer. 
Fraction Indicator Value is 1=Transfer fraction 
Full/Partial Indicator Values are: 
1=Full Transfer (moves all [[shares]] in the account) 
2=Partial Transfer (moves the exact quantity specified on the [[Asset]] input) 
Fund Account Indicator Value is 0=New account–domestic 
Fund Number Fund Number of the Security Issue [[ID]] 
[[Margin]] Account Indicator Value is 0=No 
NAV Account Indicator Value is 0=No 
Network Control Indicator 
(Delivering Firm) 
Required when the transaction type is “A” (Add) and the requested settling location 
is “10” (Fund/SERV). 
Values are: 
0=Transfer in and out: Book [[shares]]. BIN specified 
1=Transfer in and out: Book [[shares]]. FIN specified 
2=Transfer in: Book [[shares]]. Transfer out: Physical FIN specified 
Network Control Indicator 
(Receiving Firm) 
User Defined Profile. [[default]] is 0=Non-Networked 
Number of Payables Value is 00=No payables 
Originator Type Value is B=Firm 
Payable Information Indicator Value is 0=Address of record 
PI Delivery Spaces 

---

## Page 16

USER GUIDE: ACATS-Fund/SERV 
The ACATS side 16 
Field Name Field Value/Description 
Security Issue Check Digit Zeros 
Security Issue Country Code Zeros 
Security Issue [[ID]] Required when transaction type is “A” (add) and [[Asset]] description is spaces unless: 
• Requested settling location is “30” (undeliverable) and [[Option]] category is greater 
than zeros or… 
• Requested settling location is “35” (OCC) or… 
• Requested settling location is “40” (Cash Balance) or… 
• Requested settling location is “45” (Memo) and requested settling location 
reason is CASH, COMT, or SMA 
[[settlement]] Date ACATS [[settlement]] date for this transfer. 
Social Code Values are: 
18=Networking Sub-acct if Level=3 
06=[[Broker]]/Dealer for all other levels 
15=Trusts (for Banks) 
SSN/EIN Indicator Value is 0=Tax [[ID]] number 
SSN/EIN Number Tax identification number of the ACATS [[participant]] receiving the mutual fund [[Asset]]. 
State of Sale Spaces 
Transaction Type Value is 1=Transfer to new account 
Transfer Disbursement 
[[Option]]–Accruals 
Value is 4=Reinvest–Receiving firm 
Transfer Disbursement 
[[Option]]–Fractional/Cash in 
Lieu 
Value is 4=Reinvest–Receiving firm 
Transfer Disbursement 
[[Option]]–Residuals 
Value is 4=Reinvest–Receiving firm 
Transfer Dollar Amount The field consists of a floating decimal denoted by a comma (,). When the ISO 
Currency Code field is USD (U.S. Dollars), there can be only two decimal places. 
When the [[Asset]] Pricing Category is FCUR (Foreign Currency), up to four decimal 
places are supported before truncation occurs. 
The [[Asset]] Amount field is required when the transfer type is “A” (add) unless: 
• Transfer type is PTR and The [[Asset]] Request Transaction Code is 1 or 2, or… 
• Requested settling location is “45” (memo) and Requested Settling Location 
Reason is CASH, COMT, or SMA, or… 
• Requested settling location is “60” (IPS) 
Transfer Share Quantity The field consists of a floating decimal denoted by a comma (,). Up to four decimal 
places are supported before truncation occurs. 
The Transfer Share Quantity field is required when the transfer type is “A” (add) 
unless: 
• Transfer type is PTR and the [[Asset]] Request Transaction Code is 1 or 3, or… 
• Requested settling location is “40” (cash balance) or… 
• Requested settling location is “45” (memo) and Requested Settling Location 
Reason is CASH, COMT, or SMA, or… 

---

## Page 17

USER GUIDE: ACATS-Fund/SERV 
The ACATS side 17 
Field Name Field Value/Description 
• Requested settling location is “60” (IPS) 
Withholding Indicator Value is 0=Certified (W9 on file) 
Note: 
All other fields in the [[default]] registration are spaces. 

---

## Page 18

USER GUIDE: ACATS-Fund/SERV 
The Fund/SERV side 18 
THE FUND/SERV SIDE 
The Fund/SERV side of the ACATS-Fund/SERV process comprises the second half of transferring mutual fund 
assets from one owner to another through the ACATS-Fund/SERV system. The following records are 
transmitted: 
• Record Type 018 
The ACATS-Fund/SERV transfer registration record created by ACATS and passed to the mutual fund 
through Fund/SERV. 
 
• Record Type 019 
The ACATS-Fund/SERV Transfer Acknowledgment/Rejection record created by the mutual fund and 
passed to ACATS through Fund/SERV. 
 
• Record 080 
An ACATS-Fund/SERV Transfer Reminder is sent to the mutual fund if they have not responded to a 
transfer with a 019 Acknowledgment/Reject record by 8:00 pm on T+1. T+1 Transfer reminders are sent 
with reminder age date of 1.  
 
• ACATS-Fund/SERV Statistics Report 
Details the status of Record 019 and distributes it to the receiving and delivering bank/brokers.  
5.1 Record Type 018 ACATS-Fund/SERV Transfer Re-Registration 
Record type 018, the ACATS transfer re-registration record, is passed from the ACATS system to the mutual 
fund [[Companies]] via Fund/SERV. The registration information is supplied by the firms or created from [[NSCC]] 
[[default]] information (see [[default]] Registration). Funds use the transfer re-registration record to re-register 
mutual fund assets from a delivering firm to a receiving firm during the transfer process.  
Record type 018, the ACATS-Fund/SERV Transfer Re-registration record, contains the following fields: 
Field Name Field Value/Description 
ABA Routing Number The American Bankers Association routing number assigned to this account transfer. 
ACATS Control Number • The ACATS control number is used to identify the account transfer in the ACATS-
Fund/SERV system. The number consists of the ACATS-generated control 
number combined with the [[Asset]] sequence number of the mutual fund [[Asset]]. The 
format is ‘CCYYDDDNNNNNNNSSSSSS’ where: 
• CC Century when record was submitted 
• YY Year when the transfer is initiated 
• DDD Julian date when the transfer is initiated 
• NNNNNNN System assigned sequence number, beginning at ‘0000001’ for   
                       each ‘CCYYDDD’ 
• SSSSSS [[Asset]] sequence number of that mutual fund 
Account Representative Name The name of the account representative at the mutual fund. 
Account Representative 
Number 
The identification number of the account representative at the mutual fund. 

---

## Page 19

USER GUIDE: ACATS-Fund/SERV 
The Fund/SERV side 19 
Field Name Field Value/Description 
Account Type Indicator Values are: 
1=Customer name 
2=[[street name]] 
Accrual Money Amount The amount in dollars of the money that has accrued at the mutual fund. A firm or 
trust can designate on the re-registration record the accrual money amount that is 
passed from ACATS and whether the amount represents all or none of the accrual. 
Accrual Money Amount 
Indicator 
Values are: 
A=All 
B=None 
ACH (Automatic Clearing 
House) Indicator 
Values are: 
0=No 
1=Yes 
Agent for Delivering Firm 
Number 
The identification number of the agent at the delivering bank/[[Broker]]. 
Agent for Firm Number The 4-digit number identifying the agent for the firm. 
All or None Indicator Indicates whether the account transfer is all or none. The values are: 
A=All 
B=None 
Alternate Payable 1 Indicator Values are: 
0=Non-payable mailing address 
1=Bank registration (for PAC) 
2=Other 
Alternate Payable 1 Reason Required when Alternate Payable 1 indicator is “2” (Other) 
Book/Physical Share Indicator Values are: 
1=Transfer in & out: book [[shares]] 
2=Transfer in: book [[shares]] 
3=Transfer out: physical [[shares]] 
Branch Identification Number The number identifying the account representative’s branch office. 
CDSC Payment Code The code that identifies the type of Contingent Deferred Sales Charge (CDSC) 
payment (CDSC is known as Share Aging in Fund/SERV). 
Values are: 
0=Gross 
1=Net 
2=Not applicable 
CDSC Transfer Indicator 
(Receiving Firm) 
Indicates whether the receiving firm needs Contingent Deferred Sales Charge 
(CDSC) information (CDSC is known as Share Aging in Fund/SERV). 

---

## Page 20

USER GUIDE: ACATS-Fund/SERV 
The Fund/SERV side 20 
Field Name Field Value/Description 
Values are: 
0=Receiving firm does not need CDSC info 
1=Receiving firm needs CDSC info 
CDSC Transfer Indicator 
(Delivering Firm) 
Indicates whether the delivering firm needs Contingent Deferred Sales Charge 
(CDSC) information (CDSC is known as Share Aging in Fund/SERV). Values are: 
0=Delivering firm does not hold CDSC info, or N/A for this [[Asset]] 
1=Delivering firm will provide CDSC info via Networking 
2=Delivering firm will provide CDSC info outside the system 
Check Writing Privileges 
Indicator 
Values are: 
0=No 
1=Yes 
Correction Indicator C-N=Pre-[[settlement]] correction 
P=Post [[settlement]] correction/cancellation 
Space=No correction 
Cost Basis [[Option]] Values are: 
0=Unknown 
1=FIFO (First In First Out) 
2=LIFO (Last In First Out) 
3=High Cost 
4=Low Cost 
5=Average Cost 
6=Select Lot 
Country of Origin (Country 
Code) 
The country code of the country where the transfer request originated. 
Currency Indicator Indicates the nationality of the currency involved in the account transfer. The ISO 
currency code is required when the [[Asset]] pricing category is in foreign currency. 
When not entered, the [[default]] currency code is USD. 
Customer Account Number at 
Firm 
ACATS provides two customer account number fields, one to indicate the customer 
account number at the fund and the other to indicate the customer account number at 
the firm. There are separate fields for the receiving firm account information and for 
the delivering firm account information. 
The fund should utilize the firm and fund account number when trying to identify the 
account. If the fund determines that it must reject the registration because it cannot 
find the appropriate account after searching both fields, the existing Fund/SERV reject 
codes of 073— Customer (FROM) Account Number at Fund Invalid and 074— 
Customer (TO) Account Number at Fund Invalid can be used. 
Customer Account Number at 
Firm (Delivering Firm) 
The customer’s account number at the delivering firm. 
Customer Account Number at 
Fund 
The customer’s account number at the mutual fund. 

---

## Page 21

USER GUIDE: ACATS-Fund/SERV 
The Fund/SERV side 21 
Field Name Field Value/Description 
Customer Account Number at 
Fund (Receiving Firm) 
The customer’s account number at the receiving firm. 
Customer Name The customer’s name. 
Customer Name End Line 
Indicator 
The line on which the customer’s name and address ends. Values are 1-6. 
Customer Name/Address Lines 
1–6 
The name and address of the customer to which the assets are to be transferred. 
Customer Zip Code Syntax is 5-digit Zip Code+4-digit Zip-Four+2 digits for future postal expansion. 
[[default]] Registration Values are: 
0=No [[default]] 
1=[[default]] Registration 
Assists the fund in determining if the registration consists of ACATS [[default]] 
information or [[participant]] submitted information. A '0' indicates [[participant]] submitted, 
a '1' indicates ACATS [[default]]. See [[default]] Registration. 
Delivering Firm Number The identification number of the delivering firm. 
Disbursement Amount Format according to Disbursement [[Option]]: 
0=99,999,999,999,999.99 
1=999,999.9999999999 
2=999,999,999,999.9999 
3=999,999,999,999.9999 
Disbursement Options 0=Fixed cash amount 
1=Fixed percentage 
2=Fixed [[shares]] 
3=Declining balance 
[[Dividend]] Code  [[Dividend]] LTCG STCG 
0 = Cash Cash Cash 
1 = Reinvest Reinvest Reinvest 
2 = Cash Cash Reinvest 
3 = Cash Reinvest Reinvest 
4 = Cash Reinvest Cash 
5 = Reinvest Cash Cash 
6 = Reinvest Reinvest Cash 
7 = Reinvest Cash Reinvest 
 
Executing [[Broker]] The identification number of the executing [[Broker]]. 

---

## Page 22

USER GUIDE: ACATS-Fund/SERV 
The Fund/SERV side 22 
Field Name Field Value/Description 
Firm Number The identification number of the firm. 
First Check Date The date of the first check. Syntax is MMDDCCYY 
Fraction Indicator 1 = Transfer fraction 
2 = [[liquidation]] fraction 
Full/Partial Indicator Indicates whether a transfer is full or partial, allowing the deliverer to specify on the 
transfer record whether the entire account position should be moved or only the exact 
[[shares]] specified. 
Values are: 
0=Full-move all [[shares]] in the account at the Fund 
1=Partial-move the exact share quantity specified 
When a fund sees a '0' (full) in the Full/Partial Indicator field, the fund should ignore 
the transfer share quantity specified and re-register the number of [[shares]] it has for 
that account. The quantity field is used by ACATS for valuation purposes, but this 
number should be ignored by the fund when ‘0’ (full) is indicated. 
When the fund sees a '1' (partial) in the Full/Partial Indicator field, the fund should only 
re-register the specified [[shares]] in the transfer share quantity if possible. If there are 
more [[shares]] requested than actual [[shares]] in the account, the fund should try to 
contact the firm to determine if it can move the available [[shares]]. 
Presently, the number of mutual fund [[shares]] transferred through ACATS-Fund/SERV 
is based on the delivering firm’s input. The actual amount registered on the fund’s 
records can be adjusted during the deliverer’s input and [[settlement]] of the ACATS 
transfer (adjustments may be due to reinvested dividends or capital gains). The 
delivering [[Broker]] must initiate a residual credit to transfer the remaining [[shares]]. 
Note: 
The fund should specify the actual quantity transferred in Record Type 019, (transfer 
acknowledgment/rejection) record. See [[default]] Registration 
Fund Account Indicator Qualifies the type of account being established by the fund. The values for both 
Fund/SERV and ACATS are: 
0=New account-domestic 
1=New account-foreign 
2=Existing account-domestic 
3=Existing account–foreign 
Fund Number The [[NSCC]] 4-digit number assigned to a mutual fund customer at the mutual fund 
(This number is not known to ACATS. It is supplied by Fund/SERV). 
Fund/SERV Control Number The funds use the Fund/SERV control number to identify the account transfer. 
Fund/SERV assigns a control number to the ACATS transfer. The format is 
‘CATSAYDDDSSSSSS’ where: 
CATSA Literal 
‘CATSA’ Y  Last digit of the year 
DDD   Julian date when sent to the fund 
SSSSSS Sequential Number 
Logical Sequence Number Begins with 01. 

---

## Page 23

USER GUIDE: ACATS-Fund/SERV 
The Fund/SERV side 23 
Field Name Field Value/Description 
LOI Number/Date The number and date of the letter of intent (LOI). This field is eight digits. 
[[Margin]] Account Indicator Values are: 
0=No 
1=Yes 
Membership Identifier Identifies firm as a [[Member]] of a trust. Value is 01=Trust [[Member]]. 
Membership Identifier 
(Delivering Firm) 
Identifies the delivering firm as a [[Member]] of a trust. Value is 01=Trust [[Member]]. 
Memo Field Space to add additional information. 
Monthly Payment Indicators These 12 bytes represent 12 months respectively: 
1st byte=January 
2nd byte=February, etc. 
 
For each byte: 
0=No payment this month 
1=Yes payment this month 
NAV Account Indicator Values are: 
0=No 
1=Yes 
Network Control Indicator 
(Delivering Firm) 
Contains values to indicate the network level for the delivering firm’s account. The 
field is for the fund’s information only. 
Values are: 
0=Non-networked 
3=Matrix level 3 
4=Matrix level 4 
Network Control Indicator 
(Receiving Firm) 
Indicates the network level for the delivering firm’s account. The field is for the fund’s 
information only. 
Values are: 
0=Non-networked 
3=Matrix level 3 
4=Matrix level 4 
NRA Tax Value is 99 
Number of Payables Values are: 
00-06 
Original Deliverer Customer 
Account Number 
Underlying Customer Account Number at the Delivering Firm. 

---

## Page 24

USER GUIDE: ACATS-Fund/SERV 
The Fund/SERV side 24 
Field Name Field Value/Description 
Originating Customer Account 
Number at Firm 
Underlying customer account number at the originating firm. 
Originating Receiver Firm 
Number 
Originating receiving [[Broker]] firm number. 
Originating Delivering Firm 
Number 
Originating delivering [[Broker]] firm number. 
Originator Type Values are: 
B=Firm 
F=Fund 
PAC (Pre-Authorized Checks) 
Indicator 
Values are: 
0=No 
1=Yes 
Payable 1 Account Number The account number of the fund or firm for payable 1. 
Payable 1 Account Number 
Indicator 
Values are: 
1=Fund 
2=Firm 
Payable 1 Address [[Option]] This field references which account options use the payable address for disbursement 
of proceeds. 
Values are: 
1=Dividends 
2=Systematic withdrawals 
3=Automatic drafts 
4=[[Dividend]] and automatic drafts and systematic withdrawals 
5=[[Dividend]] and automatic drafts 
6=[[Dividend]] and systematic withdrawals 
7=Automatic drafts and systematic withdrawals 
8=Cross fund reinvest 
9=Alternate payable 
Payable 1 Name End Line 
Indicator 
The line where Payable 1’s name and address ends. Values are 1-6. 
Payable 1 
Name/Address Lines 1–6 
The six lines for the name and address of Payable 1. 
Payable 1 Security Issue [[ID]] The identification number of the security issue connected to Payable 1. 
Payable 1 Security Issue Check 
Digit 
The check number of the security issue connected to Payable 1. 
Payable 1 Security Issue 
Country Code 
The ISO country code of the security issue connected to Payable 1. 

---

## Page 25

USER GUIDE: ACATS-Fund/SERV 
The Fund/SERV side 25 
Field Name Field Value/Description 
Payable 1 Zip Code The 5-digit Zip Code+4-digit Zip-Code+2 digits for future postal expansion. 
Payable Information Indicator Allows the firm to designate how monies are paid from the account. Values are: 
0=Address of record 
1=Payable address 
2=Automatic clearing house 
3=Cash to firm 
4=Cross fund reinvest 
5=Cash to Trust (Allows a trust [[Member]] to more clearly define how cash dividends 
are to be paid out for a trust networked account. It should be used to indicate 
payout of cash dividends to the trust via networking) 
Payment Date Indicator Values are: 
01-31=Day of month 
L=Last day of month 
N=Normal fund cycle 
Physical Sequence Number Sequence starts with 01. 
PI Delivery Indicator Values are: 
0=Deliver to customer 
1=Deliver to firm 
2=Deliver to agent for firm 
Space=N/A 
Processing Date The date the transfer is processed. This field is eight digits and takes the 
MMDDCCYY format. 
Record Length Values are: 
• 0755, 0848, 0941 
(With no payables) 
• 1034, 1127, 1220, 1313 
(With 1 payable) 
• 1406, 1499, 1592, 1685 
(With 2 payables) 
• 1778, 1871, 1964, 2057 
(With 3 payables) 
• 2150, 2243, 2336, 2429 
(With 4 payables) 
• 2522, 2615, 2708, 2801 
(With 5 payables) 
• 2894, 2987, 3080, 3173 
(With 6 payables) 
Record Type Indicates the type of record, in this case 018=ACATS Transfer. 
Related Account Number The account number of any account related to the account being transferred. 
Related Account Number 
Indicator 
Values are: 
1=Fund 

---

## Page 26

USER GUIDE: ACATS-Fund/SERV 
The Fund/SERV side 26 
Field Name Field Value/Description 
2=Firm 
Related Trade Indicator Values are: 
0=No 
1=Yes 
Retirement Tax Indicator Values are: 
01=Premature withdrawal 
02=Rollover 
03=Disability 
04=Death 
05=Prohibited 
06=Other 
07=Normal 
08=Refund by excess contributions 
09=Divorce 
10=Plan revoked 
11=Fund transfer 
99=Not applicable 
ROA/LOI Value Indicates the total dollar value of the [[shares]] that need to be purchased to fulfill the 
ROA (Rights of Accumulation) or LOI (Letter of Intent) agreement. This field is 16 
positions. 
Secondary Social Security 
Number 
Secondary Social Security Number associated to Account 
Best Practice: The secondary social security number should be applied to search 
criteria when identifying accounts that may have multiple account owners. 
Security Issue Check Digit The check number of the security issue. 
Security Issue Country Code The ISO country code of the security issue. 
Security Issue [[ID]] The identification number of the security issue. 
[[settlement]] Date Displays the [[settlement]] date of the ACATS transfer. 
Shareholder Bank Account 
Number 
The bank account number of the holder of the mutual fund [[shares]]. 
Shareholder Bank Account 
Type 
Values are: 
0=Checking 
1=Savings 
2=Other 
Social Code A value of 42 indicates an institutional trust account. 
SSN/EIN Indicator Values are: 
0=Checking 

---

## Page 27

USER GUIDE: ACATS-Fund/SERV 
The Fund/SERV side 27 
Field Name Field Value/Description 
0=Tax [[ID]] number 
1=Social security number 
SSN/EIN Number The Social Security or Employee Identification Number of the account holder. 
State of Sale (State Code) The code for the state in which the sale took place. 
SWP (Systematic Withdrawal 
Plan) Indicator 
Values are: 
0=No 
1=Yes 
SWP/PAC Effective Date The effective date of the implementation of the Systematic Withdrawal Plan 
(SWP)/Pre-Authorized Checks (PAC). Date format is MMDDCCYY. An SWP allows 
shareholders to automatically [[Liquidate]] [[shares]] in the account according to an agreed-
upon schedule and amount. A PAC arrangement is a privilege that allows drafts to be 
drawn against a shareholder’s bank account for the purpose of purchasing fund 
[[shares]] on a regular basis. 
Test Indicator Indicates whether the transaction is a test or is part of production. Values are: 
0=Production 
1=Test 
TPA Number The [[NSCC]] 4-digit number assigned to a Third-Party Administrator (TPA) of the mutual 
fund [[Asset]], if any. If no TPA is associated with the ACATS transfer, the field defaults 
to spaces. 
Transaction Type Values are: 
1=Transfer to new account 
2=Transfer to existing account 
3=Firm of record change only 
Transfer Disbursement [[Option]]-
Accruals 
Values are: 
2=Cash to customer-Delivering firm 
4=Reinvest-Receiving firm (bucket to bucket) 
Note: 
For most ACATS transfers of accrual funds, [[Option]] 4, which is the accrual "bucket to 
bucket" movement from deliverer to receiver, should be used. For omnibus or house 
accounts it is possible to use [[Option]] 2, which is cashing out the accrual bucket at the 
delivering firm. 
Transfer Disbursement [[Option]]-
Fractional [[Cash-in-Lieu]] 
Values are: 
0=Cash to [[Broker]]–Delivering firm 
1=Reinvest-Delivering firm 
2=Cash to customer–Delivering firm 
3=Cash to [[Broker]]-Receiving firm 
4=Reinvest-Receiving firm 
5=Cash to customer-Receiving firm 

---

## Page 28

USER GUIDE: ACATS-Fund/SERV 
The Fund/SERV side 28 
Field Name Field Value/Description 
Note: 
Although the Transfer Disbursement [[Option]] Fractional-[[Cash-in-Lieu]] field is a required 
field for the receiver, the existing Fraction Indicator field will most likely be utilized to 
determine whether to transfer or [[Liquidate]] any fractional [[shares]]. Most funds have 
indicated that they will transfer the fractions that exist in the account to the receiver. 
This Transfer Disbursement [[Option]] Fractional-[[Cash-in-Lieu]] field can be used to 
determine where the transfer/[[liquidation]] can occur (i.e. at the deliverer or the 
receiver). If there were a discrepancy between the Fraction Indicator and the Transfer 
Disbursement [[Option]] Fractional-[[Cash-in-Lieu]] field, the fund would most likely utilize 
the Fraction Indicator field. 
Note: 
If the fund is unable to process the disbursement as requested, the fund should 
indicate the disbursement [[Option]] taken on the Transfer Acknowledgment/Rejection 
Record 019. This facilitates communication with the [[Broker]]. 
Transfer Disbursement [[Option]]-
Residuals 
Values are: 
0=Cash to [[Broker]]–Delivering firm 
1=Reinvest-Delivering firm 
2=Cash to customer-Delivering firm 
3=Cash to [[Broker]]–Receiving firm 
4=Reinvest-Receiving firm 
5=Cash to customer-Receiving firm 
Note: 
The disbursement options are not applicable for a partial transfer. However, even with 
a partial transfer, the disbursement options are required for input by the receiver in the 
ACATS system and included with the registration information for the fund. This is 
because a partial transfer request may turn into a full transfer if the requested amount 
is greater than the actual [[shares]] in the account. 
Note: 
The current re-registration record contains indicators that apply to the handling of 
fractions and payable information for the account. These above-mentioned fields only 
apply to the monies in the account during the account transfer process. 
Transfer Money Amount The dollar amount of the transfer. This field is used for valuation in ACATS and should 
not be used by the fund to determine the [[shares]] to be transferred. This field is 16 
positions. 
Transfer Share Quantity The amount of [[shares]] in the transfer. This field is 14 positions. 
W8 Certification Date The date the W-8 tax withholding was certified. Format is MMDDCCYY. 
W8 Expiration Date The date the W-8 tax withholding expires. Format is MMDDCCYY. 
W8 Override Country Code The ISO country code of the country that permits the W-8 tax form to be overridden. 
W8 Override NRA Special Rate The tax rate in the country that permits the W-8 tax form to be overridden. 

---

## Page 29

USER GUIDE: ACATS-Fund/SERV 
The Fund/SERV side 29 
Field Name Field Value/Description 
W8 Qualified [[intermediary]] 
Indicator 
Values are: 
1=QI (qualified [[intermediary]]–primary withholding) 
2=QI (Qualified [[intermediary]]–non-withholding) 
3=Non-QI (non-Qualified [[intermediary]]–non-withholding, not the [[Beneficial Owner]]) 
4=Partnership (withholding) 
5=Partnership (non-withholding) 
6=U. S. branch (non-withholding) 
7=Trust (withholding) 
8=Trust (non-withholding) 
Withhold Indicator Allows the firm to designate the customer’s tax status. Funds should use these fields 
as they would be used in Fund/SERV. 
W9 indications 
0=Certified (W-9 on file) 
1=Failure to provide tin 
2=Failure to certify tin 
3=Notification of incorrect TIN from the Secretary of Treasury 
(Withhold due to B Notice) 
4=Failure to certify backup withholding status 
5=Voluntary disclosure from payee of affirmative backup withholding status 
6=Notification to commence Backup Withholding from Secretary of 
Treasury for underreporting [[Dividend]] and/or interest payments 
(Withhold due to C Notice) 
7=Applied for social security number 
8=Exempt recipient 
9=Account(s) subject to both B and C Notice Withholding 
 
W8 indications 
A=Uncertified foreign account (no W8 form on file-backup withholding necessary) 
B=Certified foreign [[Beneficial Owner]] account (form W8-BEN on file) 
C=Certified foreign [[intermediary]] account (form W8-IMY on file) 
D=Certified valid foreign account (form W8-ECI on file with ITIN) 
E=Certified foreign exempt account (form W8-EXP on file) 
F=W8 on file-no treaty rate claimed 
G=W8 Beneficiary with TIN on file 
  

---

## Page 30

USER GUIDE: ACATS-Fund/SERV 
The Fund/SERV side 30 
5.2 Record Type 019 ACATS-Fund/SERV Transfer 
Acknowledgment/Rejection 
Record type 019, the ACATS transfer acknowledgment/rejection record, is passed from the mutual fund 
[[Companies]] via Fund/SERV to the ACATS system. The mutual fund sends the record to either acknowledge or 
reject record type 018 (the initial ACATS transfer re-registration request). 
Acknowledgement 
If the fund uses Record 019 to acknowledge the transfer on or before the [[settlement]] date, the delivering firm is 
not charged any fee because offsetting monies are processed when the fund acknowledges the transfer. The 
deliverer is credited, and the receiver debited the amount in the money [[settlement]] system.  
Rejection 
If the fund uses Record 019 with reject code to reject the transfer, the receiving and delivering firms must use 
the ACATS receive and deliver instructions to re-register the account outside the ACATS-Fund/SERV system. 
Record type 019, the ACATS-Fund/SERV Transfer Acknowledgment/Rejection record, contains the following 
fields: 
Items marked with a red asterisk (*) are required. 
Field Name Field Value/Description 
ACATS Control Number * The ACATS control number is used to identify the account transfer in the ACATS-
Fund/SERV system. The number consists of the ACATS-generated control number 
combined with the [[Asset]] sequence number of the mutual fund [[Asset]]. The format is 
‘CCYYDDDNNNNNNNSSSSSS’ where: 
• CC                Century when record was submitted 
• YY                 Year when the transfer is initiated 
• DDD              Julian date when the transfer is initiated 
• NNNNNNN    System assigned sequence number, beginning at ‘0000001’ for  
                each ‘CCYYDDD’ 
• SSSSSS        [[Asset]] sequence number of that mutual fund 
Accrual Money Amount The amount in dollars of the money that has accrued at the mutual fund. A firm or 
trust can designate on the re-registration record the accrual money amount that is 
passed from ACATS and whether the amount represents all or none of the accrual. 
Accrual Money Amount 
Indicator 
Values are: 
A=All 
B=None 
C=Not accepted 
Actual Share Quantity 
Transferred * 
This is the share quantity re-registered to the receiving account. Although the fund 
advises [[NSCC]] of the actual changed quantity, only the original quantity reported on 
the [[Asset]] input settles through ACATS. Both the original and actual quantities are 
reported to the receiving and delivering firms so that the receiving firm can update its 
records if there is a difference between original and actual quantity. 
If a partial transfer is indicated, the fund should not change the quantity on the partial 
unless the share quantity in the account is less than the quantity requested. 
If a full transfer is indicated, the fund must place the new quantity on the 
acknowledgment back to [[NSCC]]. 
All or None indicator Values are: 
A=All 

---

## Page 31

USER GUIDE: ACATS-Fund/SERV 
The Fund/SERV side 31 
Field Name Field Value/Description 
B=None 
C=Not Accepted 
Customer Account Number at 
Fund (Receiving Firm) * 
The account number of the customer at the mutual fund. 
Customer Account Number at 
Fund Indicator (Receiving 
Firm) * 
Indicates whether the receiving firm is a mutual fund or a bank/brokerage. Values 
are: 
1=Fund 
2=Firm 
Delivering Firm Number * The identification number of the delivering firm. 
Fund CDSC Transfer Indicator Indicates the fund’s response to the receiver and deliverer regarding the Contingent 
Deferred Sales Charge (CDSC). CDSC is known as Share Aging in Fund/SERV. 
Values are: 
0=Fund does not hold CDSC info, or N/A for this [[Asset]] 
1=Fund will provide CDSC info via Networking 
2=Fund will provide CDSC info outside the system 
Fund Number The identification number of the mutual fund. 
Fund [[settlement]] Date * The effective date the transfer moved on a fund’s books. 
Best Practice: Funds should populate this field with the trade date. This date 
represents the effective date the transfer moved on the books of the Fund. 
NOTE: 
Funds that process as-of transfers should populate this field with the ‘as-of’ date. 
Fund Reject Code * A value other than a space or a zero indicates rejection. This field is used to 
communicate to the firm what is wrong with the registration. Refer to the Fund/SERV 
manual for existing reject codes and use the appropriate code to reject. 
Fund/SERV Control Number * The identification number assigned to the transfer by Fund/SERV. 
Logical Sequence Number * Sequence starts with 01. 
Network Control Indicator * Values are: 
0=Non-networked 
3=Matrix level 3 
4=Matrix level 4 
[[NSCC]] Reject Code * Values are: 
Input: Space 
Output: Reject code 
[[NSCC]] Rejection Indicator * Input: Space 
Output: 
0=Accepted by [[NSCC]] 

---

## Page 32

USER GUIDE: ACATS-Fund/SERV 
The Fund/SERV side 32 
Field Name Field Value/Description 
1=Rejected by [[NSCC]] 
2=Rejected by [[NSCC]], multiple errors 
Originator Type * Value is F=Fund 
Physical Sequence Number * Sequence begins at 01. 
PI Delivery Indicator Values are: 
0=Deliver to customer 
1=Deliver to firm 
2=Deliver to agent for firm 
Receiving Firm Number* The identification number of the receiving firm. 
Record Length * The length of the record (0197, 0290). 
Record Type * Indicates the type of record (Record 019=ACATS Transfer 
Acknowledgment/Rejection). 
Security Issue Check Digit * Space. For future use. 
Security Issue Country Code * Space. For future use. 
Security Issue [[ID]] * The identification number of the security issue. 
Social Code A value of 42 indicates an institutional trust account. 
Submission Date * The 8-digit date (MMDDCCYY) on which the record was submitted. 
Test Indicator * Values are: 
0=Production 
1=Test 
Transfer Disbursement 
[[Option]]-Accruals 
Values are: 
2=The fund gave the accrual as cash to the customer at the delivering firm. 
4=The fund processed a "bucket to bucket" transfer of the accrual to the account at 
the receiving firm. 
If the fund must reject because it could not accommodate any of the transfer 
disbursement [[Option]] choices, the [[NSCC]] reject code for these fields is "134". This is a 
reject code for the full registration "Disbursement Options" field and means 
"Disbursement [[Option]] missing or invalid." 
Transfer Disbursement 
[[Option]]-Fractional [[Cash-in-Lieu]] 
Values are: 
0=The fund gave the cash to the [[Broker]] at the delivering firm. 
1=The fund reinvested at the delivering firm. 
2=The fund gave the cash to the customer at the delivering firm. 
3=The fund gave the cash to the [[Broker]] at the receiving firm. 
4=The fund reinvested at the receiving firm. 
5=The fund gave the cash to the customer at the receiving firm. 

---

## Page 33

USER GUIDE: ACATS-Fund/SERV 
The Fund/SERV side 33 
Field Name Field Value/Description 
If the fund cannot process the [[Option]] that was passed via Fund/SERV, the fund 
should find an [[Option]] that it can process and change the acknowledgment record to 
reflect the actual [[Option]] used. 
Transfer Disbursement [[Option]]-
Residuals 
Values are: 
0=The fund gave the cash to the [[Broker]] at the delivering firm. 
1=The fund reinvested at the delivering firm. 
2=The fund gave the cash to the customer at the delivering firm. 
3=The fund gave the cash to the [[Broker]] at the receiving firm. 
4=The fund reinvested at the receiving firm. 
5=The fund gave the cash to the customer at the receiving firm. 
W8 Certification Date The 8-digit date for the W8 withholding tax certification in CCYYMMDD format. 
Required if withholding indicator is B, C, D, or E. 
5.3 Record Type 080 ACATS-Fund/SERV Transfer Reminder 
An ACATS Transfer Reminder is sent via Fund/SERV when an ACATS transfer has not been acknowledged or 
rejected by the mutual fund by 8:00 pm ET on T+1. 
Once an ACATS reminder is sent, the fund can: 
• Acknowledge the transfer using record type 019 Acknowledgment. 
• Reject the transfer using record type 019 Rejection (with a valid reject code). 
• Allow the transfer to pend for up to 1½ business days. Funds must respond to the 018 request by       
11:00 am ET on T+2. 
 
If the mutual fund does not respond to a pending ACATS-Fund/SERV transfer with 019 acknowledgment/reject 
record by 8:00 pm ET on T+1, the 080 Reminder record will be sent to the fund with a reminder date of 1.  
If no response is received from the mutual fund by 11:00 am ET on T+2 the pending ACATS-Fund/SERV 
transfer is purged from ACATS.  Any 019 Acknowledgment received after 11:00 am on T+2 is rejected back to 
the mutual fund. 
The ACATS system generates ACATS-Fund/SERV receive/deliver instructions to the two parties to the transfer 
and ACATS reports the status on the ACATS-Fund/SERV Statistics Report. 
The ACATS-Fund/SERV Transfer Reminder record contains the following fields: 
Field Name Field Value/Description 
ACATS [[Asset]] Sequence 
Number 
All 6 positions should be populated with ACATS [[Asset]] Sequence Number. 
ACATS Control Number The ACATS control number is used to identify the account transfer in the ACATS-
Fund/SERV system. The number consists of the ACATS-generated control number 
combined with the [[Asset]] sequence number of the mutual fund [[Asset]]. The format is 
‘CCYYDDDNNNNNNNSSSSSS’ where: 
• CC     Century when record was submitted 
• YY     Year when the transfer is initiated 
• DDD     Julian date when the transfer is initiated 
• NNNNNNN  System assigned sequence number, beginning at ‘0000001’ for  
                           each ‘CCYYDDD’ 

---

## Page 34

USER GUIDE: ACATS-Fund/SERV 
The Fund/SERV side 34 
Field Name Field Value/Description 
• SSSSSS     [[Asset]] sequence number of that mutual fund 
ACATS TIF Number All 14 positions should be the ACATS Control Number. 
Fund/SERV Control Number The number that the fund uses to identify the transfer in Fund/SERV. 
TPA (Third Party 
Administrator) Number 
Field remains as spaces unless a TPA is associated with the ACATS transfer. 
 
5.4 ACATS Fund/SERV Statistics Report 
The status of Record 019 is detailed in the ACATS-Fund/SERV Status Report. ACATS creates this report and 
distributes it to both receiver and deliverer. 
The ACATS-Fund/SERV Status Report contains the following fields: 
Field Name Field Value/Description 
ACATS Control Number The ACATS control number is used to identify the account transfer in the ACATS-
Fund/SERV system. The number consists of the ACATS-generated control number 
combined with the [[Asset]] sequence number of the mutual fund [[Asset]]. The format is 
‘CCYYDDDNNNNNNNSSSSSS’ where: 
• CC     Century when record was submitted 
• YY     Year when the transfer is initiated 
• DDD     Julian date when the transfer is initiated 
• NNNNNNN  System assigned sequence number, beginning at ‘0000001’ for  
                           each ‘CCYYDDD’ 
• SSSSSS     [[Asset]] sequence number of that mutual fund 
Account Transfer 
Disbursement–Accruals Code 
Reduce options to only the following: 
2 =Cash to customer–delivering firm 
4 =Process bucket to bucket transfer to receiving firm 
Account Transfer 
Disbursement–
Fractional/Cash–in-Lieu Code 
Values are: 
0=Cash to [[Broker]]–delivering firm 
1=Reinvest–delivering firm 
2=Cash to customer–delivering firm 
3=Cash to [[Broker]]–receiving firm 
4=Reinvest–receiving firm 
5=Cash to customer–receiving firm 
Account Transfer 
Disbursement–Residuals Code 
Values are: 
0=Cash to [[Broker]]–delivering firm 
1=Reinvest–delivering firm 
2=Cash to customer–delivering firm 
3=Cash to [[Broker]]–receiving firm 
4=Reinvest–receiving firm 
5=Cash to customer–receiving firm 

---

## Page 35

USER GUIDE: ACATS-Fund/SERV 
The Fund/SERV side 35 
Field Name Field Value/Description 
Account Type Indicator Values are: 
1=Customer Name 
2=[[street name]] 
0=Deliver to customer 
Accrual Amount The amount in dollars of the money that has accrued at the mutual fund. A firm or 
trust can designate on the re-registration record the accrual money amount that is 
passed from ACATS and whether the amount represents all or none of the accrual. 
Accrual Amount Indicator Values are: 
A=All 
B=None 
C=Not Accepted 
Action Type Values are: 
A=Accepted/Acknowledged by Fund 
P=Pending reminder 
R=Rejected by Fund 
S=System Purge 
Actual Quantity Actual Quantity returned from the Fund via Fund/SERV. Floating decimal denoted by 
a ‘,’ (comma). 
Amount Floating decimal denoted by a ‘,’ (comma). 
[[Asset]] Description Description of the assets to be transferred. 
[[Asset]] Sequence Number The sequence number of the assets to be transferred 
CDSC Indicator Fund Indicates whether the mutual fund needs Contingent Deferred Sales Charge (CDSC) 
information (CDSC is known as Share Aging in Fund/SERV). Values are: 
0=Not applicable 
1=Delivering firm will provide CDSC information within Networking 
2=Delivering firm will provide CDSC information outside Networking 
Certification Date Format not guaranteed. Format as returned from Fund via Fund/SERV. 
Certification Number The identification number of the underlying customer’s mutual fund [[Asset]]. 
Current [[settlement]] Date The date scheduled for [[settlement]] of the account transfer. Format is CCYYMMDD 
Customer Account Number at 
Fund (Receiving Firm) 
The account number of the customer at the mutual fund. 
Customer Account Number at 
Fund Indicator (Receiving 
Firm) 
Whether the customer is an account or a firm. Values are: 
1=Fund (FIN) 
2=Firm (BIN) 
Customer Account Type Values are: IR=IRA 

---

## Page 36

USER GUIDE: ACATS-Fund/SERV 
The Fund/SERV side 36 
Field Name Field Value/Description 
4K=401K 
AG=Agency 
BC=Bank [[custody]] 
CO=Corporate 
CT=Co-Trustee 
CU=Custodian (UGMA) 
DR=Direct Rollover 
EI=Educational IRA 
ES=Estate 
JT=Joint 
MS=Medical Savings Account 
OT=Other 
QP=Qualified/Profit Sharing/Pension 
R=Roth IRA 
SI=Simple IRA 
SN=Single 
TR=Trust 
Customer Name The name of the customer to which the account is being transferred. 
Debit Credit Indicator Values are: 
C=Credit 
D=Debit 
Deliverer Customer Account 
Number 
The account number of the customer at the deliverer. 
Distribution [[participant]] The [[participant]] who receives the ACATS-Fund/SERV statistical output. 
Distribution Side Value is B=Both Original Receiver and Original Deliverer. 
[[Dividend]] Code  [[Dividend]]  
0=Cash  
1=Reinvest  
2=Cash  
3=Cash  
4=Cash  
5=Reinvest  
6=Reinvest  
7=Reinvest  
Long Term Cap Gain  
Cash  
Reinvest  
Cash  
Reinvest  
Reinvest  
Cash  
Reinvest  
Cash  
Short Term Cap Gain  
Cash  
Reinvest  
Reinvest  
Reinvest  
Cash  
Cash  
Cash  
Reinvest  
Fund [[settlement]] Date  Represents the effective date the transfer moved on the books of the Fund.  
Fund/SERV Control Number  The control number generated by Fund/SERV to identify the account transfer in the 
Fund/SERV system.  
ISIN Country Code  The code that identifies the country where the account transfer is taking place.  
ISIN Security  The code that identifies the type of [[securities]] involved in the account transfer.  
ISIN Security Check Digit  The code that identifies the country where the account transfer is to take place.  
ISO Currency Code  The code that identifies the currency involved in the account transfer. The ISO 
currency code is required when the [[Asset]] pricing category is in foreign currency. 
When not entered, the [[default]] currency code is USD.  
Logical Sequence Number  Logical sequence begins at 01.  

---

## Page 37

USER GUIDE: ACATS-Fund/SERV 
The Fund/SERV side 37 
Field Name Field Value/Description 
Network Control Indicator  Values are:  
0=Not Networked  
1=[[Broker]] controlled [[Margin]]/IRA account  
2=Customer name brokerage account  
3=[[Broker]] controlled brokerage account  
4=Fund controlled brokerage account  
Original Deliverer Number  The identification number of the original deliverer of the account to be transferred.  
Original Quantity  Original Quantity requested input. Floating decimal a ‘,’ (comma).  
Original Receiver Number  The identification number of the original receiver of the account to be transferred.  
Original [[settlement]] Date  The original date scheduled to settle the account transfer. Format is CCYYMMDD.  
Physical Sequence Number  Physical sequence begins at 01.  
PI Delivery Indicator  Values are:  
1=Deliver to clearing/settling [[Broker]]  
2=Deliver to executing [[Broker]]  
Processing Date  Format is CCYYMMDD.  
Receiver Customer Account 
Number 
The account number of the bank/[[Broker]] that receives the account transfer. 
Record Length The numerical value that indicates the record’s length. This record is 520. 
Record Type Value is F=Fund/SERV Statistics MRO. 
Reject Code See Fund/SERV manual for reject codes. 
 

---

## Page 38

USER GUIDE: ACATS-Fund/SERV 
Frequently Asked Questions 38 
FREQUENTLY ASKED QUESTIONS 
1. Once [[NSCC]] has sent [[default]] registration information to the fund, can any more registrations be 
sent to the fund? 
No. Once registration information is sent to the fund via the ACATS-Fund/SERV link, either [[default]] 
information or information supplied by the receiver via the Fund Registration (FR) record, it cannot be 
updated or changed via ACATS. 
 
2. On the Fund Registration (FR) record, can participants pick different account transfer 
disbursement options for accruals, fractional [[Cash-in-Lieu]], and residuals? 
 
The options for accruals are: 
a. [[Option]] 2 
The fund should give the accrual as cash to the customer at the delivering firm (used mainly for 
omnibus or house accounts) 
b. [[Option]] 4 
The fund should process a “bucket to bucket” transfer of the accrual to the account at the receiving 
firm (used for most transfers). 
 
3. There are several options to choose for the Account Transfer Disbursement [[Option]] fields. What is 
the purpose of these fields? 
 
The Account Transfer Disbursement Options were meant to help the fund understand how the firm w ould 
like the fund to handle the following situations that can occur during the transfer. For example:  
 
a. When a daily accrual is part of the account transfer and the [[Dividend]] was not paid during the transfer 
period, an accrual “bucket” exists as part of the account. The two disbursement options for accruals 
tell the fund what should be done. For example, if [[Option]] 4 was chosen, the fund would transfer the 
accrual bucket to the receiving account. 
b. If fractional [[shares]] are part of the transfer, the firm can tell the fund what to [[DO]] with them. For 
example, if [[Option]] 0 was chosen, cash from the fractional [[shares]] would be sent to the customer 
account at the delivering [[Broker]]. 
c. If a [[Dividend]] was paid on the day of the transfer, a residual [[Dividend]] occurs. The fund wi ll be 
instructed what to [[DO]] with that residual. If [[Option]] 3 was chosen, the cash from the residual [[Dividend]] 
will be paid to the receiving firm  
 
Note:   
See Trailing Dividends Best Practices – F55 for more information on residual dividends. These practices can be found 
under the [[Mutual Funds]] Services Networking Resources tab on the Learning Center filtered for Best Practices. 
 
These options were intended to help communication between the fund and the firm. If the firm feels that 
there are too many options, the firm can choose one or two options for all accounts and ignore the 
remaining options. If the fund cannot process a particular [[Option]], the fund should not reject the transfer. 
Instead, the fund should choose an [[Option]] that it can process and then communicate back to the firm in 

---

## Page 39

USER GUIDE: ACATS-Fund/SERV 
Frequently Asked Questions 39 
the Fund Acknowledgement record in the Fund/SERV system. The firm will see this in the Fund/SERV 
Statistics file (record type F). 
 
4. [[participant]]’s books will be out of balance if the original and actual amounts in an account transfer 
[[DO]] not match in the F (Fund/SERV Statistics) file. Will participants receive any other type of 
notification about this out-of-balance condition? 
 
No additional records are generated from ACATS for the difference between original and actual amounts 
in an account transfer. The original amount is the amount that will settle through ACATS. The likelihood of 
a difference in the original and actual amounts is strong if, for example, a full transfer was requested but 
the firm did not know the exact number of [[shares]] in the account. The firm must look at the difference 
between the original and actual amounts as an indicator that there is an out-of-balance situation and must 
correct the discrepancy on its books. 
 
For example, if a 50-share [[Dividend]] was paid during the transfer period and the original amount of the 
transfer was 1,000 [[shares]], the actual amount would be 1,050 [[shares]] and the original amount would 
remain at 1,000 [[shares]]. The receiving firm receives no additional notification. The delivering firm receives 
a Networking DIV record pertaining to the 50 [[shares]] once the [[Dividend]] is paid. 
 
5. Does the ACATS system allow a mutual fund registration to be added multiple times for the same 
[[Asset]] (for instance, the same [[Asset]] sequence number)? What will be the effect?  
 
Each time a mutual fund registration is added, any previously-held mutual fund registration data for this 
mutual fund [[Asset]] is overwritten. 
 
6. How are the BIN and FIN indicators used in ACATS? 
 
The BIN number is used to identify the [[Broker]]’s internal account number and the FIN is used to identify 
the fund identification number. Delivering firms must enter the Fund/SERV Customer Account Number on 
the [[Asset]] Transfer (AT) record and receiving firms must enter the Fund/SERV Customer Account Number 
on the Fund Registration (FR) record. The Fund/SERV Customer Account Number can be either a BIN or 
FIN number. There is a field on both the [[Asset]] Transfer (AT) and Fund Registration (FR) records titled 
Book Physical Share Indicator that allows the entry of either a BIN or FIN number. 
 
The Book Physical Share field has three values: 
 
a. 0=Transfer in-and-out book [[shares]]; the [[Broker]] account number (BIN) is supplied on the Fund/SERV 
customer account number. 
b. 1=Transfer in-and-out book [[shares]]; the fund account number is supplied on the Fund/SERV 
customer account number. 
c. 2=Transfer-in Book [[shares]], transfer-out physical [[shares]]; the fund account number (FIN) is supplied 
on the Fund/SERV customer account number. 
 
 
 

---

## Page 40

USER GUIDE: ACATS-Fund/SERV 
Frequently Asked Questions 40 
The ACATS system passes the data to the fund in the following manner: 
When the Book/Physical Share 
Indicator on the ACATS [[Asset]] 
Transfer (AT) record from the 
Deliverer is… 
…then the Customer Account 
Number at the firm, the Deliverer’s 
(BIN) on the Fund/SERV registration 
record (Record Type 018) to the 
fund, is… 
…and the Customer Account 
Number at the Fund, the Deliverer‘s 
(FIN) on the Fund/SERV registration 
record (Record Type 018) to the fund 
is… 
“0” (BIN) AT record—Fund/SERV Customer 
Account Number—Deliverer 
Spaces 
“1” (FIN) Spaces AT record—Fund/SERV Customer 
Account Number—Deliverer 
“2” (FIN) Spaces AT record—Fund/SERV Customer 
Account Number—Deliverer 
 
When the Book/Physical Share 
Indicator on the ACATS [[Asset]] 
Transfer (AT) record from the 
Receiver is… 
…then the Customer Account 
Number at the firm, the Receiver’s 
(BIN) on the Fund/SERV registration 
record (Record Type 018) to the 
fund, is… 
…and the Customer Account 
Number at the Fund, the Receiver’s 
(FIN) on the Fund/SERV registration 
record (Record Type 
018) to the fund is… 
“0” (BIN) AT record–Fund/SERV Customer 
Account Number— Receiver 
Spaces 
“1” (FIN) Spaces AT record–Fund/SERV Customer 
Account Number— Receiver 
“2” (FIN) Spaces AT record–Fund/SERV Customer 
Account Number— Receiver 
 

---

## Page 41

USER GUIDE: ACATS-Fund/SERV 
For More Information 41 
FOR MORE INFORMATION 
For questions or additional information concerning the ACATS-Fund/SERV interface, please contact your 
[[Mutual Funds]] Relationship or Account Manager at (212) 855-8877 or, for ACATS, your Clearing Services 
Relationship Manager at 212-855-4270. 
• Additional ACATS information as well as the ACATS-Fund/SERV interface record layouts mentioned in 
this guide can be accessed under the ACATS Resource tab in the [[DTCC]] Learning Center. 
 
• The ACATS-Fund/SERV record layouts (018 & 019) can be located in the [[Mutual Funds]] ACATS-
Fund/SERV page under Record Types on the [[DTCC]] Learning site at https://dtcclearning.com/products-
and-services/mutual-fund-services/record-layouts.html 
 
• (018 is in Fund/SERV Record Layout part 2, 019 in part 3). 
 
• Passwords are required to access the Learning Center. 

---

## Page 42

USER GUIDE: ACATS-Fund/SERV 
Appendix A: Glossary of ACATS Terms 42 
APPENDIX A: GLOSSARY OF ACATS TERMS 
Deliverer 
The deliverer is an [[NSCC]] [[participant]] subscribing to ACATS. The deliverer has possession of the account and 
must deliver the assets to the receiver. The receiver must subscribe to ACATS-Fund/SERV to be part of the 
ACATS-Fund/SERV link. 
Non-Standard Transfer 
This is a partial transfer, residual credit, mutual fund cleanup, fail reversal, or reclaim. Review and Settle-P rep 
statuses occur on one day and [[settlement]] occurs the next day. 
Note: 
It should make no difference to the fund if the item is a standard or non-standard transfer; as with a standard transfer, the 
fund should acknowledge as soon as possible. 
Receiver 
The receiver is an [[NSCC]] [[participant]] requesting the account be transferred through ACATS. The receiver must 
subscribe to ACATS-Fund/SERV to be part of the ACATS-Fund/SERV link. 
Request Status 
The account is in request status when a receiver submits a transfer initiation (TI) record to the deliverer through 
ACATS. 
Review Status 
The account enters review status when assets are submitted by the deliverer to the receiver for both the 
receiver and deliverer’s review. When the receiver gets the [[Asset]] list, the receiver can:  
1. Take no action. If no action is taken, the [[Asset]] transfers in two days for a standard transfer or next day for 
a non-standard transfer. 
2. Reject the transfer because either something in the account does not meet with the firm’s credit policy or  
the receiver fails to accept the non-standard transfer. 
3. Accelerate the [[settlement]] of the transfer by one day if it is a standard transfer. 
4. Receiver can delete mutual fund assets. 
 
Settle-Prep Status 
The account is in settle-prep status when the account transfer is ready for [[settlement]]. The transfer instructions 
for the account assets are sent to their proper settling organizations. At this time, the funds would receive 
Record Type 018 (ACATS-Fund/SERV Transfer Re-registration) from Fund/SERV and be expected to respond 
with Record Type 019 (ACATS-Fund/SERV Transfer Acknowledgment/Rejection). 
 
[[settlement]] Day 
The account transfer takes effect on [[settlement]] day. The deliverer is debited, and the receiver credited in 
money [[settlement]] if the ACATS transfer is valued. [[Broker]]-to-[[Broker]] transfers are valued; if a bank is on one 
side of the transfer there is no money [[settlement]] charge. 
When the fund acknowledges, there is a money [[settlement]] reversal crediting the deliverer and debiting the 
receiver the original value of the [[Asset]]. If this occurs on or before [[settlement]] date, the net charge to the ACATS 
[[participant]] is zero. 
 
 

---

## Page 43

USER GUIDE: ACATS-Fund/SERV 
Appendix A: Glossary of ACATS Terms 43 
Standard Transfer 
This is a full transfer. Normally there is one day for Review status, one day for Settle- Prep status, and then the 
item settles one day later. This transfer could be accelerated so that Settle-Prep occurs the same day as the 
Review status. 
 

---

## Page 44

 
 
© 2024 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation [[DTCC]].  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
 
Doc Info: January 31, 2024 
Publication Code: MFS355 
Service: Fund/SERV
® 
Title: User Guide: ACATS-Fund/SERV 
For More Information 
 
Email Core Learning Service at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 