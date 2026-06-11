---
title: "Networking Share Aging Best Practices"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_share_aging_bp_mfs351_20240108.pdf"
pages: 11
size: "309.0 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Networking Share Aging Best Practices

**Original File:** [net_share_aging_bp_mfs351_20240108.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_share_aging_bp_mfs351_20240108.pdf)  
**Category:** Other  
**Total Pages:** 11  
**File Size:** 309.0 KB  

---

## Page 1

 
 
 
 
Networking 
SHARE AGING BEST PRACTICES  
JANUARY 8, 2024 
 
 
 
 
 

---

## Page 2

Share Aging Best Practices 
Change History 2 
CHANGE HISTORY 
January 8, 2024 Document rebranded. Content reviewed.  
April 8.2022 Learning upgrade caused some link(s) to break.  Links have been corrected. 
07/14/2020 Corrected broken link 
  

---

## Page 3

Share Aging Best Practices 
Change History 3 
TABLE OF CONTENTS 
Change History ..................................................................................................................................................... 2 
Share Aging Overview ......................................................................................................................................... 4 
Overview ............................................................................................................................................................. 4 
Transfers ............................................................................................................................................................... 5 
Control/Reference Number and Control/Reference Number Indicator ............................................................... 5 
Automated Transfers .......................................................................................................................................... 5 
Direct Transfers .................................................................................................................................................. 5 
Share Aging File ................................................................................................................................................... 7 
Incomplete Lots ................................................................................................................................................... 7 
12B-1 Indicator .................................................................................................................................................... 7 
12B-1 Lot Date .................................................................................................................................................... 8 
Detailed Lots versus Rolled Up Lots ................................................................................................................... 8 
Short-Term Redemption Lots ............................................................................................................................. 8 
Jumbo Transaction Indicator .............................................................................................................................. 8 
Commissionable Share Indicator ........................................................................................................................ 9 
Indicators on Networking and Fund/SERV® .................................................................................................... 10 
Delivering Firm Share Aging Indicator ..............................................................................................................10 
 

---

## Page 4

Share Aging Best Practices 
 
Share Aging Overview 4 
 
SHARE AGING OVERVIEW 
[[NSCC]], together with the Enhancement Committee of the Investment Company Institute's [[Broker]]/Dealer 
Advisory Committee, endeavored to develop a standard and automated process to facilitate the transfer of 
share lot history information. The "best practices" contained in this guide are the result of this collaboration.  
Overview 
Accurate share aging allows funds and firms to ensure shareholders are charged the appropriate CDSC and/or 
short-term redemption fees upon redemption. Share aging also allows funds and firms to accurately track and 
remit 12b-1 fees and perform accurate share class rolls. When a mutual fund transfer occurs, the share aging 
information must be transmitted to the receiver. The receiving firm or fund will then assume the tracking of the 
share aging information. 
The process, through the [[NSCC]] Networking System, employs the use of a Share Aging file containing share 
lot history information. It also leverages other functionality within the ACATS, Fund/SERV®, and Networking 
services, thereby allowing the process to be centralized and standardized. 
The proposed guidelines will provide "best practices", specified by the industry participants, for the use of 
various fields and indicators in the Share Aging records, as well as functionality within the ACATS, 
Fund/SERV® and Networking services. 

---

## Page 5

Share Aging Best Practices 
 
Transfers 5 
 
TRANSFERS 
Control/Reference Number and Control/Reference Number Indicator 
In order to match share lot data to the applicable transfer, it is important that the Share Aging B/F75 record 
includes the Control Reference Number associated with the transfer. 
Effective June 2011, a "Control/Reference Number" and a "Control/Reference Number Indicator" are required 
fields on the B/F75 record. 
To ensure that every transfer contains a Control Reference Number, a Required fiel d for "Original Control 
Number Indicator" was added to the F55 Activity record. In addition, the "Original Control Number" field was 
changed from Optional to Optional/Conditional and is Required for all Direct Transfers (direct transfers are 
defined on the F55 record with a transaction type of '13'). Every automated transfer whether via Networking or 
ACATS-Fund/SERV® is already assigned a Control Number. 
Best practices for automated and manual transfers are discussed below. 
Automated Transfers 
When transferring via Networking, the resigning firm or fund should populate the "Control/Reference Number" 
field with the Networking Control Number and populate the "Control/Reference Number Indicator" field with a 
value of '2' (Networking Control Number) on the B/F75 Share Aging record. 
When transferring via ACATS-Fund/SERV®, the resigning firm or fund should populate the "Control/Reference 
Number" field with the Fund/SERV® Control Number and populate the "Control/Reference Number Indicator" 
field with a value of '1' for Fund/SERV® control number on the B/F75 Share Aging record. 
Note:  
In the case of ACATS, the "Control Reference Number" field (Share Aging Record F75, record 2, positions 26-45) needs to 
be populated with the Fund/SERV® Control Number, or the control number beginning with CATSA. If a fund or firm chooses 
to supply the Control Number supplied in the ACATS facility, this number should be entered into the "ACATS Control 
Number" field (Share Aging Record F75, record 2, positions 47-66) 
Direct Transfers 
When a direct transfer is requested by a firm for a rejected Networking or ACATS -Fund/SERV® transfer, the 
best practice is for the firm to provide the Control Number associated with the rejected transfer. The fund 
should populate the "Control/Reference Number" (B/F75 Share Aging Record) and the "Original Control 
Number" (F55 Activity Record) with this rejected Control Number and use the applicable indicator value ("1" for 
Fund/SERV® Control Number or "2" for Networking Control Number) on the "Control/R eference Number 
Indicator" field (B/F75) and "Original Control Number Indicator" field (F55).  
When the "Control/Reference Number Indicator" is populated with a '1' the [[NSCC]] will validate that the value 
supplied in the "Control/Reference Number" field or the "Original Control Number" field follows the required 
format for a Fund/SERV® control number. If the "Control/Reference Number Indicator" is populated with a value 
of '2' the [[NSCC]] will validate that the value supplied in the "Control/Reference Number" fie ld or the "Original 
Control Number" field follows the format for a Networking Control Number. If the supplied control number does 
not follow the appropriate format, the F55 Activity and/or the B/F75 Share Aging record will be rejected.  
If a Control Number is not provided by the requesting firm, or for a direct transfer, the fund should populate the 
F55 Activity Record and the B/F75 Share Aging Record with a Fund Originated Control Number and the 
Control Number Indicator should be updated with a value of '3' for Manual Reference Number. 

---

## Page 6

Share Aging Best Practices 
 
Transfers 6 
 
Note:  
The best practice for creation of a Fund Originated Control Number is to use the following format: 
DPPPPYYYY999999 where 
D—Stands for Direct  
PPPP—[[participant]] # 
YYYY—Julian Year (1st character would be the last character of the current year, and the next three would represent the 
Julian day i.e. August 28, 2023=2240)  
999999-Numeric Sequence Assigned by the [[Member]] 
The manual Control Number on the F55 should not exceed 15 bytes. 

---

## Page 7

Share Aging Best Practices 
 
Share Aging File 7 
 
SHARE AGING FILE 
Lots should be sent after every transfer, regardless of share class. The receiving firm or fund needs to 
determine which sub-files to update with the information based on the rules for that fund family/[[CUSIP]]. 
Therefore, the delivering firm/fund should utilize the Share Aging file for every transfer within 3 business days 
of posting the transfer to their record keeping system. In most cases, the Lots should be sent within 1 business 
day and the number of Lots must equal the number of [[shares]] transferred. Senders of Lots should not code to 
exclude any transfer. This coding will be developed on the Receiving firm's side.  
It's important to note; delaying the transmission of lot data after the transfer posts to the receiver's record 
keeping system may cause the client account to erroneously be charged Redemptions Fees (CDSC and Short -
term). 
Each date field represents the lot start date. The date should either be the trade date of the original purchase 
or the trade date of an exchange to another fund, whichever applies. If these dates are unavailable "Share 
Trade Date and Price Unknown" (transaction code 08) should be used. 
The following information provides details on select fields contained in the Share Aging Detail Record. The 
Share Aging Record layouts are available on the Learning Center under the Networking Record Layouts tab at:  
https://dtcclearning.com/products-and-services/mutual-fund-services/record-layouts.html 
Incomplete Lots 
As a best practice, the delivering firm or fund should ensure that the Lots in the Share Aging File equal the 
amount of the transfer. If the delivering firm's record keeping system does not have the  full lot information, then 
lots should be created prior to sending the information to ensure the number of lots equal the number of [[shares]] 
transferred. The delivering firm should use the date of the original transfer; therefore, they should never be 
sending incomplete lots or state they cannot provide complete lots. A required "[[default]] Lot Indicator" field 
should be used to indicate whether a specific share lot was defaulted to the original transfer date. The "[[default]] 
Lot Indicator" is located on the Share Aging Detail record (76), record 1 of 2, position 76. 
Field Name Start End Len Type Description O/R 
[[default]] Lot 
Indicator 
76 76 1 A/N 0 = No 
1 = Yes 
R 
12B-1 Indicator 
The "12b-1 Indicator" field on the Share Aging File record layout indicates whether the [[shares]] are eligible, pre-
agreement, ineligible, or not eligible for 12b-1's. If the transaction code is 08 (Share Trade Date and Price 
Unknown), the price, amount and trade date WILL NOT be required fields. The "12b -1 Indicator" is located on 
the Share Aging Detail record (76), record 1 of 2, position 77, and is required when the transaction code = "08."  
Field Name Start End Len Type Description O/R 
12b-1 Indicator 77 77 1 A/N 0 =Pre-Agreement [[shares]]  
1 =Eligible [[shares]] 
2= [[shares]] Ineligible/ Not Fully Aged 
3 =[[shares]] Ineligible Due to Other 
Required if Transaction Code= 08 
OC 

---

## Page 8

Share Aging Best Practices 
 
Share Aging File 8 
 
12B-1 Lot Date 
The "12b-1 Lot Date" field is a mandatory field that record keepers will need if [[shares]] are ineligible. This date 
field is located on the Share Aging Detail record (76), record 1 of 2, position 78-85, and is required when the 
transaction code = "0" or "2." 
Field Name Start End Len Type Description O/R 
12b-1 Lot Date 78 85 8 A/N mmddccyy 
Required if 12b-1 
Indicator = 0 or 2 
OC 
Detailed Lots versus Rolled Up Lots 
If the delivering firm or fund has the lot details, then all details should be sent to the receiving firm or fund. If the 
delivering firm or fund "rolls" up lots, then they can be rolled up after the appropriate CDSC and 12B -1 periods 
have completed (not applicable to B share Lots, since each lot needs to age for conversion to class A), this is 
generally 12 months. A separate lot needs to be created for each unique Lot type that is rolled -up and passed, 
such as differing 12B-1 payment rates and differing CDSC periods. 
Short-Term Redemption Lots 
The "Short Term Redemption Lot Date" field will be utilized to determine if [[shares]] are liable to be assessed 
short term redemption fees, or not. An Optional "Short Term Redemption Lot Date " field is located on the 
Share Aging Detail record (76), record 2 of 2, position 46-53. 
Field Name Start End Len Type Description O/R 
Short Term 
Redemption Lot 
Date 
46 53 8 A/N mmddccyy O 
Jumbo Transaction Indicator 
The "Jumbo Transaction Indicator" field should be used for any liable (for CDSC or short -term redemption fee) 
dated lot passed as part of a million dollar jumbo transactions. The indicator is an optional field, with Not Liable 
as the [[default]] value. The "Jumbo Transaction Indicator" is located on the Share Aging Detail record (76), 
record 2 of 2, position 54. 
Field Name Start End Len Type Description O/R 
Jumbo 
Transaction 
Indicator 
54 54 1 A/N 0 = No  
1 = Yes 
O 
 

---

## Page 9

Share Aging Best Practices 
 
Share Aging File 9 
 
Commissionable Share Indicator 
The "Commissionable Share Indicator" is a required field that is necessary for Firms and Funds to indicate 
whether a client has paid a commission on a specific share Lot and these [[shares]] may not be subject to 
additional commissions on future exchanges. The indicator is located on the Share Aging Detail record (76), 
record 2 of 2, position 55. 
Field Name Start End Len Type Description O/R 
Commissionable 
Share Indicator 
55 55 1 A/N 0 =Non-commissionable  
1 = Commissionable 
R 

---

## Page 10

Share Aging Best Practices 
 
Indicators on Networking and Fund/SERV® 10 
 
INDICATORS ON NETWORKING AND FUND/SERV® 
The fund is expected to transmit lot history on any fund held assets on behalf of the delivering firm and the 
"Delivering Firm Share Aging Indicator" is a mandatory field. 
The following Share Aging Indicators will be used in ACATS, Fund/SERV® and Networking. 
Delivering Firm Share Aging Indicator 
Value   Description 
1 The delivering firm or fund company will provide the aging information in an automated fashion through the 
Networking Share Aging records. 
2 The delivering firm or fund company will provide the share aging information outside of the system. 
 

---

## Page 11

 
 
© 2024 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation [[DTCC]].  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
Doc Info: January 8, 2024 
Publication Code: MFS351 
Service: Networking 
Title: Share Aging Best Practices 
For More Information 
 
Email Core Learning Service at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 
 