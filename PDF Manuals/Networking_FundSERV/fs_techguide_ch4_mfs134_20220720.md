---
title: "Fund/SERV Technical Manual - Chapter 4: Communicating with Fund/SERV"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_techguide_ch4_mfs134_20220720.pdf"
pages: 14
size: "338.6 KB"
category: "Networking_FundSERV"
ingested_on: "2026-06-05"
---

# Fund/SERV Technical Manual - Chapter 4: Communicating with Fund/SERV

**Original File:** [fs_techguide_ch4_mfs134_20220720.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_techguide_ch4_mfs134_20220720.pdf)  
**Category:** Networking_FundSERV  
**Total Pages:** 14  
**File Size:** 338.6 KB  

---

## Page 1

 
 
 
FUND/SERV ® 
TECHNICAL MANUAL - CHAPTER 4: COMMUNICATING WITH FUND/SERV 
JULY 20, 2022 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by  certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in wh ich such entity operates. Please see 
www.[[DTCC]].com  for more information on [[DTCC]], its affiliates and the services they offer.  
 
 
Doc Date: July 20, 2022 
Publication Code:  MFS134 
Service: Fund/SERV
® 
Title: Fund/SERV Technical Manual -  Chapter 4: Communicating with Fund/SERV  
 

---

## Page 3

 
 
CHANGE HISTORY 
 
Dates Changes 
July 20, 2022 Learning upgrade caused some link(s) to break.  Link(s) are now corrected.  
July 21, 2021 Guide reviewed and content refreshed.  
January 21, 2021 Rebranded  
July 10, 2020  Broken links corrected.  
 
 

---

## Page 4

 
 
TABLE OF CONTENTS 
 
Communicating with Fund/SERV ...................................................................................................... 6  
Introduction.................................................................................................................................... 6  
Communications Background .......................................................................................................... 7  
Method of Connection ..................................................................................................................... 7  
Determining Methods of Communication ............................................................................................ 7  
General Timeframes ....................................................................................................................... 7  
Communication of [[settlement]]........................................................................................................... 8  
Turnaround Time ............................................................................................................................ 8  
[[settlement]] Files ............................................................................................................................. 8  
[[settlement]] Funds ........................................................................................................................... 8  
Settling Bank ................................................................................................................................. 8  
Co nso lid ated Statement File............................................................................................................. 9  
Fund/SERV Communications Options ..............................................................................................10  
Selecting a Communication [[Option]] .................................................................................................. 10 
Terminology................................................................................................................................. 10 
Selecting Different Communication Options ...................................................................................... 10 
Input Communication Options .........................................................................................................11  
Sing le Batc h ................................................................................................................................ 11 
Multi-Batc h .................................................................................................................................. 11 
Interactive ................................................................................................................................... 11 
Output Communication Options ......................................................................................................12  
Interactive Output ......................................................................................................................... 12 
Multi-Cyc le Output ........................................................................................................................ 12 
Sing le Outp ut ............................................................................................................................... 12 
Fund/SERV Processing Files ...........................................................................................................13  
Introduction.................................................................................................................................. 13 
DataTrak ..................................................................................................................................... 13 

---

## Page 5

 
 
AutoR ou te ................................................................................................................................... 13 
 
 

---

## Page 6

Technical Manual - Chapter 4: Communicating with Fund/SERV  
Communicating with F und/SERV 6 
COMMUNICATING WITH FUND/SERV 
Introduction 
This chapter contains information on communicating with Fund/SERV. It contains the following topics:  
• Communications Background: This topic describes the ways that Fund/SERV accepts input from clients. 
Each client submits input to Fund/SERV according to their communications options.  
• Communication of [[settlement]]: This topic contains information on communicating [[settlement]].  
• Fund/SERV Communications Options: This topic provides information on the communications options 
offered by Fund/SERV.  
• Input Communications Options: This topic describes the three input communications levels in Fund/SERV. 
These levels include single batch (once a day), multi-batch (throughout the day), and interactive (real time 
- as data is received, it is processed).  
• Output Communications Options: This topic describes the four output communications options in 
Fund/SERV. These options include intra-day (at specified time frames throughout the day), interactive 
(real time), multi-cycle (throughout the day), and single (once a day).  
• Fund/SERV Processing Files: These are the Fund/SERV processing files for both firm and fund 
transactions.  
 
 

---

## Page 7

Technical Manual - Chapter 4: Communicating with Fund/SERV  
Communications Background 7 
COMMUNICATIONS BACKGROUND 
Method of Connection 
The method of connection can be:  
• CPU to CPU (mainframe)  
• MyDTCC web portal 
Determining Methods of Communication 
Your [[NSCC]] Relationship Manager will connect you with the [[NSCC]] Connectivity team to help you determine 
the best method for you or your service provider. They will analyze the following:  
• expected volume  
• existing software  
• communications software, and  
• communications hardware.  
Reference: 
For more information,  there are connectivity reference materials available under “Connectivity”  section of the Learning 
Center https://dtcclearning.com/content/2633- connectivity -repository.html  
The way information flows to and from Fund/SERV is dependent upon the communication [[Option]] chosen. 
Funds and firms can select their input and output methods from the following options:  
• single (use with fixed or variable length records)  
• multiple (use with fixed length or variable length records)  
• interactive (use with variable length records only).  
Notes:  
Interactive players are required to use MQ Series software. These options can  affect the type of connection that is 
established. For example, if you use variable length records, then a leased line with a file transfer package is required.  
[[NSCC]] edits all input for required data elements.  
General Timeframes 
All time frames specified are Eastern Time (ET).  
Firms and funds can submit transactions between 2 a.m. and midnight. 
Reference: 
For detailed information on processing times, please visit  https://dtcclearning.com/products -and-services/mutual-fund -
services/schedules.html  

---

## Page 8

Technical Manual - Chapter 4: Communicating with Fund/SERV  
Communication of [[settlement]] 8 
COMMUNICATION OF [[settlement]] 
Turnaround Time 
[[NSCC]] processes incoming data every hour on the hour with an extra cycle at peak times. Turnaround times 
depend on the volume of transactions taken in by the system the previous hour. [[NSCC]] transmits output files on 
an hourly basis and additional times during high volume. For more information, please see Schedules in the 
Mutual Fund section of the Learning Center https://dtcclearning.com/products-and-services/mutual-fund-
services/schedules.html 
 
[[settlement]] Files 
Fund/SERV issues two [[settlement]] files to each client every day.  
• One file is produced each evening between 8 p.m. and 9 p.m. ET for mutual fund orders settling the next 
day (02112365).  
 
Example: Load funds typically with a Trade Date+2 [[settlement]] date, will appear on Trade Date+1. 
• The other file is produced at approximately 12 noon ET. This [[settlement]] file is for orders due to settle on 
the same day the file is generated (02112364).  
 
Examples:  
No-Load orders typically with a Trade Date+1 [[settlement]] date, and  
Money Market Fund orders typically with a Trade Date equal to the [[settlement]]. 
[[settlement]] Funds 
All [[obligations]] settle with [[NSCC]]'s Treasury/Money [[settlement]] Department using Same Day Funds (Fed Funds 
Wire). 
Settling Bank 
[[NSCC]] has requested that each client select a "Settling Bank" who will settle on their behalf.  
A consolidated [[settlement]] statement for each client is produced and provided to each client's settling bank at 
approximately 4 p.m. ET. The settling bank either acknowledges and settles (pays or collects) the client's 
obligation or refuses to pay.  If the settling bank refuses to pay, [[settlement]] [[obligations]] for the impacted [[Member]] 
will be reversed across contra parties to bring the client from a debit position to a flat or credit position.  They 
will need to settle their [[obligations]] outside of [[NSCC]]. 

---

## Page 9

Technical Manual - Chapter 4: Communicating with Fund/SERV  
Communication of [[settlement]] 9 
Consolidated Statement File 
Consolidated [[settlement]] information is available through [[DTCC]] [[settlement]] on the MyDTCC web p ortal via a 
special AutoRoute 02132518 file. 

---

## Page 10

Technical Manual - Chapter 4: Communicating with Fund/SERV  
Fund/SERV C ommunicati ons Options 10 
FUND/SERV COMMUNICATIONS OPTIONS 
Selecting a Communication [[Option]] 
Each client who joins Fund/SERV is required to complete a Fund/SERV Membership Profile form.  These 
forms are on the MyDTCC web portal under the Fund/SERV product menu [[Option]] at MyDTCC portal. 
To access these forms, you should contact your firm’s Super Access Coordinator (SAC) and have the SAC 
grant you access to the ‘MFS forms’ role under the Fund/SERV product. Once the MFS forms role is granted, 
no further action is required. 
If a SAC does not have [[Entitlement]] to grant access to the Fund/SERV product, or if a SAC needs to be 
established, you may contact WMS Management Services at 212-855-8877 or WMSConnect@[[DTCC]].com.  
 
Reference: 
For more information on the [[Member]] Profile Form, refer to the topic "[[Member]] Profile Field Descriptions" in Chapter 3.   
Terminology 
The following terms are used to describe input and output.  
• Batch refers to client input to [[NSCC]].  
• Cycle refers to [[NSCC]] output to clients.  
• DataTrak is the facility for transmitting data to [[NSCC]].  
• AutoRoute is the facility for transmitting data to clients.  
Selecting Different Communication Options 
A client may pick different communications options for their input and their output. 
Example: 
A [[Member]] can be Multi -Batch input into Fund/SERV and output from Fund/SERV.  
 

---

## Page 11

Technical Manual - Chapter 4: Communicating with Fund/SERV  
Input Communic ation Options 11 
INPUT COMMUNICATION OPTIONS 
Single Batch 
This [[Option]] is for clients who wish to send Fund/SERV data to [[NSCC]] just once a day. One input batch is 
processed daily by [[NSCC]]. 
Note: 
Only client s with very low transaction volume (under 10 orders per day) should consider this [[Option]].  
Multi-Batch 
With the multi-batch [[Option]], a client can transmit Fund/SERV data into [[NSCC]] multiple times throughout the 
day. A client can transmit files starting at 2 a.m. ET to 12 midnight. Each multi-batch transmission has the 
same file number, but transmissions are differentiated by a batch counter. 
Example: 
All Fixed Length order files sent by a firm would have a file number of 01125. If it were the firm's first file of the day, t he 
batch counter would read: 001. The next file would bump the file counter to 002, etc . 
In addition to the batch counter, there is a "Last File" indicator on each transmission. A client notifies [[NSCC]] 
that this is or is not the last file they intend to send for the day.  
• "Y" signifies it is the last file, and  
• "N" signifies it is not the last file.  
This [[Option]] is recommended for firms and funds processing high numbers of transactions through the system. 
Interactive 
The Interactive [[Option]] allows members to submit Fund/SERV transactions to [[NSCC]] as activity becomes 
available. Transactions are processed as they are received, in real time. [[NSCC]] uses MQ for its message 
switching software. MQ is a message switching software protocol from IBM. Interactive Clients [[DO]] not use 
DataTrak. 
Note: 
Clients  who choose the interactive method must use variable length record layouts . 
 

---

## Page 12

Technical Manual - Chapter 4: Communicating with Fund/SERV  
Output Communication Options 12 
OUTPUT COMMUNICATION OPTIONS 
Interactive Output 
Clients choosing interactive communications will receive output transactions, created by contra clients, 
immediately as it becomes available on a transaction basis. However, records created by Fund/SERV (as 
Reminders, [[settlement]], etc.) will be sent out via AutoRoute. AutoRoute automatically determines whether the 
output files are in fixed or variable format, according to the client’s setup.  
The following are the output files being sent out to interactive clients via AutoRoute 
Transactions AutoRoute File Number  
Same Day [[settlement]] file  02112364  
Next Day [[settlement]] file  02112365  
[[NSCC]] reminders only  02112362  
Multi-Cycle Output 
The multi-cycle [[Option]] provides clients with multiple output files, which are made available throughout the day. 
Multi-cycle files are generated every hour or less, from 2 a.m. to midnight.  
Since each multi-cycle transmission has the same file number, a cycle counter differentiates the transmission. 
Example: 
All multi- cycle output files received by a firm would have a file number of 02112361. If it were the firm's first file transmitted 
that day, it would contain a cycle counter 01. The next file would bump the cycle counter to 02, etc. The last 02112361 file 
of the day will contain cycle counter 98 . 
Single Output 
A [[Member]] choosing the single [[Option]] will receive only two output files in addition to Reminder and [[settlement]] 
files. These are the 02112361 and 02112363 files with a cycle counter of 98. 
 
 

---

## Page 13

Technical Manual - Chapter 4: Communicating with Fund/SERV  
Fund/SERV Processi ng Files 13 
FUND/SERV PROCESSING FILES 
Introduction 
Fund/SERV accepts input files via DataTrak and sends out output files via AutoRoute for both firm and fund 
transactions. 
DataTrak 
DataTrak provides systems information (input) to [[NSCC]] about a firm or fund, including: 
• the data being sent, and  
• how it is being sent.  
Note: 
1. Every Multi-batch file sent to [[NSCC]] will have a batch counter associated with it. Clients can send as many 
files as they wish (up to 999 files a day). For each subsequent file sent, the client must bump up their batch 
counter by one. This prevents [[NSCC]] from processing the same file twice and keeps each file unique.  
2. Clients must identify whether the file they have sent is their last one for the day. The DataTrak header record 
contains a "Last File Indicator." Clients must specify either a  
• “Y" (for “Yes, it is the last file I'm sending today"), or  
• "N" (for "No,  it is not the last file, I will be sending an additional file.")  
AutoRoute 
AutoRoute allows [[NSCC]] to communicate to the firm or fund (output) and includes  
• identifying the client  
• the system being used, and  
• how the data is being transmitted.  
Notes: 
1. [[NSCC]] bumps up the output cycle counter by one every time it sends out a file. This prevents the client  from processing 
the same file twice and keeps each file unique.  
2. Client s should program their file cycle counter dynamically. This will allow client s to be flexible in the number of files they 
receive if more output cycles are added. If the counters are "hard coded," it can necessitate a programming change. The 
only exception is for a cycle count of 98 since these are [[NSCC]]'s last multi -cycle (02112361 or 02112363) files of the day.  
Reference: You can access the “Schedules” in the Learning Center https://dtcclearning.com/products-and-
services/mutual-fund-services/schedules.html  
If you have any questions or comments, please contact Wealth Management Services at 212-855-8877. 

---

## Page 14

Technical Manual - Chapter 4: Communicating with Fund/SERV  
Fund/SERV Processi ng Files 14 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 