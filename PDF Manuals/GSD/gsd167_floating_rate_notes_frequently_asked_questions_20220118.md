---
title: "DVP Floating Notes FAQs "
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd167_floating_rate_notes_frequently_asked_questions_20220118.pdf"
pages: 15
size: "284.5 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# DVP Floating Notes FAQs 

**Original File:** [gsd167_floating_rate_notes_frequently_asked_questions_20220118.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd167_floating_rate_notes_frequently_asked_questions_20220118.pdf)  
**Category:** GSD  
**Total Pages:** 15  
**File Size:** 284.5 KB  

---

## Page 1

 
[[FICC]] – [[GSD]]  
FLOATING RATE NOTES (FRN) FREQUENTLY ASKED QUESTIONS (FAQ)  
 
VERSION 2.1 
JANUARY 18, 2022 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: January 18, 2022 
Publication Code: GSD167 
Service: [[FICC]] – [[GSD]]  
Title: Floating Rate Notes (FRN) Frequently Asked Questions (FAQ)  
 
 
The Floating Rate Notes (FRN) Frequently Asked Questions (FAQ) (hereinafter, the "document") is provided as a 
convenience to Members and is for information purposes only. Although [[FICC]] may make this document available to 
Members, it shall be under no obligation to [[DO]] so, nor having once or more done so, shall [[FICC]] have a continuing 
obligation to make available this document or other related information of a certain type.  
 
[[FICC]] does not represent the accuracy, adequacy, timeliness, completeness, or fitness for any particular purpose 
of any information provided to Members in this document, which is provided as-is. [[FICC]] shall not be liable for any 
loss related to such information (or the act or process of providing such information) resulting directly or 
indirectly from mistakes, errors, or omissions, other than those caused directly by gross negligence or willful 
misconduct on the part of [[FICC]]. [[FICC]] shall not be liable for: (1) any loss resulting directly or indirectly from 
interruptions, delays, or defects arising from or related to providing this guide; and (2) any special, consequential, 
exemplary, incidental, or punitive damages.  
 
Further, the information contained in this document is subject to change. Members and other authorized users of the 
document will find the most current version of the document on [[DTCC]]’s Learning Center site, 
www.dtcclearning.com. 
[[FICC]] shall bear no responsibility for any losses associated with the failure of Members or other authorized users to follow 
[[FICC]]’s most current document. 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Introduction .......................................................................................................................................................... 4 
Floating Rate Notes (FRN) FAQ .......................................................................................................................... 5 
1. What changes has the Fixed Income Clearing Corporation’s ([[FICC]]) Government [[securities]] Division 
([[GSD]]) made to its processing with regard to FRN? .................................................................................. 5 
2. How is a T+1 Buy/Sell trade being handled for FRN? .............................................................................. 5 
3. Has the introduction of the FRN impacted a [[Member]] firm’s input to [[GSD]]’s systems? ............................ 5 
4. Has [[GSD]]’s Auction Takedown Process changed due to the introduction of FRN? ................................. 5 
5. Has there been any impact to When Issued (WI) Processing with the introduction of FRN? .................. 5 
6. Can you describe the change if a matched forward trade (post WI period) is open in the system and 
crosses a reset date? ................................................................................................................................ 7 
7. What outputs does [[GSD]] provide when the FRN final money is changed on a trade? ............................. 7 
8. How does [[GSD]] process the coupon payment due on FRN [[securities]] [[settlement]] [[obligations]] that fail to 
settle by the payable date? ...................................................................................................................... 7 
9. How does the introduction of the FRN impact [[GSD]]’s GCF Repo® service? ........................................... 8 
10. How are term GCF Repo trades crossing over the reset date handled? .................................................. 8 
11. What should [[Member]] firms test if they anticipate trading buy/sell trades in the FRN? ............................ 8 
12. Can you provide some examples of the FRN processing logic? .............................................................. 9 
 

---

## Page 4

Floating Rate Notes (FRN) Frequently Asked Questions (FAQ) 
Introduction 4 
INTRODUCTION 
On July 31, 2013, the Treasury Department published the final rule which, among other things, addressed the 
accrual and the frequency of the rate change for Treasury [[securities]] with floating rate interest payments. The 
final rule also summarized key provisions and features of the floating rate note (“FRN”) program. The Treasury 
Department’s final rule, frequently asked questions and term sheet are available at: 
www.treasurydirect.gov/instit/statreg/auctreg/auctreg.htm. 
On November 20th, 2013, “Treasury has provided examples of floating rate note calculations and an interest 
accrual schedule. Please note that these examples are for illustrative purposes only.” These examples are 
available at http://www.treasurydirect.gov/instit/statreg/auctreg/auctreg_frncalex.htm. 
Other supporting information is available at https://www.treasurydirect.gov/instit/marketables/frn/frn.htm.  
 

---

## Page 5

Floating Rate Notes (FRN) Frequently Asked Questions (FAQ) 
Floating Rate Notes (FRN) FAQ 5 
FLOATING RATE NOTES (FRN) FAQ 
1. What changes has the Fixed Income Clearing Corporation’s ([[FICC]]) 
Government [[securities]] Division ([[GSD]]) made to its processing with regard 
to FRN? 
From a trade flow perspective, FRN is handled in the same processing manner as fixed rate notes. 
The matching logic, netting and subsequent [[settlement]] logic has not changed, apart from par 
summarization which is not applied to FRN.  
2. How is a T+1 Buy/Sell trade being handled for FRN? 
There are no changes in the processing of the majority of T+1 Buy/Sell trades. [[Member]] firms executing 
a buy/sell trade and trading off the existing index rate at the time of the trade, submit the price and/or 
final money to [[GSD]] for matching and processing. 
However, if a T+1 trade is booked on a Monday and Tuesday is a holiday, the final money calculation 
will change. Please see the examples in the section labeled “Can you provide some examples of the 
FRN processing logic?”, which highlights how final money will change on a T+1 trade when the 
[[settlement]] date is extended due to a holiday.  
3. Has the introduction of the FRN impacted a [[Member]] firm’s input to [[GSD]]’s 
systems? 
There have been no input changes to the [[GSD]] Real-Time Trade Matching (RTTM®) Web application, 
messages or batch files. 
4. Has [[GSD]]’s Auction Takedown Process changed due to the introduction of 
FRN? 
No, firms participate in the auction process as they had before the introduction of the FRN. The Fed 
forwards the final results of the auction awards to [[GSD]] on Auction date and these trades inclusive of 
final money are processed as they were prior to FRN. These trades are locked-in trades. Firms have 
the [[Option]] of submitting trades against the Auction Takedown trades for operational matching 
purposes. 
5. Has there been any impact to When Issued (WI) Processing with the 
introduction of FRN? 
Yes, [[GSD]] has enhanced its existing When Issue (WI) Processing for FRN.  

---

## Page 6

Floating Rate Notes (FRN) Frequently Asked Questions (FAQ) 
Floating Rate Notes (FRN) FAQ 6 
When Issued (WI) Processing of FRN: 
• Firms submit FRN trades with [[CUSIP]], yield (defined as the index rate plus the discount [[Margin]] or 
“r” + “m”) and par during the WI period. 
o For FRN trades with a negative yield, firms should not submit such trades to [[GSD]] during the 
WI period. Such trades should be submitted after the auction. 
• On a daily basis the assumed spread “s” will be derived by taking the average of the trade “yields” 
(“r” + “m”) for the purpose of calculating a MtM. 
• On the FRN auction date, the effective index rate and the actual spread the FRN “yield”-to-price 
conversion will be executed for the computation of [[GSD]]’s final money. 
• For firms trading during the WI period, post FRN announcement and prior to FRN auction, if an 
index rate change occurs, [[GSD]] will update the index rate on the transaction to the index rate in 
effect at auction to perform the “yield”-to-price conversion. 
• The newly calculated final monies are reported to [[GSD]] [[Member]] firms. [[GSD]]’s calculated final 
monies will match the final monies calculated by the [[Member]] firms. 
 
The Treasury Department’s FRN will trade on a discount [[Margin]] basis “m”. The Treasury Department 
published the following formula for the [[Margin]]-to-price conversion. 
 
 
 
Definitions as per the Final Rule, http://www.treasurydirect.gov/instit/statreg/auctreg/2013-18178.pdf :  
• “m” is the discount [[Margin]] on which the security will be traded 
• “r” is the index rate, to a precision of 9-decimal places, the High Rate from the 13-week T-bill 
auction converted to a simple-interest money market yield on an actual/360 basis as computed in 
the Uniform Offering Circular 
• “s” is the spread, or the assumed coupon 
 
[[GSD]]’s When Issued (WI) Processing for all [[securities]] other than FRN: 
• Firms trade on a yield basis and submit [[CUSIP]], yield and par during the WI period. 
• On a daily basis, [[GSD]] calculates a WI trade’s assumed final money, based on an assumed 
coupon, and performs a [[mark-to-market]] (“MtM”) 
o [[GSD]] derives an assumed coupon from the weighted average of all the WI trade yields in the 
system at that time. 
o For the purpose of MtM, a yield-to-price (“YTP") conversion is performed using the trade’s 
yield and the calculated [[GSD]] assumed coupon. 


---

## Page 7

Floating Rate Notes (FRN) Frequently Asked Questions (FAQ) 
Floating Rate Notes (FRN) FAQ 7 
o From the point of match until auction date, each night [[GSD]] will recalculate the trade’s 
assumed final money based on the most current assumed coupon as calculated by all the 
trades in the system. 
o Each night [[GSD]] sends to its Members, reporting (i.e. MRO or batch files) reflecting [[GSD]]’s 
calculated assumed final monies. 
• On auction date, the real coupon is known and the actual (current) YTP conversion is run to 
calculate final money on the affected trades. 
o The newly calculated final monies are reported to [[GSD]] [[Member]] firms. [[GSD]]’s calculated final 
monies will match the final monies calculated by the [[Member]] firms. 
6. Can you describe the change if a matched forward trade (post WI period) 
is open in the system and crosses a reset date? 
Please see #12 of this document which describes this scenario. 
7. What outputs does [[GSD]] provide when the FRN final money is changed on 
a trade? 
Matched forward trades that are in the system and that subsequently cross over the FRN index reset 
date, will have a change in their processing. While the initial input for forward trades (i.e., messaging, 
web or batch) will not change, there will be a change to the output generated by [[GSD]]. When a forward 
buy/sell trade crosses over the reset date, [[GSD]] changes the final money on the trade based upon the 
new index adjusted “new” accrual. The final money change will be reflected in the following output: 
• PDF reports in [[FICC]] Report Center 
• End-of-day Netting MRO Record Type “25” (Recalculated Money for Coupon Reset) was added to 
support the batch file process and is available for firms opting to take this output. This file is 
generated at the end of business day of reset date minus 1. 
 
Forward buy/sell trades in the system that are open on payable date will settle vs. [[GSD]] via the Funds-
Only [[settlement]] process and will reflect the most recent accrual. 
8. How does [[GSD]] process the coupon payment due on FRN [[securities]] 
[[settlement]] [[obligations]] that fail to settle by the payable date? 
Coupon payments on FRNs are processed in the same manner that other coupon payments are 
processed by [[GSD]]. If a [[securities]] [[settlement]] obligation resulting from a Forward buy/sell trade fails to 
settle by the payable date, the appropriate amount of cash will settle vs. [[GSD]] via the Funds-Only 
[[settlement]] process and will reflect the most recent coupon. All coupon payments processed by [[GSD]], 
are reflected in the Coupon Paid report located in the DVP folder of the [[GSD]] section of [[FICC]] Report 
Center. 
  

---

## Page 8

Floating Rate Notes (FRN) Frequently Asked Questions (FAQ) 
Floating Rate Notes (FRN) FAQ 8 
9. How does the introduction of the FRN impact [[GSD]]’s GCF Repo® service? 
With respect to the GCF Repo® service, the Floating Rate Notes are eligible as good [[collateral]] in the 
following GCF Repo Generic CUSIPS:  
• 371487AD1 – U.S. Treasury Maturing in Less than 10 Years (TU10) 
• 371487AE9 – U.S. Treasury Maturing in Less than 30 Years (TU30) 
10. How are term GCF Repo trades crossing over the reset date handled? 
No changes are made to the final monies on term GCF Repo trades. The end-of-day GCF output files 
will not change on these transactions.  
11. What should [[Member]] firms test if they anticipate trading buy/sell trades in 
the FRN? 
All [[Member]] firms that anticipate trading U.S. buy/sells in the FRN should update their systems in order 
to test with [[GSD]]. [[Member]] firms should review the MRO file specifications and consult with your 
internal technology staff because the netting files may not be sequential within [[GSD]]’s end-of-day file 
transmission. [[FICC]] recommends that the MRO 25 records be read prior to reading the MRO 17 record 
in order to reconcile to the new final money values.  
 Firms can test: 
• End of day MRO 25 Record (attached to existing file) 
• Test to ensure Next Day and Forward cash trade calculations match [[GSD]] 
• Test T+1 Holiday logic 
• Ensure Yield calculations on when issued trades are submitted properly 
• Test to ensure their internal when issued final money calculations match [[GSD]] 
 
The [[FICC]] Integration Team can be contacted at FICCIntegration@[[DTCC]].com. A test script may be 
provided. The [[GSD]] DVP RTTM PSE test region is available to [[GSD]] members and is open at 
approximately 6:00 AM ET and will remain open until 4:30 PM ET each business day. Support for the 
PSE region will be available from 8:30 AM to 4:30 PM ET each business day. 
  

---

## Page 9

Floating Rate Notes (FRN) Frequently Asked Questions (FAQ) 
Floating Rate Notes (FRN) FAQ 9 
12. Can you provide some examples of the FRN processing logic? 
For Reference: 
• T-Bill Auction Date – Mondays excluding holidays 
• Index Reset Date – T-Bill Auction Date +1 
• Trading Logic – Although the T-Bill Auction occurs on Monday and results are announced midday, 
firms should continue to trade off the prior Monday’s rate all day. The new rate becomes effective 
on Tuesday. 
 
The below examples show how Regular Way Trades submitted post the WI period will be processed. These 
trades are submitted to [[GSD]] with price and final money – Non-Holiday. 
SAMPLE CALENDAR 
DATE ACTIVITY APPLICABLE RATE USED FOR TRADE DATE 
Monday, October 21, 2019 T-Bill Auction Prior T-Bill auction high rate 
Tuesday, October 22, 2019   10/21 T-Bill auction high rate 
Wednesday, October 23, 2019   10/21 T-Bill auction high rate 
Thursday, October 24, 2019   10/21 T-Bill auction high rate 
Friday, October 25, 2019   10/21 T-Bill auction high rate 
Monday, October 28, 2019 T-Bill Auction 10/21 T-Bill auction high rate 
Tuesday, October 29, 2019   10/21 T-Bill auction high rate 
Wednesday, October 30, 2019   10/21 T-Bill auction high rate 
Thursday, October 31, 2019   10/21 T-Bill auction high rate 
 
T + 1 Trade Examples – No Money Changes 
• T+1 Trades with a Trade Date (TD) of Tuesday 10/22 through Friday 10/25 will utilize the Monday 
10/21 Rate. 
• T+1 Trades with a TD of Monday 10/28 will utilize the Monday 10/21 Rate. 
• Trades with a TD of Tuesday 10/29 will utilize the Monday 10/28 Rate. 
 
Forward Trade Examples 
• Trades with a TD of Wednesday 10/23 and [[settlement]] Date (SD) of Friday 10/25 will utilize the 
Monday 10/21 Rate. No change is made to final money. 
• Trades with a TD of Wednesday 10/23 and SD of Monday 10/28 will utilize the Monday 10/21 Rate. No 
change is made to final money. 
• Trades with a TD of Wednesday 10/23 and SD of Tuesday 10/29 will utilize the Monday 10/21 Rate. 
No change is made to final money. 
• Trades with a TD of Wednesday 10/23 and SD of Wednesday 10/30 will have a change to final money. 
The MRO 25 will be generated by [[FICC]] [[GSD]] on Monday night (10/28) reflecting the change in final 
money. Any affect trades going into the net on 10/29 will reflect the new final money. 
 

---

## Page 10

Floating Rate Notes (FRN) Frequently Asked Questions (FAQ) 
Floating Rate Notes (FRN) FAQ 10 
The below examples show how Regular Way Trades submitted post the WI period will be processed. These 
trades are submitted to [[GSD]] with price and final money – Tuesday Holiday. 
SAMPLE CALENDAR 
DATE ACTIVITY APPLICABLE RATE USED FOR TRADE DATE 
Monday, December 31, 2018 T-Bill Auction Prior T-Bill (12/24) auction high rate 
Tuesday, January 01, 2019 New Year's Day 
Holiday 
New Year's Day Holiday - accrues at 12/31/2018 
rate 
Wednesday, January 02, 2019   12/31 T-Bill auction high rate 
Thursday, January 03, 2019   12/31 T-Bill auction high rate 
Friday, January 04, 2019   12/31 T-Bill auction high rate 
 
T+1 Trade Examples – Holiday (Assume Tuesday on 01/01 is a holiday) 
• For a T+1 Trade with a Trade Date (TD) Monday (12/31) and [[settlement]] Date (SD) of Wednesday 
(01/02), the final money on the trade will be changed. The new rate is effective on Tuesday, which is a 
holiday, as per the final rule referenced in the Introduction. The MRO 25 will be generated by [[FICC]] 
[[GSD]] on Monday night. Affected firms should change final money on their trades prior to reading the 
MRO 17 netting file. Trade will have accrual at two different rates (Monday 12/31 at the 12/24 Rate and 
Tuesday 01/01 at the 12/31 Rate). In this example the MRO 25 and final money updates to netting file 
will occur on the same night. 
• T+1 Trades with a TD of Wednesday 01/02 will utilize the Monday 12/31 Rate. No change is made to 
final money. 
 
Forward Trade Examples – Holiday (Assume Tuesday on 01/01 is a holiday) 
• For Trades with a TD of Wednesday (12/26) and SD of Wednesday (01/02), the final money on the 
trade will change. The new rate is effective on Tuesday, which is a holiday, as per the final rule 
referenced in the Introduction. The MRO 25 will be generated by [[FICC]] [[GSD]] on Monday night. Affected 
firms should change final money on their trades prior to reading the MRO 17 netting file. The trade will 
now have accrual at two different rates. In this example the MRO 25 and final money updates to 
netting file will occur the same night. 
 
  

---

## Page 11

Floating Rate Notes (FRN) Frequently Asked Questions (FAQ) 
Floating Rate Notes (FRN) FAQ 11 
The below examples show how Regular Way Trades submitted post the WI period will be processed. These 
trades are submitted to [[GSD]] with price and final money – Showing a Lock Out scenario. Lock out days are 
defined as Business Days. 
SAMPLE CALENDAR 
DATE ACTIVITY APPLICABLE RATE USED FOR TRADE DATE 
Thursday, April 25, 2019   04/22 T-Bill auction high rate 
Friday, April 26, 2019   04/22 T-Bill auction high rate 
Monday, April 29, 2019 T-Bill Auction - 
Lock Out Period  
04/22 T-Bill auction high rate 
Tuesday, April 30, 2019 Lock Out Period  04/22 T-Bill auction high rate 
Wednesday, May 01, 2019 Coupon Payment 04/22 T-Bill auction high rate 
Thursday, May 02, 2019   04/29 T-Bill auction high rate 
Friday, May 03, 2019   04/29 T-Bill auction high rate 
 
T+1 Trade / Coupon Payment Date Examples – Assume Payable Date Wednesday 05/01. 
Monday, Tuesday are Lock-Out Period and Wednesday is a Coupon Payment Date. 
• T+1 Trades with a TD of Monday (04/29) through Wednesday (05/01) will utilize the Monday 04/22 
Rate. No change is made to final money. 
 
Forward Trade / Coupon Payment Date Examples – Assume Payable Date Wednesday 05/01. 
Monday, Tuesday are Lock-Out Period and Wednesday is a Coupon Payment Date. 
• For Trades with a TD of Thursday (04/25) and [[settlement]] Date (SD) of Wednesday (05/01), the final 
money on the trade will not change. The new rate from 4/29 is effective on Thursday (05/02). The 
04/22 Rate will be utilized in the calculation from 04/25 through 04/30. 
• Trades with a TD of Thursday (04/25) and a SD of Thursday (05/02), the final money will change. The 
new rate from 4/29 is effective on Thursday (05/02), as per the final rule referenced in the Introduction. 
The MRO 25 will be generated by [[FICC]] [[GSD]] on Monday night. Affected firms should change final 
money on their trades prior to reading the MRO 17 netting file. 
 
  

---

## Page 12

Floating Rate Notes (FRN) Frequently Asked Questions (FAQ) 
Floating Rate Notes (FRN) FAQ 12 
 
This example demonstrates a Reopening (re-issue) with a Lock Out Period and the impact on the applicable 
rate used. 
Monday Holiday – 05/27/2019 (Memorial Day is a Monday Holiday) 
Normally, if a holiday falls on a Monday, the Auction would take place on Tuesday with the effective index rate 
being reset on Wednesday. However, for the Memorial Day holiday, this process will be different due to the re-
issue. 
SAMPLE CALENDAR 
DATE ACTIVITY APPLICABLE RATE USED FOR TRADE DATE 
Friday, May 24, 2019   05/20 T-Bill auction high rate 
Saturday, May 25, 2019   05/20 T-Bill auction high rate 
Sunday, May 26, 2019   05/20 T-Bill auction high rate 
Monday, May 27, 2019 Memorial Day 
Holiday  
05/20 T-Bill auction high rate 
Tuesday, May 28, 2019 T-Bill Auction 05/20 T-Bill auction high rate 
Wednesday, May 29, 2019 Lock Out Period  05/20 T-Bill auction high rate 
Thursday, May 30, 2019 Lock Out Period  05/20 T-Bill auction high rate 
Friday, May 31, 2019 SD of 1st re-issue of 
the April FRN 
05/20 T-Bill auction high rate 
Saturday, June 01, 2019   05/28 T-Bill auction high rate 
Sunday, June 02, 2019   05/28 T-Bill auction high rate 
Monday, June 03, 2019 T-Bill Auction 05/28 T-Bill auction high rate 
Tuesday, June 04, 2019   06/03 T-Bill auction high rate 
Note: WI trades are submitted with a “Yield” Price Type to [[GSD]]; “Yield” = “r” + “m”. 
 
T+1 Trade Examples – No Money Changes 
• T+1 Trades with a Trade Date (TD) of Friday 05/31 will utilize the Monday 05/20 Rate.                                                                                                                                        
However, final money submitted by the [[Member]] firms should be inclusive of Saturday and Sunday 
accrual at the Tuesday 05/28 Rate. 
 
  

---

## Page 13

Floating Rate Notes (FRN) Frequently Asked Questions (FAQ) 
Floating Rate Notes (FRN) FAQ 13 
 
The below examples show how WI Trades submitted during the WI period will be processed. These trades are 
submitted to [[GSD]] with a 'Yield' Price Type. [[GSD]] defines 'Yield' for the purposes of Floating Rate Notes as the 
Effective Index Rate or "r" +/- "m". 
  SAMPLE CALENDAR 
DATE ACTIVITY APPLICABLE RATE USED FOR TRADE DATE 
Monday, January 21, 2019 Martin Luther King, Jr. 
Day Holiday 
01/14 T-Bill auction high rate 
Tuesday, January 22, 2019 T-Bill Auction 01/14 T-Bill auction high rate 
Wednesday, January 23, 2019   01/22 T-Bill auction high rate 
Thursday, January 24, 2019 
FRN 
Announcement Date 
• 01/22 T-Bill auction high rate. 
• WI trading begins. 
• Firms submit a “Yield” Price Type to [[GSD]]. 
• “Yield” = “r” + “m”. 
• [[GSD]] issues the Compared Trade Summary 
file with assumed final money. 
• All compared WI trades shall have assumed 
final money calculated based on an 
assumed spread. 
• Current MRO 29 is sent. 
Friday, January 25, 2019  • 01/22 T-Bill auction high rate. 
• WI trading begins. 
• Firms submit a “Yield” Price Type to [[GSD]]. 
• “Yield” = “r” + “m”. 
• [[GSD]] issues the Compared Trade Summary 
file with assumed final money. 
• All compared WI trades shall have assumed 
final money calculated based on an 
assumed spread. 
• Current MRO 29 is sent. 
Saturday, January 26, 2019   01/22 T-Bill auction high rate 
Sunday, January 27, 2019   01/22 T-Bill auction high rate 
Monday, January 28, 2019 T-Bill Auction 
• 01/22 T-Bill auction high rate. 
• WI trading begins. 
• Firms submit a “Yield” Price Type to [[GSD]]. 
• “Yield” = “r” + “m”. 
• [[GSD]] updates the index rate on WI 
transactions to the 1/28 index rate. 
• [[GSD]] issues the Compared Trade Summary 
file with assumed final money. 
• All compared WI trades shall have assumed 
final money calculated based on an 
assumed spread. 
• Current MRO 29 is sent. 
Tuesday, January 29, 2019   • 01/22 T-Bill auction high rate. 
• WI trading begins. 
• Firms submit a “Yield” Price Type to [[GSD]]. 
• “Yield” = “r” + “m”. 

---

## Page 14

Floating Rate Notes (FRN) Frequently Asked Questions (FAQ) 
Floating Rate Notes (FRN) FAQ 14 
• [[GSD]] issues the Compared Trade Summary 
file with assumed final money. 
• All compared WI trades shall have assumed 
final money calculated based on an 
assumed spread. 
• Current MRO 29 is sent. 
Wednesday, January 30, 
2019 
FRN Auction / Lock 
Out Period 
• 01/28 T-Bill auction high rate 
• WI trading ends. 
• Post Auction Results, [[GSD]] will issue 
final monies based on the “yield”-to-
price conversion utilizing the 01/28 Rate 
and the announced spread. This is the 
final money that will go into the net. 
• This is the final money that will appear 
on the Netting reports. 
• Current MRO 29 is sent. 
Thursday, January 31, 2019 Lock Out Period 01/28 T-Bill auction high rate 
Friday, February 01, 2019 1st Floater Issuance 
Date 
01/28 T-Bill auction high rate 
Note:  
• For buy /sell trades, firms are required to submit price and should submit final money to [[GSD]].                                                                                                                                                                     
• Final money will be changed for compared trades only. Uncompared trades will not see a final money 
change.                                                                                                                                           
• The related MRO 25 will only be sent the night of the weekly T-Bill Auction. This data will be sent on 
trades even if the final monies are not changing due to the fact the rate did not change from week to 
week. 
 
 
 
 
 
 
 
 

---

## Page 15

 
 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 