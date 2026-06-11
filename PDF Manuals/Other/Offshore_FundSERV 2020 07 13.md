---
title: "Offshore Fund/SERV Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Offshore_FundSERV%202020%2007%2013.pdf"
pages: 76
size: "1127.9 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Offshore Fund/SERV Guide

**Original File:** [Offshore_FundSERV 2020 07 13.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Offshore_FundSERV%202020%2007%2013.pdf)  
**Category:** Other  
**Total Pages:** 76  
**File Size:** 1127.9 KB  

---

## Page 1

 
 
 
 
U S E R G U I D E 
 
 
 
 
 
 
 
 
 
 
 
MutualFundServices 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 


---

## Page 2

 
 
 
Copyright 2004 National [[securities]] Clearing Corporation. All Rights Reserved. 

---

## Page 3

  April 2004   
i 
 
  
 
 
 
Contents   
 
1. Introduction ....................................................................................................................................... 1 
Multi-Currency Trading and External [[settlement]] ...................................................................... 2 
Holiday Calendars ............................................................................................................... 2 
Forward Dating................................................................................................................... 2 
2. Contact Information ............................................................................................................ 4 
3. A Note on Terminology ........................................................................................................ 5  
Mutual Fund Industry Terminology ........................................................................................ 5 
Fund/SERV® Terminology..................................................................................................... 5 
4. Security Types ................................................................................................................... 7 
Domestic Security Types ...................................................................................................... 7 
Offshore Security Types ....................................................................................................... 7 
5. Multi-Currency for Luxembourg and Dublin Funds .................................................................... 9 
“Single [[CUSIP]]/Single Currency” Funds ................................................................................... 9 
“Pseudo NAV” Funds............................................................................................................ 9 
“Pseudo Classes of [[shares]]” Funds ........................................................................................10 
Frequently Asked Questions ................................................................................................10 
6. Multi-Currency Setup (Fund [[Companies]]) ...............................................................................13 
Selecting a Currency .......................................................................................................... 13 
Standard Instructions for Choosing and Submitting Profile Forms .............................................14 
7. Multi-Currency Processing ...................................................................................................15 
Distributors: Submitting a Trade ..........................................................................................15 
Fund Company Processing ...................................................................................................15 
Security Type Mismatches ...................................................................................................15 
8. Changes to Record Layouts (Multi-Currency and Forward Dating) .............................................16 
New Fields ........................................................................................................................16 
Change to Existing Field ......................................................................................................16 
9. Holiday Calendars ..............................................................................................................17 
Why Holiday Calendars?......................................................................................................17 
How [[DO]] Holiday Calendars and Multi-Currency Work Together? ................................................17 
How [[DO]] Holiday Calendars and Forward Dating Work Together? ...............................................17 
10. Setting Up Holiday Calendars (Fund [[Companies]] Only) .............................................................19 
[[NSCC]] Processing ...............................................................................................................19 
Analyzing [[CUSIP]] and [[participant]] Levels .................................................................................20 
Calendar Setup Worksheet ..................................................................................................22 
11. Holiday Calendars on PCWeb Direct: Fund Usage Only ...........................................................27 
Web Interface ................................................................................................................... 27 
Accessing Calendar Functions ..............................................................................................28 
Creating a Calendar ...........................................................................................................29 
Assigning a Calendar ..........................................................................................................31 

---

## Page 4

  April 2004   
ii 
 
  
Editing a Calendar .............................................................................................................36 
Deleting a Calendar............................................................................................................41 
12. Holiday Calendars on PCWeb Direct: [[participant]] and [[NSCC]] Usage .............................................43 
Web Interface ................................................................................................................... 43 
Browsing via PCWeb Direct .................................................................................................43 
13. Using Holiday Calendars (without Forward Dating) .................................................................48 
Distributors—Entering a Trade .............................................................................................48 
[[NSCC]]—Trade Date Editing and Verification ............................................................................48 
[[NSCC]]—[[settlement]] Date Processing ......................................................................................48 
Fund [[Companies]]—Confirming the Trade ................................................................................49 
[[settlement]]........................................................................................................................50 
14. Forward Dating..................................................................................................................51 
Why Forward Dating? .........................................................................................................51 
15. Setting Up Forward Dating ..................................................................................................53 
Fund [[Companies]]—Choosing Security Types ...........................................................................53 
Fund [[Companies]]—Setting Forward Dating Permissions............................................................53 
Standard Instructions for Choosing and Submitting Profile Forms .............................................54 
Distributors—Coding Trade Entries .......................................................................................54 
16. Using Forward Dating (without Holiday Calendars) .................................................................55 
Distributors—Entering a Trade .............................................................................................55 
[[NSCC]]—Trade Date Editing and Verification ............................................................................55 
[[NSCC]]—[[settlement]] Date Processing ......................................................................................55 
Fund [[Companies]]—Confirming the Trade ................................................................................55 
[[settlement]]........................................................................................................................56 
17. Using Holiday Calendars and Forward Dating Together............................................................57 
Distributors—Entering a Trade .............................................................................................57 
[[NSCC]]—Trade Date Editing and Verification ............................................................................57 
[[NSCC]]—[[settlement]] Date Processing ......................................................................................58 
Fund [[Companies]]—Confirming the Trade ................................................................................58 
[[settlement]]........................................................................................................................58 
18. Scenarios: Using Holiday Calendars and Forward Dating Together ............................................59 
Scenario 1: Security Type 62, Forward Dating, No Holidays .....................................................60 
Scenario 2: Security Type 62, Forward Dating, [[settlement]] Holidays..........................................61 
Scenario 3: Security Type 62, Forward Dating, Holiday Anticipated by Distributor .......................62 
Scenario 4: Security Type 63, Forward Dating, No Holidays .....................................................63 
Appendix A: Glossary...............................................................................................................64 
Appendix B: Converting to Security Types 62 and 63 ...................................................................66 
Frequently Asked Questions ................................................................................................66 
Appendix C: About [[NSCC]] Mutual Fund Products & Services ...........................................................69 
Fund/SERV ....................................................................................................................... 69 
Mutual Fund Profile Service (MFPS): Price & Rate ...................................................................69 
Networking .......................................................................................................................69 

---

## Page 5

  April 2004   
ii 
 
 
 
Commission [[settlement]] ......................................................................................................70 
Appendix D: Obtaining a Digital Certificate for Offshore Fund/SERV................................................71 
 
 
 
 
LEGAL DISCLAIMER 
The functions described in this user guide address the November 2002 enhancements made only to the 
Fund/SERV® system to process offshore trading. These functions are not applicable to other [[NSCC]] 
Mutual Fund Products (Mutual Fund Profile Service, Networking, Commission [[settlement]]). Any non- 
U.S. dollar activity sent through the Networking or Commission [[settlement]] services by the fund that 
triggers a [[settlement]] exposure will be calculated by [[NSCC]] as part of the fund’s daily [[settlement]] 
obligation in U.S. dollars and will be the liability of the fund. 

---

## Page 6

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 1 
 
 
 
 
 
 
1.
Introduction   
 
 
Early in 2002, [[NSCC]] Mutual Fund Services began an assessment of “offshore funds” that were being 
traded and reported through the core [[NSCC]] products: 
 
• Fund/SERV 
• Profile Price & Rate File 
• Networking 
• Commission [[settlement]] 
 
In interviews and meetings with clients, [[NSCC]] recognized a general pattern: 
 
 
Offshore funds based in the Caribbean (for example, Cayman Islands) or Bermuda generally 
traded and reported with no exception processing. 
 
Funds based in Ireland or Luxembourg (known in Europe as “cross-border” funds), on the 
other hand, experienced several operational difficulties with [[NSCC]]’s products, due to 
differences in time zones, process cycles, holidays, and currencies. 
 
[[NSCC]] responded with a two-part initiative: 
 
 
• In June of 2002 [[NSCC]] created the OFS Working Group—an advisory body of [[Broker]]/dealers, funds, 
and third party service providers all interested in streamlining the servicing of “cross-border” funds 
sold via U.S. [[Broker]]/dealers. The OFS Working Group and its various task forces completed          
its analysis in February of 2003. 
• As the OFS Working Group analyzed operational issues, [[NSCC]] launched its first product 
enhancement for “offshore funds” in November of 2002 for mainframe processing systems. 
Enhancements to its web-based system, PCWeb Direct, went live in March of 2003. 
 
The November 2002 and March 2003 enhancements were first steps towards reducing exception 
processing and manual workarounds for Luxembourg and Dublin funds sold via U.S. [[Broker]]/dealers. 
Since the enhancements were established before a considerable portion of the OFS Working Group 
analysis was in place, they were never intended to be a complete solution. 
 
The November 2002 and March 2003 product enhancements are the subject of this user 
guide. 
 
Once the OFS Working Group analysis was complete in the winter of 2003, [[NSCC]]’s Product 
Management and Information Technology staff began to develop solutions that would complete 
straight-through processing (STP) and straight-through reporting (STR) for offshore funds and 
distributors. As of July of 2003, the solutions had been defined, and implementation will take place in 

---

## Page 7

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 2 
 
 
 
 
 
2004 and 2005. These solutions will not be built as an extension to [[NSCC]]’s core products, because to 
solve fully the issues of multi-currency, multi-time zone and processing cycle, substantially new 
capabilities must be created. 
 
This user guide explains the November 2002 and March 2003 product releases that will be used to 
process offshore funds until a more complete solution is rolled out in 2004 and 2005. [[Companies]] that 
wish to continue using the current core system can elect to [[DO]] so. As newer solutions reach the 
market, they will be available to all participants. Some new programming will be required. The new 
solutions will have up-to-date user guides describing the new functionality. 
 
The functions described in this user guide are relevant to Fund/SERV only, not to the other [[NSCC]] 
mutual fund products (Profile Price & Rate File, Networking, and Commission [[settlement]]). They are: 
 
• Multi-Currency Trading and External [[settlement]] 
• Holiday Calendars 
• Forward Dating 
 
MULTI-CURRENCY TRADING AND EXTERNAL [[settlement]] 
[[NSCC]] will allow fund [[Companies]] to accept and confirm mutual fund trades of Security Types 62 and 63 
in euros and other currencies, with [[settlement]] outside of [[NSCC]]. (Security Types 62 and 63 are new 
security types added as part of the November 2002 and March 2003 enhancements.) 
 
HOLIDAY CALENDARS 
In the U.S. market, fund [[Companies]] and distributors typically share the same business holidays. For 
most holidays, the markets are closed for both trading and [[settlement]]; for some holidays such as 
Columbus Day, markets are open for trading but closed for [[settlement]]. However, Luxembourg and 
Dublin fund [[Companies]], as well as the banks in which their trades settle, may have trading and 
[[settlement]] holidays that differ from U.S. holidays. 
 
Using holiday calendars, fund [[Companies]] will be able to add, change, or delete holiday lists for their 
[[Mutual Funds]] so that Fund/SERV can more accurately reflect trade and [[settlement]] dates. Calendar 
input will be done initially through PCWeb Direct, while discussions continue on adding other methods 
of entry in the future. 
 
FORWARD DATING 
By using a new indicator, distributors can submit a trade date for situations where the submission 
date of the distributor differs from the trade date of the fund company. 
 
Forward dating should only be used when the fund company and the distributor have 
agreed on how and when to use it. However, it may be helpful for: 
 
• Periodic-valued funds, where pre-notification is often required 

---

## Page 8

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 3 
 
 
 
 
 
• Daily-valued funds based in Luxembourg or Dublin, where the fund company’s cutoff time and 
processing cycle makes it impractical for the New York processing date to be the same as the 
fund company's trade date. 

---

## Page 9

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 4 
 
 
 
 
 
 
2.
Contact Information   
 
 
Multi-currency, holiday calendars, and forward dating are too complex to be exhaustively covered in 
this user guide. Before implementing one or more of them, we strongly encourage you to contact 
[[NSCC]]’s [[Mutual Funds]] Marketing Group at the numbers below. We will help you relate these products 
to your own business. 
 
Paul Lacher (212) 855-5673 
Jeannette McDonald (212) 855-5664 

---

## Page 10

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 5 
 
 
 
 
 
 
3.
A Note on Terminology   
 
MUTUAL FUND INDUSTRY TERMINOLOGY 
The word “fund” is used colloquially within the [[Mutual Funds]] industry in several different senses. 
Although the context is often enough to prevent confusion, these different meanings may occasionally 
cause difficulty. A “fund” can be: 
 
• A fund management company as a whole 
• A [[transfer agent]] acting for the fund company 
• An [[NSCC]] Rule 51 [[participant]], or fund [[Member]] 
• A family of [[Mutual Funds]] 
• A portfolio 
• A share class 
• A [[CUSIP]] 
 
FUND/SERV® TERMINOLOGY 
In contrast, Fund/SERV processing, including PCWeb Direct, only recognizes two entities: 
 
 
• An [[NSCC]] [[participant]] or [[Member]], which is a legal entity having a unique combination of a 
settling bank number and a [[transfer agent]] routing number. It has its own unique [[participant]] 
number, or in some cases two or more [[participant]] numbers. Mutual fund processing normally 
deals with both Rule 51 participants/members (funds) and Rule 2 participants/members 
(distributors). This roughly accommodates the following street meanings of the word “fund”: 
• The fund management company as a whole (a Rule 51 [[Member]]/[[participant]] that has at 
least one [[participant]] number) 
• A [[transfer agent]] acting for the fund company 
• Any [[NSCC]] Rule 51 [[Member]]/[[participant]] 
• A family of [[Mutual Funds]] (may or may not be a [[Member]]/[[participant]] with its own 
[[participant]] number, but never has a [[CUSIP]] number) 
 
 
• A [[CUSIP]] number of a specific security type. This roughly accommodates the following street 
meanings of the word “fund”: 
• A portfolio (if there are no share classes, it has one unique [[CUSIP]] number and one 
security type; if there are share classes, it does not have its own [[CUSIP]] number or 
security type) 
• A share class (always has one unique [[CUSIP]] number and one security type) 
• A [[CUSIP]] (sometimes referred to as a security issue) 

---

## Page 11

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 6 
 
 
 
 
 
For clarity, this user guide uses the following terms: 
 
The term Always refers to 
  [[CUSIP]] A security identified by the 9-digit security identification numbering system used in the 
U.S. market. This term is used when describing [[NSCC]] processing at a detailed level, 
especially holiday calendar processing. (The term ISIN will not be used.) 
  Distributor A [[Broker]] or other firm that sells [[Mutual Funds]]. (In other [[NSCC]] documentation, the 
distributor may be referred to as the “firm.” Also, note that this user guide will not use 
this term to refer to a fund company.) 
  Fund A fund company, fund family, portfolio, or share class, when it is obvious from context 
and inconvenient to be more specific. 
  Fund 
company 
A fund management company. 
Fund 
family 
A fund family or fund group. 
Fund group (To avoid confusion  this term is not used in this user guide) 
  Group (To avoid confusion, this term is not used in this user guide) 
  Grouping An entity created by the fund to accommodate holiday calendar processing. It has its 
own [[participant]] number and holiday calendar. (Note that this term has been devised to 
clarify holiday calendar concepts. It is not an industry standard term nor is it used 
elsewhere in [[NSCC]] in this sense.) 
  [[participant]] An entity represented by an [[NSCC]] [[participant]] number. Also known as a [[Member]]. This 
term will be used when describing [[NSCC]] processing at a detailed level, especially 
holiday calendar processing. In practice, this may be a fund company, a fund family, or 
some other grouping devised by the fund company for its processing and reporting 
convenience. 
  Portfolio One specific mutual fund. If there are no share classes, the portfolio has one unique 
[[CUSIP]] number and one security type. If there are share classes, it does not have its 
own [[CUSIP]] number or security type; each share class does. 
  Security (This term will not be used in this user guide.) 
  Security 
type 
A specific [[NSCC]] processing type for a [[CUSIP]]. Security types covered in this user guide 
include 25, 26, 59, 62, and 63. For details see Security Types in this user guide. 
  Share class A category of [[shares]] with its own cost structure (Class “A” [[shares]], Class “B” [[shares]], 
and so forth) that exists in a portfolio. Each share class in the portfolio has its own 
[[CUSIP]] number. 
 
 
 
 
Note: For other terms, see Appendix A: Glossary. 

---

## Page 12

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 7 
 
 
 
 
 
4.
Security Types   
 
DOMESTIC SECURITY TYPES 
Within Fund/SERV, there are currently two domestic security types for funds regulated by the 
[[securities]] & Exchange Commission ([[SEC]]) and set to U.S. standards. They are processed using U.S. 
processing cycles, holidays, and currency, and are marked for sales through U.S. dealers. Because of 
market changes the differences between them continue to diminish. 
 
Security Type 25 
These were originally load funds, typically sold by full-service brokers, that typically settled on 
T+3. However, the [[settlement]] cycle can be specified on the Fund/SERV Security Issue [[ID]] Form. 
 
Security Type 26 
These were originally no-load funds, typically sold by discount brokers, that typically settled on 
T+1. However, the [[settlement]] cycle can be specified on the Fund/SERV Security Issue [[ID]] Form. 
 
OFFSHORE SECURITY TYPES 
Within Fund/SERV there are currently three designated offshore security types. Luxembourg and 
Dublin fund [[Companies]] wishing to take advantage of product enhancements for holidays and future 
dating should choose either Security Type 62 or Security Type 63, which were introduced in 
November, 2002. 
 
Security Type 59 
Denominated in U.S. Dollars only, this is the original security type for CUSIPs domiciled outside 
of the United States that are not regulated by the [[SEC]], but are set to U.S. standards. In other 
words, these offshore CUSIPs operate using U.S. processing cycles, holidays, and currency, and are 
marked for sales through U.S. dealers. Any offshore [[CUSIP]] that is currently Security Class 59 may 
choose to remain so; [[NSCC]] expects that this will be the case for most Cayman and Bermuda 
CUSIPs. 
 
Many overseas CUSIPs [[DO]] not share U.S. operating schedules and have incurred manual 
workarounds due to: 
 
• Country-specific trading and [[settlement]] holidays 
• Differences between U.S. and European trade dates 
• Different methodologies for commission calculation that impacted the calculation of share 
issues 
• The need for multi-currency functionality. 
 
The approach adopted by [[NSCC]] has been to incrementally address these issues. In the autumn of 
2002, [[NSCC]] introduced its first enhancements to extend the capability of Fund/SERV to process 

---

## Page 13

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 8 
 
 
 
 
 
offshore fund transactions. As noted previously, this process is not complete and further 
incremental improvements are being planned. 
 
Security Type 62 
This must have U.S. Dollars as its base currency. Processing cycles, including holiday 
calendars, may differ from U.S. CUSIPs. The advantage of Security Type 62 is the enhanced 
processing capabilities offered by [[NSCC]]. 
 
Security Type 63 
This must not have U.S. Dollars as its base currency. Processing cycles, including holiday 
calendars, may differ from U.S. CUSIPs. 
 
 
 
Note: Security types are administered at the [[CUSIP]] level. Therefore within the same fund family or 
portfolio, there may be both Security Types 62 and 63. For more details see Appendix B: Converting to 
Security Types 62 and 63. However, the conversion of CUSIPs to Security Types 62 and 63 is not 
automated, and should not be attempted without assistance from the [[NSCC]] [[Mutual Funds]] Marketing 
Department. 

---

## Page 14

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 9 
 
 
 
 
 
 
5.
Multi-Currency for Luxembourg and Dublin Funds   
 
 
[[NSCC]], based on its research in 2002 and 2003 with the Multi-Currency Task Force, as well as in one- 
on-one discussions with OFS Working Group members, determined that fund families based in 
Luxembourg and Dublin fall in one of three broad categories: 
 
• “Single [[CUSIP]]/Single Currency” 
• “Pseudo NAV” 
• “Pseudo Classes of [[shares]]” 
 
This classification terminology is informal and is used colloquially within the [[Mutual Funds]] industry to 
categorize different types of offshore funds. It is defined in the following sections. 
 
“SINGLE [[CUSIP]]/SINGLE CURRENCY” FUNDS 
Each portfolio in a Single [[CUSIP]]/Single Currency fund family based in Luxembourg and Dublin has 
separate share classes (and thus separate [[CUSIP]] numbers) for each separate currency. For example: 
 
• U.S. dollar share classes (CUSIPs) trade, settle, and report only in U.S. dollars. 
• Euro share classes (CUSIPs) trade, settle, and report only in euros. 
 
For Single [[CUSIP]]/Single Currency funds, only the U.S. dollar share classes were eligible to trade and 
settle as part of Fund/SERV as Security Types 25, 26, or 59 prior to the November 2002 release. By 
converting the U.S. dollar CUSIPs to Security Type 62, fund [[Companies]] can set holiday calendars or 
accept trades dated for the future. 
 
CUSIPs with a base currency other than U.S. dollars were not eligible for any type of Fund/SERV 
activity until the November 2002 release. Now they can trade through Fund/SERV when coded as 
Security Type 63 and designated for [[settlement]] outside [[NSCC]]. 
 
“PSEUDO NAV” FUNDS 
A “Pseudo NAV” fund is a fund based in Luxembourg or Dublin in which each [[CUSIP]] is at the portfolio 
level, and the portfolio reports net [[Asset]] values (NAV) in more than one currency for its [[CUSIP]], 
generally based on a foreign exchange rate. The portfolio (and [[CUSIP]]) accepts trading and [[settlement]] 
and provides NAV reporting in two or more currencies. Many “Pseudo NAV” funds support two or more 
currencies without an explicit foreign exchange charge to the distributor or end client. 
 
A significant number of “Pseudo NAV” funds were part of Fund/SERV prior to the November 2002 
release and are categorized by Fund/SERV as U.S. dollar funds. All [[NSCC]] trading and reporting has 
been done only in U.S. dollars regardless of the [[CUSIP]]’s official base currency. [[NSCC]] does not 
mandate that the base currency specified in the fund prospectus be the same as the currency in the 
Fund/SERV [[CUSIP]] Profile. 

---

## Page 15

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 10 
 
 
 
 
 
 
“Pseudo NAV” Funds differ operationally from the third category of offshore funds, “Pseudo Classes of 
[[shares]]” Funds, in the following ways: 
 
• A “Pseudo NAV” [[CUSIP]] has a single [[Ledger]] on the [[transfer agent]] books. 
• Accruals such as daily dividends and brokerage payments (trail fees) are in the [[CUSIP]]’s base 
currency only. 
• Reporting in other currencies is calculated by multiplying the base currency by the foreign 
exchange rate. This formula is used to calculate NAV and dividends and commissions 
declared/paid. 
 
“PSEUDO CLASSES OF [[shares]]” FUNDS 
A “Pseudo Classes of [[shares]]” fund is a fund based in Luxembourg or Dublin in which each portfolio has 
its own [[CUSIP]] and reports NAVs and makes accruals in more than one currency for its [[CUSIP]], based 
generally upon a foreign exchange rate. 
 
The fund accepts trading and [[settlement]] and provides NAV reporting in two or more currencies for its 
[[CUSIP]]. “Pseudo Classes of [[shares]]” funds support two or more currencies without an explicit foreign 
exchange charge to the distributor or end client. Whatever can be calculated or reported in base 
currency can also be calculated and reported in the other currencies. 
 
A significant number of “Pseudo Classes of [[shares]]” funds were part of Fund/SERV prior to the 
November 2002 release and are categorized by Fund/SERV as U.S. dollar funds. All [[NSCC]] trading and 
reporting has been done only in U.S. dollars regardless of the fund’s official base currency. [[NSCC]] does 
not mandate that the base currency specified in the fund prospectus be the same as the currency in 
the Fund/SERV [[CUSIP]] Profile. 
 
“Pseudo Classes of [[shares]]” Funds differ operationally from “Pseudo NAV” funds in the following ways: 
 
 
• Each [[CUSIP]] has a separate sub-[[Ledger]] in the [[transfer agent]] system for every currency it 
supports. That is, shareholder positions are kept in more than one currency. 
• Accruals such as daily dividends and trail fees are in the [[CUSIP]]’s base currency and also in 
the other reporting currencies. 
• There is no difference between the information that can be reported in U.S. dollars and the 
information reported in other currencies. 
 
FREQUENTLY ASKED QUESTIONS 
 
1. Can a distributor enter a non-U.S. dollar trade for a Security Type 62 [[CUSIP]]? 
A distributor may enter a non-U.S. dollar trade for any [[CUSIP]] of Security Type 62 provided the 
distributor enters a valid non-U.S. dollar currency code and designates the [[CUSIP]] for X- 
[[settlement]]. Single [[CUSIP]]/Single Currency funds, if they adhere strictly to their fund convention, 
would have to reject those trades. 

---

## Page 16

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 11 
 
 
 
 
 
2. If a Single [[CUSIP]]/Single Currency fund family is a mix of Security Types 62 and 
63, how should it use the Profile Price & Rate file? 
The multi-currency enhancements provided in the November 2002 release are strictly for trading 
and [[settlement]] through Fund/SERV, and [[DO]] not enhance the Profile Price & Rate file. The Profile 
Price & Rate file is a broadcast reporting mechanism, without currency indicators. 
 
Security Type 62 
Security Type 62 CUSIPs may use the Profile Price & Rate file in the same way it was used prior to 
the November 2002 enhancements. 
 
Security Type 63 
For Security Type 63 CUSIPs, there are two interim choices until the 2004-2005 solutions provide 
explicit currency fields for Price & Rate reporting: 
 
• Avoid using the Profile Price & Rate file. The prices and rates broadcast in the [[CUSIP]]’s 
base currency (non-U.S. dollars) may be misread as U.S. dollars currency. 
• If you still wish to use the Profile Price & Rate file, inform all distributors trading the 
Security Type 63 [[CUSIP]] that the prices and rates provided reflect the base non-U.S. dollar 
currency of the [[CUSIP]]. 
 
3. If a “Single [[CUSIP]]/Single Currency” fund family is a mix of Security Types 62 
and 63, how should it use Networking and Commission [[settlement]]? 
The multi-currency enhancements of the November 2002 release are strictly for trading and 
[[settlement]] through Fund/SERV and [[DO]] not affect Networking and Commission [[settlement]]. 
[[Companies]] that wish to continue using the current core system can elect to [[DO]] so. As newer 
solutions are rolled out to the market, they will be available to all participants. 
 
Security Type 62 CUSIPs 
For Security Type 62 CUSIPs, Networking and Commission [[settlement]] may be used as is 
customary, since the [[settlement]] [[obligations]] created will be intended by the fund to be U.S. dollars. 
 
Networking and Commission [[settlement]] products [[DO]] not now have currency indicators. Certain 
activities in Networking (like [[Dividend]] payments) and Commission [[settlement]] (like trail fee 
payments) will automatically update a fund’s [[settlement]] obligation in U.S. dollars. 
 
Security Type 63 CUSIPs 
[[DO]] not use Networking or Commission [[settlement]] for Security Type 63. Any non-U.S. dollar 
activity in Networking or Commission [[settlement]] that triggers a [[settlement]] exposure will be 
calculated by [[NSCC]] as part of the fund’s daily [[settlement]] obligation in U.S. dollars and will be the 
liability of the fund. 

---

## Page 17

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 12 
 
 
 
 
 
4. Should a “Pseudo NAV” or a “Pseudo Classes of [[shares]]” fund family convert to 
Security Type 62, 63, or a combination of both? 
In assessing “Pseudo NAV” and “Pseudo Classes of [[shares]]” funds, it is important to remember 
that the November 2002 release enhancements only address trading and [[settlement]] through 
Fund/SERV and not the Profile Price & Rate file, Networking, or Commission Statement products, 
none of which, at present, have currency fields. 
 
Consequently, this question requires a case-by-case analysis. Every Security Type 62 or 63 
prospectus must state a single base currency to be included in the [[NSCC]] [[CUSIP]] Master File. Unlike 
the “Single [[CUSIP]]/Single Currency” funds, where the base currency of the fund is always equal to 
the base currency in the [[NSCC]] [[CUSIP]] Master file, a “Pseudo NAV” or “Pseudo Classes of [[shares]]” 
fund typically has flexibility in choosing the currency to be stated as the base currency in the  
[[NSCC]] [[CUSIP]] Master file. [[NSCC]] does not insist that the base currency in the fund’s prospectus 
should be the same as the base [[CUSIP]] in the [[CUSIP]] Master file. 
 
For a more detailed discussion, see Appendix B: Converting to Security Types 62 and 63. 
 
 
The [[NSCC]] [[Mutual Funds]] Marketing Department is available for assistance. See Contact 
Information in this user guide. 

---

## Page 18

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 13 
 
 
 
 
 
 
6.
Multi-Currency Setup (Fund [[Companies]])   
 
SELECTING A CURRENCY 
To choose a currency for a [[participant]] number, update the Fund/SERV Master Profile Form. To choose 
a currency for a single Security Issue [[ID]], update the Fund/SERV Security Issue [[ID]] Add/Modify form. 
Submitting one of these forms will update the appropriate Master File.  The forms require a Username 
and passcode.  If you don’t already have access, contact Mutual Fund Services at 212-855-8877.   
 
1 Go to https://portal.[[DTCC]].com.  Enter your User [[ID]] and password and click Login. The Mutual 
Funds Services page reappears with a list of options. 
2 Click Connectivity. 
The Introduction to Connectivity page appears with general information and a list of options. 
3 Under either Master Profile Forms or Security Issue [[ID]] Forms, click Add or Modify. 
4 Update the form according to the standard instructions. (See the note at the end of this procedure 
for details.) 
 
 
 
 
5 To select a currency, in the Currency Type field: 
• For U.S. dollar currency, select either USD or USN 
—or— 
 
• For a non-U.S.dollar currency, select one of the listed currencies or Other. 
 
 
• A non-U.S. currency code is allowed on the Fund/SERV [[CUSIP]] Profile Update form only if 
the security type is 63 (Offshore non-U.S. dollar processing). 
• A non-U.S. currency code is allowed on the Fund/SERV [[Member]] Profile Update form only if 
all the [[Member]]’s security types are 63 (Offshore non-U.S. dollar processing). 


---

## Page 19

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 14 
 
 
 
 
 
• The five specific non-U.S. currency codes displayed are the most likely candidates, but 
they are only examples of the different types of tradable currencies. For other currencies, 
click the Other field and type the appropriate code. Only valid International Standards 
Organization (ISO) currency codes are permitted. 
 
6 Submit the form according to the standard instructions. (See the note at the end of this procedure 
for details.) 
 
 
 
STANDARD INSTRUCTIONS FOR CHOOSING AND SUBMITTING PROFILE FORMS 
1 Go to https://portal.[[DTCC]].com and log in. 
2 Click Mutual Fund Services. 
3 Under Mutual Fund Services, click Fund/SERV. Then click Fund/SERV Technical Manual, 
then Chapter 3 – Establishing a new Fund/SERV [[Member]]. 
4 For members, consult the following topics: 
• Fund/SERV [[Member]] Profile 
• [[Member]] Profile Field Descriptions 
5 For individual CUSIPs, consult the following topics: 
• Mutual Fund Security Profile 
• Mutual Fund Security Profile Field Descriptions 
 
Note: The above procedure only concerns updating the currency type. For specific instructions on how to 
choose which form to use and how to fill out and submit it, [[DO]] the following: 

---

## Page 20

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 15 
 
 
 
 
 
 
7.
Multi-Currency Processing   
 
DISTRIBUTORS: SUBMITTING A TRADE 
A distributor can enter a non-U.S. currency codes on trade input for a Security Type 62 or 63. 
 
 
• If a distributor does not enter a currency code, Fund/SERV supplies one based on the currency 
indicated on the Master Files. 
• If the distributor enters a currency code, Fund/SERV does not attempt to establish a match 
with the currency code indicated on the security or fund master files. 
 
Only X-[[settlement]] trades are allowed a non-U.S. currency code. If a distributor indicates a settling 
order and supplies a non-U.S. currency code, Fund/SERV will reject the order. 
 
FUND COMPANY PROCESSING 
A fund company cannot modify an original currency received on an order. If the code is incorrect, the 
fund company can use reject code 110 (currency code invalid) to reject the order 
 
SECURITY TYPE MISMATCHES 
Fund/SERV will reject an order if a distributor supplies a security type and one of the following occurs: 
 
 
• Security Type 62 or 63 was indicated but it does not match the security type on the security 
master file. 
• The security type on the security master file is 62 or 63 but it does not match the security 
type indicated by the distributor. 

---

## Page 21

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 16 
 
 
 
 
 
 
8.
Changes to Record Layouts (Multi-Currency and Forward Dating)   
 
NEW FIELDS 
New fields have been added to the Fund/SERV Order (001) and Exchange (015) record layouts for 
multi-currency and forward dating: 
 
Field Processing Description 
Currency 
Code 
Multi- 
currency 
New field added to accommodate different 
currencies. It is equivalent to the Currency Type 
field on the Profile forms. 
Future Trade 
Date 
Forward 
dating 
New field added to contain the forward date. 
Trade Date 
Forward 
Indicator 
Forward 
dating 
New field added to indicate whether forward dating 
has been requested for this trade. 
 
 
CHANGE TO EXISTING FIELD 
A new value has been added to the [[settlement]] Override Reason Code field in the following record 
layouts: 
 
• Order (001) 
• Correction (003) 
• Confirmation (005) 
• Reconfirmation (006) 
• Exchange (015) 
• Exchange Confirmation (016) 
• Exchange Reconfirmation (017) 
• Post [[settlement]] Exchange Cancellation (021) 
• Correction Confirmation (025) 
 
Field Processing Description 
[[settlement]] 
Override Reason 
Code 
Multi-currency 06 = X-[[settlement]] offshore enhanced (allowed for 
Security Types 62 and 63 only) 

---

## Page 22

Fund/SERV Applications for Offshore Trading and [[settlement]] > 17 
April 
2004 
 
 
 
 
 
9.
Holiday Calendars   
 
WHY HOLIDAY CALENDARS? 
In the U.S. market, fund [[Companies]] and distributors typically share the same business 
holidays. On most holidays, the markets are closed for both trading and [[settlement]]; on some 
holidays such as Columbus Day, markets are open for trading but closed for [[settlement]]. 
 
However, Luxembourg and Dublin fund [[Companies]], as well as the banks in which non-U.S. 
dollar trades settle, may have trading and [[settlement]] holidays that differ from U.S. holidays. 
Among a fund company’s offerings, or even within a fund family, there may be some common 
holidays and some holidays specific only to a [[CUSIP]] or portfolio. 
 
This can affect a transaction not only if a holiday falls on a specific trade date or [[settlement]] 
date, but also if one or more holidays occur within a specified time period, such as a 
[[settlement]] cycle. 
 
Fund [[Companies]] can use PCWeb Direct to create their own holiday calendars for trading, 
[[settlement]], or both. Calendars can be assigned to specific CUSIPs or to a larger entity such as 
a fund family or another grouping determined by the fund company. Distributors can view 
these calendars via PCWeb Direct. 
 
 
 
Holiday Calendars should only be used after the distributors and the fund company 
have agreed on the details. You are also strongly encouraged to contact [[NSCC]]’s Mutual 
Funds Marketing Group. We will help you relate these products to your own business. See 
Contact Information in this user guide. 
 
HOW [[DO]] HOLIDAY CALENDARS AND MULTI-CURRENCY WORK TOGETHER? 
“Single [[CUSIP]]/Single Currency” funds may logically sort themselves into similar holiday 
calendar groupings. However, the situation for “Pseudo NAV” and “Pseudo Classes of [[shares]]” 
funds may be considerably more complicated. 
 
For more information see Multi-Currency for Luxembourg and Dublin Funds in this user guide. 
You are also strongly encouraged to work with the [[NSCC]] [[Mutual Funds]] Marketing Department. 
See Contact Information in this user guide. 
 
HOW [[DO]] HOLIDAY CALENDARS AND FORWARD DATING WORK TOGETHER? 
A difference between a distributor’s and a fund company’s holiday dates, or a difference 
between a distributor’s trade date and a fund company’s trade date for a specific transaction, 
 
Note: Current [[NSCC]] processing takes holiday calendars into account only for assigning 
[[settlement]] dates to CUSIPs settling in U.S. dollars. 

---

## Page 23

Fund/SERV Applications for Offshore Trading and [[settlement]] > 18 
April 
2004 
 
 
 
 
can result in rejected transactions or awkward workarounds. There can also be a mismatch 
between a distributor’s anticipated [[settlement]] date and the fund’ company’s [[settlement]] date. 
Differences in both holidays and trade dates can further complicate record keeping. 
 
Holiday calendars and forward dating, when implemented together, may help simplify or 
eliminate these problems. However, this is a complex process that should not be 
attempted without assistance from the [[NSCC]] [[Mutual Funds]] Marketing Department. 
See Contact Information in this user guide. 

---

## Page 24

Fund/SERV Applications for Offshore Trading and [[settlement]] > 19 
April 
2004 
 
 
 
 
 
10.
Setting Up Holiday Calendars (Fund [[Companies]] Only)   
 
 
Aside from Saturdays and Sundays, there are days on which trading, [[settlement]], or both are 
not possible because a specific office or group of offices of a distributor or fund company are 
closed for business. Bank holidays in varying jurisdictions may also affect [[settlement]] dates. 
 
The reason for the closure is usually but not always a local, state, or national holiday. 
Sometimes a firm determines that a particular facility must stay open for trading and/or 
[[settlement]] in spite of the holiday. 
 
In order to accommodate this complex reality, fund [[Companies]] may create their own list of 
closures, called holiday calendars, for CUSIPs of Security Type 62 or 63. These calendars may 
be created at the individual [[CUSIP]] level if necessary, or may be applied to larger groupings 
such as fund families or other groupings that the fund company finds convenient—even to all 
CUSIPs managed by the fund company. 
 
Fund/SERV recognizes the following types of holidays: 
 
 
• Trading Holiday: No trading activity 
• [[settlement]] Holiday: No [[settlement]] activity 
• Both: Neither trading nor [[settlement]] activity. 
Each holiday calendar has the following attributes: 
• It has a name assigned by the fund company at creation. 
• It can contain all trading holidays, all [[settlement]] holidays, or a mixture of both. 
• It can be assigned either to all CUSIPs within a [[participant]] number or to one or more 
CUSIPs. 
• Each [[participant]] number or [[CUSIP]] may have only one calendar. 
 
 
 
[[NSCC]] PROCESSING 
 
[[settlement]] Holidays 
Current [[NSCC]] processing takes [[settlement]] holiday calendars into account only for 
assigning [[settlement]] dates to CUSIPs settling in U.S. dollars (Security Type 62). For 
Security Type 63, [[settlement]] date is either input by the distributor in the order record or 
by the fund company in the confirmation record. 
 
Note: We recommend setting up holiday calendars for only one calendar year at a time. 

---

## Page 25

April 
2004 
Fund/SERV Applications for Offshore Trading and [[settlement]] > 20 
 
 
 
 
Trading Holidays 
Current [[NSCC]] processing does not take trading holiday calendars into account for either 
Security Type 62 or 63 except for forward dating. In future releases, [[NSCC]] plans to extend 
this functionality. 
 
Distributors 
Distributors may find that browsing the holiday settings is useful in setting up accurate 
trade dates and anticipated [[settlement]] dates. 
 
[[default]] Calendars 
To give you more flexibility in assigning calendars, there are three [[default]] levels: 
1. If a particular [[CUSIP]] has a calendar assigned to it, [[NSCC]] uses the [[CUSIP]]’s calendar 
in its processing. It does not use the calendar assigned to the [[participant]]. 
2. If the [[CUSIP]] does not have a calendar assigned to it but its [[participant]] does, [[NSCC]] 
uses the [[participant]]’s calendar. 
3. If neither the [[CUSIP]] nor the [[participant]] has an assigned calendar, [[NSCC]] uses 
[[DTCC]]’s [[default]] U.S. holiday calendar. 
 
ANALYZING [[CUSIP]] AND [[participant]] LEVELS 
A calendar can apply to either a [[participant]] number or to a single [[CUSIP]]. 
 
 
Assigning calendars to a specific [[CUSIP]] may be appropriate in a number of circumstances, for 
example: 
 
• In a portfolio with different currency share classes, each share class may have its own 
set of [[settlement]] holiday closings. 
• In a country fund, the market in which the portfolio invests may have a unique set of 
trading and [[settlement]] holiday closings. 
 
If separate families or other groupings within the same fund company need different 
calendars, there are currently two options: 
 
• We recommend that you assign a specific calendar to each [[CUSIP]]. This is useful if you 
[[DO]] not want to create multiple [[participant]] numbers, if the CUSIPs have complex 
differences in trading and [[settlement]] holidays, or if you want to refine the calendar   
for one of the groupings you created. This [[Option]] is more labor-intensive but it may 
allow you to take better advantage of future improvements in automated [[NSCC]] holiday 
and forward dating processing. 
• Instead, you may prefer to obtain a separate [[participant]] number for each grouping 
and assign one calendar to the [[participant]] number. This is useful if you are willing to 
have multiple [[participant]] numbers, and if CUSIPs fall into clearly defined groupings 
that have identical or very similar holidays. However, because of membership criteria 

---

## Page 26

April 
2004 
Fund/SERV Applications for Offshore Trading and [[settlement]] > 21 
 
 
 
 
it may be difficult to get another [[participant]] number. (Note also that the Holiday 
Calendar Web interface sometimes refers to these groupings as “funds,” since in 
[[NSCC]] processing, “fund” is synonymous with “[[participant]] number.”) 

---

## Page 27

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 22 
 
 
 
 
 
 
CALENDAR SETUP WORKSHEET 
The samples on the four pages that follow illustrate a suggested procedure for determining how many calendars you may need and to which  
CUSIPs and/or participants they should be assigned. This procedure is recommended whether you wish to attach calendars to [[participant]] numbers 
for the groupings, or you prefer to attach a calendar to each [[CUSIP]]. 
 
Construct calendars by determining trading and [[settlement]] closures for each [[CUSIP]]. Then look for common patterns and group them together. 
 
 
 
 
Note: If you find that one grouping within a [[participant]] number has many more CUSIPs than any of the others, you may want to make it the “fund [[default]] 
calendar” for the [[participant]]. This way, you will not have to manually attach a calendar to the CUSIPs in that grouping. 

---

## Page 28

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 23 
 
 
 
 
 
1 Create a spreadsheet with a row for each individual [[CUSIP]] and a column for each possible holiday. In each cell, indicate whether that [[CUSIP]] is 
closed for trading, [[settlement]], or both. (In this example, the fund is creating a calendar based on French holidays.) 
 
 
 
 
GROUP ING  
 
[[CUSIP]]  
HO LIDAYS   
            
  New  Year's  
Day  
Good  Friday   Easter  
Monday   
Labour  
Day/May  
Day 
Ascension  W hit  
Monday   
Bastille  Day  Assum  ption  Arm  istice  
Day  
Christm  as 
Day 
  1 -Jan -03   18 -Apr -03  21 -Apr -03  1 -May -03  29 -May -03  9 -Jun -03   14 -Jul -03   15  -Aug -03   11  -Nov -03  25 -Dec -03 
 000001305  B T S B B T S B B B 
 111111112  B T  B B T  B B B 
 111111113  B   B B   B B B 
 000000562  B T S B B T S B B B 
 11111111 5 B B B B B B B B B B 
 000003608  B T S B B T S B B B 
 111111117  B   B B   B B B 
 111111118  B T  B B T  B B B 
 111111119  B   B B   B B B 
 111111120  B T  B B T  B B B 
 111111121  B T S B B T S B B B 
 111111122  B B B B B B B B B B 
 111111123  B B B B B B B B B B 
 111111124  B B B B B B B B B B 
 111111125  B B B B B B B B B B 
 111111126  B B B B B B B B B B 
 111111127  B B B B B B B B B B 
 111111128  B B B B B B B B B B 
 111111129  B B B B B B B B B B 
 111111130  B B B B B B B B B B 
 
T=Trading   Holiday  
S=Settlem  ent  Holiday  
B=Both  Trading & Settlem  ent  
 
Suggestion: Create a calendar for only one year at a time. 

---

## Page 29

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 24 
 
 
 
 
 
2 Determine common patterns of holiday schedules. 
 
GROU PING  CU SIP HOLIDAYS  
            
  New  Year's  
day 
Good  Friday  Easter  
Monday  
Labour  
Day/May 
D ay 
Ascension  W hit  
Monday  
Bastille  Day  Assumption  Armis tice  
Day  
Christmas  
D ay 
  1-Jan -03  18 -Apr-03  21 -Apr -03  1-May -03  29 -May -03  9-Jun -03  14 -Jul -03  15-Aug -03  11 -Nov -03  25 -Dec -03  
 000001305  B T S B B T S B B B 
 111111112  B T  B B T  B B B 
 111111113  B   B B   B B B 
 000000562  B T S B B T S B B B 
 111111115  B B B B B B B B B B 
 000003608  B T S B B T S B B B 
 111111117  B   B B   B B B 
 111111118  B T  B B T  B B B 
 111111119  B   B B   B B B 
 111111120  B T  B B T  B B B 
 111111121  B T S B B T S B B B 
 111111122  B B B B B B B B B B 
 111111123  B B B B B B B B B B 
 111111124  B B B B B B B B B B 
 111111125  B B B B B B B B B B 
 111111126  B B B B B B B B B B 
 111111127  B B B B B B B B B B 
 111111128  B B B B B B B B B B 
 111111129  B B B B B B B B B B 
 111111130  B B B B B B B B B B 
 
 
T=Trading Holiday  
S=[[settlement]]  Holiday  
B=Both  Trading  & [[settlement]]  Holiday  

---

## Page 30

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 25 
 
 
 
 
Note: Since in this example we are only dealing with one [[participant]] number, we have made the fourth and largest grouping the “fund [[default]] calendar” 
for the [[participant]]. This way, we will not have to manually attach a calendar to the CUSIPs in that grouping. 
 
 
3 Group CUSIPs with the same holiday schedule together. 
 
GROUPING CUSIPS 
 
 
 Grouping A 000001305 
000000562 
000003608 
111111121 
 
 Grouping B 111111112 
111111118 
111111120 
 
Grouping C 111111113 
 111111117 
 111111119 
[[default]] 111111115 
 111111122 
 111111123 
 111111124 
 111111125 
 111111126 
 111111127 
 111111128 
 111111129 
 111111130 

---

## Page 31

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 26 
 
 
 
 
 
4 Give each grouping a unique calendar name. You are now ready to create the calendars in PCWeb Direct. 
HOLIDAYS 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
T=Trading Holiday 
S=[[settlement]] Holiday 
B=Both Trading & [[settlement]] Holiday 
 
CALENDAR-A 
CALENDAR-B 
CALENDAR-C 
[[default]]-CALENDAR (carried at the [[participant]] level) 
 
 
 
Note: In this example, one fund company will have four holiday calendars. CALENDAR-A, CALENDAR-B, AND CALENDAR-C will be assigned to individual 
CUSIPs. [[default]]-CALENDAR will be assigned to the [[participant]] number. We will not have to manually attach a calendar to the CUSIPs in that grouping. 
GROUPING [[CUSIP]]  
            
  New Year's Day Good Friday Easter Monday Labour Day/May Day Ascension Whit Monday Bastille Day Assumption Armistice Day Christmas Day 
  1-Jan-03 18-Apr-03 21-Apr-03 1-May-03 29-May-03 9-Jun-03 14-Jul-03 15-Aug-03 11-Nov-03 25-Dec-03 
A 0000001305 B T S B B T S B B B 
B 111111112 B T  B B T  B B B 
C 111111113 B   B B   B B B 
A 000000562 B T S B B T S B B B 
[[default]] 111111115 B B B B B B B B B B 
A 000003608 B T S B B T S B B B 
C 111111117 B   B B   B B B 
B 111111118 B T  B B T  B B B 
C 111111119 B   B B   B B B 
B 111111120 B T  B B T  B B B 
A 111111121 B T S B B T S B B B 
[[default]] 111111122 B B B B B B B B B B 
[[default]] 111111123 B B B B B B B B B B 
[[default]] 111111124 B B B B B B B B B B 
[[default]] 111111125 B B B B B B B B B B 
[[default]] 111111126 B B B B B B B B B B 
[[default]] 111111127 B B B B B B B B B B 
[[default]] 111111128 B B B B B B B B B B 
[[default]] 111111129 B B B B B B B B B B 
[[default]] 111111130 B B B B B B B B B B 
 

---

## Page 32

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 27 
 
 
 
 
 
 
11.
Holiday Calendars on PCWeb Direct: Fund Usage Only   
 
 
This chapter is only for fund [[Companies]]. If you are a distributor, see the next chapter, 
Holiday Calendars on PCWeb Direct: [[participant]] and [[NSCC]] Usage. 
 
WEB INTERFACE 
Fund/SERV provides a Web interface via PCWeb Direct that you can use to create, manage, and 
browse calendars. 
 
Using holiday calendars on PCWeb Direct requires a digital certificate valid for “Offshore Funds 
Calendar.” For information on obtaining and updating digital certificates, see Appendix D: Obtaining a 
Digital Certificate. 
 
 
 
Before attempting to use the Web interface to set up your calendars for production: 
 
 
• Work closely with your [[NSCC]] representatives and with your distributors to make sure that the 
software and manual procedures are correctly and efficiently coordinated. 
• Use worksheets similar to those in the previous section of this user guide to plan out your calendar 
structure. 
Note: If you have set up separate groupings of CUSIPs with their own [[participant]] numbers, remember 
that in the Holiday Calendar Web interface, “fund” is synonymous with “[[participant]] number” and “security 
issue” is synonymous with “[[CUSIP]].” 

---

## Page 33

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 28 
 
 
 
 
 
 
ACCESSING CALENDAR FUNCTIONS 
If your fund company has multiple [[participant]] numbers, you may only log in as one [[participant]] at a 
time. Any additions, updates, deletions, or assignments affect this [[participant]] number only (which the 
interface refers to interchangeably as “[[participant]]” or “fund.”) 
 
1 Access PCWeb Direct and log in. 
The Welcome to PCWeb Direct page appears. 
 
 
2 Under [[Mutual Funds]] at the left of the page, click Offshore Funds Calendar. 
The Select [[participant]] page appears. 
 
 
3 Type a [[participant]] number and click Submit. 
The Calendar Menu page appears. 
 
 
4 On the Calendar Menu, in the Calendar Action area, select the action you wish to take and click 
Submit. 


---

## Page 34

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 29 
 
 
 
 
 
CREATING A CALENDAR 
 
 
 
1 On the Calendar Menu, in the Calendar Action area, select Add new calendar and click Submit. 
—or— 
 
 
 
In the Go To  list at the upper right select Add calendar. 
The Add Calendar page appears. 
 
 
 
 
 
 
 
 
 
 
 
 
 
2 In the Holiday Calendar [[ID]] field type a name for the calendar. Calendar names are not case 
sensitive. You may choose any name, but try to make the name one you will remember. 
3 Create the first holiday by entering three data elements: 
• In the First Holiday Calendar Date field, type a date in mmddyyyy format. 
• In the Holiday Description field, type a name for the holiday. Holiday descriptions are case 
sensitive. You may choose any name, but try to make the name one you will remember. 
• In the Holiday Type field, select the appropriate type. 


---

## Page 35

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 30 
 
 
 
 
4 Click Submit. 
The page name changes to Edit Calendar Dates. The information for the calendar appears in the 
Calendar... area at the bottom of the screen. 
 
 
 
 
 
5 Optional: To continue adding dates, in the Required Data section, for each holiday enter the 
three elements and click Add. For more details, see Editing a Calendar in this section of the user 
guide. 
—or— 
 
To exit, in the Go To list at the upper right select Calendar Menu. 
 
—or— 
 
To select another [[participant]] number, in the Go To list at the upper right select Select 
[[participant]]. 
 
Notes: 
 
To print this list, use your browser’s standard print capability. 
 
You will still need to assign the calendar to a [[participant]] or [[CUSIP]]. See Assigning a Calendar in this section 
of the user guide. 

---

## Page 36

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 31 
 
 
 
 
 
ASSIGNING A CALENDAR 
Use this procedure to assign a calendar to a [[CUSIP]] or to assign a calendar to your [[participant]] number 
(that is, to make it the fund [[default]] calendar). 
 
Also use it to effectively remove an assignment. There is no way to remove a calendar assignment 
directly; instead, you must assign another calendar, the fund [[default]] calendar, or [[DTCC]]’s [[default]] US 
calendar to the [[participant]] number or [[CUSIP]]. 
 
If your fund company has multiple [[participant]] numbers, you may only log on as one [[participant]] at a 
time. Any additions, updates, deletions, or assignments affect this [[participant]] number only (which the 
interface refers to interchangeably as “[[participant]]” or “fund.”) 
 
 
 
 
1  On the Calendar Menu, in the Calendar Action area, select Assign calendar to Security Issue or 
Fund and click Submit. 
 
 
 
—or— 
 
 
 
In the Go To list at the upper right select Assign Calendar. 
 
Note: Remember that “security issue” is synonymous with “[[CUSIP]]” and “fund” is synonymous with 
“[[participant]] number.” 

---

## Page 37

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 32 
 
 
 
 
 
The Assign Calendar page appears. 
 
 
 
 
 
You can now assign a calendar to either a [[participant]] number or a [[CUSIP]]. 

---

## Page 38

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 33 
 
 
 
 
 
Assigning a Calendar to a [[participant]] number 
Use this subprocedure to assign the “fund [[default]] calendar.” 
 
 
1 In the Fund / Security Issue list select Fund. 
2 In the Available calendars for assignment list select the calendar you wish to assign and click 
Submit. 
 
 
 
A message appears confirming the new assignment. 
 
Note: One possibility for assignment is [[DTCC]]’s [[default]] US calendar. This in effect removes the 
assignment of a calendar you created. 

---

## Page 39

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 34 
 
 
 
 
 
Assigning a Calendar to a [[CUSIP]] 
Use this subprocedure to assign a calendar to an individual [[CUSIP]] (referred to in the interface as 
“Security Issue”). 
 
If a [[CUSIP]] involved in a trade has no calendar assigned to it and its [[participant]] number has 
no calendar assigned to it, Fund/SERV processing uses [[DTCC]]’s [[default]] US calendar. 
 
 
1 From the Fund / Security Issue list select Security Issue. 
2 In the Security Issue [[ID]] field type the nine-digit [[CUSIP]] number. 
3 From the Available calendars for assignment list select the calendar and click Submit. 
 
 
 
The new assignment appears in the List of Security Issue IDs... area. 
 
 
4 Optional: Click on the calendar name to display all the holidays in a calendar. 
The list of holidays appears for the chosen calendar. 
 
 
 
 
Note: Possibilities for assignment include the fund [[default]] calendar, if there is one, and [[DTCC]]’s  
[[default]] US calendar. This in effect removes the assignment of a calendar you created from the [[CUSIP]]. 
 
NOTE: To print this list, use your browser’s standard print capability. 

---

## Page 40

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 35 
 
 
 
 
5 Optional: To exit, in the Go To list at the upper right select Calendar Menu. 
—or— 
 
To select another [[participant]] number, in the Go To list at the upper right select Select 
[[participant]]. 

---

## Page 41

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 36 
 
 
 
 
 
EDITING A CALENDAR 
 
 
 
1 On the Calendar Menu, in the Calendar Action area, select Edit/Delete existing calendar and 
click Submit. 
—or— 
 
 
 
In the Go To list at the upper right select Edit/Delete Calendar. 
The Edit/Delete Calendar page appears. 
 
 
 
 
 
 
 
 
 
 
 
 
 
2 In the Select Holiday Calendar field, select the calendar you wish to edit. 
3 In the Calendar Action field, select Edit existing calendar and click Submit. 


---

## Page 42

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 37 
 
 
 
 
 
 
You can now create a new holiday, update an existing holiday, or delete an existing 
holiday. 

---

## Page 43

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 38 
 
 
 
 
 
Creating a New Holiday 
Use this subprocedure to add a date to the calendar. 
 
 
1 In the Required Data area enter three data elements: 
• In the Holiday Date field, type a date in mmddyyyy format. 
• In the Holiday Description field, type a name for the holiday. Holiday descriptions are case 
sensitive. You may choose any name, but try to make the name one you will remember. 
• In the Holiday Type field, select the appropriate type. 
2 Click Add+. 


---

## Page 44

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 39 
 
 
 
 
 
 
Updating an Existing Holiday 
Use this subprocedure to change the name, description, or type for a date you have already created. 
If the actual date is wrong, you must delete and recreate the holiday. 
 
The following is an example of an incorrect holiday type for Good Friday: 
 
 
 
 
 
Here is the procedure for correcting it: 
 
 
1 In the Calendar... area, in the row for the holiday you want to update: 
 
 
• In the Holiday Description field, type any corrections to the name for the holiday. Holiday 
descriptions are case sensitive. 
• In the Holiday Type field, select the appropriate type. 
 
 
2 In the row for the same holiday, click Update". 


---

## Page 45

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 40 
 
 
 
 
 
Deleting an Existing Holiday 
Use this subprocedure to delete an existing date. 
 
 
1 In the Calendar... area, in the row for the holiday you want to delete, click Delete —. 
A message appears asking you to confirm your deletion. 
2 Click OK. 
The holiday no longer appears. 
 
 
3 Optional: To exit, in the Go To list at the upper right select Calendar Menu. 
—or— 
 
To select another [[participant]], in the Go To list at the upper right select Select [[participant]]. 


---

## Page 46

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 41 
 
 
 
 
 
DELETING A CALENDAR 
You cannot delete a calendar if it is assigned to any [[participant]] or to any [[CUSIP]], and there is no way 
to remove a calendar assignment directly. 
 
Instead, for each [[participant]] or [[CUSIP]] to which the calendar is assigned, you must first reassign 
another calendar, the [[participant]]’s “fund [[default]] calendar,” or [[DTCC]]’s [[default]] US calendar. For details, 
see Assigning a Calendar in this chapter. 
 
 
1 On the Calendar Menu, in the Calendar Action area, select Edit/Delete existing calendar and 
click Submit. 
—or— 
 
 
 
In the Go To list at the upper right, select Edit/Delete Calendar. 


---

## Page 47

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 42 
 
 
 
 
 
The Edit/Delete Calendar page appears. 
 
 
 
2 In the Select Holiday Calendar field, select the calendar you wish to delete. 
3 In the Calendar Action field, select Delete existing calendar and click Submit. 
A message appears asking you to confirm your deletion. 
4 Click OK. 
 
 
 
 
5 Optional: To exit, in the Go To list at the upper right, select Calendar Menu. 
—or— 
 
To select another [[participant]], in the Go To list at the upper right, select Select [[participant]]. 
 
Warning: No confirmation message appears. 

---

## Page 48

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 43 
 
 
 
 
 
12.
Holiday Calendars on PCWeb Direct: [[participant]] and [[NSCC]] Usage   
 
WEB INTERFACE 
Fund/SERV provides a Web interface via PCWeb Direct that you can use to browse calendars. This is 
especially useful in determining holidays not currently automated by [[NSCC]] processing, namely: 
 
• Trading holidays for both security types 62 and 63 
• [[settlement]] holidays for [[securities]] not settling in U.S. dollars (Security Type 63). 
 
 
 
BROWSING VIA PCWEB DIRECT 
1 Access PCWeb Direct and log in. 
The Welcome to PCWeb Direct page appears. 
 
 
2 Under [[Mutual Funds]] at the left of the page, click Offshore Funds Calendar. 
The Select [[participant]] page appears. 
 
 
3 Type your [[participant]] number and click Submit. 
Notes: 
 
Using holiday calendars on PCWeb Direct requires a digital certificate valid for “Offshore Funds Calendar”. 
For information on obtaining and updating digital certificates, see Appendix D: Obtaining a Digital 
Certificate. 
 
In addition to using its own [[participant]] number to log on, a distributor needs to know the [[NSCC]] [[participant]] 
number of the fund or [[CUSIP]] in order to access calendar information. 
 
In the Holiday Calendar Web interface, “fund” is synonymous with “[[participant]] number” and “security 
issue” is synonymous with “[[CUSIP]].” 

---

## Page 49

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 44 
 
 
 
 
 
The Browse Calendar Menu page appears. If the [[participant]] number under which you logged in 
represents a distributor, only actions appropriate for browsing appear. To view calendars, you will 
also need to know either: 
• The [[participant]] number of the fund company, fund family, or other holiday calendar grouping 
—or— 
 
• The [[CUSIP]] number of the individual security issue. 
 
 
 
 
 
 
You can now browse either [[participant]] calendars or [[CUSIP]] calendars. 

---

## Page 50

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 45 
 
 
 
 
 
 
Browsing [[participant]] Calendars 
 
 
1 On the Browse Calendar Menu, in the Fund Number to Browse area: 
1. Type the number of the fund company, fund family, or other grouping. 
2. Click Browse Calendars. 
2 Click Submit. 
The list of calendars for the [[participant]] appears. 
 
 
 
3 Optional: To see the holidays for a calendar, in the row for that calendar click dates. 
The calendar listing appears. 
 
 
 
 
4 Optional: To see the [[participant]] or [[CUSIP]] assignments for a calendar, in the row for that calendar 
click assignments. 
 
NOTE: To print this list, use your browser’s standard print capability. 

---

## Page 51

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 46 
 
 
 
 
 
The list of assignments for that calendar appears. 
 
 
5 Optional: To display all the holidays in a calendar, in the in the Assignment List area click the 
calendar name. 
The list of holidays appears for the chosen calendar. 
 
 
 
 
 
NOTE: To print either or both of these lists, use your browser’s standard print capability. 

---

## Page 52

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 47 
 
 
 
 
 
Browsing [[CUSIP]] Calendars 
 
 
 
 
 
1 On the Browse Calendar Menu, in the Fund Number to Browse area, click Browse Security 
Issues with non-[[default]] assignments. 
2 In the Security Issue [[ID]] to Browse field, type the [[CUSIP]] number whose calendar you want to 
view. 
 
 
 
3 Click Submit. 
The calendar’s assignments and dates appear. 
 
 
 
 
 
4 Optional: To view the calendar for another [[participant]] number, in the Go To list at the upper right 
select Select [[participant]]. 
 
Note: If a [[CUSIP]] involved in a trade has no calendar assigned to it and its [[participant]] number has no 
calendar assigned to it, Fund/SERV processing uses [[DTCC]]’s [[default]] US calendar. 
 
Hint: To get a current list of CUSIPs that have calendars assigned to them, browse the [[participant]] 
calendar first. 
 
NOTE: To print this list, use your browser’s standard print capability. 

---

## Page 53

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 48 
 
 
 
 
 
 
13.
Using Holiday Calendars (without Forward Dating)   
 
 
 
 
DISTRIBUTORS—ENTERING A TRADE 
There are no specific coding requirements on the Fund/SERV Order (001) or Exchange (015) record. 
 
 
Fund/SERV does not edit or verify the trade date submitted by the distributor against the fund 
calendar. However, distributors may view the fund calendars for trading holidays. See Holiday 
Calendars: [[participant]] and [[NSCC]] Usage in this user guide for details. 
 
The distributor may set [[settlement]] date by entering a date in the Anticipated [[settlement]] Date field. 
If this field is left blank and if [[settlement]] is in U.S. dollars, [[NSCC]] calculates the [[settlement]] date,   
taking into account the [[settlement]] holidays in the appropriate fund calendar. 
 
[[NSCC]]—TRADE DATE EDITING AND VERIFICATION 
Fund/SERV does not edit or verify the trade date submitted by the distributor against a fund calendar. 
• Distributors may view the fund calendar to determine trading holidays. 
• A fund company may reject trades that are submitted on a trading holiday. 
 
[[NSCC]]—[[settlement]] DATE PROCESSING 
 
Trades Settling in U.S. Dollars 
 
If the distributor has not entered a date in 
the Anticipated [[settlement]] Date field: 
 If the distributor has entered a date in the 
Anticipated [[settlement]] Date field: 
   
• Fund/SERV calculates the anticipated 
[[settlement]] date based on trade date plus 
the [[settlement]] cycle of the [[CUSIP]] (for 
example, T+3) maintained in [[NSCC]] Master 
Files 
• Fund/SERV determines whether the 
calculated anticipated [[settlement]] date is a 
[[settlement]] holiday or if there is an 
intervening fund holiday. 
• If “no,” then the anticipated [[settlement]] 
date calculation is completed. 
 • Fund/SERV does not edit or verify against 
the fund calendar, but does edit against 
[[NSCC]] [[settlement]] holidays. 
• The anticipated [[settlement]] date is passed 
through to the fund company. 
• If the anticipated [[settlement]] date is 
unacceptable to the fund company, it may 
reject the trade. 
 
Note: In this chapter, the terms “fund holiday” and “fund calendar” refer to the holiday calendar in force 
for the [[CUSIP]] being traded, whether the fund company assigned the calendar at the [[participant]] or at the 
[[CUSIP]] level. 

---

## Page 54

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 49 
 
 
 
 
 
  
 
 
Trades Not Settling in U.S. Dollars (X-[[settlement]]) 
 
If the distributor has not entered a date in 
the Anticipated [[settlement]] Date field: 
 If the distributor has entered a date in the 
Anticipated [[settlement]] Date field: 
   
• Fund/SERV does not calculate the 
anticipated [[settlement]] date. It is left blank 
on the order record. 
• The fund company must create an 
anticipated [[settlement]] date in its 
confirmation. 
 • Fund/SERV does not edit or verify the 
anticipated [[settlement]] date against the 
fund calendar. 
• The anticipated [[settlement]] date is passed 
through to the fund company. 
• If the anticipated [[settlement]] date is 
unacceptable to the fund company, the 
fund company may override it with a 
subsequent transaction. 
 
FUND [[Companies]]—CONFIRMING THE TRADE 
Fund/SERV does not edit or verify the trade date submitted by the distributor against the fund 
calendar. Fund [[Companies]] may reject trades that are submitted on fund trading holidays. 
 
Trades Settling in U.S. Dollars 
If the anticipated [[settlement]] date is unacceptable to the fund company, it may reject the trade. 
 
Trades Not Settling in U.S. Dollars (X-[[settlement]]) 
 
 
If the distributor has not entered a date in 
the Anticipated [[settlement]] Date field: 
 If the distributor has entered a date in the 
Anticipated [[settlement]] Date field: 
   
• The fund company must create an 
anticipated [[settlement]] date in its 
confirmation. 
• Fund/SERV does not edit or verify the 
anticipated [[settlement]] date. 
• Fund/SERV reports the anticipated 
[[settlement]] date to the distributor by 
means of the confirmation. 
 • Fund/SERV does not edit or verify the 
anticipated [[settlement]] date against the 
fund calendar. The anticipated [[settlement]] 
date is passed through to the fund 
company. The fund company must confirm 
or reject the trade. 
• If “yes,” then the anticipated 
[[settlement]] date is rolled forward one 
day for each holiday to the next 
available business day that is neither a 
U.S. nor fund [[settlement]] holiday. 

---

## Page 55

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 50 
 
 
 
 
[[settlement]] 
If the settling trade is in U.S. dollars, if it is confirmed, if there are no cancellations or corrections, 
and if the trade is settling at [[NSCC]], [[NSCC]] will schedule the [[settlement]] date as follows: 
 
 
The [[settlement]] Date equals the trade date on the order record plus the [[settlement]] 
cycle (for example, T+3) indicated by the [[CUSIP]] on [[NSCC]]’s master files. 

---

## Page 56

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 51 
 
 
 
 
14.
Forward Dating   
 
WHY FORWARD DATING? 
The date when a distributor actually enters a trade (trade date on the distributor’s books) may or may 
not be the trade date assigned by the fund company. Some possible reasons are: 
 
• Some Luxembourg and Dublin fund [[Companies]] have cutoff times for trades (including [[NSCC]] files) 
that are too early in the day for most distributors to meet. The trades submitted by the distributor 
may be processed by the fund company on the following day. 
• Some Luxembourg and Dublin fund [[Companies]] schedule their cutoff times for trade date minus 
one. 
 
As a result, differences in trade dates can result in a reconciliation difference as well as a difference 
between the distributor’s anticipated [[settlement]] date and the fund company’s expected [[settlement]] 
date. 
 
Forward dating can be a partial solution to these problems. In forward dating, the distributor is 
permitted to enter a trade date later than its submission date. The distributor chooses to use forward 
dating to align the trade date in the order record with the actual trade date of the fund company. 
 
When to use forward dating 
Forward dating should only be used when the fund company and the distributor have 
agreed on how to use it. The November 2002 and March 2003 enhancements were first steps 
established before a considerable portion of the OFS Working Group analysis was in place. They 
were never intended to be a complete solution. BY July of 2003, the solutions were defined, and 
their implementation will take place in 2004 and 2005. These solutions will not be built as an 
extension of [[NSCC]]’s core products, because substantially new capabilities must be created. As 
noted previously, this process is not complete and further incremental improvements are being 
planned. 
 
The following chart details some current processing issues raised by time zone considerations, as 
well as their possible resolutions. To deal with your specific situations, you are encouraged to seek 
assistance from the [[NSCC]] [[Mutual Funds]] Marketing Department. See Contact Information in this 
user guide. 

---

## Page 57

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 52 
 
 
 
 
 
[[Option]] Fund Company Cutoff Procedure Effect Without 
Forward Dating 
Usefulness of 
Forward Dating 
1 The fund company runs its books at end of day 
in European time with a late-day cutoff time, 
often too early for American distributors. 
Distributor’s trade 
date is one or 
more days before 
fund company’s 
trade date. 
Very useful if 
jointly agreed to 
by distributor and 
fund company. 
2 The fund company runs its books the morning 
of the next business day for the previous 
business day. 
Fund’s trade date 
is designed to 
match distributor’s 
trade date. 
Not needed. 
3 The fund company has a cutoff time towards 
end of day, but the trade is priced the following 
business day (that is, the cutoff time is trade 
date minus one). 
Fund’s trade date 
is next business 
day after 
distributor’s trade 
date. 
Useful if jointly 
agreed to by 
distributor and 
fund company. 
4 The fund company runs its books at end of day, 
with a late-day cutoff time; however, the 
distributor is able to enter trades before cutoff 
by taking advantage of automated processing. 
Fund and 
distributor trade 
dates are identical. 
Not needed. 

---

## Page 58

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 53 
 
 
 
 
 
15.
Setting Up Forward Dating   
 
FUND [[Companies]]—CHOOSING SECURITY TYPES 
 
Security Type 62 
Use Security Type 62 for a [[CUSIP]] that has U.S. dollars as its base currency. The advantage of 
Security Type 62 is the enhanced processing capabilities offered by [[NSCC]]. 
 
Security Type 63 
Use Security Type 63 for a [[CUSIP]] that does not have U.S. dollars as its base currency. 
 
FUND [[Companies]]—SETTING FORWARD DATING PERMISSIONS 
To determine if forward dating would be useful for your distributors, see the previous chapter in this 
user guide, Forward Dating. 
 
To activate forward dating for a [[participant]] number, update the Fund/SERV [[Member]] Profile Update 
form. To activate forward dating for a [[CUSIP]], update the Fund/SERV Security Issue [[ID]] Form. 
Submitting one of these forms will update the appropriate Master File. 
 
 
1 Type https://portal.[[DTCC]].com and enter your User [[ID]] and password.  
2 Click Connectivity. 
The Introduction to Connectivity page appears with general information and a list of options. 
3 Under either Master Profile Forms or Security Issue [[ID]] Forms, click Add or Modify. 
4 Update the form according to the standard instructions. (See the note at the end of this procedure 
for details.) 
 
 
 
5 In the Future Trade Date Indicator field, click Yes. 
 
 


---

## Page 59

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 54 
 
 
 
 
6 Type the number of business days into the future you will allow forward dating by the distributor. 
The [[NSCC]] [[default]] is 45 business days. Daily valued funds should set a much narrower range. 
 
 
 
STANDARD INSTRUCTIONS FOR CHOOSING AND SUBMITTING PROFILE FORMS 
1 On the Web, go to https://portal.[[DTCC]].com and log in. 
 and log in as a [[Member]]. 
2 Click Mutual Fund Services. 
3 Under Mutual Fund Services, click Fund/SERV. Then click Fund/SERV Technical Manual, 
then Chapter 3 – Establishing a new Fund/SERV [[Member]]. 
4 For members, consult the following topics: 
• Fund/SERV [[Member]] Profile 
• [[Member]] Profile Field Descriptions 
5 For individual CUSIPs, consult the following topics: 
• Mutual Fund Security Profile 
• Mutual Fund Security Profile Field Descriptions 
 
 
DISTRIBUTORS—CODING TRADE ENTRIES 
The Trade Date Forward Indicator in a Fund/SERV Order (001) or Exchange (015) record needs to 
be set. See the chapters on using forward dating in this user guide for details. 
 
Note: The above procedure only concerns updating the currency type. For specific instructions on how to 
choose which form to use and how to fill out and submit it, [[DO]] the following: 

---

## Page 60

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 55 
 
 
 
 
 
16.
Using Forward Dating (without Holiday Calendars)   
 
 
 
 
DISTRIBUTORS—ENTERING A TRADE 
The Trade Date Forward Indicator in a Fund/SERV Order (001) or Exchange (015) record must be 
set as follows: 
 
This value Indicates 
0 or blank 
or “ 
Trade date not forwarded. On an original order, the indicator must be 0 (zero), 
blank (spaces), or “ (double quotes) if the trade date is equal to the submission 
date. 
1 Trade date forwarded. On an original order, the indicator must be 1 if the trade 
date is greater than the submission date. 
2 Trade date corrected. On a correction, the indicator must be 2 if the trade date on 
the original order is not equal to the current trade date. 
 
The distributor may override the calculated [[settlement]] date by entering a date in the Anticipated 
[[settlement]] Date field. 
 
[[NSCC]]—TRADE DATE EDITING AND VERIFICATION 
[[NSCC]] requires that: 
 
 
• The distributor has properly set the Trade Date Forward Indicator on the Order or 
Exchange record. 
• The fund company accepts forward dates, based on the Future Trade Date Indicator in the 
[[NSCC]] files for the specific [[participant]] or [[CUSIP]]. 
 
[[NSCC]] edits an order with a forward date as follows: 
 
 
• If the forward date is a Saturday or Sunday, the trade is rejected. 
• [[NSCC]] edits the number of forwarded days against the range indicator set up by the fund 
company for that [[participant]] or [[CUSIP]] on the [[NSCC]] Master Files. 
 
[[NSCC]]—[[settlement]] DATE PROCESSING 
[[NSCC]] calculates the anticipated [[settlement]] date from the forward trade date. 
 
FUND [[Companies]]—CONFIRMING THE TRADE 
When the fund company confirms the trade, it cannot override a forward trade date. 
 
Reminder: A fund company can assign forward dating at either the [[participant]] level or the [[CUSIP]] level. 

---

## Page 61

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 56 
 
 
 
 
Trades Settling in U.S. Dollars  Trades Not Settling in U.S. Dollars (X- 
[[settlement]]) 
   
A fund company may not override a [[settlement]] 
date if [[settlement]] is to be made in U.S.  
dollars. 
 There are no forward dating considerations. 
 
 
[[settlement]] 
If the settling trade is confirmed, if there are no cancellations or corrections, if the trade is in U.S. 
dollars, and if the trade is settling at [[NSCC]], [[NSCC]] will schedule the [[settlement]] date as follows: 
 
 
The [[settlement]] date equals the trade date on the order record plus the [[settlement]] 
cycle (for example, T+3) indicated by the [[CUSIP]] or [[participant]] on [[NSCC]]’s master 
files. 

---

## Page 62

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 57 
 
 
 
 
 
17.
Using Holiday Calendars and Forward Dating Together   
 
 
 
 
DISTRIBUTORS—ENTERING A TRADE 
Fund/SERV does not edit or verify the trade date submitted by the distributor against the fund 
calendar. However, distributors may view the fund calendars for trading holidays. See Holiday 
Calendars on PCWeb Direct: [[participant]] and [[NSCC]] Usage in this user guide for details. 
 
The Trade Date Forward Indicator in a Fund/SERV Order (001) or Exchange (015) record must be set 
as follows: 
 
This value Indicates 
0 or blank 
or “ 
Trade date not forwarded. On an original order, the indicator must be 0 (zero), 
blank (spaces), or “ (double quotes) if the trade date is equal to the submission 
date. 
1 Trade date forwarded. On an original order, the indicator must be 1 if the trade 
date is greater than the submission date. 
2 Trade date corrected. On a correction, the indicator must be 2 if the trade date on 
the original order is not equal to the current trade date. 
 
There is normally no need for the distributor to override the calculated [[settlement]] Date by entering a 
date in the Anticipated [[settlement]] Date field. 
 
[[NSCC]]—TRADE DATE EDITING AND VERIFICATION 
[[NSCC]] requires that: 
• The distributor has properly set the Trade Date Forward Indicator on the Order or 
Exchange record. 
• The fund company accepts forward dates, based on the Future Trade Date Indicator in the 
[[NSCC]] files for that [[participant]]. 
 
[[NSCC]] edits an order with a forward date as follows: 
• If the forward date is a Saturday or Sunday, the trade is rejected. 
 
 
 
Note: In the following chapter, the terms “fund holiday” and “fund calendar” refer to the holiday calendar 
in force for the [[CUSIP]] being traded, whether the fund company assigned the calendar at the [[participant]] or 
at the [[CUSIP]] level. 
 
Also, the fund company can assign forward dating at either the [[participant]] level or the [[CUSIP]] level. 
 
Warning: In the current release there is no editing to determine if the forward date is a fund 
trading holiday. 

---

## Page 63

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 58 
 
 
 
 
• [[NSCC]] edits to ensure that the forward date is not a U.S. trading holiday: 
• A settling trade is rejected if the forward date is a U.S. trading holiday. 
• A non-settling trade is allowed if the forward date is a U.S. trading holiday. 
• [[NSCC]] edits the number of forwarded days against the range indicator set up for the 
[[participant]] or [[CUSIP]] on the [[NSCC]] Master Files. Fund holidays are part of this edit process. 
 
[[NSCC]]—[[settlement]] DATE PROCESSING 
 
 
Trades Settling in U.S. Dollars  Trades Not Settling in U.S. Dollars (X- 
[[settlement]]) 
   
The forward date becomes the trade date and 
thus the basis for calculating [[settlement]] date. 
For holiday calendar processing, see Using 
Holiday Calendars (without Forward Dating) in 
this user guide. 
 There is no forward date processing. For 
holiday calendar processing, see Using Holiday 
Calendars (without Forward Dating) in this 
user guide. 
 
 
FUND [[Companies]]—CONFIRMING THE TRADE 
When the fund company confirms the trade, it cannot override a forward trade date. 
 
 
Trades Settling in U.S. Dollars  Trades Not Settling in U.S. Dollars (X- 
[[settlement]]) 
   
A fund company may not override a [[settlement]] 
date if [[settlement]] is to be made in U.S.  
dollars. 
 There are no forward date considerations. For 
holiday calendar processing, see Using Holiday 
Calendars (without Forward Dating) in this 
user guide. 
 
 
[[settlement]] 
If the settling trade is confirmed, if there are no cancellations or corrections, if the trade is in U.S. 
dollars, and if the trade is settling at [[NSCC]], [[NSCC]] will schedule the [[settlement]] date as follows: 
 
 
The [[settlement]] Date equals the trade date on the order record plus the [[settlement]] 
cycle (for example, T+3) indicated by the [[CUSIP]] on [[NSCC]]’s master files. 

---

## Page 64

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 59 
 
 
 
 
18.
Scenarios: Using Holiday Calendars and Forward Dating Together   
 
 
In the following four scenarios, the terms “fund calendar,” “ fund holiday,” “trading holiday,” and 
“[[settlement]] holiday” refer to the holiday calendar in force for the [[CUSIP]] being traded, whether the 
fund company assigned the calendar at the [[participant]] or at the [[CUSIP]] level. 
 
Also, the fund company can assign forward dating at either the [[participant]] level or the [[CUSIP]] level. 

---

## Page 65

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 60 
 
 
The trade goes through with a submission date of Monday, May 19, and a trade date
of Tuesday, May 20. The [[settlement]] date is Friday, May 23. 
 
 
 
SCENARIO 1: SECURITY TYPE 62, FORWARD DATING, NO HOLIDAYS 
Distributor X in San Francisco submits a buy order for a Type 62 [[CUSIP]] with Fund Company Y, 
headquartered in Dublin. The cutoff time for trade submission is 3 p.m. Greenwich mean time, which 
is 7 a.m. Pacific time. The trade is submitted on Monday, May 19, 2003 at 11 a.m. Pacific time, thus 
missing the cutoff time. To allow for this, the distributor sets the Forward Date Indicator, indicates a 
forward date of Tuesday, May 20, and does not override the [[settlement]] date. The trade is to settle in 
dollars at [[NSCC]]. 
 
Fund Company Y allows forward dating and there are no trade or [[settlement]] holidays that week either 
for the distributor or the fund company. The fund company uses the forward dating range of three 
days. [[settlement]] is T+3. 
 
After [[NSCC]] edits, the fund company does not attempt to override the [[settlement]] date. After 
confirmation, there are no cancellations or corrections. 
 
 
TABLE 1. SCENARIO 1 BREAKDOWN 
 
Details Validation by [[NSCC]] Result 
Security Type 62 (USD) Follow USD processing logic OK 
Fund company allows trade date forward with three 
day limit 
Follow forwarding logic OK 
Distributor sets Trade Date indicator to “1” and 
forward date to the next day 
Forward trade date is greater than 
today’s date 
OK 
Distributor does not override [[settlement]] date Follow non-override logic OK 
Trade submission date is not a U.S. holiday Validated by [[NSCC]] against U.S. holiday 
calendar 
OK 
Trade submission date is not a fund holiday Not validated by [[NSCC]] OK 
Forward date is not a U.S. holiday Validated against U.S. holiday calendar OK 
Forward date is not a fund holiday Not validated by [[NSCC]] OK 
Forward date is not a Saturday or Sunday Validated against [[NSCC]] standard 
calendar 
OK 
There are no fund holidays during [[settlement]] period Validated against fund calendar OK 
[[settlement]] date is not a Saturday or Sunday Validated against [[NSCC]] standard 
calendar 
OK 
After [[NSCC]] edits, the fund company does not 
attempt to override the [[settlement]] date 
 OK 
   

---

## Page 66

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 61 
 
 
The trade goes through with a submission date of Thursday, May 22, and a trade
date of Friday, May 23. One day is added to the [[settlement]] period to account for U.K. 
Spring Bank Holiday. The [[settlement]] date is Thursday, May 29. 
Note that the U.S. holiday does not impact this scenario because it is identical to the 
fund’s [[settlement]] holiday. 
 
 
SCENARIO 2: SECURITY TYPE 62, FORWARD DATING, [[settlement]] HOLIDAYS 
This is the same as Scenario 1 with the following exceptions: 
• The trade is entered on Thursday, May 22, 2003. 
• Monday, May 26, is a U.S. [[settlement]] holiday (Memorial Day observed). 
• Monday, May 26, is also a fund [[settlement]] holiday (U.K. Spring Bank Holiday), as declared in 
the holiday calendar for that [[CUSIP]]. 
 
 
TABLE 2. SCENARIO 2 BREAKDOWN 
 
Details Validation by [[NSCC]] Result 
Security Type 62 (USD) Follow USD processing logic OK 
Fund company allows trade date forward with three 
day limit 
Follow forwarding logic OK 
Distributor sets Trade Date indicator to “1” and 
forward date to the next day 
Forward trade date is after today’s date OK 
Distributor does not override [[settlement]] date Follow non-override logic OK 
Trade submission date is not a U.S. holiday Validated against U.S. holiday calendar OK 
Trade submission date is not a fund holiday Not validated by [[NSCC]] OK 
Forward date is not a U.S. holiday Validated against U.S. holiday calendar OK 
Forward date is not a fund holiday Not validated by [[NSCC]] OK 
Forward date is not a Saturday or Sunday Validated against [[NSCC]] standard 
calendar 
OK 
There is one fund holiday during [[settlement]] 
period 
Validated against fund calendar OK 
[[settlement]] date is not a Saturday or Sunday Validated against [[NSCC]] standard 
calendar 
OK 
After [[NSCC]] edits, the fund does not attempt to 
override the [[settlement]] date 
 OK 
   

---

## Page 67

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 62 
 
 
The trade goes through with a submission date of Friday, May 2, and a trade date of
Tuesday, May 6. The [[settlement]] date is Friday, May 9. 
 
 
 
SCENARIO 3: SECURITY TYPE 62, FORWARD DATING, HOLIDAY ANTICIPATED BY 
DISTRIBUTOR 
This is the same as Scenario 1 with the following exceptions: 
• The trade is entered on Friday, May 2, 2003. 
• Monday, May 5, is a [[settlement]] holiday for that [[CUSIP]] (U.K. May Day Bank Holiday). 
• The distributor notes the holiday and sets the forward date to Tuesday, May 6, to account for 
both the intervening weekend and the Monday holiday. 
 
 
TABLE 3. SCENARIO 3 BREAKDOWN 
 
Details Validation by [[NSCC]] Result 
Security Type 62 (USD) Follow USD processing logic OK 
Fund company allows trade date forward with three 
day limit 
Follow forwarding logic OK 
Distributor sets Trade Date indicator to “1” and 
forward date to next business day in U.K. 
Forward trade date is greater than 
today’s date 
OK 
Distributor does not override [[settlement]] date Follow non-override logic OK 
Trade submission date is not a U.S. holiday Validated against U.S. holiday calendar OK 
Trade submission date is not a fund holiday Not validated by [[NSCC]] OK 
Forward date is not a U.S. holiday Validated against U.S. holiday calendar OK 
Forward date is not a fund holiday Not validated by [[NSCC]]; however, 
distributor has taken U.K. holiday 
into account 
OK 
Forward date is not a Saturday or Sunday Validated against [[NSCC]] standard 
calendar 
OK 
There are no fund holidays during [[settlement]] period Validated against fund holiday calendar OK 
[[settlement]] date is not a Saturday or Sunday Validated against [[NSCC]] standard 
calendar 
OK 
After [[NSCC]] edits, the fund does not attempt to 
override the [[settlement]] date 
 OK 
   

---

## Page 68

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 63 
 
 
The trade goes through with a submission date of Monday, May 19, and a trade date
of Tuesday, May 20. The [[settlement]] date is Friday, May 23. 
 
 
 
SCENARIO 4: SECURITY TYPE 63, FORWARD DATING, NO HOLIDAYS 
This is the same as Scenario 1, except that the [[CUSIP]] is a Security Type 63, denominated in pounds 
sterling. The cash will settle in London. 
 
After [[NSCC]] edits, the fund company creates a [[settlement]] date of Friday, May 23, in its confirmation. 
After confirmation, there are no cancellations or corrections. 
 
 
TABLE 4. SCENARIO 4 BREAKDOWN 
 
Details Validation by [[NSCC]] Result 
Security Type 63 (non- USD) Follow non-USD processing logic OK 
Fund company allows trade date forward with three 
day limit 
Follow forwarding logic OK 
Distributor sets Trade Date indicator to “1” and 
forward date to the next day 
Forward trade date is after today’s date OK 
Distributor does not override [[settlement]] date Follow non-override logic OK 
Trade submission date is not a U.S. holiday Validated against U.S. holiday calendar OK 
Trade submission date is not a fund holiday Not validated by [[NSCC]] OK 
Forward date is not a U.S. holiday Validated against U.S. holiday calendar OK 
Forward date is not a fund holiday Not validated by [[NSCC]] OK 
Forward date is not a Saturday or Sunday Validated against [[NSCC]] standard 
calendar 
OK 
There are no fund or U.S. holidays during 
[[settlement]] period 
Validated against fund holiday calendar 
and against U.S. holiday calendar 
OK 
[[settlement]] date is not a Saturday or Sunday Validated against [[NSCC]] standard 
calendar 
OK 
After [[NSCC]] edits, the fund company does not 
attempt to override the [[settlement]] date 
 OK 
   

---

## Page 69

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 64 
 
 
 
 
 
Appendix A: Glossary   
 
 
[[CUSIP]] A security identified by the 9-digit security identification numbering 
system used in the U.S. market. This term is used when describing 
[[NSCC]] processing at a detailed level, especially holiday calendar 
processing. (The term ISIN will not be used.) 
Distributor A [[Broker]] or other firm that sells [[Mutual Funds]]. (In other [[NSCC]] 
documentation, the distributor may be referred to as the “firm.” 
Also, note that this user guide will not use this term to refer to a 
fund company.) 
Fund A fund company, fund family, portfolio, or share class, when it is 
obvious from context and inconvenient to be more specific. 
Fund company A fund management company. 
Fund family A fund family or fund group. 
Fund group (To avoid confusion, this term is not used in this user guide) 
Fund/SERV Master File [TBD] See also Security Issue [[ID]] Master File. 
  Group (To avoid confusion, this term is not used in this user guide) 
Grouping An entity created by the fund to accommodate holiday calendar 
processing. It has its own [[participant]] number and holiday calendar. 
(Note that this term has been devised to clarify holiday calendar 
concepts. It is not an industry standard term nor is it used 
elsewhere in [[NSCC]] in this sense.) 
ISIN International [[securities]] Identification Number. (This term will not be 
used in this user guide. See [[CUSIP]].) 
Master File See Fund/SERV Master File and Security Issue [[ID]] Master File. 
[[participant]] An entity represented by an [[NSCC]] [[participant]] number. Also known as 
a [[Member]]. This term will be used when describing [[NSCC]]     
processing at a detailed level, especially holiday calendar processing. 
In practice, this may be a fund company, a fund family, a holiday 
calendar grouping, or some other grouping devised by the fund 
company for its processing and reporting convenience. 
Portfolio One specific mutual fund. If there are no share classes, it has one 
unique [[CUSIP]] number and one security type. If there are share 
classes, it does not have its own [[CUSIP]] number or security type; 
each share class does. 
Pseudo NAV funds [[Mutual Funds]] based in Luxembourg or Dublin where each investment 
portfolio reports NAVs in more than one currency per [[CUSIP]], based 
on a foreign exchange rate 
Security (This term will not be used in this user guide.) 

---

## Page 70

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 65 
 
 
 
 
Security Issue [[ID]] Master 
File 
[TBD] See also Fund/SERV Master File. 
Security type A specific [[NSCC]] processing type for a [[CUSIP]]. Security types covered 
in this user guide include 25, 26, 59, 62, and 63. For details see 
Security Types in this user guide. 
Security Type 25 A domestic security type for funds regulated by the [[securities]] & 
Exchange Commission and set to U.S. standards. These were 
originally load funds, typically sold by full-service brokers and 
typically settling at T+3. However, the [[settlement]] cycle can be 
specified on the Fund/SERV Security Issue [[ID]] Form. 
Security Type 26 A domestic security type for funds regulated by the [[securities]] & 
Exchange Commission and set to U.S. standards. These were 
originally no-load funds, typically sold by discount brokers and 
typically settling at T+1. However, the [[settlement]] cycle can be 
specified on the Fund/SERV Security Issue [[ID]] Form. 
Security Type 59 An offshore fund using [[NSCC]]’s Mutual Fund Services that elects to 
use [[NSCC]] processing features that mirror U.S. holidays and 
processes, and that trades and settles only in U.S. dollars. 
Security Type 62 An offshore fund using [[NSCC]]’s Mutual Fund Services that elects to 
use the offshore enhancements and has a base currency in U.S. 
dollars. 
Security Type 63 An offshore fund using [[NSCC]]’s Mutual Fund Services that elects to 
use the offshore enhancements and has a base currency other than 
U.S. dollars. 
Share class A category of [[shares]] with its own cost structure (Class “A” [[shares]], 
Class “B” [[shares]], and so forth) that exists in a portfolio. Each share 
class in the portfolio has its own [[CUSIP]] number. 
Single [[CUSIP]], Single 
Currency 
[[Mutual Funds]] based in Luxembourg and Dublin where each 
investment portfolio has separate share classes per currency 
[[transfer agent]] The operational role of [[transfer agent]], whether or not the role is 
performed by the fund company or outsourced to a third party. 
X-[[settlement]] Cross-[[settlement]]. Trades that [[DO]] not settle via [[NSCC]] [[settlement]], 
but have [[settlement]] exposures calculated by [[NSCC]]. Non-dollar 
trades at [[NSCC]] are X-[[settlement]] 

---

## Page 71

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 66 
 
 
 
 
 
Appendix B: Converting to Security Types 62 and 63   
 
 
Most “Pseudo NAV” and “Pseudo Classes of [[shares]]” funds are already part of Fund/SERV via one of 
the existing security types (25, 26, 59). (For more details see Multi-Currency for Luxembourg and 
Dublin Funds in this user guide.) 
 
Therefore, the fund company must consider support of its existing businesses and distributors as well 
as its ability to leverage the November 2002 release (and subsequent releases) for future business. 
Here are some of the factors relevant to decisions being made by the fund. 
 
[[NSCC]] Mutual Fund Marketing will be available to assist fund [[Companies]] and their transfer 
agents as they discuss these factors. See Contact Information in this user guide. 
 
FREQUENTLY ASKED QUESTIONS 
 
1. What is the best way to use Networking and Commission [[settlement]] today for  
a fund that is multi-currency, until such time as these products are enhanced to 
add more offshore functionality? 
If a “Pseudo NAV” or a “Pseudo Classes of [[shares]]” fund is presently using Networking and 
Commission [[settlement]] with [[settlement]] [[obligations]] in U.S. dollars, and if a [[CUSIP]] within the fund 
family converts to Security Type 62, it can continue to use Networking and Commission 
[[settlement]] as before, with no adverse consequences. However, it will not be able to support 
Networking and Commission [[settlement]] in non-U.S. dollars in the interim until [[NSCC]] makes 
subsequent adjustments. 
 
If the fund company converts a [[CUSIP]] to Security Type 63, it should not use Networking and 
Commission [[settlement]], because [[Dividend]] and commission payments must be in US dollars and 
[[settlement]] [[obligations]] are created. 
 
The key difference between the operational capability of “Pseudo NAV” and “Pseudo Classes of 
[[shares]]” funds may be important to this question: 
 
• A “Pseudo NAV” [[CUSIP]] may have difficulty supporting a U.S. dollar Networking and 
Commission [[settlement]] if it is also accepting [[NSCC]] trades in euros. 
• “Pseudo Classes of [[shares]]” CUSIPs may be able to support U.S. dollar Networking and 
Commission [[settlement]] for their U.S. dollar sub-[[Ledger]] and accept [[NSCC]] trades in euros via a 
euro sub-[[Ledger]]. 
 
2. How can the Profile Price & Rate file be used for funds that are multi-currency? 
If a “Pseudo NAV” [[CUSIP]] is a daily [[Dividend]] fund it is likely to accrue in the base currency only. A 
“Pseudo Classes of [[shares]]” [[CUSIP]] that is a daily [[Dividend]] fund may accrue in all currencies. If 
accrual is only in the base currency, it may be best to use the prospectus base currency for Profile 

---

## Page 72

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 67 
 
 
 
 
Price & Rate file, and to inform all distributors that the information in the Profile Price & Rate file is 
base currency. 
 
If a [[CUSIP]] is not a daily [[Dividend]] fund or can accrue daily dividends in multiple currencies, it must 
make a business decision as to which currency to display in the Price & Rate file. 
 
• For Security Type 62, it is assumed that the Price & Rate file is in U.S. dollars. Reporting of 
non-U.S. dollar prices and rates will continue to be manual. 
• For Security Type 63, it is assumed that the Price & Rate file is in the [[CUSIP]]’s stated base 
currency set out in the [[CUSIP]] Master File. The fund company must inform its distributors  
which currency is being used in the Price & Rate file. Reporting of a second currency for prices 
and rates will continue manually until further enhancements are made by [[NSCC]]. 
 
3. What impact does conversion to Security Type 62 or 63 have on current or 
prospective distributors? 
If the fund company elects to designate a [[CUSIP]] as Security Type 62, distributors that [[DO]] not 
upgrade to support trading in Security Types 62 and 63 must enter the trade the regular way. 
[[NSCC]] will [[default]] the trade to U.S. dollars. A distributor wishing to purchase the “Pseudo NAV” 
[[CUSIP]] in non-U.S. dollars as a Security Type 62 must have its system upgraded to show the 
Currency Code and X-[[settlement]] Indicators before it can enter the trade record. 
 
If the fund company elects to designate a [[CUSIP]] as Security Type 63, distributors that want to 
continue to trade the [[CUSIP]] in U.S. dollars must make the upgrade. The trade record must show 
U.S. dollars in the Currency field. 
 
 
 
Funds should be consistent in their use of [[NSCC]] products with respect to multi-currency. If, for 
example, Networking were run in U.S. dollars and Profile Price & Rate in euros there could be 
some confusion. [[Dividend]] reinvestment would be in one currency for NAV (value) in Networking 
and another currency (value) in the Price & Rate file. [[Dividend]] accruals in the Price & Rate file 
would be in a different currency from the dividends stated in Networking. 
 
4. When and how will [[NSCC]] enhance Profile Price & Rate file, Networking, and 
Commission [[settlement]] to support multiple currencies? 
[[NSCC]]’s Product Management and IT staff are developing solutions that will complete straight- 
through processing (STP) and straight-through reporting (STR) for fund [[Companies]] and 
distributors. As of July of 2003, the solutions have been defined, and implementation will take 
place in 2004 and 2005. 
 
Note: [[NSCC]] will reject trades for Security Type 63 CUSIPs that fail to show a [[settlement]] Override of “06” 
if not in U.S. dollars, or [[DO]] not show the currency code if in U.S. dollars. 

---

## Page 73

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 68 
 
 
 
 
In general, these solutions will not be built as extensions to [[NSCC]]’s core products, because to 
solve fully the issues of multi-currency, multi-time zone, and multiple processing cycles, 
substantially new capabilities must be created. 
 
As appropriate, modifications will be made to the Profile Price & Rate file, Networking, and 
Commission [[settlement]]. 

---

## Page 74

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 69 
 
 
 
 
 
Appendix C: About [[NSCC]] Mutual Fund Products & Services   
 
 
For detailed information about [[NSCC]] [[Mutual Funds]] products and services, please contact [[NSCC]]’s 
[[Mutual Funds]] Marketing Group. See Contact Information in this user guide. 
 
FUND/SERV 
Fund/SERV is the industry standard for processing and settling of investment funds, including both 
1940 Act and other pooled investment products for investment [[Companies]], money managers and 
financial intermediaries. The service provides standardized formats and centralized processing of 
purchase, redemption, and exchange orders, account registrations, and provides participants with a 
single daily net [[settlement]]. 
 
Fund/SERV offers 29 processing cycles over 22 hours, giving trading partners convenient access to a 
single automated trading platform. Fund/SERV significantly reduces the time and cost of processing 
transactions. 
 
Fund/SERV is accessible via CPU-to-CPU links, PCWeb Direct—a Web interface that allows [[NSCC]] 
participants direct access to [[NSCC]] services over the Internet, and with Fund/SPEEDSM—[[NSCC]]'s XML 
interface. 
 
Any qualified and interested [[NSCC]] members can participate in Fund/SERV. Special mutual fund-only 
memberships are available. 
 
MUTUAL FUND PROFILE SERVICE (MFPS): PRICE & RATE 
Mutual Fund Profile Service (MFPS) automates the flow of information between [[NSCC]] participants in a 
centralized system, using standardized formats. Two distinct MFPS services, Price & Rate and 
[[participant]] & Product & Distribution, allow participants to exchange accurate and timely information of 
daily prices and [[Dividend]] rates, firm and fund [[Member]] profiles, individual security data, and projected 
and actual distribution declarations. 
 
Price & Rate files report daily Net [[Asset]] Value (NAV) and daily distribution rates for individual mutual 
funds for a specific date. Both firms and funds can receive Price & Rate files and have the [[Option]] also 
to receive the National Association of Security Dealers, Inc. ([[NASD]]) Price file. [[NSCC]] stores Price & 
Rate information for 90 days and [[NASD]] information for 30 days. Files are processed as single and 
multiple batch transmissions. 
 
MFPS Price & Rate is accessible via CPU-to-CPU links, or through PCWeb Direct. 
 
NETWORKING 
Networking is an automated, centralized record-keeping system through which all customer account 
activities can be exchanged by participants. The service provides accurate, timely updates in a 

---

## Page 75

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 70 
 
 
 
 
controlled environment. A standard format uniformly reports account positions, activity and [[Dividend]] 
information, and registration updates between investment [[Companies]] or their transfer agents and 
financial intermediaries. Dividends may be settled through [[NSCC]]'s net [[settlement]] [[Option]]. 
 
Participants choose one of four types of reporting options, based on the structure of their business and 
reporting responsibilities. Although Networking does not require Fund/SERV participation, the two 
services work best when used in conjunction with each other. 
 
With Networking, financial intermediaries are able to maintain fully reconciled client sub-account 
information with the information maintained at investment [[Companies]]. Networking participants are 
able to generate consolidated statements with the most current and accurate information available. 
 
Networking is accessible via CPU-to-CPU links, or through PCWeb Direct. 
 
COMMISSION [[settlement]] 
Commission [[settlement]] is the most efficient method of accurately reporting fund commission 
information to financial services firms. Using a standard format in [[NSCC]]'s centralized processing 
environment, the service supports all types of fund commissions including Contingent Deferred Sales 
Charge (CDSC) payouts, 12b-1 fees (or trail commissions), or other types of payments. [[settlement]] 
occurs through [[NSCC]]'s [[settlement]] system. 
 
Commission [[settlement]] is accessible via CPU-to-CPU links, or through PCWeb Direct. Transmissions 
are limited to no more than two hours per file. 
 
Any interested financial organization that meets [[NSCC]] qualifications can use the service. Commission 
[[settlement]] requires that participants be qualified to settle at [[NSCC]]. 

---

## Page 76

  April 2004   
Fund/SERV Applications for Offshore Trading and [[settlement]] > 71 
 
 
 
 
 
Appendix D: Obtaining a Digital Certificate for Offshore Fund/SERV   
 
 
This information will be distributed as a separate manual. 