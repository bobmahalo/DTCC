---
title: "User Guide: ACATS-Fund/SERV"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/acats_FundSERV_guide_mfs368_20240215.pdf"
pages: 23
size: "437.4 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# User Guide: ACATS-Fund/SERV

**Original File:** [acats_FundSERV_guide_mfs368_20240215.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/acats_FundSERV_guide_mfs368_20240215.pdf)  
**Category:** Other  
**Total Pages:** 23  
**File Size:** 437.4 KB  

---

## Page 1

 
 
FUND/SERV® 
USER GUIDE: ACATS-FUND/SERV 
FEBRUARY 15, 2024 
 

---

## Page 2

 
 
 
 
 
REVISION HISTORY 
  
February 15, 2024 To access the current version of record layouts, the sample layouts in this guide were 
removed and replaced with links to Learning. 
January 31, 2024 Rebranded document. Content reviewed. 
April 22, 2022 Learning upgrade caused some link(s) to break.  Links have been corrected. 
Effective 02/24/2020 The ACATS-Fund/SERV Transfer record (018) will be sent to the funds multiple times 
each day (changed from once per day).  For more information, please see Important 
Notices a8276 (10/27/2016), a8359 and a8736. 
Effective 02/29/2016 The T+2 080 reminder will no longer be sent to funds at 8:00 pm. Also, new reject codes 
were created. See Important Notice a8107, dated 10/27/2015. 
August 26, 2014 Updated to reflect timing of when Fund/SERV will delete a transfer request on T+2 
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
2.2 Tips and Best Practices for Mutual Fund [[Companies]] .................................................................................. 8 
Walkthrough of a mutual fund transfer using ACATS-Fund/SERV ............................................................... 12 
The ACATS side ................................................................................................................................................. 13 
4.1 Requesting the Account Transfer ...............................................................................................................13 
4.2 Submitting the Assets .................................................................................................................................13 
4.3 Submitting Registration Information ...........................................................................................................13 
4.4 [[default]] Registration ....................................................................................................................................13 
The Fund/SERV side .......................................................................................................................................... 15 
5.1 Record Type 018 ACATS-Fund/SERV Transfer Re-Registration ..............................................................15 
5.2 Record Type 019 ACATS-Fund/SERV Transfer Acknowledgment/Rejection ............................................15 
5.3 Record Type 080 ACATS-Fund/SERV Transfer Reminder ........................................................................16 
5.4 ACATS Fund/SERV Statistics Report ........................................................................................................16 
Frequently Asked Questions ............................................................................................................................ 17 
For More Information ......................................................................................................................................... 20 
Appendix A: Glossary of ACATS Terms .......................................................................................................... 21 
 

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
The following are the record types used to communicate information between ACATS and Fund/SERV:  
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
 
• Record Type 019 (transfer acknowledgment/rejection) is expected back from the funds by 11:00  am ET 
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
Further information can be obtained from ACATS reference manual located on the ACATS sectio n of the 
[[DTCC]] Learning Center https://dtcclearning.com/products-and-services/equities-clearing/acats/acats-
users.html 
 
3. Verify that sales/trading agreements are in place between the receiving [[Broker]]/dealers, banks, and the 
mutual fund company. If there is no agreement in place, then, as a receiver, you would select the 
Receiver [[Asset]] Delete function in ACATS. This function enables the receiving firm to remove a specific 
mutual fund [[Asset]] from the [[Asset]] list submitted by the deliverer. Please note [[NSCC]] does not retain 
sales/trading agreements. To obtain agreement information, it will be necessary to contact the trading 
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
 
  

---

## Page 8

USER GUIDE: ACATS-Fund/SERV 
Tips for [[Broker]]/dealers, banks, and [[Mutual Funds]] 8 
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
 
4. If re-registration data is continually omitted, please contact your [[Broker]]/dealers, bank, or M utual Funds 
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

---

## Page 9

USER GUIDE: ACATS-Fund/SERV 
Tips for [[Broker]]/dealers, banks, and [[Mutual Funds]] 9 
 
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
Update and process the 018 record or reject 
it depending on outcome.  
 
 
 
 
 

---

## Page 10

USER GUIDE: ACATS-Fund/SERV 
Tips for [[Broker]]/dealers, banks, and [[Mutual Funds]] 10 
 
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

---

## Page 11

USER GUIDE: ACATS-Fund/SERV 
Tips for [[Broker]]/dealers, banks, and [[Mutual Funds]] 11 
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

## Page 12

USER GUIDE: ACATS-Fund/SERV 
Walkthrough of a mutual fund transfer using ACATS-Fund/SERV 12 
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
Transfer13 
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

## Page 13

USER GUIDE: ACATS-Fund/SERV 
The ACATS side 13 
THE ACATS SIDE 
The ACATS side of the ACATS -Fund/SERV process comprises the first half of transferring mutual fund assets 
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
Transfer Initiat ion (TI) record through ACATS to the present account holder (the deliverer). At this point the 
account is in Request status. 
Please reference the Transfer Initiation File (TIF) record layout in the ACATS section of the Learning Center at 
https://dtcclearning.com/products-and-services/equities-clearing/acats/acats-technical-resources.html 
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
registration. The [[default]] registration is created from a combination of general [[default]] values and user-defined 

---

## Page 14

USER GUIDE: ACATS-Fund/SERV 
The ACATS side 14 
profile data. Please reference the fund re-registration record in the ACATS section of the Learning Center at 
https://dtcclearning.com/products-and-services/equities-clearing/acats/acats-technical-resources.html 
 
 

---

## Page 15

USER GUIDE: ACATS-Fund/SERV 
The Fund/SERV side 15 
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
Record type 018 can be referenced in the Mutual Fund section of the Learning Center under Record Layouts 
https://dtcclearning.com/products-and-services/mutual-fund-services/record-layouts.html 
 
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

---

## Page 16

USER GUIDE: ACATS-Fund/SERV 
The Fund/SERV side 16 
Record type 019, the ACATS-Fund/SERV Transfer Acknowledgment/Rejection record can be referenced in the 
Mutual Fund section of the Learning Center under Record Layouts https://dtcclearning.com/products -and-
services/mutual-fund-services/record-layouts.html 
 
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
The ACATS-Fund/SERV Transfer Reminder record can be referenced in the Mutual Fund section of the 
Learning Center under Record Layouts https://dtcclearning.com/products-and-services/mutual-fund-
services/record-layouts.html 
  
5.4 ACATS Fund/SERV Statistics Report 
The status of Record 019 is detailed in the ACATS-Fund/SERV Status Report. ACATS creates this report and 
distributes it to both receiver and deliverer.  Information pertaining to the Fund/SERV statistical report is 
available in the ACATS section of the Learning Center   https://dtcclearning.com/products-and-
services/equities-clearing/acats.html.  Search for Fund/SERV.  
 
 
 

---

## Page 17

USER GUIDE: ACATS-Fund/SERV 
Frequently Asked Questions 17 
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
 
The Account Transfer Disbursement Options were meant to help the fund understand how the firm would 
like the fund to handle the following situations that can occur during the transfer. For example:  
 
a. When a daily accrual is part of the account transfer and the [[Dividend]] was not paid during the transfer 
period, an accrual “bucket” exists as part of the account. The two disbursement options for accruals 
tell the fund what should be done. For example, if [[Option]] 4 was chosen, the fund would transfer the 
accrual bucket to the receiving account. 
b. If fractional [[shares]] are part of the transfer, the firm can tell the fund what to [[DO]] with them. For 
example, if [[Option]] 0 was chosen, cash from the fractional [[shares]] would be sent to the customer 
account at the delivering [[Broker]]. 
If a [[Dividend]] was paid on the day of the transfer, a residual [[Dividend]] occurs. The fund will be 
instructed what to [[DO]] with that residual. If [[Option]] 3 was chosen, the cash from the residual [[Dividend]] 
will be paid to the receiving firm. 
Note:   
See Trailing Dividends Best Practices – F55 for more information on residual dividends. These practices can be found 
under the [[Mutual Funds]] Services Networking Resources tab on the Learning Center filtered for Best Practices. 
These options were intended to help communication between the fund and the firm. If the firm feels that 
there are too many options, the firm can choose one or two options for all accounts and ignore the 
remaining options. If the fund cannot process a particular [[Option]], the fund should not reject the transfer. 
Instead, the fund should choose an [[Option]] that it can process and then communicate back to the firm in 
the Fund Acknowledgement record in the Fund/SERV system. The firm will see this in the Fund/SERV 
Statistics file (record type F). 
 

---

## Page 18

USER GUIDE: ACATS-Fund/SERV 
Frequently Asked Questions 18 
 
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

## Page 19

USER GUIDE: ACATS-Fund/SERV 
Frequently Asked Questions 19 
 
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

## Page 20

USER GUIDE: ACATS-Fund/SERV 
For More Information 20 
FOR MORE INFORMATION 
For questions or additional information concerning the ACATS-Fund/SERV interface, please contact Wealth 
Management Services at WMSConnect@[[DTCC]].com.  
• Additional ACATS information as well as the ACATS-Fund/SERV interface record layouts mentioned in 
this guide can be accessed under the ACATS Resource tab in the [[DTCC]] Learning Center. 
 
• The ACATS-Fund/SERV record layouts (018 & 019) can be located in the [[Mutual Funds]] ACATS-
Fund/SERV page under Record Types on the [[DTCC]] Learning site at https://dtcclearning.com/products-
and-services/mutual-fund-services/record-layouts.html 
 
• 018 is in Fund/SERV Record in fixed format is in part 2, record 019 is in part 3 
• 018 and 019 Fund/SERV records in variable format are in part 2 
 
• Passwords are required to access the Learning Center. 

---

## Page 21

USER GUIDE: ACATS-Fund/SERV 
Appendix A: Glossary of ACATS Terms 21 
APPENDIX A: GLOSSARY OF ACATS TERMS 
Deliverer 
The deliverer is an [[NSCC]] [[participant]] subscribing to ACATS. The deliverer has possession of the account and 
must deliver the assets to the receiver. The receiver must subscribe to ACATS-Fund/SERV to be part of the 
ACATS-Fund/SERV link. 
Non-Standard Transfer 
This is a partial transfer, residual credit, mutual fund cleanup, fail reversal, or reclaim. Review and Settle- Prep 
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

## Page 22

USER GUIDE: ACATS-Fund/SERV 
Appendix A: Glossary of ACATS Terms 22 
Standard Transfer 
This is a full transfer. Normally there is one day for Review status, one day for Settle-Prep status, and then the 
item settles one day later. This transfer could be accelerated so that Settle-Prep occurs the same day as the 
Review status. 
 

---

## Page 23

 
 
© 2024 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation [[DTCC]].  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
 
Doc Info: February 15, 2024 
Publication Code: MFS368 
Service: Fund/SERV
® 
Title: User Guide: ACATS-Fund/SERV 
For More Information 
 
Email Core Learning Service at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 