---
title: "MFPS II: Best Practices - Dividend and Capital Gain Distributions"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfpsii_div_capital_gain_bp_mfs348_20231122.pdf"
pages: 30
size: "598.5 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# MFPS II: Best Practices - Dividend and Capital Gain Distributions

**Original File:** [mfpsii_div_capital_gain_bp_mfs348_20231122.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfpsii_div_capital_gain_bp_mfs348_20231122.pdf)  
**Category:** Other  
**Total Pages:** 30  
**File Size:** 598.5 KB  

---

## Page 1

 
 
Mutual Fund Profile Service II 
BEST PRACTICES – [[Dividend]] AND CAPITAL GAIN 
DISTRIBUTIONS 
November 22, 2023 
 
 
 
 
 
 

---

## Page 2

Best Practices – [[Dividend]] and Capital Gain Distributions 
Change History 2 
CHANGE HISTORY 
Date Description 
11/22/2023 Document rebranded and reviewed.  Incorporated the addition of communicating [[Dividend]] 
and gain events via MF Info Xchange. 
06/13/2022 Broken links corrected and embedded Distribution Calendar Template was removed (link 
included in this document). 
07/15/2020 Broken links corrected. 

---

## Page 3

 
 
TABLE OF CONTENTS 
Change History ..................................................................................................................................................... 2 
Introduction .......................................................................................................................................................... 5 
Executive Summary ............................................................................................................................................. 6 
Distribution Background and Complexity ......................................................................................................... 7 
Background ......................................................................................................................................................... 7 
Complexity and Volumes .................................................................................................................................... 8 
Accurate and Timely Delivery of Information–A Changing Landscape ......................................................... 9 
Accurate and Timely Delivery of Distribution Information ................................................................................... 9 
Growth of Omnibus Accounts ........................................................................................................................... 9 
Growth of Retirement Plans .............................................................................................................................. 9 
Complexity of Products ..................................................................................................................................... 9 
Regulatory Impacts .........................................................................................................................................10 
Communication of [[Dividend]] Events................................................................................................................. 11 
Special Dividends............................................................................................................................................... 12 
Challenges for Firms ......................................................................................................................................... 13 
Timeliness of Communication ...........................................................................................................................13 
Accuracy of Data...............................................................................................................................................13 
Consistency of Format & Terminology..............................................................................................................14 
Omnibus Processing .........................................................................................................................................14 
Daily Accrual Processing ..................................................................................................................................14 
Inflated Accrual factors ....................................................................................................................................15 
Fluctuating Accrual Cycle End Dates ............................................................................................................16 
Posting Rules for Calculating Income on Transactions during the Accrual Cycle .........................................16 
Challenges for Funds/Transfer Agents ............................................................................................................ 17 
Accuracy ...........................................................................................................................................................17 
Timeliness .........................................................................................................................................................17 
Product Distribution...........................................................................................................................................18 
DETAILED BEST PRACTICES - [[Dividend]] and Capital Gain Distributions ................................................... 19 
Transmission of Distribution Information ..........................................................................................................19 

---

## Page 4

 
 
Special Dividends .............................................................................................................................................24 
Communication of Errors or Corrections ..........................................................................................................24 
Best Practices – Summary of Key points ........................................................................................................ 26 
Commonly Used Terms ..................................................................................................................................... 27 
Distributions ......................................................................................................................................................27 
Daily Accrual Dividends ....................................................................................................................................28 
Appendix ............................................................................................................................................................. 29 
 

---

## Page 5

Best Practices - [[Dividend]] and Capital Gain Distributions 
Introduction 5 
INTRODUCTION 
Challenges related to [[Dividend]] and capital gain distributions have been a consistent and recurring theme in 
reconciliation and recordkeeping of [[Mutual Funds]] by [[intermediary]] firms. In an effort to address these challenges 
in 2015, the Investment Company Institute’s Bank, Trust, and Retirement Advisory Committee (BTRAC) 
launched a task force made up of [[intermediary]] firms, service providers, and fund [[Companies]].  
The Task Force pursued several goals related to the topic of distributions: 
• Educate: raise awareness of the significance of the processes, and the dependencies that exist for this 
critical information. As the provider of this essential data, fund [[Companies]], including those managing fund 
accounting and [[transfer agent]] functions, must have an appreciation of the needs of the downstream 
consumers of the information. Similarly, an understanding of the opportunities and channels by which 
[[Dividend]] and capital gain distribution information is shared is of key value to the recipients of the data.  
• A nalyze : assess opportunities to gain efficiencies and improve timeliness of the delivery of [[Dividend]] and 
capital gain information, both in terms of receipt of the data and the consistency in formatting and data 
components. 
• D evelop: create resources for Funds and [[intermediary]] firms in the form of enhanced best practices, 
allowing for consistent approaches and processes by which information is shared and internalized.  
 
In pursuit of these goals, key components of the [[Dividend]] and capital gain distribution process were examined.  
Fundamental work, including a detailed assessment of the current [[Dividend]] and capital gain distribution 
environment, identification and definition of key terms, and determination of critical data points was performed. 
A detailed look at experiences of firms, service providers and Funds in this space helped to formulate a series 
of best practices and technical resources to ensure timely and efficient management and utilization of this 
critical information. While the document is focused primarily on the processes and work related to periodic 
dividends and capital gains, information about daily [[Dividend]] processes and best practices have been included 
where appropriate. 
These collective efforts are intended to encourage and promote timely and consistent delivery of this critical 
information to the industry. The end goal being the highest possible level of service and most  efficient 
operating environment for shareholders. 

---

## Page 6

Best Practices - [[Dividend]] and Capital Gain Distributions 
Executive Summary 6 
EXECUTIVE SUMMARY 
As stated above, timely and accurate distribution of [[Dividend]] and capital gain information in consistent and 
standard formats is critical for fund [[Companies]], service providers, and firms. To achieve this, the following best 
practices are encouraged, and covered in greater detail within this paper.  
1. Fully leverage [[DTCC]] capabilities: Funds and Firms should fully leverage the [[DTCC]] Mutual Fund Profile I 
and II Services to transmit and collect information regarding distributions. 
a. Periodic distribution information for future dividends and capital gains should be sent through Mutual 
Fund Profile II Distribution Declaration Database (MFPS II–Distribution Database), using the 
‘Projected’ indicator. 
b. Transmission of actual distribution information should be sent on Ex-date through MFPS II–
Distribution Database, by 6:00 p.m. ET ([[DTCC]] Cycle 12), using the ‘Actual’ Indicator. 
c. When communicating Daily Accrual Rates over weekends and holidays, it is recommended that 
Funds publish single rates for each day. It is understood, however, that bulk rates are an inherent 
part of many Funds’ delivery of this information; in cases where bulk rates are utilized, Funds should 
include the appropriate attributes to indicate the bulk accrual methodology, referenced within this 
paper. 
d. For all outbound [[DTCC]] records that include [[Dividend]] and capital gain distribution information, it is 
recommended that Funds populate all key data points as defined within this paper.  
2. Use a standardized calendar template when communicating projected distributions to firms : For situations 
where usage of the [[DTCC]] products are not an [[Option]], Funds should distribute distribution calendars as 
early as available (not later than early January) for the full year or distribute a monthly calendar beginning 
in January.  A standardized distribution calendar template with projected dates and details for all planned 
periodic distributions is available on Learning Center in MFSPII section 
https://dtcclearning.com/documents/mutual-fund-services-1/mfpsii/guides-12/4139-distribution-calendar-
template.html  
3. Communicate changes and corrections immediately: Immediate communication by Funds to shareholders 
and partner firms is recommended when distribution changes or corrections occur. 
4. Use standard terminology: Agreed-upon terms and definitions, as outlined in Commonly Used Terms of 
this document, should be used consistently to avoid confusion and miscommunication.  

---

## Page 7

Best Practices - [[Dividend]] and Capital Gain Distributions 
Distribution Background and Complexity 7 
DISTRIBUTION BACKGROUND AND COMPLEXITY 
Background 
The periodic distribution of mutual fund dividends and capital gains to the shareholders of a fund is an inherent 
part of how [[Mutual Funds]] are structured. Subchapter M of the Internal Revenue Code provides regulated 
investment [[Companies]] avoidance of the double taxation that regular corporations and shareholders are subject 
to when dividends and capital gains are paid to shareholders. 
A regular corporation pays corporate income taxes on its earnings and when dividends are paid to 
shareholders, [[The Corporation]] does not get a tax deduction for the dividends paid and the dividends are taxed 
again to the shareholders, thus double taxation. 
If a regulated investment company passes through at least 90% of the sum of its taxable income for a year in 
the form of dividends to its shareholders, the investment company gets a tax deduction for the dividends paid 
so only the shareholders receiving dividends are taxed. 
Furthermore, the character of the income, such as ordinary income or long-term capital gains, is retained when 
it is received by the shareholders. Section 19(a) of the 1940 Act generally prohibits a fund from making a 
distribution from any source other than the fund’s net income, unless that payment is accompanied by a written 
statement that adequately discloses the source or sources of the payment. The distribution of income from 
[[Mutual Funds]] to their shareholders will continue as long as [[Mutual Funds]] retain this favorable tax status under 
the Internal Revenue Code. 
The exchange of [[Dividend]] and capital gain information is a critical process to all parties involved in mutual fund 
trading, including fund [[Companies]], firms, and service providers. Timely application and incorporation of 
[[Dividend]] and capital gain information is a core component of accurate shareholder rec ords, timely payments, 
and efficient reconciliation practices for all parties involved. Information is shared in a variety of ways, ranging 
from automated file transmissions through the [[DTCC]] using both Mutual Fund Profile I and II, and manually 
using distribution calendars and declaration memos. 

---

## Page 8

Best Practices - [[Dividend]] and Capital Gain Distributions 
Distribution Background and Complexity 8 
A high-level view of the distribution process is included below. 
 
Figure 2 Lifecycle of a Mutual Fund Distribution 
Complexity and Volumes 
On an average business day, there is a significant amount of 
[[Dividend]] and capital gain data exchanged. The number of 
distribution events over the period of a month, quarter, or calendar 
year is significant, which is further compounded by the increasingly 
intermediated and outsourced mutual fund servicing environment, as 
well as the complexity of mutual fund products. 
The visual to the right shows a variety of parties involved in the 
exchange and dissemination of [[Dividend]] distribution information 
once declared or communicated by a Fund company. From a 
volume perspective, the statistics included below help to underscore 
how critical efficient, timely, automated, and consistent processes 
are within the intermediated [[Dividend]] distribution process.  
Washington, DC; October 31, 2022—According to new research 
published today by the Investment Company Institute (ICI), 68.6 
million, or 52.3 percent of, households in the United States owned 
[[Mutual Funds]] in 2022. This represents 115.3 million individual 
investors owning [[Mutual Funds]] in 2022. 
Figure 1 Fund Declares [[Dividend]] 

---

## Page 9

Best Practices - [[Dividend]] and Capital Gain Distributions 
Accurate and Timely Delivery of Information–A Changing Landscape 9 
ACCURATE AND TIMELY DELIVERY OF INFORMATION–
A CHANGING LANDSCAPE 
Accurate and Timely Delivery of Distribution Information 
When mutual fund shareholders were primarily registered in fully disclosed accounts on t he fund company’s 
[[transfer agent]] system, challenges related to the distribution of dividends and capital gains were minimal. 
Shareholders either elected to take the distribution in cash or re-invest. The Fund’s [[transfer agent]] managed the 
calculation and the processing of the distribution for the shareholder. Several significant changes have 
occurred over time that have complicated the issue of mutual fund distributions. Following are four of the more 
significant changes that occurred that have created a heightened importance around the delivery of timely and 
accurate mutual fund distribution data. 
Growth of Omnibus Accounts 
Millions of mutual fund shareholders now have their records kept by [[intermediary]] firms rather than by the fund 
company. [[intermediary]] firms utilize sub-accounting systems to track individual shareholders and their 
purchases, redemptions, dividends, and capital gains much like the fund [[Companies]] transfer agency systems 
[[DO]]. The [[intermediary]] firms aggregate individual shareholder trades and submit rolled up trades to an omnibus 
account at the Fund. The Fund calculates and distributes income only to the omnibus account, not to the 
underlying shareholders. It is the responsibility of the [[intermediary]] firm to calculate the individual shareholder 
[[Dividend]] and capital gain amounts and post to their account or pay out in cash. For an [[intermediary]] firm to 
calculate the proper [[Dividend]] and post it to the shareholders account, the [[intermediary]] firm needs accurate and 
timely declared distribution records. Most omnibus [[intermediary]] firms cannot wait for the posting of the paid 
[[Dividend]] to the omnibus account on payable date; and require the [[Dividend]] rate on ex-date in order to calculate 
and post dividends at the shareholder level that day. 
Growth of Retirement Plans 
The investments in retirement plans are generally [[Mutual Funds]] or wrapped products like fund- of-funds. 
Retirement plans are another form of omnibus accounts, as only the plan level trades are traded at the F und 
and in some cases, even plan level trades are rolled together and traded in what is called a super omnibus 
account. Recordkeepers track the [[participant]] account level trades, dividends, and capital gains. Most 
recordkeeping systems run what is called a “nightly cycle” where they process the day’s transaction after 
receiving the end of day prices, accrual rates, [[Dividend]] rates, and capital gains. For the larger recordkeepers, 
the “nightly cycle” process can involve processing millions of transactions. This nightly processing can take 
several hours so it is critical that the recordkeeper has both accurate and timely receipt of the end of day prices 
and accrual rates as well as any declared [[Dividend]] and capital gain distributions. A delay in the receipt of 
prices, accrual rates, or [[Dividend]] and capital gain rates may delay the nightly cycle and possibly cause an 
[[intermediary]] firm to miss the next morning’s cut off for trading via the [[DTCC]]’s DCC&S (Defined Contribution 
Clearance & [[settlement]]) service. 
Complexity of Products 
More and more firms are creating their own proprietary investment products, often utilizing only [[Mutual Funds]] or 
having [[Mutual Funds]] as part of the core investments inside the proprietary investment. These products can take 
many forms, such as fund-of-funds, target date funds or other wrap products. To facilitate the distribution as 
well as the recordkeeping of these investments, these proprietary investments have their own daily NAV or unit 
value. To properly calculate this daily unit value, the [[intermediary]] firm must have timely NAVs, acc rual rates 
and declared distribution rates for the underlying mutual fund [[securities]]. This unitization process can also be 
time consuming, so the sooner the NAVs, accrual rates and distribution rates are received, the sooner the 
unitization process can be kicked off. This unitization process has to be completed before intermediaries can 

---

## Page 10

Best Practices - [[Dividend]] and Capital Gain Distributions 
Accurate and Timely Delivery of Information–A Changing Landscape 10 
start their nightly cycle. Because of the timing considerations, Funds that consistently deliver timely distribution 
rates on ex-date are often good fits for wrap product programs. 
Regulatory Impacts 
As the mutual fund landscape evolves with regular changes to regulations and rules, F unds and [[intermediary]] 
firms have a heightened awareness of the role that efficient and accurate [[Dividend]] and capital gain processing 
play. Recent discussions regarding [[Liquidity]] risk, for example, may require estimated price and [[Dividend]] and 
capital gain activity to potentially occur earlier in the day, causing downstream challenges. The longer an 
[[intermediary]] firm waits on distribution information to be available, the more their ability to respond with any 
agility is limited. Introducing complex products into the equation, i.e. fund-of-funds, compounds the challenges 
with implementation of rule changes. Funds and [[intermediary]] firms should contemplate impacts and 
considerations related to [[Dividend]] and capital gain distribution and processing to ensure that related processes 
remain unaffected. 

---

## Page 11

Best Practices - [[Dividend]] and Capital Gain Distributions 
Communication of [[Dividend]] Events 11 
COMMUNICATION OF [[Dividend]] EVENTS 
[[intermediary]] firms typically support thousands of [[Mutual Funds]] on their pla tforms. As stated earlier, the 
importance of posting a fund distribution on ex-date is imperative to provide accurate account balances to 
shareholders and participants as well as providing accurate unit calculations on investment products containing 
[[Mutual Funds]]. 
When mutual fund [[Companies]] declare a [[Dividend]], they follow a sequence of events to communicate this 
information to the firms that distribute their funds. The sequence of events are generally as follows:  
1. By early January, the Fund sends out a [[Dividend]] calendar, either for the entire year or for the upcoming 
month. This communication may take  three forms: electronically through the MFPS II–Distribution 
Database, communicated through MF Info Xchange or via a spreadsheet sent from the Fund. These 
communications give firms an idea of when a Fund plans on declaring and paying dividends for their funds 
for the calendar year or the upcoming month. The calendar includes the Record, Ex, Reinvest and 
Payable dates but does not include the rate that will be paid.  
2. On the ex-date of the [[Dividend]] event, the Fund will publish an announcement/memo of the [[Dividend]] to 
include the required dates such as Record, Ex, Reinvest and Payable dates as well as the actual rate. 
This announcement/memo can be made through the MFPS II–Distribution Database, MF Info Xchange 
and in addition, is announced in the form of a press release and/or a blast email to a fund company’s 
distribution partners. 
3. Many Funds will also include the declared [[Dividend]] rate on Ex-date in the [[DTCC]]’s Mutual Fund Profile I 
Price and Rate file. This file contains limited date information pertaining to the event, specifically only 
including the ‘effective’ date. Firms that [[DO]] not need to calculate the [[Dividend]] amounts for their 
shareholders (i.e. firms with fully disclosed accounts), use this rate to verify the paid [[Dividend]] amounts 
and for communication to shareholders of the [[Dividend]] rate. Firms that are managing sub- accounting (i.e. 
retirement recordkeepers and omnibus firms) typically [[DO]] not use this source for rates as they need the 
corresponding dates in order to calculate the [[Dividend]] as of ex-date, prior to receipt of the paid [[Dividend]] 
via the Networking files. 
4. When the Fund pays the [[Dividend]] based on shareholders’ position balances as of the record date, the 
payment, whether cash or reinvested [[shares]], are typically communicated to the firms via the [[DTCC]]’s 
Networking [[Dividend]] records (F61–70 Records) the day after Ex-date. 

---

## Page 12

Best Practices - [[Dividend]] and Capital Gain Distributions 
Special Dividends 12 
SPECIAL DIVIDENDS 
At times, typically at the end of a fiscal or calendar year end, an unplanned or unscheduled [[Dividend]] may be 
declared by a fund, often referred to as a Special [[Dividend]]. Although the reasons that may trigger a Special 
[[Dividend]] vary, the drivers are typically undistributed income that exceeds a fund’s previously declar ed [[Dividend]] 
amounts or is recognized after a fund’s scheduled income distribution date for the period;  but must be 
distributed in the current fiscal or calendar year to stay in compliance with Internal Revenue Code Sub Chapter 
M or to prevent the possible imposition of an excise tax. 
When a fund declares a Special [[Dividend]], communication is key as these distributions are unscheduled and 
not known in advance by intermediaries. Typically, a [[Dividend]] Distribution Memo is created and sent through:  
• The MFPS II–Distribution Database or MF Info Xchange 
• In situations where usage of the [[DTCC]] products are not an [[Option]], a spreadsheet via ‘blast email’ to 
clients, service providers, and/or sub-accounting vendors to provide the detail about the expected 
distribution. From that point, the normal [[Dividend]] distribution process is followed with notification the 
day of the distribution through the MFPS II–Distribution Database and manual spreadsheets. For those 
firms with heightened reconciliation needs, i.e. Omnibus firms, timely notification is critical.  Funds 
should send notification of the Special [[Dividend]] as soon as it is declared. 
Because of the unique nature of these unplanned, unscheduled distributions, it is important that the [[Dividend]] is 
reported and accounted for correctly. Accordingly, it is imperative that key data points, including Record, 
Reinvest, and Payable dates are accurate. Additionally, if any portion of the distribution contains a return of 
capital to the shareholders, then a Section 19 letter must also be distributed.  

---

## Page 13

Best Practices - [[Dividend]] and Capital Gain Distributions 
Challenges for Firms 13 
CHALLENGES FOR FIRMS 
The [[Dividend]] and capital gain distribution process plays an instrumental role in ensuring accurate [[Dividend]] and 
capital gain payments and shareholder positions. The receipt, integration and application of [[Dividend]] and 
capital gain data requires the use of significant resources and complex processes, and relies heavily on the 
timeliness, accuracy, and consistency of the data. 
For [[intermediary]] firms, successful transmission of [[Dividend]] and capital gain information is of utmost 
importance. The communication between [[intermediary]] firms and vendors is critical to ensure that dividends 
and capital gains for all funds on a firm’s platform are properly transmitted. If the unique transmission 
constraints of an [[intermediary]] firm are not met, a [[Dividend]] or capital gain may have to be manually updated on 
their system with as-of information, introducing risk and added manpower. Consistent and reliable 
transmissions are critical to ensuring that dividends and capital gains post using current prices in a timely 
manner. 
Timeliness of Communication 
[[Dividend]] and capital gain transmission processes and calculation activities within [[intermediary]] firms are 
complex. These complexities are compounded by tight timeframes as [[Dividend]] and capital gain information is 
only a portion of the data included in end-of-day processing. Internal service levels make the timely receipt of 
[[Dividend]] and capital gain information even more critical, with delays carrying significant impacts ranging from 
resource costs (e.g., employees working longer hours, follow-up calls to funds & transfer agents) to processing 
errors (e.g., use of stale rates when nightly activities commence with inaccurate information) .  Adjustment 
processing carries with it yet another set of costs related to the coordination required to restore impacted 
shareholder accounts to the correct state. A firm’s internal service levels are further tested at year-end when 
higher volumes are the norm and capital gains are included in the daily processing.  
Delays in the receipt of [[Dividend]] and capital gain information can also have an impact on pricing of certain 
products, such as wrap and unitized products that are similar to fund-of-funds. With these products, a 
significant amount of work is required if prices are late and rates need to be manually loaded into the system 
prior to the [[intermediary]] firm’s nightly process. If this happens, these products have to strike an NAV without 
the accrual amount causing the NAV to be understated. If the NAV is understated by a large enough amount, it 
can result in rework to all shareholder transactions for the day. Further, if delays occur for an extended period 
of time without a communicated rate, error corrections are required and can cover several days. Extended 
delays can also impact the creation of client performance reporting, internal reports and, in some cases, tax 
forms. 
One of the main challenges faced is receiving a single batch from a third- party vendor. Any issues with the 
transmission results in a tremendous amount of manual [[Dividend]] and capital gain updates and adjustments to 
shareholder accounts. The adoption and utilization of automated resources, such as Mutual Fund Profile 
Services offered by the [[DTCC]], centralizes all [[Dividend]] and capital gain data into one reliable multi-cycle 
source, and can alleviate many of the challenges attributed to lack of timeliness in [[Dividend]] and capital gain 
transmissions. 
Accuracy of Data 
Inaccuracy of dates and rates can have significant impact to [[intermediary]] firms in the form of adjustments, 
which are risky and expensive actions on [[intermediary]] firms’ systems. For example, any shareholder 
withdrawal or [[liquidation]] before an inaccurate [[Dividend]] or capital gain is corrected must be corrected 
individually. Inaccuracies, adjustments, and delayed [[Dividend]] and capital gain payments are visible to clients 
and can also lead to reputational risk. Finally, internal systems will update based on what is received from the 
fund [[Companies]] via an automated intake process. If the data is incorrect, this will create a large number of 
adjustments and corrections to shareholder accounts. 
Events also occur when [[Dividend]] and capital gain information is not sent to [[intermediary]] firms, due to 
unanticipated challenges/issues at the Fund or [[transfer agent]]. In this case when no information is sent many 
issues arise. Dividends and capital gains are not reflected in shareholder accounts, as-of processing must 

---

## Page 14

Best Practices - [[Dividend]] and Capital Gain Distributions 
Challenges for Firms 14 
occur, and subsequent activity, terminations, and withdrawals must be manually adjusted so the activity is 
properly represented in the redemption of [[shares]]. These events can also complicate tax forms for 
shareholders. 
Consistency of Format & Terminology 
As [[Dividend]] and capital gain information is received by [[intermediary]] firms and incorporated into internal 
systems and applications, challenges related to the consistency of information are often experienced.  These 
situations often result in ‘breaks’ in the processes employed by [[intermediary]] firms related to reconciliation, 
[[settlement]], etc., and can result in the need for specialized or ‘one-off’ processes to accommodate the variety. 
General areas that often see variation include terminology and format of [[Dividend]] and capital gain information.  
Variation can also occur when Funds employ different methodologies related to the establishment or 
declaration of a [[Dividend]] or capital gain. For example, related to the practices of record date and [[Entitlement]], 
the general assumption is that shareholders who buy on record date are entitled to the [[Dividend]] or capital gain, 
and those who sell on record date are not. This approach, however, is not consistent across all fund 
[[Companies]], causing discrepancies and out of balances for firms. Similar observations have been made with the 
application of payable and ex-[[Dividend]] dates. 
Inconsistencies have also been noted in the reporting of [[Dividend]] and capital gain information on automated 
files received through the [[DTCC]]. For example, payable date reporting and calculated accruals information, 
critical to the payment and reconciliation processes, are not populated consistently by F unds on the 
Networking Activity files. 
Information received from Funds can vary in calculation methodologies, resulting in one-off processes, or 
general challenges as specialized approaches or communications are required to  integrate the required data 
into firm applications and processes. Integration of incoming data sources and formats can compound the 
already challenging operational environment. 
Omnibus Processing 
The proliferation of omnibus accounts has presented challenges surrounding the main premise that fund 
accounts and the underlying shareholders no longer maintain a one-to-one relationship. This lack of 
transparency has created an environment where information is delivered in aggregate yet  must be accounted 
for by firms at the individual account level, making the accuracy and timeliness of any [[Dividend]] or capital gain 
distribution of extreme importance. 
In order for [[intermediary]] firms to calculate and post dividends and capital gains to the underlying shareholders 
in omnibus accounts as expected, dates and rates must be delivered to the [[intermediary]] firm as precisely and 
soon as possible. Magnifying the importance of good information are outlier scenarios, such as when 
underlying individual accounts fully [[Liquidate]] their position resulting in cash dividends, or where an account is 
part of a wrapped product and further calculation must be done to strike an NAV.  Any errors or delays in 
transmission of [[Dividend]] or capital gain information can result in calculation discrepancies or latency of 
postings. This can lead to both financial and reputational risk, which can be damaging to all parties inv olved. 
Daily Accrual Processing 
Daily accrual funds have their own unique [[Dividend]] challenges. As the name indicates, daily accrual funds 
accrue a [[Dividend]] for its shareholders every day, based on a daily calculated accrual factor that is applied to a 
shareholder’s [[shares]] held each day. At the end of the accrual cycle, usually monthly, the daily accrued 
amounts are combined and paid as a single [[Dividend]] to the shareholder. The [[Dividend]] payment can take the 
form of a cash payment to the shareholder, or the [[Dividend]] can be re-invested in the fund to buy additional 
[[shares]]. 
As stated above, daily accrual funds present their own set of challenges when it comes to [[Dividend]] processing. 
Three of the main challenges related to daily accrual [[Dividend]] processing are: 
• Inflated accrual factors for weekends and holidays 

---

## Page 15

Best Practices - [[Dividend]] and Capital Gain Distributions 
Challenges for Firms 15 
• Fluctuating accrual cycle end dates 
• Posting rules for calculating income on transactions during the accrual cycle  
 
Inflated Accrual factors 
Shareholders in a daily accrual fund earn income for every day they hold [[shares]] in the fund, including weekend 
and holidays. The best practice is to send single, daily rates for each day of the weekend through Mutual Fund 
Profile I, which allows rates to be applied in the most straightforward manner. This approach is also 
recommended when operating during an Unexpected Market Close scenario, as outlined in the ‘ICI’s Mutual 
Fund Operations Planning Guide for an Unexpected Market Close’. 
It is understood, however that long standing common industry practices and methodologies within many Funds 
necessitate the distribution of an inflated factor to communicate weekend/holiday accrual rate information.  
These inflated factors are sometimes referred to as “fat” or “bulk rate” factors, using one aggregate figure to 
represent the period. 
There is a great deal of variety among fund company processes with regard to the communication of accrual 
rates, which can be observed in the following table. 
 
Accrual Rate Approach Normal Weekend Weekend/Holiday 
(which includes month-end) 
Single Rates Individual rates sent on Friday, for 
Friday, Saturday, and Sunday 
Same process as Normal weekend 
Inflated Rate Inflated rate sent on Friday, inclusive 
of Friday, Saturday, and Sunday 
Friday Inflated Rate Scenarios 
1. Same process as Normal weekend 
2. Split Inflated Rate: 
• Inflated Rate sent on Friday for days 
included in current accrual period 
• Additional single rate sent on Friday for 
day(s) that are part of the next accrual 
period 
3. Split Inflated Rate: 
• Inflated rate sent on Friday for days 
included in current accrual period. 
• Inflated rate sent on Monday for day(s) 
that are part of the next accrual period, 
including Monday’s rate 
Inflated rate sent on Monday, inclusive 
of Saturday, Sunday, and Monday 
Same process as Normal weekend 
 
Generally, during month-end scenarios, weekend accrual rates (both single and inflated) are applied to the 
position balance on the day received. An exception is noted, however with Inflated Rate>Split Inflated 
Rate>Scenario #2, as some Funds will apply the accrual rates from the new accrual period to the next 
business day’s share balance. In all cases, the receiving firm is responsible for allocating the rates to the 
appropriate accrual period. 
 
 

---

## Page 16

Best Practices - [[Dividend]] and Capital Gain Distributions 
Challenges for Firms 16 
Fluctuating Accrual Cycle End Dates 
Accrual cycles are generally monthly; but can also be quarterly. Additionally, accrual cycles can end on most 
any date, not only the last day of the month. Because of the varying processes by F und, communication of 
[[Dividend]] events by Funds is critical. Given the various methods and reasons for differing cycle end dates within 
each Fund, the likelihood of consensus on a standardized accrual cycle end date is not likely, and as such 
there is no best practice recommendation. 
Posting Rules for Calculating Income on Transactions during the Accrual Cycle 
Funds have differing rules as to when they pay income on transactions occurring during the accrual cycle. For 
example, some Funds will accrue income on purchases on [[settlement]] date and others will not accrue income 
on purchases until [[settlement]] +1 day. Different rules apply for purchases, redemptions, transfers, exchanges, 
etc. and every Fund has their own rules. This creates an enormous challenge for firms that have to accrue 
income every day on their sub omnibus accounts and [[participant]]’s accounts in retirement plans.  To aid in 
clarification of individual Fund accrual rules, the MFPS II – Security Database supports identification of a 
Fund’s daily accrual posting rules as to when various transaction types are entitled to start earning income or 
when they will stop earning income. It is strongly recommended that Funds maintain these rules within this 
service. 

---

## Page 17

Best Practices - [[Dividend]] and Capital Gain Distributions 
Challenges for Funds/Transfer Agents 17 
CHALLENGES FOR FUNDS/TRANSFER AGENTS 
The [[Dividend]] and capital gain distribution processes are a key part of Fund and [[transfer agent]]’s activities, with 
multiple steps and functions required to accurately and effectively communicate this critical data.  Robust 
technology, timely communication, strong oversight, and accuracy are critical to effective [[Dividend]] and capital 
gain distributions. This requires a significant amount of resources, both employee and financial, to support on a 
day to day basis, often requiring dedicated teams within many organizations . 
Quarter and year-end processes, special distributions, and communication about these events (i.e., anything a 
Fund triggered that [[intermediary]] firms didn’t expect) can compound the challenges that F unds face. When 
errors occur within the [[Dividend]] and capital gain distribution process, the pressure on resources of [[intermediary]] 
firms can also vary in many cases, resulting in one-off processes, or general challenges as specialized 
approaches or communications are required. 
Accuracy 
Among the concerns and challenges that Funds face when managing the [[Dividend]] and capital gain distribution 
process, accuracy perhaps plays the largest part. [[Dividend]] and capital gain information is a core component of 
shareholders’ records, and the Funds’ books and records. 
While the reasons for accuracy challenges are varied and differ by Fund, the risks that accompany these 
challenges remain consistent across the board. Financial risk is of the most concern, a misapplication of an 
accrual rate at year-end can have significant impact due to inaccurate payments and efforts to recoup the 
losses. The amount of effort and resources required when such errors occur are draining not only to the F und 
but to the [[intermediary]] firms that are involved. Costs borne by the [[intermediary]] firms to correct and reconcile 
after errors occur result in charge-backs or requests for compensation by the [[intermediary]] firms from Funds. 
Consistent errors, or recurring gaps in a Fund’s processing or communication of the distribution data, can 
result in a lack of trust-ultimately a reputational risk. Business risk may be realized when strategies and/or 
distribution of certain products and/or services suffer as a result of recurring [[Dividend]] and capital gain 
challenges. 
Timeliness 
Accurate information does not serve its purpose if not transmitted by Funds and transfer agents to the 
[[intermediary]] firms in a timely manner. Recent statistics show that there is still a considerable amount of data 
that does not reach the [[DTCC]] by the standard best practice time of 6:00 p.m. ET (MFPS II–Distribution 
Database, cycle 12). This can be for multiple reasons. Within many organizations, legacy systems and 
infrastructures make it difficult to effect large-scale changes to streamline internal processes and technical jobs 
to achieve the desired timing of distribution. Awareness within an organization of the criticality of [[Dividend]] and 
capital gain information to the end consumers is often not where it needs to be, which can compound the 
problem. 
As the industry has evolved, a greater number of functions at Funds are outsourced to third parties and 
external vendors. As the number of parties involved in the distribution of pricing, [[Dividend]] and capital gain 
information increase, additional stresses related to timeliness are experienced. 
When an external [[transfer agent]] is part of the relationship, this presents one more step, transmission, and 
consideration in an already complex and tight timeframe. 
Another challenge that can have an effect on timely delivery of [[Dividend]] and capital gain information is related 
to the specific data points included on the outbound [[Dividend]] and capital gain records.  Historically, [[Dividend]] 
and capital gain information was only released once all NAVs have been struck.  Changes recently to the 
[[DTCC]] MFPS II – Distribution Database records and related best practices have made the “Reinvest NAV” an 
optional field, as it is not critically tied to [[Dividend]] and capital gain distribution processes.  Within many Funds, it 
will require a significant change, an almost philosophical change in thinking in some cases, to release rates 
before the NAV is final. 

---

## Page 18

Best Practices - [[Dividend]] and Capital Gain Distributions 
Challenges for Funds/Transfer Agents 18 
As the dependence on timely delivery of [[Dividend]] and capital gain information grows, [[intermediary]] firms have 
taken steps to incorporate service level expectations into trading agreements or other forms of reporting. While 
this is an early observation, growing trend points to the significance and criticality of the data, and underscores 
the need for awareness and focus by the Funds. 
Product Distribution 
As the mutual fund product landscape evolves, additional emphasis and focus grows on the timeliness and the 
accuracy of [[Dividend]] and capital gain distribution information. Because of the complexity, wrap programs, and 
‘fund-of-funds’ products, for example, require additional processes and requirements which add to the already 
tight timeframes that [[intermediary]] firms work with each evening. A potential consequence to late and/or 
unreliable delivery of the [[Dividend]] and capital gain information is the inability or unwillingness for the F und’s 
products to be included in wrap programs or lineups. 

---

## Page 19

Best Practices - [[Dividend]] and Capital Gain Distributions 
DETAILED BEST PRACTICES - [[Dividend]] and Capital Gain Distributions 19 
DETAILED BEST PRACTICES - [[Dividend]] AND CAPITAL 
GAIN DISTRIBUTIONS 
Transmission of Distribution Information 
As stated earlier, it is strongly recommended that Funds and Firms leverage the automated options offered by 
[[DTCC]] to communicate and receive distribution information. These options, leveraging standard formatting and 
multi-cycle processes are listed below: 
• [[DTCC]]’s Mutual Fund Profile Service I (MFPS I) - Price and Rate service provides Funds with an 
automated solution for providing intermediaries with prices in the form of net [[Asset]] values (NAVs) and 
daily accrual rates (see ‘[[DTCC]] Mutual Fund Profile Service I Price & Rate User Guide/Best Practices’ for 
additional information on this service) 
• Mutual Fund Profile Service II (MFPS II) - Distribution Declaration service allows Funds to send declared 
distribution rates and corresponding dates (Ex, record, payable, etc.) to [[intermediary]] firms.  Funds also 
have the [[Option]] to send capital gain and [[Dividend]] calendars in advance in the form of ‘projected’ records.  
In addition to batch file transmissions, [[DTCC]] also provides the ability to submit MFPS II Distribution 
Declaration files through the [[DTCC]] Web portal*. 
• The MFPS II - Security Database allows Funds to maintain [[Dividend]] type, payment frequency and daily 
accrual income posting rules. 
• MF Info Xchange – Funds are advised to communicate their projected and actual monthly, quarterly and 
annual dates as well as estimated and actual rates (once rates become available). 
 
The MFPS II - Distribution Database should be the primary source for Fund delivery of actual and projected 
distribution information to firms. In situations where use of the [[DTCC]] services is not an [[Option]], [[Dividend]] and 
capital gain distribution information should be emailed by Funds to distribution partners leveraging the 
standardized calendar template (for Projected Distributions) and spreadsheet (for Actual Distributions). This 
template is available on Learning in MFPSII section https://dtcclearning.com/documents/mutual-fund-services-
1/mfpsii/guides-12/4139-distribution-calendar-template.html. 
*Note: 
[[DTCC]] currently provides the ability for Funds to upload projected and actual distributions through the [[DTCC]] Web Portal 
utilizing the existing variable MFPS II – Distribution Capital Gain (041) and [[Dividend]] (042) record formats.  For additional 
information on this feature please contact your Wealth Management Relationship Manager.  In addition to currently 
providing the ability to upload a projected distribution record layout via the MyDTCC Web Portal.  
 
Best Practices for the transmission of [[Dividend]] and capital gain distribution information through the [[DTCC]] are 
outlined below. 
[[DTCC]] 
Service 
Scenario Best Practice – Actual Periodic Distributions 
Mutual Fund Profile II–
Distribution Declaration 
Database 
Timing of ‘Actual’ [[Dividend]] and 
Capital Gain information leveraging 
the [[DTCC]] MFPS II Capital Gain 
(041) and [[Dividend]] (042) 
Records. 
• Funds and [[transfer agent]] providers should make every effort to 
transmit all available distribution information to [[DTCC]] by 6:00 pm ET, 
or Cycle 12, on Ex-Date. 
• If necessary, any remaining distribution data should be forwarded as 
soon as the information is available.  
 
Important Note: 
Funds should not hold the transmission until all distribution data is 
gathered but transmit data as it becomes available. The [[DTCC]] MFPS 
II Distribution service does provide the ability for clients to submit 

---

## Page 20

Best Practices - [[Dividend]] and Capital Gain Distributions 
DETAILED BEST PRACTICES - [[Dividend]] and Capital Gain Distributions 20 
  
[[DTCC]] 
Service 
Scenario Best Practice – Actual Periodic Distributions 
input files until 10:00 p.m. (cycle 98).  However, the later cycles are 
intended to be used for corrections or for passing data previously 
unknown. 
 
Mutual Fund Profile II–Distribution Declaration 
Database 
Using the Capital Gain (041) and 
[[Dividend]] (042) Records to 
communicate ‘Actual’ periodic 
distribution information  
• ‘Action Type’ Indicator field should be populated with an ‘A’ = add 
record for initial distribution information (see ‘Communications of 
Errors or Corrections’ section for information on corrections of 
[[Dividend]] and capital gains previously communicated by Funds) 
• The ‘Projected/Actual Indicator’ field should be populated with the 
value = 1 (Actual) 
• In the case of Special Dividends, the Distribution Indicator on the 042 
Record should be populated with the value ‘5’ (Special). 
• File layouts should be regularly reviewed to ensure that attention is 
paid to required and/or optional fields 
o Both NAV and distribution information should be sent when 
available, with no dependencies on availability of each 
component. 
o The ‘Reinvest Price’ field is an optional data point; it is 
recommended that Funds proceed with the transmission of 
distribution data without waiting for NAVs to be finalized. 
NAVs should be transmitted separately as soon as they 
become available via the MFPS I Price and Rate service. 
• “Reinvest Price” for distributions should only be provided if the 
Reinvest Price differs from the Ex-Date price. 
Mutual Fund Profile I–
Price and Rate Using the Price and Rate Record 
(030) to communicate ‘Actual’ 
periodic distribution information 
• Because reconciliation needs vary by client, Funds may also use 
Record 030 within Mutual Fund Profile I to populate information 
specific to the periodic distribution, including the rate and effective 
date. 
• This information should be included on Ex Date 
Mutual Fund Profile II–Distribution 
Declaration Database 
Handling an Unexpected Market 
Close scenario (Periodic 
Dividends) 
If the record date occurs during an unexpected market close (UMC) 
situation: 
• The industry practice is to [[default]] to the Funds’ first business day 
following the UMC event. 
• Related dates, i.e. ex-date and payment date/reinvestment date(s) 
should be adjusted based on the changes to the record date. 
(For additional information on UMC practices, see section “ICI Mutual 
Fund Operations Planning Guide for an Unexpected Market Close”) 

---

## Page 21

Best Practices - [[Dividend]] and Capital Gain Distributions 
DETAILED BEST PRACTICES - [[Dividend]] and Capital Gain Distributions 21 
Mutual Fund Profile II–Distribution Declaration Database 
Using the Capital Gain (041) and 
[[Dividend]] (042) Records to 
communicate Projected [[Dividend]] 
and capital gain information 
Funds and [[transfer agent]] providers are encouraged to communicate 
projected periodic distribution dates to the firms as soon as the capital 
gain or [[Dividend]] calendar is finalized (it is understood that advance 
notice may not be available for capital gain information). This ‘projected’ 
data on future distributions is intended to notify [[intermediary]] firms of 
anticipated record and ex dates, not estimated rates. Firms have 
indicated they require projected information at minimum 72 hours in 
advance of the actual rate information. 
 
Through MFPS II - Distribution Database Service: 
• The ‘Action Type’ Indicator field should be populated with an ‘A’ = 
add record for initial distribution information 
• Enter/Update Distribution dates in the Record Date and Ex-Date 
fields on or prior to Record date  
• ‘Projected/Actual Indicator’ field should be populated with a value 
of ‘0’ (Projected) 
 
Important Note: If a previously submitted projected distribution is 
no longer going to pay a [[Dividend]] or capital gain, the Fund should 
send a zero rate with the “Projected/Actual Indicator” of ‘1’ (Actual) 
on Ex-date. 
Timing of records is recommended as follows: 
Timing for Communicating 
Projected Distribution 
Information 
Best Practice Utilizing the 
041 and 042 Records 
From first date available 
through 72 hours prior to Ex-
Date 
Send Projected indicator and 
Record and Ex-dates 
On or before Ex-date if 
distribution will be paid on a 
different date than originally 
communicated 
Send Change Record with 
Projected indicator and Ex-date 
On Ex-date if a projected 
distribution was communicated 
but will no longer be paid 
Send record with 
‘Projected/Actual Indicator’ =  
“1”  (Actual) and populate a “0” 
rate. 
 
  
[[DTCC]] 
Service 
Scenario Best Practice – Projected Periodic Distributions 

---

## Page 22

Best Practices - [[Dividend]] and Capital Gain Distributions 
DETAILED BEST PRACTICES - [[Dividend]] and Capital Gain Distributions 22 
 
Mutual Fund Profile II–Security Issue Database 
Using the MFPS II - Security 
Issue Database (020) Record to 
Communicate Daily Accrual 
Posting Rules 
 
 
 
 
 
 
 
 
 
 
 
 
Note: 
An enhancement to expand the 
Bulk Rate Month-End Method 
Codes will be evaluated by the 
[[Dividend]] Distribution Task Force 
to ensure all approaches used 
with Inflated rates are captured. 
Funds should include details related to daily accrual communication 
and handling in the MFPS II - Security Issue Database for each 
applicable fund to aid in reconciliation and accurate processing of 
dividends. Using Record 20, Funds should populate the following fields 
as indicated: 
 
Posting Rules: 
To illustrate the funds daily accrual posting rules, Funds should 
populate the following: 
• [[Dividend]] Accrual Exchange Start Date Code 
• [[Dividend]] Accrual Exchange Stop Date Code 
• [[Dividend]] Accrual Full Transfer Start Date Code 
• [[Dividend]] Accrual Partial Transfer Start Date Code 
• [[Dividend]] Accrual Transfer Stop Date Code 
• [[Dividend]] Accrual Purchase Start Date Code 
• [[Dividend]] Accrual Redemption Stop Date Code 
 
Bulk Rate Method Code: 
On a normal weekend, Funds should populate the fields below 
accordingly: 
 
Bulk Rate Scenario Bulk Rate Method Code 
Inflated Rate sent on Friday 0–Prior Business Day 
Inflated Rate sent on Monday 1–Next Business Day 
[[DTCC]] 
Service 
Scenario Best Practice – Communicating Accrual Posting Rules 

---

## Page 23

Best Practices - [[Dividend]] and Capital Gain Distributions 
DETAILED BEST PRACTICES - [[Dividend]] and Capital Gain Distributions 23 
  
Bulk Rate Month-End Method Code: 
On a weekend that includes a month-end and/or business holiday, 
fields should be populated as outlined below:  
Inflated Rate Scenario: Bulk Rate Month-End Method 
Code 
Inflated Rate for full weekend 
sent on Friday 
0–Prior Business Day 
Inflated rate for the full weekend 
and Monday sent on Monday 
1–Next Business Day 
Inflated Rate for current accrual 
period sent on Friday, 
accompanied by single rate for 
day(s) of the next accrual period 
2–Split prior/Next Business Day 
Inflated rate for current accrual 
period sent on Friday; inflated for 
day(s) of next accrual period on 
Monday, accompanied by 
Monday’s rate 
2–Split prior/Next Business Day 
 
Mutual Fund Profile I–Price and 
Rate 
Using the MFPS I - Price and 
Rate Record (030) to transmit 
Daily Accrual Information 
When operating normally, Funds currently communicate two types of 
accrual factors for daily accrual funds via [[DTCC]]’s Mutual Fund Profile I 
Price & Rate service: 
• A single rate for each day of the weekend/holiday. 
• In the case of weekends or certain holidays, an inflated, or multi-day 
rate, is sent to cover that period. 
In scenarios where Funds utilize an inflated rate, it is important that 
related fields in Mutual Fund Profile II Security Issue Database are 
populated so receiving firms understand the content of inflated rate and 
month-end accrual details (see Mutual Fund Profile II–Security Issue 
Database 020 Record for information). 
Mutual Fund Profile I–Price and Rate Handling an Unexpected Market 
Close scenario 
(Daily Accrual Dividends) 
In the case of a UMC event, the common fund industry practice for 
[[Dividend]] accrual activity is as follows: 
• Fund [[Companies]] should deliver single rates for each day during the 
UMC and follow their normal multi-rate procedures when one or 
more normal non-business days (i.e. weekends, certain holidays) 
are encountered. 
• Funds should provide a daily rate for all open and closed funds. 
 
(For additional information on UMC practices, see  the “ICI Mutual Fund 
Operations Planning Guide for an Unexpected Market Close”) 

---

## Page 24

Best Practices - [[Dividend]] and Capital Gain Distributions 
DETAILED BEST PRACTICES - [[Dividend]] and Capital Gain Distributions 24 
Special Dividends 
Upon the declaration of a Special [[Dividend]], Funds should communicate the available details promptly to 
trading partners and service providers.  
Scenario Best Practice 
Communicating Expected Special [[Dividend]] 
information 
• Because there is limited notice of a Special [[Dividend]] declaration, Funds 
should send an announcement via press release or blast email of the 
upcoming [[Dividend]] event to distribution partners. 
• If information about a Special [[Dividend]] is available prior to Ex Date, 
Funds should send Record 042 with a ‘Projected’ indicator. 
Communicating ‘Actual’ Special [[Dividend]] 
information 
• On Ex Date, using Record (042) of MFPS II–Distribution Database, 
Funds should populate the ‘Distribution Indicator’ field with a 5 (Special) 
along with the actual rates. 
• Also, on Ex-date, Funds should publish an announcement of the [[Dividend]] 
to include the required dates, such as Record, Ex, Reinvest, and Payable 
dates, as well as the actual rate. This announcement/memo can be made 
by a Fund’s standard communication method, including press release or 
blast email. 
 
Communication of Errors or Corrections 
As discussed, accuracy of data related to distributions is critical to the process. When breaks or errors [[DO]] occur 
and incorrect rate information is transmitted or communicated to [[intermediary]] firms, timely and expeditious 
communication, by both systematic and manual means, is key. The best practices below illustrate the steps 
Funds should take when errors are realized. 
Action  Best Practice 
Step 1: Communicate to trading partners 
and service providers 
• Upon identification of an error, Funds should immediately notify trading 
partners and service providers via standard communication methods, 
including email, phone calls, and/or updated distribution 
memos/spreadsheets. 
• Communication should include updated distribution information, with all 
key fields included. 
Note: 
If account corrections are required, Funds should include the corrective steps 
being taken (i.e. cancel/rebook of [[Dividend]] or share adjustments) in 
communications. This is an essential piece of information for firms. 

---

## Page 25

Best Practices - [[Dividend]] and Capital Gain Distributions 
DETAILED BEST PRACTICES - [[Dividend]] and Capital Gain Distributions 25 
Action  Best Practice 
Step 2: Send Change records through 
[[DTCC]] (on Ex Date only) using the Capital 
Gain (041) and [[Dividend]] (042) Records 
If the error is identified on Ex Date, Funds that leverage the [[DTCC]] services 
should take the following steps once initial communication efforts have 
begun: 
• Submit a Change record to modify existing data that has been 
transmitted. 
• Populate the ‘Action Type’ field with a value of ‘C’ = Change. 
• Change records may be submitted for projected or actual distributions. 
• An “Action Type’ indicator of ‘Change’ should not be delivered to the 
firms after Ex Date. 
 
Important Note:  A “Change” should not be delivered to the firms after Ex 
Date.  If the error is identified after Ex Date, Funds should follow the 
communication guidelines outlined in Step 1; information should not be sent 
through the [[DTCC]]. 
 
As previously referenced, it is strongly recommended that Funds transmit projected and actual [[Dividend]] and 
capital gain information through the [[DTCC]]. In situations where this is not possible, refer to the following best 
practices for the communication of distribution information through manual processes.  
Scenario Best Practice 
Communicating Projected Distribution 
Information 
• In early January, Funds should publish a distribution calendar, which 
should include all periodic distributions to be paid. This calendar can be a 
yearly version (with all projected dates for the year included) or sent to 
partner firms monthly with information included for the upcoming month. 
• The standardized calendar template should be leveraged, which includes 
the following key values: 
o Security Description (Fund Name & Class) 
o Security Issue [[ID]]  
o Ticker 
o Fund Number 
o Fund Company [[NSCC]] # 
o Change Indicator 
o Distribution type 
o Record Date 
o Ex-Date  
o Reinvest Date 
o Payable Date 
 
Note: Date Formats should be ccyymmdd 
 
The standardized calendar template is available on Learning in MFPSII 
section https://dtcclearning.com/documents/mutual-fund-services-
1/mfpsii/guides-12/4139-distribution-calendar-template.html. 
 
Communicating Actual Distribution 
Information 
• On Ex-date, Funds should publish an announcement of the distribution to 
include the required dates, such as Record, Ex, Reinvest, and Payable 
dates, as well as the actual rate. 
• This announcement/memo can be made by a Fund’s standard 
communication method, including press release or a blast email to 
distribution partners. 

---

## Page 26

Best Practices - [[Dividend]] and Capital Gain Distributions 
Best Practices – Summary of Key points 26 
BEST PRACTICES – SUMMARY OF KEY POINTS  
 
The following outlines key points for communicating projected and actual periodic distributions 
through [[DTCC]]’s MFPS II – Capital Gain (041) and [[Dividend]] (042) Distribution records 
 
Communication of 
Projected Distribution 
information 
 
• Funds and [[transfer agent]] providers are encouraged to communicate projected 
periodic distribution dates to firms as soon as the capital gain or [[Dividend]] calendar 
is finalized through the [[DTCC]]. 
• Projected data is to notify Firms of anticipated Record and Ex-date, not estimated 
rates. 
• Firms have indicated they require projected information at minimum 72 hours in 
advance of the actual rate information. 
• Immediate communication by Funds to shareholders and partner firms is recommended 
when special [[Dividend]] declarations occur. 
• If a previously submitted distribution for a fund is no longer going to pay a [[Dividend]] or 
capital gain, the Fund should send a zero rate with the “Projected/Actual Indicator” of 
‘1’ (Actual). 
 
Communication of 
Actual Distribution 
information 
 
• Transmission of final distribution information should be sent to [[DTCC]] on Ex-date, by 
6:00 p.m. ET (Cycle 12). 
• The ‘Reinvest Price’ field is an optional data point; it is recommended that Funds 
proceed with the transmission of distribution data without waiting for NAVs to be 
finalized. NAVs should be transmitted separately as soon as they become available 
via the MFPS I Price and Rate service. 
• The Reinvest Price should only be provided if it differs from the Ex-Date price. 
• In the case of Special Dividends, the Distribution Indicator on the 042 Record should 
be populated with a value of ‘5’ (Special). 
 
 
Corrections to Actual and 
Projected Distributions 
 
• Upon identification of an error, Funds should immediately notify trading partners and 
service providers via standard communication methods, including email, phone calls, 
and/or updated distribution memos/spreadsheets.   
• Communication should include updated distribution information, with all key fields 
included. 
• If the error is identified on or before Ex Date, once initial communication efforts have 
begun, Funds that leverage the [[DTCC]] services should also submit a “Change” 
record to modify existing data that has been transmitted, by populating the ‘Action 
Type’ field
 with a value of ‘C’ = Change.  A “Change” record should not be 
transmitted to the firms after Ex Date. 
 
 
 

---

## Page 27

Best Practices - [[Dividend]] and Capital Gain Distributions 
Commonly Used Terms 27 
COMMONLY USED TERMS 
Distributions 
When Funds make distributions of their gains to shareholders, the gain either is classified as an ordinary 
[[Dividend]] or as a capital gain [[Dividend]]. When the distribution is a capital gain [[Dividend]], then it is further broken 
down into one of the five types of capital gains as defined in the Internal Revenue Code.  
• Mutual Fund Capital gains differ entirely than Equities as the duration is not based on how long a 
shareholder has held the security, but rather is based on how long the particular underlying [[securities]] 
making up the Mutual Fund portfolio were held before they were sold for a profit.  
• Long Term: Profits made from the sale of underlying [[securities]] held for 12 months or longer. Taxed at the 
capital gains rate established by the IRS based on a shareholder’s tax bracket. 
• S hort Term : Profits made from the sale of underlying [[securities]] held for less than 12 months. Taxed the 
same as the shareholder’s ordinary income rate. 
• The following three capital gain indicators are fairly rare for mutual fund distributions but they can occur on 
certain funds. 
• Gain on collectibles: Profits made from the sale of collectibles, such as rare art or stamps. The tax rate 
on this type of gain is 28%. 
• S ection 1202 Gain : Profits from the sale of qualified small business [[Stock]]. Based on meeting certain 
criteria to be a qualified small business [[Stock]] and meeting certain holding periods, up to 100% of these 
gains may be excluded from income. 
• U
nrecaptured Section 1250 Gain : When depreciable real estate is sold, that portion of the gain 
attributable to a reduction in the original cost basis because of depreciation is not considered a capital 
gain. It is considered a recapture of prior depreciation and is taxed at an individual’s regular tax rate but 
not more than 25%. 
Declaration Date: The date a Fund’s Board of Trustees announces the amount of the [[Dividend]] and/or capital 
gains to be paid to clients: record, reinvest, payable, and calculation dates established. 
Excise Tax: Regardless of a fund’s fiscal year-end, all funds must make required income distributions based 
on a calendar year and capital gain distributions based on an October 31 year-end. Failure to distribute the 
required amounts under the excise rules results in a 4% excise tax. 
Ex-[[Dividend]] Date (Ex-Date): The date on or after which a security is traded without a previously declared 
[[Dividend]] or distribution. It is also the day which the price of the security decreases by the amount of the 
declared [[Dividend]] (rate). The Ex-[[Dividend]] term can be applicable to Dividends or Capital Gains. 
Foreign Tax Credit: A non-refundable tax credit for income taxes paid to a foreign government as a result of 
foreign income tax withholdings. The foreign tax credit is available to anyone who either worked in a foreign 
country or has investment income from a foreign source. 
Payable Date: This is day the shareholders will receive the [[Dividend]] if they elect to receive their dividends in 
cash. For Periodic [[Dividend]] paying funds, Payable date will either be the same as Ex and Reinvest date, or it 
will be the day after Ex and Reinvest date. In either case, the cash will generally be available the same day 
(the day after Ex date.) There are isolated exceptions to the handling of Payable dates but are very few. 
Periodic [[Dividend]] (Income [[Dividend]]): A type of [[Dividend]] that is earned based on [[shares]] held on a 
predetermined date (known as record date). Periodic Dividends can pay monthly, quarterly, semi -annually, or 
annually. 
Qualified Interest Income: Income that may be exempt from U.S. withholding tax on foreign accounts. The 
Internal Revenue code permits a regulated investment company (RIC) to designate distributions of qualified 
interest income and short-term capital gains as exempt from U.S. withholding tax when paid to non-U.S. 
shareholders with proper documentation. 

---

## Page 28

Best Practices - [[Dividend]] and Capital Gain Distributions 
Commonly Used Terms 28 
Reclassification [[Dividend]]: The process of changing the type of a mutual fund [[Dividend]] or capital gain once 
certain requirements have been met (i.e. income [[Dividend]] to capital gain). Reclassifications are typically not 
considered to be a taxable event. 
Record Date: The date which determines whether shareholders are entitled to the declared [[Dividend]].  
Typically, shareholders who buy on the Record Date are entitled to the [[Dividend]], and shareholders who sell on 
Record Date are not. 
Reinvestment Date: The date which the NAV is used to purchase additional [[shares]] for shareholders electing 
to reinvest their earned [[Dividend]]. For Periodic [[Dividend]] paying funds, this can vary, but is typically the day after  
RECORD date for [[Mutual Funds]]. 
Reinvest Price: The NAV used to buy additional [[shares]] with the [[Dividend]] earned.  
Special [[Dividend]]: A non-recurring [[Dividend]] or distribution. Also known as an Extra [[Dividend]]. In general, 
special distributions are usually related to the excise and Sub M distribution requirements and are made for the 
purpose of avoiding fund level tax and possibly complying with qualification requirements for [[Mutual Funds]].  
Spillover [[Dividend]]: A [[Dividend]] from a prior year's income or capital gains after the close of a taxable year.  
Also known as a spillback [[Dividend]]. 
 
Daily Accrual Dividends 
Accrual [[Dividend]]: A type of [[Dividend]] that is earned based on a daily rate (daily rate) * ([[shares]] held) = daily 
[[Dividend]] amount ($). The daily [[Dividend]] earned accumulates until the end of Accrual Period.  
Accrual Period: Comprised of a start and end date for which dividends are earned. The payable date is 
generally the day after the end of the accrual period. (Generally, this is based on a calendar month, but an 
accrual period can start and end mid-month or be quarterly). 
AM/PM Rules: These rules, determined by the Fund company, dictate when dividends will begin or stop 
accruing, following a purchase or redemption. 
While most often applicable for accrual funds, there are some situations, where similar rules apply to period ic 
dividends. In general, dividends earned are based on the record date closing share balance. For a few F und 
[[Companies]], however, the payment is based on the beginning balance on record date, resulting in an AM 
assessment, vs a ‘closing balance’ or PM assessment. 
Bulk Rate: Also known as fat or inflated rate, the combined rate used to reflect separate accrual rates for 
weekend days. Fund [[Companies]] may choose to send inflated accrual rates on Fridays (composed of Friday, 
Saturday and Sunday’s rates) and days that precede holidays (composed of the current day as well as the 
holiday’s rate) instead of sending individual daily rates for each non-business day. 
Cumulative Rate: The Cumulative accrual rate is the sum of all the daily accrual rates within the Accrua l 
Period. Shareholders owning Accrual [[Dividend]] paying funds are not automatically entitled to the Cumulative 
Rate; only those making no changes to their share balance for the duration of the Accrual Period.  
Reinvestment (Calculation) Date: For Accrual paying funds, this is the last day of the Accrual Period and the 
date for which reinvested [[shares]] are purchased at NAV (Net [[Asset]] Value). 
Payable Date: For accounts with a ‘cash’ [[Dividend]] [[Option]], this is the day the shareholders will receive the 
[[Dividend]]. For accrual [[Dividend]] paying funds, this is typically the day after the accrual period ends.  Unlike 
periodic dividends, there is no one record date or ex-date for accrual paying dividends; each day is essentially 
a record date. 

---

## Page 29

Best Practices - [[Dividend]] and Capital Gain Distributions 
Appendix 29 
APPENDIX 
• The Transmission Schedule for Mutual Fund Profile II – Distribution Declaration service can be found on 
the Learning Center (Login Required) at https://dtcclearning.com/products-and-services/mutual-fund-
services/schedules.html 
• Unexpected Market Close Guidelines - The ICI’s Mutual Fund Operations Planning Guide for an 
Unexpected Market Close can be accessed at https://www.ici.org/pdf/14_ops_manual_marketclose.pdf 
(Login Required). 
• Projected Distributions - Calendar Template (includes the template and a separate instructions tab) is 
available on Learning in MFPSII section https://dtcclearning.com/documents/mutual -fund-services-
1/mfpsii/guides-12/4139-distribution-calendar-template.html 
 
 
 
 

---

## Page 30

 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation [[DTCC]].  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
Doc Info: November 22, 2023 
Publication Code: MFS348 
Service: Mutual Fund Profile Service II 
Title: Best Practices – [[Dividend]] and Capital Gain Distributions 
For More Information 
 
Email Core Learning Service at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 