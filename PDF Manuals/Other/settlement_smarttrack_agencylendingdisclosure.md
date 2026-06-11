---
title: "settlement_smarttrack_agencylendingdisclosure.pdf"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/settlement_smarttrack_agencylendingdisclosure.pdf"
pages: 15
size: "414.4 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# settlement_smarttrack_agencylendingdisclosure.pdf

**Original File:** [settlement_smarttrack_agencylendingdisclosure.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/settlement_smarttrack_agencylendingdisclosure.pdf)  
**Category:** Other  
**Total Pages:** 15  
**File Size:** 414.4 KB  

---

## Page 1

   
 


---

## Page 2

  Contents 
   
 
Agency Lending – Help  ii 
 
Table of Contents 
SMART/Track for Agency Lending Disclosure - Overview ............................................................................. 3 
Welcome to SMART/Track for Agency Lending Disclosure ...................................................................... 3 
About File Processing ................................................................................................................................ 4 
About OFAC ............................................................................................................................................... 4 
About Unique Identifiers .......................................................................................................................... 4 
Creation process ................................................................................................................................... 4 
Searching for principal lender details ................................................................................................... 5 
Browsing File Input Errors ............................................................................................................................. 6 
To browse input errors ............................................................................................................................. 6 
Browsing File Output/Receipt Errors ............................................................................................................ 7 
To browse output errors ........................................................................................................................... 7 
Browsing File Processing Status .................................................................................................................... 8 
To browse file processing status ............................................................................................................... 8 
Requesting a Unique Identifier ................................................................................................................... 10 
First, verify the unique identifier ............................................................................................................ 10 
If no unique identifier exists... ................................................................................................................ 10 
Browsing for Principal Lender Details ......................................................................................................... 12 
Browse Errors Status page ...................................................................................................................... 13 
Browsing File Processing Status page ..................................................................................................... 14 
Browse Output/Receipt Errors Status page ............................................................................................ 15 
 

---

## Page 3

  Overview 
   
 
Agency Lending – Help  3 
 
SMART/Track for Agency Lending Disclosure - Overview 
 
Welcome to SMART/Track for Agency Lending Disclosure 
The SMART/Track for Agency Lending Disclosure service facilitates increased transparency in 
[[securities]] lending by providing a communications link between agent lenders and borrowers for the 
transmission of daily and periodic data files. 
 
Agent lenders and borrowers can use the service to transmit and receive, either directly or through a 
vendor, loan information for credit monitoring and capital requirement purposes. Previously, 
[[Broker]]/dealers that borrowed [[securities]] against [[collateral]] could not effectively monitor, at the 
principal level, exposure, credit risk, or capital requirements. With disclosure of principal lender 
identities, borrowers can adjust, if necessary, any [[collateral]] posted for the [[securities]] borrowed. 
 
Additionally, SMART/Track for Agency Lending Disclosure enables agent lenders and borrowers to 
obtain via the Web unique identifiers for those principal lenders that [[DO]] not have U.S. tax 
identification numbers. 
 
For more information: 
 About Unique Identifiers  
 About File Processing  
 Procedures  
 Field Definitions  
  


---

## Page 4

  Overview 
   
 
Agency Lending – Help  4 
 About File Processing 
There are five files sent between participants: three for credit purposes and two for regulatory capital 
and daily concentration monitoring. 
File Name File 
Function 
From/To Frequency 
Credit Incremental 
Add/Delete 
AGI Sent from lender to [[Borrower]] 
to request approval of new 
principal lender.  
As needed or whenever a 
new principal lender is 
added or deleted. 
Credit [[Borrower]]'s 
Approval Response 
AGA Sent from [[Borrower]] to lender 
to approve or deny a new 
principal lender.  
In response to a request to 
approve or deny a new 
principal lender. 
Credit Master AGM Sent from lender to [[Borrower]]. 
At a minimum, list of all 
approved principals (for 
reconciliation purposes). 
At least annually (bi-lateral 
agreement to send more 
often). 
Daily Loan Data AGD Sent from lender to [[Borrower]]. 
Allocation of daily loans by 
principal lender.  
Daily. 
Daily Non-Cash [[collateral]] 
Data 
AGN Sent from lender to [[Borrower]]. 
Allocation of specific non-cash 
[[collateral]] to each principal 
lender.  
Daily. 
About OFAC 
The Office of Foreign Assets Control (OFAC) of the US Department of the Treasury administers and 
enforces economic and trade sanctions based on US foreign policy and national security goals against 
targeted foreign countries, terrorists, international narcotics traffickers, and those engaged in 
activities related to the proliferation of weapons of mass destruction.  
 OFAC acts under Presidential wartime and national emergency powers, as well as authority granted 
by specific legislation, to impose controls on transactions and freeze foreign assets under US 
jurisdiction. Many of the sanctions are based on United Nations and other international mandates, 
are multilateral in scope, and involve close cooperation with allied governments. 
About Unique Identifiers  
Most principal lenders have a U.S. taxpayer identification number and this number is a required 
element in the loan file transmitted between agent lenders and borrowers. However, since some U.S. 
and many foreign principal lenders [[DO]] not have U.S. Tax IDs, alternative identification is required. The 
Agency Lending Disclosure system provides this alternative by assigning unique identifiers to principal 
lenders without U.S. Tax IDs. 
Creation process  
Agent lenders request unique identifiers for principal lenders. [[DTCC]] administers the unique identifier 
database, allowing one unique identifier for each principal lender. Agent lenders requesting a unique 
identifier for a principal lender that already has one will be prompted to that effect. 

---

## Page 5

  Overview 
   
 
Agency Lending – Help  5 
Searching for principal lender details 
You can use a unique identifier, the principal lender's name, or the creation date of the unique 
identifier to search the Agency Lending Disclosure service for detailed information about the principal 
lender. See Browsing for Principal Lender Details. 
  

---

## Page 6

  Browsing File Input Errors  
 
Agency Lending – Help  6 
 
Browsing File Input Errors  
You can browse the Agency Lending Disclosure application to view any processing errors in files sent 
between agent lender and [[Borrower]].  
To browse input errors 
1. On the SMART/Search Agency Lending Disclosure menu, click File Status Browse. 
The Browser File Processing Status page appears with your Signon [[ID]] pre-filled. 
2. In the Go To field, select Browse Errors from the drop-down list. 
The Browse Errors page appears. For information about the fields on this page, see Browse 
Errors Status page field definitions. 
3. In the Job Type field, select either Output or Receipt. 
Selecting Output retrieves errors in processed files. Selecting Receipt retrieves errors in receipts 
for processed files. 
4. In the Function field, select the file type for which you want to view errors, either the AGD - 
Daily Loan Data Detail file, the AGM - Master file, the AGI - Incremental file, the AGA - Approval 
by [[Borrower]] file, the AGN - Daily Non-Cash [[collateral]] file, or All files. 
5. In the Error Start Date field, type the start date of the error file for which you are seeking status. 
You can use the Calendar icon to the right of the Error Start Date field to select a date. 
6. In the Error Start Time field, type the error file creation time in hours/minutes/seconds format. 
7. Click Search. 
The lower half of the page displays the error records of file processing and receipt errors based 
on the criteria you entered. If there are more than one page of errors, click Next to see the next 
page and Previous to return to the previous page.  

---

## Page 7

  Browsing File Output/Receipt Errors 
 
Agency Lending – Help  7 
 
Browsing File Output/Receipt Errors  
You can browse the Agency Lending Disclosure application to view all file requests that cannot be 
matched to an input file, either due to an error in the request or lack of available data for retrieval.  
To browse output errors 
1. On the SMART/Search Agency Lending Disclosure menu, click Browse Output/Receipt Errors. 
The Browser File Processing Status page appears with your Signon [[ID]] pre-filled. For information 
about the fields on this page, see Browse Output/Receipt Errors Status page field definitions. 
2. In the Job Type field, select either Output or Receipt. 
o Select Output to view requests for output for which no data is available for retrieval 
or 
to view requests for output containing errors that are preventing retrieval. 
o Select Receipts to see requests for receipts (acknowledgement that the receiver received 
your file) for which no data is available for retrieval 
or 
to see requests for receipts containing errors that are preventing retrieval. 
3. In the Function field, select the file type for which you want to view errors, either the AGD - 
Daily Loan Data Detail file, the AGM - Master file, the AGI - Incremental file, the AGA - Approval 
by [[Borrower]] file, the AGN - Daily Non-Cash [[collateral]] file, or All files. 
4. In the Error Start Date field, type the start date of the error file for which you are seeking status. 
You can use the Calendar icon to the right of the Error Start Date field to select a date. 
5. In the Error Start Time field, type the error file creation time in hours/minutes/seconds format. 
6. Click Search. 
The lower half of the page displays the output/receipt error records based on the criteria you 
entered. If there are more than one page of errors, click Next to see the next page and Previous 
to return to the previous page.  
 

---

## Page 8

  Browsing File Processing Status 
 
Agency Lending – Help  8 
 
Browsing File Processing Status  
You can browse the Agency Lending Disclosure application to determine the status of files you have 
sent and to view a snapshot of file activity to determine if there are files you need to retrieve.  
 
Note: If you have errors in your input request, see Browsing Input Errors. For output or receipt 
request errors, see Browsing File Output/Receipt Errors. 
To browse file processing status 
1. On the SMART/Search Agency Lending Disclosure menu, click File Status Browse. 
The Browser File Processing Status page appears with your Signon [[ID]] and [[participant]] [[ID]] pre-
filled.  
For information about the fields on this page, see Field Definitions—Browse File Processing 
Status page. 
2. In the Side field, select either Sender or Receiver from the drop-down list.  
Selecting Sender retrieves the status of files your firm has sent. Selecting Receiver retrieves files 
that you have received or displays files that await your retrieval.  
3. In the Function field, select the file type for which you want to determine status, either the Daily 
Loan Data AGD file, the Credit Master AGM file, the Credit Incremental Add/Delete AGI file, the 
Credit [[Borrower]]'s Approval Response AGA file, the Daily Non-Cash [[collateral]] Data AGN file, or 
all files.  
4. In the File Creation Date field, type the creation date of the file for which you are seeking status. 
The field defaults to the current date. Click the Calendar icon to the right of the File Creation 
Date field to select a date. Data is only available for the past seven calendar days; if you enter a 
date beyond seven days past, no data is retrieved. 
5. In the Start File Creation Time field, type the start file creation time in hours/minutes/seconds 
format. This field defaults to zeros so, if you accept the [[default]], you will retrieve files from 12:00 
midnight on.  
6. In the Status field, select a status for the type of file you want to view. 
You can retrieve a specific status or all statuses. Statuses are:  
• All Input (accepted and errors)  
• Accepted Input  
• Input Errors  
• Output Processed  
• Receipts Processed  
7. Click Search. 
The lower half of the page displays the records of the files you requested. If there is more than 
one page of records, click Next to see the next page (and Previous to return to the previous 

---

## Page 9

  Browsing File Processing Status 
   
 
Agency Lending – Help  9 
page). 
 
Each record section on the page displays the processing status for each input transmission, as 
well as the complete flow of that input transmission through the SMART/Track for Agency 
Lending Disclosure system (output and receipts).  
 

---

## Page 10

  Requesting a Unique Identifier 
 
Agency Lending – Help  10 
 
Requesting a Unique Identifier  
You request creation and assignment of a unique identifier for a principal lender from the Principal 
Agent Lender Unique Identifier **Browse** page. 
First, verify the unique identifier 
1. On the SMART/Search Agency Lending Disclosure menu, click Unique Identifier Search/Browse. 
The Principal Agent Lender Unique Identifier **Browse** page appears.  
2. In the Legal Name field, type the name of the principal lender. 
3. Click Search. 
The page fills with unique identifier information based on the name you entered. If the principal 
lender already possesses a unique identifier, it will be displayed in the Unique Identifier link. You 
can click the unique identifier link to view additional details about the Principal Agent Lender. 
If no unique identifier exists... 
1. Click Create Unique [[ID]] (on the page's lower right). 
The Request Creation of New Unique Identifier ** page appears. 
2. Type the Legal Name of the principal lender for which you are requesting a unique identifier. 
3. Select a Classification Code/Name from the codes provided in the drop-down list. 
4. Click the OFAC checkbox. 
Clicking the OFAC checkbox indicates that the agent lender has screened the principal lender 
against the OFAC database. You cannot create a unique identifier for the principal lender without 
clicking the OFAC checkbox. See About OFAC.  
5. Complete the mailing address fields as required. If the mailing and business addresses are the 
same, click the Business Address check box to populate the business address fields with the 
mailing address. 
6. Complete the Requestor Contact Information fields. 
7. Click the Create Unique [[ID]] button. 
The Confirmation Ticket window appears.  
 
Note 1: If the data you entered is similar to the data of a principal lender that already exists, the 
View Similar Name pop-up window appears. If your information matches an existing principal 
lender, click Cancel to close the View Similar Name pop-up window and cancel the operation 
(because a unique [[ID]] already exists for this particular principal lender). To return to the Principal 
Lender Identifier Browse screen and search for another identifier, click the Back button (bottom 
right of the screen). If the information does not match, click Continue. 
 

---

## Page 11

  Requesting a Unique Identifier 
   
 
Agency Lending – Help  11 
Note 2: You can also click the Reset button on the Request Creation of New Unique Identifier ** 
page to clear all fields to search for a different unique identifier.  
8. If you clicked Continue (see last sentence in Note 1 above), the Confirmation Ticket window 
appears with a unique identifier now assigned to the principal lender. 
 
You can click the Back button to request creation of another unique identifier or click the Print 
button to print the Confirmation Ticket.  
  

---

## Page 12

  Browsing for Principal Lender Details 
 
Agency Lending – Help  12 
 
Browsing for Principal Lender Details  
When browsing for principal lender details, you can search by the principal lender's legal name, by the 
principal lender's unique identifier, or by the creation date of the unique identifier. See also 
Requesting a Unique Identifier.  
1. On the SMART/Search Agency Lending Disclosure menu, click Unique Identifier Search/Browse. 
The Principal Agent Lender Unique Identifier **Browse** page appears.  
2. In the Legal Name field, type the legal name associated with the principal lender 
or 
In the Unique Identifier field, type the unique identifier for which you want details  
or 
In the Unique [[ID]] Creation Date field, type the creation date of the unique [[ID]].  
3. Click Search. 
The page fills with unique identifier information based on the criteria you entered. You can click 
the Next link to view any additional pages of unique identifiers or the Previous link to return to 
the page from which you started.  
4. To view the details of a specific unique identifier, click the appropriate Unique Identifier link. 
The Principal Agent Lender Unique Identifier **Detail Information** page appears 
or 
If there is no unique identifier for the principal lender, click the Create Unique [[ID]] button (in the 
lower right corner of the window).  
  
  

---

## Page 13

  Browsing for Principal Lender Details 
   
 
Agency Lending – Help  13 
Browse Errors Status page 
Items marked with a red asterisk (*) are required.  
In this field You can 
Calendar * Click this icon to open the calendar pop-up page where you can select a date for 
the File Creation Date field. 
Error Start Time * Type the creation time (in hours/minutes/seconds format) of the file for which 
you wish to view processing errors. 
Error Start Date * Type the start date of the file for which you wish to view processing errors. You 
can also select a date and enter it automatically by clicking the Calendar icon to 
the right of the File Creation Date field. 
Function * Select one or all of the following files to view processing errors:  
 AGD - Daily Loan Data Detail file  
 AGM - Master file  
 AGI - Incremental file  
 AGA - Approval by [[Borrower]] file  
 AGN - Daily Non-Cash [[collateral]] file  
Go to Display additional Agency Lending Disclosure functions that you can access. 
Job Type * Select either Output or Receipt. Selecting Output retrieves errors in processed 
files. Selecting Receipt retrieves errors in receipts for processed files. 
Next Click to go to the next page of file processing status records. 
Previous Click to go to the previous page of file processing status records. 
Reset Reset the page's fields to what they were when you first opened the page. 
Search Click this button to retrieve file processing statuses based on the criteria you 
entered. 
  
  
  

---

## Page 14

  Browsing for Principal Lender Details 
   
 
Agency Lending – Help  14 
Browsing File Processing Status page 
Items marked with a red asterisk (*) are required. 
In this field You can 
Calendar * Click this icon to open the calendar pop-up page where you can select a date for 
the File Creation Date field. 
File Creation Date * Type the creation date of the file for which you wish to view processing status. You 
can also select a date and enter it automatically by clicking the Calendar icon to the 
right of the File Creation Date field. The field defaults to the current date.  
File Creation Time * Type the creation time (in hours/minutes/seconds format) of the file for which you 
wish to view processing status. The field defaults to zeros.  
Function * Select one or all of the following files to retrieve file status:  
 AGD - Daily Loan Data Detail file  
 AGM - Master file  
 AGI - Incremental file  
 AGA - Approval by [[Borrower]] file  
 AGN - Daily Non-Cash [[collateral]] file  
Go to Display additional Agency Lending Disclosure functions that you can access. 
Next Click to go to the next page of file processing status records. 
Previous Click to go to the previous page of file processing status records. 
Reset Reset the page's fields to what they were when you first opened the page. 
Search Click this button to retrieve file processing statuses based on the criteria you 
entered. 
Side * Select either Sender (the Send side) or Receiver (the Receive side). Selecting 
Sender retrieves the processing status of files that your firm sent. Selecting 
Receiver retrieves processing status of files that you have received or that are 
available for retrieval. 
Status * Select one or all of the following types of file processing statuses:  
 All Input (Accepted and Errors) 
All files that have been input but not yet processed, regardless of whether 
they were accepted or contained errors  
 Accepted Input 
Inputted files that have been accepted but not yet processed  
 Input Errors 
Inputted files that have errors and will not be processed  
 Output Processed 
Inputted files that have been processed for output  
 Receipt Processed 
Inputted files that have been processed for output and a receipt was also 
requested  
  

---

## Page 15

  Browsing for Principal Lender Details 
   
 
Agency Lending – Help  15 
Browse Output/Receipt Errors Status page 
Items marked with a red asterisk (*) are required.  
In this field You can 
Calendar * Click this icon to open the calendar pop-up page where you can select a date for 
the File Creation Date field. 
Error Start Time * Type the creation time (in hours/minutes/seconds format) of the file for which 
you wish to view processing errors. 
Error Start Date * Type the start date of the file for which you wish to view processing errors. You 
can also select a date and enter it automatically by clicking the Calendar icon to 
the right of the File Creation Date field. 
Function * Select one or all of the following files to view processing errors:  
 AGD - Daily Loan Data Detail file  
 AGM - Master file  
 AGI - Incremental file  
 AGA - Approval by [[Borrower]] file  
 AGN - Daily Non-Cash [[collateral]] file  
Go to Display additional Agency Lending Disclosure functions that you can access. 
Job Type * Select either Output or Receipt. Selecting Output retrieves errors in processed 
files. Selecting Receipt retrieves errors in receipts for processed files. 
Next Click to go to the next page of file processing status records. 
Previous Click to go to the previous page of file processing status records. 
Reset Reset the page's fields to what they were when you first opened the page. 
Search Click this button to retrieve file processing statuses based on the criteria you 
entered. 
  
  
 
 