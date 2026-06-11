---
title: "FICC GSD RTTM® WFE Member User Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd207_gsd_rttm_wfe_member_user_guide.pdf"
pages: 276
size: "11875.4 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# FICC GSD RTTM® WFE Member User Guide

**Original File:** [gsd207_gsd_rttm_wfe_member_user_guide.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd207_gsd_rttm_wfe_member_user_guide.pdf)  
**Category:** GSD  
**Total Pages:** 276  
**File Size:** 11875.4 KB  

---

## Page 1

 
 
 
[[FICC]] – [[GSD]]  
[[FICC]] [[GSD]] RTTM® WFE [[Member]] USER GUIDE 
VERSION 1.0.1 
JULY 2023 
 


---

## Page 2

 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by  certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in wh ich such entity operates. Please see 
www.[[DTCC]].com  for more information on [[DTCC]], its affiliates and the services they offer.  
 
 
Doc Date: July 2023 
Publication Code:  GSD207 
Service: [[FICC]] – [[GSD]]  
Title: [[FICC]] [[GSD]] RTTM
® WFE [[Member]] User Guide 
 
 
The [[FICC]] [[GSD]] RTTM® WFE [[Member]] User Guide (hereinafter, the "document ") is provided as a convenience to [[Member]] s 
and is for information purposes only. Although [[FICC]] may make this document  available to Members, it shall be under no 
obligation to [[DO]] so, nor having once or more done so, shall [[FICC]] have a continuing obligation to make available this 
document  or other related information of a certain type.   
 
[[FICC]] does not represent the accuracy, adequacy, timeliness, completeness, or fitness for any particular purpose 
of any information provided to M embers in this document , which is provided as -is. [[FICC]] shall not be liable for any 
loss related to such information (or the act or process of providing such information) resulting directly or 
indirectly from mistakes, errors, or omission s, other than those caused directly by gross negligence or willful 
misconduct on the part of [[FICC]]. [[FICC]] shall not be liable for: (1) any loss resulting directly or indirectly from 
interruptions, delays, or defects arising from or related to providing this guide; and (2) any special, consequential, 
exemplary, incidental, or punitive damages.  
 
Further, the information contained in this document is subject to change. Members  and other authorized users of the 
document  will find the most current version of the document on [[DTCC]]’s Learning Center  site, www.dtcclearning.com. 
[[FICC]] shall bear no responsibility for any losses associated with the failure of Members or other authorized users to follow  
[[FICC]]’s most current docum ent. 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
About the Real-Time Trade Matching (RTTM®) Web Application .......................................................... 6  
About This Guide ............................................................................................................................. 7  
Access to [[FICC]] GS D RTTM Web ....................................................................................................... 8  
Pr ovisionin g U ser  Acce ss ................................................................................................................ 8  
Login into the [[GSD]] RTTM Web application ......................................................................................... 8  
Us ing the Prod uct Sp ec ific URL ........................................................................................................ 9  
Login into the RTTM Web Application ............................................................................................... 9  
Using the General URLs through MyDTCC ....................................................................................... 10 
Timing Out................................................................................................................................... 11 
[[GSD]] RTTM Web Navigation Bar .......................................................................................................12  
Navigation Toolbar........................................................................................................................ 12  
Contact U s .................................................................................................................................. 13 
Logout ........................................................................................................................................ 13 
Alerts .......................................................................................................................................... 14 
[[GSD]] Dashboard ..............................................................................................................................15  
DVP D as hbo ard ........................................................................................................................... 16 
Current Day Statis tics .................................................................................................................. 16 
Historical Statistics ...................................................................................................................... 21 
GCF D as hbo ard ........................................................................................................................... 25 
GCF Dashboard – Bro k er View...................................................................................................... 25 
GCF Dashboard – Dealer/CCIT View ............................................................................................. 31 
Useful Information and Links .......................................................................................................... 38 
Trades............................................................................................................................................40  
Trades > Entry ............................................................................................................................. 40 
DVP Trad e Entry ......................................................................................................................... 41 
GCF Trad e Entry ......................................................................................................................... 63 
Trades > Search & Management..................................................................................................... 83 
DVP Trade Search & Management ................................................................................................ 83 

---

## Page 4

 
 
GCF / CCIT Trade Search & Management .....................................................................................104  
Trades > Advisory Management ....................................................................................................124  
DVP Advisories ..........................................................................................................................124  
GCF / CCIT Adv iso ries ................................................................................................................133  
Trades > Rejects .........................................................................................................................136  
Trade Rejects Search .................................................................................................................137  
Trade Rejects Search Results ......................................................................................................139  
Trades > CCIT Trade Fund Allocation (Reserved for Future Use)........................................................145  
[[obligations]]................................................................................................................................... 146 
Quick Search – [[obligations]] ...........................................................................................................146  
Advanced Search – O bliga tion s .....................................................................................................150  
Substitutions ................................................................................................................................ 155 
Substitutions > Entry ....................................................................................................................155  
Subs titution Entry for Dealer Submitter ..........................................................................................156  
Substitution Entry for [[Broker]] Submitter ..........................................................................................168  
Examples of Invalid Substitution Entries.........................................................................................180  
Subs titutions > Search & Management ...........................................................................................185  
Substitutions Search for Dealer Submitter ......................................................................................185  
Substitutions Management for Dealer Submitter ..............................................................................186  
Substitutions Search for [[Broker]] Submitter ......................................................................................201  
Substitutions Management for [[Broker]] Submitter ..............................................................................201  
Tools............................................................................................................................................ 219 
Tools > Security Search................................................................................................................219  
DVP [[securities]]...........................................................................................................................220  
GCF [[securities]] ..........................................................................................................................227  
Tools > Product Search ................................................................................................................229  
DVP Prod uct Typ es ....................................................................................................................229  
GCF Prod uc t Typ es ....................................................................................................................232  
To ols > Co ntac t Manag ement ........................................................................................................234  
Acc ess ing the [[FICC]] [[GSD]] Co ntac t List ...........................................................................................234  

---

## Page 5

 
 
View All [[GSD]] Contacts................................................................................................................234  
Adding, Updating or Deleting Contact Information............................................................................235  
Who to Contact for Issues............................................................................................................241  
Tools > CCLF..............................................................................................................................242  
Acc ess ing the CCLF Ob lig atio ns Manag ement sc reen .....................................................................242  
Overview of the CCLF [[obligations]] Management Screen...................................................................243  
Tools > DVP Bulk Trade Upload (Only Available for Contingency Purposes).........................................253  
Acc ess ing the D VP Bulk Trad e Up lo ad Too l in [[GSD]] RTTM Web .......................................................253  
Up lo ading , Valid ating  and Co nfirming  Sub mitted  Trad es ..................................................................254  
Reports ........................................................................................................................................ 267 
Acc ess ing [[FICC]] Repo rt Center – [[GSD]] Reports ................................................................................267  
[[FICC]] Report Center – [[GSD]]  Repo rts ...............................................................................................268  
How to Use [[FICC]] Report Center – [[GSD]]  Repo rts ..............................................................................269  
Guides and Other Learning Materials ............................................................................................269  
Report Center Quick Tips ............................................................................................................269  
Common Icons and Buttons in RTTM Web...................................................................................... 271 
Other Miscellaneous Features ....................................................................................................... 273 
Accessing Support ....................................................................................................................... 275 
 

---

## Page 6

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
About the R eal-Time Trade Matchi ng (RTTM®) Web Application 6 
ABOUT THE REAL-TIME TRADE MATCHING (RTTM®) 
WEB APPLICATION 
The Government [[securities]] Division (“[[GSD]]”) and the Mortgage-Backed [[securities]] Division (“MBSD”) of Fixed 
Income Clearing Corporation (“[[FICC]]”) each offer their Members a web-based interface called the Real-Time 
Trade Matching (“RTTM®”) Web, that serves as a centralized point of entry, providing transaction management 
and screen-based error resolution across fixed income instrument types. These web interfaces or applications 
are secure, browser-based trade entry/management tools that incorporate robust search capabilities, statistical 
reporting, and exception processing along with tools such as an online security search screen and a [[Member]] 
contact list.  
RTTM Web provides a common electronic platform for collecting and matching trade data, enabling the parties 
to trade, monitor and manage the status of their trade activity in real-time. Through RTTM, the parties can track 
a transaction from trade entry through clearance and regulatory reporting. Customers can submit their trades 
upon execution in real-time for matching, exchange trade status messages, submit DNA messages for pair-off 
processing, access and transmit reports, and cancel or modify trades in RTTM using one of two methods: via 
RTTM Web, the web-based user interface, or via mainframe-based interactive messages.  
Through the RTTM Web Modernization effort, the RTTM Web for [[GSD]] and MBSD underwent a web front end 
(WFE) refresh and reduced the number of screens necessary to complete certain actions. Users are able to 
access the [[GSD]] RTTM Web and MBSD RTTM Web applications via MyDTCC (formerly known as the [[DTCC]] 
Web Portal) with a single sign-on that can be used across multiple [[DTCC]] systems. Also, with this 
modernization effort [[GSD]]’s DVP and GCF RTTM Web applications were combined into a single WFE, [[GSD]] 
RTTM Web. These efforts streamlined user navigation and simplified Members’ ability to manage their trades. 
  

---

## Page 7

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
About This Guide 7 
ABOUT THIS GUIDE 
The primary purpose of this guide is to provide Members of the Fixed Income Clearing Corporation‘s (“[[FICC]]”) 
Government [[securities]] Division (“[[GSD]]”) who utilize the [[GSD]] RTTM WFE with instructions on how to navigate 
and use the functions within [[GSD]] RTTM Web. Along with such instructions, this guide will provide descriptions 
for the client facing user interface (UI) screens within the [[GSD]] RTTM Web application. This guide will cover 
such topics as: 
• Client Dashboard 
o S tatistical data and published rates 
o Quick Links and Upcoming [[FICC]] Holidays 
• Trades / Search & Management 
o Querying trades by product type, individual security, contra, or a combination of criteria 
o Querying Rejects or Advisories 
o Performing trade actions such as: 
 Trade entry 
 Trade modifications 
 Trade affirmations/comparison 
 Trade cancellations and DKs 
• [[obligations]] queries for current day and historical clearance statuses 
• Substitutions Entry, Search and Management (of related trades and [[obligations]]) 
• Tools such as Security Search, Contact Management and Bulk Trade Upload 
• Viewing intraday, end-of-day, and historical reports 
 
It should be noted that this document is for informational purposes only, and is not, in any way, intended to 
communicate legal definitions as to when trades are guaranteed or novated by [[GSD]]. Members should refer to 
the [[FICC]] [[GSD]] Rulebook for such information. 
Audience 
This document was written for operations staff, systems and development personnel including managers, 
analysts, and programmers of [[GSD]] [[Member]] firms. It presumes readers are familiar with technical concepts 
and terms as well as having a [[BASIC]] understanding of [[GSD]]'s products and services. 
Communication 
For information on [[FICC]] Connectivity, please contact [[DTCC]] CAPS at FICCConnectivity@[[DTCC]].com or [[FICC]] 
Integration at ficcintegration@[[DTCC]].com
. 
Additional Information 
• For additional documentation, access the [[DTCC]] Learning Center. 
• For additional service details, please refer to the Clearing Services > Fixed Income – [[GSD]] section 
available at www.[[DTCC]].com. 
• For questions regarding this User Guide or [[GSD]] Products and Services, please contact your [[FICC]] 
Relationship Manager. 

---

## Page 8

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Access to [[FICC]] [[GSD]] RTTM Web 8 
ACCESS TO [[FICC]] [[GSD]] RTTM WEB 
This section explains how to log-on and log-off of [[FICC]]’s [[GSD]] RTTM Web application. 
Provisioning User Access 
Instructions for how to provision a user can be found in the [[FICC]] RTTM Super Access Coordinator Guide 
currently in the [[DTCC]] Learning Center. The purpose of the [[FICC]] RTTM Super Access Coordinator Guide is to 
assist super access coordinators (SACs) and access coordinators (ACs) on how to provision members of their 
firm with the necessary access to [[FICC]]’s [[GSD]] RTTM Web application through the Customer Registration 
System (CRS).  
Login into the [[GSD]] RTTM Web application 
Once a user is provisioned, the user should be able to access the [[GSD]] RTTM Web application. The functions 
that a user has access to will depend on the access provisioned for the user by their Super Access 
Coordinator.  
A user may select one of the two URLs shown below to access [[GSD]] RTTM Web: 
Environment Application ICC Web URL Description 
PRODUCTION [[DTCC]] Portal  https://login.[[DTCC]].net 
https://portal.online.[[DTCC]].net 
Generic URL to Applic ations 
PRODUCTION [[FICC]] [[GSD]] https://[[GSD]] -ficcweb.[[DTCC]].net Direct [[FICC]] [[GSD]] Web Application URL  
PRODUCTION [[FICC]] Report Center   https://fhrweb.[[DTCC]].net Direct [[FICC]] Report Center Application  URL  
PSE (Test)  [[DTCC]] Portal  https://loginu.[[DTCC]].net 
https://portalu.online.[[DTCC]].net   
Generic URL to Applications  
PSE (Test)  [[FICC]] [[GSD]] https://[[GSD]] -ficcweb-
pse.[[DTCC]].net  
Direct [[FICC]] [[GSD]] Web Application URL  
PSE (Test) [[FICC]] Report Center  https://fhrweb-pse.[[DTCC]].net Direct [[FICC]] Report Center Application URL  
Table 1: List of URLs to access RTTM Web 
 
For connectivity issues, contact the [[DTCC]] CAPS team via email at FICCConnectivity@[[DTCC]].com or the [[FICC]] 
Integration team via email at FICCIntegration@[[DTCC]].com.   

---

## Page 9

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Access to [[FICC]] [[GSD]] RTTM Web 9 
Using the Product Specific URL 
If  a user selects to access RTTM Web via the product specific URLs https://[[GSD]]-ficcweb.[[DTCC]].net to login to the 
specific [[GSD]] RTTM Web application, the below screen will appear.  
 
Figure 1: Single Sign-on Login Screen for Product Specific RTTM Web URLs 
Login into the RTTM Web Application 
A user will be able to login directly to the [[GSD]] RTTM web application using product specific URL. The user 
would enter their single sign-on credentials and select the Login button. Next, the user will be directed to the 
[[GSD]] Dashboard (Landing Page). If the user selects to access RTTM Web via the product specific URL, then 
skip to the section on the [[GSD]] Dashboard. 
  


---

## Page 10

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Access to [[FICC]] [[GSD]] RTTM Web 10 
Using the General URLs through MyDTCC 
If  a user selects to access RTTM Web via the General URLs https://login.[[DTCC]].net or 
https://portal.online.[[DTCC]].net to login to the [[GSD]] RTTM Web application, the below screen will appear. The user 
would enter their single sign-on credentials and select the Login button. The user will be directed to the 
MyDTCC page.  
 
Figure 2: Single Sign-on Login Screen for MyDTCC - General URL for various [[DTCC]] Applications 
  


---

## Page 11

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Access to [[FICC]] [[GSD]] RTTM Web 11 
A menu of [[DTCC]] products/applications provisioned to the user’s single sign-on credentials would be displayed 
upon login. 
 
Figure 3: MyDTCC Product Listing 
To access [[GSD]] RTTM Web, the user should select the [[FICC]] [[GSD]] RTTM Web tile as seen below. Up on 
selecting the [[FICC]] [[GSD]] RTTM Web tile, the user is directed to the [[GSD]] Dashboard (Landing Page). 
 
Figure 4: [[FICC]] [[GSD]] RTTM Web Tile 
Timing Out 
For enhanced security, the [[GSD]] RTTM Web is equipped with a timeout feature that logs the user off of the 
application if it is inactive for a given period of time. To regain access to the system, you must re-enter your 
logon credentials.   


---

## Page 12

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] RTTM Web Navigation Bar 12 
[[GSD]] RTTM WEB NAVIGATION BAR 
Navigation Toolbar 
The Navigation Toolbar is located at the top of every [[GSD]] RTTM Web page. It is used to access all underlying 
[[GSD]] RTTM Web screens and functions, which are referenced below:  
 
• Dashboard – The [[GSD]] Dashboard provides at a glance, statistical data on Members [[GSD]] trades and  
[[obligations]], for the current day and any past business date (up to five years in the past) 
• Trades –The Trades dropdown menu item is used to enter trades and to access various query functions 
regarding your trading activity. From this menu you can: 
o Enter DVP Trades, Cash and Repo/Reverse Trades  
o Enter GCF Repo/CCIT Trades 
o Search for and Manage DVP Trades  
o Search for and Manage GCF Repo/CCIT Trades 
o View Current Day’s Rejects  
o Search for and Manage Advisories 
• [[obligations]] – The [[obligations]] menu item allows the user to search for current [[obligations]] and historical 
[[settlement]] statuses on past [[obligations]]  
• Substitutions – The Substitutions dropdown menu item allows the user to enter and Search for 
Substitutions 
• Tools – The Tools dropdown menu item provides users with access to reference data such as the Security 
Masterfile and [[Member]] Contact information  
• Reports – The Reports menu item will direct the user to the [[FICC]] Report Center where access to all 
current and historical [[GSD]] Activity Reports are stored.  
 
Note:  
A User must be provisioned to have access to the Reports.  
 
 
Figure 5: [[GSD]] RTTM Web Navigation Toolbar 
  


---

## Page 13

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] RTTM Web Navigation Bar 13 
Contact Us 
This link will direct the user to the Client Center landing page on [[DTCC]].com where a list of contact information is 
provided for various business lines within [[DTCC]]. 
 
Figure 6: Contact Us link redirects to [[DTCC]].com/client-center 
Logout 
To ensure optimum security, always use the Logout button to disconnect from the RTTM Web application. 
Browsing to web pages external to [[GSD]] RTTM Web will not automatically terminate an open session.  
 
However, a session will automatically terminate upon expiration of the timing period as mentioned previously.  
 
Click the Logout button. A confirmation popup window will appear. Then, click either the: 
• Yes button to logout, or 
• No button to abort logging off the application. 
 
 
Figure 7: Logout Confirmation popup window 
  


---

## Page 14

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] RTTM Web Navigation Bar 14 
Alerts 
The Alerts function serves as a communications tool within RTTM Web so that [[GSD]] can communicate to its 
Members o n various deadlines, timeframes, or other system or service-related information in a timely manner.  
An alert may be displayed on the screen in one of two ways:  
1. At the top right of the screen, a red flag (Alert Icon) with a numerical value alongside it would be displayed. 
The numerical value displays for the user how many alerts have been communicated.  
 
Figure 8: Alert Icon (Red Flag) 
 
To view the list of alerts, use your mouse to click the Alert Icon. A popup window similar to the below will 
appear. This window would display the available alerts. Once viewed, you may click the Exit      icon or Close 
button to close the window. 
 
Figure 9: Alerts popup window 
 
2. An Alert such as the one seen below, would appear as a temporary popup window in [[GSD]] RTTM Web.  
 
Figure 10: Alert temporary popup window


---

## Page 15

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 15 
[[GSD]] DASHBOARD 
Once the user is logged in to [[GSD]] RTTM Web, the user is directed to the [[GSD]] Dashboard (Landing Page). 
The Dashboard defaults to the Current Day view for a user and contains real-time statistical data based on the 
selected [[Member]]’s current day trading and [[settlement]] activity.  
 
 
Figure 11: Main Toolbar - Dashboard 
 
The Dashboard is separated into three sections: 
• DVP Dashboard – Located at the top of the Dashboard Landing Page 
• GCF Dashboard – Located at the bottom of the Dashboard Landing Page 
• Useful information and links – Located to the right on the Dashboard Landing Page 
 
The remainder of this section will provide the user with descriptions of the statistical data displayed on the DVP 
Dashboard and GCF Dashboard, as well as descriptions of the useful information and links section of the 
Dashboard. 
  


---

## Page 16

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 16 
DVP Dashboard 
The DVP Dashboard displays real-time trade and obligation data, including a display of exceptions and easy to 
understand real-time statistics to [[GSD]] users in [[GSD]] RTTM Web.  
Note:  
Unlike the GCF Dashboard, the statistical data that is displayed on the DVP Dashboard is the same for a user that is 
viewing  data for an account that is a [[Broker]] or Dealer.  
Current Day Statistics 
The current day statistics on the DVP Dashboard are dynamically updated by the system at set time 
increments. The current day’s statistical data displayed on the DVP Dashboard is organized into two sections: 
Trade Statistics and [[obligations]] by Par. 
 
Figure 12: DVP Dashboard - Current Day Statistics 
 
1 
2 
 3 
4 
5 
6 
8 
7 

---

## Page 17

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 17 
The Current Day Statistics on the DVP Dashboard are displayed as follows: 
1. DVP Dropdown: The DVP Dashboard provides details for Delivery versus Payment trade and [[settlement]] 
activity in real-time. To show/hide the DVP Dashboard, click this arrow. 
2. [[Member]] [[ID]] and Name: Select the [[Member]] [[ID]] and Name to view the desired statistical data for the 
selected account. Access to a single or to multiple [[Member]] accounts is based on the provisioned access 
associated with a user’s User [[ID]] and password. 
3. Date (Range) Picker: The date to which the DVP statistical data pertains to. It defaults to the current 
business date. Click this field and select a business date other than the current business date to view the 
desired historical statistical data. 
4. Trade Alerts: This section displays the number of trade inputs submitted to [[GSD]] that may require the 
viewing [[Member]]’s attention. Click each alert to view the trade search results for the selected alert.  
 
The following table describes the statistical data displayed in the Alerts section of the DVP Dashboard. The 
items described in the table are organized in the order as they appear on the screen. 
 
Item Description 
Note:  
This table describes the fields displayed for the date populated in the Date (Range) Picker field.  
Advisories Represents the number of trades submitted on the current business day against the 
viewing [[Member]] as indicated by the [[Member]] [[ID]] field. These trades are awaiting a 
comparison/affirmation action.  
Rejects Represents t he number of trades submitted on the current business  day that have been 
rejected by the DVP system due to a failure to pass validation criteria. 
Cancel Requests  Represents the number of all compared trades for which the counterparty has 
subsequently submitted a cancel action. This field can include trades with prior submission 
dates.  
Table 2: DVP Dashboard – Current Day Statistics – Trade Alerts Field Descriptions 
5. Transaction Type Selector: Use this drop-down to limit the viewable statistical data by transaction 
type(s). The options are Repo/Revr and Buy/Sell. To return the viewable statistical data for all transaction 
types, click the     button that appears in the Transaction Type Selector field.  
6. Trade Statistics: The statistics in this table are based on all DVP trade data for the current business date. 
Click on the trade state links to view the search results that correspond to the trade state.  
  


---

## Page 18

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 18 
The following table describes the statistical data displayed in the Trade Statistics section of the DVP 
Dashboard. The items described in the table are organized in the order as they appear on the screen. 
Item Description 
Note:  
This table describes the fields displayed for the date  populate d in the Date (Range) Picker field.  
Compared  Represents the total number (Items, Par and Amount) of all trades compared (CMP) by the 
[[Member]] on the current business date.  
Pending Comparison  Represents the total number (Items, Par and Amount) of all trades that are in the 
uncompared (PCP) state awaiting contra -party action.  
Pending Cancel  Represents the total number (Items, Par and Amount) of all compared trades for which the  
[[Member]] has submitted a cancel action on , resulting in a cancel request (CNR) to the 
contra -party and is awaiting contra- party action.  
Canceled  Represents the total number (Items, Par and Amount) of  all trades that have been fully 
cancelled on the current business date.  
Buy/Sell Forward S ettling   Represents the total number (Items, Par and Amount) of  all active buy/sell transactions that 
have a forward settling date in the system.  
Repo Forward Starting 
and  Term 
Represents the total number (Items, Par and Amount) of  all active Repo Transactions that 
have started and have an End Leg [[settlement]] Date greater than the current business date.  
Sponsored GC Trades 
Matched and Novated  
Represents the total number (Items, Par and Amount) of  all Sponsored GC Trades that are 
matched and novated in the system.  
Sponsored GC Trades 
Matched and Not Novated 
Represents the total number (Items, Par and Amount) of  all Sponsored GC Trades that are 
matched  and have a start date of the current business date,  but have not been novated by 
the system.  
Sponsored GC Maturing 
Trades  
Represents the total number (Items, Par and Amount) of all  previously novated Sponsor ed 
GC Trades that are maturing on the current business date. Maturing trades that are “rolled” 
will also appear here. 
Sponsored GC Term 
Trades  
Represents the total number (Items, Par and Amount) of all  novated term Sponsored GC 
Trades that are active and have a future [[settlement]] date ( not maturing today ).  
Comparison Percentage  Represents the percentage of all DVP trades that have been submitted and compared on 
the current business date.  
Total Submitted  Represents the total number of all DVP trades (Repo/Revr & Buy/Sell) that have been 
submitted on the current business date.  
Table 3: DVP Dashboard – Current Day Statistics – Trade Statistics Field Descriptions  

---

## Page 19

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 19 
7. [[obligations]] by Par Dropdown: The [[obligations]] by Par section of the DVP Dashboard provides details 
on the [[settlement]] statuses of [[securities]] [[settlement]] [[obligations]] due to settle on the current business date, 
in real-time. [[securities]] [[settlement]] [[obligations]] are the receive orders and deliver orders a [[Member]] is 
obligated to settle, as applicable, vs. [[FICC]] [[GSD]] on the current business date. To show/hide the 
[[obligations]] by Par, click this arrow. 
8. [[obligations]] by Par Table/Graph: The [[obligations]] in this table/graph represents all [[securities]] [[settlement]] 
[[obligations]] due to settle on the current business date. The [[obligations]] by Par defaults to the Graph tab 
which displays in a linear graph the Pending and Settled Status of the [[obligations]] for the current business 
date as settlements progress throughout the day. The Pending and Settled lines on the graph are 
inversely proportional. Click on the Pending and Settled Lines to control which Clearance State is visible.  
 
 
Figure 13: DVP Dashboard – Current Day Statistics – [[obligations]] by Par (Graph) 
Click the Table tab to view the underlying statistical data on [[securities]] [[settlement]] [[obligations]] by Business 
Event and Clearance State.  
 
 
Figure 14: DVP Dashboard – Current Day Statistics – [[obligations]] by Par (Table) 
 
  


---

## Page 20

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 20 
The following table describes how to read the statistical data displayed in the [[obligations]] by Par Table. The  
items described in the table below are organized in the order as they appear on the screen. 
Item Description 
Note:  
This table describes the fields displayed for the date populated  in the Date (Range) Picker field.  
Pending – The Clearance State of the [[obligations]] that are due to settle on the current business date but ha ve yet 
to settle. 
SOD Represents the total number (Items, Par and Amount) of the start of day open orders that a 
[[Member]] is obligated to settle with [[FICC]] on the current business date. Thes e open orders  
orig inated from the Netting Process.  
SDS  Represents the total number (Items, Par and Amount) of  the open orders that were 
generated as a result of a compared Same- Day Settling Trade for which the [[Member]] is 
obligated to settle with [[FICC]] on the current business date. These open orders originated 
from the Same-Day Settling Process . 
SUBS Represents the total number (Items, Par and Amount) of  the open orders that were 
generated as a result of a substitution notification request for which the [[Member]] is 
obligated to settle with [[FICC]] on the current business date. These open orders originated 
from the Substitution Process . 
ADMIN Represents the total number (Items, Par and Amount) of  the open orders that were 
generated as a result of [[GSD]] Business Operations action. Thes e open orders originated 
through Admin Processing . 
Settled – The Clearance State of the obligation s that were due to and have settled on the current business date.  
SOD Represents the total number (Items, Par and Amount) of  the start of day open orders that a 
[[Member]] settled with [[FICC]] on the current business date. Thes e open orders originated from 
the Netting Process.  
SDS  Represents the total number (Items, Par and Amount) of  the open orders that were 
generated as a result of a compared Same- Day Settling Trade for which the [[Member]] 
settled with [[FICC]] on the current business date. These open orders originated from the 
Same-Day Settling Process.  
SUBS Represents the total number ( Items, Par and Amount) of  the open orders that were 
generated as a result of a substitution notification request for which the [[Member]] settled wi th  
[[FICC]] on the current business date. These open orders originated from the Substitution 
Process.  
ADMIN Represents the total number (Items, Par and Amount) of  the open orders that were 
generated as a result of  [[GSD]] Business Operations action. Thes e open orders originated 
through Admin Processing.  
Table 4: DVP Dashboard – Historical Statistics – [[obligations]] by Par (Table) Field Descriptions 
 
  

---

## Page 21

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 21 
Historical Statistics 
From the DVP section of the Dashboard, a user can choose to view DVP and/or Sponsored GC trade data 
from an earlier business date. To [[DO]] this, select the Date (Range) Picker field located at the top of the DVP 
section of the Dashboard. Then either select a day from the list of Shortcuts, i.e., Today, Yesterday or Last 
Month, or select an earlier business date from the Date (Range) Picker tool.  
 
The screen will update based on the date selection. Then, if applicable, select a trade status category to view 
trade search results filtered to match those selections. To display the current day’s activity again, click the     
button in the Date (Range) Picker. The historical statistical data displayed on the DVP Dashboard is organized 
into two sections: Trade Statistics and [[obligations]] by Par. 
 
  
Figure 15: DVP Dashboard – Historical Statistics 
  
1 
2 
 3 
4 
5 
7 
6 


---

## Page 22

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 22 
The Historical Statistics on the DVP Dashboard are displayed as follows: 
1. DVP Dropdown: The DVP Dashboard provides details for Delivery versus Payment trade and [[settlement]] 
activity for the selected business date. To show/hide the DVP Dashboard, click this arrow. 
2. [[Member]] [[ID]] and Name: Select the [[Member]] [[ID]] and Name to view the desired statistical data for the 
selected account. Access to a single or to multiple [[Member]] accounts is based on the provisioned access 
associated with a user’s User [[ID]] and password. 
3. Date (Range) Picker: The date to which the DVP statistical data pertains to. It defaults to the current 
business date. Click this field and select a business date other than the current business date to view the 
desired historical statistical data. 
4. Transaction Type Selector: Use this drop-down to filter the viewable statistical data by transaction 
type(s). The options are Repo/Revr and Buy/Sell. To return the viewable statistical data for all transaction 
types, click the     button that appears in the Transaction Type Selector field.  
5. Trade Statistics: The statistics in this table are based on all DVP trade data for the selected business 
date. Click on the trade state links to view the search results that correspond to the trade state.  
 
The following table describes the statistical data displayed in the Trade Statistics section of the DVP 
Dashboard. The items described in the table are organized in the order as they appear on the screen. 
 
Item Description 
Note:  
This table describes the fields displayed for the da te populated  in the Date (Range) Picker field.  
Compared  Represents the total number (Items, Par and Amount) of all trades compared (CMP) by the 
[[Member]] on the selected  business date.  
Pending Comparison  Represents the total number (Items, Par and Amount) of all trades that were in the 
uncompared (PCP) state awaiting contra -party action  on the selected business date.  
Buy/Sell Forward S ettling  Represents the total number (Items, Par and Amount) of all act ive buy/sell transactions that 
had a forward settling date in the system  on the selected  business date. 
Repo Forward Starting 
and Term 
Represents the total number (Items, Par and Amount) of all active Repo Transactions that 
started and ha d an End Leg [[settlement]] Date greater than the selected  business date.  
Sponsored GC Trades 
Matched and Novated  
Represents the total number (Items, Par and Amount) of  all Sponsored GC Trades that 
were matched and novated in the system  on the selected  business date. 
Sponsored GC Trades 
Matched and Not Novated 
Represents the total number (Items, Par and Amount) of  all Sponsored GC Trades that 
were matched and had a start date of the selected business date, but were not novated by 
the system  on the selected  business date. 
Sponsored GC Maturing 
Trades  
Represents the total number (Items, Par and Amount) of all  previously novated Sponsor ed 
GC Trades that were maturing on the selected business date. Maturing trades that are 
“rolled” will also appear here. 
Sponsored GC Term 
Trades  
Represents the total number (Items, Par and Amount) of all  novated term Sponsored GC 
Trades that were active and had a future [[settlement]] date ( not maturing that day ) as of the 
selected business date.  


---

## Page 23

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 23 
Item Description 
Comparison Percentage  Represents the percentage of all DVP trades submitted and compared on the selected  
business date.  
Total Submitted  Represents the total number of all DVP trades submitted on the selected  business date. 
All Trades Netted  Represents the total number of all DVP trades netted on the selected  business date.  
All Dollars Netted  Represents the total dollar value of all DVP trades netted on the selected  business date.  
Table 5: DVP Dashboard - Historical Statistics - Trade Statistics Field Descriptions 
 
6. [[obligations]] by Par Dropdown: The [[obligations]] by Par section of the DVP Dashboard provides historical 
data on the [[settlement]] statuses of [[securities]] [[settlement]] [[obligations]] that were due to settle on the 
selected business date. [[securities]] [[settlement]] [[obligations]] are the receive orders and deliver orders a 
[[Member]] is obligated to settle, as applicable, vs. [[FICC]] [[GSD]] on the selected business date. To show/hide 
the [[obligations]] by Par, click this arrow. 
7. [[obligations]] by Par Table: The [[obligations]] in this table represent all [[securities]] [[settlement]] Obligation data 
that were due to settle on the selected business date. Click on the Business Event links to view the search 
results that correspond to the selected event.  
 
 
Figure 16: DVP Dashboard – Historical Statistics - [[obligations]] by Par (Table) 
 
  


---

## Page 24

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 24 
The following table describes how to read the statistical data displayed in the [[obligations]] by Par Table. The  
items described in the table below are organized in the order as they appear on the screen. 
 
Item Description 
Note:  
This table describes the fields displayed for the date  populated  in the Date (Range) Picker field.  
Pending – The Clearance State of the [[obligations]] that were due to settle on the selected  business date but did 
not settle. 
SOD Represents the total number (Items, Par and Amount) of the start of day open orders that a 
[[Member]] was obligated to settle with [[FICC]] on the selected  business date. These  open 
orders  originated from the Netting Process.  
SDS  Represents the total number (Items, Par and Amount) of  the open orders that were 
generated as a result of a compared Same- Day Settling Trade for which the [[Member]] was 
obligated to settle with [[FICC]] on the selected  busines s date. These open orders originated 
from the Same-Day Settling Process . 
SUBS Represents the total number (Items, Par and Amount) of  the open orders that were 
generated as a result of a substitution notification request for which the [[Member]] was 
obligated to settle with [[FICC]] on the selected  business date. These open orders originated 
from the Substitution Process . 
ADMIN Represents the total number (Items, Par and Amount) of  the open orders that were 
generated as a result of [[GSD]] Business Operations action. There open orders originated 
through Admin Processing.  
Settled – The Clearance State of the [[obligations]] that settled on the selected business date.  
SOD Represents the total number (Items, Par and Amount) of  the start of day open orders that a 
[[Member]] was obligated to settle with [[FICC]] on the selected  business date. Thes e open 
orders originated from the Netting Process.  
SDS  Represents the total number (Items, Par and Amount) of  the open orders that were 
generated as a result of a compared Same- Day Settling Trade for which the [[Member]] was 
obligated to settle with [[FICC]] on the selected  business date. These open orders originated 
from the Same-Day Settling Process.  
SUBS Represents the total number (Items, Par and Amount) of  the open orders that were 
generated as a result of a substitution notification request for which the [[Member]] was 
obligated to settle with [[FICC]] on the selected  business date. These open orders originated 
from the Substitution Process.  
ADMIN Represents the total number (Items, Par and Amount) of  the open orders that were 
generated as a result of  [[GSD]] Business Operations action. Thes e open orders originated 
through Admin Processing.  
Table 6: DVP Dashboard – Historical Statistics – [[obligations]] by Par (Table) Field Descriptions 
  

---

## Page 25

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 25 
GCF Dashboard 
The GCF Dashboard displays real-time GCF Repo® and Centrally Cleared Institutional Tri-party (CCIT™) trade 
data, as applicable, including a display of exceptions and easy to understand real-time statistics to [[GSD]] users 
in [[GSD]] RTTM Web.  
GCF Dashboard – [[Broker]] View  
Current Day Statistics 
For a [[Broker]], the current day statistics displayed on the GCF Dashboard are dynamically updated by the 
system at set time increments. The current day’s statistical data displayed on the GCF Dashboard is organized 
into two sections: Trade Statistics and Net Delta. 
 
Figure 17: GCF Dashboard - [[Broker]] View - Current Day Statistics 
1 
2 
 3 
4 
5 
6 
7 

---

## Page 26

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 26 
For a [[Broker]], the Current Day Statistics on the GCF Dashboard are displayed as follows: 
1. GCF Dropdown: The GCF Dashboard provides details for GCF Repo trading activity in real-time. To 
show/hide the GCF Dashboard, click this arrow. 
2. [[Member]] [[ID]] and Name: Select the [[Member]] [[ID]] and Name to view the desired statistical data for the 
selected account. Access to a single or to multiple [[Member]] accounts is based on the provisioned access 
associated with a user’s User [[ID]] and password. 
3. Date (Range) Picker: The date to which the GCF Repo statistical data pertains to. It defaults to the 
current business date. Click this field and select a business date other than the current business date to 
view the desired historical statistical data. 
4. Trade Alerts: This section displays the number of trade inputs submitted to [[GSD]] that may require the 
viewing [[Member]]’s attention. Click each alert to view the trade search results for the selected alert.  
 
The following table describes the statistical data displayed in the Alerts section of the GCF Dashboard. The 
items described in the table are organized in the order as they appear on the screen. 
 
Item Description 
Note:  
This table describes the fields displayed for the date populated in the Date (Range) Picker field.  
Unbalanced  Represents the number of unbalanced (one- sided Repo or Reverse) trades submitted on 
the current business day by the [[Member]]  ( Repo Brok er) indicated.  
Cancel Requests  Represents the number of affirmed trades submitted on the current business day by the  
[[Member]] (Repo [[Broker]]) indicated, for which the counterparty has subsequently submitted a 
cancel action. This field  can include trades with prior submission dates for whic h a cancel 
request was submitted on the current business day . 
[[Broker]] in Position Represents the number of trades in pending affirm (PAF) status  submitted for the current 
business day by the [[Member]] (Repo [[Broker]]) indicated, where the dealer counterparty has  
canceled the trade. This results in t he Repo [[Broker]] being in position because the remaining 
unbalanced trade has not been canceled.  
Rejects Represents the number of trades submitted on the current business day that have been 
rejected by the GCF system due to a failure to pass validation criteria.  
Table 7: GCF Dashboard – [[Broker]] View – Current Day Statistics – Trade Alerts Field Descriptions 
5. [[CUSIP]] Selector: Use this drop-down to limit the viewable statistical data by GCF Repo Generic [[CUSIP]] 
Number. To return the viewable statistical data for all CUSIPs, click the     button that appears in the 
[[CUSIP]] Selector field.  
6. Trade Statistics: The statistics in this table are based on all GCF Repo trade data, as applicable, for the 
current business date. Click on the trade state links to view the search results that correspond to the trade 
state.  
  


---

## Page 27

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 27 
The following table describes the statistical data displayed in the Trade Statistics section of the GCF 
Dashboard. The items described in the table are organized in the order as they appear on the screen. 
 
Item Description 
Note:  
This table describes the fields displayed for the date populated in the Date (Range) Picker field.  
Affirmed Represents the total number (Items, Par and Amount) of all trades in the following trade 
states: Affirmed (AFF), Cancel Request (CNR) and Pending Cancel (PCN).  
Pending Affirm  Represents the total number (Items, Par and Amount) of all trades submitted by the 
[[Member]] (Repo [[Broker]]) indicated on the current business day, for which the affirm action 
has not yet been taken by contra -party (Dealers).  
Note:  
Excludes trades in a pending affirm trade state for which the Repo [[Broker]] has taken a side 
as such trades are reported in the [[Broker]] in Position field.  
Note:  
This field is only applicable to GCF Repo Transactions. GCF Repo Transactions submitted 
by GCF-Authorized Inter -Dealer Brokers (Repo Brokers) are submitted on a Locked -in basis 
and are deemed compared upon receipt per [[GSD]] Rules.  
Pending Cancel  Represents the total number (Items, Par and Amount) of all compared trades for which the  
[[Member]] (Repo [[Broker]]) indicated has submitted a cancel action on, resulting in a cancel 
request (CNR) to the contra -party and is awaiting contra- party action. This item can 
represent trades with prior submission dates that are still in p ending cancel state. 
Canceled  Represents the total number (Items, Par and Amount) of all trades that have been fully 
cancelled on the current business date.  
Note:  
Canceled unbalanced trades will not be included in the Canceled field.  
Forward & Term Represents the total number (Items , Par and Amount) of  all active forward and term trades 
for the [[Member]] (Repo [[Broker]]) indicated. ‘Active’ represents trades that:  
• have not reached the start date (Forward)  
• starts on current business day  or a previous business day  with an end date greater 
than current business day (Term)  
• are not in a status of canceled.  
Affirmed Represents the percentage of all GCF Repo Transactions  that are in the following trade 
states: Affirmed (AFF), Cancel Request (CNR) and Pending Cancel (PCN).  
Total Submitted Represents the total number of all GCF Repo T ransactions  that have been submitted on 
the current business date.  
Table 8: GCF Dashboard – [[Broker]] View – Current Day Statistics – Trade Statistics Field Descriptions 

---

## Page 28

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 28 
7. Net Delta: The GCF Net Delta table displays the total par v alue of the previous business day’s net 
obligation, what the net obligation is expected to be on the current business day, and the delta between 
the two amounts. The data is ordered by GCF Repo Generic [[CUSIP]] Number and each [[CUSIP]] is a link to 
the underlying trade data. The table acts as a position monitor that allows the user to see what their 
current position is at a glance and to understand the change in net position day over day at the GCF Repo 
Generic [[CUSIP]] level. 
 
Click on each GCF Repo Generic [[CUSIP]] link to view the search results of trade data that correspond to the 
selected item. 
 
 
Figure 18: GCF Dashboard - [[Broker]] View - Current Day Statistics - Net Delta 
The following table describes how to read the statistical data displayed in the Net Delta Table. The items 
described in the table below are organized in the order as they appear on the screen. 
 
Item Description 
Note:  
This table describes the fields displayed for the date populated in the Date (Range) Picker field.  
[[CUSIP]] Represents GCF Repo Generic [[CUSIP]] Numbers:  371487AD1, 371487AE9, 371487AH2, 
371487AL3, 371487AQ2, 371487AM1, 371487AR0, 371487AG4 and 371487AF6. 
Click on each GCF Repo Generic [[CUSIP]] link to view the search results of trade data that 
correspond to the selected item.  
Previous Business Day  Represents the final net position for the GCF Repo Generic [[CUSIP]] Number as of end of 
day on the previous business day.  
Current Business Day  Represents the current net position of compared trades for the GCF Repo Generic [[CUSIP]] 
Number for the current business day.  
Net Cash  Represents the net delta amount of the previous business day’s net position vs. the current 
business day’s net position for the GCF Repo Generic [[CUSIP]] Number.  
Table 9: GCF Dashboard – [[Broker]] View – Current Day Statistics – Net Delta Field Descriptions  


---

## Page 29

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 29 
Historical Statistics 
 
From the GCF section of the Dashboard, a user can choose to view GCF Repo, as applicable, from an earlier 
business date. To [[DO]] this, select the Date (Range) Picker field located at the top of the GCF section of the 
Dashboard. Then either select a day from the list of Shortcuts, .i.e., Today, Yesterday or Last Month, or select 
an earlier business date from the Date (Range) Picker tool.  
The screen will update based on the date selection and then if applicable, select a trade status category to 
view trade search results that match those selections. To display the current day’s activity again, click the     
button in the Date (Range) Picker.  
The historical statistical data displayed on the GCF Dashboard is organized into two sections: Trade Statistics 
and Net Delta. 
 
Figure 19: GCF Dashboard - [[Broker]] View - Historical Statistics 
  
1 
2 
3 
4 
5 

---

## Page 30

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 30 
For a [[Broker]], the Historical Statistics on the GCF Dashboard are displayed as follows: 
1. GCF Dropdown: The GCF Dashboard provides details for GCF Repo and CCIT trading activity for the 
selected business date. To show/hide the GCF Dashboard, click this arrow. 
2. [[Member]] [[ID]] and Name: Select the [[Member]] [[ID]] and Name to view the desired statistical data for the 
selected account. Access to a single or to multiple [[Member]] accounts is based on the provisioned 
access associated with a user’s User [[ID]] and password.  
3. Date (Range) Picker: The date to which the GCF Repo/CCIT statistical data pertains to. It defaults to 
the current business date. Click this field and select a business date other than the current business 
date to view the desired historical statistical data. 
4. Trade Statistics: The statistics in this table are based on all GCF Repo/CCIT trade data, as 
applicable, for the selected business date. Click on the trade state links to view the search results that 
correspond to the trade state.  
 
The following table describes the statistical data displayed in the Trade Statistics section of the GCF 
Dashboard. The items described in the table are organized in the order as they appear on the screen. 
Item Description 
Note:  
This table describes the fields displayed for the date populated in the Date (Range) Picker field.  
Compared  Represents the total number (Items, Par an d Amount) of all trades that  were compared on 
behalf of the [[Member]] for the selected business date. 
[[obligations]]  Represents the total number (Items, Par and Amount) of [[obligations]] between [[FICC]] and the 
[[Member]] indicated. This field will display new [[obligations]] as well as outstanding [[obligations]] 
from the previous day . 
In-Net Represents the total number (Items, Par and Amount ) of all trades that went into the net on 
the selected business date for the [[Member]] indicated.  
Note:  
This is a subset of the trades captured in the Forward & Term field.  
Forward & Term Represents the to tal number (Items, Par and Amount) of  all forward and term trades for the 
[[Member]] indicated.  
Table 10: GCF Dashboard – [[Broker]] View – Historical Statistics – Trade Statistics Field Descriptions 
 
5. Net Delta: The historical data in the GCF Net Delta table displays the total par value of the previous 
business day’s net obligation, what is expected to be the net obligation on the current business day. The 
delta between the two amounts is based on the data as of the selected business date displayed in the 
Date (Range) Picker field. The data is ordered by GCF Repo Generic [[CUSIP]] Number and each [[CUSIP]] is 
a link to the underlying trade data. 
  

---

## Page 31

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 31 
GCF Dashboard – Dealer/CCIT View 
Current Day Statistics 
For a Dealer or CCIT [[Member]], the current day statistics displayed on the GCF Dashboard are dynamically 
updated by the system at set time increments. The current day’s statistical data displayed on the GCF 
Dashboard is organized into two sections: Trade Statistics and Net Delta. 
 
Figure 20: GCF Dashboard - Dealer/CCIT View - Current Day Statistics 
  
1 
2 
 3 
4 
5 
6 
7 

---

## Page 32

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 32 
For a Dealer or CCIT [[Member]], the Current Day Statistics on the GCF Dashboard are displayed as follows: 
1. GCF Dropdown: The GCF Dashboard provides details for GCF Repo and CCIT trading activity in real-
time. To show/hide the GCF Dashboard, click this arrow. 
2. [[Member]] [[ID]] and Name: Select the [[Member]] [[ID]] and Name to view the desired statistical data for the 
selected account. Access to a single or to multiple [[Member]] accounts is based on the provisioned access 
associated with a user’s User [[ID]] and password. 
3. Date (Range) Picker: The date to which the GCF Repo/CCIT statistical data pertains to. It defaults to the 
current business date. Click this field and select a business date other than the current business date to 
view the desired historical statistical data. 
4. Trade Alerts: This section displays the number of trade inputs submitted to [[GSD]] that may require the 
viewing [[Member]]’s attention. Click each alert to view the trade search results for the selected alert.  
 
The following table describes the statistical data displayed in the Alerts section of the GCF Dashboard. The 
items described in the table are organized in the order as they appear on the screen. 
Item Description 
Note:  
This table describes the fields displayed for the date populated in the Date (Range) Picker field.  
Advisories Represents the number of bilateral trades submitted on the current business day against 
the viewing [[Member]] as indicated by the [[Member]] [[ID]] field. These trades are awaiting an 
affirmation action. 
Cancel Requests  Represents the number of affirmed trades submitted on the current business day for the 
[[Member]] indicated, for which the counterparty has subsequently submitted a cancel action. 
This field  can include trades with prior submission dates that were canceled on the current 
business day  and as well as trades from a prior business date that are still in a cancel 
request state. 
Rejects Represents the number  of trades submitted on the current business day that have been 
rejected by the GCF system due to a failure to pass validation criteria. 
Table 11: GCF Dashboard – Dealer/CCIT View – Current Day Statistics – Trade Alerts Field Descriptions 
 
5. [[CUSIP]] Selector: Use this drop-down to limit the viewable statistical data by GCF Repo Generic [[CUSIP]] 
Number. To return the viewable statistical data for all CUSIPs, click the     button that appears in the 
[[CUSIP]] Selector field.  
6. Trade Statistics: The statistics in this table are based on all GCF Repo/CCIT trade data, as applicable, 
for the current business date. Click on the trade state links to view the search results that correspond to 
the trade state.  
  


---

## Page 33

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 33 
The following table describes the statistical data displayed in the Trade Statistics section of the GCF 
Dashboard. The items described in the table are organized in the order as they appear on the screen. 
Item Description 
Note:  
This table describes the fields displayed for the date  populated  in the Date (Range) Picker field.  
Compared  & Affirmed Represents the total number (Items, Par and Amount) of all trades in the following trade 
states: CCIT Compared (CMP), Affirmed (AFF), Pending Affirm (PAF), Cancel Request 
(CNR) and Pending Cancel (PCN).  
Pending Comparison  Represents the total number (Items, Par and Amount) of all trades that have been 
submitted on the current business day and are in the uncompared (PCP) state awaiting 
contra -party action.  
Note:  
GCF Repo Transactions  submitted by GCF-Authorized Inter -Dealer Brokers (Repo Brokers) 
are submitted on a Locked -in basis and are deemed compared upon receipt by the 
Corporation.  
Pending Affirm  Represents the total number (Items, Par and Amount) of all trades that have been 
submitted on the current business day by GCF -Authorized Inter -Dealer Brokers (Repo 
[[Broker]] s) on behalf of the [[Member]] indicated for which such [[Member]] has not yet taken 
action to  affirm or cancel such trades.  
Note:  
This field is only applicable to G CF Repo Transactions .  
Note:  
GCF Repo Transactions submitted by GCF -Authorized Inter -Dealer Brokers (Repo Brokers) 
are submitted on a Locked -in basis and are deemed compared upon rec eipt per [[GSD]] Rules.  
In-Net Represents the total number (Items, Par and Amount ) of all trades submitted for the 
[[Member]] indicated that are eligible for the current business day’s net. Where applicable, 
item represents:  
• Trades submitted  and set to start to day 
• Previously submitted forward trades that start today  
• Term trades that have an end date greater than today  
Note:  
This is a subset of the trades captured in the Forward & Term field.  
Pending Cancel  Represents the total number (Items, Par and Amount) of all compared trades for which the  
[[Member]] has submitted a cancel action on, resulting in a cancel request to the contra -party 
and is awaiting contra -party action.  
Canceled  Represents the total number  (Items, Par and Amount) of all trades that have been fully 
cancelled on the current business date. Also represents:  

---

## Page 34

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 34 
Item Description 
• Cancels submitted vs. dealer and [[Broker]] in the AFF state and subsequently canceled  
Note:  
Cancels should only be returned for trades where the dealer has initiated the cancel. This 
includes admin cancels the dealer requested (via e- mail) where an Admin performs a cancel 
action on his behalf.  
Forward & Term Represents the total number (Items, Par and Amount) of  all active forward and term trades 
for the [[Member]] indicated. ‘Active’ represents trades that:  
• have not reached the start date (Forward)  
• start on the current business day with an end date greater than the current business 
day (Term) 
• started on a previous  business day with an end date greater than the current business 
day (Term) 
• are not in a status of canceled.  
Affirmed Represents the percentage of all GCF Repo Transactions  that have been affirmed on the 
current business date.  
Total Submitted Represents the total number of all GCF Repo T ransactions  that have been submitted on 
the current business date.  
CCIT Compared  Represents the percentage of all CCIT Transactions that have been compared on the  
current business date.  
Total Submitted Represents the total number of all CCIT Transactions  that have been submitted on the 
current business date.  
Table 12: GCF Dashboard – Dealer/CCIT View – Current Day Statistics – Trade Statistics Field Descriptions 
Note: 
Dealer item counts and amounts are on a trade- by-trade basis. (1 instruct = 1 trade) and are based on the last state of the 
trades.   
 
7. Net Delta: The GCF Net Delta table displays the total par v alue of the previous business day’s net 
obligation, what is expected to be the net obligation on the current business day, and the delta between 
the two amounts. The data is ordered by GCF Repo Generic [[CUSIP]] Number and each [[CUSIP]] is a link to 
the underlying trade data. 
 
The table acts as a position monitor that allows the user to see what their current position is at a glance 
and to understand the change in net position day over day at the GCF Repo Generic [[CUSIP]] level. 
 
  

---

## Page 35

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 35 
Click on each GCF Repo Generic [[CUSIP]] link to view the search results of trade data that correspond to the 
selected item. 
 
Figure 21: GCF Dashboard - Dealer/CCIT View - Current Day Statistics - Net Delta 
 
The following table describes how to read the statistical data displayed in the Net Delta Table. The items 
described in the table below are organized in the order as they appear on the screen. 
Item Description 
Note:  
This table describes the fields displayed for the date  populated  in the Date (Range) Picker field.  
[[CUSIP]] Represents GCF Repo Generic [[CUSIP]] Numbers:  371487AD1, 371487AE9, 371487AH2, 
371487AL3, 371487AQ2, 371487AM1, 371487AR0, 371487AG4 and 371487AF6. 
Click on each GCF Repo Generic [[CUSIP]] link to view the search results of trade data that 
correspond to the selected item.  
Previous Business Day  Represents the final net position for the GCF Repo Generic [[CUSIP]] Number as of end of 
day on the previous business day.  
Current Business Day  Represents the current net position of compared trades for the GCF Repo Generic [[CUSIP]] 
Number for the current business day. 
Net Cash  Represents the net delta amount of the previous business day’s net position vs. the current 
business day’s net position for the GCF Repo Generic [[CUSIP]] Number.  
Table 13: GCF Dashboard – Dealer/CCIT View – Current Day Statistics – Net Delta Field Descriptions 
 
 
  


---

## Page 36

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 36 
Historical Statistics 
From the GCF section of the Dashboard, a user can choose to view GCF Repo and CCIT trade data, as 
applicable, from an earlier business date. To [[DO]] this, select the Date (Range) Picker field located at the top of 
the GCF section of the Dashboard. Then either select a day from the list of Shortcuts, .i.e., Today, Yesterday 
or Last Month, or select an earlier business date from the Date (Range) Picker tool.  
The screen will update based on the date selection and then, if applicable, select a trade status category to 
view trade search results that match those selections. To display the current day’s activity again, click the     
button in the Date (Range) Picker.  
The historical statistical data displayed on the GCF Dashboard is organized into two sections: Trade Statistics 
and Net Delta. 
 
Figure 22: GCF Dashboard - Dealer/CCIT View - Historical Statistics 
 
  
1 
2 
3 
4 
5 

---

## Page 37

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 37 
For a Dealer or CCIT [[Member]], the Historical Statistics on the GCF Dashboard are displayed as follows: 
1. GCF Dropdown: The GCF Dashboard provides details for GCF Repo and CCIT trading activity for the 
selected business date. To show/hide the GCF Dashboard, click this arrow. 
2. [[Member]] [[ID]] and Name: Select the [[Member]] [[ID]] and Name to view the desired statistical data for the 
selected account. Access to a single or to multiple [[Member]] accounts is based on the provisioned access 
associated with a user’s User [[ID]] and password. 
3. Date (Range) Picker: The date to which the GCF Repo/CCIT statistical data pertains to. It defaults to the 
current business date. Click this field and select a business date other than the current business date to 
view the desired historical statistical data. 
4. Trade Statistics: The statistics in this table are based on all GCF Repo/CCIT trade data, as applicable, 
for the selected business date. Click on the trade state links to view the search results that correspond to 
the trade state.  
 
The following table describes the statistical data displayed in the Trade Statistics section of the GCF 
Dashboard. The items described in the table are organized in the order as they appear on the screen. 
Item Description 
Note:  
This table describes the fields displayed for the date  populated  in the Date (Range) Picker field.  
Compared  Represents the total number (Items, Par and Amount) of all trades that were compared on 
behalf of the [[Member]] for the selected  business date. 
[[obligations]]  Represents the total number (Items, Par and Amount) of [[obligations]] between [[FICC]] and the 
[[Member]] selected . This field will display new [[obligations]] as well as outstanding [[obligations]] 
from the previous day . 
In-Net Represents the total number (Items, Par and Amount ) of all trades that went into the net on 
the selected  business date for the [[Member]] indicated.  
Note:  
This is a subset of the trades captured in the Forward & Term field.  
Forward & Term Represents the to tal number (Items, Par and Amount) of  all forward and term trades for the 
[[Member]] indicated.  
Table 14: GCF Dashboard – Dealer/CCIT View – Historical Statistics – Trade Statistics Field Descriptions 
 
5. Net Delta: The historical data in the GCF Net Delta table displays the total par value of the previous 
business day’s net obligation, what is expected to be the net obligation on the current business day, and 
the delta between the two amounts and is based on the data as of the selected business date displayed in 
the Date (Range) Picker field. The data is ordered by GCF Repo Generic [[CUSIP]] Number. 
  

---

## Page 38

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 38 
Useful Information and Links  
On the right-hand side of the [[GSD]] Dashboard, the user will find useful information related to [[GSD]] products and 
services as well as links to commonly used web pages.  
Note:  
Links within [[GSD]] RTTM Web are displayed in blue  font . When a user hovers over a lin k, it will be displayed in blue 
font/underlined.  
 
 
  
  
 
 
 
 
 
 
1 Current Investment Rate:  The interest rate used to calculate 
interest earned on [[FICC]]’s overnight investments of cash.  
  
2 Latest GCF MBS Index:  The latest GCF Repo Index Rate for 
[[CUSIP]] 371487AL3 – Fannie Mae & Freddie Mac Fixed Rate MBS 
(FFFIX). 
  
3 Latest GCF Treasury Index:  The latest GCF Repo Index Rate for 
[[CUSIP]] 371487AE9 – U.S. Treasury < 30- year maturity (TU30)  
  
4 Current When Issued [[securities]]:  When -issued (WI) U.S. 
Treasury [[securities]] that are reissues or newly issued [[securities]] will 
appear in this space, as applicable.  
  
5 Upcoming [[FICC]] Holidays :  Holidays that are observed by [[FICC]] 
where no trade input will be accepted and no [[settlement]] will  occur . 
5 
4 
3 
2 
1 
Figure 23: Dashboard - Useful Information 

---

## Page 39

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[GSD]] Dashboard 39 
  
 
 
 
6 Links: This list contains links to internal and external resources 
that a user may find helpful.  
  
 [[GSD]] Rulebook : Click to view the [[GSD]] Rules on [[DTCC]].com . 
  
 [[GSD]] System Schedules: Click to view a list containing a 
complete list of both DVP and GCF Repo/CCIT Timeframes.  
Note:  
Once link is selected, scroll up to view the DVP Timeframes  
 [[GSD]] Sponsored Membership Statistics: Click to view the 
Sponsored Membership page on  [[DTCC]].com .   
  
 Daily Fails – Treasury and Agency: Click to view data for U.S. 
Treasury and Agency fails on [[DTCC]].com . 
  
 [[DTCC]] Learning: Click to access the landing page for the 
[[DTCC]] Learning Center.  
  
 Treasury Direct Announcements (External) : Click to access 
the “Announcements, Data & Results” page on the 
treasurydirect.gov .   
  
 Secured Overnight Financing Rate – SOFR (External): Click 
to access the SOFR Data page on the website of the Federal 
Reserve Bank of New York.  
  
 Office of Financial Research – OFR (External): Click to 
access the OFR’s Repo Markets Data Release page.  
  
 Consumer Price Index (CPI) News Release Calendar 
(External): Click to view the Schedule of Releases for the CPI 
on the website of the U.S. Bureau of Labor Statistics.  
6 
Figure 24: Dashboard - Useful Links 

---

## Page 40

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 40 
TRADES 
The Trades dropdown menu allows a user to navigate to certain trade management screens within [[GSD]] RTTM 
Web, such as Trade Entry, Trade Search & Management, Trade Advisory Management, Trade Rejects, and 
CCIT Trade Fund Allocation. These functions will allow the user to enter cash and repo trades manually into 
the system, search for active and historical trades within a certain criteria, search for, monitor and enter 
substitutions, view rejects in real time and search for and action on advisories (trades) submitted against the 
user’s [[Member]] firm. 
 
Figure 25: Trades dropdown menu 
Trades > Entry 
From the Trades > Entry menu selection, users with the appropriate access can enter trades on behalf of their 
[[Member]] firm(s).  
 
Figure 26: Trades > Entry 
Note:  
A user must be provisioned to have update access to enter trades via [[GSD]] RTTM Web.   


---

## Page 41

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 41 
DVP Trade Entry 
This section will explain to the user how to use the DVP Trade Entry screens to enter Repo and Reverse Repo 
Transactions as well as Buy / Sell Transactions. 
Enter a Buy / Sell Transaction 
To enter a Buy and/or Sell Transaction, the user must enter the required information (*) in the Trade Details 
section ([[CUSIP]], Trade Date, [[settlement]] Date, Pricing Method, [[Broker]] Xref (for [[Broker]] submissions only) 
Transaction Type) and in the Allocation section (Par, Price, Contra [[ID]], and Trade Reference (Xref) Number).  
Note:  
Once the Transaction Type is selected, the screen will update to display the Allocation section as seen below.  
Note:  
The [[Member]] [[ID]] and Product type are preselected by [[default]].  
 
Figure 27: DVP Buy / Sell Trade Entry Screen (fields unpopulated) 
 
  


---

## Page 42

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 42 
To submit a Buy and/or Sell Transaction, the user must populate the fields in the Trade Details section and the 
Allocation section as seen below.  
 
Figure 28: DVP Buy / Sell Trade Entry Screen (fields populated) - Pre-Validation 
 
If the user has additional trades to enter with different allocation details, then the user would select the + Add 
Row button and enter the additional trade details, as applicable. 
Note:  
Up to 5 rows can be entered for each Transaction type (trade side), per submission, i.e., 5 Repo Transactions and 5 
Reverse Transactions can be submitted at one time.  
Note: 
If the user has to enter both trade sides (Repo and Reverse) and the Reverse allocation(s) are similar to the Repo 
allocation( s), then the user can use the Copy Side      icon (located to the right of the Transaction Type field) to copy all  the 
data for the Repo allocation(s) into the Reverse allocation(s) section (except the Xref(s)  which must be unique and 
therefore entered  separately .  
Note:  
The max par value that is allowed to be submitted per row is $50 million.  If the total par value of the transaction is greater 
than $50 million, then the user can use th e Copy Row      icon t o copy all the data from the current  row into a new row 
(except the Xref(s), which must be unique and therefore entered  separately).   


---

## Page 43

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 43 
Note:  
To delete a row added in error select the Delete Row     icon.  
Once all of relevant details are entered, the user should select the Validate button. Once the Validate button is 
selected, the system will check the trade entry against its validation rules. Validating entries before submission 
will alert the user to any system trade validation issues. The system will display a message that either 1) the 
trades were successfully validated or 2) One or more of the trades failed validation. 
See below for an example of trades successfully validated by the system. 
 
Figure 29: DVP Buy / Sell Trade Entry Successfully Validated 
  


---

## Page 44

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 44 
See below for an example of trades that failed validation. 
 
Figure 30: DVP Buy / Sell Trade Entry Failed Validation 
 
If one or more trades failed validation, the user can modify the trade details in order for the trade(s) to pass the 
system’s trade validation process. To see why a particular trade failed validation, the user should click the 
Warning       icon located to the right of the trade. A popup window will appear.  
  


---

## Page 45

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 45 
The popup window would display one or more possible trade errors that the user may need to resolve before 
submitting the trade. 
 
Figure 31: DVP Trade Entry Validation: Trade Errors Popup Window – Final Money Differs From Calculated 
Amount 
 
In the above example, the user can select to use the money entered as final money or use the system’s 
calculated money. For simplification, the System Money has been selected using the Select button. Once the 
[[Option]] is selected, the popup window will close, and the final money field will update to reflect the selected 
value.  
If the user is alerted to a trade error that is not modifiable from the popup window, the user should view the 
trade error and then close the window by using the Close button. Then the user should make the necessary 
modifications in the Trade Entry screen. See below for an example of a trade error that must be modified in the 
Trade Entry screen. 
 
Figure 32: DVP Trade Entry Validation: Trade Errors Popup Window – Contra [[participant]] Not Cash [[Member]]  
 


---

## Page 46

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 46 
The above trade error occurs when a trade is entered against a [[Member]] that does not participate in the 
Service for which the trade settles under, i.e. CCIT [[Member]] cannot participate in DVP Services. The user 
would need to close this popup window and edit the Contra [[ID]] field.  
If the Warning      icon appears for more than one trade, click the Warning      icon for each trade to display the 
possible Trade Errors and address any and all relevant errors that would cause the system not to validate the 
trade submission. Once all of errors have been addressed, the user may select the Validate button again. If no 
further warnings appear, the user should select the Submit button to submit the trade(s) to [[GSD]] RTTM Web for 
processing. 
If the user selects the Submit button in lieu of the Validate button, the system will check the trade entry against 
its validation rules. The system will display a message that either 1) the trades have been accepted or 2) the 
trades have been rejected. 
 
Figure 33: DVP Buy / Sell Trade Entry Submission (in leu of Validation) 
 
  


---

## Page 47

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 47 
See below for an example of trades accepted by the system successfully. 
 
Figure 34: DVP Buy / Sell Trade Entry Accepted (comparable to MT509 Trade Input Accepted (PACK) 
Message) 
 
Upon validation and submission, each trade is assigned a unique identifier, the Trade [[ID]] (TID). 
 
  


---

## Page 48

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 48 
See below for an example of trades rejected by the system. 
 
Figure 35: DVP Buy / Sell Trade Entry Rejected (comparable to MT509 Trade Input Rejected (REJT) Message) 
 
Once the system completes its trade validation process after initial submission, each rejected trade is assigned 
a unique identifier, a Reject [[ID]]. Hover over the Reject [[ID]] and it will display as “Rejected” . Click the Reject [[ID]] 
for each rejected trade to display the possible Trade Errors so that they may be corrected. A popup window will 
appear. The popup window would display one or more possible trade errors that the user must resolve before 
submitting the trade. Once all of errors have been addressed, the user may select the Submit button again. 
 
Figure 36: DVP Trade Entry Validation: Trade Errors Popup Window – Par Greater Than Max Trade Size 


---

## Page 49

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 49 
For instructions and field descriptions regarding the DVP Buy / Sell Trade Entry screen, please refer to the 
below table.  
Note:  
The fields  described in the  table below are organized in the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom  within each section).  
Field/Item Name  Instructions/Descriptions 
Trade Details 
[[Member]] [[ID]] The system will automatically [[default]] to the 4- digit [[GSD]] [[Member]] [[ID]] and Name associated 
with the user’s logon credentials.  
Note:  
The [[Member]] [[ID]] field defaults to the [[GSD]] [[Member]] [[ID]] and Name associated with the user’s 
logon credentials with the exception of u sers that have multiple [[Member]] IDs associated with 
their logon credentials.  
Product  This is a mandatory field. Specify the Product of the trade that is being entered.  
Note:  
For Buy / Sell Trade Entry, the system will [[default]] to the DVP Product type.  
[[CUSIP]] This is a mandatory field. Enter the [[CUSIP]] number of the security for the trade. This field 
must contain the whole [[CUSIP]] (9 -character maximum) and be in alphanumeric format.  
Note:  
Use the [[CUSIP]] Finder         function if only the root of the [[CUSIP]]  is known. Click on this icon 
to open a popup window to search for a particular [[CUSIP]]. If you select a [[CUSIP]] from the 
popup screen, the [[CUSIP]] will be populated in the field.  
Trader [[ID]] Enter the unique identifier of the Trader  (10-character maximum, no spe cial characters ). 
Trade Date This is a mandatory field. Specify the date the trade was executed. Format = mm/dd/ yyyy.  
Trade Time Specify the time when the trade was executed. Format = hh 24:mm:ss. 
[[settlement]] Date This is a mandatory field. Specify the [[settlement]]  Date of the trade. Format = mm/dd/yyyy. 
Pricing Method This is a mandatory field.  Specify the Price Type of the trade(s).  
Choose : D = discount, P = price, or Y = yield.  
Executing Firm Symbol  Enter the 4- or 5-character [[ID]] (5-character maximum) of the Executing Firm , if applicable . 
[[Broker]] Xref Dealers - Dealers may leave this field blank.  
Repo Brokers - This is a mandatory field for [[Broker]] submissions. Specify the [[Broker]] Xref 
number of the trade being entered  (18-character maximum, no special characters ). 
Transaction Type  This is a mandatory field. Select either Buy , Sell, or both checkboxes.  


---

## Page 50

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 50 
Field/Item Name  Instructions/Descriptions 
Buy / Sell Transaction 
Details / Allocation 
Section 
These fields describe the economic details of a Buy/Sell Transaction as the fields are 
the same for both Transaction  Types. 
Par This is a mandatory field. Enter the par value, where each row cannot exceed 50M  (18-
character maximum, incl. commas ). If your par value exceeds 50M, use either the Add Row 
or Copy Row button to add another row.  
Price This is a mandatory field. Specify the Contract Price  (14-character maximum, 10 decimal  
places maximum).  
[[settlement]] Amount  Enter the Amount f or final money  (18-character maximum, incl. commas and 2 decimal  
places ).  If this field is left blank, the amount is calculated by the system.   
Commission  Enter the Commission  (10 decimal places maximum), as applicable.  
Contra [[ID]] This is a mandatory field. You can either enter the 4- digit [[GSD]] [[Member]] [[ID]] associated with 
the contra -party or select the contra -party’s [[Member]] [[ID]] and Name from the dropdown list, 
which lists all available [[GSD]] Members.  
Contra Exec. Firm  Enter the 4- or 5-character [[ID]] (5-character maximum) of the Contra Executing Firm , if 
applicable. 
Trade Xref This is a mandatory field. Enter your reference number for the trade ( 16-character maximum, 
no special characters ).  
Note:  
Each trade must have a unique Xref . 
Icon/Button  Instructions/Description 
 Click to add a row.  
 Click to select a singular date or a date range, as applicabl e.  
 Located parallel and to the right of the Transaction Type field, click to copy all the data 
entered on the Buy side (except for the Xref entry) to the Sell side of the Allocation section. 
Allows the user to add  up to 5 rows of copied trade data.  
 Click to copy all the data from the current row to a new row, except the Xref. This differs 
from the Add Row icon.  
* Indicates a required field.  
 Click to delete a row.  
 Click the down arrow to display a dropdown menu from which you can make a selection.  
 Click to close the selected window.  
Reset Returns the fields on current screen to the original [[default]] values.  
Submit Click to submit the data you entered on the Trade Entry screen.  


---

## Page 51

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 51 
Field/Item Name  Instructions/Descriptions 
Validate Click to validate  your trade entry versus the [[GSD]] system  prior to submission. 
Validation / Submission 
Results 
Instructions/Description 
Status Indicator  
Indicates a rejected submission status of an entry. 
 Indicates a warning/pending submission status of an entry.  
Indicates an accepted submission status of an entry. 
 Indicates an  entry has been validated/accepted . 
Net Eligible  
The system populates this field upon validation and acceptance of a trade entry. It indicates 
whether the trade is subject to the net.  
• Y indicates Yes the trade is subject to the net.  
• N indicates No the trade is not subject to the net.  
Reject [[ID]] System generated  identifier that i ndicates the [[ID]] of a rejected trade entry.  
Trade [[ID]] (TID)  System generated identifier that indicates the [[ID]] of an accepted trade entry.  
Trade State Indicates the Trade State of a single trade entry, which can be any of the following: CAN, 
CMP, CNR, CPA, CPN, CPS, PCN, PCP, NVT, or PPC.   
Note:  
On submission of a trade entry, the Trade State will almost always be PCP (Pending 
Comparison) . 
Table 15: DVP Buy / Sell Trade Entry Screen Field Descriptions 
  


---

## Page 52

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 52 
Enter a Repo / Reverse Repo Transaction 
To enter a Repo and/or Reverse Repo Transaction, the user must enter the required information (*) in the 
Trade Details section (Product, [[CUSIP]], Trade Date, [[settlement]] Date, Pricing Method, [[Broker]] Xref (for [[Broker]] 
submissions only) and Transaction Type) and in the Allocation section (Par, Price, Contra [[ID]], and Trade 
Reference (Xref) Number).  
Note:  
The [[Member]] [[ID]] is preselected by [[default]]  and the availability of the DVP and/or GCF/CCIT Product type will depend on the 
membership type of the user’s [[Member]] firm.  
Note:  
Once the Transaction Type is selected, the screen will update to display the Allocation section as seen below.  
 
Figure 37: DVP Repo / Revr Trade Entry Screen w/ Allocation section (fields unpopulated)  


---

## Page 53

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 53 
To submit a Repo and/or Revr Transaction, the user must populate the fields in the Trade Details section and 
the Allocation section as seen below.  
 
Figure 38: DVP Repo / Revr Trade Entry Screen (fields populated) – Pre-Validation 
 
If the user has additional trades to enter with different particulars, then the user would select the + Add Row 
button and enter the additional trade details, as applicable. 
Note:  
Up to 5 rows can be entered for each Transaction type (trade side), per submission, i.e., 5 Repo Transactions and 5 
Reverse Transactions can be submitted at one time.  
Note: 
If the user h as to enter both trade sides (Repo and Reverse) and the Reverse allocation(s) are similar to the Repo 
allocation( s), then the user can use the Copy Side      icon (located to the right of the Transaction Type field) to copy all  the 
data for the Repo alloca tion(s) into the Reverse allocation(s) section (except the Xref(s)  which must be unique and 
therefore entered  separately .  


---

## Page 54

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 54 
Note:  
The max par value that is allowed to be submitted per row is $50 million.  If the total par value of the transaction is greater 
than $50 million, then the user can use th e Copy Row      icon t o copy all of the data from the current row into a new row 
(except the Xref(s), which must be unique and therefore entered  separately).   
Note:  
To delete a row added in error select the Delete Row     icon.  
Once all of relevant details are entered, the user should select the Validate button. Once the Validate button is 
selected, the system will check the trade entry against its validation rules. Validating entries before submission 
will alert the user to any system trade validation issues. The system will display a message that either 1) the 
trades were successfully validated or 2) One or more of the trades failed validation. 
See below for an example of trades successfully validated by the system. 
 
Figure 39: DVP Repo / Revr Trade Entry Successfully Validated 
  


---

## Page 55

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 55 
See below for an example of trades that failed validation. 
 
Figure 40: DVP Repo / Revr Trade Entry Failed Validation 
 
If one or more trades failed validation, the user can modify the trade details in order for the trade(s) to pass the 
system’s trade validation process. To see why a particular trade failed validation, the user should click the 
Warning       icon located to the right of the trade. A popup window will appear.  
 
  


---

## Page 56

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 56 
The popup window would display one or more possible trade errors that the user may need to resolve before 
submitting the trade. 
 
Figure 41: DVP Trade Entry Validation: Trade Errors Popup Window – Final Money Differs from Calculated 
Amount 
 
In the above example, the user can select to use the money entered as final money or use the system’s 
calculated money. For simplification, the System Money has been selected using the Select button. Once the 
[[Option]] is selected, the popup window will close, and the final money field will update to reflect the selected 
value.  
If the user is alerted to a trade error that is not modifiable from the popup window, the user should view the 
trade error and then close the window by using the Close button. Then the user should make the necessary 
modifications in the Trade Entry screen. See below for an example of a trade error that must be modified in the 
Trade Entry screen. 
 
Figure 42: DVP Trade Entry Validation: Trade Errors Popup Window – Security Not Found 
 


---

## Page 57

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 57 
The above trade error occurs when a trade is entered with a [[CUSIP]] that is not in the [[GSD]] Security Masterfile. 
This error can occur if the user enters an invalid [[CUSIP]] or a [[CUSIP]] that has not been setup in the [[GSD]] 
Security Masterfile. The user would need to close this popup window and edit the [[CUSIP]] field.  
If the Warning      icon appears for more than one trade, click the Warning      icon for each trade to display the 
possible Trade Errors and address any and all relevant errors that would cause the system not to validate the 
trade submission. Once all of errors have been addressed, the user may select the Validate button again. If no 
further warnings appear, the user should select the Submit button to submit the trade(s) to [[GSD]] RTTM Web for 
processing. 
If the user selects the Submit button in lieu of the Validate button, the system will check the trade entry against 
its validation rules. The system will display a message that either 1) the trades have been accepted or 2) the 
trades have been rejected. 
 
Figure 43: DVP Repo / Revr Trade Entry Submission (in leu of Validation) 
  


---

## Page 58

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 58 
See below for an example of trades accepted by the system successfully. 
 
Figure 44: DVP Repo / Revr Trade Entry Accepted (comparable to MT509 Trade Input Accepted (PACK) 
Message) 
 
Upon validation and submission, each trade is assigned a unique identifier, the Trade [[ID]] (TID). 
 
  


---

## Page 59

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 59 
See below for an example of trades rejected by the system. 
 
Figure 45: DVP Repo / Revr Trade Entry Rejected (comparable to MT509 Trade Input Rejected (REJT) 
Message) 
Once the system completes its trade validation process after initial submission, each rejected trade is assigned 
a unique identifier, a Reject [[ID]]. Hover over the Reject [[ID]] and it will display as “Rejected” . Click the Reject [[ID]] 
for each rejected trade to display the possible Trade Errors so that they may be corrected. A popup window will 
appear. The popup window would display one or more possible trade errors that the user must resolve before 
submitting the trade. Once all of errors have been addressed, the user may select the Submit button again. 
 
Figure 46: Trade Entry Validation: Trade Errors Popup Window – Xref Already Exists 


---

## Page 60

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 60 
For instructions and field descriptions regarding the DVP Repo / Revr Trade Entry screen, please refer to the 
below table.  
Note:  
The fields  described in the table below are organized in the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom  within each section).  
Field/Item Name  Instructions/Descriptions 
Trade Details 
[[Member]] [[ID]] The system will automatically [[default]] to the 4- digit [[GSD]] [[Member]] [[ID]] and Name associated 
with the user’s logon credentials.  
Note:  
The [[Member]] [[ID]] field defaults to the [[GSD]] [[Member]] [[ID]] and Name associated with the user’s 
logon credentials with the exception of users that have multiple [[Member]] IDs associated with 
their logon credentials.  
Product  This is a mandatory field. Specify the Product of the trade that is being entered.  
[[CUSIP]] This is a mandatory field. Enter the [[CUSIP]] number of the security for the trade. This field 
must contain the whole [[CUSIP]] (9 -character maximum) and be in alphanumeric format.  
Note:  
Use the [[CUSIP]] Finder         function if only the root of the [[CUSIP]] is known. Click on this icon 
to open a popup window to search for a particular [[CUSIP]]. If you select a [[CUSIP]] from the 
popup screen, the [[CUSIP]] will be populated in the field.  
Trader [[ID]] Enter the unique identifier of the Trader  (10-character maximum, no special characters ). 
Trade Date This is a mandatory field. Specify the date the trade was executed. Format = mm/dd/ yyyy.  
Trade Time Specify the time when the trade was executed. Format = hh 24:mm:ss. 
Start Date This is a mandatory field. Specify the Repo Start D ate of the trade. Format = mm/dd/yyyy. 
[[settlement]] Date This is a mandatory field. Specify the Repo End Date of the trade. Format = mm/dd/yyyy.  
Executing Firm Symbol  Enter the 4- or 5-character [[ID]] (5-character maximum)  of the Executing Firm , if applicable . 
[[Broker]] Xref Dealers - Dealers may leave this field blank.  
Repo Brokers - This is a mandatory field for [[Broker]] submissions. Specify the [[Broker]] Xref 
number of the trade being entered  (18-character maximum, no special c haracters) . 
Transaction Type  This is a mandatory field. Select either Repo , Revr, or both checkboxes.  
Repo / Reverse 
Transaction Details / 
Allocation Section  
These fields describe the economic details of a Repo /Reverse Transaction as the 
fields are the same for both Transaction types.  
Par This is a mandatory field. Enter the par value, where each row cannot exceed 50M (18-
character maximum, incl. commas ). If your par value exceeds 50M, use either the Add Row 
or Copy Row button to add another row.  


---

## Page 61

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 61 
Field/Item Name  Instructions/Descriptions 
Start Money  This is a mandatory field. Specify the Start Money  (18-character maximum, incl. commas 
and 2 decimal places) . 
Repo Rate (%)  This is a mandatory field. Specify the Contract Repo Rate for the Repo or Revr  (14-
character maximum, 10 decimal places maximum) .  
Final Money  Enter the Amount f or final money  (18-character maximum, incl. commas and 2 decimal 
places) . If this field is left blank, the amount is calculated by the system.  
Accrued To Date Specifies the Accrued Interest.  The amount is c alculated by the system.  
Contra [[ID]] This is a mandatory field. You can either enter the 4- digit [[GSD]] [[Member]] [[ID]] associated with 
the contra -party or select the contra -party’s [[Member]] [[ID]] and Name from the dropdown list, 
which lists all available [[GSD]] Members.   
Contra Exec. Firm  Enter the 4- or 5-character [[ID]] (5-character maximum) of the Contra Executing Firm , if 
applicable. 
Trade Xref This is a mandatory field. Enter the  reference number for the trade (1 6-character maximum, 
no special characters) .  
Note:  
Each trade must have a unique Xref.  
Icon/Button  Instructions/Description 
 Click to add a row.  
 Click to select a singular date or a date range, as applicable.  
 Located parallel and to the right of the Transaction Type field, click to copy all the data 
entered on the Repo side (except for the Xref entry) to the Revr side of the Allocation 
section. Allows the user to add up to 5 rows of copied trade data.  
 Click to copy all the data from the current row to a new row, except the Xref. This differs 
from the Add Row icon.  
* Indicates a required field.  
 Click to delete a row.  
 Click the down arrow to display a dropdown menu from which you can make a selection.  
 Click to close the selected window.  
Reset Returns the fields on current screen to the original [[default]] values.  
Submit Click to submit the data you entered on the Trade Entry screen.  
Validate Click to validate your trade entry versus the [[GSD]] system prior to submission.  
Validation / Submission 
Results 
Instructions/Description 
Status Indicator  
Indicates a rejected submission status of an entry. 
 Indicates a warning/pending submission status of an entry.  
Indicates an accepted submission status of an entry. 


---

## Page 62

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 62 
Field/Item Name  Instructions/Descriptions 
 Indicates an  entry has been validated/accepted . 
Net Eligible  
The system populates this field upon validation and acceptance of a trade entry. It indicates 
whether the trade is subject to the net.  
• Y indicates Yes the trade is subject to the net.  
• N indicates No the tr ade is not subject to the net.  
Reject [[ID]] System generated  identifier that i ndicates the [[ID]] of a rejected trade entry.  
Trade [[ID]] (TID)  System generated identifier that indicates the [[ID]] of an accepted trade entry.  
Trade State Indicates the Trade State of a single trade entry, which can be any of the following: CAN, 
CMP, CNR, CPA, CPN, CPS, PCN, PCP, NVT, or PPC.   
Note:  
On submission of a trade entry, the Trade State will almost always be PCP (Pending 
Comparison) . 
Table 16: DVP Repo / Revr Trade Entry Screen Field Descriptions 
  


---

## Page 63

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 63 
GCF Trade Entry 
This section will explain to the user how to use the GCF / CCIT Trade Entry screens to enter Repo and 
Reverse Repo Transactions as a [[Broker]]. 
Enter a Repo / Reverse Repo Transaction – [[Broker]] 
To enter a Brokered GCF Repo and GCF Reverse Repo Transaction, the user must enter the required 
information (*) in the Trade Details section (Product, [[CUSIP]], Trade Date, Start Date, End Date, and [[Broker]] 
Xref (for [[Broker]] submissions only)) and in the Allocation section (Start Money, Repo Rate, Contra [[ID]], and 
Trade Reference (Xref) Number).  
Note:  
Once the GCF / CCIT Product is selected, the system will preselect the checkbox es for both Repo and Reverse in the 
Transaction Type field, if the [[Member]] account in the [[Member]] [[ID]] field is categorized in the system as a [[Broker]]. The 
Transaction Type field will not be come editable unless the DVP Product is selected or a “non- [[Broker]]” [[Member]] is selected 
from the [[Member]] [[ID]] field .   
Note:  
The [[Member]] [[ID]] is preselected by [[default]]  and the availability of the DVP and/or GCF/CCIT Product type will depend on the 
membership type of the user’s [[Member]] firm.  
 
Figure 47: GCF / CCIT ([[Broker]]) Repo / Revr Trade Entry Screen w/ Allocation section (fields unpopulated)  


---

## Page 64

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 64 
To submit a GCF Brokered Repo and Revr Transaction, the user must populate the fields in the Trade Details 
section and the Allocation section as seen below.  
 
Figure 48: GCF / CCIT ([[Broker]]) Repo / Revr Trade Entry Screen (fields populated) – Pre-Validation 
 
Certain fields are calculated by the system, i.e., Repo Term and Final Money. 
For efficiency, you may select the checkbox “Retain Trade Details on Reset”. After selecting the Submit button 
to process the current trade submission, select the Reset button. This will reset the Allocation section of the 
screen and allow you to enter repeat trade entries, with similar trade details, quicker. Each time the Reset 
button is selected after a trade submission, select the checkbox for “Retain Trade Details on Reset”, if the next 
trade entry has similar details. 
Note:  
The max par value that can be submitted via RTTM Web is $2 billion  on each transaction (side) .  
The max par value that can be submitted via MQ (IM SWIFT MT515) is $9.999 billion  on each transaction (side).  
  


---

## Page 65

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 65 
Once all of relevant details are entered, the user should select the Validate button. Once the Validate button is 
selected, the system will check the trade entry against its validation rules. Validating entries before submission 
will alert the user to any system trade validation issues. The system will display a message that either 1) the 
trades were successfully validated or 2) One or more of the trades failed validation. 
See below for an example of trades successfully validated by the system. 
 
Figure 49: GCF / CCIT ([[Broker]]) Repo / Revr Trade Entry Successfully Validated 
  


---

## Page 66

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 66 
See below for an example of trades that failed validation. 
 
Figure 50: GCF / CCIT ([[Broker]]) Repo / Revr Trade Entry Failed Validation 
 
If one or more trades failed validation, the user can modify the trade details in order for the trade(s) to pass the 
system’s trade validation process. To see why a particular trade failed validation, the user should click the 
Warning       icon located to the right of the trade. A popup window will appear.  
  


---

## Page 67

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 67 
The popup window would display one or more possible trade errors that the user may need to resolve before 
submitting the trade. 
 
Figure 51: Trade Entry Validation: Trade Errors Popup Window – Repo Dealer Locked-In relationship not 
established 
 
In the above example, the user will need to change the Repo Dealer entered on the Trade Entry screen to a 
Repo Dealer (Netting [[Member]]/GCF Counterparty) that the [[Broker]] has an established relationship with and 
such relationship is captured in the [[GSD]] system. This is not modifiable in the popup window.  
If the user is alerted to a trade error that is not modifiable from the popup window, the user should view the 
trade error and then close the window by using the Close button. Then the user should make the necessary 
modifications in the Trade Entry screen.  
If the Warning      icon appears for more than one trade, click the Warning      icon for each trade to display the 
possible Trade Errors and address any and all relevant errors that would cause the system not to validate the 
trade submission. Once all of errors have been addressed, the user may select the Validate button again. If no 
further warnings appear, the user should select the Submit button to submit the trade(s) to [[GSD]] RTTM Web for 
processing. 
  


---

## Page 68

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 68 
If the user selects the Submit button in lieu of the Validate button, the system will check the trade entry against 
its validation rules. The system will display a message that either 1) the trades have been accepted or 2) the 
trades have been rejected. 
 
Figure 52: GCF / CCIT ([[Broker]]) Repo / Revr Trade Entry Submission (in leu of Validation) 
  


---

## Page 69

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 69 
See below for an example of trades accepted by the system successfully. 
 
Figure 53: GCF / CCIT ([[Broker]]) Repo / Revr Trade Entry Accepted (comparable to MT509 Trade Input 
Accepted (PACK) Message) 
 
Upon validation and submission, each trade is assigned a unique identifier, the Trade [[ID]] (TID). 
 
  


---

## Page 70

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 70 
See below for an example of trades rejected by the system. 
 
Figure 54: GCF / CCIT ([[Broker]]) Repo / Revr Trade Entry Rejected (comparable to MT509 Trade Input 
Rejected (REJT) Message) 
 
Once the system completes its trade validation process after initial submission, and one or more trades failed 
validation, the user can see why a particular trade failed validation by clicking the Reject      icon located to the 
right of the trade. Once the Reject      icon is selected, a popup window will appear. The popup window would 
display one or more possible trade errors that the user must resolve before resubmitting the trade.  
 
Figure 55: Trade Entry Validation: Trade Errors Popup Window – End Date is not a Business Day 
Once all of errors have been addressed, the user may select the Submit button again. 


---

## Page 71

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 71 
For instructions and field descriptions regarding the GCF / CCIT [[Broker]] Repo / Revr Trade Entry screen, 
please refer to the below table.  
Note:  
The fields  described in the table below are organized in the same order as they appear on the screen (i.e., movin g from left 
to right and top to bottom  within each section).  
Field/Item Name  Instructions/Descriptions 
Trade Details 
[[Member]] [[ID]] The system will automatically [[default]] to the 4- digit [[GSD]] [[Member]] [[ID]] and Name associated 
with the user’s logon credentials.  
Note:  
The [[Member]] [[ID]] field defaults to the [[GSD]] [[Member]] [[ID]] and Name associated with the user’s 
logon credentials with the exception of users that have multiple [[Member]] IDs associated with 
their logon credentials.  
Product  This is a mandatory field. Specify the Product of the trade that is being entered.  
[[CUSIP]] This is a mandatory field. Select the GCF Repo Generic [[CUSIP]] Number  for the trade. This 
field contain s dropdown list of the GCF Repo Generic [[CUSIP]] Numbers:  371487AD1, 
371487AE9, 371487AH2, 371487AL3, 371487AQ2, 371487AM1, 371487AR0, 371487AG4 
and 371487AF6. 
Trade Date This is a mandatory field. Specify the date the trade was executed. Format = mm/dd/ yyyy.  
Start Date This is a mandatory field. Spec ify the Repo Start Date of the trade. Format = mm/dd/yyyy. 
End Date This is a mandatory field. Specify the Repo End Date of the trade. Format = mm/dd/yyyy.  
Repo Term Trade term in number of days . 
Transaction Type  This is a mandatory field. Select either Repo, Rev erse, or both checkboxes. For CCIT 
Members, the Reverse checkbox is automatically selected. For Brokers, both Repo and 
Reverse checkboxes are selected.  
Repo / Reverse 
Transaction Details / 
Allocation Section  
These fields describe the economic details of a Repo /Reverse Transaction  as the 
fields are the same for both Transaction types. 
Start Money  This is a mandatory field. Specify the Start Money  (18-character maximum, incl. commas 
and 2 decimal places) . 
Repo Rate (%)  This is a mandatory field. Specify the Contract Repo Rate for the Repo or Revr (14 -
character maximum, 6 decimal places maximum).  
Final Money  Enter the Amount f or final money  (18-character maximum, incl. commas and 2 decimal 
places) . If this field is left blank, the amount is calculated by the system.  
Accrued To Date Specifies the Accrued Interest.  The amount is calculated by the system.  
Contra [[ID]] This is a mandatory field. You can either enter the 4- digit [[GSD]] [[Member]] [[ID]] associated with 
the contra -party or  select the contra- party’s [[Member]] [[ID]] and Name from the dropdown list, 
which lists all available [[GSD]] Members.  

---

## Page 72

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 72 
Field/Item Name  Instructions/Descriptions 
Trade Xref This is a mandatory field. Enter the  reference number for the trade (16-character maximum, 
no special characters).   
Note:  
Each trade must have a unique Xref.  
Icon/Button  Instructions/Description 
 Click to select a singular date or a date range, as applicable.  
* Indicates a required field.  
 Click the down arrow to display a dropdown menu from which you can make a selection.  
 Click to close the selected window.  
Reset Returns the fields on current screen to the original [[default]] values.  
Submit Click to submit the data you entered on the Trade Entry screen.  
Validate Click to validate your trade entry versus the [[GSD]] system prior to submission.  
Validation / Submission 
Results 
Instructions/Description 
Status Indicator  
Indicates a rejected submission status of an entry. 
 Indicates a warning/pending submission status of an entry.  
Indicates an accepted submission status of an entry. 
 Indicates an  entry has been validated/accepted . 
[[Broker]] Trade [[ID]] (TID)  System generated identifier that indicates the [[ID]] of an accepted trade entry.  
Table 17: GCF / CCIT ([[Broker]]) Repo / Revr Trade Entry Screen Field Descriptions 
 
  


---

## Page 73

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 73 
Enter a Repo / Reverse Repo Transaction – CCIT [[Member]] / Dealer 
To enter a CCIT Transaction, the user must enter the required information (*) in the Trade Details section 
(Product, [[CUSIP]], Trade Date, Start Date, End Date) and in the Allocation section (Start Money, Repo Rate, 
Contra [[ID]], and Trade Reference (Xref) Number).  
Note:  
For CCIT Members - Once the GCF / CCIT Product is selected, the system will preselect the checkbox for Reverse in the 
Transaction Type field.   
Note:  
The [[Member]] [[ID]]  is preselected by [[default]]  and the availability of the DVP and/or GCF/CCIT Product type will depend on the 
membership type of the user’s [[Member]] firm.  
 
Figure 56: GCF / CCIT (CCIT [[Member]] / GCF Netting [[Member]]) Repo / Revr Trade Entry Screen w/ Allocation 
section (fields unpopulated) 
  


---

## Page 74

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 74 
To submit a Bilateral Repo or Revr Transaction, the user must populate the fields in the Trade Details section 
and the Allocation section as seen below.  
 
Figure 57: GCF / CCIT (CCIT [[Member]] / GCF Netting [[Member]]) Repo / Revr Trade Entry Screen (fields 
populated) – Pre-Validation 
 
Certain fields are calculated by the system, i.e., Repo Term and Final Money. 
For efficiency, you may select the checkbox “Retain Trade Details on Reset”. After selecting the Submit button 
to process the current trade submission, select the Reset button. This will reset the Allocation section of the 
screen and allow you to enter repeat trade entries, with similar trade details quicker. Each time the Reset 
button is selected after a trade submission, select the checkbox for “Retain Trade Details on Reset”, if the next 
trade entry has similar details. 
 
Note:  
The max par value that can be submitted via RTTM Web is $2 billion on each transaction (side).   
The max par value that can be submitted via MQ (IM SWIFT MT515) is $9.999 billion on eac h transaction (side).  
  


---

## Page 75

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 75 
Once all of relevant details are entered, the user should select the Validate button. Once the Validate button is 
selected, the system will check the trade entry against its validation rules. Validating entries before submission 
will alert the user to any system trade validation issues. The system will display a message that either 1) the 
trades were successfully validated or 2) One or more of the trades failed validation. 
See below for an example of trades successfully validated by the system. 
 
Figure 58: GCF / CCIT (CCIT [[Member]] / GCF Netting [[Member]]) Repo / Revr Trade Entry Successfully Validated 
 
 
 
 
 
 
 
 
  


---

## Page 76

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 76 
See below for an example of trades that failed validation. 
 
Figure 59: GCF / CCIT (CCIT [[Member]] / GCF Netting [[Member]]) Repo / Revr Trade Entry Failed Validation 
 
If one or more trades failed validation, the user can modify the trade details in order for the trade(s) to pass the 
system’s trade validation process. To see why a particular trade failed validation, the user should click the 
Warning       icon located to the right of the trade. A popup window will appear.  
 
  


---

## Page 77

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 77 
The popup window would display one or more possible trade errors that the user may need to resolve before 
submitting the trade. 
 
Figure 60: Trade Entry Validation: Trade Errors Popup Window – Buy Side and Contra should clear at same 
Bank 
 
In the above example, the user will need to change the Contra entered on the Trade Entry screen to a Netting 
[[Member]] that clears through the same GCF Clearing Agent Bank as the CCIT [[Member]]. This is not modifiable in 
the popup window.  
If the user is alerted to a trade error that is not modifiable from the popup window, the user should view the 
trade error and then close the window by using the Close button. Then the user should make the necessary 
modifications in the Trade Entry screen.  
If the Warning      icon appears for more than one trade, click the Warning      icon for each trade to display the 
possible Trade Errors and address any and all relevant errors that would cause the system not to validate the 
trade submission. Once all of errors have been addressed, the user may select the Validate button again. If no 
further warnings appear, the user should select the Submit button to submit the trade(s) to [[GSD]] RTTM Web for 
processing. 
 
 
 
 
 
 
 
 
 


---

## Page 78

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 78 
If the user selects the Submit button in lieu of the Validate button, the system will check the trade entry against 
its validation rules. The system will display a message that either 1) the trades have been accepted or 2) the 
trades have been rejected. 
 
Figure 61: GCF / CCIT (CCIT [[Member]] / GCF Netting [[Member]]) Repo / Revr Trade Entry Submission (in leu of 
Validation) 
 
 
  


---

## Page 79

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 79 
See below for an example of trades accepted by the system successfully. 
 
Figure 62:GCF / CCIT (CCIT [[Member]] / GCF Netting [[Member]]) Repo / Revr Trade Entry Accepted (comparable 
to MT509 Trade Input Accepted (PACK) Message) 
 
Upon validation and submission, each trade is assigned a unique identifier, the Trade [[ID]] (TID). 
 
  


---

## Page 80

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 80 
See below for an example of trades rejected by the system. 
 
Figure 63: GCF / CCIT (CCIT [[Member]] / GCF Netting [[Member]]) Repo / Revr Trade Entry Rejected (comparable 
to MT509 Trade Input Rejected (REJT) Message) 
 
Once the system completes its trade validation process after initial submission, and one or more trades failed 
validation, the user can see why a particular trade failed validation by clicking the Reject      icon located to the 
right of the trade. Once the Reject      icon is selected, a popup window will appear. The popup window would 
display one or more possible trade errors that the user must resolve before resubmitting the trade.  
 
  


---

## Page 81

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 81 
For instructions and field descriptions regarding the GCF / CCIT (CCIT [[Member]] / GCF Netting [[Member]]) Repo / 
Revr Trade Entry screen, please refer to the below table.  
Note:  
The fields  described in the table below are organized in the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom  within each section).  
Field/Item Name  Instructions/Descriptions 
Trade Details 
[[Member]] [[ID]] The system will automatically [[default]] to the 4- digit [[GSD]] [[Member]] [[ID]] and Name associated 
with the user’s logon credentials.  
Note:  
The [[Member]] [[ID]] field defaults to the [[GSD]] [[Member]] [[ID]] and Name associated with the user’s 
logon credentials with the exception of users that have multiple [[Member]] IDs associated with 
their logon credentials.  
Product  This is a mandatory field. Specify the Product of the trade that is being entered.  
[[CUSIP]] This is a mandatory field. Select the GCF Repo Generic [[CUSIP]] Number  for the trade. This 
field contains a dropdown list of the GCF Repo Generic [[CUSIP]] Numbers:  371487AD1, 
371487AE9, 371487AH2, 371487AL3, 371487AQ2, 371487AM1, 371487AR0, 371487AG4 
and 371487AF6. 
Trade Date This is a mandatory field. Specify the date the trade was executed. Format = mm/dd/ yyyy.  
Start Date This is a mandatory field. Spec ify the Repo Start Date of the trade. Format = mm/dd/yyyy. 
End Date This is a mandatory field. Specify the Repo End Date of the trade. Format = mm/dd/yyyy.  
Repo Term Trade term in number of days . 
Transaction Type  This is a mandatory field. Select either Repo , Revr, or both checkboxes. For CCIT Members, 
the Reverse checkbox is automatically selected. For  Brokers, both Repo and Rev erse 
checkboxes are selected.  
Repo / Reverse 
Transaction Details / 
Allocation Section  
These fields describe the economic details of a Repo /Reverse Transaction  as the 
fields are the same for both Transaction types. 
Start Money  This is a mandatory field. Specify the Start Money  (18-character maximum, incl. commas 
and 2 decimal places).  
Repo  Rate (%)  This is a mandatory field. Specify the Contract Repo Rate for the Repo or Revr (14 -
character maximum, 10 decimal places maximum).  
Final Money  Enter the Amount f or final money  (18-character maximum, incl. commas and 2 decimal 
places) . If this field is left blank, the amount is calculated by the system.  
Accrued To Date Specifies the Accrued Interest . The amount is calculated by the system.  
Contra [[ID]] This is a mandatory field. You can either enter the 4- digit [[GSD]] [[Member]] [[ID]] associated with 
the contra -party or select the contra -party’s [[Member]] [[ID]] and Name from the dropdown list, 
which lists all available [[GSD]] Members.  

---

## Page 82

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 82 
Field/Item Name  Instructions/Descriptions 
Trade Xref This is a mandatory field. Enter the  reference number  for the trade  (16-character maximum, 
no special characters).  
Note:  
Each trade must have a unique Xref.  
Icon/Button  Instructions/Description 
 Click to select a singular date or a date range, as applicable.  
* Indicates a required field.  
 Click the down arrow to display a dropdown menu from which you can make a selection.  
 Click to close the selected window.  
Reset Returns the fields on current screen to the original [[default]] values.  
Submit Click to submit the data you entered on the Trade Entry screen.  
Validate Click to validate your trade entry versus the [[GSD]] system prior to submission.  
Validation / Submission 
Results 
Instructions/Description 
Status Indicator  
Indicates a rejected submission status of an entry. 
 Indicates a warning/pending submission status of an entry.  
Indicates an accepted submission status of an entry. 
 Indicates an  entry has been validated/accepted . 
Dealer / CCIT Trade [[ID]] 
(TID) 
System generated identifier that indicates the [[ID]] of an accepted trade entry.  
Table 18: GCF / CCIT (CCIT [[Member]] / GCF Netting [[Member]]) Repo / Revr Trade Entry Screen Field 
Descriptions 
  


---

## Page 83

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 83 
Trades > Search & Management 
From the Trades > Search & Management menu selection, all users with the appropriate access can query 
trades and manage the status on your active trades.  
 
Figure 64: Trades > Search & Management 
DVP Trade Search & Management 
The DVP Trade Search functionality in [[GSD]] RTTM Web allows users to query both active trades and trades in 
[[GSD]]’s historical database. The trade search function also provides users with the ability to search for a specific 
trade or multiple trades that fit within specified parameters.  
DVP Advanced Search  
Upon selecting the Trades > Search & Management menu [[Option]], the Advanced Search screen will appear. 
This screen appears by [[default]]. From this screen, the user can select the DVP Product and search for a single 
DVP trade or multiple DVP trades using various parameters and criteria.  
 
Figure 65: DVP Advanced Search Screen 


---

## Page 84

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 84 
See below for a full screen view of the DVP search parameters available. Populate the required fields marked 
with a red asterisk ( * ). The remaining fields are optional, and allow you to refine your search parameters 
further. To broaden your se arch, enter less criteria. Once the search criteria has been entered, click th e Search 
button to view the trade search results. 
 
Figure 66: DVP Advanced Search Screen - Full View 
 
 


---

## Page 85

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 85 
For instructions and field descriptions regarding the DVP Advanced Search screen, please refer to the below 
table.  
Note:  
The fields  described in the table below are organized in the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom  within each section).  
Field/Item Name  Instructions/Descriptions 
Trade Details 
[[Member]] [[ID]] The system will automatically [[default]] to the 4- digit [[GSD]] [[Member]] [[ID]] and Name associated 
with the user’s logon credentials.  
Note:  
The [[Member]] [[ID]] field defaults to the [[GSD]] [[Member]] [[ID]] and Name associated with the user’s 
logon credentials with the exception of u sers that have multiple [[Member]] IDs associated with 
their logon credentials.  
TID / Xref / [[Broker]] Xref This field is used when a user wants to retrieve details for a specific trade or trades within a 
block of trades (via [[Broker]] Xref only).  
• From the dropdown menu, select either TID, Xref or [[Broker]] Xref, if applicable.  
• Then enter the number for the selected reference number . 
Business Date Range This is a mandatory field. Enter the date range to be search ed. For the “From” date, select 
the earliest date for the desired period. Then for the “To” date, select the latest date for the 
desired period.  
Product  This is a mandatory field. S elect DVP as the Product for searches pertaining  to DVP trades. 
[[CUSIP]] Enter the [[CUSIP]] number of the security for the trade. Thi s field must contain a minimum of 
4-characters for the wildcard functionality , a maximum of 9-character s for the whole [[CUSIP]] 
with no special characters  and be in alphanumeric format.  
Note:  
Use the [[CUSIP]] Finder         function if only the root of the [[CUSIP]] is known. Click on this icon 
to open a popup window to search for a particular [[CUSIP]]. If you select a [[CUSIP]] from the 
popup screen, the [[CUSIP]] will be populated in the field.  
[[settlement]] Date Range Enter the date range to be search ed. For the “From” date, select the earliest date for the 
desired period. Then for the “To” date, select the latest date for the desired period.  
Trade Active or Trade 
History  
This is a mandatory field . Specify whether the trade search  is for active or his torical trad es. 
Par To search by this criteri on, the following fields/boxes must be completed:  
• Select one of the comparison  operators from the dropdown list: =,  >, <, >=, <=, <>. 
• Specify the par value of the desired trade(s).  
Trade Date Range  Enter the date range to be search ed. For the “From” date, select the earliest date for the 
desired period. Then for the “To” date, select the latest date for the desired period.  


---

## Page 86

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 86 
Field/Item Name  Instructions/Descriptions 
Transaction Type  This is a mandatory field. Select  the Repo, Revr, Buy and/ or Sell checkbox( es).  
[[settlement]] Amount  To search by this criteri on, the following fields/boxes must be completed:  
• Select one of the comparison  operators from the dropdown list: =, >, <, >=, <=, <>. 
• Specify the amount of the desired trade(s).  
Submission Date Range Enter the date range to be search ed. For the “From” date, select the earliest date for the 
desired period. Then for the “To” date, select the latest date for the desired period.  
Trade State / Advisories  The Trade State field offers t wo search options:  
• You can limit your search results by selecting one or more of the following Trade State(s):  
o Compared – Assigned to trades compared on the current business date, where a 
trade is matched either through an offsetting bilateral trade submission, a demand 
trade submission or  a locked -in trade submission. Compared trades cannot be 
unilaterally canceled; both sides must submit a cancellation request.  
o Compared Pending Auction – Assigned to compared trades, which were submitted 
with a yield price  before the auction date. The final  money cannot be calculated until 
the coupon of the security has been assigned  on auction date. 
o Compared Pending [[Novation]] – Assigned to compared trades, where the S tart Leg 
[[settlement]] Date is greater than the current business date. 
o Compared Pending [[settlement]] – Assigned to compared trades, where the [[settlement]] 
date is greater than the current business date.  
o Novated – Applicable only to Sponsored GC Transactions. Assigned to matched 
trades, where the start leg of the Sponsored GC trade h as settled.  
o [[Broker]] Balanced – Identifies unbalanced “sets” of [[Broker]] submitted trades, with 
multiple contra -parties, some of which are executed versus non -eligible members. 
o Pending Comparison – Assigned to unmatched trades, where no offsetting match 
exist. These trades can be unilaterally canceled  by the Submitting [[Member]]. 
o Pending Price Conversion – Assigned to When Issue d (WI) trades. 
o Canceled – Assigned to trades that were successfully canceled by the system.  
o Pending Cancel – Applied to the submitter side of the cancellation for a previously 
matched trade.  
o Cancel Request – Assigned to a compared trade when the contra -party has 
submitted a cancellation request.  
o DK Received – Assigned to the [[Broker]] side of the trade for which a DK action has 
been processed against . From this trade state, the trade can be modified . 
• Or you can select Advisory and / or DK Initiated to include all trades that have been 
submitted against you, where no offsetting matching trade has been submitted by you.  
o Advisory – Assigned to Advisories submitted against the [[Member]] .  
Note:  
If Advisory is selected,  no other  selections  will be permitted, except for DK Initiated . 
o DK Initiated – Applied to the su bmitter side of the DK action processed on the [[Broker]] 
Submitted trade(s). From this trade state, the Undo DK action can be performed.  
Contra [[ID]] You can either enter the 4- digit [[GSD]] [[Member]] [[ID]] associated with the contra -party or select 
the contra -party’s [[Member]] [[ID]] and Name from the dropdown list, which lists all available 
[[GSD]] Members. 
Comparison Date Range  Enter the date range to be search ed. For the “From” date, select the earliest date for the 
desired period. Then for the “To” date, select the latest date for the desired period.  

---

## Page 87

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 87 
Field/Item Name  Instructions/Descriptions 
Netting Eligible  Specify whether the trade(s) will be or has/have been subject to the net. Select Yes or No.  
• Yes – Indicates subject to the net.  
• No – Indicates not subject to the net.  
Repo / Revr If Repo and / or Reverse is selected for the Transaction Type, all Repo / Reverse fields 
will be enabled.  
Repo Start Date Range Enter the date range to be search ed. For the “From” date, select the earliest date for the 
desired period. Then for the “To” date, select the latest date for the desired period.  
Repo Start Money  To search by this criteri on, the following fields/boxes must be completed:  
• Select one of the comparis on operators from the dropdown  list: =, >, <, >=, <=, <>. 
• Specify the amount of the desired trade(s).  
Repo Secondary Xref  Specify the Repo Secondary Reference Number of the desired trade(s).  
Repo Rate (%)  To search by this criteri on, the following fields/boxes must be completed:  
• Select one of the comparison  operators from the dropdown list: =, >, <, >=, <=, <>. 
• Specify the Contract Repo Rate  of the desired trade(s).   
Buy / Sell If Buy and / or Sell is selected for the Transaction Type, al l Buy / Sell fields will be 
enabled. 
Pricing Method Specify a Price Type for the desired trade(s) from the dropdown menu.  
Choose: D = discount, P = price, or Y = yield.  
Price To search by this criteri on, the following fields/boxes must be completed:  
• Select one of the comparison  operators from the dropdown list: =, >, <, >=, <=, <>. 
• Specify the Contract Price  of the desired trade(s).  System accepts up to 10 decimals.  
Yield (%) To search by this criteri on, the following fields/boxes must be completed:  
• Select one of the comparison  operators from the dropdown list: =, >, <, >=, <=, <>. 
• Specify the yield of the desired applicable WI trades. System accepts up to 10 decimals.  
Executing Firm  These fields pertain to Executing Firm details, as applicable. 
Executing Firm Symbol  Enter the 4- or 5-character [[ID]] of the Executing Firm , if applicable . 
Contra Executing Firm  Enter the 4- or 5-character [[ID]] of the Contra Executing Firm , if applicable . 
Icon/Button  Instructions/Description 
 Click to select a singular date or a date range, as applicable.  
* Indicates a required field.  
 Click the down arrow to display a dropdown menu from which you can make a selection.  
 Click to close the selected window.  
Reset Returns the fields on current screen to the original [[default]] values.  
Search Click to search for the data you entered on the search screens for the records that fit the 
entered search criteria.  
Table 19: DVP Advanced Search Screen Field Descriptions  


---

## Page 88

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 88 
DVP Quick Search 
To access the Quick Search function, select the Quick Search tab located in the left [[Margin]] of the screen.  
 
Figure 67: Accessing Quick Search 
 
To use the DVP Quick Search function, select DVP from the Product field on the Quick Search screen. Use the 
Quick Search feature to search for a specific trade by selecting a reference number type and entering its 
corresponding reference number in the available field.  
Note: 
For Broke rs, there is an additional Search Criterion / String  parameter; [[Broker]] Xref, that may be selected and used to 
search for one or more trades with the corresponding reference number . 
 
Figure 68: DVP Quick Search - [[Broker]] View 
 
Figure 69: DVP Quick Search - Dealer View 


---

## Page 89

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 89 
For instructions and field descriptions regarding the DVP Quick Search screen, please refer to the below table.  
Note:  
The fields  described in the table below are organized in the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom  within each section).  
Field/Item Name  Instructions/Descriptions 
Trade Details 
[[Member]] [[ID]] The system will automatically [[default]] to the 4- digit [[GSD]] [[Member]] [[ID]] and Name associated 
with the user’s logon credentials.  
Note:  
The [[Member]] [[ID]] field defaults to the [[GSD]] [[Member]] [[ID]] and Name associated with the user’s 
logon credentials with the exception of users that have multiple [[Member]] IDs associated with 
their logon credentials.  
Product  This is a mandatory field. Select the DVP as the Product for searches pertaining to DVP 
trades. 
Search Criteria / String  This field is used when a user wants to retrieve details for a specific trade or trades within a 
block of trades (via [[Broker]] Xref only).  
• From the dropdown menu, select either TID , Xref or [[Broker]] Xref, if applicable.  
• Then enter the number for the selected reference number . 
Icon/Button  Instructions/Description 
* Indicates a required field.  
 Click the down arrow to display a dropdown menu from which you can make a selection.  
Search Click to search for the data you entered on the search screens for the records that fit the 
entered search criteria.  
Table 20: DVP Quick Search Screen Field Descriptions 
  


---

## Page 90

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 90 
DVP Trade Search Results / Trade Management 
The DVP Trade Search Results screen is a summary of   all trades that fit the search criteria entered on the 
DVP Advanced Search screen or DVP Quick Search screen.  
Trade Search Results 
The search results are displayed in three  sections: 
1. Totals - The total number transactions (Long vs. Short) that fit the submitted search criteria, including their 
totals in par and dollar amounts. 
2. Long Trade Summary - A list of all the Buy/Repo trades that fit the search criteria. 
3. Short Trade Summary - A list of all the Sell/Revr trades that fit the search criteria. 
 
The trade results screen will appear displaying the results of your search as seen below. For active trades, this 
screen will allow you to manage the statuses of your trades. From this screen you will be able to View, Modify, 
Cancel, Affirm, DK or view Potential Matches (as applicable based on trade state selection and submission 
type). For queries where Trade History is selected, the View [[Option]] will be the only available action. 
 
Figure 70: DVP Trade Search Results Screen 
 
  


---

## Page 91

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 91 
Trade Search Results can be exported to Excel. To export the trade search results, click the export (     ) icon 
located at the top right of your screen. An Excel spreadsheet similar to the one shown below will open.  
 
Figure 71: Excel export of DVP Trade Search Results 
 
For instructions and field descriptions regarding the DVP Trade Search Results screen, please refer to the 
below table.  
Note:  
The fields  described in the table below are organized in the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom  within each section).  
Field/Item Name  Instructions/Descriptions 
Totals 
Transaction Type  Indicates the type of transaction: Long or Short . 
Items The total number of all Buy, Sell, Repo, and/ or Revr transactions that fit the submitted 
search criteria. 
Par The total par value of all Buy, Sell, Repo, and/ or Revr transactions that fit the submitted 
search criteria. 
[[settlement]] Amount  The total dollar value of all Buy, Sell, Repo, and/ or Revr transactions that fit the submitted 
search criteria. 
Long Lists the total number of Long trades that fit the submitted search criteria, including their 
totals in par and dollar amounts.  
Short  Lists the total number of Short  trades that fit the submitted search criteria, including their 
totals in par and dollar amounts.  
Long Trades Summary / 
Short Trades Summary  
Listed below are th e [[default]] column headers which are the same for both Long and 
Short Trades Summaries. 
Vertical Ellipsis  Click the ‘Vertical Ellipsis“ next to the trade to display an action dropdown menu from which 
you can make a selection.  
The action dropdown menu allows you to access the selected transaction and perform one 
of the following actions:  
Action * Allows you to: 
View ** View trade details  only.  No other action can be taken from this view screen.  


---

## Page 92

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 92 
Field/Item Name  Instructions/Descriptions 
   * Depending on a record’s Trade State, the list of available Actions available may vary.  
 **  Action Screen Descriptions – This section of the document will only cover the View, 
Modify and Cancel actions as Affirm, DK  and Potential Matches are covered in the DVP 
Advisories section). 
Modify  ** Modify  the following  fields: 
• For Uncompared (PCP) trades – all fields can be modified, except for 
the [[Member]] [[ID]] (Submitting [[Member]]) and the Transaction Type.  
• For Compared (CMP) trades – only the reference numbers (Xref, [[Broker]] 
Xref and Secondary Xref ) can be modified.  
Affirm ** Affirm advisory trades and  modify  the Xref, [[Broker]] Xref, and Secondary  
Xref fields only.  
DK ** Select a DK Reason and DK advisory trades .  
Cancel  ** Cancel  the trade only.  No fields can  be modified.  
Potential 
Matches ** 
If the selected  transaction is  an: 
• Advisory  – view potential matching  Uncompared  trades. 
• Uncompared Trades  – view potential matching  Advisories.  
TID (Transaction [[ID]])  [[GSD]] assigned Transaction Reference Number to identify a specific trade.  
Transaction Type  Indicates the type of transaction: Buy, Sell, Repo or Revr.  
[[CUSIP]] The 9-character alphanumeric security identifier associated with the selected trade.  
[[Member]] [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]] associated with the user’s logon credentials . 
Contra [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]] associated with the contra -party. 
Trade Date The date the trade was executed.  
Start Date The date the Start Leg of the Repo/Revr Transaction is scheduled to contractually settle (as 
submitted by the [[Member]] or assigned by [[GSD]]).  
[[settlement]] Date The date the  trade or End Leg of the Repo/Revr Transaction is scheduled to contractually 
settle (as submitted by the [[Member]] or assigned by [[GSD]]).  
Price / Rate The Contract Market Price (for Buy/Sell ) or Rate (for R epo/Revr ) of the [[CUSIP]] on the trade. 
Par The par value of the selected trade. 
[[settlement]] Amount The contract value of the transaction  on its scheduled [[settlement]] Date. For a Repo 
Transaction , this would be Final Money as of the End Leg [[settlement]] Date.  
Trade State Reflects the latest status of a trade. It can be any of the following:  
• CMP - Compared  • PPC - Pending Price Conversion  
• CPA - Compared Pending Auction • CAN - Canceled  
• CPN - Compared Pending [[Novation]]  • PCN - Pending Cancel  
• CPS - Compared Pending [[settlement]]  • CNR - Cancel Request  
• NVT - Novated  • DKR - DK Received  
• BKB - [[Broker]] Balanced  • DKI - DK Initiated  

---

## Page 93

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 93 
Field/Item Name  Instructions/Descriptions 
• PCP - Pending Comparison  • ADV - Advisory  
 
Submission Type  Indicates whether the trade was submi tted for Bilateral Comparison, Demand Comparison, 
or Locked -In Comparison. BL = Bilateral, DM = Demand, LI = Locked -In 
PC (Phased Comparison)  If “Y” appears in this column, it indicates that the trade has undergone Phased Comparison.  
Otherwise this column will be left blank.  
SDS [[settlement]] Status Indicates the [[settlement]] status of  same-day settling [[securities]] [[settlement]] obl igations 
generated on the current business date.  
[[Broker]] Xref The [[Broker]] Xref associated with the trade. This field applies to [[Broker]] submissions only.  
Column Header Selector The columns listed below are not displayed by [[default]].  
Submission Date The date the trade was submitted to [[GSD]].  
Submission Timestamp  The time the trade was submitted to [[GSD]].  
Executing Firm Symbol The 4- or 5-character [[ID]] of the Executing Firm , as applicable. 
Trade Time The time when the trade was executed . 
Security Description  The full name of the selected Security.  
[[Prime Broker]]  Indicates whether the trade is a [[Prime Broker]] trade. “Y”  indicate s that the trade is a Prime 
[[Broker]] trade and “N” indicate s the trade is not a [[Prime Broker]] trade. 
Net Indicates whether the trade is subject to the net . “Y” indicates that the trade is subject to the 
net and “N” indicates the trade is not subject to the net . 
Start Amount  The contract value of the transaction  on its scheduled Start Leg [[settlement]] Date. This field 
applies to Repo Transactions only.  
Total Repo Interest  Reserved for Future Use.  
Contra Executing Firm  The 4- or 5-character [[ID]] of the Contra  Executing Firm , as applicable. 
XREF The external reference number provided by the [[Member]]  on submission of the trade.  
Business Date The current business date for the system . 
Comparison Date  The date the trade was compared in the system.  
Comparison Timestamp The time the trade was compared in the system.  
Icon/Button  Instructions/Description 
  Click to open a popup window that allows you to select which columns you want to view for 
your search results.  
 Click the down arrow to display a menu from which you can make a selection.  
 Click to export the data on the page to an Excel spreadsheet.  
 Click to filter a column by a specific data point or a set of data points.  
 Click to refresh the screen when search criteria or values in the filtered fields change.  
 Click to display an action drop -down menu from which you can make a selection.  
Table 21: DVP Trade Search Results Screen Field Descriptions 


---

## Page 94

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 94 
Trade Management > View  
To view a trade from the DVP Trade Search Results Screen (or the DVP Advisory Management screen), select 
the vertical ellipsis       icon located to the left of the trade. Then select View from the Action Dropdown Menu.  
 
Figure 72: DVP Trade Search Results  > View 
 
Upon selecting the View action, the trade details will appear on the screen.  
See below for an example of the viewable fields for a DVP Buy/Sell transaction. 
 
Figure 73: DVP Trade Search Results - View Trade (Buy/Sell) Details 


---

## Page 95

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 95 
See below for an example of the viewable fields for a DVP Repo/Revr Transaction. 
 
Figure 74: DVP Trade Search Results - View Trade (Repo/Revr) Details 
 
No further action can be taken from the View Trade Details screen. You can close the View Trade Details 
screen by clicking     .    
For instructions and field descriptions regarding the DVP Trade Search Results – View Trade Details screen, 
please refer to the below table.  
Note:  
The fields  desc ribed in the table below are organized in the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom  within each section).  These fields are also applicable to all Trade Action screens.  
Field/Item Name  Instructions/Descriptions 
TID (Transaction [[ID]])  The [[GSD]] assigned Transaction Reference Number to identify a specific trade.  
Product  The Product of the trade that is being viewed . 
Status Reflects the latest status of a trade. It can be any of the following:  
• CMP - Compared  • PPC - Pending Price Conversion  
• CPA - Compared Pending Auction • CAN - Canceled  
• CPN - Compared Pending [[Novation]]  • PCN - Pending Cancel  
• CPS - Compared Pending [[settlement]]  • CNR - Cancel Request  
• NVT - Novated  • DKR - DK Received  
• BKB - [[Broker]] Balanced  • DKI - DK Initiated  
• PCP - Pending Comparison  • ADV - Advisory  
 


---

## Page 96

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 96 
Field/Item Name  Instructions/Descriptions 
Trade Details 
[[Member]] [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]] associated with the user’s logon credentials . 
[[CUSIP]] The 9-character alphanumeric security identifier associated with the selected trade.  
Trade Date The date the trade was executed.  
Trade Time The time when the trade was executed.  
Start Date The date the trade is scheduled to contractually settle (as submitted by the [[Member]] or 
assigned by [[GSD]]).  This field is only applica ble to Repo/Revr Transactions.  
[[settlement]] Date The date the  trade is scheduled to contractually settle (as submitted by the [[Member]] or 
assigned by [[GSD]]).  
Pricing Method The Price Type for the selected trade. This field is only applicable to Buy/Sell Transactions.  
D = discount, P = price, or Y = yield.  
Repo Term Trade term in number of days.  This field is only applicable to Repo/Revr Transactions.  
Executing Firm Symbol  The 4- or 5-character [[ID]] of the Executing Firm , as applicable.  
[[Broker]] Xref The [[Broker]] Xref associated with the trade.  This field is only applicable for [[Broker]] 
submissions.  
Trader [[ID]] The unique identifier of the Trader  on the trade. 
Netting Eligible  Specifies whether the trade(s) will be or has/have been subject to the net. “Y” indicates the 
trade is subject to the net  and “N” indicates the trade is not subject to the net.  
[[Prime Broker]]  Indicates whether the trade is a [[Prime Broker]] trade. “Y” indicates that the trade is a Prime 
[[Broker]] trade and “N” indicates the trade is not a [[Prime Broker]] trade.  
Transaction Type  Indicates the type of transaction: Buy, Sell, Repo or Revr.  
Repo / Reverse 
Transaction Details  
These fields describe the economic details of a Repo /Reverse Transaction  as the 
fields are the same for both Transaction types. 
Par The par value of the selected trade.  
Start Money  The contract value of the transaction  on its scheduled Start Leg [[settlement]] Date.  
Final Money  The contract value of the transaction on its scheduled End Leg [[settlement]] Date. 
Repo Rate (%)  Specifies the Contract Repo Rate for the Repo or Revr.  
Accrued To Date Specifies the Accrued Interest. The amount is calculated by the system.  
Contra [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]] associated with the contra -party. 
Contra Exec. Firm  The 4- or 5-character [[ID]] of the Contra Executing Firm , as applicable. 
Trade Xref The external reference number for the trade.  
Secondary Xref  The secondary reference number for the trade.  

---

## Page 97

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 97 
Field/Item Name  Instructions/Descriptions 
Buy / Sell Transaction 
Details  
These fields describe the economic details of a Buy/Sell Transaction as the fields are 
the same for both Transaction types. 
Par The par value of the selected trade.  
Price Specifies the Contract Price for the Buy or Sell.  
[[settlement]] Amount  The contract value of the transaction on its scheduled [[settlement]] date. 
Commission  The Commission on the trade, as applicable.  
Contra [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]] associated with the contra -party. 
Contra Exec. Firm  The 4- or 5-character [[ID]] of the Contra Executing Firm , as applicable. 
Trade Xref The external reference number for the trade.  
Trade History 
Date The date the memo of the selected trade was created . 
Time The time when the memo of the selected trade was created . 
Cmd (Command)  The system command that created the memo.  
Memo The memo description of the selected trade.  
Contra TID The [[GSD]] assigned Transaction Reference Number associated wi th the contra -party’s trade, 
if applicable . 
Contra Xref The external reference number associated with the contra -party’s trade, if applicable. 
User The user whose action generated the memo: either a [[Member]] [[ID]] or if it is System 
generated, then the appropr iate 4 -character system action is displayed in this field . 
Icon/Button  Instructions/Description (View, Modify, Cancel, Affirm , DK  and Potential Matches) 
 
 or 
The Additional Data screen contains an audit trail of the selected trade’s processing history. 
Click the plus sign to view the processing history for the trade. Click the minus sign to hide 
the processing history . 
 Click to affirm an advisory trade submitted against you.  
 Click to submit the trade data you modified.  
 Click to cancel an entry or action.  
 Click to select a singular date or a date range, as applicable.  
 Click to DK an advisory trade submitted against you.  
 Hover over to see additional information.  
 Click the down arrow to display a dropdown menu from which you can make a selection.  
 Click to close the selected window.  
 Indicates an entry has been validated/accepted.  
Table 22: DVP Trade Search Results – View Trade Details Screen Field Descriptions 


---

## Page 98

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 98 
Trade Management > Modify 
You can modify a Buy/Sell transaction if such transaction is active and is in one of the following Trade States: 
PCP, CMP, CNR, CPA, CPN, CPS, or PCN. 
• For Uncompared trades, you can modify all fields except for the [[Member]] [[ID]], Transaction Type and any 
field calculated or derived by the system, i.e., Netting Eligible flag and [[Prime Broker]] flag. 
• For Compared trades (including trades in a PCN or CNR Trade State), only the Trade Xref and [[Broker]] 
Xref can be modified. 
 
You can modify a Repo/Revr Transaction if such transaction is active and is in one of the following Trade 
States: PCP, CMP, CNR, CPA, CPN, CPS, or PCN. 
• For Uncompared trades, you can modify all fields except for the [[Member]] [[ID]], Transaction Type and any 
field calculated or derived by the system, i.e., Repo Term, Accrued Interest to Date, Netting Eligible flag 
and [[Prime Broker]] flag. 
• For Compared trades (including trades in a PCN or CNR Trade State), only the Trade Xref, Secondary 
Xref and [[Broker]] Xref, as applicable, can be modified. 
 
To modify a trade from the DVP Trade Search Results Screen (or the DVP Advisory Management screen), 
select the vertical ellipsis       icon located to the left of the trade. Then select Modify from the Action Dropdown 
Menu.  
 
Figure 75: DVP Trade Search Results > Modify 
  


---

## Page 99

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 99 
Upon selecting the Modify action, the trade details will appear on the screen. You can modify the trade and 
click the “Apply Changes” button once done.  
See below for an example of the modifiable fields for an uncompared DVP Buy/Sell transaction. 
 
Figure 76: Modifiable fields on an uncompared DVP Buy/Sell Transaction 
 
See below for an example of the modifiable fields for an uncompared DVP Repo/Revr Transaction. 
 
Figure 77: Modifiable fields on an uncompared DVP Repo/Revr Transaction 


---

## Page 100

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 100 
For instructions and field descriptions regarding the modifiable fields highlighted in the above examples, refer 
to the DVP Trade Search Results – View Trade Details Screen Field Descriptions table.  
Once the Apply Changes button is selected, the below confirmation window will appear. Select Yes to confirm 
your changes. Select No to return back to the Modify screen and make additional changes as applicable. 
 
Figure 78: Modify Trade Confirmation Window 
 
Once Yes is selected, the confirmation window will close. The modification has been accepted by the system. 
The Modify screen will update with a success message as seen below. You can close the Modify screen by 
clicking     . 
 
Figure 79: Trade Modification Accepted Successfully Message 
 
  


---

## Page 101

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 101 
Trade Management > Cancel 
You can submit a cancel action on a Buy/Sell transaction where you are the submitter of such transaction and 
if such transaction is active. 
• For Uncompared trades, you can unilaterally cancel the trade. 
• For Compared trades (excluding trades in a CNR Trade State), it requires both parties to the trade to 
submit cancel actions for the trade to be fully cancelled. A trade in the CNR Trade State has already been 
cancelled by the contra-party and is awaiting your cancel action. 
 
You can submit a cancel action on a Repo/Revr Transaction where you are the submitter of such transaction 
and if such transaction is active.  
• For Uncompared trades, you can unilaterally cancel the trade. 
• For Compared trades (excluding trades in a CNR Trade State), it requires both parties to the trade to 
submit cancel actions for the trade to be fully cancelled. A trade in the CNR Trade State has already been 
cancelled by the contra-party and is awaiting your cancel action. 
 
To cancel a trade from the DVP Trade Search Results Screen (or the DVP Advisory Management screen), 
select the vertical ellipsis       icon located to the left of the trade. Then select Cancel from the Action Dropdown 
Menu.  
 
Figure 80: DVP Trade Search Results > Cancel 
  


---

## Page 102

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 102 
Upon selecting the Cancel action, the trade details will appear on the screen. From this screen, you can cancel 
the trade by clicking the “Cancel” button.  
See below for an example of the Cancel screen prior to the submission of the cancel action. 
 
Figure 81: Cancel screen prior to submission of Cancel action 
 
For instructions and field descriptions regarding the Cancel screen, refer to the DVP Trade Search Results – 
View Trade Details Screen Field Descriptions table.  
Once the Cancel button is selected, the below confirmation window will appear. Select Yes to confirm your 
cancel. Select No to return back to the Cancel screen. 
 
Figure 82: Cancel Trade Confirmation Window 
 
 
 


---

## Page 103

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 103 
Once Yes is selected, the confirmation window will close. The cancellation has been accepted by the system. 
The Cancel screen will update with a success message as seen below. You can close the Cancel screen by 
clicking     . 
 
Figure 83: Trade Cancellation Accepted Successfully Message 
  


---

## Page 104

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 104 
GCF / CCIT Trade Search & Management 
The GCF/CCIT Trade Search functionality in [[GSD]] RTTM Web allows users to query both active trades and 
trades in [[GSD]]’s historical database. The trade search function also provides users with the ability to search for 
a specific trade or multiple trades that fit within specified parameters.  
GCF / CCIT Advanced Search 
Upon selecting the Trades > Search & Management menu [[Option]], the Advanced Search screen will appear. 
This screen appears by [[default]]. From this screen, the user can select the GCF/CCIT Product and search for a 
single GCF Repo/CCIT trade or multiple GCF Repo/CCIT trades using various parameters and criteria. The 
available search parameters are slightly different depending on the type of [[Member]] account associated with 
the user’s logon credentials.  
GCF / CCIT Advanced Search  – [[Broker]] View 
Below is a full screen view of the GCF/CCIT search parameters available to Brokers. Brokers have an 
additional Search Criterion / String; [[Broker]] Xref. Brokers also have a Repo [[ID]] and Revr [[ID]] as search 
parameters instead of a Contra [[ID]] field.  
As a [[Broker]], populate the required fields marked with a red asterisk ( * ). The remaining fields are optional, and 
allow you to refine your search parameters further. To broaden your search, enter less criteria. Once the 
search criteria has been entered, click the Search button to view the trade search results. 
 
Figure 84: GCF/CCIT Advanced Search Screen - [[Broker]] View 


---

## Page 105

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 105 
GCF / CCIT Advanced Search – GCF Dealer / CCIT [[Member]] View 
Below is a full screen view of the GCF/CCIT search parameters available to GCF Dealers and CCIT Members. 
GCF Dealers and CCIT Members [[DO]] not have the [[Option]] to search by the Search Criterion / String; [[Broker]] 
Xref. Also, GCF Dealers and CCIT Members have a Contra [[ID]] field as a search parameter instead of the Repo 
[[ID]] and Revr [[ID]] fields.  
As a GCF Dealer or CCIT [[Member]], populate the required fields marked with a red asterisk ( * ). The remaining 
fields are optional, and allow you to refine your search parameters further. To broaden your search, enter less 
criteria. Once the search criteria has been entered, click the Search button to view the trade search results. 
 
Figure 85: GCF / CCIT Advanced Search Screen - GCF Dealer / CCIT [[Member]] View 
 
  


---

## Page 106

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 106 
For instructions and field descriptions regarding the GCF/CCIT Advanced Search screen, please refer to the 
below table.  
Note:  
The fields  described in the table below are organized in the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom  within each section).  
Field/Item Name  Instructions/Descriptions 
Trade Details 
[[Member]] [[ID]] The system will automatically [[default]] to the 4- digit [[GSD]] [[Member]] [[ID]] and Name associated 
with the user’s logon credentials.  
Note:  
The [[Member]] [[ID]] field defaults to the [[GSD]] [[Member]] [[ID]] and Name associated with the user’s 
logon credentials with the exception of users that have multiple [[Member]] IDs associated with 
their logon credentials.  
TID / Xref / [[Broker]] Xref This field is used when a user wants to retrieve details for a specific trade or trades within a 
block of trades (via [[Broker]] Xref only).  
• From the dropdown menu, select either TID , Xref or [[Broker]] Xref, if applicable.  
• Then enter the number for the selected reference number . 
Business Date Range This is a mandatory field. Enter the date range to be searched. For the “From” date, select 
the earliest date for the desired period. Then for the “To” date, select the latest date for the 
desired period.  
Product  This is a mandatory field. Select GCF/CCIT as the Product for searches pertaining to GCF 
Repo Transactions or CCIT Transactions . 
[[CUSIP]] Select the GCF Repo Generic [[CUSIP]] Number  or leave this field blank . This field contains a 
dropdown list of the GCF Repo Generic [[CUSIP]] Numbers:  371487AD1, 371487AE9, 
371487AH2, 371487AL3, 371487AQ2, 371487AM1, 371487AR0, 371487AG4 and 
371487AF6. 
[[settlement]] Date Range Enter the date range to be search ed. For the “From” date, select the earliest date for the 
desired period. Then for the “To” date, select the latest date for the desired period.  
Trade Active or Trade 
History  
This is a mandatory field. Specify whether the trade sear ch is for active or historical trades.  
Start Money  To search by this criterion, the following fields/boxes must be completed:  
• Select one of the comparison operators from the dropdown  list: =, >, <, >=, <=, <>. 
• Specify the amount of the desired trade(s).  
Trade Date Range Enter the date range to be search ed. For the “From” date, select the earliest date for the 
desired period. Then for the “To” date, select the latest date for the desired period.  
Transaction Type  This is a mandatory field. Select  the Repo and/or  Revr checkbox( es).  

---

## Page 107

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 107 
Field/Item Name  Instructions/Descriptions 
Final Money   To search by this criteri on, the following fields/boxes must be completed:  
• Select one of the comparison operators from the dropdown list: =, >, <, >=, <=, <>. 
• Specify the amount of the desired trade(s).  
Submission Date Range Enter the date range to be search ed. For the “From” date, select the earliest date for the 
desired period. Then for the “To” date, select the latest date for the desired period.  
Trade State / Advisories  The Trade State field offers two search options:  
• You can limit your search results by selecting one or more of the following Trade State(s):  
o Affirmed – Assigned to the current business date’s  brokered trades for which the 
affirm action has been taken by the [[Member]] (dealer) indicated. Affirmed  trades 
cannot be unilaterally canceled; both sides must submit a cancellation request.  
o Pending Affirm – Assigned to the current business date’s brokered trades for which 
the affirm action has not yet been taken by the [[Member]]  (dealer) indicated.  
o Pending Comparison – Assigned to current business date’s unmatched bilateral 
trades, where there is no offsetting match against the trade. Trades in this state can 
be unilaterally canceled  by the Submitting [[Member]]. 
o Compared – Assigned to bilateral trades compared  on the current business date, 
where a trade is matched through an offsetting bilateral trade submission. Compared 
trades cannot be unilaterally canceled; both sides must submit a cancellation 
request. 
o Canceled – Assigned to trades that were successfully canceled by the system.  
o Pending Cancel – Applied to the submitter side of the cancellation for a previously 
matched trade.  
o Cancel Request – Assigned to a compared trade when the contra -party has 
submitted a cancellation request.  
• Or you can select Advisory to include all bilateral trades that have been submitted against 
you, where no offsetting matching trade has been submitted by you.  
o Advisory – Assigned to Advisories submitted against the [[Member]] .  
Note:  
If Advisory is selected,  no other  selections  will be permitted. 
Repo  [[ID]] / Contra [[ID]]  You can either enter the 4- digit [[GSD]] [[Member]] [[ID]] associated with the  contra -party or select 
the contra -party’s [[Member]] [[ID]] and Name from the dropdown list, which lists all available 
[[GSD]] Members. The Repo [[ID]] field is appli cable for the [[Broker]] View. The Contra [[ID]] field is 
applicable for the GCF  Dealer /CCIT [[Member]] view.  
Comparison Date Range  Enter the date range to be search ed. For the “From” date, select the earliest date for the 
desired period. Then for the “To” date, select the latest date for the desired period.  
Repo Secondary Xref  Specify the Repo Secondary Reference Number of the desired trade(s).  
Repo Rate (%)  To search by this criterion, the following fields/boxes must be completed:  
• Select one of the comparison operators from the dropdown list: =, >, <, >=, <=, <>.  
• Specify the Contract Repo Rate of the desired trade(s).   
Repo Start Date Range Enter the date range to be search ed. For the “From” date, select the earliest date for the 
desired period. Then for the “To” date, select the latest date for the desired period.  

---

## Page 108

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 108 
Field/Item Name  Instructions/Descriptions 
Revr [[ID]] You can either enter the 4- digit [[GSD]] [[Member]] [[ID]] associated with the contra -party or select 
the contra -party’s [[Member]] [[ID]] and Name from the dropdown list, which lists all available 
[[GSD]] Members. This field is applicable for the [[Broker]] View. 
Icon/Button  Instructions/Description 
 Click to select a singular date or a date range, as applicable.  
* Indicates a required field.  
 Click the down arrow to display a dropdown menu from which you can make a selection.  
 Click to close the selected window.  
Reset Returns the fields on current screen to the original [[default]] values.  
Search Click to search for the data you entered on the search screens for the records that fit the 
entered search criteria.  
Table 23: GCF/CCIT Advanced Search Screen Field Descriptions 
 
  


---

## Page 109

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 109 
GCF / CCIT Quick Search 
To access the Quick Search function, select the Quick Search tab located in the left [[Margin]] of the screen.  
 
Figure 86: Accessing Quick Search 
 
To use the GCF / CCIT Quick Search function, select GCF / CCIT from the Product field on the Quick Search 
screen. Use the Quick Search feature to search for a specific trade by selecting a reference number type and 
entering its corresponding reference number in the available field.  
Note: 
For Brokers, there is an addi tional Search Criterion / String [[Option]];  [[Broker]] Xref, that may be selected and used to search for 
one or more trades with the corresponding reference number.  
 
Figure 87: GCF / CCIT Quick Search - [[Broker]] View 


---

## Page 110

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 110 
 
 
Figure 88: GCF / CCIT Quick Search - GCF Dealer / CCIT [[Member]] View 
For instructions and field descriptions regarding the GCF / CCIT Quick Search screen, please refer to the 
below table.  
Note:  
The fields  described in the table below are organized in  the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom  within each section).  
Field/Item Name  Instructions/Descriptions 
Trade Details 
[[Member]] [[ID]] The system will automatically [[default]] to the 4- digit [[GSD]] [[Member]] [[ID]] and Name associated 
with the user’s logon credentials.  
Note:  
The [[Member]] [[ID]] field defaults to the [[GSD]] [[Member]] [[ID]] and Name associated with the user’s 
logon credentials with the exception of u sers that have multiple [[Member]] IDs associated with 
their logon credentials.  
Product  This is a mandatory field. Select the GCF / CCIT as the Product for searches pertaining to 
GCF Repo Transactions or CCIT Transactions.  
Search Criteria / String  This field is used when a user wants to retrieve details for a specific trade or trades within a 
block of trades (via [[Broker]] Xref only).  
• From the dropdown menu, select either TID , Xref or [[Broker]] Xref, if applicable.  
• Then enter the number for the selected reference number . 
Icon/Button  Instructions/Description 
* Indicates a required field.  
 Click the down arrow to display a dropdown menu from which you can make a selection.  
Search Click to search for the data you entered on the search screens for the records that fit the 
entered search criteria.  
Table 24: GCF / CCIT Quick Search Screen Field Descriptions  


---

## Page 111

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 111 
GCF / CCIT Trade Search Results / Trade Management 
The GCF / CCIT Trade Search Results screen is a summary of all trades that fit the search criteria entered on 
the GCF / CCIT Advanced Search screen or GCF / CCIT Quick Search screen. 
Trade Search Results  
The search results are displayed in two  sections: 
1. Totals - The total number transactions (Repo vs. Revr) that fit the submitted search criteria, including their 
totals in item count, start money and final money dollar amounts. 
2. Trade Summary - A list of all the Repo/Revr trades that fit the search criteria. 
 
The trade results screen will appear displaying the results of your search as seen below. For active trades, this 
screen will allow you to manage the statuses of your trades. From this screen you will be able to View, Modify, 
Cancel, Affirm or view Potential Matches (as applicable based on trade state selection). For queries where 
Trade History is selected, the View [[Option]] will be the only available action. 
Below is an example of the GCF/CCIT Trade Search Results screen for Brokers. 
 
Figure 89: GCF / CCIT Trade Search Results Screen ([[Broker]] View) 
 
Trade Search Results can be exported to Excel. To export the trade search results, click the export (     ) icon 
located at the top right of your screen. An Excel spreadsheet similar to the one shown below will open.  
 
Figure 90: Excel export of GCF / CCIT Trade Search Results ([[Broker]] View) 
  


---

## Page 112

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 112 
Below is an example of the GCF/CCIT Trade Search Results screen for GCF Dealers and CCIT Members. 
 
Figure 91: GCF / CCIT Trade Search Results Screen (GCF Dealer / CCIT [[Member]] View) 
 
Trade Search Results can be exported to Excel. To export the trade search results, click the export (     ) icon 
located at the top right of your screen. An Excel spreadsheet similar to the one shown below will open.  
 
Figure 92: Excel export of GCF / CCIT Trade Search Results (GCF Dealer / CCIT [[Member]] View) 
 
  


---

## Page 113

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 113 
For instructions and field descriptions regarding the GCF / CCIT Trade Search Results screen, please refer to 
the below table.  
Note:  
The fields  described in the table below are organized in the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom  within each section).  
Field/Item Name  Instructions/Descriptions 
Totals 
Transaction Type  Indicates the type of transaction: Repo  or Revr. 
Items The total number of all Repo and/ or Revr Transactions that fit the submitted search criteria. 
Start Money  The total dollar  value of the Start Leg on all Repo and/ or Revr Transactions that fit the 
submitted search criteria. 
Final Money  The total dollar value of the End Leg on all Repo and/ or Revr Transactions that fit the 
submitted search criteria. 
Repo  Lists the total number of Repo Transactions  that fit the submitted search criteria, including 
their totals in Start Money and Final Money . 
Revr Lists the total number of Reverse Repo Transactions  that fit the submitted search criteria, 
including their totals in Start Money and Final Money . 
Trades Summary Listed below are the [[default]] column headers which are the same for both Repo and 
Revr Transactions. 
Vertical Ellipsis  Click the ‘Vertical Ellipsis“ next to the trade to display an action dropdown menu from which 
you can make a selection.  
The action dropdown menu allows you to access the selected transaction and perform one 
of the following actions:  
   * Depending on a record’s Trade State, the list of available Actions available may vary.  
 **  Action Screen Descriptions – This section of the document will only cover the View, 
Modify and Cancel actions as Affirm is covered in the GCF/CCIT Advisories section). 
Action * Allows you to: 
View ** View trade details  only.  No other action can be taken from this view screen.  
Modify  ** Modify  the following  fields: 
• For Uncompared (PCP) trades – all fields can be modified, except for 
the [[Member]] [[ID]] (Submitting [[Member]]), Contra [[ID]], Transaction Type and 
any field  calculated or derived by the system.  
• For Compared (CMP) trades – only the reference numbers ( Trade Xref, 
[[Broker]] Xref and Secondary Xref ) can be modified.  
• For Brokered trades – only the Contra [[ID]] and reference numbers (Trade 
Xref, [[Broker]] Xref and Secondary Xref)  can be modified.  
Affirm ** Affirm advisory trades and pending affirm trades and  modify  the Xref and  
Secondary Xref  fields only.  
Cancel  ** Cancel  the trade only.  No fields can  be modified.  


---

## Page 114

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 114 
Field/Item Name  Instructions/Descriptions 
[[Broker]] TID / TID 
(Transaction [[ID]])  
The [[GSD]] assigned Transaction Reference Number to identify a specific trade.  
[[Broker]] Xref / Xref  The external reference number provided by the [[Member]]  on submission of the trade.  
[[CUSIP]] The 9-character alphanumeric security identifier associated with the selected trade.  
[[Broker]] / [[Member]] [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]] associated with the user’s logon credentials . 
Dealer [[ID]] / Contra [[ID]]  The 4-digit [[GSD]] [[Member]] [[ID]] associated with the contra -party. 
Transaction Type  Indicates the type of transaction: Repo or Revr.  
Start Date The date the Start Leg of the Repo/Revr Transaction is scheduled to contractually settle (as 
submitted by the [[Member]] or assigned by [[GSD]]).  
End Date The date the  End Leg of the Repo/Revr Transaction is scheduled to contractually settle (as 
submitted by the [[Member]] or assigned by [[GSD]]).  
Start Money  The contract value of the transaction  on its scheduled Start Leg [[settlement]] Date.  
Final Money  The contract value of the transaction  on its scheduled End Leg [[settlement]] Date. 
Repo Rate (%) The Contract Repo Rate for the Repo or Revr  Transaction . 
Other Reference The secondary reference number for the trade.  Field not applicable for  [[Broker]] View. 
Free of Payment Amount  Reserved for Future Use.  
Trade State Reflects the latest status of a trade. It can be any of the following:  
• CMP - Compared  • CAN - Canceled  
• CNR - Cancel Request  • PCN - Pending Cancel  
• PAF – Pending Affirm  • AFF - Affirmed  
• PCP - Pending Comparison  • ADV - Advisory  
 
Business Date The current business date for the system . 
Icon/Button  Instructions/Description 
  Click to open a popup window that allows you to select which columns you want to view for 
your search results.  
 Click the down arrow to display a menu from which you can make a selection.  
 Click to export the data on the page to an Excel spreadsheet.  
 Click to filter a column by a specific data point or a set of data points.  
 Click to refresh the screen when search criteria or values in the filtered fields change.  
 Click to display an action drop- down menu from which you can make a selection.  
Table 25: GCF / CCIT Trade Search Results Screen Field Descriptions 
 
  


---

## Page 115

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 115 
Trade Management > View  
To view the trade details of an advisory from the GCF / CCIT Trade Search screen, select the vertical elipsis 
icon located to the left of the trade. Then select View from the Action Dropdown Menu.  
 
Figure 93: GCF / CCIT Trade Search Results > View ([[Broker]] View - GCF Repo Transaction) 
 
Upon selecting the View [[Option]], the trade details will appear on the screen. See below for an example of the 
viewable fields for a GCF Repo Transaction.  
 
Figure 94: GCF / CCIT Trade Search Results – View Trade (GCF Repo Transaction) Details  


---

## Page 116

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 116 
No further action can be taken from the View Trade Details screen. You can close the View Trade Details 
screen by clicking     .    
Note:  
The CCIT Transaction fields displayed on the View Trade Details screen are simi lar, therefore only a GCF Repo transaction 
example is shown.  
For instructions and field descriptions regarding the GCF / CCIT Trade Search Results – View Trade Details 
screen, please refer to the below table. 
Note:  
The fields  described in the table below are organized in the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom  within each section).  
Field/Item Name  Instructions/Descriptions 
[[Broker]] TID / TID 
(Transaction [[ID]])  
The [[GSD]] assigned  Transaction Reference Number to identify a specific trade.  
Product  The Product of the trade that is being viewed . 
  Trade Details 
[[Member]] [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]] associated with the user’s logon credentials . 
[[CUSIP]] The 9-character GCF Repo Generic [[CUSIP]] Number  associated with the selected trade.   
Trade Date The date the trade was executed.  
[[Broker]] Xref The [[Broker]] Xref associated with the trade. This field is only applicable for [[Broker]] 
submissions.  
Start Date The date the trade is scheduled to contractually settle (as submitted by the [[Member]] or 
assigned by [[GSD]]).  This field is only applicable to Repo/Revr Transactions.  
End Date The date the  trade is scheduled to contractually settle (as submitted by the [[Member]] or 
assigned by [[GSD]]).  
Repo Term Trade term in number of days. This field is only applicable to Repo/Revr Transactions.  
Repo / Reverse 
Transaction Details  
These fields describe the economic details of a Repo/Reverse Transaction as the 
fields are the same for both Transaction types. 
Status Reflects the latest status of a trade. It can be any of the following:  
• AFF - Affirmed • PAF - Pending Affirm 
• PCP - Pending Comparison  • CMP - Compared  
• CAN - Canceled  • PCN - Pending Cancel  
• CNR - Cancel Request  • ADV - Advisory  
 
TID (Transaction [[ID]])  The [[GSD]] assigned Transaction Reference Number to identify a specific trade.  This field 
would only appear as part of the Transaction Details, if the [[Member]] [[ID]] is for a [[Broker]]. 
Start Money  The contract value of the transaction  on its scheduled Start Leg [[settlement]] Date.  
Final Money  The contract value of the transaction on its scheduled End Leg [[settlement]] Date. 


---

## Page 117

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 117 
Field/Item Name  Instructions/Descriptions 
Repo Rate (%)  Specifies the Contract Repo Rate for the Repo or Revr.  
Total Repo Interest  Specifies the Total Repo Interest  calculated on the trade.  
Accrued to Date Specifies the Accrued Interest. The amount is calculated by the system.  
Contra [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]] associated with the contra -party. 
Trade Xref The external reference number for the trade.  
Secondary Xref  The secondary reference number for the trade.  
Trade History 
Date The date the memo of the selected trade was created.  
Time The time when the memo of the selected trade was created.  
Cmd (Command)  The system command that created the memo. 
Memo The memo description of the selected trade.  
Contra TID The [[GSD]] assigned Transaction Reference Number associated with the contra- party’s trade, 
if applicable.  
Contra Xref The external reference number associated with the contra -party’s trade, if applicable.  
User The user whose action generated the memo: either a [[Member]] [[ID]] or if it is System 
generated, then the appropr iate 4 -character system action is displayed in this field.  
Icon/Button  Instructions/Description (View, Modify, Cancel, and Affirm screens)  
 
or 
The Additional Data screen contains an audit trail of the selected trade’s processing history. 
Click the plus sign to view the processing history for the trade. Click the minus sign to hide 
the processing history . 
 Click to affirm an advisory trade submitted against you.  
 Click to submit the trade data you modified.  
 Click to cancel an entry or action.  
 Click to select a singular date or a date range, as applicable.  
 Hover over to see additional information.  
 Click the down arrow to display a dropdown menu from which you can make a selection.  
 Click to close the selected window.  
 Indicates an entry has been validated/accepted.  
Table 26: GCF/CCIT Trade Search Results - View Trade Details Screen Field Descriptions 
  


---

## Page 118

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 118 
Trade Management > Modify 
You can modify a GCF Repo/Revr or CCIT Transaction if such transaction is active and is in one of the 
f ollowing Trade States: PCP, CMP, CNR, or PCN. 
• For Uncompared trades (CCIT Transactions and GCF Repo Transactions submitted by a GCF Dealer), 
you can modify all fields except for the [[Member]] [[ID]], Contra [[ID]], Transaction Type and any field calculated 
or derived by the system, i.e., Repo Term, Final Money, Total Repo Interest, and Accrued to Date. 
• For Compared trades (CCIT Transactions that are in CMP, PCN or CNR Trade State), only the Trade Xref 
and Secondary Xref can be modified. 
• For Brokered trades (including tades in a PAF, PCN or AFF Trade State), only the [[Broker]] Xref, Contra [[ID]], 
Trade Xref and Secondary Xref can be modified. 
 
To modify a trade from the DVP Trade Search Results Screen (or the DVP Advisory Management screen), 
select the vertical ellipsis       icon located to the left of the trade. Then select Modify from the Action Dropdown 
Menu.  
 
Figure 95: GCF / CCIT Trade Search Results > Modify 
 
  


---

## Page 119

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 119 
Upon selecting the Modify action, the trade details will appear on the screen. You can modify the trade and 
click the “Apply Changes” button once done.  
See below for an example of the modifiable fields for an uncompared CCIT Transaction. 
 
Figure 96: Modifiable fields on an uncompared CCIT Transaction 
 
See below for an example of the modifiable fields for a Brokered GCF Repo/Revr Transaction in the pending 
affirm trade state. 
 
Figure 97: Modifiable fields on a pending affirm Brokered GCF Repo/Revr Transaction 


---

## Page 120

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 120 
For instructions and field descriptions regarding the modifiable fields highlighted in the above examples, refer 
to the GCF / CCIT Trade Search Results – View Trade Details Screen Field Descriptions table.  
Once the Apply Changes button is selected, the below confirmation window will appear. Select Yes to confirm 
your changes. Select No to return back to the Modify screen and make additional changes as applicable. 
 
Figure 98: Modify Trade Confirmation Window 
 
Once Yes is selected, the confirmation window will close. The modification has been accepted by the system. 
The Modify screen will update with a success message as seen below. You can close the Modify screen by 
clicking     . 
 
Figure 99: Trade Modification Accepted Successfully Message 


---

## Page 121

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 121 
Trade Management > Cancel 
You can submit a cancel action on a Repo/Revr Transaction where you are the submitter of a GCF/CCIT  
Repo/Revr Transaction or if you are a contra-party to Brokered GCF Repo/Revr Transaction and if such 
transaction is active.  
• For Uncompared and pending affirm trades, you can unilaterally cancel the trade if you are the original 
submitter of the trade. 
• For Compared and Affirm trades (excluding trades in a CNR Trade State), it requires both parties to the 
trade to submit cancel actions for the trade to be fully cancelled. A trade in the CNR Trade State has 
already been cancelled by the contra-party and is awaiting your cancel action. 
 
To cancel a trade from the GCF / CCIT Trade Search Results Screen, select the vertical ellipsis       icon 
located to the left of the trade. Then select Cancel from the Action Dropdown Menu.  
 
Figure 100: GCF / CCIT Trade Search Results > Cancel 
 
  


---

## Page 122

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 122 
Upon selecting the Cancel action, the trade details will appear on the screen. From this screen, you can canc el 
the trade by clicking the “Cancel” button.  
See below for an example of the Cancel screen prior to the submission of the cancel action. 
 
Figure 101: Cancel screen prior to submission of Cancel action 
 
For instructions and field descriptions regarding the Cancel screen, refer to the GCF / CCIT Trade Search 
Results – View Trade Details Screen Field Descriptions table.  
Once the Cancel button is selected, the below confirmation window will appear. Select Yes to confirm your 
cancel. Select No to return back to the Cancel screen. 
 
Figure 102: Cancel Trade Confirmation Window 
 
 


---

## Page 123

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 123 
Once Yes is selected, the confirmation window will close. The cancellation has been accepted by the system. 
The Cancel screen will update with a success message as seen below. You can close the Cancel screen by 
clicking     . 
 
Figure 103: Trade Cancellation Accepted Successfully Message 
  


---

## Page 124

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 124 
Trades > Advisory Management  
From the Trades > Search & Management menu selection, users with the appropriate access can query trades 
and manage the status on your active trades. Advisories are trades that were submitted against the viewing 
[[Member]] for which the viewing [[Member]] has not yet submitted their side of the trade.  
DVP Advisories 
The DVP Advisories submitted on the current business date can be accessed by clicking the Advisories quick 
link in the Statistics section of the DVP Dashboard. The Advisories quick link will take you directly to the results 
page where trades submitted against the viewing [[Member]] can be found along with any potential matches. 
 
Figure 104: DVP Advisories Quick Link 
 
To view DVP Advisories vs. Uncompared DVP trades, use the main toolbar located at the top of the page, and 
select Trades > Advisory Management. 
 
Figure 105: Trades > Advisory Management (DVP only) 


---

## Page 125

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 125 
Advisory Management 
Once the Advisory Management menu [[Option]] is selected, the DVP Advisories Management screen will appear. 
The DVP Advisories Management screen offers a split-view where users can see their Advisories and 
Uncompa red DVP trades. 
 
Figure 106: DVP Advisory Management Screen 
 
The DVP Advisories Management screen has three sections: 
1. Totals – Lists the total number of Advisory and Uncompared transactions (Repo, Revr, Buy & Sell), along 
with total par and dollar amounts. 
2. Advisories – This section lists all of the viewing [[Member]]’s Advisories.  
Note:  
Advisories are trades that the contra- party has submitted against the viewing [[Member]] , but the viewing [[Member]] has not yet 
submitted their side of the trade with matching trade details.  
3. Uncompared – This section lists all of the viewing [[Member]]’s Uncompared trades.  
Note:  
Uncompared trades are trades that the viewing [[Member]] has  submitted, but th e contra -party has not yet submitted their side 
of the trade with matching trade details.  
  
1 
2 
 3 

---

## Page 126

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 126 
For additional instructions and field descriptions regarding the DVP Advisories Management screen, please 
refer to the below table. 
Note:  
The fields described in the table below are organized in the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom  within each section).  
Item Description 
Totals 
Items The total number of all Buy, Sell, Repo, or Revr  transactions  in the applicable category.  
Par The total par value of all Buy, Sell, Repo, or Revr  transactions  in the applicable category.  
[[settlement]] Amount  The total dollar value of all Buy, Sell, Repo, or Revr  transactions in the applicable category.  
Advisories Lists the total number of all Advisory transactions (Repo, Revr, Buy & Sell), along with total 
par and dollar value. 
Uncompared Lists the total number of all Uncompared transactions (Repo, Revr, Buy & Sell), along with 
total par and dollar value. 
Advisories Lists the total number of all Advisory transactions (Repo, Revr, Buy & Sell) . 
TID [[GSD]] assigned Transaction Reference Number to identify the  specific trade.  
Transaction Type  Indicates the type of transaction: Buy, Sell, Repo or Revr.  
[[CUSIP]] The 9-character alphanumeric security identifier ([[CUSIP]] number) associated with the 
selected trade.  
[[Member]] [[ID]] The system will automatically [[default]] to the 4- digit [[GSD]] [[Member]] [[ID]] associated with the 
user’s logon credentials.  
Business Date The current business date.  
Trade Date The date the trade was executed.  
[[settlement]] Date The date a trade is scheduled to contractually settle (as submitted by the [[Member]] or 
assigned by [[GSD]]).  
Price/Rate The Contract Market Price (for Buy/Sell ) or Rate (for R epo/Revr ) on the trade. 
Par The total par value of the selected trade. 
[[settlement]] Amount  The dollar value of the transaction.  
Submission Type  Indicates the type of submission: Bilateral (BL), Demand  (DM) or Locked -In (LI)  
Uncompared Lists the total number of all Uncompared transactions (Repo, Revr, Buy & Sell) . 
TID [[GSD]] assigned Transaction Reference Number to identify the  specific trade.  
Transaction Type  Indicates the type of transaction: Buy, Sell, Repo or Revr.  
[[CUSIP]] The 9-character alphanumeric security identifier ([[CUSIP]] number) associated with the 
selected trade.  

---

## Page 127

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 127 
Item Description 
[[Member]] [[ID]] The system will automatically [[default]] to the 4- digit [[GSD]] [[Member]] [[ID]] associated with the 
user’s logon credentials.  
Contra [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]] associated with the contra -party. 
Business Date The current business date.  
Trade Date The date the trade was executed.  
[[settlement]] Date The date a trade is scheduled to contractually settle (as submitted by the [[Member]] or 
assigned by [[GSD]]).  
Price/Rate The Contract Market Price (for Buy/Sell ) or Rate (for R epo/Revr ) on the trade. 
Par The par value of the selected trade. 
[[settlement]] Amount  The dollar value of the trade. 
Submission Type  Indicates the type of submission: Bilateral (BL), Demand (DM) or Locked -In (LI)  
Table 27: DVP Advisory Management Screen Field Descriptions 
An Action Dropdown menu is provided next to each transaction record displayed on the DVP Advisory 
Management screen. The available actions are as follows: 
1. For Advisories – you can view the trade, affirm it, DK or look for potential matches from the trades listed in 
the Uncompared section of the screen. 
2. For Uncompared trades – you can view the trade, modify it, cancel it, or look for potential matches from 
the Advisories section of the screen. 
 
Figure 107: DVP Advisories Action Dropdown Menu 
Note:  
The DK [[Option]] will only appear on advisor y trades that have been submitted by a Repo [[Broker]] during the Demand Period  
where the viewing party is the contra -party. All other advisory trades will only display View, Affirm and Potential Matches as 
available actions in the dropdown menu.  


---

## Page 128

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 128 
Advisory Management > Affirm 
To affir m  an advisory from the DVP Advisory Management screen, select the vertical ellipsis       icon located to 
the left of the trade. Then select Affirm from the Action Dropdown Menu. Upon selecting the Affirm [[Option]], the 
trade details will appear on the screen.  
An external reference number must be entered before the Affirm button becomes accessible. Once the 
reference number has been entered, select the Affirm button.  
Because the confirmation and validation steps for the Affirm action is similar to the Modify action, those steps 
will not be covered here. For instructions and field descriptions regarding the Affirm screen, refer to the DVP 
Trade Search Results – View Trade Details Screen Field Descriptions table.  
 
Figure 108: DVP Advisory – Trade Affirmation 
Note: 
The Affirm button will not be enabled until an external reference number has been entered into the Trade Xref field.  
 
 
  


---

## Page 129

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 129 
Advisory Management > DK 
To DK an advisory from the DVP Advisory Management screen, select the vertical ellipsis       icon located to 
the left of the trade. Then select DK from the Action Dropdown Menu. Upon selecting the DK [[Option]], the trade 
details will appear on the screen.  
Note:  
Currently, only a Demand trade submitted by a Repo [[Broker]] may be DK’d.  
A DK Reason must be entered before the DK button becomes accessible. Once the DK Reason has been 
selected the from DK Reason Dropdown Menu, select the DK button.  
 
Figure 109: DVP Advisory – Trade DK 
Note: 
The DK button will not be enabled until a DK Reason is selected from the DK Reason Dropdown  Menu. 
 
 
 
  


---

## Page 130

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 130 
Upon selecting the DK Reason, the DK button becomes accessible. Now you can DK the trade by clicking the 
“DK” button.  
See below for an example of the DK screen prior to the submission of the DK action. 
 
Figure 110: DK screen prior to submission of DK action\ 
 
For instructions and field descriptions regarding the DK screen, refer to the DVP Trade Search Results – View 
Trade Details Screen Field Descriptions table.  
Once the DK button is selected, the below confirmation window will appear. Select Yes to confirm your DK. 
Select No to return back to the DK screen. 
 
Figure 111: DK Trade Confirmation Window 
 


---

## Page 131

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 131 
Once Yes is selected, the confirmation window will close. The DK has been accepted by the system. The DK 
screen will update with a success message as seen below. You can close the DK screen by clicking     . 
 
Figure 112: Trade DK Accepted Successfully Message 
  


---

## Page 132

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 132 
Advisory Management > Potential Matches 
To view potential matches for an advisory from the DVP Advisory Management screen, select the vertical 
ellipsis        icon located to the left of the trade. Then select Potential Matches from the Action Dropdown Menu. 
Upon selecting the Potential Matches [[Option]], the trade details will appear on the screen.  
From the Potential Matches screen you will be able to view any uncompared trades that may be potential 
matches for the selected advisory. If an uncompared trade requires modification, you can access the trade 
from the Uncompared trades, make the necessary modifications to affect a match. Also from this screen you 
can select to View or Affirm the Advisory.  
The Potential Matches screen for both an Advisory and Uncompared trade is separated into two sections: 
1. The top section of the screen shows all the details/fields of the selected trade (either an Advisory or 
Uncompared), but no fields may be modified in this section of the screen. 
2. The bottom section contains a list of potential matches that are the opposite transaction type of the 
selected trade (as described above in item #1). 
a. If an Advisory is selected, the list consists of Uncompared trades. 
b. If an Uncompared trade is selected, the list consists of Advisories. 
 
 
Figure 113: DVP Advisory - Potential Matches 
Note:  
If there is a potential match, the text that is highlighted in red  shows which fields are different between the selected trade 
and the trade in the list of potential matches.  
1 
2 


---

## Page 133

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 133 
GCF / CCIT Advisories 
The GCF / CCIT Advisories submitted on the Current Business Date can be accessed by clicking the 
Advisories quick link in the Statistics section of the GCF Dashboard. The Advisories quick link will take you 
directly to the results page where the trades submitted against the viewing [[Member]] can be found along with 
any potential matches, if applicable.  
Currently, unmatched CCIT Transactions submitted by either a [[GSD]] Netting [[Member]] or a CCIT [[Member]] will 
appear as Advisories to the contra-party. 
 
Figure 114: GCF / CCIT  Advisories Quick Link 
 
Note:  
Currently, there isn’t a GCF Advisory Management screen  as all GCF Repo Transactions are submitted for Locked -In 
Comparison. GCF Repo Transactions submitted by a GCF -Authorized Inter -Dealer [[Broker]] will appear in a pending 
affirmation (PAF) trade state for the GCF Counterparties. To view GCF Repo Transactions submitted against you, that are  
pending affirmation, click the Pending Affirm quick link located in the GCF Dashboard in the Statistics section.  
Note: 
GCF Repo Transactions submitted by GCF Counterparties will remain in pending comparison (PCP) trade state as such 
transactions are submitted for Bilateral Comparison. Currently GCF Repo Transactions are submitted to [[GSD]] on a Locked -
In Trade basis by GCF -Authorized Inter -Dealer Brokers, who are pursuant to [[FICC]] [[GSD]] Rules, Locked -In Trade Sources.  
Note:  
Advisories are trades that the contra- party has submitted against the viewing [[Member]] , but the viewing [[Member]] has not yet 
submitted their side of the trade with matching trade details.  


---

## Page 134

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 134 
Advisory Management 
Once the Advisories quick link is selected, the applicable CCIT Advisories will appear on the Trade Search 
results screen, similar to if you used the trade search functionality to view your advisories.  
 
Figure 115: Trade Search – GCF / CCIT Advisories 
 
An Action Dropdown menu is provided next to each transaction record. The allowable actions are View and 
Af firm.  
 
Figure 116: GCF / CCIT Advisories Action Dropdown Menu 


---

## Page 135

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 135 
Advisory Management > Affirm 
To affir m  an advisory from the GCF / CCIT Trade Search screen, select the vertical ellipsis       icon located to 
the left of the trade. Then select Affirm from the Action Dropdown Menu. Upon selecting the Affirm [[Option]], the 
trade details will appear on the screen 
You can choose to edit the existing Trade Xref and/or add a Secondary Xref. Once the reference numbers 
have been entered, select the Affirm button.  
Because the confirmation and validation steps for the Affirm action is similar to the Modify action, those steps 
will not be covered here. Refer to the DVP Trade Search Results / Trade Management section for further 
details on the confirmation and validation steps and screenshot examples. 
 
 
Figure 117: GCF / CCIT Advisory - Trade Affirmation 
  


---

## Page 136

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 136 
Trades > Rejects 
Rejects are trades that were submitted on the current business day by the [[Member]], but such trades were not 
processed by the system as they did not pass the validation criteria.  
Rejected DVP trades submitted on the current business date can be accessed by clicking the Rejects quick 
link in the Statistics section of the DVP Dashboard. The Rejects quick link will take you directly to the results 
page where the rejected trades can be found along with the reject reason(s) for each trade submission. 
 
Figure 118: DVP Rejects Quick Link 
Rejected GCF Repo and/or CCIT Transactions submitted on the current business date can be accessed by 
clicking the Rejects quick link in the Statistics section of the GCF Dashboard. The Rejects quick link will take 
you to the results page where the rejected trades can be found along with applicable reject reason(s). 
 
Figure 119: GCF/CCIT Rejects Quick Link 


---

## Page 137

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 137 
Trade Rejects Search 
To narrow search parameters specific to rejected trades, you can use the Trade Rejects Search screen. From 
the main toolbar located at the top of the page, select Trades > Rejects.  
 
Figure 120: Trades > Rejects 
 
When selecting the Rejects menu [[Option]] from the Trades dropdown menu, you will be directed to the Trade 
Rejects Search screen. From this screen you can enter criteria to narrow search parameters, i.e., specify 
product, [[CUSIP]] and/or Reject Reason. Once the search criteria is entered, click the Submit button. 
 
Figure 121: Trade Rejects Search Screen 
Note: 
The [[Member]] [[ID]] is preselected by [[default]] . Also, the availability of the DVP and/or GCF/CCIT Product type will depend on 
the membership type of the user’s [[Member]] f irm. 
  


---

## Page 138

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 138 
The Trade Rejects Search Screen contains the fields described in the following table. 
Note:  
The fields described in the table below are organized in the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom  within each section).  
Item Description 
[[Member]] [[ID]] The system will automatically [[default]] to the 4- digit [[GSD]] [[Member]] [[ID]] and Name associated 
with the user’s logon credentials.  
Note:  
The [[Member]] [[ID]] field defaults to the [[GSD]] [[Member]] [[ID]] and Name associated with the user’s 
logon credentials with the exception of u sers that have multiple [[Member]] IDs associated with 
their  logon credentials.  
Product  This is a mandatory field. Specify the Product of the trade that is being entered.  
[[CUSIP]] This is a mandatory field. Enter the [[CUSIP]] number of the security for the trade. This field 
must contain the whole [[CUSIP]] (9 -character maximum) and be in alphanumeric format.  
Note:  
Use the [[CUSIP]] Finder         function if only the root of the [[CUSIP]] is known. Click on this icon 
to open a popup window to search for a particular [[CUSIP]]. If you select a [[CUSIP]] from the 
popup screen, the [[CUSIP]] will be populated in the field.  
Reject Reason  The reason that the trade was not accepted by the system.  Also listed is the r eject reason 
code , which is a unique identifier  assigned by [[GSD]] to each reject reason . 
Reset Returns the fields on current screen to the original [[default]] values.  
Search Equivalent to a Submit button. Click to submit the data you entered on the Search screen to 
search for the records that fit the entered search criteria.  
Table 28: Trade Rejects Search Screen Field Descriptions 
 
  


---

## Page 139

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 139 
Trade Rejects Search Results 
Based on the search criteria entered, a user can use the information provided on the Trade Rejects Results 
screen to determine why a trade rejected by referring to the Reject Reason column. Users can also click the 
Reject [[ID]] hyperlink to view the available trade details for each of the listed rejects. 
Below is an example of the DVP Trade Rejects Results screen.   
 
Figure 122: DVP Trade Rejects Search Results 
 
Below is an example of the available trade details for a rejected trade submitted to the DVP system. 
 
Figure 123: Rejected DVP Trade Details 


---

## Page 140

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 140 
For field descriptions regarding the DVP Trade Rejects Results screen, please refer to the below table.  
Note:  
The fields described in the table below are organized in the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom  within each section).  
Item Description 
Reject [[ID]] The system generated unique message identifier  of a rejected trade, which is also a 
hyperlink to a popup window that displays the available trade details parsed from the SWIFT 
message along with the applicable reject code(s) and reject reason(s) . 
Trans Type  The transaction type of a  rejected trade, which can be a Buy, Sell, Repo, or Revr.  
[[CUSIP]] The 9-character [[CUSIP]] of the rejected trade.  
[[Member]] [[ID]] Indicates the [[Member]] [[ID]] for the [[Member]] who submitted the trades. This data is pulled from 
the [[Member]] [[ID]] field of the inbound SWIFT message.  
Contra  [[ID]] Data from the Contra [[ID]] field of the SWIFT message.  
Xref  The external reference number provided by the [[Member]] on the submission of the rejected 
trade. 
Reject Reason  The reason that the trade was not accepted by the system. 
Command Type  The system command that created the memo.  
Table 29: DVP Trade Rejects Results Screen Field Descriptions 
 
When a user selects the Reject [[ID]] from the DVP Trade Rejects Results screen, a popup window will appear. 
This popup window displays the available trade details parsed from the SWIFT message of the rejected trade. 
Also displayed in this window are the applicable reject code(s) and reject reason(s) for the submitted trade. For 
field descriptions regarding the Rejected Trade Details screen, please refer to the below table.  
Note:  
The fields described in the table below are organized in the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom  within each section).  
 
Item Description 
Reject [[ID]] The system generated unique message identifier  of a rejected trade. 
Product  The [[GSD]] Product for which the rejected trade was submitted for . 
Command Type  The system command that created the memo.  
[[Member]] [[ID]] Indicates the [[Member]] [[ID]] for the [[Member]] who submitted the trades. This data is pulled from 
the [[Member]] [[ID]] field of the inbound SWIFT message.  
Executing Firm Symbol  The 4- or 5-character [[ID]] of the Executing Firm , as applicable.  
[[CUSIP]] The 9-character [[CUSIP]] of the rejected trade.  
[[Broker]] Xref The [[Broker]] Xref associated with the rejected trade . 

---

## Page 141

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 141 
Item Description 
Trade Date The date the rejected trade was agreed upon/executed. The trade date is sent by the 
submitter as part of the SWIFT message.  
Trade Time The time when the rejected trade was executed . 
[[settlement]] Date The [[settlement]] Date (End Date) of the rejected trade.  
The transaction type of the rejected trade, which can be a Buy, Sell, Repo, or Revr.  
Par The Par Value from the SWIFT message. 
Amount The [[settlement]] Amount from the SWIFT m essage. 
Price The underlying price for the submitted trade. Displays the price  as-is from the SWIFT 
message.  
Contra  [[ID]] Data from the Contra [[ID]] field of the SWIFT message.  
Contra Executing Firm  The 4- or 5-character [[ID]] of the Contra Executing Firm, as applicable.  
Trade Xref  The external reference number provided by the [[Member]] on the SWIFT message. 
Pricing Method The Price Type specified on the inbound SWIFT message.  
D = discount, P = price, or Y = yield.  
Reject Reasons These fields describe applicable reject code(s) and reject reason(s) . 
Reject Code The Reject error code(s).  
Reject Reason  The detailed rejection reason(s).  
Reject Date The date when the reject occurred.  
Table 30: DVP Rejected Trade Details Screen Field Descriptions 
Note: 
If the in bound  SWIFT message is properly formatted, the user can see all of the fields that came across with the message, 
along with the reasons for the rejection. If the inbound  message is not properly formatted (unparsable), the message detail 
screen will show the entire SWIFT message (in XML format) sent by the submitter.  
 Note:  
Unparsable - Not able to split search results input into bits of data that can be easily stored.  
 
  

---

## Page 142

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 142 
Below is an example of the GCF Trade Rejects Results screen.   
 
Figure 124: GCF Trade Rejects Search Results 
 
Below is an example of the available trade details for a rejected trade submitted to the GCF system. 
 
Figure 125: Rejected GCF Trade Details 
 


---

## Page 143

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 143 
For field descriptions regarding the GCF Trade Rejects Results screen, please refer to the below table.  
Note:  
The fields described in the table below are organized in the same order as they appear on the screen (i.e., moving from top 
to bottom and left to right within each section) .  
Item Description 
Reject [[ID]] The system generated unique message identifier  of a rejected trade which is also a hyperlink 
to a popup window  that displays the available trade details  parsed from the SWIFT message 
along with the applicable reject code(s) and reject reason(s) . 
Trans Type  The transaction type of a rejected trade, which can be a Buy, Sell, Repo, or Revr.  
[[CUSIP]] The 9-character [[CUSIP]] of the rejected trade.  
[[Member]] [[ID]] Indicates the [[Member]] [[ID]] for the [[Member]] who submitted the trades. This data is pulled from 
the [[Member]] [[ID]] field of the inbound SWIFT message.  
Contra  [[ID]] Data from the Contra [[ID]] field of the SWIFT message. In the case of a Repo [[Broker]] Instruct 
message, this field contains the B roker ’s [[Member]] [[ID]]. 
Xref  The external reference number provided by the [[Member]] on the submission of the rejected 
trade. 
Reject Reason  The reason that the trade was not accepted by the system.  
Command Type  The system command that created the memo. 
Table 31: GCF Trade Rejects Results Screen Field Descriptions 
 
When a user selects the Reject [[ID]] from the GCF Trade Rejects Results screen, a popup window will appear. 
This popup window displays the available trade details parsed from the SWIFT message of the rejected trade. 
Also displayed in this window are the applicable reject code(s) and reject reason(s) for the submitted trade. For 
field descriptions regarding the Rejected Trade Details screen, please refer to the below table.  
Note:  
The fields described in the table below are organized in the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom  within each section).  
 
Item Description 
Reject [[ID]] The system generated unique message identifier  of a rejected trade. 
Product  The [[GSD]] Product for which the rejected trade was submitted for . 
Command Type  The system command that created the memo.  
[[Member]] [[ID]] Indicates the [[Member]] [[ID]] for the [[Member]] who submitted the trades. This data is pulled from 
the [[Member]] [[ID]] field of the inbound SWIFT message.  
Submitter [[participant]] [[ID]]  Indicates the [[Member]] [[ID]] of the submitting [[Member]] . 
[[CUSIP]] The 9-character [[CUSIP]] of the rejected trade.  

---

## Page 144

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 144 
Item Description 
[[Broker]] Xref The [[Broker]] Xref associated with the rejected trade . 
Trade Date The date the rejected trade was agreed upon/executed. The trade date is sent by the 
submitter as part of the SWIFT message.  
Trade Time The time when the rejected trade was executed . 
[[settlement]] Date The [[settlement]] Date (End Date) of the rejected trade.  
The transaction type of the rejected trade, which can be a Buy, Sell, Repo, or Revr.  
Start Money  The Start Money from the SWIFT m essage. 
Rate The Contract Repo  Rate for the repurchase agreement. Displays the rate as it was 
submitted on  the SWIFT message.  
Contra  [[ID]] Data from the Contra [[ID]] field of the SWIFT message . For a Brokered trade, this field 
contains the Repo B roker’s [[Member]] [[ID]]. 
Trade Xref  The external reference number provided by the [[Member]] on the SWIFT message. 
Secondary Xref  The secondary reference number from the SWIFT message.  
Reject Reasons These fields describe applicable reject code(s) and reject reason(s) . 
Reject Code The Reject error code(s).  
Reject Reason  The detailed rejection reason(s).  
Reject Date The date when the reject occurred.  
Table 32: GCF Rejected Trade Details Screen Field Descriptions 
Note: 
If the in bound  SWIFT message is properly formatted, the user can see all of the fields that came across with the message, 
along with the reasons for the rejection. If the inbound  message is not properly formatted (unparsable), the message detail 
screen will show the entire SWI FT message (in XML format) sent by the submitter.  
 Note:  
Unparsable - Not able to split search results input into bits of data that can be easily stored.  
 
  

---

## Page 145

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Trades 145 
Trades > CCIT Trade Fund Allocation (Reserved for Future Use) 
 
 

---

## Page 146

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[obligations]] 146 
[[obligations]] 
[[securities]] [[settlement]] [[obligations]] are the receive and/or deliver versus payment instructions of a [[Member]] 
versus [[FICC]] [[GSD]], created for [[settlement]] purposes.  From the navigation toolbar, select the menu item 
[[obligations]] to view a particular [[Member]]’s [[securities]] [[settlement]] [[obligations]].  
 
Figure 126: [[obligations]] 
 
The [[obligations]] Search function defaults to the Advanced Search [[Option]], but a user can easily select to query 
for a specific obligation using the Quick Search [[Option]]. These query options allow the user to search for a 
single obligation or multiple [[obligations]] versus [[FICC]] [[GSD]] on a given day, based on entered search criteria. 
Quick Search – [[obligations]]  
To search for [[obligations]] for which the Obligation [[ID]] (OID) or [[CUSIP]] is known, select the Quick Search [[Option]] 
as seen below.  
 
Figure 127: Quick Search - [[obligations]] 
  


---

## Page 147

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[obligations]] 147 
The Quick Search – [[obligations]] page contains the fields described in the following table. 
Item Description 
[[Member]] [[ID]] The system will automatically [[default]] to the 4-digit [[GSD]] [[Member]] [[ID]] and Name associated 
with the user’s logon credentials.  
Note:  
The [[Member]] [[ID]] field defaults to the [[GSD]] [[Member]] [[ID]] and Name associated with the user’s 
logon credentials with the exception of u sers that have multiple [[Member]] IDs associated with 
their  logon credentials.  
Search Criteria / String  To use Quick Search , the following selection must be made/entered : 
• For the criterion - Select either [[GSD]] assigned Obligation [[ID]] (OID) from the 
dropdown box list.  
• F or the string - Specify the whole or partial [[CUSIP]] .  
 Note:  
When entering a partial [[CUSIP]], the wildcard function does not require the use of the  
asterisk (*) in the string , but does require a minimum of 4 characters to be entered in to the 
[[CUSIP]] field . 
Search Equivalent to a Submit button. Click to submit the data you entered on the Search screen to 
search for the records that fit the entered search criteria.  
Table 33: Quick Search - [[obligations]] Screen Field Descriptions 
 
Enter the OID or [[CUSIP]], as applicable and then click Search. 
 
Figure 128: Quick Search – [[obligations]] Screen (Entered Criteria) 


---

## Page 148

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[obligations]] 148 
Once the Search button is selected, the screen will update and display the relevant search results for the 
entered criteria. In the example below, the results indicate that the user’s [[Member]] firm has a deliver “Subs” 
obligation that has yet to settle (Pending Clearance (PC) status). 
 
Figure 129: Quick Search – [[obligations]] Results Screen 
Note:  
The [[obligations]] Search Results are shown from the perspective of the user’s [[Member]] firm. [[obligations]] listed as Receive 
[[obligations]] indicate that [[FICC]]  is the deliverer of [[securities]] versus payment and the user’s [[Member]] firm is the receiver  of 
[[securities]] versus payment . [[obligations]] listed as Deliver Obligation s indicate that the user’s [[Member]] firm is the deliverer of 
[[securities]] versus payment and [[FICC]] is  the receiver of [[securities]] versus payment.  
The Quick Search – [[obligations]] Results page contains the fields described in the following table. 
Item Description 
Totals  
Receive Displays the Total Items, Total Par, and Total Amount for all Receive ( Long) [[obligations]].  
Deliver  Displays the Total Items, Total Par, and Total Amount for all Deliver ( Short ) [[obligations]].  
Receive  Displays the Receive [[obligations]] that fit the submitted search criteria. 
Vertical Ellipsis  Click the ‘Vertical Ellipsis“ next to the obligation to view additional details.  
Obligation [[ID]]  The [[GSD]] assigned Reference Number for the displayed obligation.  
[[Member]] [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]]. 
[[GSD]] Acct  The 4-digit internal [[GSD]] Account [[ID]].  
[[CUSIP]] The 9-character [[CUSIP]] for the obligation.  
[[settlement]] Date The business ([[settlement]]) date the obligation is scheduled to settle. 
Price The [[GSD]] system price.  


---

## Page 149

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[obligations]] 149 
Item Description 
Par  The [[settlement]] Par Value for the obligation.  
Amount The [[settlement]] Amount  for the obligation . 
Originator  Indicates the origination of the obligation, which would be one of the following:  
• ADMIN = Originated by Admin  Process  
• BKFL =  Originated by [[Broker]] Fail Process  
• HNET = Originated through Held Fail Process  
• NET = Originated from Netting Process  
• SDS = Originated through Same Day Sett ling Process  
• SUBS = Originated through Substitution  Process 
Status The Clearance State / Status Code of the obligation, which would be one of the following:  
• PC = Pending Clearance  
• CL = Cleared  
• CC = Clearance Cancel  
• HLD = Held  
• PO = Pair-Off  
• FD = Fails  
Deliver  Displays the Deliver [[obligations]] that fit the  submitted search criteria. 
Vertical Ellipsis  Click the ‘Vertical Ellipsis“ next to the obligation to view additional details.  
Obligation [[ID]]  The [[GSD]] assigned Reference Number for the displayed obligation.  
[[Member]] [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]]. 
[[GSD]] Acct  The 4-digit internal [[GSD]] Account [[ID]].  
[[CUSIP]] The 9-character [[CUSIP]] for the obligation.  
[[settlement]] Date The business ([[settlement]]) date the obligation is scheduled to settle. 
Price The [[GSD]] system price.  
Par  The [[settlement]] Par Value for the obligation.  
Amount The [[settlement]] Amount for the obligation . 
Originator  Indicates the origination of the obligation, which would be one of the following:  
• ADMIN = Originated by Admin  Process  
• BKFL =  Originated by [[Broker]] Fail Process  
• HNET = Originated through Held Fail Process  
• NET = Originated from Netting Process  
• SDS = Originated through Same Day Sett ling Process  
• SUBS = Originated through Substitution  Process 
Status The Clearance State / Status Code of the obligation, which would be one of the following:  
• PC = Pending Clearance  
• CL = Cleared  
• CC = Clearance Cancel  
• HLD = Held  
• PO = Pair-Off  
• FD = Fails  
Table 34: Quick Search - [[obligations]] Results Screen Field Descriptions 


---

## Page 150

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[obligations]] 150 
Advanced Search – [[obligations]]  
To [[DO]] a more granular search for [[obligations]], select the Advanced Search [[Option]] as seen below. The 
Advanced Search – [[obligations]] screen includes a number of dropdown boxes and other fields that can be 
used narrow down search parameters.  
 
Figure 130: Advanced Search - [[obligations]] Search Criteria Screen 
Note: 
The [[settlement]] Date Range will [[default]] to the current business date in the system. The [[settlement]] Date Range can be 
modified to suit the user’s search criteria.  Also, the Clearing Bank indicator will [[default]] to the Bank of New York Mellon 
(BNYM). BNYM is [[GSD]]’s Clearing Agent Bank.  


---

## Page 151

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[obligations]] 151 
Note:  
Fields marked with a red asterisk ( *  ) are mandatory and must be populated  for the system to process a search. The 
[[Member]] [[ID]] field defaults to the [[Member]] [[ID]] associated with the user’s logon credentials unless the user has multiple 
[[Member]] IDs associated with its logon credentials. All other fields are optional, which allows the user to define the search as 
specifically or broadly  as desired.  
The Advanced Search – [[obligations]] Screen contains the fields described in the following table. 
Note:  
The fields  described in the table below are organized in the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom within each section).  
Item Description 
[[Member]] [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]]. 
Obligation [[ID]]  The [[GSD]] assigned Reference Number for the displayed obligation.  
Clearance State The Clearance State / Status Code of the obligation, which would be one of the following:  
• PC = Pending Clearance  
• CL = Cleared  
• CC = Clearance Cancel  
• HLD = Held  
• PO = Pair-Off  
• FD = Fails  
[[CUSIP]] The 9-character [[CUSIP]] for the obligation.  
[[settlement]] Date Range The business ([[settlement]]) date range for when the obligation  is scheduled to settle. 
Business Event  Indicates the origination of the obligation, which would be one of the following:  
• ADMIN = Originated by Admin  Process  
• BKFL =  Originated by [[Broker]] Fail Process  
• HNET = Originated through Held Fail Process  
• NET = Originated from Netting Process  
• SDS = Originated through Same -Day Settling Process  
• SUBS = Originated through Substitution  Process 
[[settlement]] Amount The [[settlement]] Amount  for the obligation . 
[[GSD]] Account  The 4-digit internal [[GSD]] Account [[ID]].  
[[settlement]] Par  The [[settlement]] Par Value for the obligation.  
Receive / Deliver  Indicates whether the selected Obligation item is a Receive or Deliver transaction . 
Clearing Bank  The [[GSD]] Clearing Agent Bank where the obligation is to due settle.  
Reset Returns the fields on current screen to the original [[default]] values.  
Search  Equivalent to a Submit button. Click to submit the data you entered on the Search screen to 
search for the records that fit the entered search criteria.  
Comparison Operator  Select one of the comparison operators as it refers to the field: =, <>, <, <=, >, >=. 
Table 35: Advanced Search - [[obligations]] Screen Field Descriptions  

---

## Page 152

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[obligations]] 152 
To make a selection in a dropdown box, select the desired field to display the associated dropdown menu 
options. Then select the applicable menu [[Option]](s). Enter all other desired search criteria and then click the 
Search button. 
 
Figure 131: Advanced Search - [[obligations]] Screen (Entered Criteria) 
  


---

## Page 153

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[obligations]] 153 
Once the Search button is selected, the screen will update and display the relevant search results for the 
entered criteria. In the example below, the results indicate that the user’s [[Member]] firm has multiple receive 
[[obligations]] and a single deliver obligation.  
 
Figure 132: Advanced Search - [[obligations]] Results Screen 
 
The Advanced Search – [[obligations]] Results Screen contains the fields described in the following table. 
Item Description 
Totals  
Receive Displays the Total Items, Total Par, and Total Amount for all Receive ( Long) [[obligations]].  
Deliver  Displays the Total Items, Total Par, and Total Amount for all Deliver ( Short ) [[obligations]].  
Receive  Displays the Receive [[obligations]] that fit the submitted search criteria. 
Vertical Ellipsis  Click the ‘Vertical Ellipsis“ next to the obligation to view additional details.  
Obligation [[ID]]  The [[GSD]] assigned Reference Number for the displayed obligation.  
[[Member]] [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]]. 
[[GSD]] Acct  The 4-digit internal [[GSD]] Account [[ID]].  
[[CUSIP]] The 9-character [[CUSIP]] for the obligation.  
[[settlement]] Date The business ([[settlement]]) date the obligation is due to be  cleared.  
Price The [[GSD]] system price.  
Par  The [[settlement]] Par Value for the obligation.  
Amount The [[settlement]] Amount for the [[obligations]]  


---

## Page 154

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
[[obligations]] 154 
Item Description 
Originator  Indicates the origination of the obligation, which would be one of the following:  
• ADMIN = Originated by Admin  Process  
• BKFL =  Originated by [[Broker]] Fail Process  
• HNET = Originated through Held Fail Process  
• NET = Originated from Netting Process  
• SDS = Originated through Same -Day Settling Process  
• SUBS = Originated through Substitution  Process 
Status The Clearance State / Status Code of the obligation, which would be one of the following:  
• PC = Pending Clearance  
• CL = Cleared  
• CC = Clearance Cancel  
• HLD = Held  
• PO = Pair-Off  
• FD = Fails  
Deliver  Displays the Deliver [[obligations]] that fit the  submitted search criteria. 
Vertical Ellipsis  Click the ‘Vertical Ellipsis“ next to the obligation to view additional details.  
Obligation [[ID]]  The [[GSD]] assigned Reference Number for the displayed obligation.  
[[Member]] [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]]. 
[[GSD]] Acct  The 4-digit internal [[GSD]] Account [[ID]].  
[[CUSIP]] The 9-character [[CUSIP]] for the obligation.  
[[settlement]] Date The business ([[settlement]]) date the obligation is due to be cleared.  
Price The [[GSD]] system price.  
Par  The [[settlement]] Par Value for the obligation.  
Amount The [[settlement]] Amount for the obligation . 
Originator  Indicates the origination of the obligation, w hich would be one of the following:  
• ADMIN = Originated by Admin  Process  
• BKFL =  Originated by [[Broker]] Fail Process  
• HNET = Originated through Held Fail Process  
• NET = Originated from Netting Process  
• SDS = Originated through Same -Day Settling Process  
• SUBS = Originated through Substitution  Process 
Status The Clearance State / Status Code of the obligation, which would be one of the following:  
• PC = Pending Clearance  
• CL = Cleared  
• CC = Clearance Cancel  
• HLD = Held  
• PO = Pair-Off  
• FD = Fails  
Table 36: Advanced Search - [[obligations]] Results Screen Field Descriptions 


---

## Page 155

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 155 
SUBSTITUTIONS 
The Substitutions dropdown menu provides an automated facility that allows for the entry, viewing, managing 
and monitoring of the substitutions process.  
 
Figure 133: Substitutions dropdown menu 
 
Eligible parties are able to enter the substitution of current [[collateral]] of a repo transaction, that they are a party 
to, with [[collateral]] of equivalent value (known as replacement [[collateral]])  in order to keep the repurchase 
agreement intact. Through this substitution facility, the replacement [[collateral]] security then becomes the 
[[collateral]] for the repo. 
Substitutions > Entry 
From the Substitutions > Entry menu selection, eligible parties can enter repo substitution notifications on 
active term repo transactions that are in the system. 
 
Figure 134: Substitutions > Entry 
Note: 
For Bilateral term repos between two dealers, only the Repo Party can enter the substitution notification on the repo 
transaction . For Brokered term repos, where one party to the trade is a Repo [[Broker]], Demand Trade Source or Locked -In 
Trade Source, only s uch submitter can enter the substitution notification on the repo transaction.  
Note: 
Currently, repo substitution notifications can only be entered through the Substitutions > Entry screen on [[GSD]] RTTM Web.  


---

## Page 156

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 156 
Substitution Entry for Dealer Submitter  
The Dealer Substitutions Entry screen is used by the Repo Party to a Bilateral Term Repo Transaction to enter 
[[collateral]] substitution information into [[GSD]] RTTM Web. 
 
Figure 135: Dealer Substitutions Entry Screen 
 
To enter a repo [[collateral]] substitution notification the user would first enter the required information in the 
Substitution Details section and the Current [[collateral]] Details section by following one of the two entry 
methods below: 
1. Use the Get Trade function if the user knows either the TID or Xref for the trade to be subbed and then: 
a. Select either TID / Xref from the dropdown menu 
i. TID or 
ii. Xref 
b. Select to use like trades or to sub a specific trade 
i. Use Like Trades or 
ii. Use This Trade  
c. Enter either the TID or Xref, as applicable, then select the Enter      icon to submit. 
 
OR 
 
 
 


---

## Page 157

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 157 
 
2. Populate the required fields (∗) with the Current [[collateral]] Details: 
a. [[Member]] [[ID]] ([[default]] based on user logon credentials) 
b. Start Date 
c. End Date 
d. Ef fective Business Date 
e. Repo [[Member]] [[ID]] 
f. Reverse [[Member]] [[ID]] 
g. [[CUSIP]] 
h. Par 
i. Principal 
j. Repo Rate 
 
Note: 
If [[Option]] 1 above is selected and the user chose Use Like Trades, then the system would populate the required  fields with 
general trade details that were similar to the details on the trade tied to TID or Xref. 
If [[Option]] 1 above is selected and the user chose Use This Trade, then the system would populate the required fields with 
the exact trade details for the TID or Xref.  
After the Current [[collateral]] Details have been entered, the Replacement [[collateral]] Details section will become 
editable.  
Note:  
Repo substitution notifications can be entered in par value increments of 50mm up to the max par value of 400mm . R epo 
substitution notifications can also include a par value that is under 50mm. A trade with a par value of less than 50mm is 
considered a “tail”.  Only one “tail” piece can be submitted per substitution notification.  
If the user knows the details of the Replacement [[collateral]], then the user would select + Add Row and then  
enter the [[CUSIP]], Par and Principal.  
 
Figure 136: Replacement [[collateral]] Details (+ Add Row) 
Note: 
The Replacement [[collateral]] can be entered for a Real [[CUSIP]] or a Generic [[collateral]] [[CUSIP]].  
Note: 
The Repo Rate field for the Replacement [[collateral]] will not be an editable field.   


---

## Page 158

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 158 
If the user does not know the details of the Replacement [[collateral]] at the time of entry for the repo [[collateral]] 
substitution notification, then the user may leave the Replacement [[collateral]] fields blank and the system 
would, upon initial submission of the substitution notification, enter a generic [[collateral]] [[CUSIP]] as the 
Replacement [[collateral]]. The user would then receive the message, “Substitution has not been submitted. 
[[default]] [[CUSIP]] being applied to your substitution request. Please resubmit to process your request.”  
Click the Submit button again to continue with the notification. 
 
Figure 137: Dealer Substitutions Entry - Replacement [[collateral]] Not Entered 
 
The Replacement [[collateral]] will be in the generic [[collateral]] [[CUSIP]] until such time the user modifies the 
notification and allocates to a Real [[CUSIP]].  
  


---

## Page 159

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 159 
Once all of the fields have been populated, click the Submit button. 
 
Figure 138: Dealer Substitutions Entry Screen (fields populated) 
 
If the Substitutions entry passes all of the [[GSD]] validation checks, the screen would update and display a 
success message along with a Substitution identification ([[ID]]) number that has been assigned to the entry. 
 
Figure 139: Dealer Substitution Entry Successfully submitted 
Note:  
If the Replacement [[collateral]] details were not specified before submission, then note the Substitution [[ID]] in order to retri eve 
the details on the entry and submit the allocation to a Real [[CUSIP]] when those details become known.  


---

## Page 160

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 160 
If the system is not able to validate and process the substitution, a reject message will appear. The user should 
make the necessary corrections and resubmit the substitution. 
 
Figure 140: Dealer Substitution Entry Rejected 
 
For additional instructions and field descriptions regarding the Dealer Substitutions Entry screen, please refer 
to the below table. 
Note:  
The fields  described in the table below are organized in the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom  within each section).  
Field/Item Name  Instructions/Descriptions 
Substitution Details  
[[Member]] [[ID]] The system will automatically [[default]] to the 4- digit [[GSD]] [[Member]] [[ID]] and Name associated 
with the user’s logon credentials.  
Note:  
The [[Member]] [[ID]] field defaults to the [[GSD]] [[Member]] [[ID]] and Name associated with the user’s 
logon credentials with the exception of u sers that have multiple [[Member]] IDs associated with 
their  logon credentials.  
Get Trade 
• TID / Xref 
• Use Like Trades / Use 
This Trade  
The Get Trade function is used when a user wants to retrieve a specific Repo Transaction or 
like transactions systemically.  
• From the dropdown menu, select either TID or Xref  
• Select the radial button for either User Like Trades or Use This Trade 
• Then enter the number for either the TID or Xref (whichever was selected from the 
dropdown menu referenced above).  
• Then click the Enter      button.  
Start Date This is a mandatory field. Specify the Repo Start Date of the trade that is being subbed. 
Format = mm/dd/ yyyy.  
End Date This is a mandatory field. Specify the Repo End Date of the trade that is being subbed. 
Format = mm/dd/ yyyy.  


---

## Page 161

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 161 
Field/Item Name  Instructions/Descriptions 
Effective Business Date This is a mandatory field. Specify the effective date for the sub. Format = mm/dd/ yyyy.  
Repo [[Member]] [[ID]] This is a mandatory field. Based on the user ’s profile, the system automatically populates 
this field with the [[Member]] [[ID]] and Name. 
Reverse [[Member]] [[ID]]  This is a mandatory field. Enter either the 4-digit Reverse Repo Party [[Member]]  [[ID]] or the 
associated [[Member]] Name or select the 4- digit Reverse Repo Party [[Member]] [[ID]] or the 
associated [[Member]]  Name from the dropdown menu .  
Comments  An area for the user to enter any notes or comments about the Substitution Entry . 
Admin Comments  An area for Admin users to enter any notes or comments about the Substitution Entry . 
Current [[collateral]] 
Details 
These fields describe the [[collateral]] to be replaced as a result of the Substitution 
Entry. 
[[CUSIP]] Enter the [[CUSIP]] number of the current [[collateral]] to be replaced . This field must contain the 
whole [[CUSIP]] (9-character maximum)  and be in alphanumeric format .  
Note:  
Use the [[CUSIP]] Finder         function if only the root of the [[CUSIP]] is known.  Click on this icon 
to open a popup window to search for a particular [[CUSIP]]. If you select a [[CUSIP]] from the 
popup sc reen, the [[CUSIP]] will be populated in the field . 
Par This is a mandatory field. Enter the par value of the current [[collateral]] to be replaced, which 
cannot exceed 400mm. Format = ###mm with no decimal places . 
Principal This is a mandatory field. Specify the principal amount  of the current [[collateral]] to be 
replaced  (18-character maximum, incl. commas and 2 decimal places).   
Repo Rate (%)  This is a mandatory field. Specify the current Repo Rate of the current [[collateral]] to be 
replaced.  
Replacement [[collateral]] 
Details 
These fields are used to describe the Replacement [[collateral]] for t he Substitution 
Entry. 
Note:  
This section does not need to be completed until you have the information for the real 
[[collateral]] unless you prefer to enter a specific generic product [[CUSIP]]. When no information is 
entered, the system defaults to a generic [[collateral]] [[CUSIP]].   
Note:   
When adding additional rows , the use of a generic [[CUSIP]] is prohibited.  
[[CUSIP]] Enter the [[CUSIP]] number of the replacement [[collateral]] item. Format = alphanumeric, 9-
character maximum.  
Note:  
When none is entered, the system will [[default]] to a generic [[collateral]] [[CUSIP]].  


---

## Page 162

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 162 
Field/Item Name  Instructions/Descriptions 
Note:  
Use the [[CUSIP]] Finder         function if only the root of the [[CUSIP]] is known.  Click on this icon 
to open a popup window to search for a particular [[CUSIP]]. If you select a [[CUSIP]] from the 
popup screen, the [[CUSIP]] will be populated in the field . 
Par Enter the par value of the replacement [[collateral]] item. Each Substitution entry cannot 
exceed 400mm. Format = ###mm with no decimal places.  
Note:  
This field is not required on initial entry, but is required when entering the information for the 
real colla teral. 
Principal Specify the principal amount  of the replacement [[collateral]] item  (18-character maximum, incl. 
commas and 2 decimal places).   
Note:  
This field is not required on initial entry, but is required when entering the information for the 
real co llateral.  
Repo Rate (%)  This field is not editable. System will auto-populate based on what is entered into the 
Current [[collateral]] Repo Rate field . 
Icon/Button  Instructions/Description 
 Click to add a row.  
 Click to select a singular date or a date range, as applicable.  
 Click to copy all of the data from the current row to a new row, except the Xref. This differs 
from the Add Row icon. 
* Indicates a required field.  
 Click to delete a row.  
 Click the down arrow to display a dropdown menu from which you can make a selection.  
 Click to close the selected window.  
Reset Returns the fields on current screen to the original [[default]] values.  
Submit Click to submit the data you entered on the Subs titution Entry screen to process your 
notification request.  
Table 37: Dealer Substitutions Entry Screen Field Descriptions 
  


---

## Page 163

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 163 
Substitution Entry Examples for Dealer Submitter 
This section will provide examples of some types of Substitution Entries.  
How to Enter a “Bulk” Substitution Notification 
The system can process a substitution notification where the current & replacement [[collateral]] includes multiple 
lots of 50mm in par value.  
 
Figure 141: “Bulk” Substitution Notification 
 
Note:  
A “bulk” sub means a notification that is entered for multiple lots of 50mm in par value. 
Note: 
Repo substitution can be entered in par value increments of 50mm  up to the max par value of 400mm. Repo substitution 
notifications can also include a par value that is under 50mm. A trade with a par value of less than 50mm is considered a 
“tail”. Only one “tail” piece can be submitted per substitution notification.  
  


---

## Page 164

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 164 
How to Enter a Substitution Notification with Multiple Allocations (CUSIPs) 
The system can process a substitution notification where the replacement [[collateral]] has more than one 
security. 
 
Figure 142: Substitution Notification with Multiple Allocations 
  


---

## Page 165

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 165 
How to Enter a Future Pending Substitution Notification 
The system will accept a substitution notification for future processing if the effective business date is a future 
and valid business date. 
 
Figure 143: Future Pending Substitution Notification 
 
Note:  
In the above example. the substitution entry was submitted on 12/17/2021 with an effective business date of 12/20/2021.  
For reference, the Substitution [[ID]] displays the date of submission in its format, i.e., S03 2A8-1C17, is the sub number 
(S032A8), Year (1 = for 2021), Month ( C) and Day (17).  
Note:  
Regarding the date format of [[GSD]] assigned IDs  generat ed during the latter months of the year (October through 
December), the month wi ll be indicated as follows: A = October, B = November and C = December. For January through 
September, the months  will be indicated by number 1-9 , i.e., 1 = January, 2 = February, and so on. .  


---

## Page 166

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 166 
How to Enter a Substitution Notification with a “Tail” 
The system can process a substitution notification where the replacement [[collateral]] has a single tail. 
 
Figure 144: Substitution Notification with a "Tail" 
 
Note:  
A trade with a par value of less than 50mm is considered a “tail”.  Only one “tail” piece can be submitted per substitution 
notification. 
Note: 
There are two options for adding a tail to the replacement [[collateral]]:  
1. As displayed in the above screenshot, the replacement [[collateral]] can be entered with the tail included as one line item, 
i.e., the total replacement [[collateral]] par value is 75mm and is entered as 75mm, or  
2. The replacement [[collateral]] can be entered where the tail is added as a separate line item. To [[DO]] this, the user would 
enter into the available field the details  for the replacement  [[collateral]],  in par value increments of 50mm up to 400mm 
and then click the + Add Row  link and enter the tail  into the new row , i.e., the total replacement [[collateral]] par value is 
75mm and is entered as 50mm and 25mm, respectively.  
 
 


---

## Page 167

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 167 
How to Enter a Substitution Notification of a “Tail”  
The system can process a substitution notification on a repo transaction where the par value is under 50mm. 
 
Figure 145: Substitution Notification of a "Tail" 
 
Note:  
A trade with a par value of less than 50mm is considered a “tail”. Only one “tail” piece can be submitted per substitution 
notification.  


---

## Page 168

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 168 
Substitution Entry for [[Broker]] Submitter 
The [[Broker]] Substitutions Entry screen is used by the submitter to enter [[collateral]] substitution information into 
[[GSD]] RTTM Web. 
 
Figure 146: [[Broker]] Substitutions Entry Screen 
 
To enter a repo [[collateral]] substitution notification the user would first enter the required information in the 
Substitution Details section and the Current [[collateral]] Details section by following one of the two entry 
methods below: 
1. Use the Get Trade function if the user knows either the TID or Xref for the trade to be subbed and then: 
a. Select either TID / Xref from the dropdown menu 
i. TID or 
ii. Xref  
b. Enter either the TID or Xref, as applicable, then select the Enter      icon to submit. 
 
OR 
  


---

## Page 169

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 169 
2. Populate the required fields (∗) with the Current [[collateral]] Details: 
a. [[Member]] [[ID]] ([[default]] based on user logon credentials) 
b. Start Date 
c. End Date 
d. Ef fective Business Date 
e. Repo [[Member]] [[ID]] 
f. Reverse [[Member]] [[ID]] 
g. [[CUSIP]] 
h. Par 
i. Principal 
j. Repo Rate 
 
Note:  
For [[Broker]] Substitution s Entry Screen, the Get Trade function does not offer the [[Option]] to Use Like  Trades / Use This 
Trade. 
After the Current [[collateral]] Details have been entered, the Replacement [[collateral]] Details section will become 
editable.  
Note:  
Repo substitution can be entered in par value increments of 50mm up to the max par value of 400mm. Repo substitution 
notifications can also include a par value that is under 50mm. A trade with a par value of less than 50mm is considered a 
“tail”. Only one “tail” piece can be submitted per substitution notification.  
If the user knows the details of the Replacement [[collateral]], then the user would select + Add Row and then  
enter the [[CUSIP]], Par and Principal.  
 
Figure 147: Replacement [[collateral]] Details (+ Add Row) 
Note: 
The Replacement [[collateral]] can be entered for a Real [[CUSIP]] or a Generic [[collateral]] [[CUSIP]].  
Note: 
The Repo Rate field for the Replacement [[collateral]] will not be an editable field.  
  


---

## Page 170

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 170 
If the user does not know the details of the Replacement [[collateral]] at the time of entry for the repo [[collateral]] 
substitution notification, then the user may leave the Replacement [[collateral]] fields blank and the system 
would, upon initial submission of the substitution notification, enter a generic [[collateral]] [[CUSIP]] as the 
Replacement [[collateral]]. The user would then receive the message, “Substitution has not been submitted. 
[[default]] [[CUSIP]] being applied to your substitution request. Please resubmit to process your request.”  
Click the Submit button again to continue with the notification. 
 
Figure 148: [[Broker]] Substitutions Entry - Replacement [[collateral]] Not Entered 
 
The Replacement [[collateral]] will be in the generic [[collateral]] [[CUSIP]] until such time the user modifies the 
notification and allocates to a Real [[CUSIP]].  
  


---

## Page 171

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 171 
Once all of  the fields have been populated, click the Submit button. 
 
Figure 149: [[Broker]] Substitutions Entry Screen (fields populated) 
 
If the Substitutions entry passes all of the [[GSD]] validation checks, the screen would update and display a 
success message along with a Substitution identification ([[ID]]) number that has been assigned to the entry. 
 
Figure 150: [[Broker]] Substitutions Entry Successfully Submitted 
Note:  
If the Replacement [[collateral]] details were not specified before submission, then note the Substitution [[ID]] in order to retrieve 
the details on the entry and submit the allocation to a Real [[CUSIP]] when those details become known.  


---

## Page 172

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 172 
If the system is not able to validate and process the substitution, a reject message will appear. The user should 
make the necessary corrections and resubmit the substitution. 
 
Figure 151: [[Broker]] Substitutions Entry Rejected 
 
For additional instructions and field descriptions regarding the [[Broker]] Substitutions Entry screen, please refer 
to the below table. 
Note:  
The fields  described in the table below are organized in the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom  within each section).  
Field/Item Name  Instructions/Descriptions 
Substitution Details  
[[Member]] [[ID]] The system will automatically [[default]] to the 4- digit [[GSD]] [[Member]] [[ID]] and Name associated 
with the user’s logon credentials.  
Note:  
The [[Member]] [[ID]] field defaults to the [[GSD]] [[Member]] [[ID]] and Name associated with the user’s 
logon credentials with the exception of u sers that have multiple [[Member]] IDs associated with 
their  logon credentials.  
Get Trade 
• TID / Xref 
 
The Get Trade function is used when a user wants to retrieve details for like transactions.  
• From the dropdown menu, select either TID or Xref  
• Then enter the  number for either the TID or Xref (whichever was selected from the 
dropdown menu referenced above).  
• Then click the Enter      button.  
Start Date This is a mandatory field. Specify the Repo Start Date of the trade that is being subbed. 
Format = mm/dd/ yyyy.  


---

## Page 173

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 173 
Field/Item Name  Instructions/Descriptions 
End Date This is a mandatory field. Specify the Repo End Date of the trade that is being subbed. 
Format = mm/dd/ yyyy.  
Effective Business Date This is a mandatory field. Specify the effective date for the sub. Format = mm/dd/ yyyy.  
Repo [[Member]] [[ID]] This is a mandatory field. Enter either the 4- digit Repo Party [[Member]] [[ID]] or the associated 
[[Member]] Name or select the 4- digit Repo Party [[Member]] [[ID]] or the associated [[Member]]  Name 
from the dropdown menu.  
Note: 
This field is unlike the Repo [[Member]] [[ID]] field for a Dealer Substitutions Entry which is based 
on the user’s profile . 
Reverse [[Member]] [[ID]]  This is a mandatory field. Enter either the 4-digit Reverse Repo Party [[Member]]  [[ID]] or the 
associated [[Member]]  Name or select the 4- digit Reverse Repo Party [[Member]]  [[ID]] or the 
associated [[Member]]  Name from the dropdown menu .  
Comments  An area for the user to enter any notes or comments about the Substitution Entry . 
Admin Comments  An area for Admin users to enter any notes or comments about the Substitution Entry. 
Current [[collateral]] 
Details 
These fields describe the [[collateral]] to be replaced as a result of the Substitution 
Entry. 
[[CUSIP]] Enter the [[CUSIP]] number of the current [[collateral]] to be replaced . This field must contain the 
whole [[CUSIP]] (9-character maximum)  and be in alphanumeric format.  
Note:  
Use the [[CUSIP]] Finder         function if only the root of the [[CUSIP]] is known.  Click on this icon 
to open a popup window to search for a particular [[CUSIP]]. If you select a [[CUSIP]] from the 
popup screen, the [[CUSIP]] will be populated in the field . 
Par This is a mandatory field. Enter the par value of the current [[collateral]] to be replaced,  which 
cannot exceed 400mm. Format = ###mm with no decimal places . 
Principal This is a mandatory field. Specify the principal amount  of the current [[collateral]] to be 
replaced  (18-character maximum, incl. commas and 2 decimal places).   
Repo Rate (%)  This is a mandatory field. Specify the current Repo Rate of the current [[collateral]] to be 
replaced.  
Replacement [[collateral]] 
Details 
These fields are used to describe the Replacement [[collateral]] for t he Substitution 
Entry. 
Note:  
This section does not need to be completed until you have the information for the real 
[[collateral]] unless you prefer to enter a specific generic product [[CUSIP]]. W hen no information is 
entered, the system defaults to a generic [[collateral]] [[CUSIP]].  
Note:   
When adding additional rows, the use of a generic [[CUSIP]] is prohibited.  


---

## Page 174

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 174 
Field/Item Name  Instructions/Descriptions 
[[CUSIP]] Enter the [[CUSIP]] number of the replacement [[collateral]] item. Format = alphanumeric, 9-
character maximum.  
Note:  
When none is entered, the system will [[default]] to a generic [[collateral]] [[CUSIP]].  
Note:  
Use the [[CUSIP]] Finder         function if only the root of the [[CUSIP]] is known.  Click on this icon 
to open a popup window to search for a particular [[CUSIP]]. If you select a [[CUSIP]] from the 
popup screen, the [[CUSIP]] will be populated in the field . 
Par Enter the par value of the replacement [[collateral]] item. Each Substitution entry cannot 
exceed 400mm. Format = ###mm with no decimal places . 
Note:  
This field is not required on initial entry, but is required when entering the information for the 
real colla teral. 
Principal Specify the principal amount  of the replacement [[collateral]] item  (18-character maximum, incl. 
commas and 2 decimal places).   
Note:  
This field is not required on initial entry, but is required when entering the information for the 
real co llateral.  
Repo Rate (%)  This field is not editable. System will auto -populate based on what is entered into the 
Current [[collateral]] Repo Rate field.  
Icon/Button  Instructions/Description 
 Click to add a row.  
 Click to select a singular date or a date range, as applicable.  
 Click to copy all the data from the current row to a new row, except the Xref. This differs 
from the Add Row icon. 
* Indicates a required field.  
 Click to delete a row.  
 Click the down arrow to display a dropdown menu from which you can make a selection.  
 Click to close the selected window.  
Reset Returns the fields on current screen to the original [[default]] values.  
Submit Click to submit the data you entered on the Subs titution Entry screen to process your 
notification request.  
Table 38: [[Broker]] Substitutions Entry Screen Field Descriptions 
 


---

## Page 175

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 175 
Substitution Entry Examples for [[Broker]] Submitter 
This section will provide examples of some types of substitution entries a [[Broker]] may submit to [[GSD]].  
How to Enter a “Bulk” Substitution Notification 
The system can process a substitution notification where the current & replacement [[collateral]] includes multiple 
lots of 50mm in par value.  
 
Figure 152: "Bulk" Substitution Notification 
 
Note:  
A “bulk” sub means a notification that is entered for multiple lots of 50mm in par value. 
Note: 
Repo substitution notifications can be entered in par value increments of 50mm up to the max par value of 400mm. Repo 
substitution notifications can also include a par value that is under 50mm. A trade with a par value of less than 50mm is 
considered a “tail”. Only one “tail” piece can be submitted per substitution notification.  
  


---

## Page 176

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 176 
How to Enter a Substitution Notification with Multiple Allocations (CUSIPs) 
The system can process a substitution notification where the replacement [[collateral]] has more than one 
security. 
 
Figure 153: Substitution Notification with Multiple Allocations 
  


---

## Page 177

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 177 
How to Enter a Future Pending Substitution Notification 
The system will accept a substitution notification for future processing if the effective business date is a future 
and valid business date. 
 
Figure 154: Future Pending Substitution Notification 
 
Note:  
In the above example, the substitution entry was submitted on 07/19/2021 with an effective business date of 07/20/2021. 
For reference, the Substitution [[ID]] displays the date of submission in its format, i.e., S03193- 1719, is the sub number 
(S03193), Year (1 = for 2021), Month (7) and Day (19).  
Note: 
Regarding the date format of [[GSD]] assigned IDs generated during the latter months of the year (October through 
December), the month will be indicated as follows: A = October, B = November and C = December. For January through 
September, the months will be indicated by number 1- 9, i.e., 1 = January, 2 = February, and so on.   


---

## Page 178

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 178 
How to Enter a Substitution Notification with a “Tail” 
The system can process a substitution notification where the replacement [[collateral]] has a single tail. 
 
Figure 155: Substitution Notification with a "Tail" 
 
Note:  
A trade with a par value of less than 50mm is considered a “tail”.  Only one “tail” piece can be submitted per substitution 
notification. 
Note: 
There are two options fo r adding a tail to the replacement [[collateral]]:  
1. As displayed in the above screenshot, the replacement [[collateral]] can be entered where the tail is added as a separate 
line item. To [[DO]] this, the user would enter into the available field the details for the replacement [[collateral]], in par value 
increments of 50mm up to 400mm and then click the + Add Row  link and enter the tail into the new row, i.e., the total 
replacement [[collateral]] par value is 75mm and is entered as 50mm and 25mm, respectively , or 
2. The replacem ent [[collateral]] can be entered with the tail included as one line item, i.e., the total replacement [[collateral]] 
par value is 75mm and is entered as 75mm.  
 
  


---

## Page 179

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 179 
How to Enter a Substitution Notification of a “Tail” 
The system can process a substitution notification on a repo transaction where the par value is under $50mm. 
 
Figure 156: Substitution Notification of a "Tail" 
 
Note:  
A trade with a par value of less than 50mm is considered a “tail”.  Only one “tail” piece can be submitted per substitution 
notification. 
  


---

## Page 180

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 180 
Examples of Invalid Substitution Entries 
This section will provide some examples of invalid substitution entries (applies to both [[Broker]] and Dealer 
Submitters). 
Substitution Entries Rejected  
If the system is not able to validate and process the substitution, a reject message will appear. The user should 
make the necessary corrections and resubmit the substitution. 
Sub Not Accepted – Replacement [[collateral]] Has Incorrect Par Denomination  
The system will not accept a substitution notification where the replacement [[collateral]] has a par value that is 
not eligible for [[settlement]] due to an invalid par minimum/multiple denomination. 
 
 
  
Figure 157: Substitution Notification Rejected - Incorrect Par Denomination 

---

## Page 181

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 181 
Sub Not Accepted – Cannot Create Multiple Tails 
The system will not accept a substitution notification where the replacement [[collateral]] has 2 tail pieces.  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
Note:  
A trade with a par value of less than $50mm is considered a “tail”.  Only one “tail” piece can be submitted per substitution 
notification. 
  
Figure 158: Substitution Notification Rejected - Multiple Tails 

---

## Page 182

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 182 
Sub Not Accepted – Replacement [[collateral]] Has Invalid [[CUSIP]] 
The system will not accept a substitution notification where the replacement [[collateral]] has a security that is not 
eligible for [[settlement]] because the security is not set up in the security master file. 
 
Figure 159: Substitution Notification Rejected - [[CUSIP]] Not Found 
  


---

## Page 183

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 183 
Sub Not Accepted – Cannot Change the Repo Rate through a Substitution 
The system will not accept a substitution notification where there is an attempt to change the repo rate on the 
trade. The system does not permit the changing of the repo rate on either the current [[collateral]] or the 
replacement [[collateral]]. 
 
Figure 160: Substitution Notification Rejected - Repo Rate Change Not Allowed 
 
  


---

## Page 184

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 184 
Substitution Entries Accepted But Not Processed (NP-Pending) 
If the system accepts but is not able to process a substitution notification, the substitution entry will be in a 
Pending Status. The user should use the Substitutions > Search & Management function to either make the 
necessary corrections and resubmit the substitution or delete the substitution. 
Sub Accepted, Sub Not Processed – Current [[collateral]] Does Not Exist 
The system will accept but not process (NP) a substitution notification for current [[collateral]] that cannot be 
validated by the system. In the below example, the incorrect [[CUSIP]] was entered into the [[CUSIP]] field for the 
current [[collateral]]. 
 
 
Figure 161: Substitution Notification Accepted but Not Processed 
 
Note:  
This substitution notification was accepted by the system but not processed.  
 
  


---

## Page 185

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 185 
Substitutions > Search & Management  
From the Substitutions > Search & Management dropdown menu selection, eligible parties can view and 
manage their active repo substitutions. 
 
Figure 162: Substitutions > Search & Management 
Note: 
Only the Submitter of a repo substitution notification can access the details on the substitution in the Search & 
Management screen.  
Substitutions Search for Dealer Submitter 
For users that have access provisioned for more than one [[Member]] account, such users can access the search 
feature located in the left [[Margin]] of the page. Users can select from the list of available accounts, the [[Member]] 
[[ID]] and Name they wish to query for. Then click the Search button to view the search results. 
 
Figure 163: Dealer Substitutions Search Screen 
  


---

## Page 186

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 186 
Substitutions Management for Dealer Submitter 
The below screen allows users to manage their substitution entries. From this screen, users can view the 
status of their Substitutions (see item labeled 1), view related trade details and obligation details, make 
modifications and submit deletions on pending substitutions (see item labeled 2). The data on this screen is 
dynamically/automatically updated. 
 
Figure 164: Dealer Substitutions Management Screen 
 
The totals for all substitution activity for a given day are displayed in the lower right corner of the Substitutions  
Status window (see item labeled 1) on the page. Also displayed in the Substitutions Window are the  
Substitutions’ statuses (e.g., Pending, Awaiting Allocation, Fully Allocated, Deleted, and Future Pending). 
 
The All Items Status will display all active substitutions regardless of their status. To view the substitution 
activity for a selected status, click on its respective status link, i.e., to view only those substitutions with a status 
of Awaiting Allocation (see item labeled 1a), select the Awaiting Allocation link. 
 
 
Figure 165: Dealer Substitutions Status Window 
1 
2 
1a 
1 

---

## Page 187

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 187 
The total number of substitions entered on a given day is also displayed in the upper right corner of the 
Substitutions Search Results Window (see item labeled 2) on the page.  
Refer to the following page for how to access additional information or take an Action on a Substitution. 
 
Figure 166: Substitutions Search Results Window 
 
For additional instructions and field descriptions regarding the Dealer Substitutions Management Screen, 
please refer to the below table. 
Note:  
The fields  described in the table below are organized in the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom  within each section).  
Field/Item Name  Instructions/Descriptions 
Substitution Status Window 
Status The Status of the Substitution item. It can be any of the following:         
• Pending – The substitution notification has not processed. The system is not able to 
process the substitution due to incorrect data entry. The substitution notification must be 
corrected via Modify Action  for the request to be accepted.  
• Awaiting Allocation  – The substitution notification has not fully processed. O nly the 
current [[collateral]] trade details have been entered. The system is waiting for the 
replacement [[collateral]] trade details to be entered.  
• Fully Allocated  – The substitution notification has fully processed. All related trade 
details have been updated and [[obligations]] have been generated for [[settlement]] 
purposes.  
• Deleted – Any substitution notification that has not processed, can be deleted. The 
delete action will cancel the request to substitute [[collateral]].  
• Future Pending – The substitution notification details have been entered for a future 
effective date, i.e., next business day.  
Substitutions Search Results Window  
SID The Substitution [[ID]] assigned to the Substitution Entry by [[GSD]].  
[[Member]] [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]] of the [[Member]] who initiated the Substitution . 
Repo [[Member]] [[ID]] For a Dealer Submitter (Repo Party), this is the 4- digit [[GSD]] [[Member]] [[ID]] of the [[Member]] who 
initiated the Substitution.  
2 

---

## Page 188

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 188 
Field/Item Name  Instructions/Descriptions 
Reverse [[Member]] [[ID]]  The 4-digit [[GSD]] [[Member]] [[ID]] associated with the contra -party for the substituted [[collateral]].   
Start Date This is the Repo Start Date of the trade for which [[collateral]] is being substituted . 
End Date This is the Repo End Date of the trade for which [[collateral]] is being substituted .  
Effective Business Date This is the effective date for the Substitution.  
Current [[CUSIP]] The [[CUSIP]] number of the current [[collateral]] to be replaced .  
Replacement [[CUSIP]] The [[CUSIP]] number of the replacement [[collateral]] item.  
Status (scroll to the right)  The Status of the Substitution item can be any of the following: 
• NP (Pending) 
• AA (Awaiting Allocation ) 
• FA (Fully Allocated ) 
• DEL (Deleted)   
• FP (Future Pending ) 
Table 39: Dealer Substitutions Management Screen Field Descriptions 
 
By clicking on the vertical ellipsis       icon, a user can access the available actions for a Substitution Entry. 
 
 
Figure 167: Dealer Substitutions Management Screen - Action Dropdown Menu 
Note:  
The Action Dropdown Menu allows the user to View, Modify or Delete a Substitution Entry that is in Awaiting Allocation, Not 
Processed/Pending or Future Pending Status.  
The Action Dropdown Menu only allows the user to View a Substitution Entry that is in Fully Allocated or Deleted Status.  


---

## Page 189

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 189 
To view the substitution, trade and obligation details on a Substitution Entry, the user must select View from 
the Action Dropdown Menu and a window similar to the one shown below will appear.   
 
Figure 168: Dealer Substitutions Management Screen – Substitution Details View 
 
Once the Substitution Entry details are visible, [[Locate]] the Substitution History, Trade Details and Obligation 
Details section at the bottom of the screen. This is where the user will find additional information on the 
Substitution Entry.  
 
Select the Additional Details/Expand View        icon to view the Substitution History, Trade Details and 
Obligation Details. 
 
Figure 169: Dealer Substitutions Management Screen – Substitution Details View – Additional Details 


---

## Page 190

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 190 
The screen will update as seen below.  
 
Figure 170: Additional Details – Substitution History, Trade Details and Obligation Details 
 
For additional instructions and field descriptions regarding the Dealer Substitutions Details View Screen, 
please refer to the below table. 
Field/Item Name  Instructions/Descriptions 
SID The Substitution [[ID]] Number assigned to the Substitution by [[GSD]].  
Product  The [[GSD]] Product for which the entry was submitted and processed through.  
Status  The Status of the Substitution item can be any of the following: 
• NP (Pending) 
• AA (Awaiting Allocation ) 
• FA (Fully Allocated ) 
• DEL (Deleted)   
• FP (Future Pending ) 
  Substitution Details 
[[Member]] [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]] of the [[Member]] who initiated the Substitution.  
Start Date This is the Repo Start Date of the trade for which [[collateral]] is being substituted .  
End Date This is the Repo End Date of the trade for which [[collateral]] is being substituted . 


---

## Page 191

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 191 
Field/Item Name  Instructions/Descriptions 
Effective Business Date This is the effective date for the Substitution.  
Repo [[Member]] [[ID]] For a Dealer Submitter (Repo Party), this is the 4- digit [[GSD]] [[Member]] [[ID]] of the [[Member]] who 
initiated the Substitution.  
Reverse [[Member]] [[ID]]  The 4-digit [[GSD]] [[Member]] [[ID]] associated with  the contra -party for the substituted [[collateral]].   
Submitted Business Date This is the submission date for the Substitution.  
Current [[collateral]] Details 
[[CUSIP]] The [[CUSIP]] number of the current [[collateral]] to be replaced.  
Par The par value of the current [[collateral]] to be replaced.  
Principal The principal  amount of the current [[collateral]] to be replaced.  
Repo Rate (%)  The current Repo Rate of the current [[collateral]] to be replaced . 
Replacement [[collateral]] Details 
[[CUSIP]] The [[CUSIP]] number of the replacement [[collateral]] . 
Par The par value of the replacement [[collateral]] . 
Principal The principal  amount of the replacement [[collateral]] . 
Repo Rate (%)  The Repo Rate of the replacement [[collateral]]  item. 
Substitution History  
Date The date for the memo of the selected Substitution . 
Time The time at which the memo for the  selected  Substitution was generated . 
Cmd The system command that created the memo.  
Memo The memo description for the select ed Substitution . 
User The user whose action generated the memo: either a [[Member]] [[ID]], User [[ID]]  or if it is System 
generated, then the appropr iate 4 -character system action is displayed in this field.  
Trade Details 
TID Seq# The Trade [[ID]] Sequence number.  
Note:  
The last number listed indicates the total number of trades modified by the Substitution.  
Repo / Revr The transaction type of the selected Substitution. Can be either Repo or Reverse Repo . 
TID The [[GSD]] assigned Trade [[ID]] of the trade modified by the processing of t he selected 
Substitutio n. 
Note:  
To view the specifics of a particular trade, click on the link for the TID to open the DVP Trade 
Detail View Screen. 

---

## Page 192

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 192 
Field/Item Name  Instructions/Descriptions 
[[Member]] [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]] for the selected Substitution.  
Contra [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]] associated with the contra -party of the selected Substitution.  
Long / Short  Indicates whether the modified trade for the selected Substitution is either a Long or a Short.  
[[CUSIP]] The 9-character [[CUSIP]] of the replacement [[collateral]] for the selected Substitution . 
Par The replacement par value for the selected Substitution.  
Amount The replacement principal amount for the selected Substitution.  
Current [[collateral]] Ref.  The Obligation [[ID]] ([[GSD]] reference number) of the current (old) [[collateral]] for the selected 
Substitution item.  
Replacement [[collateral]] 
Ref. 
The Obligation [[ID]] ([[GSD]] reference number) of the replacement (new) [[collateral]] for the 
selected Substitution item.  
Obligation Details – Original [[collateral]] 
Trans.  Indicates the type of transaction - either a Deliver (DLV) or Receive (RCV).  
Repo / Revr Indicates whether the transaction is a Repo or Reverse Repo transaction.  
[[settlement]] [[ID]] The [[GSD]] assigned Reference Number (Obligation [[ID]]) of the [[collateral]] transaction.  
[[GSD]] Acct. The 4-digit internal [[GSD]] Account [[ID]].  
[[Member]] [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]]. 
[[CUSIP]] The 9-character [[CUSIP]] of the current [[collateral]].  
[[settlement]] Par The [[settlement]] par value of the current [[collateral]].  
[[settlement]] Amount  The principal amount  of the current [[collateral]].  
TID The [[GSD]] assigned Trade [[ID]] of the current/replacement [[collateral]].  
Obligation Details – Replacement [[collateral]] 
Trans.  Indicates the type of transaction - either a Deliver (DLV) or Receive (RCV).  
Repo / Revr Indicates whether the transaction is a Repo or Reverse Repo transaction.  
[[settlement]] [[ID]] The [[GSD]] assigned Reference Number (Obligation [[ID]]) of the [[collateral]] transaction.  
[[GSD]] Acct.  The 4-digit internal [[GSD]] Account [[ID]].  
[[Member]] [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]]. 
[[CUSIP]] The 9-character [[CUSIP]] of the replacement [[collateral]].  
[[settlement]] Par The [[settlement]] par value of the replacement [[collateral]].  
[[settlement]] Amount  The principal amount  of the replacement [[collateral]].  
TID The [[GSD]] assigned Trade [[ID]] of the replacement [[collateral]].  
Table 40: Dealer Substitutions Management Screen - Substitution Details View Field Descriptions 
  

---

## Page 193

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 193 
Substitutions Management Examples for Dealer Submitter 
This section will provide examples of some certain actions a Dealer may take on a Substitution exception. 
How to Allocate Replacement [[collateral]] on a Substitution in Awaiting Allocation Status 
As previously stated in the section Substitution Entry for Dealer Submitter, if the user does not know the details 
of the Replacement [[collateral]] at the time of entry for the repo [[collateral]] substitution notification, then the user 
may leave the Replacement [[collateral]] fields blank and the system would allocate to a generic [[collateral]] 
[[CUSIP]]. 
 
Figure 171: Entry of Generic [[collateral]] [[CUSIP]] as Replacement [[collateral]] on Dealer Substitution Notification 
 
To allocate to the real replacement [[collateral]], the user would follow the below steps: 
Access the Dealer Substitution Management Screen and [[Locate]] the substitution notification that is awaiting 
allocation (AA).  
There are two ways to [[Locate]] the desired substitution notification. The user can either: 
1. Select the Awaiting Allocation link from the Substitutions Status Window which would update the 
Substitutions Search Results window so that it only displays items in the Awaiting Allocation status,  
OR 
2. View the list of substitution notifications in the Substitutions Search Results window and [[Locate]] the 
Replacement [[CUSIP]] column. Under that column [[Locate]] the generic [[CUSIP]] that the substitution was 
allocated to upon the submission of the original notification. 


---

## Page 194

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 194 
Then the user would click the vertical ellipsis       icon for the desired substitution to display the available 
actions in the Action dropdown menu. The user would select the Modify Action from the dropdown menu. 
 
 
Figure 172: Dealer Substitution Management Screen – Action Dropdown - Modify of Substitution Awaiting 
Allocation 
 
The below screen would appear. Note that the Comments fields and the Replacement [[collateral]] Details fields 
are editable, with the exception of the Repo Rate field.   
 
Figure 173: Substitution Details View - Awaiting Allocation Status 


---

## Page 195

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 195 
Enter the real replacement [[collateral]] information into the Replacement [[collateral]] Details field.  Then select the 
Modify button located at the upper right corner of the screen.  
 
Figure 174: Substitution Details View - Modify Replacement [[collateral]] Details 
 
A confirmation window will appear. Select Yes to proceed with the modification. Select No to go back to the 
substitution modification screen. 
 
Figure 175: Modify Substitution Confirmation Window 
 
 
 
 


---

## Page 196

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 196 
Once Yes is selected, the confirmation window will close. The modification has been accepted by the system. 
Close the substitution modification screen by clicking     . The Substitution Management Screen will appear 
again where the updates to the substitution will be displayed. 
 
Figure 176: Substitution Modification Accepted Successfully Message 
  


---

## Page 197

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 197 
Note that the Substitution Management Screen has been updated. The substitution is no longer Awaiting 
Allocation (AA). It is now Fully Allocated (FA).  
 
Figure 177: Dealer Substitution Management Screen - Modified Substitution Fully Allocated 
How to Delete a Pending Substitution 
The system will accept but not process (NP) a substitution notification for current [[collateral]] that cannot be 
validated by the system.  
 
Figure 178: Dealer Entry of Pending/Not Processed Substitution Notification  


---

## Page 198

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 198 
To Delete a substitution in Pending (Not Processed – NP) status, the user would follow the below steps: 
Access the Dealer Substitution Management Screen and [[Locate]] the substitution notification that is Pending 
(NP).  
There are two ways to [[Locate]] the desired substitution notification. The user can either: 
1. Select the Pending link from the Substitutions Status Window which would update the Substitutions Search 
Results window so that it only displays items in the Pending status,  
OR 
2. View the list of substitution notifications in the Substitutions Search Results window and [[Locate]] the Status 
column. Under the Status column, [[Locate]] the substitution with the NP status that also matches the details 
of the desired substitution. 
 
Note:  
The Status column by [[default]] is located to the far right of the screen. The user must scroll to the right to [[Locate]] the colum n.  
 
Then the user would click the vertical ellipsis       icon for the desired substitution to display the available 
actions in the Action dropdown menu as seen below. The user would select the Delete Action from the 
dropdown menu. 
 
 
Figure 179: Dealer Substitution Management Screen -  Action Dropdown  - Delete Pending Substitution 
Notification  
 
  


---

## Page 199

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 199 
The below screen would appear.  Then select the Delete button located at the upper right corner of the screen. 
 
Figure 180: Substitution Details View - Not Processed Status 
 
A confirmation window will appear. Select Yes to proceed with the deletion. Select No to go back to the 
substitution deletion screen. 
 
Figure 181: Modify Substitution Confirmation Window 
 
  


---

## Page 200

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 200 
Once Yes is selected, the confirmation window will close. The deletion has been accepted by the system. Now 
close the substitution deletion screen by clicking the     . The Substitution Management Screen will appear 
again where the updates to the substitution will be displayed. 
 
Figure 182: Substitution Deletion Accepted Successfully Message 
 
The Substitution Management Screen has been updated. The substitution is now Deleted (DEL). 
 
Figure 183: Dealer Substitution Management Screen - Substitution Deleted 


---

## Page 201

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 201 
Substitutions Search for [[Broker]] Submitter 
For users that have access provisioned for more than one [[Member]] account, such users can access the search 
feature located in the left [[Margin]] of the page. Users can select from the list of available accounts, the [[Member]] 
[[ID]] and Name they wish to query for. Then click the Search button to view the search results. 
 
Figure 184: [[Broker]] Substitutions Search Screen 
Substitutions Management for [[Broker]] Submitter 
The below screen allows users to manage their substitution entries. From this screen, users can view the 
status of their Substitutions, view related trade details and obligation details, make modifications and submit 
deletions on pending substitutions. The data on this screen is dynamically/automatically updated. 
 
Figure 185: [[Broker]] Substitutions Management Screen 
4 
3 

---

## Page 202

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 202 
The totals for all substitution activity for a given day are displayed in the lower right corner of the Substitutions  
Status window (see item labeled 3) on the page. Also displayed in the Substitutions Window are the  
Substitutions’ statuses (e.g., Pending, Awaiting Allocation, Fully Allocated, Deleted, and Future Pending). 
 
The All Items Status will display all active substitutions regardless of their status. To view the substitution 
activity for a selected status, click on its respective status link, i.e., to view only those substitutions with a status 
of Pending (see item labeled 3a), select the Pending link. 
 
  
Figure 186: [[Broker]] Substitutions Status Window 
 
The total number of substitutions entered on a given day is also displayed in the upper right corner of the 
Substitutions Search Results Window (see item labeled 4) on the page. Refer to the following page for how to 
access additional information or take an Action on a Substitution Entry. 
 
Figure 187: [[Broker]] Substitutions Search Results Window 
For additional instructions and field descriptions regarding the [[Broker]] Substitutions Management Screen, 
please refer to the below table. 
Note:  
The fields  desc ribed in the table below are organized in the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom  within each section).  
Field/Item Name  Instructions/Descriptions 
Substitution Status Window 
Status The Status of the Substitution item. It can be any of the following:          
• Pending – The substitution notification has not processed. The system is not able to 
process the substitution due to incorrect data entry. The substitution notification must be 
corrected via Mo dify Action  for the request to be accepted.  
3 
3a 
4 

---

## Page 203

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 203 
Field/Item Name  Instructions/Descriptions 
• Awaiting Allocation  – The substitution notification has not fully processed. Only the 
current [[collateral]] trade details have been entered. The system is waiting for the 
replacement [[collateral]] trade details to be entered.  
• Fully Allocated  – The substitution notification has fully processed. All related trade 
details have been updated and [[obligations]] have been generated for [[settlement]] 
purposes.  
• Deleted – Any substitution notification that has not processed, can be del eted. The 
delete action will cancel the request to substitute [[collateral]].  
• Future Pending – The substitution notification details have been entered for a future 
effective date, i.e., next business day.  
Substitutions Search Results Window  
SID The Substitution [[ID]] assigned to the Substitution Entry by [[GSD]].  
[[Member]] [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]] of the [[Member]] who initiated the Substitution.  
Repo [[Member]] [[ID]] For a [[Broker]]  Submitter, this is the  4-digit [[GSD]] [[Member]] [[ID]] associated with  the contra -party 
who will be delivering the replacement [[collateral]]/receiving current [[collateral]]  on the 
Substitution. 
Reverse [[Member]] [[ID]]  For a [[Broker]] Submitter, this is the 4- digit [[GSD]] [[Member]] [[ID]] associated with the contra -party 
who will be delivering the current [[collateral]] /receiving replacement [[collateral]]  on the 
Substitution.  
Start Date This is the Repo Start Date of the trade for which [[collateral]] is being substituted . 
End Date This is the Repo End Date of the trade for which [[collateral]] is being substituted .  
Effective Business Date This is the effective date for the Substitution .  
Current [[CUSIP]] The [[CUSIP]] number of the current [[collateral]] to be replaced .  
Replacement [[CUSIP]] The [[CUSIP]] number of the replacement [[collateral]] item.  
Status (scroll to the right)  The Status of the Substitution item can be any of the following: 
• NP (Pending) 
• AA (Awaiting Allocation ) 
• FA (Fully Allocated ) 
• DEL (Deleted)   
• FP (Future Pending ) 
Table 41: [[Broker]] Substitutions Management Screen Field Descriptions 
  

---

## Page 204

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 204 
By clicking on the vertical ellipsis       icon, a user can access the available actions for a Substitution Entry. 
 
 
Figure 188: [[Broker]] Substitutions Management Screen - Action Dropdown Menu 
Note:  
The Action Dropdown Menu allows the  user to View, Modify or Delete a Substitution Entry that is in Awaiting Allocation, Not 
Processed/Pending or Future Pending Status.  
The Action Dropdown Menu only allows the user to View a Substitution Entry that is in Fully Allocated or Deleted Status.  
  


---

## Page 205

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 205 
To view the substitution, trade and obligation details on a Substitution Entry, the user must select View from 
the Action Dropdown Menu and a window similar to the one shown below will appear.   
 
Figure 189: [[Broker]] Substitutions Management Screen - Substitution Details View 
 
Once the Substitution Entry details are visible, [[Locate]] the Substitution History, Trade Details and Obligation 
Details section at the bottom of the screen. This is where the user will find additional information on the 
Substitution Entry.  
Select the Additional Details/Expand View        icon to view the Substitution History, Trade Details and 
Obligation Details. 
 
Figure 190: [[Broker]] Substitutions Management Screen – Substitution Details View – Additional Details 


---

## Page 206

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 206 
The screen will update as seen below.  
 
Figure 191: Additional Details – Substitution History, Trade Details and Obligation Details 
 
For additional instructions and field descriptions regarding the [[Broker]] Substitutions Details View Screen, 
please refer to the below table. 
Field/Item Name  Instructions/Descriptions 
SID The Substitution [[ID]] Number assigned to the Substitution by [[GSD]].  
Product  The [[GSD]] Product for which the entry was submitted and processed through.  
Status  The Status of the Substitution item can be any of the following: 
• NP (Pending) 
• AA (Awaiting Allocation ) 
• FA (Fully Allocated ) 
• DEL (Deleted)   
• FP (Future Pending ) 
Substitution Details 
[[Member]] [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]] of the [[Member]] who initiated the Substitution.  
Start Date This is the Repo Start Date of the trade for which [[collateral]] is being substituted . 
End Date This is the Repo End Date of the trade for which [[collateral]] is being substituted .  


---

## Page 207

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 207 
Field/Item Name  Instructions/Descriptions 
Effective Business Date This is the effective date for the Substitution .  
Repo [[Member]] [[ID]] For a Dealer Submitter (Repo Party), this is the 4- digit [[GSD]] [[Member]] [[ID]] of the [[Member]] who 
initiated the Substitution.  
Reverse [[Member]] [[ID]]  The 4-digit [[GSD]] [[Member]] [[ID]] asso ciated with the contra -party for the substituted [[collateral]].   
Submitted Business Date This is the submission date for the Substitution .  
Current [[collateral]] Details 
[[CUSIP]] The [[CUSIP]] number of the current [[collateral]] to be replaced.  
Par The par value of the current [[collateral]] to be replaced.  
Principal The principal  amount of the current [[collateral]] to be replaced.  
Repo Rate (%)  The current Repo Rate of the current [[collateral]] to be replaced . 
Replacement [[collateral]] Details 
[[CUSIP]] The [[CUSIP]] number of the replacement [[collateral]] . 
Par The par value of the replacement [[collateral]] . 
Principal The principal  amount of the replacement [[collateral]] . 
Repo Rate (%)  The Repo Rate of the replacement [[collateral]]  item. 
Substitution History  
Date The date for the memo of the selected Substitution . 
Time The time at which the memo for the  selected  Substitution was generated . 
Cmd The system command that created the memo.  
Memo The memo description for the select ed Substitution . 
User The user whose action generated the memo: either a [[Member]] [[ID]], User [[ID]]  or if it is System 
generated, then the appropr iate 4 -character system action is displayed in this field.  
Trade Details 
TID Seq# The Trade [[ID]] Sequence number.  
Note:  
The last number lis ted indicates the total number of trades modified by the Substitution.  
Repo / Revr The transaction type of the selected Substitution. Can be either Repo or Reverse Repo . 
TID The [[GSD]] assigned Trade [[ID]] of the trade modified by the processing of the selected 
Substitution.  
Note:  
To view the specifics of a particular trade, click on the link for the TID to open the DVP Trade 
Detail View Screen.  

---

## Page 208

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 208 
Field/Item Name  Instructions/Descriptions 
[[Member]] [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]] for the selected Substitution.  
Contra [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]] asso ciated with the contra -party of the selected Substitution.  
Long / Short  Indicates whether the modified trade for the selected Substitution is either a Long or a Short.  
[[CUSIP]] The 9-character [[CUSIP]] of the replacement [[collateral]] for the selected Substitution . 
Par The replacement par value for the selected Substitution.  
Amount The replacement principal amount for the selected Substitution.  
Current [[collateral]] Ref.  The Obligation [[ID]] ([[GSD]] reference number) of the current (old) [[collateral]] for the selected 
Substitution item.  
Replacement [[collateral]] 
Ref. 
The Obligation [[ID]] ([[GSD]] reference number) of the replacement (new) [[collateral]] for the 
selected Substitution item.  
Obligation Details – Original [[collateral]] 
Trans.  Indicates the type of transaction - either a Deliver (DLV) or Receive (RCV).  
Repo / Revr Indicates whether the transaction is a Repo or Reverse Repo transaction.  
[[settlement]] [[ID]] The [[GSD]] assigned Reference Number (Obligation [[ID]]) of the [[collateral]] transaction.  
[[GSD]] Acct.  The 4-digit internal [[GSD]] Account [[ID]]. 
[[Member]] [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]]. 
[[CUSIP]] The 9-character [[CUSIP]] of the current [[collateral]].  
[[settlement]] Par The [[settlement]] par value of the current [[collateral]].  
[[settlement]] Amount  The principal amount  of the current [[collateral]].  
TID The [[GSD]] assigned Trade [[ID]] of the current/replacement [[collateral]].  
Obligation Details – Replacement [[collateral]] 
Trans.  Indicates the type of transaction - either a Deliver (DLV) or Receive (RCV).  
Repo / Revr Indicates whether the transaction is a Repo or Reverse Repo transaction.  
[[settlement]] [[ID]] The [[GSD]] assigned Reference Number (Obligation [[ID]]) of the [[collateral]] transaction.  
[[GSD]] Acct.  The 4-digit internal [[GSD]] Account [[ID]].  
[[Member]] [[ID]] The 4-digit [[GSD]] [[Member]] [[ID]]. 
[[CUSIP]] The 9-character [[CUSIP]] of the replacement [[collateral]].  
[[settlement]] Par The [[settlement]] par value of the replacement [[collateral]].  
[[settlement]] Amount  The principal amount  of the replacement [[collateral]].  
TID The [[GSD]] assigned Trade [[ID]] of the replacement [[collateral]].  
Table 42: [[Broker]] Substitutions Management Screen – Substitution Details View Field Descriptions 
 
 

---

## Page 209

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 209 
Substitutions Management Examples for [[Broker]] Submitter 
This section will provide examples of some certain actions a [[Broker]] may take on a Substitution exception. 
How to Allocate Replacement [[collateral]] on a Substitution in Awaiting Allocation Status 
As previously stated in the section Substitution Entry for [[Broker]] Submitter, if the user does not know the details 
of the Replacement [[collateral]] at the time of entry for the repo [[collateral]] substitution notification, then the user 
may leave the Replacement [[collateral]] fields blank and the system would allocate to a generic [[collateral]] 
[[CUSIP]]. 
 
Figure 192: Entry of Generic [[collateral]] [[CUSIP]] as Replacement [[collateral]] on [[Broker]] Substitution Notification 
To allocate to the real replacement [[collateral]], the user would follow the below steps: 
Access the [[Broker]] Substitution Management Screen and [[Locate]] the substitution notification that is awaiting 
allocation (AA).  
There are two ways to [[Locate]] the desired substitution notification. The user can either: 
1. Select the Awaiting Allocation link from the Substitutions Status Window which would update the 
Substitutions Search Results window so that it only displays items in the Awaiting Allocation status,  
OR 
2. View the list of substitution notifications in the Substitutions Search Results window and [[Locate]] the 
Replacement [[CUSIP]] column. Under that column [[Locate]] the generic [[CUSIP]] that the substitution was 
allocated to upon the submission of the original notification. 
 


---

## Page 210

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 210 
Then the user would click the vertical ellipsis       icon for the desired substitution to display the available 
actions in the Action dropdown menu. The user would select the Modify Action from the dropdown menu. 
 
 
Figure 193: [[Broker]] Substitution Management Screen – Action Dropdown - Modify of Substitution Awaiting 
Allocation 


---

## Page 211

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 211 
The below screen would appear. Note that the Comments fields and the Replacement [[collateral]] Details fields 
are editable, with the exception of the Repo Rate field.   
 
 
Figure 194: Substitution Details View - Awaiting Allocation Status 
 
Enter the real replacement [[collateral]] information into the Replacement [[collateral]] Details field.  Then select the 
Modif y button located at the upper right corner of the screen. 


---

## Page 212

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 212 
 
Figure 195: Substitution Details View - Modify Replacement [[collateral]] Details 
 
A confirmation window will appear. Select Yes to proceed with the modification. Select No to go back to the 
substitution modification screen. 
 
Figure 196: Modify Substitution Confirmation Window 
 
 
 


---

## Page 213

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 213 
Once Yes is selected, the confirmation window will close. The modification has been accepted by the system. 
Close the substitution modification screen by clicking     . The Substitution Management Screen will appear 
again where the updates to the substitution will be displayed. 
 
Figure 197: Substitution Modification Accepted Successfully Message 
 
  


---

## Page 214

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 214 
The Substitution Management Screen has been updated. The substitution is now Fully Allocated (FA).  
 
Figure 198: [[Broker]] Substitution Management Screen - Substitution Fully Allocated 
How to Delete a Pending Substitution 
The system will accept but not process (NP) a substitution notification for current [[collateral]] that cannot be 
validated by the system.  
 
Figure 199: [[Broker]] Entry of Pending/Not Processed Substitution Notification 


---

## Page 215

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 215 
To Delete a substitution in Pending (Not Process – NP) status, the user would follow the below steps: 
Access the [[Broker]] Substitution Management Screen and [[Locate]] the substitution notification that is Pending 
(NP).  
There are two ways to [[Locate]] the desired substitution notification. The user can either: 
1. Select the Pending link from the Substitutions Status Window which would update the Substitutions Search 
Results window so that it only displays items in the Pending status,  
OR 
2. View the list of substitution notifications in the Substitutions Search Results window and [[Locate]] the Status 
column. Under the Status column, [[Locate]] the substitution with the NP status that also matches the details 
of the desired substitution. 
 
Note:  
The Status column by [[default]] is located to the far right of the screen. The user must scroll to the right to [[Locate]] the column.  
 
Then the user would click the vertical ellipsis       icon for the desired substitution to display the available 
actions in the Action dropdown menu as seen below. The user would select the Delete Action from the 
dropdown menu. 
 
Figure 200: [[Broker]] Substitution Management Screen -  Action Dropdown  - Delete Pending Substitution 
Notification 
 
 


---

## Page 216

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 216 
The below screen would appear. Then select the Delete button located at the upper right corner of the screen. 
 
Figure 201: Substitution Details View - Not Processed / Pending Status 
 
A confirmation window will appear. Select Yes to proceed with the deletion. Select No to go back to the 
substitution deletion screen. 
 
Figure 202: Modify Substitution Confirmation Window 
 
 


---

## Page 217

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 217 
Once Yes is selected, the confirmation window will close. The deletion has been accepted by the system. 
Close the substitution deletion screen by clicking     . The Substitution Management Screen will appear again 
where the updates to the substitution will be displayed. 
 
Figure 203: Substitution Deletion Accepted Successfully Message 
 
 
  


---

## Page 218

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Substitutions 218 
The Substitution Management Screen has been updated. The substitution is now Deleted (DEL).  
 
Figure 204: [[Broker]] Substitution Management Screen - Substitution Deleted 
 


---

## Page 219

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 219 
TOOLS 
The Tools dropdown menu allows a user to access certain reference data relating to [[GSD]] eligible [[securities]], 
[[GSD]] Product Types and Members Contact Information. Also available from the Tools dropdown menu are the 
CCLF Obligation Management screens (Test and Real Event) and the DVP Bulk Trade Upload. 
 
Figure 205: Tools Dropdown Menu 
Tools > Security Search 
From the Tools > Security Search dropdown menu selection, users can search for information on one or more 
DVP CUSIPs ([[GSD]] Eligible [[securities]]) based on selected search criteria or identify which security shells are 
eligible for trading in the GCF Repo Service or CCIT Service. 
 
Figure 206: Tools > Security Search 


---

## Page 220

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 220 
DVP [[securities]] 
To search for information on one or more DVP CUSIPs ([[GSD]] Eligible [[securities]]) based on the selected search 
criteria, access the Security Search function by selecting Tools > Security Search > DVP. 
 
Figure 207: Tools > Security Search > DVP 
 
The below screen will appear. Enter criteria to narrow your search results. Then click the Search button. 
 
Figure 208: DVP [[securities]] Search screen 


---

## Page 221

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 221 
The DVP [[securities]] Search Screen contains the fields described in the following table. 
Note:  
The fields  described in the table below are organized in the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom  within each section).  
Field/Item Name Instructions/Descriptions 
[[CUSIP]] Enter the [[CUSIP]] for the desired Security search.  This field accepts either the whole [[CUSIP]] 
(9-character maximum) or a partial [[CUSIP]] .  
Note:  
Use the wildcard function if entering a partial [[CUSIP]]  number. The wildcard character (*) is not 
needed , but does require a minimum of 4- characters to be entered into the [[CUSIP]] field.  For 
example, if 912796 is entered into the [[CUSIP]] field, then the search results will display all 
records for a [[CUSIP]] beginning with 912796.  
Short Name Enter the abbreviated name of the Security that is associated with the [[CUSIP]].  
Product Type  The Product association created when the new [[CUSIP]] was added.  Field defaults to ALL, but 
to narrow down search criteria, s elect one of the following Product Types:  AGENCY, 
DAGENC, FUNDS, NONNET, REPTRD, RTRUST, SAGENC,  SPONGC, STRIPS, TBILL, 
TBOND, TFRNA, TIPSBD, TIPSNT, TIPST or TNOTE.  
Coupons Per Year Enter the number of coupons issued per year for the Security.  
Payment Day  Enter the day of the month that the coupon amount is to be paid out.  
Coupon Status  Field defaults to ALL, but to narrow down search criteria, s elect one of the following coupon 
statuses for the Security: Real or Assumed.  
 Current Price  Enter the current price for the Security.  
Coupon %  Enter the coupon rate for the Security .  
Priced By Field defaults to ALL, but to narrow down search criteria, s elect one of the following options  
to indicate who priced the Security : Vendor, Average Price, or [[default]] Price.  
Forward Netting Indicate s whether the [[CUSIP]] is Forward Netting. Enter ‘Y’ for yes and ‘N’ for no.  
Netting Eligible  Indicate s whether the [[CUSIP]] can be netted. Enter ‘Y’ for yes and ‘N’ for no.  
Floating Coupon Basis  Indicates the Product type used to derive the index rate (along with the spread) to calculate 
the coupon rate.  Currently TBILL is the only selectable [[Option]] for this field. 
Yield to Price Indicate s whether the [[CUSIP]] is marked as Yield to Price. Enter ‘Y’ for yes and ‘N’ for no.  
Delay Payment Indicates a security for which the coupon and/or  principal payment has been delayed 
beyond the original coupon payment/maturity date. Enter ‘Y’ for yes and ‘N’ for no.  
Coupon Reset Frequency  Indicates the frequency at  which the Coupon is reset.  Field defaults to ALL, but to narrow 
down search criteria, select one of the follow options to indicate frequency: Quarterly, 
Annual, Bi-Weekly, Monthly, Semi -Annual, Weekly, or Daily . 
Available for Entry  Indicates the enablement (’Y’) or disablement (‘N ’) of the [[CUSIP]] for trade entry. 
Auction Date Enter the auction date for the [[CUSIP]]. Format = mm/dd/ yyyy. 

---

## Page 222

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 222 
Field/Item Name Instructions/Descriptions 
Dated Date Enter the date from which the [[CUSIP]] begins to accrue interest. Format = mm/dd/ yyyy. 
Last Priced Date Enter the date that the [[CUSIP]] was last priced . Format = mm/dd/yyyy. 
Issue Date Enter the issue date of the [[CUSIP]]. Format = mm/dd/ yyyy. 
Reissue Date Enter the reissue date of the [[CUSIP]]. Format = mm/dd/ yyyy. 
Maturity Date Enter the maturity date of the [[CUSIP]] . Format = mm/dd/ yyyy. 
Reset Returns the fields on current screen to the original [[default]] values.  
Search Equivalent to a Submit button.  Click to submit the data you entered on the Search  screen to 
search for the records that fit the entered  search criteria.  
Comparison Operator  Select one of the comparison operators as it refers to the field: =, <>, <, <=, >, >=.  
Table 43: DVP [[securities]] Search Screen Field Descriptions 
 
Once search criteria is entered and the Search button is selected, the below screen will appear. This screen 
displays search results based on the entered search criteria. From this screen the user can view available 
info rmation on a particular security or a set of of [[securities]]. 
 
Figure 209: DVP [[securities]] Search Results Screen 
Note: 
The DVP [[securities]] Search Results can be downloaded by using the download button  or printed by using the print 
function within the web browser. Also, the user may change the way the results are displayed by using the advanced query 
functions, column sor t er, column filter, etc.   
Such information may include but is not limited to coupon status, netting eligibility, coupon payment day, 
current system price, and coupon frequency.  


---

## Page 223

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 223 
The DVP [[securities]] Search Results Screen contains the fields described in the following table. 
Note:  
The fields  described in the table below are organized in the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom  within each section).  
 Item Description 
[[CUSIP]] Committee on Uniform [[securities]] Identification Procedures ([[CUSIP]]) is  the nine -character 
alphanumeric code that identifies a North American financial security for the purposes of 
facilitating clearing and [[settlement]] of trades.   
Description  The information created that will be displayed on screens containing the [[CUSIP]]  Description.  
Coupon The coupon rate for the Security.  
Maturity Date The current  maturity date of the [[CUSIP]].  
Original Maturity Date The original  maturity date of the [[CUSIP]].  
Last Priced Date The date that the [[CUSIP]] was last priced . 
Priced By Indicates who priced the Securit y. 
Last Price The last price for the Security. 
Netting Eligible  Indicate s whether the [[CUSIP]] can be netted.  
Delay Payment Indicates coupon and/or principal payment has been delayed beyond the original coupon 
payment/ maturity date. 
Table 44: DVP [[securities]] Search Results Screen Field Descriptions 
 
To view details on a particular security, click the desired security listed under the [[CUSIP]] column. Each listed 
DVP [[CUSIP]] is a hyperlink to that security’s reference data. 
 
Figure 210: Hyperlink to Detailed View of selected DVP [[CUSIP]]  
 
  


---

## Page 224

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 224 
Once the hyperlink of a DVP [[CUSIP]] is selected, a new window will appear as seen below. This screen will 
display all of the available details for the particular DVP [[CUSIP]] selected. 
 
Figure 211: Detail View of selected DVP [[CUSIP]] 
Note: 
The Detail View of the selected DVP [[CUSIP]] can be printed by using the print function within the web browser.   
  


---

## Page 225

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 225 
The DVP [[CUSIP]] Detail View contains the fields described in the following table. 
Note:  
The fields  described in the table below are organized in the same order as they appear on the screen (i.e., moving from left 
to right and top to bottom  within each section).  
Field/Item Name  Instructions/Descriptions 
Description  The information created that will be displayed on the screen . Contains the 
[[CUSIP]]/Description  for the Security. 
Security Info  
 Short Name The abbreviated name of the Security that is associated with the [[CUSIP]].  The system uses 
the [[CUSIP]] for the Security as a [[default]] .  
Product Type  The Product association created when the new [[CUSIP]] was added.   
Yield to Price  Indicate s whether the [[CUSIP]] is marked as Yield to Price.  
Coupon The coupon rate for the Security .  
CPI Index  Indicates if the Security is CPI Indexed (rate calculated from Consumer Price Index).  
Netting Eligible  Indicate s whether the [[CUSIP]] can be netted.  
Coupon Status  The coupon status for the Security.  
Delay Payment Indicates coupon and/or principal payment has been delayed beyond the original  coupon 
payment/ maturity date. 
Available for Entry  Indicates the enablement or disablement of the [[CUSIP]] for trade entry.  
Forward Netting Indicate s whether the [[CUSIP]] is Forward Netting.  
Date Info  
Maturity Date The maturity date of the [[CUSIP]] .  
Issue Date The issue date of the [[CUSIP]].  
Auction Date The auction date for the [[CUSIP]].  
Dated Date The date from which the [[CUSIP]]  begins to accrue interest.  
Orig. Maturity Date  The original  maturity date of the [[CUSIP]].  
Reissue Date The reissue date of the [[CUSIP]]. 
Orig. Setup Date The “into -service” date of the [[CUSIP]]. 
Pricing 
Current Price  The current price for the Security.  
Priced By Ind icates who priced the Security.  
Last Priced Date The date that the [[CUSIP]] was last priced . 
  Denomination  

---

## Page 226

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 226 
Field/Item Name  Instructions/Descriptions 
Minimum The minimum denomination par for the  Security. 
Divisor  The [[default]] divisor of the Security.  
Multiple  The multiple denomination par for the Security.  
Auction Size The auction size of the selected Security.  
Interest Accrual Info  
Coupons Per Year The number of coupons paid per year for the Security.  
Days in Month The number of days in the relevant month.  Values can be either 30 or ACT (ACT = Actual = 
e.g., 31 for May and 30 for April).  
Payment Day  The day of the month that the coupon amount is to be paid out.  
Days in Year The number of days in the relevant Year. Values can be either 360, 365, or ACT (where 
ACT = Actual = 365 or 366, depending on the year).  
First Payment The date of the first coupon payment for  the Security. 
Last Payment The date of the last coupon payment for  the Security. 
Floating Rate 
Coupon Reset Frequency  Indicates the frequency at  which the Coupon is reset.  
Coupon Reset Date The date the Coupon is reset.  
Floating Coupon Basis  Indicates the Product type used to derive the index rate (along with the spread) to calculate 
the coupon rate.  
Coupon Basis Spread The rate applied to the interest index rate.  
Last Reset Date The date of the last Coupon reset.  
Table 45: DVP [[CUSIP]] Detail View Field Descriptions 
  

---

## Page 227

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 227 
GCF [[securities]] 
To identify which security shells are eligible for trading in the GCF Repo Service or CCIT Service access the 
Security Search function by selecting Tools > Security Search > GCF. 
 
Figure 212: Tools > Security Search > GCF 
 
The below screen will appear. The GCF [[securities]] are listed in alphabetical order by Short Name. 
 
Figure 213: GCF [[securities]] Search Results Screen 
  


---

## Page 228

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 228 
The GCF [[securities]] Search Results screen contains the fields described in the following table. 
Note:  
The fields  described in the table below are organized in the same order as they appear on the screen (i.e., left to right 
within each section).  
Item Description 
[[CUSIP]] The [[CUSIP]] identifier created to represent a general [[collateral]] security shell . 
Description  The inf ormation created that will be displayed on screens containing the [[CUSIP]]/Description.  
Short Name The short name created by which the [[CUSIP]] is known.  Values can be AGCY, FFARM, 
FFFIX, GNARM, GNMA, STRP, TIPS, TU10 or TU30 . 
Product  The Product/[[CUSIP]] association created when the new [[CUSIP]] was added. Values can be  
AGCY, FFARM, FFFIX, GNARM, GNMA, STRP, US TIPS, T R10 or TR30. 
Minimum Denomination  The minimum denomination that may be traded for the [[CUSIP]].  
Multiple Denomination  The denomination multiple that may be traded for the [[CUSIP]].  
Trading Enabled  Indicates the enablement (’Y’) or disablement (‘N’) of the [[CUSIP]] for trade entry.  
Table 46: GCF [[securities]] Search Results Screen Field Descriptions 
  

---

## Page 229

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 229 
Tools > Product Search  
From the Tools > Product Search dropdown menu selection, users can view a list of all [[GSD]] product types for 
DVP and GCF/CCIT. 
 
Figure 214: Tools > Product Search 
DVP Product Types 
To view the list of DVP Product Types, access the Security Search function by selecting Tools > Product 
Search > DVP. 
 
Figure 215: Tools > Product Search > DVP 


---

## Page 230

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 230 
The below screen will appear. From this screen the user can view available information for each DVP Product.  
 
Figure 216: DVP Product Types Search Results Screen 
Note: 
The DVP Product Types Search Results screen can be downloaded by using the download button  or printed by using 
the print function within the web browser.  
The DVP Product Types Search Results screen contains the fields described in the following table. 
Item Description 
Type  Indicates the Product Type . Values can be AGENCY, DAGENC, FUNDS, NONNE T, 
REPTRD, RTRUST, SAGENC, SPONGC, STRIPS, TBILL, TBOND, TFRNA, TIPSBD, 
TIPSNT, TIPST or TNOTE  
Description  The description of the selected DVP P roduct Type.  
[[default]] Pricing Method  The [[default]] price type of the selected DVP P roduct.  
Table 47: DVP Product Types Search Results Screen Field Descriptions 
 
To view information on a particular Product Type, click the Product listed under the Type column. Each listed 
DVP Product is a hyperlink to that products’ d ata. 
  
Figure 217: Hyperlink to Detailed View of selected DVP Product Type 


---

## Page 231

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 231 
Once the hyperlink of a DVP Product is selected, a new window will appear as seen below. This screen will 
display all of the available details for the particular DVP Product Type selected. 
 
 
Figure 218: Detailed View of DVP Product Type 
 
The DVP Product Type Detail View contains the fields described in the following table. 
Note:  
The fields  described in the table below are organized in the same order as they appear on the screen (i.e., moving from top 
to bottom within each section).  
Item Description 
[[default]] Pricing  Method The [[default]] price type of the selected DVP Product.  
Repo Net Eligible  Indicates if the selected DVP P roduct is Repo Net ting Eligible . Can be either ‘Y’ for yes or 
‘N’ for no.  
Yield Convert  Indicates whether the yield is converted on the selected DVP Product. Can be either ‘Y’ for 
yes or ‘N’ for no.  
Cash Net Eligible  Indicates if the selected DVP Product is  Cash Netting Eligible . Can be either ‘Y’ for yes or 
‘N’ for no.  
Day Count Method The number of days in a year, used to compute accrued interest  for the selected  DVP 
Product.  
Max Delivery Size The maximum delivery size for the selected  DVP Product.  
Fed Delivery Size The maximum Fed delivery  size for the selected DVP Product.  
Max Trade Size The maximum trade size for the selected  DVP Product.  
Max Lock -in The maximum trade size for a locked -in trade submission for the selected DVP Product.  
Coupons Per Year The number of coupons that can be paid  per year for the selected DVP Product.  
Table 48: DVP Product Type Detail View Field Descriptions  


---

## Page 232

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 232 
GCF Product Types  
To view the list of GCF Product Types, access the Security Search function by selecting Tools > Product 
Search > GCF. 
 
Figure 219: Tools > Product Search > GCF 
 
The below screen will appear. Users can view available information for each GCF Product Type. 
 
Figure 220: GCF Product Types Search Results Screen 
Note: 
The GCF Product Types Search Results screen can be downloaded by using the download button  or printed by using 
the print function within the web browser.  
  


---

## Page 233

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 233 
The GCF Product Types Search Results contains the fields described in the following table. 
Item Description 
Type  Indicates the Product Type . 
Description  The description of the GCF  Product Type.  
Maximum Web Trade Size The maximum trade size submitted via the web for the selected GCF  Product.  
Maximum IM Trade Size  The maximum trade size submitted via IM/MQ for the selected GCF  Product.  
Table 49: GCF Product Types Search Results Screen Field Descriptions 
  

---

## Page 234

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 234 
Tools > Contact Management 
The Contact List is a resource that Members can utilize in order to retrieve contact information for other [[FICC]] 
[[GSD]] Members. Each [[Member]] is responsible for maintaining their firm’s contact information within the Contact 
List tool. Therefore, the tool is also used by each firm to maintain their own contact information. On a regular 
basis each firm should review their firm’s contact information within the Contact List tool and update the 
information as necessary.  
Accessing the [[FICC]] [[GSD]] Contact List  
Using the navigation toolbar, select Tools dropdown menu as seen below. Hover over Tools > Contact 
Management to view your available options.   
 
Figure 221: Tools > Contact Management  
View All [[GSD]] Contacts 
To view all [[GSD]] contacts listed in [[GSD]] RTTM Web, Select Tools > Contact Management > View ALL. 
 
Figure 222:Tools > Contact Management > View All  
Note:  
Super Access Coordinators and other users that have DVP – Update and/or GCF – Update Roles provisioned can make 
Contact List modifications. 


---

## Page 235

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 235 
Once the user selects View ALL from the dropdown menu, the below screen will appear. This screen displays 
all available contacts for [[GSD]] Members. 
 
Figure 223: View All [[GSD]] Contacts Screen 
Note:  
This Contact List is maintained by the membership and not [[FICC]].  
Adding, Updating or Deleting Contact Information 
Adding New [[GSD]] Contact Information 
To add a new contact to the Contact List in [[GSD]] RTTM Web, select Tools > Contact Management > 
Entry/Update/Delete. 
 
Figure 224: Tools > Contact Management > Entry/Update/Delete 
  


---

## Page 236

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 236 
Once the user selects Entry/Update/Delete from the dropdown menu, the below screen will appear. This 
screen will allow a user to add new contact information to the list of available contacts of [[GSD]] Members. To 
add a new contact, click + Add Row. 
 
Figure 225: Add New Contact Information 
Note:  
If the user’s login credentials allows for them to access more than one (1) [[GSD]] account, the user  will need to select from 
the [[Member]] [[ID]] dropdown list the account that the new contact information will be listed under.  
Once + Add Row is selected, the screen will update and the Contact Name, Email and Phone Number fields 
will become editable.  
 
Figure 226: Add New Row 
Note:  
The Contact Name is a required field.  


---

## Page 237

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 237 
Next, the user should enter the relevant information in the available fields as seen on the screen below. Once 
the user has entered the relevant information into the fields, click the Save icon.  
Note:  
When the user hovers over  the Save icon  with their mouse , the “Add Contact” label will appear.  
 
Figure 227: Enter Contact Information 
 
Once the entry has been saved, the screen will update as seen below. 
 
Figure 228: Success message – Contact Added 
 
The user can repeat the above steps to add additional contacts to the Contact List.  


---

## Page 238

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 238 
Edit Existing [[GSD]] Contact Information 
To edit an existing contact in the Contact List, select Tools > Contact Management > Entry/Update/Delete. 
 
 
Figure 229: Tools > Contact Management > Entry/Update/Delete 
 
Once the user selects Entry/Update/Delete from the dropdown menu, the below screen will appear. This 
screen will allow a user to modify an existing contact. To modify the contact information for a particular 
name/group, click the Edit icon on the screen that is in line with the contact information that needs to be 
modified.  
Note:  
When the user hovers over  the Edit icon  with their mouse , the “Edit Contact” label will appear.  
 
Figure 230: Edit Icon 
Note:  
If the user’s login credentials allows for the user  to access more  than one (1) [[GSD]] account, then the user  will need to select 
from the [[Member]] [[ID]] dropdown list which account’s contact infor mation will need to be modified.  


---

## Page 239

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 239 
Once the Edit icon is selected, the screen will update and the Contact Name, Email and Phone Number fields 
will become editable.  
 
Figure 231: Modify Existing Contact Information 
Note:  
The Contact Name is a required field.  
Next, update the relevant information in the available fields as seen on the screen below.  
In the example shown below, the Phone Number was updated. Once the relevant information has been updated, 
click the Save icon.  
Note:  
When the user hovers over  the Save icon  with their mouse , the “Update Contact” label will appear.  
 
Figure 232: Update Contact Information 
 
  


---

## Page 240

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 240 
Once the update has been saved, the screen will update as seen below. 
 
Figure 233: Success message – Contact Modified 
Delete Existing [[GSD]] Contact Information 
To delete an existing contact in the Contact List, select Tools > Contact Management > Entry/Update/Delete. 
 
 
Figure 234: Tools > Contact Management > Entry/Update/Delete 
  


---

## Page 241

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 241 
Once the user selects Entry/Update/Delete from the dropdown menu, the below screen will appear. This screen 
allows the user to delete an existing contact. To delete the contact information for a particular name/group, click 
the Delete icon on the screen that is in line with the contact information that needs to be deleted.  
Note:  
When the user hovers over the Delete icon  with their mouse , the “Delete Contact” label will appear.  
 
Figure 235: Delete Icon 
Note:  
If your login credentials allows for you to access more than one (1) [[GSD]] account, you will need to select from the [[Member]] 
[[ID]] dropdown list which account you will be deleting contact information from.  
Once the Delete icon is selected, the screen will update as seen below. 
 
Figure 236: Success message – Contact Deleted 
Who to Contact for Issues 
At any time should you encounter a technical issue, please contact the [[GSD]] Operations team at 
(212) 855-7600 or gsd_ops@[[DTCC]].com.  


---

## Page 242

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 242 
Tools > CCLF 
All Netting Members have access to the “CCLF [[obligations]] Management Screen.” For each Netting [[Member]], 
the screen will reflect (1) Deliver [[obligations]] that are destined for the hypothetical Defaulting [[Member]] for the 
[[settlement]] date of the CCLF test date or (2) have no Deliver [[obligations]] that are destined for the hypothetical 
Defaulting [[Member]].  
Accessing the CCLF [[obligations]] Management screen 
To access the CCLF [[obligations]] Management Screen on [[GSD]] RTTM Web for a CCLF Test, select Tools from 
the dropdown menu bar at the top of the application, then select CCLF > Test Event.  
 
Figure 237: Tools > CCLF > (Real Event or Test Event, as applicable) 
Note: 
To access the CCLF [[obligations]] Management Screen  if a CCLF Event is declared, select Tools from the dropdown menu 
bar at the top of the application, then selec t CCLF > Real Event. 
  


---

## Page 243

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 243 
Overview of the CCLF [[obligations]] Management Screen 
Upon navigating to the CCLF [[obligations]] Management screen the below will appear. In upcoming sections, we 
will review the different sections of the CCLF [[obligations]] Management screen.   
 
Figure 238: CCLF [[obligations]] Management Screen 
 
Each number on the screen above represents an area within the CCLF [[obligations]] Management screen that 
will be discussed in this guide. 
1. [[Member]] Reference Information 
2. Potential Financing Amount 
3. Actual Financing Amount 
4. System Information 
5. CCLF Reference Rates 
6. CCLF [[Haircut]] and Repo Amount 
7. Redistribution Repo 
8. [[obligations]] Management 
 
  
1 
2 
3 
4 
5 
6 
8 
7 
4 

---

## Page 244

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 244 
[[Member]] Information 
This page will provide the descriptions of fields within the [[Member]] Information section of the CCLF [[obligations]] 
Management screen. 
 
Figure 239: CCLF [[obligations]] Management Screen - [[Member]] Information 
• [[Member]] [[ID]] – [[GSD]] [[Member]] Identification Number. 
• CCLF Cap – Netting [[Member]]'s Individual Total Amount based on the last CCLF reset. This field is marked 
as “Aggregate Total Amount” on the daily “[[GSD]] Capped Contingency [[Liquidity]] Facility [[participant]] Report.” 
If a Netting [[Member]] has a value other than zero (0) in either the “Potential GCF Financing Amount” or 
the “Potential DVP Financing Amount” then that Netting [[Member]] is considered a “Direct Affected 
[[Member]]”, per the [[GSD]] Rulebook. 
  


---

## Page 245

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 245 
Potential Financing Amount 
This page will provide the descriptions of fields within the Potential Financing Amount section of the CCLF 
[[obligations]] Management screen.  
 
Figure 240: CCLF [[obligations]] Management Screen - Potential Financing Amount 
• Potential GCF Financing Amount – The total dollar amount of a Direct Affected [[Member]]’s GCF 
[[obligations]] destined for the Defaulting [[Member]].  
• Potential DVP Financing Amount – The total dollar amount of a Direct Affected [[Member]]'s DVP 
[[obligations]] destined for the Defaulting [[Member]].  
• Potential Total Financing Amount – The total potential dollar amount (up to a Direct Affected [[Member]]’s 
CCLF Cap) of CCLF Transactions which that Direct Affected [[Member]] may be asked to enter into with 
[[FICC]]. 
• Potential Under CCLF Cap – The difference between a Direct Affected [[Member]]'s CCLF Cap and the 
sum of that Direct Affected [[Member]]’s “Potential GCF Financing Amount” and “Potential DVP 
Financing Amount.” If this value is negative, then the Direct Affected [[Member]]’s “Potential Financing 
Amount” has exceeded their CCLF Cap.  
  


---

## Page 246

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 246 
Actual Financing Amount 
This page will provide the descriptions of fields within the Actual Financing Amount section of the CCLF 
[[obligations]] Management screen. 
 
Figure 241: CCLF [[obligations]] Management Screen - Actual Financing Amount  
• Actual GCF Financing Amount – The total dollar amount of a Direct Affected [[Member]]’s Financing 
Amount in GCF. This value is the same as the “Potential GCF Financing Amount.” 
• Actual DVP Financing Amount – The value of a Direct Affected [[Member]]’s DVP [[obligations]] which are 
marked as “Available For Delivery” on the CCLF [[obligations]] Management screen. If the sum of a Direct 
Affected [[Member]]’s “Actual GCF Financing Amount” and their “Actual DVP Financing Amount” exceeds 
their CCLF Cap, then [[GSD]] will notify that [[Member]] which of the DVP [[obligations]] (destined for a Defaulting 
[[Member]]) they may deliver to [[GSD]]. Following this notification, the value of the “Actual DVP Financing 
Amount” field will be reduced by the dollar value in the “Approved for Delivery Value” field.  
• Actual CCLF Financing Amount – This field displays the dollar amount of CCLF Transactions that a 
Direct Affected [[Member]] will be asked to enter into with [[FICC]]. The value of this field is calculated as the 
sum of the “Actual GCF Financing Amount” field and the “Actual DVP Financing Amount” field. 
• Approved for Delivery Value – This field displays the dollar amount of a Direct Affected [[Member]]’s 
Financed [[securities]] which that [[Member]] will be allowed to deliver to [[GSD]] if the [[Member]] is over their CCLF 
Cap. 
• Actual Under CCLF Cap – The difference between a Direct Affected [[Member]]’s “CCLF Cap” and their 
“Actual CCLF Financing Amount.” A negative value means the [[Member]] is over their CCLF Cap. 


---

## Page 247

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 247 
System Information 
This page will provide the descriptions of fields within the System Information section of the CCLF [[obligations]] 
Management screen. 
 
Figure 242: CCLF [[obligations]] Management Screen - System Information 
• [[settlement]] Date – The [[settlement]] date of the [[obligations]] displayed on the screen. 
• Last Submission Status – This field displays the last date and time stamp a Direct Affected [[Member]] 
submitted its entries for Deliver [[obligations]] that are “Available For Delivery”. 
• Admin Confirmation Status – Once a Direct Affected [[Member]] submits its marked selection of Deliver 
[[obligations]] “Available For Delivery”, [[GSD]] will send a confirmation reflecting the marked Deliver 
[[obligations]] as well as the interest rate and haircuts applicable to the CCLF Transactions. This 
confirmation will display “Last Confirmed" status and a time stamp once [[GSD]] processes the [[Member]]’s 
submission. 
 
 
  


---

## Page 248

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 248 
CCLF Reference Rates 
This page will provide the descriptions of fields within the CCLF Reference Rates section of the CCLF 
[[obligations]] Management screen.  
 
Figure 243: CCLF [[obligations]] Management Screen - CCLF Reference Rates  
• CCLF TR Repo Rate – This field displays the [[GSD]]-determined overnight rate used to calculate CCLF 
Repo Interest on CCLF Transactions executed in U.S. government [[Bonds]] and agency [[Bonds]]. 
• CCLF MBS Repo Rate – This field displays the [[GSD]]-determined overnight rate used to calculate CCLF 
Repo Interest on CCLF Transactions executed in mortgage‐backed [[securities]]. 
• CCLF TR Repo [[Haircut]] – This field displays the [[Haircut]] that clients will receive when they enter into 
CCLF Transactions executed in U.S. government [[Bonds]] and agency [[Bonds]]. 
• CCLF MBS Repo [[Haircut]] – This field displays the [[Haircut]] that clients will receive when they enter into 
CCLF Transactions executed in mortgage‐backed [[securities]]. 
 
 
 
  


---

## Page 249

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 249 
CCLF [[Haircut]] Repo Amount 
This page will provide the descriptions of fields within the CCLF [[Haircut]] Repo Amount section of the CCLF 
[[obligations]] Management screen.  
 
Figure 244: CCLF [[obligations]] Management Screen - CCLF [[Haircut]] Repo Amount  
• Total CCLF Repo [[Haircut]] Amount – This field displays the total dollar value of haircuts on CCLF 
Transactions. 
• Total CCLF Repo Interest – This field displays the total CCLF Repo Interest on CCLF Transactions. 
 
  


---

## Page 250

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 250 
Redistribution Repo 
This page will provide the descriptions of fields within the Redistribution Repo section of the CCLF [[obligations]] 
Management screen.  
 
Figure 245: CCLF [[obligations]] Management Screen - Redistribution Repo 
• Potential Redistribution Amount – This field displays the dollar amount of the Remaining Financing 
Amount that [[FICC]] may initiate with a Direct Affected [[Member]], if such [[Member]] is under their CCLF Cap. 
This amount reflects a [[Member]]’s funding availability within their Individual Total Amount. If a [[Member]] is 
over their CCLF Cap, this amount will be zero. 
• Actual Redistribution Amount – The dollar amount of the Remaining Financing Amount that the [[FICC]] 
intends to initiate with a Direct Affected [[Member]]. If a [[Member]] is over their CCLF Cap this amount will be 
zero. 
 
  


---

## Page 251

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 251 
[[obligations]] Management 
This page will provide the descriptions of fields within the [[obligations]] Management section of the CCLF 
[[obligations]] Management screen. The Netting [[Member]] should review the CCLF [[obligations]] Management 
screen to confirm which of its deliver [[obligations]] to [[GSD]] (that are destined for the Defaulting [[Member]]) it has 
box position available for. Those [[obligations]] should be marked as “Available For Delivery” on the CCLF 
[[obligations]] Management screen. 
If the Netting [[Member]] is under its CCLF Cap, [[GSD]] will enter into a CCLF Transaction (CCLF Repo) with the 
Netting [[Member]]. The Netting [[Member]] will book this as a bilateral overnight reverse repo vs. [[GSD]]. 
 
Figure 246: CCLF [[obligations]] Management Screen - [[obligations]] Management (Part 1)  
• Obligation Details – The line item details under the Product, Obligation [[ID]], [[CUSIP]], Par and [[settlement]] 
Obligation $ Value columns displays each obligation destined for a Defaulting [[Member]]. 
• Available for Delivery – Each obligation that an Affected Direct [[Member]] has a box position in should be 
marked as “Yes.” Direct Affected Members that have Deliver [[obligations]] on their screen will be expected 
to review and mark “Yes” for those Deliver [[obligations]] that would be available for delivery to [[GSD]]. GCF 
will be automatically set to “Yes.” 
 
 


---

## Page 252

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 252 
Using the scroll bar at the bottom of the [[obligations]] Management section, scroll right to see the remaining 
columns within the section.    
 
Figure 247: CCLF [[obligations]] Management Screen - [[obligations]] Management (Part 2)  
• CCLF Start Money – This column displays Start Money for each CCLF Transaction. 
• CCLF Repo [[Haircut]] – This column displays the dollar value of a [[Haircut]] for each CCLF Transaction. 
• CCLF Repo Interest – This column displays the Repo Interest for each CCLF Transaction. 
• CCLF Repo Final Money – This column displays the Final Money for each CCLF Transaction. This is the 
value at which the End Leg of a CCLF Transaction will need to be delivered to [[FICC]]. 
• Admin Approved for Delivery $ Value – This column displays the dollar value for each obligation that 
[[FICC]] is instructing a [[Member]] to deliver to [[FICC]]. 
 
 
  


---

## Page 253

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 253 
Tools > DVP Bulk Trade Upload (Only Available for Contingency 
Purposes) 
The DVP Bulk Trade Upload tool in [[GSD]] RTTM Web may be used by Members to submit their DVP trades to 
[[GSD]] in the event other input channels (i.e., MQ) are temporary unavailable in the production environment. The 
DVP bulk upload tool described in this document does not allow for the submission of modifications or 
cancellations on existing trades. The bulk upload tool can only be used for trade input. 
Accessing the DVP Bulk Trade Upload Tool in [[GSD]] RTTM Web 
 
From the menu bar, select Tools > DVP Bulk Trade Upload. 
 
Figure 248: Tools > DVP Bulk Trade Upload 
Note: 
Because the DVP Bulk Trade Upload Tool may only be made available as a contingency, the dropdown menu [[Option]] for 
the tool will only be visible once the tool is enabled by [[GSD]] Business Operations.  
The tool would only be visible and accessible in certain circumstances , after approval from [[FICC]] Senior Management , and  
only  once the temporary availability of the tool has been  communicated to the membership . 
 
  


---

## Page 254

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 254 
Uploading, Validating and Confirming Submitted Trades 
Once the user navigates to the DVP Bulk Trade Upload menu [[Option]], three sub menu options will appear: 
• DVP Bulk Trade Upload > Entry – Allows [[GSD]] Members the ability to upload DVP trades via Pipe 
Delimited format to the DVP system when other trade input channels are unavailable. 
• DVP Bulk Trade Upload > Validate – Allows [[GSD]] Members to manage (view, submit and delete) their 
uploaded DVP trades before they are submitted to RTTM for trade validation and comparison.  
• DVP Bulk Trade Upload > Confirmation – Allows [[GSD]] Members to confirm what trades were successfully 
submitted and validated in [[GSD]] RTTM Web. 
 
Figure 249: Tools > DVP Bulk Trade Upload Menu Options 
DVP Bulk Trade Upload > Entry  
 
From the main menu bar at the top of the page, select Tools > DVP Bulk Trade Upload > Entry to access the 
Bulk Trade Entry screen. 
 
Figure 250: Tools > DVP Bulk Trade Upload > Entry 
 


---

## Page 255

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 255 
The below screen will appear. From this screen a user can upload a file from their local drive to the [[GSD]] RTTM 
Web application. Also, from this screen a user can download the sample template needed in order to upload 
trades to [[GSD]] RTTM Web.   
 
Figure 251: Trade Bulk Entry (DVP only) screen 
 
Below are the File Upload Instructions: 
1. File should have .csv extension. Field separator is: | 
2. File size should be below 250KB 
3. File should have a maximum of 1000 trades 
4. File should have the below template 
5. Empty/Optional fields require field separator 
6. Trailer row - number of trades in the file 
 
Below is the sample trade data format for the file upload process.  
Note:  
The below screenshot shows the format wrapping to the next line, however , within the .CSV file each line should not wrap 
to another line. With the exception of the header and trailer rows, each line within the file shall contain data for 1 trade. 
Refer to the 2nd and 3rd screenshot on this page.  
 
memberId|product|tradeType|[[CUSIP]]|traderId|tradeDate MM/DD/YYYY|tradeTime HH24:MM:SS|startDate 
MM/DD/YYYY|settlementDateMM/DD/YYYY|pricingMethod|execFirm|brokerXref|par|price|startAmount|settlem
entAmount|commission|rate|contra|contraExecFirm|xref  
#####trade_count:nnnn#####  
 
 
  
Figure 252: Sample Template for Cash and/or Repo Trades 

---

## Page 256

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 256 
Below is a sample of Cash and Repo trade data in pipe delimited format.  
Note:  
The “pipe character” separates each field.  
 
 
Figure 253: Sample Cash and Repo Trade in Pipe Delimited format 
Note: 
Data entries for Pricing Method and Price are not required for Repo Trade submissions.  
Below is an example of a .CSV file containing sample trades.  
 
Figure 254: Sample CSV file 
 
A user that has trade data in the format outlined on the Trade Bulk Entry screen (and above) would click the 
Choose a File button on the Trade Bulk Entry screen. This button will allow the user to browse their local drive 
so that the user can search for the file with the trades in the aforementioned format. 
  


---

## Page 257

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 257 
Once the Choose a File button is selected the Windows Explorer window would appear, similar to what is seen 
below. The user would then select the file that is to be uploaded to [[GSD]] RTTM Web and then click the Open  
button in the File Explorer window.  
 
Figure 255: File Explorer Window 
 
The File Explorer window will close and the Trade Bulk Entry screen will update showing the selected file name 
attached. Once the selected file name is attached the user can click the upload button located at the lower right 
side of the screen.  
 
Figure 256: Selected File Uploaded to Trade Bulk Entry Screen 
 
  


---

## Page 258

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 258 
If the user selects the incorrect file, the user can either select the Reset button located at the lower right side of 
the screen to refresh the page or the user can click the Choose a File button again and select the correct file.  
If the user selects the Reset button, the screen will update as seen below. After the screen refreshes, the user 
can then click the Choose a File button and select the correct file. 
 
Figure 257: Trade Bulk Entry screen after Reset button is selected 
 
Upon selecting the Upload button, the system will perform a file validation to ensure that the data in the .CSV 
file meets the necessary requirements for the upload process. If the file does not meet the requirements for any 
reason, the entire file will be rejected, and the reject reason will be displayed for the user. If a file is rejected, 
the user must rectify the issue resulting in the rejection before resubmitting the file. See below for an example 
of a rejected file. 
 
 
Figure 258: Example of Rejected File 
 
  


---

## Page 259

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 259 
If a file does pass the initial file format validation process, the user will receive a success message via popup 
window on the page. The user will also at this time be prompted to select to stay on the Trade Bulk Entry 
screen or be redirected to the DVP Trades Validation screen.  
 
Figure 259: Upload Success Message 
 
The user may select No if the user has more trades to input.  
The user may select Yes if they have no more trades to input and/or the user wishes to validate the uploaded 
trades before proceeding with further trade uploads. 
See below for an example of the Trade Bulk Entry screen once a file upload is successfully processed. 
 
Figure 260: Trade Bulk Entry screen after successful upload of file 
  


---

## Page 260

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 260 
DVP Bulk Trade Upload > Validate  
From the main menu bar at the top of the page, select Tools > DVP Bulk Trade Upload > Validate to access 
the DVP Trades Validation screen.  
 
Figure 261: Tools > DVP Bulk Trade Upload > Validate 
 
The below screen will appear. From this screen a user can submit trades to [[GSD]] RTTM Web for validation and  
comparison or delete the trades from the upload process. The trades have not gone through the system’s  
trade validation process. The status of the trades will be “Not Submitted” at this point. 
 
Figure 262: DVP Trades Validation screen 


---

## Page 261

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 261 
Note: 
From this screen, the user can select to refresh the screen or download the listed data by selecting either the Refresh 
button or the Download button seen here .   
Note:  
The Refresh button may be useful if there are multiple users within a firm that are uploading or have uploaded trades during 
a particular day. Any user, with the appropriate credentials, of a particular firm can view all trades uploaded for its firm on 
the DVP Trades Validation screen. Any user, with the appropriate credentials, of a particular firm can submit or delete 
uploaded trades from the DVP Trades Validation screen.  
Note:  
The DVP Trades Validation screen displays all of the relevant details submi tted on a trade including the user [[ID]] of the 
individual who submitted the trade and the time at which the trade was uploaded.  
 
To submit a trade to RTTM Web so that it goes through the trade validation process, select the trade by 
clicking the checkbox next to the trade. Then click the Submit button. If the user would like to submit all trades 
to RTTM Web, the user would select the “All” checkbox which is located in the header of the checkbox column.  
 
Figure 263: Selecting trade(s) to Submit for Trade Validation 
Note:  
Currently, the max number of trades that can be submitted at one time is 2,000 trades.  
   


---

## Page 262

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 262 
 Once the trades are selected and the Submit button is clicke d, the below popup confirmation window will 
appear. Select Yes to proceed with the trade submission. Otherwise, select No. For the purposes of this 
document, Yes is selected.  
 
Figure 264: Submission Confirmation Popup Window 
 
Once the user selects Yes, the DVP Trades Validation screen will update displaying the status of the trade(s).  
 
Figure 265: Trade(s) submitted successfully  
Note:  
During the processing of a large amount of trades, the status of the trades being submitted will change from Not Submitted 
to In Progress temporarily. Upon succesful validation of the trade(s), the status will change to Submitted.  
 
  


---

## Page 263

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 263 
To delete a trade from the system before it is submitted for trade validation, select the trade by clicking the 
checkbox next to the trade. Then click the Delete button. If the user would like to delete all trades on the 
screen, the user would select the “All” checkbox which is located in the header of the checkbox column and 
then click the Delete button.  
 
Figure 266: Selecting Trade(s) to Delete 
 
Once the trades are selected and the Delete button is selected, the below popup confirmation window will 
appear. Select Yes to proceed with the trade deletion. Otherwise, select No. For the purposes of this 
document, Yes is selected.  
 
Figure 267: Deletion Confirmation Popup Window 
 
  


---

## Page 264

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 264 
Once the user selects Yes, the DVP Trades Validation screen will update. The trade will be removed from the 
Validation screen and successfully deleted from the [[GSD]] RTTM Web system because the trade was never 
submitted, only uploaded.   
 
Figure 268: Trade(s) deleted successfully 
 
Once all of trades have been successfully submitted on the DVP Trades Validation screen, the user can 
navigate to the DVP Trades Confirmation screen. 
DVP Bulk Trade Upload > Confirmation  
 
From the main menu bar at the top of the page, select Tools > DVP Bulk Trade Upload > Confirmation to 
access the DVP Trades Confirmation screen.  
 
Figure 269: Tools > DVP Bulk Trade Upload > Confirmation 
  


---

## Page 265

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 265 
The below screen will appear. From this screen a user can view and/or download the list of trades that have 
been successfully submitted for their firm on the current day, along with their [[GSD]]-assigned Trade Identifiers 
(TIDs). 
 
Figure 270: DVP Trades Confirmation Screen 
Note: 
All trade data will be purged from the Trade Upload screens during the system end of day process. There is no histor ical 
view within the Trade Upload Tool. However, all successfully submitted trades can be viewed by navigating to the Trades > 
Search & Management screen and entering search criteria for the particular trade(s).  
 
To view the details of an individual trade from the DVP Trades Confirmation screen, select the vertical elipsis 
icon located to the left of the specific trade. The “View” [[Option]] will appear. Select View. 
 
Figure 271: Action: View Trade Details 
  


---

## Page 266

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Tools 266 
Upon selecting the View [[Option]], the trade details will appear on the screen. This screen displays the same 
details that the user would view from the Trades > Search & Management screen. 
 
Figure 272: Trade Details View 
 
  


---

## Page 267

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Reports 267 
REPORTS 
Reports utilized by [[GSD]] Members and other provisioned users are located on [[FICC]] Report Center. The [[FICC]] 
Report Center function allows users to access all current and historical reports that may be visible based on 
the user’s log on credentials. Most reports are in at least one of these three formats: 1) PDF, 2) TXT and/or 3) 
CSV and can be downloaded to the user’s PC and printed.   
Accessing [[FICC]] Report Center – [[GSD]] Reports 
Users that have been provisioned with read only or update access for [[GSD]] RTTM Web, will be able to access 
[[GSD]] Reports in [[FICC]] Report Center by selecting the Reports menu item from the navigation toolbar.  
 
Figure 273: Selecting Reports from the Navigation Toolbar 
 
Users that can access [[FICC]] Report Center through [[GSD]] RTTM Web should go directly to the section on [[FICC]] 
Report Center – [[GSD]] Reports. 
Certain users may only be provisioned for access to [[FICC]] Report Center and specifically, [[GSD]] Reports. Such 
users would access [[FICC]] Report Center via the [[DTCC]] Portal by using one of the 2 “General URLs,” 
https://login.[[DTCC]].net or https://portal.online.[[DTCC]].net.  The user would enter their single sign-on credentials and 
select the Login button. The user would be directed to the MyDTCC page where they would select the [[FICC]] 
Report Center tile from a menu of [[DTCC]] products/applications provisioned to the user’s single sign-on 
credentials would be displayed upon login. 
 
Figure 274: Selecting [[FICC]] Report Center from the MyDTCC page 


---

## Page 268

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Reports 268 
[[FICC]] Report Center – [[GSD]] Reports 
Once the user navigates to [[FICC]] Report Center, either via the Reports menu item on the navigation toolbar in 
[[GSD]] RTTM Web or through selecting the [[FICC]] Report Center tile from the list of products/applications on 
MyDTCC page, the below screen will appear. From this screen select [[GSD]] Reports. 
 
Figure 275: Selecting [[GSD]] Reports in [[FICC]] Report Center 
Note:  
Some user s may have access to both [[GSD]] Reports and MBSD Reports. Only accessing [[GSD]] Reports will be discussed in 
this guide.  
Once [[GSD]] Reports is selected, the [[GSD]] Reports Main Menu would appear. From this main menu, users can 
access various client facing reporting generated in support of [[GSD]]’s products and services. 
 
Figure 276: [[GSD]] Reports Main Menu 


---

## Page 269

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Reports 269 
How to Use [[FICC]] Report Center – [[GSD]] Reports 
Guides and Other Learning Materials 
Reporting guides and other reporting related learning materials are available on the [[DTCC]] Learning Center for 
the following report types: 
• Clearing Fund 
• Funds-Only [[settlement]] 
• GCF 
• DVP 
Report Center Quick Tips 
See below for a list of quick tips to use once a product/service report folder is selected. 
Report Center Page Features 
The [[GSD]] Report Center pages are divided into three sections: 
1. The Search Feature for historical reports is displayed on the left side of the screen.  
2. The list of available reports is displayed on the right side of the screen. 
3. The navigational features are located below the Search function. 
 
 
Figure 277: Report Center Page Features 
  
2 
3 
1 

---

## Page 270

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Reports 270 
Navigational Features 
See the below table for helpful instructions and field descriptions for the Report Center Page.  
Field/Item Name  Instructions/Descriptions 
Select a [[participant]] [[ID]] The system defaults to the [[GSD]] [[Member]] [[ID]] number based on the user’s log on credenti als. 
Users with access to multiple accounts may select from a list of available [[Member]] IDs in the  
dropdown list.  
Enter a Date Enter the Report date for the desired report(s).  
« Select this button to change the Report Date field to the  previous valid Report Date and to 
resubmit the query.  
Retrieve Equivalent to a Submit button.  
» Select this button to change the Report Date field to the next valid Report Date and to 
resubmit the query.  
Go To Latest Select this button to change the Report Date field to the most recent Report Date and to 
resubmit the query.  
Report Headings  • Compar e – Lists all comparison related r epor ts generated for trades prior  to Netting. 
• Net – Lists all Intraday and End -of-Day Reports, as applicable, generated  for activity 
(trade positions/[[obligations]] ) subject to the Netting process . 
• Other – Lists all Reports that [[DO]] not fit in the above two categories . 
Report Name Click on a Report Name to view the report.  
 Select this button to download a report.  
Home Click this link t o be redirected to the [[FICC]] Report Center Menu page. 
[[GSD]] Reports  Click this link to be redirected back to the [[GSD]] Reports Main Menu. 
Previous Page Click this link to go to the previously viewed page.  
Table 50: Navigational Features 
To View, Print or Download a Report 
 
To View a Report, click on the desired report name to open the report in a web browser window. 
To View Historical Reports (from an earlier date), use the Search feature located on the left side of the screen. 
Enter the desired business date, using the format mm/dd/yyyy and either select: 
• the Retrieve button to view reports for the desired date or 
• the Back or Forward button to retrieve reports generated one day prior or after the displayed date. 
 
A list of historical reports for the selected date will appear on the right side of the screen. Click on the desired 
report name to open the report in a web browser window. 
To print the displayed report, use the web browser’s Print function. To download a report, click the download     
      button for the desired report. Once downloaded, the report can be saved locally.  


---

## Page 271

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Common Icons and Buttons in RTTM Web 271 
COMMON ICONS AND BUTTONS IN RTTM WEB 
Listed in the following table are the descriptions of common elements seen across the [[FICC]] [[GSD]] RTTM® Web 
application.  
Icon/Button  Name Description 
 
                               ...or  
Additional Data 
(expand or collapse)  
The Additional Data screen contains an audit trail of 
the selected trade’s processing history. Click the plus 
sign to view the processing history for the trade. Click 
the minus sign to hide the processing histor y . 
 Add Row Click to add a row.  
 
Affirm Click to affirm an advisory trade submitted against 
you. 
 Alert Indicates a system warning message.  
 Apply Changes  Click to submit a modification of trade data.  
* Asterisk Indicates a required field . 
 Business Date Current System Business Date 
 Cancel  Click to cancel an entry or action.  
 
Column Header   
Selector  
Click to open a popup window that allows you to 
select which columns you want to view for your 
search results.  
 
Copy  Click to copy all the data from the current row to a 
new row, except the Xref . This differs from the Add 
Row icon.  
 
Date (Range) 
Picker 
Click to select a singular date or a date range, as 
applicable.  
  Delete Click to delete a row. 
 DK Click to DK an advisory trade submitted against you.  
  Download Click to download the selected report.  
  Drop -down menu Click the down arrow to display a menu from which 
you can make a selection.  
 Export  Click to export the data on the page to an Excel  
spreadsheet.  


---

## Page 272

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Common Icons and Buttons in RTTM Web 272 
Icon/Button  Name Description 
 
Error / Reject 
Message 
Indicates the entry has been rejected by the system. 
Click to open a popup window that displays the 
error(s) in your entry.  
 Exit Click to close the selected window.  
 
Filter  Click to filter a column by a specific data point or a set 
of data points.  
 
Home Click to navigate back to the Dashboard  or click 
Dashboard from the navigation tool bar.  
 Information  Hover over to see additional information.  
 Logout  Click to log out of the system. For optimal security, 
always use this link to log off the system.  
 
Magnifying Glass  If the icon appears next to an empty field, click to 
search for a value for the field. If it appears next to a 
record, click to view more detailed information.  
 Refresh Click to refresh the screen.  
 Reset Click to return all fields to their original [[default]] values.  
 
Search Click to search for the data you entered on the search  
screens for the records that fit the entered  search 
criteria.  
 Submit Click to submit the data you entered . 
 Success Message Indicates the entry has been submitted.  
 Validate Click to validate your entry versus the [[GSD]] system 
prior to submission.  
 Vertical Ellipsis  Click to display a n action drop -down menu from which 
you can make a selection.   
 Warning  Click to open a popup window that displays warnings 
in your entry.  
Table 51: Common Elements 


---

## Page 273

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Other Miscellaneous Featur es 273 
OTHER MISCELLANEOUS FEATURES 
Use the navigation toolbar to access all [[GSD]] functions. 
 
Figure 278: Navigation toolbar 
 
Links within [[GSD]] RTTM Web are displayed in blue font (as seen below). These links may direct the user to 
certain data sets within [[GSD]] RTTM Web, (e.g., Trade Search results) or to sites away from [[GSD]] RTTM Web 
(e.g., [[DTCC]] Learning or Treasury Direct). 
 
Figure 279: Trade Statistics Links 
 
Use the wildcard function if you [[DO]] not wish to enter the full [[CUSIP]] number. You can enter a portion of the 
data. In the following example, the search results will display all records for a [[CUSIP]] beginning with 912796.  
 
Figure 280: [[CUSIP]] field 
Note:  
The wildcard character (*) is not required for a search with a partial  [[CUSIP]].    


---

## Page 274

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Other Miscellaneous Featur es 274 
On a search results page, click on any column header to sort the records in ascending or descending order. 
On a search results page, click on any column header to filter the records. See Filter icon in the above table. 
 
Figure 281: Trade Search Column Header Order and Filter 
 
On a search results page, you can click and drag any column header so that the column order is displayed per 
your preference.  
 
Figure 282: Trade Search Column Header Rearrangement 
 
The below shorthand features are available in various trade entry and trade search screens within [[GSD]] RTTM 
Web. 
Shorthand Description Example 
M Thousand 3,000 can be entered as 3M 
MM Million  3,000,000 can be entered as 3MM  
MMM Billion  3,000,000,000 can be entered as 3MMM  
Table 52: Trade Data Shorthand 


---

## Page 275

[[FICC]] [[GSD]]
 
RTTM® WFE [[Member]] User Guide 
Accessing Support 275 
ACCESSING SUPPORT 
Access the [[DTCC]] Learning Center to learn more about [[GSD]] through the step-by-step procedures, 
presentation material, and other content available. 
If you have issues logging on to the system, contact [[DTCC]] Client Support using one of the numbers listed: 
• US and Canada callers: 1-888-382-2721  
• International callers: +1-212-855-8099 

---

## Page 276

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 