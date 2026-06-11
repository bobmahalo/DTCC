---
title: "CMU CSV Trade Batch Upload Quick Reference Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cmu109r_csv_trade_batch_upload_2021Aug5.pdf"
pages: 15
size: "528.6 KB"
category: "Connectivity_MQ"
ingested_on: "2026-06-05"
---

# CMU CSV Trade Batch Upload Quick Reference Guide

**Original File:** [cmu109r_csv_trade_batch_upload_2021Aug5.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cmu109r_csv_trade_batch_upload_2021Aug5.pdf)  
**Category:** Connectivity_MQ  
**Total Pages:** 15  
**File Size:** 528.6 KB  

---

## Page 1

CMU CSV Trade Batch Upload Quick Reference Guide 
CORPORATE, MUNICIPAL, AND [[UIT]] 
(CMU) 
CMU CSV TRADE BATCH UPLOAD QUICK REFERENCE GUIDE 
NO
VEMBER 15, 2019 
In ex
traordinary situations, when a [[participant]] who submits the MT515 trade messages is unable to submit 
trades to RTTM through interactive messaging, [[DTCC]] Client Support can enable access to the CSV Trade 
Batch Upload page. This page allows you to upload trades, stored in a CSV file, to the CMU RTTM® Web and 
submitted to RTTM. 
This guide reviews the CSV upload process, shows the accepted formats, and walks you through how to 
upload a file to the CMU RTTM Web application. 


---

## Page 2

CMU CSV Trade Batch Upload Quick Reference Guide 
General Trade Batch Workflow 2 
GENERAL TRADE BATCH WORKFLOW 
To understand the general workflow of the CSV Trade Batch upload: 
1. Create an CSV file matching the specification described in this document. You can either [[DO]] this 
programmatically or by using the CSV File Template spreadsheet that is available as a download from the 
CMU RTTM Web application. 
2. Upload the CSV file to the CMU RTTM Web, where you can then visually inspect the trades you are about 
to submit.  
Note  
At this point, the CSV input is validated and some or all of the trade records can be rejected if there are errors. 
3. [[DO]] one of the following: 
• If the file contains errors, it is rejected allowing you to load a new, updated file. 
• If the file does not contain errors or if the user wants to submit only the valid trade records, submit the 
file to CMU RTTM Web. 
4. Receive a receipt of what was accepted or rejected by CMU RTTM Web.  
CMU RTTM Web applies more thorough and comprehensive validation; therefore, some trades may still 
be rejected after they are submitted. These rejects are typically attributed to specific business reasons 
rather than incorrect input data. 
 


---

## Page 3

CMU CSV Trade Batch Upload Quick Reference Guide 
Preparing the CSV File for Upload 3 
PREPARING THE CSV FILE FOR UPLOAD 
Q What format can I upload files? 
A The Trade Batch Upload page only accepts text-based CSV files. Any other file types, such as Microsoft 
Excel workbooks, non-CSV text files, other binary files, are rejected. 
Q Are there any content restrictions to my CSV file? 
A Yes. Each file that is loaded to CMU RTTM Web undergoes extensive validation before the content is 
submitted to CMU RTTM. Depending on the type of errors encountered during file validation, some or all 
trades could be rejected, preventing submission to CMU RTTM. 
Q How [[DO]] I upload a file to the CMU RTTM Web? 
A Contact [[DTCC]] Client Support at 1 888 382-2721, and then follow the prompt for client support . Use the 
CSV file upload process only for emergency situations. After Client Support has accepted your 
request, follow the instructions in Managing CSV Files. 
The following sections explain the validation that is performed on each file:  
Allowed Characters  
If you use any character other than the allowed characters, the entire file is rejected. The following characters 
are allowed and validated for each file:  
• Alphanumerical characters (A-Z, a-z, 0-9). 
• Dashes (-) and underscores (_). 
• Commas, as long as they are used to separate fields. Numerical fields cannot be formatted using 
commas. 
• Forward Slashes (/). These are used to represent date values. 
• Colons (:). These are used to represent time values. 
• Blank spaces. 
• Periods. 
Allowed Columns 
Each CSV file is expected to contain a minimum required column set. If any of these columns is missing, the 
entire file is rejected. Undefined columns are ignored. For more information, see Appendix A. Additionally, you 
can download the CSV File Template spreadsheet, which contains a set of sample trades and their associated 
columns. 

---

## Page 4

CMU CSV Trade Batch Upload Quick Reference Guide 
Preparing the CSV File for Upload 4 
Data Types and Format 
The data format in each column needs to match the expected data type for that column. This is done by 
formatting each column value in a specific and consistent way. Each parsed trade record checks for the proper 
format. If any errors are encountered, the entire record is rejected. Data Types for each of the columns can be 
one of the following:  
Name Description 
Unformatted 
strings 
Enter unformatted string values as is. Other than allowed characters and size of the string, there are 
really no restrictions on what can be entered. For example, Trader IDs, [[participant]] Notes, and XREFs all 
fall under this category. 
Enumerated 
strings 
Enumerated strings are values that must be picked from a list of available selections. They are 
effectively a drop down list. Appendix A explains this in greater detail. As an example, consider the 
ProductID column where you specify if this were a Municipal, Corporate, or [[UIT]] trade. In this case, only 
the following values are acceptable: MU, CP, UI.  Any other value causes the trade record to be 
rejected. 
Integers Integers are whole numbers with no decimal portion to them.  
Decimals Decimals are numbers reflecting fractions, such as 100.234, 10.2, 0.2, .01. 
Dates Specify the date fields in the MM/DD/YYYY format. Any other format causes the record to be rejected. 
 
Times Specify the time fields using the 24 hour clock with the format as HH:MM:SS. For example, 14:30:23 is 
an acceptable format, while 02:30:23 PM is not and causes the record to be rejected. 
 

---

## Page 5

CMU CSV Trade Batch Upload Quick Reference Guide 
Managing CSV Files 5 
MANAGING CSV FILES 
Ensure that the CSV file conforms to the specifications described in this document.  For guidance, use the 
template provided in the CMU RTTM Web application  
To manage CSV files: 
1. Prepare the upload. 
2. Upload the CSV file. 
3. View the CSV file content. 
4. Reject or submit the trade records to CMU RTTM Web. 
5. Review the CMU RTTM Web submission. 
Preparing the CSV File Upload 
To prepare the upload of the CSV file: 
1. Access the CMU RTTM Web Home page. 
For instructions about accessing and using CMU RTTM Web, see the CMU RTTM ® Web User Guide. 
2. From the main menu, select Trade Management > Trade Batch Upload – On Request only. 
3. Optionally, download the CSV file template spreadsheet, which contains a handful of sample trades, by 
selecting the [csv file template] link, as shown in the following figure: 
 
The following figure shows an example of the spreadsheet.  
 
  


---

## Page 6

CMU CSV Trade Batch Upload Quick Reference Guide 
Managing CSV Files 6 
Using the spreadsheet can be beneficial for the following reasons: 
o Many of the validation and formatting rules are already enforced by the template. For example, the 
spreadsheet visually shows the mandatory, optional, and conditional fields. 
o Date and Time fields are automatically converted to the correct format as long as a date or time value 
is entered. 
o Enumerated String fields are selectable using a drop down list, as shown in the following figure: 
 
4. To download the CSV file, click  Download.  
The CSV file is downloaded locally, as highlighted in the following figure: 
 
Uploading the CSV File to the CMU RTTM Web 
To upload the CSV file to the CMU RTTM Web: 
1. Access the CMU RTTM Web Home page. 
For instructions about accessing and using CMU RTTM Web, see the CMU RTTM ® Web User Guide. 
2. From the main menu, select Trade Management > Trade Batch Upload – On Request only. 
3. From the Upload CSV Batch Trade File page, browse and select the newly created CSV file.  
Keep in mind that at this point nothing has been submitted to the CMU RTTM Web. 
 
4. Click Display File. 
  


---

## Page 7

CMU CSV Trade Batch Upload Quick Reference Guide 
Managing CSV Files 7 
Viewing the CSV File Content 
To view the CSV file content: 
All parsed trades are displayed in a table. If any trades cannot be parsed because of an error with the CSV 
input, they are displayed in a separate table named Invalid Records. The details of the parsed record can be 
displayed in a separate popup window by clicking the Line Number hyperlink next to each record. When 
displaying the details of an invalid record you are able to view the reason why the record was rejected. 
Note: 
If you use the CSV file template and deletes rows from that spreadsheet, you might have trades that cannot be parsed for 
those records. To avoid this scenario, open the CSV file in a text editor, such as Notepad, to view the rows of commas at 
the end. Delete these commas, save the file, and then upload it to CMU RTTM Web. 
Access the Valid Records tab to view valid records, as shown in the following figure: 
 
  


---

## Page 8

CMU CSV Trade Batch Upload Quick Reference Guide 
Managing CSV Files 8 
Access the Invalid Records tab to view invalid records, as shown in the following figure: 
 
The following figure shows the record detail view of the single rejected record. You can hover over an invalid 
field to highlight the issue with the input. 
 
  


---

## Page 9

CMU CSV Trade Batch Upload Quick Reference Guide 
Managing CSV Files 9 
Rejecting or Submitting the Trade Records 
To reject or submit the trade records to the CMU RTTM Web application: 
Rejecting a file discards the file contents and resets the workflow. There is no penalty for rejecting or not 
rejecting a file.  
Submitting a file, sends all valid trades to the CMU RTTM Web for processing after you approve the 
confirmation. As shown in the following figure, when you click OK, the files are submitted: 
 
In general, CMU RTTM Web processes trades quickly; however, the process might take a few minutes if the 
CSV file is large. After submitting the file allow the page to refresh on its own; otherwise, you are not able to 
view the final submission results. While trades are being processed, the Reject this file and Submit Valid 
Records options are replaced with the Submitting Trades [[Option]], as shown in the following figure, to show that 
the trades are processing: 
 
Reviewing the CMU RTTM Web Submission 
To review the CMU RTTM Web submission: 
After all of the trades are submitted, they are displayed again using similar tables. Trades are separated into 
those that were accepted or pending accepted by CMU RTTM Web and those that were rejected because of a 
more specific business reason. Hovering over the details of a rejected trade highlight the reasons for the 
rejection. 


---

## Page 10

CMU CSV Trade Batch Upload Quick Reference Guide 
Appendix A: CSV Batch Trade File Structure 10 
APPENDIX A: CSV BATCH TRADE FILE STRUCTURE 
The following table shows the CSV batch trade file structure: 
Column Name Data Format Required Description 
TradeAction Enumerated String 
• INSTRUCT 
• MODIFY 
• CANCEL 
• DK 
Yes Determines the trade action being taken 
from the account or contra side. 
TradeDest Enumerated String 
• NSCCTRRS 
• NSCCREGO 
Yes Determines whether this is a Street or an 
IDRO trade.  
•  NSCCTRRS =  Street Trade  
• NSCCREF =  IDRO trade 
ProductID Enumerated String 
• MU 
• CP 
• UI 
Yes Product [[ID]] for this trade  
• MU = Municipal Trade  
• CP = Corporate Trade  
• UI = [[UIT]] Trade 
TradeReport Enumerated String 
• RTTM 
• MSRB 
• BOTH 
Yes Indicates how this trade should be 
Processed: 
• RTTM = RTTM only. No MSRB 
Reporting 
• MSRBMSRB only.  
• BOTH = Both RTTM and MSRB 
TradeType Enumerated String 
• BIL 
• QSR_SRC 
• QSR_TGT 
• SYN_SRC 
• SYN_TGT 
Yes Trade Submission Type: 
• BIL = Bilateral Trade  
• QSR_SRC = QSR Source Trade  
• QSR_TGT = QSR Target Trade  
• SYN_SRC = [[syndicate]] Source Trade 
• SYN_TGT = [[syndicate]] Target Trade 
ParticipantID Unformatted String Yes [[participant]] [[ID]] associated with the trade. 
Must be supplied as a [[FICC]] account [[ID]]. 
ParticipantCorrespondentID Unformatted String No [[participant]] Correspondent [[ID]] Max length 
allowed is 5 
ContraID Unformatted String Yes Contra [[ID]] to the trade. Must be supplied as a 
[[FICC]] Contra [[ID]] 
ContraCorrespondentID Unformatted String No Contra Correspondent [[ID]] Max length 
allowed is 32 
Xref Unformatted String Yes XREF of the Trade 
Max length allowed is 16 
BuySell Enumerated String 
• B 
• S 
Yes Indicates a Buy/Sell Trade 
• B = Buy 
• S = Sell 
 

---

## Page 11

CMU CSV Trade Batch Upload Quick Reference Guide 
Appendix A: CSV Batch Trade File Structure 11 
Column Name Data Format Required Description 
SpecialTrade Enumerated String 
• RPTO 
• CPRO 
• STDR 
Yes Special Trade Indicator  
• RPTO = Not Special  
• CPRO = Comparison Only  
• STDR = Trade For Trade [[settlement]] 
TradeDate Date (mm/dd/yyyy) Yes Trade Date 
SettlementDate Date (mm/dd/yyyy) Yes [[settlement]] Date. For trades submitted in 
Dollar Price or Yield, this should reflect a 
value of “WI” to indicate a When-Issue trade 
when [[settlement]] date is not available. 
[[CUSIP]] Unformatted String Yes [[CUSIP]] [[ID]] 
Exact string of length 9 expected. 
ReversalFlag Enumerated String 
RVSL 
No Indicates whether this trade is a reversal or 
not 
RVSL = Reversal Trade Otherwise the field 
should be left blank. 
Quantity Integer Yes Trade Quantity (Par) 
PricingMethod Enumerated String 
• FM 
• DP 
• YC 
Yes Pricing Method of the trade. Note the values 
of the following 5 fields will be dependent on 
this:  
• FM = Final Money 
• DP = Dollar Price 
• YC = Yield/Concession 
DollarPrice Decimal Depends 
on Pricing 
Method 
Trade Dollar Price 
Amount Decimal Depends 
on Pricing 
Method 
Trade Amount (Final Money) 
Yield Decimal Depends 
on Pricing 
Method 
Trade Yield 
AccruedInt Decimal Depends 
on Pricing 
Method 
Trade’s accrued interest 
Concession Decimal Depends 
on Pricing 
Method 
Trade Concession 
ExtendedSettlement Integer No Extended [[settlement]] value. Usually a 
number between 0 and 50, but it may vary. 
TraderID Unformatted String No Trader [[ID]] 
Max length allowed is 10 
TradeTime Time (hh24:mm:ss) No Time of Trade 

---

## Page 12

CMU CSV Trade Batch Upload Quick Reference Guide 
Appendix A: CSV Batch Trade File Structure 12 
Column Name Data Format Required Description 
RegPrice Decimal No Regulatory Price. 
ParticipantCapacity Enumerated String 
• PRIN 
• AGEN 
No [[participant]] Capacity.  
• PRIN = Principal  
• AGEN = Agent 
ContraCapacity Enumerated String 
• PRIN 
• AGEN 
No Contra Capacity.  
• PRIN = Principal  
• AGEN = Agent 
WeightedAvgPrice Enumerated String 
• WGTP 
No Weighted average price  
• WGTP = Indicates weighted average 
price. 
Otherwise, leave the field blank. 
AltTradingSystem Unformatted String No Alternate trading system, 
Maximum length allowed is 6. 
ReversalControl Unformatted String No Reversal control number Max length allowed 
is 16. 
SpecialCondition Unformatted String No Special Condition 
Max length allowed is 4. 
ParticipantNotes Unformatted String No [[participant]] Notes 
Max length allowed is 32. 
RegYield Decimal No Regulatory Yield 
ExecBrokerCommission Decimal No Executing [[Broker]] Commission 
TidID Unformatted String No RTTM generated reference (TID) for trades 
upon submission. 
For pre-match modifies and Cancels, can be 
used to identify or target the trade. 
Exact length of 10. 
TradeId Unformatted String No RTTM assigned match control number upon 
matching of trades. For post-match modifies, 
can be used to identify or target the trade. 
Exact length of 10. 
DKReasonCd Unformatted String No DK Reason code for DK action. Max length 
allowed is 4. 
RegMiscFee Decimal No Regulatory Miscellaneous Fee 

---

## Page 13

CMU CSV Trade Batch Upload Quick Reference Guide 
Appendix B: Reasons trade records are rejected 13 
APPENDIX B: REASONS TRADE RECORDS ARE 
REJECTED 
There are several reasons why your trades may be rejected. Let’s review one at a time:  
Bad Input File 
Any non-CSV file or CSV file containing illegal characters (even a single one) will be rejected. When this 
happens, the following error is displayed: 
 
At this point the file can only be rejected. The above example shows what would happen if the CSV File 
Template was uploaded in its original format and not exported to CSV. 
  


---

## Page 14

CMU CSV Trade Batch Upload Quick Reference Guide 
Appendix B: Reasons trade records are rejected 14 
Bad Input in Trade Record 
When a CSV record is parsed and any field isn’t supplied in the format, it will be marked as invalid, and it will 
be prevented from being submitted to the RTTM. Viewing the details of each invalid record will highlight the 
exact errors with the input. 
 
Trade Record Rejected by the CMU RTTM Web application 
CMU RTTM Web rejects trades for a variety of reasons. When this happens, the reason is displayed in a 
banner when viewing the details of the rejected trade. Here are some examples: 
• RTTM Trade Reject 
This reject has several reasons. For example, 
  
• Unexpected RTTM Error 
This is caused by an internal error. Contact [[DTCC]] Client Support at 1 888-382-2721, and then follow the 
prompt for product support. 
 


---

## Page 15

 
 
© 2021 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
Doc Date: August 5, 2021 
Publication Code: CMU109r 
Service: Corporate, Municipal,  and [[UIT]] (CMU) 
Title: CMU CSV Trade Batch Upload Quick Reference Guide 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 