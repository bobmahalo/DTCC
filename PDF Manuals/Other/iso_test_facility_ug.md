---
title: "ISO Test Facility - User's Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/iso_test_facility_ug.pdf"
pages: 32
size: "1677.5 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# ISO Test Facility - User's Guide

**Original File:** [iso_test_facility_ug.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/iso_test_facility_ug.pdf)  
**Category:** Other  
**Total Pages:** 32  
**File Size:** 1677.5 KB  

---

## Page 1

ISO TEST FACILITY
USER'S GUIDE
 
JULY 22, 2020


---

## Page 2

© 2020 [[DTCC]]. All rights reserved.   [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. 
TOGETHER, and the Interlocker graphic are registered and unregistered trademarks of The Depository 
Trust & Clearing Corporation.
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The 
Depository Trust & Clearing Corporation (“[[DTCC]]”).   [[DTCC]] itself does not provide such services.   Each of 
these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or 
countries in which such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its 
affiliates and the services they offer.
 
Publication Code: SET151
Service: ISO Test Facility
Title:   User's Guide   

---

## Page 3

TABLE OF CONTENTS
1. Introduction 5
Overview of the ISO Test Facility 5
Steps For Using the ISO Test Facility 5
Business Terms 6
2. Procedures 12
Entering Messages 12
Downloading Messages 13
Making Messages Printable Documents 13
Deleting Stored Content and Starting     a New File 13
3. Page Buttons and Field Definitions 15
Message Entry Page Buttons and Field     Definitions 15
File Content Review Page Buttons and     Field Definitions 16
4. [[DO]] Process Flow 17
[[DO]] Process Flow Illustrated 17
How to Set Up My System to Process Messages 19
How is a Deliver Order Processed? 20
Message Type 20
5. PO Process Flow 21
PO Process Flow Illustrated 21
When [[DO]] I Use a Payment Order? 23
How is a Payment Order Processed? 24
Message Type 24
6. [[collateral]] Pledge Process Flow 25

---

## Page 4

[[collateral]] Pledge Process Flow Illustrated 25
When to use a [[collateral]] Pledge 27
How to Set up My System to Process Messages 27
How is a [[collateral]] Pledge or Release Processed? 28
Message Type 28
7. Accounting Process Flow 30
Accounting Process Flow Illustrated 30
When to Use Accounting Segregation of [[securities]]? 31
How [[DO]] I Set up my System to Process Messages? 32
How is a Segregation of [[securities]] or Release Processed? 32
Message Type 32

---

## Page 5

OverviewoftheISOTestFacility 5
1. INTRODUCTION
Overview of the ISO Test Facility
The ISO Test Facility is a web-based tool that assists         you in the construction of [[DTC]] [[settlement]] related ISO 
input and output         messages. Use this tool as:     
 l An         online resource reference
 l An interactive guide for           creating and testing ISO messages       
You can perform the following tasks:     
 l Enter         messages in an easy-to-read web spreadsheet
 l Store         up to five messages in a file that can be downloaded to your computer
 l View           messages in a printer-friendly format with additional business definitions       
See process flows for       each of the transaction types in this document.
Steps For Using the ISO Test Facility
Below is a typical work flow for working in the Test Facility.
 1.  Select a message from the ISO Test Facility home page
 2.  Enter data in the fields of the header portion of the message.   Select Continue.
 3.  Enter data in the fields of the transaction portion of the     message. Select Store.
 4.  Add up to five messages in the file. Select Add More Messages.
 5.  Download the file to your computer. Select Download.
 6.  Clear the file in order to enter new messages in a new file.     Select New File .
 7.  To edit a file, from the home page you may select Review,   Edit, Discard, or Download.” This link is 
only visible on the     home page when messages are currently stored in a file.

---

## Page 6

OverviewoftheISOTestFacility 6
Business Terms
B
[[Broker]] Internal Account
Submitter’s or Recipient’s BIC Number/[[participant]] [[ID]].
Buy Sell indicator
Indicates that the Prime [[Broker]] is buying or selling.
C
Call
Indicates the [[Option]] is a call.
Certification Indicator
Indicator that is set to track if brokers warrant that they have the applicable certificate/papers.
Classification Type
Type   of [[DTCC]] defined [[Asset]] class.
CMO Factor
Factor to determine the face value of an amortizing security.   DOs only.
[[CNS]] Level Indiator
Indicates how [[CNS]] short (levels 1 and 2) and long (level 4) [[shares]] should be processed.     For 
example, Short [[shares]] can be exempted and long [[shares]] anticipated
Command Indicator
A [[settlement]] command that is applied to transations. For example, autorize, exempt, and 
pend are commands.
Command Scope Indicator
Defines     the parameters of the [[settlement]] command that is applied to transactions.  For 
example, scope     could apply to transactions globally, in a list, or by [[Asset]] class-transaction.   
type
Contract Date
The     contract date for an security payment order. The delivery date is the     contract date and is 
required for reason codes
Correspondent Account
Correspondent account number
Cross Reference Line Number
Relates     to the Depository Release Number or Receipt of Deposit on the OCC orm. This field 
is optional

---

## Page 7

OverviewoftheISOTestFacility 7
D
Deliverer
[[participant]]     that delivers the security; for a payment order the payee; for a [[collateral]]     pledge the 
pledgor
Deliverer Account Number
Deliverer,     payee, or pledgor account number.     Could be [[DTCC]] [[participant]] number or the 
deliverer’s internal account     number
Deliverer Contact Information
Contact     information for the deliverer
Deliverer Internal Account
The     deliverer’s internal account number
[[DTCC]] Function Type
[[DTCC]]     function transmission type ( e.g. for Deliver Orders: 
DOI1,DOI5,DOI6,DOI7,DOX1,DOX3,DOX5,DOX7     For Payment Orders: 
POL1,POL5,POL6,POL7 For Pledges: PLG1,PLG5,PLG7, For     MA/NA: MNA1,MNA5 and 
SEG-SEG1,SEG5,SEG7)
Due Bill Indicator
Indicates     whether a due bill is carried or not
E
Error Code
[[DTCC]]     field error code (a list of codes is available using [[PTS]] function ICMF     or through 
retrieval of a DTF file from [[DTCC]])
Exercise Price
[[Option]]     exercise price.     (New price)
Expiration Date
Date     that rights expire (become worthless)
F
Federal Reserve Purpose
Reason     for the free Fed pledge or release return
Field Code
Uniquely     identifies the field in error
Free Format text
Text     description. For example a description of an error field

---

## Page 8

OverviewoftheISOTestFacility 8
H
[[Hypothecation]] Code
Mandatory     code entered by the [[participant]] to effect deliveries for pledge activity
I
[[ID]] Control Number
Unique     reference used to identify Institutional Delivery ([[ID]]) transactions processed     by Omgeo
IMS TID
Inventory     Management System (IMS) transaction identifier
IMS TID Reclaim
Unique     transaction reference number assigned by the Inventory Management System     (IMS) 
and used to process a reclaim or DK (don’t know) request
Internal Source Code
Identifies     the input media for the transaction
[[IPO]] Indicator
Indicator     used for the [[IPO]] Tracking system
ISIN
Identification     of the financial Instrument (Country Code, [[CUSIP]] and Check Digit)
Issue Date
The     date when the security is released or sold, for [[Equity]] [[securities]]. For     MMI-eligible secur-
ities, the record date is equivalent to the issue date
L
Loan Date
Loan     date for a pledge or pledge release transaction
M
Market Price
The     market value (old price)
Message Function
Field     that identifies the function of the message
Message Status
Acknowledgement     message status tag

---

## Page 9

OverviewoftheISOTestFacility 9
N
Narrative & [[DTC]] Comments
Provides additional [[settlement]] processing information
Number Of Contracts
The     number of contracts in the transaction
O
OCC Name
Options     Clearing Corporation [[participant]] name or account number
Original Message Header
The     portion of a message that contains control information (for example, the     sender, the 
receiver, the message type and the priority information)
P
Payable Date
Pay     date for the [[securities]]
Payee Reference Number
Assigned     by payee (deliverer) for audit trail
Payment Indicator
Indicates     whether the underlying [[securities]] are free or valued
Place of [[settlement]]
[[DTCC]]     BIC Number
Pledge Purpose
Reason     for the pledge such as for a new loan, loan increase, [[collateral]] increase     or substitution
Pledgor’s Account Number
Pledgor     [[DTCC]] [[participant]] number
Prevent Pend Indicator
Indicates     if the transaction should be prevented from recycling
PTA Indicator
Indicates     if the transaction should affect the Protected Transaction Account
Put Indicator
Indicates     the [[Option]] is a put

---

## Page 10

OverviewoftheISOTestFacility 10
Q
Quantity
Quantity     of financial instrument to be settled expressed as units such as share     quantity
R
Reason
Provides     an explanation for the reject, pend, drop, or cancel
Reason Code
The     reason code for the transaction.     This required field must be filled with a 2-character 
alpha-numeric reason     code defined by [[DTC]]. The validity of a reason code is partly dependent     
upon the time of transmission
Reason Description
Reason     Code Description
Receipt Release Indicator
Indicates     receipt or release of the underlying [[securities]] for a [[Premium]] payment     order
Receiver
[[participant]]     that receives the security; for a payment order, the payor; for a [[collateral]]     pledge 
the pledgee
Receiver Account Number
Receiver,     payor, or ledge account number.     Could be [[DTCC]] [[participant]] number or the 
receiver’s internal account     number
Receiver Contact Information
Contact     information for the receiver
Receiver Deliverer Indicator
Contact     information for the deliverer
Receiver Internal Account
The     receiver’s internal account number
Recipient Of Message
The     receiver’s BIC
Record Date
Date on which a security holder must be registered on the books of the [[issuer]] to receive the 
income distribution on the payable date
Reject Code Error
Reason     for the reject
Reject Code Field
Reject     code

---

## Page 11

OverviewoftheISOTestFacility 11
Release Type
The     reason for the release request
S
Safekeeper
Identifies     account where financial instruments are maintained
Senders Ref
Sender's     reference number
Serial Number
Serial     number supplied by the [[participant]]
Settle Today Only Indicator
Indicates     if the transaction can only settle on [[settlement]] date or can attempt the     next set-
tlement date if past cutoff
[[settlement]] Amount
Dollar     Amount that was settled with regards to this transaction
[[settlement]] Date
Date     on which the transaction should be settled
Status
The     IMS or ATP states assigned as the transaction is processed through IMS     and ATP
Status Code
The     IMS or ATP states assigned as the transaction is processed through IMS     and ATP
Submitter Of Message
The     BIC of the message submitter
T
Trading Symbol
Ticker     symbol of the security
Tran Update Date
Date     the transmission was updated
Transaction Type
IMS     transaction type
Transmission Processed Date
Date     the transmission was processed
Transmission Received Date
Date     the transmission was received

---

## Page 12

Procedure 12
2. PROCEDURES
Entering Messages
 1.  From the ISO Message Test Facility home     page, select an input or output message.
The header portion of the message is displayed containing     general information identifying the 
message.
 2.  Type     data in the required fields in UPPERCASE.
 l To automatically populate all fields with filler values     that demonstrate the length and format of the 
field, click Autofill. 
 l To set all fields to their [[default]] values, select     Start New. 
 l To set all fields to the values they contained when     the page was first entered, select Reset. 
 3.  Select Continue at the bottom     of the page.
The transaction portion of the message is displayed.     
 4.  Type data in the required fields for     the transaction portion of the message.
 5.  When you have finished entering the     data in the message, select Store.
The File Content Review page appears with the messages     you entered so far displayed in the format 
in which they will be downloaded     or sent as a file. 
 6.  To continue entering messages, select     Add More Messages. You can add up to five messages.
Note: You     can modify the file content on this page, and if you [[DO]], you must select     Apply to save the 
changes before     clicking Add More Messages.
The ISO Test Facility home page appears allowing you     to choose another input or output message.
Tip: You can access     messages currently stored on the File Content Review page from the Test     
Facility home page. Under the ISO Test File Contents heading on the home     page, you may select 
"Review, Edit, Discard or Download."     This link is only visible on the home page when messages 
are currently     stored. 
Note:     If after entering and storing messages in a file, you wish to delete     all the messages and start 
over, you can [[DO]] this by selecting New File.   Caution:   Selecting New File deletes all messages stored 
or previously saved in   the file contents panel. For more information, see  Deleting Stored Content and 
Starting     a New File on the next page. 
 7.  To download the messages in the file     contents to your computer, select Download     and follow the 
prompts. For more information, see Downloading Messages on the next page.

---

## Page 13

Procedure 13
Downloading Messages
After entering and saving messages, you can download the file contents     to your computer. 
 1.  From the File Content Review page, ensure     that messages you entered are correct. See Entering 
Messages on the previous page. 
Note
You can access     messages currently stored on the File Content Review page from the home     
page. Under the ISO Test File Contents section, you may select Review,   Edit, Discard or 
Download. This link is only visible on the home page     when messages are currently stored. 
 2.  Select Download.
 3.  To save the files to a location on your computer,     when prompted, choose Save
Making Messages Printable Documents
The View As Document function allows you to see and print any ISO message     spreadsheet as a printer-
friendly document. In this view, you can also     see business definitions for fields and expanded content rules 
for the     fields as well.
 1.  From any message entry page, you may     select View as Document.
A window appears containing your entry.
 2.  To print this version, select Print   in the upper right corner of the window.
Deleting Stored Content and Starting   a New File
If after entering and storing messages in a file, you wish to delete     all the messages and start a new file, use 
the New File function     to [[DO]] this. 
 1.  Display the File Content Review page.     
From the ISO Message Test Facility home page, under the ISO Test File     Contents section, you may 
select Review,   Edit, Discard or Download.
This link is only visible on the home page when messages     are currently stored.
 2.  Select New File.
Caution
Selecting New File deletes     all messages stored or previously saved in the file contents 
pane.

---

## Page 14

Procedure 14
When you select New File, a message is displayed:     "Are you sure you want to discard   the 
current file and start a new one?" To delete the current     file, click OK. The messages are     cleared 
and you are returned to the ISO Test Facility home page.

---

## Page 15

PageButtonsandFieldDefinitions 15
3. PAGE BUTTONS AND FIELD DEFINITIONS
Message Entry Page Buttons and Field   Definitions
Term Definition
Auto-fill Automatically populates all fields with filler values that     demonstrate the 
length and format of the field. When Autofill     is used, you can see the 
format of a message with all the fields populated.
Back/Continue Back returns you to the     previous page. Continue pages you forward to the 
transaction portion     of the message.
Content Rule Rule stating the conditions to be met by a field for validity.
Field Description Describes the field on a message row.
Input Value Field in which to enter message data.
Length Total allowed length of the field in the header block.
Position The starting position index of the field inside the message     Header block.
Print (access from header 
block or transaction): 
Prints the header block or transaction you are working     in. Choose 
landscape orientation for best results.
Print (access from View as 
Document): 
Prints the ISO message spreadsheet as a printer-friendly     document. Select 
View as Document,     then select Print. Choose landscape     orientation for 
best results.
Question Mark Icon:  Displays expanded content rules for a given field. From any header 
block     or spreadsheet, click the question mark icon next to a field. Tip: To 
see or print expanded     content rules for an entire spreadsheet, select 
View   as Document.
Reset Sets all fields to the values they contained when the page     was first 
entered.
Start New Sets all fields to their [[default]] values. 
Store Displays entered content in the File Content Review page.     After entering 
content, select Store at the bottom of the message     entry page. 
View as Document See or print an entire spreadsheet as a printer-friendly     document. In this 
view, you can also see business definitions for fields     and expanded 
content rules for fields as well.
Message Entry Page Buttons and Field   Definitions

---

## Page 16

PageButtonsandFieldDefinitions 16
File Content Review Page Buttons and   Field Definitions
Term Definition
Add More Messages Returns you to the ISO Test Facility home page where you     can choose 
another message to enter.
Apply Saves any modifications you make to the file content on     this page. Note: 
You can modify     the file content, and if you [[DO]], you must select Apply     to 
save the changes before clicking Add More Messages.
Download Saves up to five messages in a file to your computer.
New File Deletes all messages stored or previously saved in the     file contents panel.
Reset Undoes unsaved changes. 
Message Entry Page Buttons and Field   Definitions

---

## Page 17

DOProcessFlow 17
4. [[DO]] PROCESS FLOW
[[DO]] Process Flow Illustrated
Overall Process Flow Chart
The overall process flow of a deliver order transaction between [[DTC]]     and parties to the deliver order are as 
follows


---

## Page 18

DOProcessFlow 18
The following diagrams show the process flow for each party to a payment     order or deliver order .
Deliverer Diagram


---

## Page 19

DOProcessFlow 19
Receiver Diagram
How to Set Up My System to Process Messages
See the ISO 15022   [[settlement]] Messaging Getting Started Information Request Form on the [[DTCC]] Learning 
Center (login required) for instructions on how to set up your     systems for processing SWIFT input 
messages.
Setting up a transaction flow for deliver orders involves the following     steps:
 1.  In the deliverer’s Inventory Management     System (IMS) notification profile 
 l Choose whether you want     to receive full or short messages (applies to MT548 and MT578) 
 l Choose which [[settlement]]     status you want to receive (applies to MT548) 
 2.  The deliverer submits either a free     deliver order ( [[DO]] MT542) or a for value deliver order ([[DO]], MT543) 
 l Submit the deliver order      
 l Receive an acknowledgment     (ACK, MT548) if successful or a non-acknowledgement (NAK, 
MT548) if rejected     

---

## Page 20

DOProcessFlow 20
 3.  The deliverer validates or edits the     message.
 l If validated, submit the     message to IMS for processing.
 l If edited, resubmit the     message to IMS for processing.
 4.  Both the deliverer and the receiver     receive a [[settlement]] confirmation message 
 l The deliverer receives     a deliver free (MT546) or deliver versus payment (MT547) confirmation     mes-
sage 
 l The receiver receives     a receive free (MT544) or receive versus payment (MT545) confirmation     mes-
sage
 5.  Use the MT530 (transaction command)     message layout to take action upon a transaction.
How is a Deliver Order Processed?
A deliver order between a deliverer and a receiver consists of the following     message layouts.
Message Type 
 l MT542 - Free Deliver Order 
 l MT543 -  Value Deliver Order 
 l MT598 - Acknowledged/Not     Acknowledged 
 l MT544 - Receive     Free Confirmation 
 l MT545 - Receive     Against Payment Confirmation 
 l MT546 - Deliver     Free Confirmation 
 l MT547 - Deliver     Against Payment Confirmation 
 l MT548 - [[settlement]]     Status and Advice Message 

---

## Page 21

POProcessFlow 21
5. PO PROCESS FLOW
PO Process Flow Illustrated
Overall Process Flow Chart
The overall process flow of a payment order transaction between [[DTC]]     and parties to the payment order are 
as follows:


---

## Page 22

POProcessFlow 22
The following diagrams show the process flow for each party to a payment     order or deliver order.
Payee Diagram


---

## Page 23

POProcessFlow 23
Payor Diagram
When [[DO]] I Use a Payment Order?
A [[participant]] wanting to collect money (the payee [[participant]]) from     another [[participant]] (the payor [[participant]]) 
first contacts the payor [[participant]]     to reach agreement on the amount payable. The payee [[participant]] then 
submits     to [[DTC]] a [[Premium]] payment order (PPO) or a [[securities]]     payment order (SPO). The PPO is     used to 
collect a net [[Option]] contract [[Premium]] for an opening writing or     closing purchase transaction. The SPO is 
used to collect     a [[mark-to-market]] payment based on the difference between the current and     previous market 
value of an open [[securities]] contract. Either type of payment     order authorizes [[DTC]] to credit the payee 
[[participant]]'s [[settlement]] account     with the specified amount and to debit the payor [[participant]]'s [[settlement]]     
account for the same amount.  
The following are typical situations in which     you might use the Payment Order service.
 l A   bank's customer writes an opening [[Call option]]. Through [[DTC]] the     bank deposits underlying secur-
ities with the Options Clearing Corporation     (OCC). The bank (the payee [[participant]]) submits to     [[DTC]] a 
PPO crediting its [[settlement]] account for the     amount of the net [[Option]] contract [[Premium]] and debiting the 
account of     the [[Broker]] (the payor [[participant]]) for the same amount.  

---

## Page 24

POProcessFlow 24
 l A   bank's customer purchases a closing [[Call option]]. OCC     releases underlying [[securities]] previously 
deposited with it through [[DTC]].     The [[Broker]] (the payee [[participant]]) submits to [[DTC]] a PPO     crediting its set-
tlement account for the amount of the net [[Option]] [[Premium]]     and debiting the account of the bank (the payor 
[[participant]]) for the same     amount.  
 l A   [[participant]] delivers [[securities]] to another [[participant]] through [[DTC]] in   a [[Stock]] loan transaction. 
Thereafter, the market value of the [[securities]]     increases significantly. The lender (the payee [[participant]]) 
submits an     SPO to [[DTC]] crediting its [[settlement]] account for the amount of the difference     between the ori-
ginal and new market values and debiting the account of     the [[Borrower]] (the payor [[participant]]) for the same 
amount.
How is a Payment Order Processed?
A payment order between a payor and a payee consists of the following     message layouts.
Message Type 
 l MT543 - Security Payment Order 
 l MT543 - [[Premium]] Payment Order
 l MT598 - Acknowledged/Not     Acknowledged 
 l MT544 - Receive     Free Confirmation 
 l MT545 - Receive     Against Payment Confirmation 
 l MT546 - Deliver     Free Confirmation 
 l MT547 - Deliver     Against Payment Confirmation 
 l MT548 - [[settlement]]     Status and Advice Message 
 l MT530 - Transaction     Command

---

## Page 25

CollateralPledgeProcessFlow 25
6. [[collateral]] PLEDGE PROCESS FLOW
 
[[collateral]] Pledge Process Flow Illustrated
Overall Process Flow Chart
The overall process flow of a [[collateral]] pledge between [[DTC]]     and parties to the pledge are as follows: 


---

## Page 26

CollateralPledgeProcessFlow 26
The following diagrams show the process flow for each party to a [[collateral]]     pledge: 
Pledgor Diagram


---

## Page 27

CollateralPledgeProcessFlow 27
Pledgee Diagram
When to use a [[collateral]] Pledge
The [[collateral]] Loan Program allows you to pledge [[securities]] from your     general free account as [[collateral]] for 
a loan or for other purposes (such     as Letters of Credit) to a pledgee participating in the program. You can     also 
request that the pledgee releases pledge [[securities]] back to your     general free account. These pledges and 
releases can be free (when money     proceeds are handled outside [[DTC]]) or valued (when money     proceeds are 
applied as debits and credits to the pledgee's and pledgor's     money [[settlement]] accounts).
The following are typical situations in which you might use the [[collateral]]     Loan Program:
 l To pledge U. S. government     [[securities]] to satisfy OCC put and call [[Margin]] requirements     
 l To pledge [[securities]] to     the FRB where the [[collateral]] is used for discount,     [[book-entry]] daylight overdrafts 
or daylight (funds) overdrafts
 l To pledge U. S. government     [[securities]] of sufficient value to cover the exercise price of put and     call [[Option]] 
contracts.
How to Set up My System to Process Messages
See the Getting Stared with ISO 15022   [[settlement]] Messaging Getting Started Information Request Form on 
the [[DTCC]] Learning Center (login required)for instructions on how to set up your     systems for processing 

---

## Page 28

CollateralPledgeProcessFlow 28
SWIFT input messages.
Setting up a transaction flow for [[collateral]] pledges and releases involves     the following steps:
 1.  In the deliverer’s Inventory Management     System (IMS) notification profile 
 l Choose whether you want     to receive full or short messages (applies to MT548 and MT578) 
 l Choose which [[settlement]]     status you want to receive (applies to MT548) 
 2.  The pledgor submits either a free pledge     ( COL MT542) or a for value pledge (COL, MT543) 
 l Submit the pledge  
 l Receive an acknowledgment     (ACK, MT548) if successful or a non-acknowledgement     (NAK, 
MT548) if rejected 
 3.  The COL application validates or edits     the message 
 l If validated, submit the     message to IMS for processing 
 l If edited, reject back     to pledgor (for re-submission) 
 4.  Both the pledgor and the pledgee receive     a [[settlement]] confirmation message 
 l The pledgor receives a     free pledge (MT546) or valued pledge (MT547) confirmation message 
 l The pledgee receives a     free pledge (MT544) or valued pledge (MT545) confirmation message
 5.  Use the MT530 (transaction command)     message layout to take action upon a transaction.
How is a [[collateral]] Pledge or Release Processed?
A [[collateral]] pledge between a pledgor and pledgee consists of the following     message layouts.
Message Type 
 l MT542 - Free Pledge
 l MT543 - Value Pledge
 l MT540 - Free Release Return
 l MT541  - Valued Release Return
 l MT542   &endash; Free Fed Pledge
 l MT540 - Free Fed Release Return
 l MT598 - Acknowledged/Not     Acknowledged 

---

## Page 29

CollateralPledgeProcessFlow 29
 l MT544 - Receive     Free Confirmation 
 l MT545 - Receive     Against Payment Confirmation 
 l MT546 - Deliver     Free Confirmation 
 l MT547 - Deliver     Against Payment Confirmation 
 l MT548 - [[settlement]]     Status and Advice Message
 l MT530 - Transaction     Command

---

## Page 30

AccountingProcessFlow 30
7. ACCOUNTING PROCESS FLOW
Accounting Process Flow Illustrated
Overall Process Flow Chart
The overall process flow of a sub-accounting segregation of [[securities]]     is as follows:


---

## Page 31

AccountingProcessFlow 31
The following diagram shows the process flow for a [[participant]] performing     an account movement:
Deliverer Diagram
 
When to Use Accounting Segregation of [[securities]]?
The Sub-Accounting Service allows you to protect [[securities]] on deposit     at [[DTC]] by moving them from your 
general free account to your segregated     account. The [[securities]] remain segregated and unavailable for any 
transactions     until you authorize [[DTC]] to release them and return them to your general     free account. 
On payment day, [[DTC]] will automatically allocate cash merger and mandatory     put payments as well as 
municipal and corporate redemption payments for     [[securities]] segregated on [[DTC]]'s books.
You should release on or before the payment date certain segregated     positions for [[securities]] being 
reorganized. Failure to release these positions     may delay payment and drive your general free accounts into 
short (negative)     positions when proceeds are allocated. 
The following are typical situations in which you might use the Sub-Accounting     Service:
 l To protect fully-paid-for     [[securities]] in your general free or [[IPO]] control account
 l To release segregated     [[securities]] back to your general free account
 l To segregate [[securities]]     for Internal Revenue Service purposes.

---

## Page 32

AccountingProcessFlow 32
How [[DO]] I Set up my System to Process Messages?
See the Getting Stared with ISO 15022   [[settlement]] Messaging guide for instructions on how to set up your     
systems for processing SWIFT input messages.
Setting up a transaction flow for sub-accounting involves the following     steps:
 1.  In the [[participant]]'s Inventory Management     System (IMS) notification profile.
 l Choose whether you want     to receive full or short messages (applies to MT548 and MT578).
 l Choose which [[settlement]]     status you want to receive (applies to MT548).
 2.  The [[participant]] submits a ( MT524) for     SEG, SEG Release, Memo Seg, Investment [[ID]], Investment [[ID]] 
Release, or an     MA/NA Transfer.
 l Submit the account movement.
 l Receive an acknowledgment     (ACK, MT548) if successful or a non-acknowledgement     (NAK, 
MT548) if rejected.
 3.  The segregation application validates     or edits the message.
 l If validated, submit the     message to IMS for processing. 
 l If edited, reject back     to the [[participant]] (for re-submission) s
 4.  The [[participant]] receives a [[settlement]]     confirmation message.
 l The [[participant]] receives     an account movement (MT546) confirmation message.
How is a Segregation of [[securities]] or Release Processed?
A sub-accounting segregation of [[securities]] consists of the following     message layouts. 
Message Type 
 l MT524 - SEG
 l MT524 - SEG Release
 l MT524 - Memo Seg 
 l MT524 - Investment [[ID]] 
 l MT524 - Investment [[ID]] Release
 l MT524 - MA/NA Transfer
 l MT598 - Acknowledged/Not     Acknowledged
 l MT548 - [[settlement]]     Status and Advice Message 