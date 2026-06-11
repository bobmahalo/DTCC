---
title: "UWC: Quick Guide to Features and Upcoming Functionality"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/UWC_QuickGuide_v8-4_20210610.pdf"
pages: 52
size: "2461.6 KB"
category: "Underwriting"
ingested_on: "2026-06-05"
---

# UWC: Quick Guide to Features and Upcoming Functionality

**Original File:** [UWC_QuickGuide_v8-4_20210610.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/UWC_QuickGuide_v8-4_20210610.pdf)  
**Category:** Underwriting  
**Total Pages:** 52  
**File Size:** 2461.6 KB  

---

## Page 1

 
 
 
[[Underwriting]] CENTRAL 
QUICK GUIDE TO FEATURES AND UPCOMING FUNCTIONALITY 
VERSION 8.4 
JUNE 10, 2021 
 


---

## Page 2

 
 
Copyright © 1999 - 2021 by The Depository Trust & Clearing Corporation (“[[DTCC]]”). 
 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Info: June 10, 2021 
Publication Code: UW125 
Service: [[Underwriting]] Central 
Title: Quick Guide to Features and Upcoming Functionality 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
General Information ............................................................................................................................................. 6 
In Scope .............................................................................................................................................................. 6 
Out of Scope ....................................................................................................................................................... 6 
Areas of Focus .................................................................................................................................................... 6 
Future Release Information ................................................................................................................................ 7 
We want your feedback! ..................................................................................................................................... 7 
Dashboard ............................................................................................................................................................. 8 
Offering Grid ....................................................................................................................................................... 8 
Dashboard Table Column Names ................................................................................................................... 10 
Offering [[ID]] & [[issuer]] Live Data Available .................................................................................................... 10 
Closing Date Live Data Available ............................................................................................................... 10 
Legal Live Data Available ........................................................................................................................... 10 
Agent Information Live Data Available (except for [[transfer agent]]) ........................................................... 11 
Compliance Live Data Available ............................................................................................................... 11 
Data Conflicts Live Data Available ............................................................................................................. 11 
Data Conflict Modal ...................................................................................................................................... 12 
Data Conflicts – Interest Periods ................................................................................................................. 13 
Crediting [[participant]] Live Data Available ................................................................................................... 14 
[[settlement]] Eligible Live Data Available ...................................................................................................... 14 
Inventory Status  Live Data Available ......................................................................................................... 15 
Specialist [[ID]] Live Data Available ............................................................................................................... 15 
Takedown Amount ......................................................................................................................................... 16 
Position Delivery Status ................................................................................................................................. 16 
Correspondents Tile ......................................................................................................................................... 17 
Search Tile ........................................................................................................................................................ 19 
Search Area .................................................................................................................................................... 20 
Saved Search Criteria ..................................................................................................................................... 21 
Alerts Tile .......................................................................................................................................................... 23 

---

## Page 4

 
 
Certificate Declined / Undeliverable ................................................................................................................ 24 
Certificate Ready for Submission .................................................................................................................... 24 
Offering Created by [[DTC]] ................................................................................................................................. 24 
Certificate Destroyed ....................................................................................................................................... 24 
Quick Search .................................................................................................................................................... 25 
Creating an Offering .......................................................................................................................................... 27 
CD Creation Wizard: Primary Offering.............................................................................................................. 27 
1. [[CUSIP]] ......................................................................................................................................................... 28 
2. Offering ....................................................................................................................................................... 29 
BLOR Requirements ...................................................................................................................................... 30 
3. [[securities]] .................................................................................................................................................. 32 
4. Submit to [[DTC]] ............................................................................................................................................ 34 
5. Submit to [[issuer]] .......................................................................................................................................... 35 
Undeliverable Items ....................................................................................................................................... 38 
Managing Draft Offerings ................................................................................................................................ 38 
Modifying [[securities]] After Dissemination ........................................................................................................ 39 
Creating a Secondary Offering ......................................................................................................................... 39 
Creating Offerings via Spreadsheet Upload ..................................................................................................... 40 
Using the Spreadsheet Template .................................................................................................................... 42 
Offering Tab ................................................................................................................................................... 43 
CorpCDs-01 Tab ............................................................................................................................................ 44 
Viewing an Audit Trail ........................................................................................................................................ 46 
Special Events / Items ....................................................................................................................................... 48 
Letter of Possession ......................................................................................................................................... 48 
Deleting an Offering .......................................................................................................................................... 48 
Deletion Restrictions ....................................................................................................................................... 48 
Postponing an Offering ..................................................................................................................................... 49 
Postponing Restrictions ................................................................................................................................... 49 
Destroying a Certificate .................................................................................................................................... 50 
Postpone / Delete ............................................................................................................................................ 50 

---

## Page 5

 
 
Alerts ............................................................................................................................................................... 50 
Reactivating an Issue ....................................................................................................................................... 51 
 

---

## Page 6

Quick Guide to Features and Upcoming Functionality 
General Information 6 
GENERAL INFORMATION 
The ongoing incremental release of [[Underwriting]] Central (UWC) is meant to give you the opportunity to test 
drive the new application.  
In Scope 
Phase 1 of the UWC project is specific to Retail Certificates of Deposit. 
[[DTC]], in partnership with the industry, developed four standardized master electronic certificate templates for 
Phase 1 of the UW rewrite. The system automatically selects the appropriate template based on a security’s 
features.  
The four standardized master electronic certificate templates include: 
• [[DTC]] – Form Fixed Rate Noncallable 
• [[DTC]] – Form Fixed Rate Callable 
• [[DTC]] – Form Step Rate Callable 
• [[DTC]] – Form Step Rate Noncallable 
Out of Scope 
Products that are out of scope for this phase of the UWC project are: 
• [[FAST]], 
• Structured CDs (zero-coupon, variable), 
• CDs issued by Credit Unions, and 
• [[Secondary Offerings]] where the [[CUSIP]] was not submitted via UWC. 
Areas of Focus 
Our areas of focus for this release are deleting offerings / [[securities]], postponing offerings, reactivating 
offerings, destroying certificates previously signed by the [[issuer]], implementation of the Credit Union indicator, 
data conflicts for [[securities]] with step up features, and [[Secondary Offerings]]. 
We are also continuing to test the Digital Certificates workflow via an integration with DocuSign. The (4) final 
versions of the electronic master certificates have been implemented into the system, as well as the final 
version of the electronic BLOR. 
The following Quick Guide walks you through the screens and functionality available in the October 2020 
release.  
 
 

---

## Page 7

Quick Guide to Features and Upcoming Functionality 
General Information 7 
Future Release Information 
Check out the material noted with green bars for some insight into what you can expect from future 
releases. 
Material marked in this fashion is not yet available in the test application. 
We want your feedback! 
[[DO]] you have any questions or comments on UWC’s screens, or about the functionality you are able to test? 
Are there any features that you feel are critical to add to UWC as we move forward in its development?  
We want to hear it! Questions and feedback can be directed to UWCPM@[[DTCC]].com. 
 
 

---

## Page 8

Quick Guide to Features and Upcoming Functionality 
Dashboard 8 
DASHBOARD  
The Dashboard allows you to view your firm’s offerings quickly and easily. It also helps you identify items that 
need your attention: in particular, offerings closing within the next 5 business days. An offering only advances 
when its row is filled with gray check marks. 
Only the first four tiles are live. The remaining 2 tiles are not yet functional and will be part of a future release. 
Note that the Correspondents tile is only visible to full [[DTC]] members. Correspondents will not see this tile. 
Offering Grid 
The grid looks essentially the same for the first three tiles: Closing in 5 Business Days, All Offerings, and 
Closing. 
Note: 
If this table is empty, you need to go through the CD creation process to enter test offerings. 
 
 
 

---

## Page 9

Quick Guide to Features and Upcoming Functionality 
Dashboard 9 
Tile Name Contains 
Closing in 5 
Business Days 
Populates the grid with offerings that are closing within the next five business days and 
may require your immediate attention. All issues in this grid have already been submitted 
to [[DTC]].  
Use the filters to display only those items that are pending [[settlement]] eligibility or are 
pending [[issuer]] signature. This is the [[default]] landing page for the Dashboard.  
All Offerings Populates the grid with all of your offerings, whether in Draft or Submitted status. You can 
then filter by “All Offerings,” “Drafts,” “Active,” and “Postponed”. 
Closing Only populates the grid with issues that have been submitted to [[DTC]]. Here, you can filter 
the offerings by “All,” “Open,” or “Closed.” 
 
The Offering table reflects issues submitted by your firm for [[Asset]] classes for which you have entitlements. 
Crediting participants can view issues for their correspondents and can confirm or reject them when 
appropriate. This release of UWC only includes CDs. 
Hover over any of the status icons in the table to get further information about that item.  
• Click one of the Filters under the Closing in 5 Business Days tab to display items that need repair, 
specifically those offerings/certificates for which the Digital Certificate has yet to be executed (Pending 
Inventory). 
• A red exclamation mark ! indicates an offering status in need of repair that will need to be addressed by 
the user or [[DTC]].  
Hover over the exclamation mark to display more details on the item that is missing or in conflict. 
• A  indicates that all processing has been completed for that given category. 
• A yellow “caution” icon  indicates that the status is pending a [[DTC]] specialist action. Hover over this icon 
to see the action that is pending. 
• Note the menus under the Actions column at the end of the row.  
o Mouse over the three vertical dots at the end of a row to view its action menu. 
o Click Modify to be returned to step 4 of the CD Offering wizard.  
From step 4, you can choose to edit either your offering and/or security details by selecting the edit 
icon  next to the appropriate section. If a data element is updated, you must continue advancing 
through the workflow and resubmit your offering to ensure changes are captured by [[DTC]]. 
Note: 
Once a digital certificate is submitted to the [[issuer]], you can only modify fields not included on the digital 
certificate. In addition, after a security is made [[settlement]] Eligible, specific fields will be locked for editing (e.g. 
[[CUSIP]], [[issuer]], Article 8, and Digital Certificate). 
o Click Delete to delete the entire offering record. Click Postpone to postpone the entire offering. 
 
You are able to select the number of offerings that you want to view in this table (10, 25, 50, or 100), if 
applicable.
 
 

---

## Page 10

Quick Guide to Features and Upcoming Functionality 
Dashboard 10 
Dashboard Table Column Names 
Offering [[ID]] & [[issuer]] Live Data Available 
This information is automatically populated from the CD Offering wizard.  
The [[issuer]] is attached to the Offering [[ID]] in step 2 of the wizard. The Offering [[ID]] is generated in step 3 of the 
wizard. 
Tile Name Text Appearance / Action 
All Offerings • For pure draft and postponed items, this column’s text is displayed in red. 
Hovering over the red text presents a warning message that indicates whether the 
offering is in draft or postponed status.  
Aside from the Closing Date, all other columns are blank when an offering is in pure 
draft. When an issue is Postponed, the Closing Date is “12/31/9999”. 
• For items that have been submitted and subsequently modified, this column’s 
text is also displayed in red. Hovering over the red text will present a warning 
message.  
All other columns contain the status of the initial submission, not the modified 
version.  
These items MUST be resubmitted in order for [[DTC]] to possess the most recent 
offering information. 
• Submitted offerings appear in black text. 
Closing 
Closing in 5 Days 
Neither view will display pure draft or postponed items.  
The offerings with red text in this column were submitted to [[DTC]] but have been 
modified since their initial submission. These items must be resubmitted in order for 
[[DTC]] to possess and reflect the most recent updates. 
Closing Date Live Data Available 
The closing date of the Offering is automatically populated from the CD Offering wizard in step 2. 
Legal Live Data Available 
Hover over the icon in this field to see the legal status of this offering. A check mark indicates that there is an 
approved BLOR matched to this offering. In a pure draft, this field is blank. 
Each [[issuer]] looking to make their [[securities]] eligible at [[DTC]] must submit a Blanket Letter of Representation 
(BLOR) to establish a relationship with [[DTC]]. A new BLOR will be required for any [[issuer]] leveraging the digital 
certificate model, even if an existing BLOR is on file. 
 

---

## Page 11

Quick Guide to Features and Upcoming Functionality 
Dashboard 11 
Further notes on the Legal column and BLORs: 
• A [[DTC]] Specialist will review submitted BLORs and either approve or reject each one. 
• If a BLOR is not on file, you will receive a pop-up message upon advancing from step 2 to step 3 of the 
CD Offering wizard. You will be able to continue through the workflow, but you will see a red exclamation 
mark ! in this column after submission. 
• If a BLOR has been submitted to [[DTC]] by the [[issuer]] but the BLOR has not yet been reviewed/approved, 
you will see a yellow "caution" icon  in this column.  
• If a BLOR is already on file, then you WILL NOT receive a pop-up message upon advancing from step 2
 
to step 3 of the wizard. Additionally, you will see a gray check mark  in this column after submission. 
• While the pop-up message provides a link to UW’s New [[issuer]] Eligibility page where the new BLOR 
document for digital certificate [[securities]] will be located in the future, for this release you will need to use 
this link: PSE BLOR. 
o When you encounter this scenario, click the above link and direct the BLOR to UWCPM@[[DTCC]].com. 
[[DTC]] can then match the BLOR to your offering, and the updated status will be reflected by the check 
mark on your dashboard. The [[issuer]] contact listed on the BLOR will receive an email once the BLOR 
is matched.  
Agent Information Live Data Available (except for [[transfer agent]]) 
A check mark in this field indicates that a paying agent has been attached to this offering.  
In a pure draft, this field is blank. 
In the future, this column will also indicate whether a [[transfer agent]] has been properly attached to the offering 
(if applicable). 
Compliance Live Data Available 
A check mark indicates that the [[issuer]] information passes regulatory controls as defined by the Office of 
Foreign Assets Control (OFAC). 
If this column contains a red exclamation point !, a UW specialist will have to review this status. 
In a pure draft, this field is blank. 
Data Conflicts Live Data Available 
If underwriters are submitting the same [[CUSIP]], all fields must match aside from Takedown Amount and 
Brokerage Agreement Date. Any conflicts must be resolved prior to the offering’s closing. 
A gray check mark indicates that the issue is free of data conflicts as indicated above.  
If this column contains a red exclamation point !, data conflicts exist and must be corrected: 
 
 

---

## Page 12

Quick Guide to Features and Upcoming Functionality 
Dashboard 12 
1. On the Dashboard, click the Data Conflicts status for this issue.  
 
This invokes the Data Conflict modal. 
• The conflict modal only displays the fields in conflict.  
• You can review the fields in conflict at the Offering / Issue level or the Security level.  
• See the Data Conflict Modal section for more information. 
2. Within the modal, select the hyperlink of your Offering [[ID]] to land on step 4 of the wizard.  
Once at step 4, click Edit to update your data elements. Then, click Submit to [[DTC]]. 
Once the conflict is resolved, the Dashboard displays a gray check mark in this column. 
In a pure draft, the Data Conflicts field is blank. 
Data Conflict Modal 
Offering / Issue Level Data Conflicts 
 
In the image above, conflicts only exist at the Offering / Issue level. Therefore, the Security-level grid is blank.  
Within the data conflict grid: 
• Only the fields in conflict are displayed. 
• The first row in the table displays what [[DTC]] has on file. 
• The second row is your firm’s record. 
• Any subsequent rows reflect any other underwriters that are submitting the [[CUSIP]] for eligibility. Other 
underwriters’ firm-specific information is anonymized.  
 


---

## Page 13

Quick Guide to Features and Upcoming Functionality 
Dashboard 13 
In the Offering / Issue example above, [[DTC]] has an expected closing date of 1/08/2020. The second row 
(representing your firm’s submission) has a closing date of 1/10/2020. Each subsequent [[underwriter]] has a 
closing date that does not match what [[DTC]] has on file. This field must match across all underwriters for the 
offering to close.  
If your record requires an update:  
1. C lick the hyperlink located in your grid to advance to your record. 
2. U pdate the field in conflict. 
3. Click Submit to [[DTC]]. 
 
Security Level Data Conflicts 
 
The above image is a snapshot of the Security Level Conflicts grid.  
• Only the fields in conflict are displayed. 
• The first row in the table displays what [[DTC]] has on file. 
• The second row is your firm’s record.  
• Any subsequent rows reflect any other underwriters that are submitting the [[CUSIP]] for eligibility.  
 
In this example, there are data elements within your record that [[DO]] not match what the other underwriters have 
on file. For instance, the value your firm entered into the “Call Indicator” field is “Yes” while the other two firms 
entered “No.” Since the other firms’ records match, it is likely that your record was entered incorrectly. Your 
firm should review your issue details to confirm the correct value. If your value is incorrect, your firms’ records 
must be updated and resubmitted to resolve the data conflict. 
Data Conflicts – Interest Periods 
CUSIPs shared by multiple underwriters must contain identical values within every period of the security’s 
interest table. The maximum number of interest periods is 25. 
Interest periods display a data conflict if there are discrepancies between the interest start date, end date, 
and/or rate. If there is a discrepancy with any value on the row, UWC shows the details for the entire interest 
period. 


---

## Page 14

Quick Guide to Features and Upcoming Functionality 
Dashboard 14 
 
If there are any data discrepancies, the Data Conflict modal displays rows for all records in conflict. In the 
example above, there are discrepancies between the interest rates on Interest Period 1, Interest Period 2, and 
Interest Period 3. As mentioned above, if there is a discrepancy with any value on the row on the interest table, 
UWC shows the details for the entire interest period. 
Additionally, if there is a discrepancy between the total number of interest periods for the security, that is called 
out in the Interest Feature Count column. 
If you have more than 10 data conflicts for a single security, you will see a warning message in the conflict 
modal. 
Crediting [[participant]] Live Data Available 
Correspondents must have their submitted offerings approved by a Crediting [[participant]] (or full [[DTC]] [[Member]]) 
in order for their offerings/[[securities]] to become [[DTC]]-eligible. 
A gray check mark in this field indicates that a crediting [[participant]] has confirmed this offering. If you are a full 
[[DTC]] [[participant]], this field always displays a gray check mark. 
A red exclamation point ! in this column indicates that the offering is still awaiting approval, or that at least one 
security was rejected. 
For more information, please see the Correspondents Tile section. 
[[settlement]] Eligible Live Data Available 
A check mark indicates that the [[securities]] in the issue have satisfied all processes and prerequisites to become 
eligible on [[DTC]]’s Security Masterfile (SMF). 
If this column contains a red exclamation point !, then at least one security has not been made [[settlement]] 
eligible or one security contains lock and chills, which prevents deposits or withdrawals on the security.  


---

## Page 15

Quick Guide to Features and Upcoming Functionality 
Dashboard 15 
This column also contains a [[CUSIP]] grid which outlines the status of each security within the offering (i.e., 
[[settlement]] Eligible, Globally Locked or Chilled, Pending). 
In a pure draft, the [[settlement]] Eligible field is blank. 
Inventory Status  Live Data Available 
This field reflects the current status of the offering as it exists in [[DTC]]’s records as of this moment. 
A check mark indicates that the [[issuer]] has signed all digital certificates related to this issue. 
A red exclamation point ! means that: 
1. At least one certificate has not been signed by the [[issuer]] and submitted back to [[DTC]], or 
2. A certificate was sent to an undeliverable address. At this point, UW is unable to resend a certificate. You 
must call your [[DTC]] Specialist to void the undeliverable DocuSign item. Once it is voided, the mouse-over 
status of the exclamation point reads “Voided.” You must correct the offering and re-submit it. See 
Undeliverable Items for more information. 
Note: 
Mouse over the exclamation point ! to view the exact status. 
In a pure draft, the Inventory Status field is blank. 
Tile Name Content / Meaning 
All Offerings For pure draft items, this column will be blank as nothing has been submitted to [[DTC]]. 
Therefore, there are no statuses or processes feeding the dashboard. 
Closing 
Closing in 5 Days 
This field indicates whether a certificate has been delivered to [[DTC]]. 
• For digital items: they were signed by the [[issuer]]. 
• Future functionality: this field will include issues that are [[FAST]] or that use 
physical certificates.  
Items that have been submitted and subsequently modified will reflect details of the 
PREVIOUSLY SUBMITTED RECORD. This is the version that [[DTC]] has on file. To 
update the dashboard, resubmit any modifications via the step wizard. 
Specialist [[ID]] Live Data Available 
Hover over the (i) icon in the Specialist [[ID]] column to see the name of the [[DTCC]] specialist who has been 
assigned to this offering. 
In a pure draft, the Specialist [[ID]] field is blank. 
  
 
 
 
 

---

## Page 16

Quick Guide to Features and Upcoming Functionality 
Dashboard 16 
Takedown Amount 
Closing tab only  Live Data Available for Single Offering 
This is a rollup or sum of the takedown for all CUSIPS within the offering, which is entered in step 2 of the 
wizard. The roll up of the takedown is also displayed in the offering section of step 4. 
In a pure draft, the Takedown Amount field is blank. 
Position Delivery Status 
Closing tab only  Live Data Available 
A check mark in this field indicates that the inventory was delivered to the UW account. 
In a pure draft, the Position Delivery Status field is blank. 
Note: 
If there is a red exclamation point !  in this field, a UW specialist will have to manage this status 
  

---

## Page 17

Quick Guide to Features and Upcoming Functionality 
Dashboard 17 
Correspondents Tile 
The Correspondents tile is only visible to full [[DTC]] members. Correspondents will see the other five tiles only. 
If you are a full [[DTC]] [[Member]], this tile is only applicable to you if you have a crediting [[participant]]/correspondent 
relationship with any firms. Offerings submitted by your correspondents must be approved by you prior to 
submission. 
Here, you can view offerings submitted by your correspondents for the [[Asset]] classes for which you are entitled. 
At the moment, this is only CDs.  
 
• Items containing a gray check mark have been approved. 
• Items containing a red exclamation point ! either require approval or have been rejected. 
To view an individual correspondent’s offering for approval or rejection, mouse over the three vertical dots at 
the end of a row and click View Record from the Action menu.  
This invokes the Crediting [[participant]] screen. Here, you can see some of the offering details and data 
elements for each security submitted as part of the offering. 
 
 

---

## Page 18

Quick Guide to Features and Upcoming Functionality 
Dashboard 18 
 
You can approve or reject multiple items at a time: 
1. Click the checkbox(es) for the items you want to approve or reject. 
Note:  
You can click the top checkbox to select all items on the list. 
2. Enter your comments (for approval or rejection) in the Comments box.  
Note: 
Comments are required whenever an item is rejected. 
3. Click either Reject or Approve. 
After an item is approved by you, it displays a gray check mark in the Crediting [[participant]] Approval 
Status column of the Correspondents tile on the Dashboard. 
After an item is rejected by you, it displays a red exclamation point in this column.  
Note:  
If one security is rejected, then the entire status will display as rejected. All [[securities]] must be approved to render 
checkmark. 
 


---

## Page 19

Quick Guide to Features and Upcoming Functionality 
Dashboard 19 
Search Tile 
Click the Search tile to find an offering that has already been submitted. While you can use the Quick Search 
to find an offering by Offering [[ID]] or [[CUSIP]], the full search capabilities on the Search page allow you to search 
by any combination of detailed search criteria.  
You can search for records that have been submitted within the past five years. 
• If you are a crediting [[participant]], you can view records submitted by your firm or by one of your 
correspondent firms. 
• If you are a correspondent firm, you can only view records submitted by your own firm. 
 


---

## Page 20

Quick Guide to Features and Upcoming Functionality 
Dashboard 20 
Search Area 
These blank fields below the Saved Search area allow you to mix and match over 20 different search criteria. 
• You must enter at least one of the Search criteria. There is no maximum number of criteria. 
• Click Search once you have selected all criteria to narrow your search.  
Click Reset to clear all of the criteria fields. 
• Based on your search criteria, up to 5000 results are returned. 
• You can export the search results by clicking the Export to Excel  icon. 
 
After clicking Search, UWC returns your search results: 
 
Note: 
If there is more than one [[CUSIP]] in your offering, the first [[CUSIP]] in the offering is displayed here as a hyperlink. Click the 
hyperlink to view all the CUSIPs in the offering.  


---

## Page 21

Quick Guide to Features and Upcoming Functionality 
Dashboard 21 
 
If you export the results into Excel, all CUSIPs in an offering are returned. 
 
Saved Search Criteria 
This area at the top of the Search page allows you to access sets of Search criteria that you have previously 
used. You can save up to 10 search queries for later use. For example, if you frequently search by a specific 
date range, [[issuer]], and [[underwriter]] [[ID]], you can save these criteria as a single query  
To save search criteria as a single query: 
1. Complete a search using all criteria that you want to include in your saved query. 
The top of the search results page displays your search criteria. 
 
2. Click Save Search. 
The Save New Criteria box appears. 


---

## Page 22

Quick Guide to Features and Upcoming Functionality 
Dashboard 22 
 
3. Type the name of this search in the Save New Criteria box and click Save. 
The Search page displays your saved search sets at the top of the page. 
 
• Click the Edit icon  to make changes to this search set. 
• Click the Delete icon  to delete this search set. 
  


---

## Page 23

Quick Guide to Features and Upcoming Functionality 
Dashboard 23 
Alerts Tile 
Click the Alerts tile to view all alerts associated with your account. The red number in the upper right corner of 
the tile signals the number of alerts that are active for your account. 
 
To view an alert, hover your mouse over the three dots in the Actions column and click View Details from the 
pop-up menu.  
To clear an alert, click Clear Alert from this pop-up menu. This removes the alert from this list. Alerts will 
remain in this list until they are cleared manually or the associated issue closes. 


---

## Page 24

Quick Guide to Features and Upcoming Functionality 
Dashboard 24 
There are four types of alerts that can be displayed on this tile. 
If a certificate is destroyed by [[DTC]] (during step 5), UWC sends an alert to [[DTC]] and the client that initiated the 
destruction upon its completion. 
Certificate Declined / Undeliverable 
• This alert is triggered when a certificate is Declined or Undeliverable. Only one alert is displayed per 
issue. 
 
• If you receive and manually clear an alert for an issue, then create a replacement certificate that is 
subsequently declined, another alert is generated. 
 
• Clicking View Details brings you to step 5 of the certificate creation wizard. 
Certificate Ready for Submission 
• This alert is triggered when all [[securities]] within an issue have the status “Ready for Submission.” 
 
• When this alert is triggered, the [[underwriter]] receives an e-mail informing them that the certificates can be 
sent to the [[issuer]] for signature. 
 
• Clicking View Details brings you to step 5 of the certificate creation wizard. 
Offering Created by [[DTC]]  
• This alert is triggered when an offering is created by [[DTC]]. 
 
• This alert is visible to all users at an [[Underwriting]] firm with CD [[Entitlement]]. 
 
• Clicking View Details brings you to step 4 of the certificate creation wizard. 
Certificate Destroyed 
• This alert is triggered in two instances: 
o When a certificate is destroyed by [[DTC]] (during step 5), and  
o When a certificate is destroyed by a user at your firm as part of a Postpone or Delete request. 
 
• When you receive this alert, the CD is available for modification.  
 
• See the section about Destroying a Certificate for more information. 
 
  

---

## Page 25

Quick Guide to Features and Upcoming Functionality 
Dashboard 25 
Quick Search 
Once an offering has been created, you can navigate back to it by using the Quick Search fields. You can use 
the Quick Search to find offerings by using either the Offering [[ID]] or the [[CUSIP]]. 
• Users at crediting [[participant]] firms can view records submitted by their firm or records submitted by one of 
their correspondent firms. 
• Users at correspondent firms can only view records submitted by their own firm. 
• If multiple correspondents are working for you, a modal pops up. Click which offering you want to view. 
 
 
1. Select [[CUSIP]] or Offering [[ID]] from the drop-down menu. 
 
2. Enter the appropriate [[ID]]. 
 
3. Click Search. 
 
4. If you are a crediting [[participant]] with multiple correspondents submitting on your behalf, or if you entered 
the same [[CUSIP]] as your correspondent firm, you will have to select which UW record you want to view.  
Select the Offering [[ID]] of the appropriate record from the search modal.   


---

## Page 26

Quick Guide to Features and Upcoming Functionality 
Dashboard 26 
 
 
The Offering Type appears on the quick search results grid to help you identify a primary or secondary 
issuance.  
 
5. Once the appropriate UW record is selected, you are brought to step 4 in the CD creation wizard for that 
offering. 
• If the offering is a fully submitted record, you can opt to edit the record (using either the Offering 
Details or the Security Details Edit icon ) or to review the security status on step 5 by clicking 
Continue.  
• If the offering is in draft form, it must be validated before you can submit it to [[DTC]].  
Click the Security Details Edit icon  to land on step 3 and submit your record for validation.  
If your fields contain any errors, they will be noted on-screen. 
• If the offering is closed or completed, you are brought to step 4 of the wizard in view-only mode. 


---

## Page 27

Quick Guide to Features and Upcoming Functionality 
Creating an Offering 27 
CREATING AN OFFERING 
You can create an offering in one of two ways: 
1. Use the CD Creation Wizard. 
2. Upload a spreadsheet template containing offering information. 
 
The CD creation wizard takes you through the process step by step over a series of 5 pages. 
Notes: 
• The validation functionality prevents invalid or duplicate CUSIPs from being submitted for primary eligibility. 
• If an invalid [[CUSIP]] is entered, you will receive an error message on step 1 or step 3 of the wizard. You will then be 
unable to proceed. 
• Duplicate CUSIPs cannot be submitted through the test region. Please use different CUSIPs to test functionality. If you 
have trouble locating [[securities]], please use one of the multiple [[CUSIP]] generator apps that are available online. 
 
CD Creation Wizard: Primary Offering 
To create an offering using the CD Creation Wizard: 
1. Click Create CD from the menu bar. 
 
2. Click Primary Offering. 
 
 
  


---

## Page 28

Quick Guide to Features and Upcoming Functionality 
Creating an Offering 28 
1. [[CUSIP]]  
In step 1 of the wizard, you can enter a [[CUSIP]] that will be part of your offering.  
Note: 
You are only able to enter a [[CUSIP]] once, even for test purposes. 
 
This allows the application to: 
1. Validate the [[CUSIP]], and 
 
2. Search whether another user has already set up an offering with this [[CUSIP]].  
• When you enter a [[CUSIP]] in this step, you are notified if the [[CUSIP]] exists as part of another offering. 
This applies to other offerings created by your firm or another firm. 
o If the [[CUSIP]] was already entered as part of another offering created by your firm, you will be 
notified and can view or modify that offering as needed. 
o If you are a [[DTC]] [[Member]] with multiple [[participant]] numbers or correspondent relationships, you 
can either view or modify the offering as needed or continue and create an offering under a 
different UW [[ID]].  
 
• If a match is found against a different UW firm, a number of fields on the Offering page (step 2) are 
pre-populated. All of the fields are editable with the exception of the Digital Certificate field. 
You can then populate any blank fields and advance to the Security Detail page (step 3). 
 
• This pre-population also affects entry on the Security Detail page (step 3): all fields except the 
Takedown Amount/[[shares]] fields are pre-populated. The [[CUSIP]] field may not be edited on this 
page.  


---

## Page 29

Quick Guide to Features and Upcoming Functionality 
Creating an Offering 29 
2. Offering 
Step 2 of the wizard captures the necessary offering-level information. UWC auto-selects the [[issuer]], if found, 
according to the six-digit base of the [[CUSIP]] entered in step 1.  
If a match is found on particular fields on the [[CUSIP]] page (step 1), a number of the Offering fields will be pre-
populated. All of the fields are editable with the exception of the Digital Certificate field. You can then populate 
any blank fields and advance to the Security Detail page (step 3) by clicking Continue. 
 
Note: 
[[securities]] issued by credit unions are out of scope for Phase 1 of UWC.  
You must define if the [[issuer]] of a security is a credit union via the UI and via Upload. If the [[issuer]] is a credit union, then you 
will not be able to move forward. 
 
 
 

---

## Page 30

Quick Guide to Features and Upcoming Functionality 
Creating an Offering 30 
 
BLOR Requirements 
Each [[issuer]] looking to make their [[securities]] eligible at [[DTC]] must submit a Blanket Letter of Representation 
(BLOR) to establish a relationship with [[DTC]]. 
Accordingly, a new BLOR will be required for any [[issuer]] leveraging the digital certificate model, even if an 
existing BLOR (that predates the UWC system) is on file. 
If the [[issuer]] does not have a BLOR on file, you will be notified after clicking Continue to move from step 2 to 
step 3. You will have the ability to send the BLOR directly to the [[issuer]] from within the application: 
 
1. Click Add [[issuer]] BLOR to attach a BLOR to this offering. 


---

## Page 31

Quick Guide to Features and Upcoming Functionality 
Creating an Offering 31 
 
2. To activate a row for entry, click its checkbox. 
3. Type the [[issuer]] contact information. 
4. Repeat for all contacts at the [[issuer]] to whom you want to send this BLOR request. 
5. Click Submit. 
The request for the BLOR is sent to all indicated contacts at the [[issuer]]. 
Note: 
• The first recipient to open the BLOR request locks it for use.  
Note: 
You [[DO]] not have to send a BLOR request to the [[issuer]] to continue through the Offering wizard (and save as a draft). 
However, a BLOR must be approved before an offering can be digitally signed. 
  


---

## Page 32

Quick Guide to Features and Upcoming Functionality 
Creating an Offering 32 
3. [[securities]] 
Step 3 of the wizard is where UWC captures the security-level information.  
CD issues can now include up to 100 [[securities]]. You can add additional [[securities]] by clicking the + Add New 
Security link in the left side navigation panel. You will also be prompted to add new [[securities]] before leaving 
this step of the wizard.  
Note: 
Each security you enter must be saved before you can enter an additional security.  
Once the [[securities]] are saved, you can navigate between [[securities]] using the panel on the left.  
 
If the previous page (Offering, step 2) was prepopulated with [[CUSIP]] details, these fields are prepopulated here 
as well. The only field requiring population is Takedown Amount.  
[[DTC]] Participants with multiple UW IDs and / or a correspondent relationship can select the UW [[ID]] for the 
correspondent firm on whose behalf the [[participant]] is submitting.  


---

## Page 33

Quick Guide to Features and Upcoming Functionality 
Creating an Offering 33 
 
If a [[participant]] [[ID]] is selected, the UW details are copied to the crediting [[participant]] section. If a correspondent 
is selected, the user must define the crediting [[participant]] based on the established relationships with the 
correspondent.  
When all fields have been populated, click Continue to move to step 4. 
You can also click Save to save a draft version of this offering. 
Note:  
If your issue has more than one [[CUSIP]] base and a BLOR is not on file, then another BLOR modal will display. From here, 
you can direct the BLOR to the [[issuer]] for signature.   
  


---

## Page 34

Quick Guide to Features and Upcoming Functionality 
Creating an Offering 34 
4. Submit to [[DTC]] 
Step 4 of the wizard allows you to review your offering-level and security-level information prior to submitting it 
to [[DTC]]. Please note the Offering [[ID]] that is generated at this step: it will be needed to search for this record 
using the Quick Search. 
 
Click the Edit icon  in the Offering Details or Security Details areas to edit information in those fields. 
Use the left side navigation panel to view the details of other [[securities]] in your issue.  
Once all changes have been made and the information is ready to go, click Submit to [[DTC]]. 
  


---

## Page 35

Quick Guide to Features and Upcoming Functionality 
Creating an Offering 35 
5. Submit to [[issuer]] 
Step 5 of the wizard, the final step in the submission process, incorporates the Digital Certificate workflow.  
In order for the security to close, the CD ([[CUSIP]]) created as part of the offering must be disseminated to the 
[[issuer]] for e-signing.  
Upon arrival at this step, the security’s Status may display as “Pending [[DTC]] Review”. In this case, the offering 
still needs to satisfy prerequisites to meet [[DTC]] approval.  
 
The security can be distributed to the [[issuer]] once the status reads “Ready for Submission.”  
 
To send the digital certificate to the [[issuer]]: 
1. Enter the [[issuer]] Contact Details in the box on the right.  
It is important to input this information accurately: this dictates who will receive the Digital 
Certificate via email.  
Note: 
You can enter up to five recipients for the digital certificate. This allows for a number of people with the ability to sign 
the certificate for their firm. 
The first person to view the certificate locks it for use. Subsequent attempts to open the certificate for signing will be 
presented with an alert: 


---

## Page 36

Quick Guide to Features and Upcoming Functionality 
Creating an Offering 36 
 
If the user wishes to exit the e-certificate, they must select “Finish Later” as opposed to just closing out the screen. 
Otherwise, the form will remain locked. 
To enter multiple recipients: 
 
a) Fill in the information for the first recipient. 
b) Click Save [[issuer]]. 
The recipient’s information appears below the entry fields. 
c) Click Add [[issuer]]. 
d) Enter the information for the second recipient in the entry fields. 
e) Click Save [[issuer]]. 
The second recipient’s information appears below the entry fields. 
f) Repeat for all subsequent recipients.  
You may enter up to 5 recipients per offering. 
 
2. After all recipients are entered, click the check box to the left of the [[CUSIP]].  
 
 


---

## Page 37

Quick Guide to Features and Upcoming Functionality 
Creating an Offering 37 
3. Click Submit Selected.  
• The status changes from “Ready for Submission” to “Pending [[issuer]] Signature.”  
• The informational icon now displays your User [[ID]] and the time at which the certificate was triggered 
for dissemination.  
 
4. All [[issuer]] contacts indicated in step 5 receive an email with a link to the web form where they can review, 
re-assign, decline, or sign the Digital Certificate. These updates are then reflected in the status.  
For more information, please see the [[issuer]] DocuSign FAQ. 
 
[[issuer]] contact information will remain visible on step 5. If a security is added to your issue after the first 
certificate is sent, then the UW can [[Reuse]] the same [[issuer]] contacts or update as necessary.  
Note:  
Status updates on the Submit to [[issuer]] screen will be reflected every 15 minutes. 
 
To check back in on the status of a Digital Certificate: 
1. Go to the Dashboard. 
 
2. Hover over the icon in the Inventory Status column. 
A tooltip appears that explains the inventory status of this offering. 
 
3. Click the link in the tooltip popup.  
This returns you to the Submit to [[issuer]] screen (step 5). 
 
4. Review step 5 to check for updates.  
The status changes when an action has been taken by the [[issuer]] (e.g. “Signed”).  
The mouse-over information changes to reflect the status. 

---

## Page 38

Quick Guide to Features and Upcoming Functionality 
Creating an Offering 38 
 
Undeliverable Items 
The inventory status displays as “Undeliverable” (in the Dashboard grid as well as in step 5) if the digital 
certificate is sent to an invalid address. When an issue has this status, UWC is unable to resend this certificate. 
In this case: 
1. The user must contact the [[DTC]] specialist assigned to this issue.  
2. The specialist then voids the security. 
3. Once a security’s status has been updated to “Voided,” a user at your firm can update security details in 
step 4 as needed and/or re-enter the [[issuer]] contact information in step 5 and resubmit the certificate. 
Managing Draft Offerings 
Clients can now manage drafts that have not been submitted to [[DTCC]]. 
Users can access their draft offerings using the Offering [[ID]] in one of two ways: 
• Via the Dashboard Quick Search, or by 
• Clicking Edit  next to the draft offering.  
This returns you to step 4 of the CD Offering wizard.  
o From step 4, you will need to select the edit icon  next to the Offering Details or Security 
Details section. 


---

## Page 39

Quick Guide to Features and Upcoming Functionality 
Creating an Offering 39 
o If a data element is updated, you must continue advancing through the workflow and resubmit your 
offering to ensure changes are captured by [[DTC]]. 
 
You can also delete pure drafts by selecting the Delete  icon next to the offering in the grid.  
Offerings that are in pure draft status for 30 days or more (based on the “last updated” timestamp) will be 
systematically purged. 
Modifying [[securities]] After Dissemination 
All security fields are modifiable until the electronic certificate is sent to the [[issuer]] for signature. If a security is 
inflight to the [[issuer]] and your security requires updates, please either: 
• Reach out to the [[issuer]] to “Decline” the certificate via DocuSign, or 
• Reach out to a UW Specialist to “void” the certificate. 
 
If a certificate is already electronically signed by the [[issuer]] and you need to make a modification to security 
features, then a [[DTC]] specialist must destroy the certificate.  
You will receive an Alert once the destroy certificate process is complete. The alert indicates that the security is 
open for modification.  
It is imperative that you finalize the security details (including the takedown amount) prior to submitting the 
certificate to the [[issuer]] for electronic signature. 
 
Creating a Secondary Offering 
A secondary offering enables underwriters to submit additional [[shares]] for a CD that is already [[DTC]]-eligible. As 
part of Phase 1 of this project, [[Secondary Offerings]] are only available if the [[CUSIP]] was made eligible via UWC. 
To create an offering using the CD Creation Wizard: 
1. Click Create CD from the menu bar. 
 
2. Click Secondary Offering. 
 


---

## Page 40

Quick Guide to Features and Upcoming Functionality 
Creating an Offering 40 
 
 
You are brought to step 1 of the CD creation wizard. The rest of the entry process is the same with the 
following exceptions: 
• Upon entering the [[CUSIP]] in step 1, you are notified if a security does not qualify as a secondary offering. 
If the security qualifies, then you are able to advance to the next step. 
 
• When the [[CUSIP]] meets the criteria for a secondary offering, most of the offering-level data in step 2 and 
the security-level data in step 3 are populated from the primary offering. This data is uneditable aside from 
the following fields: 
o Closing Date 
o Brokerage Agreement Date, and 
o Takedown Amount. 
The [[underwriter]] must populate these fields. 
Creating Offerings via Spreadsheet Upload 
You can use a specialized template to upload up to 100 [[securities]] for an issue at a time. This spreadsheet 
template is available for download via UWC. You can also search previously uploaded submissions. 
To create an offering via spreadsheet upload: 
1. Click Create CD from the menu bar. 
 


---

## Page 41

Quick Guide to Features and Upcoming Functionality 
Creating an Offering 41 
 
2. Click Upload Offering. 
The Create Certificate of Deposit by Excel Upload page appears. 
 
 
 
3. In the Upload Template section, click Download Template to get the spreadsheet template for first use. 
Note: 
You must download this template to use with UWC. The template used for UW Source is not compatible with UWC. 
 
4. Fill out the spreadsheet template and save it locally.  
 
5. In the Upload Template section, select the [[underwriter]] Type and name of the crediting [[participant]] or 
correspondent from the drop-down menus and click Add.  
This step attaches the [[underwriter]] to the upload. [[DTC]] participants with multiple [[Underwriting]] IDs and/or a 
correspondent relationship can select the UW [[ID]] for the firm on whose behalf the user is submitting.  
After selection, the [[underwriter]] information populates the Upload Template section. 
 
6. Click Browse to browse for the spreadsheet that you saved locally. 
After you select a spreadsheet, the Upload button turns blue. 
 


---

## Page 42

Quick Guide to Features and Upcoming Functionality 
Creating an Offering 42 
7. Click Upload. 
UWC displays a message to let you know if your upload has been successful: 
 
 
or unsuccessful: 
 
 
Using the Spreadsheet Template 
The spreadsheet template offered within UWC allows for quick and easy entry of offerings with multiple 
[[securities]]. The spreadsheet is associated with the proper crediting [[participant]] or correspondent as part of the 
upload process.  
There are two tabs in the template: “Offering” and “CorpCDs-01.” 
Notes: 
• [[DO]] not change the name of either tab in the template. The template will be rejected by UWC if the tab names have 
been altered. 
• [[DO]] not hide or delete any rows or columns in the spreadsheet. 
• [[DO]] not enter data into any fields that [[DO]] not require data. Use only the fields that apply to this offering. 
  


---

## Page 43

Quick Guide to Features and Upcoming Functionality 
Creating an Offering 43 
Offering Tab 
The first sheet contains [[BASIC]] information as well as a helpful color key for the template. 
 
• The only fields that you need to fill out are white or orange.  
• Orange fields are only required if you are modifying an existing offering. 
• Other fields are either static, system-generated, or [[DO]] not apply to this offering type at this time (and may 
be used in the future). 
 
1. On this first sheet, fill out the Action field with either “Create” for a new offering or “Amend” for an existing 
offering. 
 
2. If the action is “Amend,” populate the UWC Offering [[ID]] field with the [[ID]] of the offering that you are 
editing. 
 
  


---

## Page 44

Quick Guide to Features and Upcoming Functionality 
Creating an Offering 44 
CorpCDs-01 Tab 
The second sheet contains all of the issue information and security details for the offering. 
 
Note: 
Clicking in any field provides a pop-up box containing a field definition or other information about how to fill out that field. 
For a new offering: 
1. Select “Create” in the Action (Create/Amend) field under “Issue / Reference Information” (field C7).  
 
2. Specify the Number of [[securities]] in cell C10. 
 
3. Enter the [[issuer]] Base [[CUSIP]] in cell C14. 
 
4. Enter the Expected Closing Date in cell C20. 
 
5. Select “Yes” for the Digital Master Certificate in cell C43.  
 
6. Enter the current or a past date into the Brokerage Agreement Date field in cell C44.  
 
7. Enter the [[issuer]] Contact Information of the [[issuer]] who will receive the digital certificate for 
signatures. You can enter up to 5 contacts.  
The [[issuer]] contact information will be displayed on the Submit to [[issuer]] page of the offering 
workflow. This information can be changed as necessary. 
 


---

## Page 45

Quick Guide to Features and Upcoming Functionality 
Creating an Offering 45 
8. Enter “Create” in the Action (Create/Amend) field under “Security / Reference Information” (field 
F5). 
 
9. Enter the rest of the Security Information as necessary and submit up to 100 [[securities]] per issue. 
 
10. Be sure to save your spreadsheet in an accessible location before uploading it to [[Underwriting]] 
Central. 
 
For an amended offering: 
1. Select “Modify” in the Action (Create/Amend) field under “Issue / Reference Information” (field C7).  
 
2. Select “Modify” in the Action (Create/Amend) field under “Security / Reference Information” (field 
F5). 
 
3. Enter the Issue [[ID]] in the UWC Issue [[ID]] field (field C9, marked in orange). Note: The Issue [[ID]] is 
similar to the Offering [[ID]] on the Offering tab. Add an uppercase “I” after the first two characters 
“CD” in the offering [[ID]] to obtain the issue [[ID]]. (Example: CDI21011300999) 
 
4. Confirm the [[CUSIP]] is present in the security you are looking to modify (in cell F9 and beyond). 
 
5. Add or change the amended information in any applicable white field. 
Note: 
If you are modifying an uploaded record, you must include all security details in the submission and only modify 
the necessary fields. 
6. Be sure to save your spreadsheet in an accessible location before uploading it to [[Underwriting]] 
Central. 
 
 

---

## Page 46

Quick Guide to Features and Upcoming Functionality 
Viewing an Audit Trail 46 
VIEWING AN AUDIT TRAIL 
You can view a snapshot of your submissions to [[Underwriting]] Central via the Audit trail functionality. 
1. Click Audit Trail from the UWC menu bar. 
You are brought to the Audit Trail search page. 
 
 
 
2. Select the search criterion from the drop-down list. 
You can search by [[CUSIP]], Issue [[ID]], or Offering [[ID]]. 
 
3. Enter the item number for your search. 
 
4. Click Search. 
UWC returns the audit trail for the item specified in your search.  
• The top part of the screen is populated with your search details.  
• The audit contains a list of all actions that have been taken upon the offering, starting with its 
creation. 
• You can download the search results in an excel spreadsheet by clicking the  button above the 
grid. 
• You can search for particular character strings within the table by using the filter field. 
 


---

## Page 47

Quick Guide to Features and Upcoming Functionality 
Viewing an Audit Trail 47 
 
 
 


---

## Page 48

Quick Guide to Features and Upcoming Functionality 
Special Events / Items 48 
SPECIAL EVENTS / ITEMS 
Letter of Possession 
In the extreme circumstance that [[DTC]] is unable to obtain a signed electronic certificate for a security or issue, 
a Letter of Possession (or “LOP”) provides clients with an alternative method to satisfy inventory. An LOP 
request must be discussed and approved by a [[DTC]] team [[Member]]. Issuances marked “LOP” display a yellow 
warning sign in the inventory status column on the Dashboard. Since the electronic certificate has not been 
received by [[DTC]] or e-signed, the Status column in step 5 reads “LOP.” The LOP status remains until the LOP 
is removed from the issue, usually when the e-certificate is received by [[DTC]].  
Issues closed with LOP can be filtered on the Closing tile. The statuses available here are: 
• All. Displays all items pending closure the current business day, items closed the current and previous 
business day, and items closed with LOP 
• Open. Displays only open items. 
• Closed. Displays issues that have closed on the current business day, closed with LOP, or closed the 
previous business day  
• Closed with LOP. Displays only those issues closed with LOP. 
Deleting an Offering 
You can delete a primary or secondary offering either by using the Dashboard or via step 3 of the entry wizard. 
• If you delete an offering using the dashboard, then all [[securities]] in the offering will be deleted.  
• If you opt to delete from step 3, then only the applicable security will be deleted.  
• If you delete the only security in your offering from step 3, then the entire offering will be deleted. 
 
You will receive a confirmation when the security or offering is deleted. 
Deletion Restrictions 
1. You cannot delete [[securities]] or offerings with signed certificates. You will have to destroy the certificate 
prior to deleting the offering / security. A pop-up modal will alert you if a security was already signed, 
giving you the opportunity to destroy certificates related to the offering. 
2. You cannot delete a [[CUSIP]] if it is the only [[CUSIP]] in the issue that matches the base specified in step 2. 
In this case, you will receive an error message. 
3. Due to a system restriction, you are unable to delete [[securities]] between 5:15 p.m. and 9:00 p.m. Eastern 
time. 
  

---

## Page 49

Quick Guide to Features and Upcoming Functionality 
Special Events / Items 49 
Postponing an Offering 
If an issue’s closing date is changing and you [[DO]] not know the new closing date, you can “Postpone” the issue 
via the Actions column on your Dashboard. 
• “Postpone” is only available for issues that have a single [[underwriter]] and no shared CUSIPs.  
• You can postpone once any [[CUSIP]] in your issue is [[settlement]] eligible and when the offering contains no 
CUSIPs in draft. 
• You can postpone an offering when your issue is in “Hold” status. 
• You will receive a confirmation when the offering is postponed.  
If you search for a postponed item, then step 4 displays a “Postponed” message:  
Once postponed, items will display with red text on the Dashboard. Hovering your cursor over the Offering [[ID]] / 
Issue of the postponed item displays the message “Offering is Postponed.” 
 
The closing date for postponed items displays as “12/31/9999.” The offering appears as the last record on the 
dashboard (unless you have sorted your items by “Closing Date”). 
If an issue is postponed, all alerts applicable to the issue are automatically cleared. OFAC and Crediting 
Participation confirmation must be reprocessed upon reactivation of the postponed offering. 
Postponing Restrictions 
You cannot postpone an offering with signed certificates. You must destroy the certificate prior to postponing 
the offering. A pop-up modal alerts you if a security was already signed, giving you the opportunity to destroy 
certificates related to the offering. 
  


---

## Page 50

Quick Guide to Features and Upcoming Functionality 
Special Events / Items 50 
Destroying a Certificate  
Postpone / Delete  
If you attempt to delete or postpone a security or offering that includes a signed certificate, the application 
displays a pop-up modal alerting you that the certificate(s) must be destroyed prior to deletion. You can destroy 
the certificate using this modal. 
 
You will receive an alert when the certificate is destroyed. You can then repeat the delete / postpone request. 
Alerts  
If a certificate is destroyed due to a delete / postpone request, UWC sends an alert to the client that initiated 
the destruction upon its completion. 
  


---

## Page 51

Quick Guide to Features and Upcoming Functionality 
Special Events / Items 51 
Reactivating an Issue 
To reactivate an issue or remove it from a “Postpone” state, you must enter a valid closing date in step 2 and 
advance to step 3. 
You must then enter or update the appropriate security details (e.g. valid interest dates).  
Note: 
Please remember to update interest dates: these may have changed due to the modification of the closing date.  
 
Once the security details are updated, proceed to step 4 and then submit the offering to [[DTC]]. Once submitted, 
the offering is now reactivated.  
Note: 
Standard modification / validation rules apply. 
Once reactivated, all necessary [[DTC]] processing takes place again: the OFAC must be rescanned and CP 
status is reverted to “Pending Confirmation.” Crediting participants must re-confirm the issue in order to 
achieve [[DTC]] eligibility. 
 


---

## Page 52

 
 
 
FOR MORE INFORMATION 
 
Email [[Underwriting]] Product Management at: 
UWCPM@[[DTCC]].com 