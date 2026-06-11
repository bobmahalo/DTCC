---
title: "Omni/SERV - 529 Account Aggregation Best Practices"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/529_aggregation_best_practices_mfs306_20230802.pdf"
pages: 15
size: "528.8 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Omni/SERV - 529 Account Aggregation Best Practices

**Original File:** [529_aggregation_best_practices_mfs306_20230802.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/529_aggregation_best_practices_mfs306_20230802.pdf)  
**Category:** Other  
**Total Pages:** 15  
**File Size:** 528.8 KB  

---

## Page 1

 
 
Omni/SERV® 
 
 
529 AGGREGATION BEST PRACTICES 
 
AUGUST 3, 2023 
 
 

---

## Page 2

529 AGGREGATION BEST PRACTICES 
Overview 2 
REVISION HISTORY 
 
Date of 
Changes 
Important 
Notice # 
Reason for change 
08/3/2023  Document rebranded. Content reviewed. 
08/15/2022  Additional link included in File submission deadlines section.  Content reviewed. 
06/27/2018  Document rebranded.   
529 Aggregation Working Group executed review – adopted changes have been incorporated. 
 

---

## Page 3

529 AGGREGATION BEST PRACTICES 
Overview 3 
TABLE OF CONTENTS 
Overview ............................................................................................................................................................... 5 
Plan Limitations ................................................................................................................................................... 5 
Maximum Contribution Amount Is Based on The Beneficiary........................................................................... 5 
Distribution Reporting Occurs at The Owner/Beneficiary Level ........................................................................ 5 
Investment Election Changes Determination Occurs at The Owner/Beneficiary Level  .................................... 5 
Links To 529 Aggregation File Layouts and Social Code List........................................................................... 6 
Inbound Files from [[intermediary]]/Firm .................................................................................................................. 6 
Following are common inquiries regarding the submission of files: .................................................................. 6 
Will submitting intermediaries need to create separate files for each recipient?  ............................................ 6 
What happens if files are sent after transmission deadlines? ......................................................................... 6 
Multiple accounts for the same owner/beneficiary exist at [[intermediary]].  Should ‘inbound’ sub- account data 
submitted be aggregated? ............................................................................................................................... 7 
Outbound File from Aggregator .......................................................................................................................... 7 
Following Are 529 Activity Scenarios and The Associated Best Practice: ........................................................ 7 
New contribution occurs - Limitation is not met or exceeded .......................................................................... 7 
New Contribution Determines Limitation Restrictions Are Violated................................................................. 7 
New Contributions Are Reported by Multiple Intermediaries on The Same Day -  Limitation Restrictions Are 
Violated ............................................................................................................................................................ 8 
No Contributions Are Reported for A Day; But Threshold Limitations Are Violated  ........................................ 8 
Distribution Activity .......................................................................................................................................... 8 
Investment Election Rebalances ..................................................................................................................... 8 
Investment Election Rebalancing Processing Procedures .............................................................................. 9 
Surviving  Principal  Processing Procedures ..................................................................................................... 9 
Firms/Intermediaries (Aggregation Detail B/F11 records): ............................................................................ 9 
Aggregators (Aggregated Detail G12 records): ............................................................................................. 9 
Examples of Surviving Principal ..................................................................................................................... 9 
Transaction Reversal Processing .....................................................................................................................10 
Intermediaries  .................................................................................................................................................10 
Investment Rebalance....................................................................................................................................11 
Aggregators ...................................................................................................................................................11 

---

## Page 4

529 AGGREGATION BEST PRACTICES 
Overview 4 
Workflow ............................................................................................................................................................. 12 
Frequently Asked Questions .............................................................................................................................. 13 
What data elements in the Record Layouts does [[NSCC]] edit? ......................................................................13 
Does the Response file that Aggregator sends disclose another [[intermediary]]’s account information? .........13 
[[DO]] Aggregators indicate the number of other positions held at other firms if matches occur? .....................13 
How does an Aggregator report back multiple accounts held at one [[intermediary]]? ......................................13 
What are the coding standards for LTD Contributions and Withdrawal  ONLY Fields on inbound 529 
Aggregation Account Level Detail Records if either value is zero? ..............................................................13 
Is there a possibility of not identifying a limit restriction on day 1? ................................................................13 
[[DO]] the Response files from Aggregator include data received from sources outside of [[NSCC]]? .................13 
File submission deadlines ............................................................................................................................13 
Links to Transmission Schedules, 529 Aggregation File Layouts and Social Codes  ..................................14 

---

## Page 5

529 AGGREGATION BEST PRACTICES 
Overview 5 
OVERVIEW 
A 529 plan is a tax-advantaged savings plan designed to encourage saving for future college costs, and in 
certain states, K-12 tuition. 529 plans, legally known as “qualified tuition plans,” are sponsored by states, state 
agencies, or educational [[Institutions]] and are authorized by Section 529 of the Internal Revenue Code. 
Investment options often include [[Stock]] [[Mutual Funds]], bond [[Mutual Funds]], and money market funds, as well as, 
age-based portfolios that automatically shift toward more conservative investmen ts as the beneficiary gets 
closer to college age. 
Plan Limitations 
Specific limitations on 529 plans require the monitoring of contributions, distributions, and investment election 
changes. This section outlines some specific rules relating to these requirements.  
Maximum Contribution Amount Is Based on The Beneficiary 
It is only permissible to make contributions on behalf of a beneficiary until the total of all state programs 
combined have reached the maximum allowed. Maximum amounts vary from state t o state. 
The link below provides current state-to-state limitation level restrictions: 
http://www.savingforcollege.com/ 
Distribution Reporting Occurs at The Owner/Beneficiary Level 
The 529 program rules require aggregation of all accounts with same account owner/beneficiary within a given 
529 plan for the purposes of calculating basis and earnings of a distribution. 
Investment Election Changes Determination Occurs at The Owner/Beneficiary 
Level 
The number of investment strategy changes allowed during one calendar year is set by the IRS.  This 
restriction is in place for the collective total of all accounts held within offered state plans. There may be 
investment changes to multiple accounts with the same owner/beneficiary participating in a plan on the same 
day. In such instances, these changes will be counted as a single strategy change event. Once the strategy 
change limit has been reached, administrators should systematically prevent any other strategy changes from 
taking place for the rest of the calendar year.  
Calculation of limitations includes collective totals of all state plans (per beneficiary or owner/beneficiary). 
Limitations are regardless of who holds a 529 position for a client (plan manager, firm, fund, etc.)

---

## Page 6

Links To 529 Aggregation File Layouts and Social Code List 
 
1. The 529 Aggregation Record Layouts are available within [[DTCC]]’s Learning Center under the Omni/SERV 
Record Layouts section of Mutual Fund Services. 
2. The Social Code list is available in the [[DTCC]] Learning Center at: 
https://dtcclearning.com/documents/mutual-fund-services/cross-product-documentation-infomation/2498-
social-codes/file.html 
 
Additional 529 Account documentation as well as information about othe r products is available on the 
[[DTCC]] Learning Center.  You will need a username and password to access the L earning Center.  If you [[DO]] 
not have these credentials, you may register by visiting the Learning Center and selecting ‘Login or 
register’ : https://www.dtcclearning.com/products-and-services/mutual-fund-services.html 
 
Inbound Files from [[intermediary]]/Firm 
529 Aggregation account-level detail files: Intermediaries (Firms) send files with 529 account information to 
[[NSCC]] each day after completion of nightly processing.    
 
Following are common inquiries regarding the submission of files: 
 
Will submitting intermediaries need to create separate files for each recipient? 
No. Intermediaries follow standard protocol by submitting one file. If an [[intermediary]] has to distribute the file to 
more than one recipient, the [[intermediary]] creates a separate header/trailer record for each recipient. 
What happens if files are sent after transmission deadlines? 
• All files (Aggregation Detail and Aggregated) that firms and aggregators send to [[NSCC]] after the last 
transmission deadline must be received the same day by 4pm ET for processing the next business day.   
Files received after 4pm ET will reject unless the Datatrak file header contains the next business day’s 
date, in which case accepted files will be processed during the first cycle of the next business day.  
• If inbound 529 Aggregation Account Level detail files are received after the last transmission deadline and 
held at [[NSCC]], Aggregators will receive the files on the following business day.  This data will be treated 
as as-of activity the day received. In such cases, [[NSCC]] returns multiple outbound 529 Aggregator 
Response files (current and prior business day) to intermediaries, separated by date.  
 
Please reference the Networking & Omni/SERV Transmission Schedules on the Learning Center  for details on 
529 Aggregation file cycles: https://www.dtcclearning.com/documents/mutual-fund-services/mfs-
schedules/1812-networking-omni-serv-transmissions-schedules/file.html 
 
Additionally, a Holiday Schedule announcing changes to [[NSCC]]’s operations and schedules is published 
annually.  This schedule is helpful to determine file availability due to holiday changes.  Holiday Schedules are 
available at: https://www.[[DTCC]].com/wealth-management-services/mutual-fund-services/mutual-funds-client-
public-documentation

---

## Page 7

Multiple accounts for the same owner/beneficiary exist at [[intermediary]].  Should ‘inbound’ 
sub-account data submitted be aggregated?  
Data should be sorted by activity date, by account, at the owner/beneficiary level.  If there are multiple 
accounts for the same owner/beneficiary, there is the [[Option]] to send two separate records. 
Outbound File from Aggregator 
529 Aggregated Detail Response files - Intermediaries calculate the basis/earnings breakdown on distributions 
and therefore, need the market value and net basis reported every day.  Aggregators send files to all 
Intermediaries daily through [[NSCC]] before the final transmission cutoff. (See Networking and Omni/SERV 
Transmission Schedule for transmission times.)  [[NSCC]] transmits these files daily to the Intermediaries 
assigned in the header records. 
Aggregators submit files as follows: 
• If multiple 529 accounts exist for a beneficiary, Aggregators send relevant data to all affected parties.  
• If no matches occur, Aggregators return header/trailer records as a response. 
• It is possible that Aggregators have to set up files containing both matched beneficiary data and 
empty header/trailer records.   All 529 account information sent to Aggregators is to be 
acknowledged with a response.   
 
LTD “Net” Contribution Field 
• Firms supply the netted grand total basis of all the activity made to an account since its inception to 
the end of the prior business day to the Aggr egator. 
• Aggregators return the netted grand total basis, including the values received from all parties where 
both owner and beneficiary match.  
 
Following Are 529 Activity Scenarios and The Associated Best Practice: 
New contribution occurs - Limitation is not met or exceeded 
Example: Firms A, B, and C all send daily files to the Aggregator on all 529 accounts on their platforms. They 
send these files regardless of whether there was any activity on the accounts. When there was no activity on an 
account, the only difference from the prior day’s file is the market value and the market value date. In this scenario, 
Firm B includes a contribution for $100,000.00; however, this does not meet or exceed limitation. The 
Aggregator's system does not trigger any violation. 
• The Aggrega tor sends files containing required data specified in the G12 record layouts to all 
affected Intermediaries.  
 
New Contribution Determines Limitation Restrictions Are Violated 
Example: Firms A, B, and C all send daily files to Aggregator on all 529 accounts on their platforms. They send 
these files regardless of whether there was any activity on the accounts. When there was no activity on an 
account, the only difference from the prior day’s file is the market value and the market value date. In this scenario, 
Firm B includes a contribution for $100,000.00 that meets/exceeds limitation.  The Aggregator's system 
recognizes and triggers a maximum contribution threshold violation. 

---

## Page 8

529 AGGREGATION BEST PRACTICES 
Overview 8 
• Aggregator sends files containing required data specified (including Plan Cap Met or Exceeded Limit 
Reached field on the G12)   record layouts to all three affected Intermediaries. 
New Contributions Are Reported by Multiple Intermediaries on The Same Day - Limitation 
Restrictions Are Violated 
Example: Firms A, B, C and D all send daily files to the Aggregator on all 529 accounts held on their 
platforms.  Firms A, B and D report contributions.  The combination of these three purchases pushes the 
contribution limitation over the allowed amount.  The Aggregator’s system recognizes the threshold violation.  
 
If this scenario occurs, the following best practices should be executed:  
 
• Aggregator sends files containing required data specified (including Plan Cap Met or Exceeded Limit 
Reached field on G12) in the record layouts to all affected Intermediaries. 
• Aggregators should communicate additional details to intermediaries outside of [[NSCC]] to facilitate 
resolution among the parties.  This can be done by either contacting firms directly or sending 
supplemental reporting agreed to between the parties. 
 
No Contributions Are Reported for A Day; But Threshold Limitations Are Violated 
Example: Firms A, B and C send daily files for all their 529 accounts to the Aggregator.  No activity is 
reported by any firm; however, the Aggregator’s system recognizes a threshold violation for the same 
beneficiary held at all three firms.  
• Aggregator will communicate this occurrence by populating the Plan Cap Met or Exceeded Limit 
Reached field on G12 records to all parties.  This practice will continue until the value of the combined 
accounts drops below the contribution violation threshold.  If this occurs, the Aggregator will stop 
communicating the threshold limitation has been breached. 
 
Note:  
Other than the daily file exchange, there is no other reporting or actions to be taken when account(s) have exceeded the 
contribution threshold due to a change in market value only. 
Distribution Activity 
Example: Firms A, B, C send files. Firm B’s file has recorded distr ibution activity.   
• Aggregator sends files containing required data specified in the record layouts to all three affected 
Intermediaries. 
Investment Election Rebalances 
Example: Firms A, B, and C send files. Firm C has new election balance indicator/activity. Firms should not send 
systematic activity (SWP, Age Based Roll, etc. ) to Aggregator. This type of activity is not considered an election 
rebalance. 
• Aggregator sends files containing the required data specified in the record layouts to all Intermediaries.  
This data includes the new election balance count.
 

---

## Page 9

529 AGGREGATION BEST PRACTICES 
Overview 9 
Investment Election Rebalancing Processing Procedures 
Rebalance occurs 
 
• If an i nvestment election rebalance occurs, enter the date of the rebalance in the Investment Election 
Rebalance Date field on the 529 Aggregation file.  
• Aggregators retain the count of occurrences for the calendar year. Aggregators relay updated information 
through the YTD Investment Election Rebalance Counter field on the 529 Aggregators Response file.  
 
Surviving Principal Processing Procedures 
Surviving Principal can occur when a fully redeemed account is part of an aggregation group. The surviving 
accounts most likely require an adjustment (positive or negative) to their principal. The following best practices 
should be followed when communicating surviving principle through the [[NSCC]] 529 Aggregation records:  
Firms/Intermediaries (Aggregation Detail B/F11 records): 
• Populate the surviving amount in the Surviving Principal field.  
• Communicate the disposition of surviving principal (debits or credits from surviving accounts) by entering 
'1' (debit) or '2' (credit) in the Surviving Principal Debit/Credit Indicator field. 
 
Aggregators (Aggregated Detail G12 records):   
• Calculate and report the debit or credit amount for each surviving account and populate that amount in the 
Surviving Principal field.   
• Communicate the disposition of surviving principal (debit or credited from surviving accounts) by entering 
'1' (debit) or '2' (credit) in the Surviving Principal Debit/Credit Indicator field. 
 
Examples of Surviving Principal 
The following provides an example of a redemption of $625.00 with Firm One and the respective fields that 
would be populated on the 529 Aggregation Records. 
 
Redemption 
Start  Close Position at Firm One 
 
Finish 
  Firm One Firm Two Totals  
 
 
 
 
 
P/E = $625 * ($1000/$1175) = $531.91 
 
  Firm One Firm Two Totals 
Value $625.00 $550.00 $1,175.00   Before Trade After 
 
Value $0.00 $550.00 $550.00 
Principal $500.00 $500.00 $1,000.00 Value $625.00 $625.00 0 
 
Principal -$31.91 $500.00 $468.09 
Earnings $125.00 $50.00 $175.00 Principal $500.00 $531.91 -31.91 
 
Earnings $31.91 $50.00 $81.91 
    
Earnings $125.00 $93.09 31.91 
     

---

## Page 10

Population of 529 Aggregation Records for a Redemption on Trade Date (T) and Trade Date +1 (T+1) 
T 
 529 Aggregation Record Field Name B11 - Firm One B11 – Firm  
Two 
G12 – Firm  
One 
G12 - Firm Two 
Firm’s Pre-Transaction Market Value $625.00 $550.00 $1,175.00 $1,175.00 
Market Value $0.00 $550.00 $550.00 $550.00 
LTD 'NET' Contributions Amount $0.00 $500.00 $468.09 $468.09 
Current Distribution (Redemption) Amount  $625.00       
Surviving Principal $31.91   
 
$31.91 
Surviving Principal Debit/Credit Indicator 2 = Credit   
 
2 = Credit 
 
T+1 
  529 Aggregation Record Field Name B11 - Firm One B11 - Firm  
Two 
G12 - Firm One G12 - Firm Two 
Firm’s Pre-Transaction Market Value - $550.00 - $550.00 
Market Value - $550.00 - $550.00 
LTD 'NET' Contributions Amount - $468.09 - $468.09 
Current Distribution (Redemption) Amount  -   -   
Surviving Principal -   -   
Surviving Principal Debit/Credit Indicator -   -   
Transaction Reversal Processing 
Intermediaries 
Contributions & Distributions 
The reversal of contributions or distributions will be indicated on the 529 Aggregation Account Level Detail 
(B/F11) records by either increases in Market Value and LTD ‘Net’ Contributions if the canceled transaction 
was a distribution, or by decreases in Market Value and LTD ‘Net’ Contributions if the canceled transaction was 
a contribution. The Transaction Reversal Indicator field is no longer utilized and should not be leveraged. 
Investment Rebalances 
The reversal of an Investment Rebalance event will be indicated on the 529 Aggregation Account Level Detail 
(B/F11) records by no longer providing the Investment Election Rebalance Date on which the Investment 
Rebalance event occurred. The Transaction Reversal Indicator field is no longer utilized and should not be 
leveraged. 

---

## Page 11

529 AGGREGATION BEST PRACTICES 
Overview 11 
Investment Rebalance 
Complete the following two required fields on the 529 Aggregation file (in addition to populating other fields in 
the file) in the event of an investment election rebalance reversal: 
1. Enter a value of ‘1’ in the Investment Election Rebalance Reversal Indicator field. 
2. Enter the original date of the rebalance in the Investment Election Rebalance Reversal field. 
Aggregators 
Investment Rebalances 
When an Aggregator stops receiving the date of an Investment Rebalance event in the Investment Election 
Rebalance Date fields of the 529 Aggregation Account Level Detail (B/F11) records, the Aggregator will 
consider this transaction reversed (assuming no other entities supply the same date on an incoming 529 
Aggregation Account Level Detail records) and will reduce the YTD Investment Election Rebalance Counter 
being sent on 529 Aggregated Detail (G12) records back to intermediaries.  
 
  

---

## Page 12

529 AGGREGATION BEST PRACTICES 
Workflow 12 
WORKFLOW 
 
 
 
Firms 
 
 
 
 
[[DTCC]] 
 
 
 
 
Aggregators 
 
 
 
 


---

## Page 13

529 AGGREGATION BEST PRACTICES 
Frequently Asked Questions 13 
FREQUENTLY ASKED QUESTIONS 
What data elements in the Record Layouts does [[NSCC]] edit? 
[[NSCC]] generally edits the following data elements before transmitting files:  
1. All the elements on the header/trailers 
2. The first two fields (System Code and Record Type) on the B/F11 and G12 records 
 
Does the Response file that Aggregator sends disclose another [[intermediary]]’s account information? 
Aggregator files [[DO]] not contain the account numbers of other Intermediaries when transmitting matched data. 
The files only disclose the receiving [[intermediary]]’s account number. 
 
[[DO]] Aggregators indicate the number of other positions held at other firms if matches occur? 
No. The system only reports aggregated totals to Intermediaries. 
 
How does an Aggregator report back multiple accounts held at one [[intermediary]]? 
Example: Firm A holds two accounts for the same beneficiary. Firm B holds a third account for same 
beneficiary. 
Question: [[DO]] the Response files report both account numbers for Firm A? 
Answer: If Firm A sent two account records separately, Aggregator sends back separated records. 
 
What are the coding standards for LTD Contributions and Withdrawal ONLY Fields on inbound 529 
Aggregation Account Level Detail Records if either value is zero? 
Participants who [[DO]] not provide LTD “NET” Contributions must provide the LTD Contributions ONLY amount 
and LTD Withdrawal ONLY amount fields. If only one of these fields has a data value, populate the other one 
with zero. 
 
Is there a possibility of not identifying a limit restriction on day 1? 
There is a possibility of exceeding the contribution limitation for a new beneficiary with a new contribution. The 
firm would not have any information from the Aggregator upon entry of the contribution. As a result, the Firm 
could process the contribution on day 1 and then receive data from the Aggregator on day 2. The Firm would 
process the contribution before determining that the beneficiary had exceeded the contribution limit.  
 
[[DO]] the Response files from Aggregator include data received from sources outside of [[NSCC]]? 
Aggregator files combines all 529 account information that it receives. Files that Aggregator returns to 
Intermediaries contain data from all 529 participants, whether [[NSCC]] or other non-[[NSCC]] transmission files 
delivered the information. 
 
File submission deadlines 
All files (Aggregation Detail and Aggregated) that firms and aggregators send to [[NSCC]] after the last 
transmission deadline must be received the same day by 4pm ET for processing the next business day .   
Files received after 4pm ET will reject unless the Datatrak file header contains the next business day’s date, in 
which case accepted files will be processed during the first cycle of the next business day. 
Please reference What happens if files are sent after transmission deadlines
 (in this document) for further 
details. 

---

## Page 14

529 AGGREGATION BEST PRACTICES 
Frequently Asked Questions 14 
Links to Transmission Schedules, 529 Aggregation File Layouts and Social Codes  
• 529 Aggregation file transmission cycles are available on the Learning Center site at: 
https://dtcclearning.com/products-and-services/mutual-fund-services.html#resources 
• Networking and Omni/SERV Transmission Schedules for transmission times: 
https://dtcclearning.com/documents/mutual-fund-services-1/networking/schedules-1/1812-networking-
omni-serv-transmissions-schedules/file.html 
• Holiday schedules announcing changes to [[NSCC]] operations hours are available on [[DTCC]].com at: 
https://www.[[DTCC]].com/wealth-management-services/mutual-fund-services/mutual-funds-client-public-
documentation 
• 529 Aggregation file layouts 
These files are available at on the Learning site under Omni/SERV/Record Layouts. 
https://www.dtcclearning.com/documents/mutual-fund-services/networking-1/529-processing/1664-
networking-omni-serv-sm-529-aggregation-file-record-layouts/file.html 
• Social Codes 
The Social Code list is available in the [[DTCC]] Learning Center at: 
https://dtcclearning.com/documents/mutual-fund-services/cross-product-documentation-
infomation/2498-social-codes/file.html 
 

---

## Page 15

© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The D epository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Pl ease see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
Doc Date: August 3, 2023  
Publication Code: MFS306 
Service: Omni/SERV® 
Title: 529 Aggregation Best Practices  
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 