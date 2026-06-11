---
title: "MFPS I - Price and Rate User Guide/Best Practice"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps1_Price_and_Rate_mfs358_20240131.pdf"
pages: 17
size: "643.6 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# MFPS I - Price and Rate User Guide/Best Practice

**Original File:** [mfps1_Price_and_Rate_mfs358_20240131.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps1_Price_and_Rate_mfs358_20240131.pdf)  
**Category:** Other  
**Total Pages:** 17  
**File Size:** 643.6 KB  

---

## Page 1

 
 
 
Mutual Fund Profile Service I  
PRICE AND RATE USER GUIDE/BEST PRACTICE 
JANUARY 31, 2024 
 
 

---

## Page 2

CHANGE HISTORY 
Date Revisions 
January 31, 2024 Document Rebranded.  Content reviewed. 
May 10, 2022 Document links updated due to launch of new Learning Center. 
August 12, 2020 Document was rebranded.  Links corrected. 
 
 
 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Introduction .......................................................................................................................................................... 4 
Data Input/Output Methods ................................................................................................................................. 5 
Supported Methods............................................................................................................................................. 5 
MQ Considerations ............................................................................................................................................. 6 
Record Layouts .................................................................................................................................................... 8 
Service Activation ................................................................................................................................................ 9 
MFPS I Price & Rate Daily Volume Report ....................................................................................................... 10 
Best Practices ..................................................................................................................................................... 11 
Pricing..............................................................................................................................................................11 
Pricing Delays & Corrections ..........................................................................................................................11 
Frequency Asked Questions ............................................................................................................................. 13 
Appendix A: Firm Cut-Off Times ...................................................................................................................... 14 
 

---

## Page 4

Price and Rate User Guide/Best Practice 
Introduction 4 
INTRODUCTION 
Mutual Fund Profile Service I (MFPS I 1) Price and Rate service was developed and implemented in 1996 to 
provide Funds with an automated solution for providing intermediaries with prices in the form of net [[Asset]] values 
(NAVs) and distribution rates (for daily and periodic dividends and capital gains) 2. 
Prior to 2016, the service supported single NAV funds only where funds submitted their single daily NAVs via 
MFPS I. In 2016, [[NSCC]] implemented enhancements to Mutual Fund Services in connection with Money 
Market Reform (Important Notice a8159). The MFPS I Price and Rate service was enhanced to support the 
delivery of multiple daily NAVs for a money market fund that strikes multiple NAVs per day. The modifications 
were made in support of floating NAV money market funds that offer same-day cash availability at multiple 
times throughout the business day. For additional information on money market-related enhancements, please 
refer to “Money Market Fund Reform User Guide and Best Practices” document located in the Mutual Fund 
section of the Learning Center https://dtcclearning.com/products-and-services/mutual-fund-services/mfs-cross-
products/money-market-fund.html 
The Daily Price & Rate File provides: 
• NAV date and price* 
• NAV Strike Times (for multiple NAV funds) 
• Daily & periodic distribution ([[Dividend]] & capital gain) rates 
• Security Issue IDs (these may or may not be Fund/SERV®-eligible) 
• NAV and [[Dividend]] rate corrections with associated date 
• Day count (the number of days that applies to the rate for daily accrual funds)  
• Issued and proposed symbols 
• Cumulative rates 
• Distribution types 
• Distribution indicators 
*Note: 
Effective September 2016 (please see Important Notice a8159), MFPS I was enhanced to allow for the submission and 
correction of a price for a fund that strikes multiple intra-day NAVs.  
Funds have the ability to submit prices in: 
• USD = U.S. Dollars 
• GBP = British Pounds 
• EUR = Euros 
• JPY = Japanese Yen 
• SGD = Singapore Dollar 
• HKD = Hong Kong Dollar 
• AUD = Australian Dollar 
• CAD = Canadian Dollar 
• CHF = Swiss Franc 
• CNY = China Yuan Renminbi 
• NOK = Norwegian Krone 
• SEK = Swedish Krona 
 
1 MFPS I: Daily Price & Rate File is a service offering of National [[securities]] Clearing Corporation, a wholly -owned subsidiary of [[DTCC]]. 
2 [[Mutual Funds]] utilize Price and Rate File to pass NAVs and Rates to intermediaries. [[Dividend]] Distribution information (including Record Date, Ex-Date, Payable 
Date, Payout Rate Period Start and Payout Rate Period End Dates) is available on the MFPS II Distribution Declaration File.  

---

## Page 5

Price and Rate User Guide/Best Practice 
Data Input/Output Methods 5 
DATA INPUT/OUTPUT METHODS 
Supported Methods 
The Daily Price & Rate File is accessible via mainframe over [[DTCC]]’s SMART connection. To upload or download 
files, clients can use [[DTCC]] WebDirect, a Web interface that provides clients with direct access over the Internet 
to services provided by [[DTCC]]'s subsidiaries. Files can be sent and received interactively or as single or multiple-
batch transmissions. Both ISO/SWIFT and non-ISO messaging formats are supported. 
The Price and Rate File can be transmitted via the following transmission protocols:  
Input 
• SFTP (SSH) 
• FTPS (SSL) 
• NDM (Connect:Direct) 
• [[DTCC]] WebDirect (Utilities Function) 
• MQ Series 
Output  
• SFTP (SSH) 
• FTPS (SSL): Pull ONLY 
• NDM (Connect:Direct) 
• [[DTCC]] WebDirect (Utilities Function) 
• MQ Series 
 
Transmission Schedules are located at:  
https://dtcclearning.com/products-and-services/mutual-fund-services/schedules.html 
Record Layouts are located at:  
https://dtcclearning.com/products-and-services/mutual-fund-services/record-layouts.html 

---

## Page 6

Price and Rate User Guide/Best Practice 
Data Input/Output Methods 6 
MQ Considerations 
In 2015, the MFPS I Price and Rate file was enhanced to provide clients with the ability to submit and receive 
Price and Rate data via MQ messages (Important Notice a 8005). Prior to the implementation of MQ, batch file 
processing was the only supported method for all inbound and outbound Price and Rate data communications. 
To accommodate intermediaries’ need to receive Price and Rate data as early as possible, additional batch file 
processing cycles were added over the years with batches processing minutes apart with no window to expand 
beyond the 29 batch cycles. With the continued demand for intermediaries to receive Price and Rate data quicker 
and no room to expand beyond the 29 batch cycles, the most strategic and sustainable  solution was to provide 
clients with the ability to transmit and receive data through MQ messages. With the implementation of MQ, 
intermediaries will be able to receive prices faster than the batch file transmission schedule permits.  
In order to fully realize the processing capabilities of the MFPS I service and achieve the fastest processing of 
the Price and Rate data, it is recommended that both submitting funds and receiving firms utilize the MQ protocol. 
The MQ Inbound / MQ Outbound model is the ultimate solution to improve the processing time and bring 
efficiencies to the mutual fund industry. 
Client Benefits 
• Provides an opportunity for clients choosing to utilize MQ, to transmit and/or receive prices quicker than 
the batch cycle schedule permits. 
• Allows for faster delivery of price and rate data and eliminate lag time between fund submission and 
[[NSCC]] distribution of the price and rate data to firms. 
 
The following scenario illustrates the processing times for data distributed through MQ vs. Batch Files.  For the 
purposes of this illustration, we will assume the fund provided price data for cycle 09 and was received by 
[[DTCC]] at 5:01 pm ET. 
 
Inbound Data 
Transmission Protocol 
Input Received By [[NSCC]] Data Output Transmission 
Protocol 
Output Sent by [[NSCC]] 
MQ or Batch Files 5:01:05 pm ET MQ 5:01:15 pm ET 
MQ or Batch Files 5:01:05 pm ET Batch Files 5:35 pm ET 
 
Clients that opt to receive the data through MQ, would receive prices shortly after [[DTCC]] receives the prices. In 
the above scenario, fund transmitted price and/or rate information at 5:01pm ET which would not be sent until 
5:35pm ET (based on the transmission schedule for clients who subscribe to receive price and rate data via 
batch files). 
 
  

---

## Page 7

Price and Rate User Guide/Best Practice 
Data Input/Output Methods 7 
Price and Rate data flow 
 
 
MQ Cut-off Time 
All inbound Price and Rate MQ messages submitted to [[NSCC]] after 10:14pm ET will be processed and 
transmitted the next business day when the system begins data processing (at the start of Cycle 1). The 10:14pm 
ET cut-off timeframe corresponds to the existing cut-off time for batch cycle 98. Any MQ messages submitted 
after the 10:14pm ET cut-off time must contain the next business day in the “Submission Date” field. 
For additional information on the MFPS I processing hours, please refer to the Transmission Schedule located 
at: https://dtcclearning.com/products-and-services/mutual-fund-services/schedules.html 
Data Rejected by [[NSCC]] 
Inbound Price and Rate data that does not pass [[NSCC]] validation will be rejected back to the submitter via the 
submitter’s choice of the transmission protocol. Clients can elect to receive their rejected data by specifying their 
choice of the data transmission protocol. Clients who subscribe to receive Price and Rate rejected messages via 
MQ will receive all rejected data as soon as it is received and rejected by [[NSCC]]. Clients who subscribe to receive 
their Price and Rate rejected data through batch files will receive this data at the time specified by the 
Transmission Schedule 


---

## Page 8

Price and Rate User Guide/Best Practice 
Record Layouts 8 
RECORD LAYOUTS 
Price and Rate data submitted as a batch file can be sent in the following formats: 
Inbound 
• ISO Variable 
• ISO Fixed 
• Non-ISO Variable 
• Non-ISO Fixed 
Outbound 
• ISO Variable 
• ISO Fixed 
• Non-ISO Variable 
• Non-ISO Fixed 
 
Supported Formats for MQ* 
Inbound 
• ISO Variable 
• Non-ISO Variable 
Outbound 
• ISO Variable 
• Non-ISO Variable 
Note:   
*MQ transmission protocol (both Inbound and Outbound) supports only Variable formats 
 
MFPS I Price and Rate Record Layouts can be found at the following link: 
https://dtcclearning.com/products-and-services/mutual-fund-services/record-layouts.html 
  

---

## Page 9

Price and Rate User Guide/Best Practice 
Service Activation 9 
SERVICE ACTIVATION 
In order to send or receive MFPS I Price and Rate data, clients are required to sign up for activation. Existing 
clients wishing to utilize MQ capabilities will need to fill out the required paperwork and ensure that there is a 
circuit in place. For information on the sign-up process, please contact your Relationship Manager or Wealth 
Management Services at (212) 855- 8877. 

---

## Page 10

Price and Rate User Guide/Best Practice 
MFPS I Price & Rate Daily Volume Report 10 
MFPS I PRICE & RATE DAILY VOLUME REPORT 
The Price and Rate Daily Volume Report captures the following information for each transmission cycle:  
• Number of Clients sending price and rate data to [[NSCC]] in each cycle (includes MQ and Batch File 
inbound submissions). A client can send data in multiple cycles; therefore, a s ingle client may be counted 
more than once if they transmit in multiple cycles. 
• Number of Security Issue IDs received by [[NSCC]] in each cycle (includes MQ and Batch File inbound 
submissions). A Security Issue [[ID]] can be sent in multiple cycles; therefore, a Security Issue [[ID]] will be 
counted more than once if a revision is submitted. 
 
Statistics will be broken down as follows: 
• Daily Report showing activity for one day 
• Month-to-Date Report – will show accumulated activity for one month’s period 
 
This report is created daily with running month-to-date totals and is available for clients to view. Client level 
information is not disclosed. The report provides the mutual fund industry with information on when peak/low 
volumes occur for each Price & Rate cycle. 
Access to the MFPS I Price & Rate report: 
The MFPS I Price & Rate report is accessible to clients on SMART/Search through [[DTCC]]’s [[participant]] 
Browser Services ([[PBS]]). A [[PBS]] SMART/Search connection and user [[ID]]/password is required to access the 
MFPS I Price & Rate report. To obtain access to the report, clients should contact the Super Access 
Coordinator (SAC) at their firm and have them request access to [[Entitlement]] XMFP through their Wealth 
Management Services Relationship Manager. Once the [[Entitlement]] is enabled, the “MFPS I Price and Rate - 
Daily Volume Report” report link will appear under the Mutual Fund Reports section. Clients requiring 
access to the report and [[DO]] not have a SAC, or access to the SMART/Search [[PBS]] network, should contact 
their Wealth Management Services Relationship Manager for assistance. 

---

## Page 11

Price and Rate User Guide/Best Practice 
Best Practices 11 
BEST PRACTICES 
The best practices outlined here can involve several areas within the fund company and, therefore, it is 
recommended that each fund and firm review the best practices with their technology organization for 
successful implementation and adherence to industry best practices. 
These best practices resulted from a combined effort of the Investment Company Institute’s [[Broker]] Dealer 
Advisory Committee (BDAC) and Bank, Trust and Retirement Advisory Committee (BTRAC).  
Pricing 
• The MFPS I Price & Rate File should be the primary source for delivery of NAVs to firms. Although other 
feeds are also important as back-up sources, the MFPSI Price & Rate File provides a standard and 
centralized approach for funds and firms. 
• As firms and third-party vendors also rely on [[NASDAQ]] for NAVs, funds should continue to transmit NAVs 
as soon as possible into [[NASDAQ]], preferably by 6:05 pm ET. However, funds should also send confirmed 
NAVs by the final session (8:00 pm ET). Vendors that rely on [[NASDAQ]] will be making adjustments to pull 
final NAVs up to and including the last session. 
• Funds should identify the critical cut-off times of their service provider and of [[DTCC]], to be in a better 
position to establish internal cut-off times to meet the firms’ cut-offs for receiving NAV and rates. The cut-
off times for a number of BDAC and BTRAC firms can be found in Appendix A and should only be used as 
a baseline for determining appropriate price/rate communications. 
• Firms should utilize DST Vision, BNY Mellon Advisor Central and SunGard Funds AUM Portal and/or a 
source designated by their fund partners as an [[Option]] for viewing prices in the event they need to meet 
internal system cut-offs and have not received NAVs through the MFPS I Price & Rate File.  
• If NAVs or daily distribution rates are sent out in the final MFPSI Price & Rate cycle (10:29 p.m. ET),  funds 
should be aware that NAVs received by [[DTCC]] prior to 10:14 p.m. ET will automatically be processed in 
the final cycle. If, however, the NAVs are received after 10:14 p.m. ET, but before 10:29 p.m., funds are 
encouraged to contact [[DTCC]] to verify that there was sufficient time to process and include i n the final 
cycle.  Data submitted via MQ after 10:14pm ET must have the next business day populated in the 
“Submission Date” field and will be processed the next business day at the start of Cycle 1.  
• Funds should be aware of firms’ nightly cycle start times so that it is clear when NAVs/rates need to be 
delivered to avoid adverse impacts and corrective processing. The matrix in the "ICI BDAC/BTRAC Firm 
Cut-off for NAVs and Rates" provides NAV and distribution rate cut-offs for responding firms (please see 
Appendix A) 
• For details and best practices related to the submission of multiple daily NAVs, please refer to the “Money 
Market Fund Reform User Guide and Best Practices” guide. 
 
Pricing Delays & Corrections 
• When funds are experiencing delays in pricing NAVs for certain funds, NAVs should be released for 
Security Issue IDs where the calculations are final. 
• If a fund is experiencing NAV delivery delays, the fund should provide an email/fax notific ation to firms 
regarding the delays. Other options should also be considered as back-up including keeping service 
center resources available until NAVs are released and providing key contact information to firms.  
• In the event the fund has price revisions, these revisions should be transmitted in the next available 
MFPSI Price & Rate cycle or as soon as they become available for clients utilizing MQ.  

---

## Page 12

Price and Rate User Guide/Best Practice 
Best Practices 12 
• In the event price revisions are missed in the final cycle through MFPSI Price & Rate funds should inform 
firms and send revisions via MFPSI Price/Rate as soon as the corrected price is available, preferably by 
input cut-off 5:45am ET Cycle 1 the next day or 4:00am ET for those funds that utilize MQ.  
• The MFPSI Price & Rate File should be the primary source for delivering NAV corrections to firms. Other 
feeds are also important as back-up. 
 

---

## Page 13

Price and Rate User Guide/Best Practice 
Frequency Asked Questions 13 
FREQUENCY ASKED QUESTIONS 
1. How will price corrections be reflected for batch clients when multiple corrections are 
submitted for the same Security Issue [[ID]] in different cycles? 
For Multi-Batch clients, the price corrections will only be displayed in the applicable cycle. For single 
batch customers the final price correction will be displayed in the price file (cycle 98).  
2. How will price corrections be reflected for batch clients when multiple corrections are 
submitted for the same Security Issue [[ID]] within the same cycle (with the exception of 
cycle 98 – the final cycle)? 
For Multi-Batch clients, only the final price submitted within a cycle will be displayed. For 
single batch customers the final price correction will be displayed in the price file (cycle 98). 
3. How will price corrections be handled for MQ data recipients? 
Clients subscribing to receive Price and Rate data via MQ will receive data shortly after it is 
submitted to [[NSCC]]. If multiple prices/corrections are submitted – MQ recipients will receive 
all data (multiple prices and correction) via MQ messages. 
4. How will price corrections be reflected for batch clients when multiple corrections are 
submitted for the same Security Issue [[ID]] within the cycle 98 (the final cycle)? 
For Multi-Batch and single batch clients, only the final price correction will be displayed. 
5.  Will the 98 cycle (the final cycle) of the multi-batch contain everything that has been 
submitted? 
No, cycle 98 of the multi-batch file will only contain prices and rates submitted in that file. 
6. Will the 98 cycle of the single batch contain everything that has been submitted? 
The 98 cycle will contain all original prices and rates and final corrections submitted 
throughout the day. 
7. Will clients receive both multi-batch and single batch files if they are set-up to receive 
both? 
Yes, clients who are set-up to receive single and multi-batch files will receive both. 
8. What are ISO and SWIFT? 
The International Organization for Standardization (ISO) is a worldwide federation of national 
standards bodies based in Geneva, Switzerland. The organization’s objective is to promote 
the development of international or worldwide standards in all important fields of business. 
These standards are developed by technical committees composed of experts in each field 
who are nominated by the respective branches of industry. Within the United States the 
organization that administers the development of ISO message formats is The Society for 
Worldwide Interbank Financial Telecommunications (S.W.I.F.T). In order to ensure 
compatibility of the multitude of practices, conventions, and habits of S.W.I.F.T. users, all 
messages transmitted via the S.W.I.F.T. network must adhere to these message text 
standards. 
  

---

## Page 14

Price and Rate User Guide/Best Practice 
Appendix A: Firm Cut-Off Times 14 
APPENDIX A: FIRM CUT-OFF TIMES 
Firm Platform Name 
What is the optimal 
time for this platform 
to receive price and 
rate data? 
What is the absolute latest time for 
this platform to receive price and 
rate data? 
What time [[DO]] you start running 
your jobs for this platform? 
Does your firm wait for 
MFP cycle 98 to process 
daily fund distribution 
rates? If not, what is your 
required deadline for 
receiving this 
information? 
For periodic distributions, 
what is your required 
deadline? 
Firm 1  Prior to 8pm ET 
9pm ET for service provider to 
provide files from which we confirm 
trades 
Trade confirm jobs - 8:30 ET, 
Security Master Pricing - 9:30 ET 
Our service provider does 
wait for cycle 98. 
Our service provider does 
wait for cycle 98. 
Firm 2  
As soon as available 
- by 6:45 pm ET if 
possible 
Will take it through Cycle 98 pm but 
have contractual fund of fund pricing 
deadlines to clients of between 8 and 
9 pm ET 
NAV publish job for fund of funds 
which contain [[Mutual Funds]] starts 
at 6:50 pm ET. Continues running 
through evening. Decision about 
using stale prices occurs after 8 
pm ET. 
[[DO]] not wait for 98. 
Deadline is same timeline 
as prices. Decision to go 
without rate is made after 9 
pm ET. 
Currently use an external 
vendor - need data as soon 
as possible on ex-date - 
picked up in same 6:50 pm 
NAV for fund of funds jobs. If 
not available, system waits 
and retries every 15 minutes. 
Decision to go without rate is 
made after 9 pm. 
 
Firm 3  Cycle 98 current time or 
prior Cycle 98 current time or prior After cycle 98 N/A - Sub-Accounting 
provider does this 
N/A - Sub-Accounting 
provider does this 
Firm 4 
Advisory By 7:15 PM ET 7:50 PM ET 8:10 PM ET No, 9PM ET cycle 24 9PM ET cycle 24 
Brokerage By 7:45 PM ET 7:30 PM ET 4:00 PM ET No, 9PM ET cycle 24 9PM ET cycle 24 
Firm 5  6:30 PM   6:30 PM 6:30 PM 
Firm 6  
The earlier the better. 
We pull in multiple files 
each evening starting 
with cycle 17. 
9:15pm ET/cycle 24 We start loading price files around 
7:15pm ET. 
No. We need files by 
9:15pm ET/cycle 24 
We pass these files along as 
they are received. 
Firm 7 
Proprietary 
pricing/[[Dividend]] 
system 
 
7:30 PM ET  
We have a range of deadlines 
depending on current day's batch 
processing volumes. Generally, if 
prices are going to be delayed 
beyond 9:30 PM ET we have to 
 
6:30 PM ET 
We normally receive all 
daily rate data by cycle 20 
which is generally received 
by 7:45 PM ET. Cycle 98 
would only be used in the 
6:30 PM ET is our deadline 
assuming most of the 
periodic distributions have 
been received prior to 6:30 
PM ET and only a few remain 

---

## Page 15

Price and Rate User Guide/Best Practice 
Appendix A: Firm Cut-Off Times 15 
Firm Platform Name 
What is the optimal 
time for this platform 
to receive price and 
rate data? 
What is the absolute latest time for 
this platform to receive price and 
rate data? 
What time [[DO]] you start running 
your jobs for this platform? 
Does your firm wait for 
MFP cycle 98 to process 
daily fund distribution 
rates? If not, what is your 
required deadline for 
receiving this 
information? 
For periodic distributions, 
what is your required 
deadline? 
engage senior management and 
analyze the impact to the end-to-end 
trade cycle which is dependent on the 
completion of batch processing. 
 
 
event of industry wide 
delays which is also 
delaying price files from 
being transmitted. 
to be received by this time. 
Getting this information 
earlier is preferred. 
Fund 
accounting/ 
unitization 
system 
 
 
7:45 PM ET 
We have a range of deadlines 
depending on current day's batch 
processing volumes. Generally, if 
prices are going to be delayed 
beyond 9:00 PM ET we have to 
engage senior management and 
analyze the impact to complete trade 
cycle which is dependent on the 
completion of batch processing. 
Batch processing won't commence 
until unitization process has 
completed. Unitization process 
requires additional time which can't 
start until all prices have been 
received. 
8:00 PM ET 
We normally receive all 
daily rate data by cycle 20 
which is generally received 
by 7:45 PM ET. Cycle 98 
would only be used in the 
event of industry wide 
delays which is also 
delaying price files from 
being transmitted. 
7:45 PM ET is our deadline 
assuming most of the 
periodic distributions have 
been received prior to 7:45 
PM ET and only a few remain 
to be received by this time. 
Getting this information 
earlier is preferred. 
 
Proprietary 
record keeping 
system 
8:30 PM ET 
We have a range of deadlines 
depending on current day's batch 
processing volumes. Generally, if 
prices are going to be delayed 
beyond 9:30 PM ET we have to 
engage senior management and 
analyze impact to the end-to-end 
trade cycle which is dependent on the 
completion of batch processing. 
8:30 PM ET 8:30 PM ET 8:30 PM ET 
Firm 8 
 
Platform 1 - 
Dividends 
 
6 pm - 8 pm ET 
 
Cycle 98 - as needed 
Critical Path: 
8 pm ET non-month end 9 - 9:30 
pm ET month end 
Cycle 20 low volume days 
Cycle 24 month-end or 
delay as needed 
Cycle 20 low volume days 
Cycle 24 month-end or 
delay as needed 
Platform 2 - 
Trading 
Execution 
6 pm - 7 pm ET Cycle 98 - as needed 8:40 PM ET Daily   

---

## Page 16

Price and Rate User Guide/Best Practice 
Appendix A: Firm Cut-Off Times 16 
Firm Platform Name 
What is the optimal 
time for this platform 
to receive price and 
rate data? 
What is the absolute latest time for 
this platform to receive price and 
rate data? 
What time [[DO]] you start running 
your jobs for this platform? 
Does your firm wait for 
MFP cycle 98 to process 
daily fund distribution 
rates? If not, what is your 
required deadline for 
receiving this 
information? 
For periodic distributions, 
what is your required 
deadline? 
Firm 9 7:00 p.m. ET 9:00 p.m. ET 9:00 p.m. ET 
The firm does not currently wait 
for cycle 98, but in unique 
scenarios the firm will pause the 
queue. 
3:00 p.m. ET  
Firm 10 Brokerage 
Platform 9:00 ET 9:30 ET 9:10 ET No, none N/A 

---

## Page 17

 
 
© 2024 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation [[DTCC]].  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: January 31, 2024 
Publication Code: MFS358 
Service: Mutual Fund Profile Service I 
Title: Price and Rate User Guide/Best Practice 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 
 
 