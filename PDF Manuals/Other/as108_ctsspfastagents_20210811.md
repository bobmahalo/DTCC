---
title: "CTS - Securities Processing for FAST Agents"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/as108_ctsspfastagents_20210811.pdf"
pages: 45
size: "1739.4 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# CTS - Securities Processing for FAST Agents

**Original File:** [as108_ctsspfastagents_20210811.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/as108_ctsspfastagents_20210811.pdf)  
**Category:** Other  
**Total Pages:** 45  
**File Size:** 1739.4 KB  

---

## Page 1

 
[[Asset]] SERVICES 
CORPORATE TRUST SERVICES – [[securities]] PROCESSING FOR [[FAST]] AGENTS 
VERSION 1.0 
AUGUST 11, 2021 
 


---

## Page 2

 
 
© 2021 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself 
does not provide such services.  Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in which 
such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
 
Doc Date: August 11, 2021 
Publication Code: AS108 
Service: [[Asset]] Services 
Title: Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Overview ........................................................................................................................................................................................................................ 5 
Corporate Trust Services – Accessing [[securities]] Processing ................................................................................................................................ 6 
Accessing Corporate Trust Services [[securities]] Processing Functions ...................................................................................................................... 6 
TA Direct Deposit/Withdrawal ................................................................................................................................................................................... 10 
Legal Considerations ................................................................................................................................................................................................. 10 
When to Use .............................................................................................................................................................................................................. 11 
View Deposit and Withdrawal Transactions .............................................................................................................................................................. 11 
Approve or Cancel Deposits or Withdrawals ............................................................................................................................................................. 12 
[[Direct Registration]] System ([[DRS]]) ............................................................................................................................................................................. 14 
About the [[Direct Registration]] System ([[DRS]]) ............................................................................................................................................................ 14 
Processing [[Direct Registration]] System ([[DRS]]) Transfer Requests ........................................................................................................................... 15 
Background .............................................................................................................................................................................................................. 15 
View an Open [[DRS]] Transfer Request ...................................................................................................................................................................... 16 
Approve (Update) a [[DRS]] Transfer Request .............................................................................................................................................................. 19 
Results of an Update in the [[DRS]] Function .............................................................................................................................................................. 22 
Rejecting a Transaction ............................................................................................................................................................................................. 23 
View a [[DRS]] Transaction ........................................................................................................................................................................................... 25 
Verify a [[DRS]] Transfer Request ................................................................................................................................................................................. 26 
[[FAST]] Balance Confirmations .................................................................................................................................................................................... 32 
Confirm a [[FAST]] Balance ........................................................................................................................................................................................... 32 
[[FAST]] SCL (Shipment Control List) Confirmation .................................................................................................................................................... 34 

---

## Page 4

 
 
Overview .................................................................................................................................................................................................................... 34 
When to Use .............................................................................................................................................................................................................. 34 
Confirm or Reject an SCL .......................................................................................................................................................................................... 34 
Reject or Partially Confirm SCL Line Items ............................................................................................................................................................... 36 
View the Status of an SCL......................................................................................................................................................................................... 38 
Confirm Full SCLs (Wanding) .................................................................................................................................................................................... 40 
Reject Full SCLs (Wanding) ...................................................................................................................................................................................... 41 
Confirm or Reject [[FAST]] [[Underwriting]] SCLs ............................................................................................................................................................. 42 
Unconfirm Deposit SCLs ........................................................................................................................................................................................... 43 
Confirm a Partially Confirmed or Rejected SCL ........................................................................................................................................................ 44 
 

---

## Page 5

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
Overview 5 
OVERVIEW 
This guide explains a variety of [[securities]] processing functions used by [[FAST]] Agents within the [[PBS]] – Corporate Trust Services application. It is 
intended for ([[DTC]]-eligible) [[FAST]] agents eligible for [[DTC]]'s [[Direct Registration]] System ([[DRS]]). This guide explains concepts and terms relevant to 
[[DRS]] transfers but is not intended as the be-all / end-all reference for Agent Services. For information about becoming a [[DTC]]-eligible [[FAST]] Agent, 
please visit the Agent Services page of the [[DTCC]] Corporate website. 
  

---

## Page 6

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
Corporate Trust Services – Accessing [[securities]] Processing 6 
CORPORATE TRUST SERVICES – ACCESSING [[securities]] PROCESSING 
The functions explained in this guide can all be accessed via links which appear in the [[DTC]] [[participant]] Browser Services ([[PBS]]) application (via 
Corporate Trust Services) under the [[securities]] Processing heading. Access to and some familiarity with the [[PBS]] application is assumed. This 
section demonstrates the navigation required to access the Corporate Trust Services - [[securities]] Processing functions in [[PBS]]. The screen captures 
in this guide are included for reference only and may include information not specific to the steps being explained (which you may safely ignore). 
Accessing Corporate Trust Services [[securities]] Processing Functions 
1. Login to the [[DTCC]] Portal (https://portal.[[DTCC]].org/) 
Figure 1: [[DTCC]] Portal Login 
  


---

## Page 7

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
Corporate Trust Services – Accessing [[securities]] Processing 7 
2. Under “My Products” select the [[PBS]] – [[participant]] Browser Services tile. 
Figure 2: [[PBS]] - [[participant]] Browser Services Tile 
  


---

## Page 8

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
Corporate Trust Services – Accessing [[securities]] Processing 8 
3. The [[participant]] Browser Services ([[PBS]]) application opens. Click Corporate Trust Services. 
Figure 3: Corporate Trust Services Link 


---

## Page 9

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
Corporate Trust Services – Accessing [[securities]] Processing 9 
4. The [[PBS]] – Corporate Trust Services application opens. Take note of where the “[[securities]] Processing” heading is located. The activities 
described in this guide use [[securities]] Processing functions which are accessed using the links appearing under this heading. 
Figure 4: Corporate Trust Services [[securities]] Processing 
Figure 5: [[securities]] Processing Functions (enlarged) 


---

## Page 10

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
TA Direct Deposit/Withdrawal 10 
TA DIRECT DEPOSIT/WITHDRAWAL 
The TA Direct Deposit/Withdrawal application is an on-line facility allowing [[DTC]] [[Custodians]] to approve or cancel deposit and withdrawal instructions 
that were submitted by participants with respect to [[securities]] (e.g., unit investment trusts) evidenced by a balance certificate registered in the name 
of [[DTC]]'s [[nominee]], Cede &Co. , and held for [[DTC]] by a [[DTC]] custodian. The custodian can also inquire about instructions that were previously 
entered. Upon approval of a transaction, the custodian will update [[DTC]]'s balance on the custodian's books accordingly. 
In approving a [[participant]]'s deposit instruction, the custodian attests to the existence of the [[securities]] that are the subject of the [[participant]]'s 
instruction and certifies that it or (if the custodian is not the [[transfer agent]] or registrar for the issue) the [[transfer agent]] or registrar, has registered the 
transfer of those [[securities]] in the name of Cede &Co. in accordance with the (Balance) Certificate Agreement between itself, the [[transfer agent]] or 
registrar (where applicable), and [[DTC]]. 
The custodian will use TA Direct Deposit/Withdrawal to either approve or cancel each deposit or withdrawal instruction submitted by a [[participant]] on 
the day such instruction is submitted, or, if the [[participant]] has opted for the 72-hour deposit pend [[Option]] now offered by [[DTC]], three business days 
(including the deposit date). If the custodian uses TA Direct Deposit/Withdrawal on that day to approve such instruction, the custodian will on that 
day increase or decrease [[DTC]]'s balance on the custodian's books accordingly. If the custodian uses TA Direct Deposit/Withdrawal to cancel such 
instruction or fails to use TA Direct Deposit/Withdrawal to either approve or cancel such instruction, the custodian will not increase or decrease 
[[DTC]]'s balance on the custodian's books with respect to such instruction. 
Participants have the [[Option]] of selecting a 72-hour pend period for all deposits, which gives [[Custodians]] up to three business days (including the 
deposit date) to either approve or cancel the transaction before it drops off the system. This [[Option]] saves participants the trouble of having to 
resubmit a deposit if a custodian takes no action within three days and reduces the number of deposit instructions received by the custodian. 
Note 
The 72-hour pend [[Option]] cannot be used selectively on a deposit-by-deposit or on a [[CUSIP]]-by-[[CUSIP]] basis. The [[participant]] must activate the 72-hour pend feature 
either for all or none of its transactions. 
Legal Considerations 
The [[DTC]] custodian's approval via TA Direct Deposit/Withdrawal of a [[participant]]'s deposit or withdrawal instruction shall constitute the custodian's 
statement that it has increased or decreased on its books the quantity of [[securities]] evidenced by the balance certificate in the custodian's [[custody]] on 
that day. 

---

## Page 11

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
TA Direct Deposit/Withdrawal 11 
Therefore, the custodian's approval of the [[participant]]'s deposit or withdrawal instruction shall be deemed to be the receipt by [[DTC]] of a new, reissued 
or registered certificated security on registration of transfer to the name of Cede &Co. for the quantity of [[securities]] evidenced by the balance 
certificate after the [[participant]]'s deposit or withdrawal instruction is affected. [[Custodians]] should bear in mind the finality of the TA Direct 
Deposit/Withdrawal approval when designing their TA Direct Deposit/Withdrawal procedures and completing any [[PTS]] Update Request form. 
When to Use 
If you are a custodian, use TA Direct Deposit/Withdrawal to approve or cancel any deposit or withdrawal transactions entered by participants on 
either the current business day or within three days (including the deposit date at [[DTC]]) if the 72-hour pend [[Option]] is used by the [[participant]]. 
TA Direct Deposit/Withdrawal is available on business days from 12:00 a.m. (midnight) to 5:30 p.m. 
View Deposit and Withdrawal Transactions 
Use the following procedure to view past or current deposit and withdrawal transactions. The procedure assumes you can access the [[securities]] 
Processing functions in the [[PBS]] – Corporate Trust Services application. (See the Accessing Corporate Trust Services [[securities]] Functions topic.) 
1. From the list of [[securities]] Processing functions in the [[PBS]] – Corporate Trust Services application, select TA Direct Deposit/Withdrawal. 
2. If prompted, type your User [[ID]] and password, and click Submit.  
3. The Main Menu appears. Type your custodian number in the Cust Num field. 
Figure 6: [[securities]] Processing - TA Direct Deposit/Withdrawal function / link 

---

## Page 12

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
TA Direct Deposit/Withdrawal 12 
4. Type 2 in the [[Option]] field. 
Optional: To limit the resulting display, enter values in the following fields: 
• Type: Type D or W to list deposits or withdrawals only 
• [[CUSIP]]: Type a valid nine-digit [[CUSIP]] number to list transactions for a specific security 
• Date: Type the date in mmddccyy format to list transactions that were entered on the previous business day 
• Day/Night: Type one of the following: 
o D: To list transactions entered via the NDWP function (current day transactions) 
o N: To list transactions entered via the NDWP function (current day transactions) 
o C: To list transactions entered via [[CCF]] 
5. Click Submit. 
Optional: To view the last pend date at [[DTC]], the [[participant]]’s contact name and phone number, the custodian’s contact name and phone 
number, reference [[ID]], and any comments entered for a transaction, place the cursor on the desired line and click Comment. 
 
Approve or Cancel Deposits or Withdrawals 
Use the following procedure to approve or cancel deposit or withdrawal transactions entered by a specific [[participant]]. 
1. From the list of [[securities]] Processing functions in the [[PBS]] – Corporate Trust Services application, select TA Direct Deposit/Withdrawal. 
2. If prompted, type your user [[ID]] and password, and click Submit. 
3. The Main Menu appears. Type your custodian number in the Cust Num field. 
Figure 7: [[securities]] Processing - TA Direct Deposit/Withdrawal function / link 

---

## Page 13

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
TA Direct Deposit/Withdrawal 13 
4. Type 1 in the [[Option]] field. 
Optional: To list deposits or withdrawals only, type D or W in the Type field. 
Optional: To list transactions for a specific security, type the [[CUSIP]] number in the [[CUSIP]] field. 
5. Click Submit. 
6. Type one of the following in the A/C field to the left of the desired transaction: 
• “A” (to approve the transaction) 
• “C” (to cancel the transaction) 
Note 
If you cancel a transaction, you must enter a reason in the Comment field and type identifying information in the Cust Contact Name and Phone fields. 
7. Click Update to confirm the entry. 
8. Click Update again to transmit. 
 
  

---

## Page 14

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[Direct Registration]] System ([[DRS]]) 14 
[[Direct Registration]] SYSTEM ([[DRS]]) 
About the [[Direct Registration]] System ([[DRS]]) 
Transfer Agents use the [[Direct Registration]] System function (see Fig. 8) to transfer [[DRS]] [[shares]] from the [[transfer agent]]'s account to a [[Broker]]'s 
account at [[DTCC]]. Transfer Agents can also view [[DRS]] transactions for a specific [[CUSIP]] and date range. 
  
Figure 8: [[Direct Registration]] System function / link 


---

## Page 15

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[Direct Registration]] System ([[DRS]]) 15 
Processing [[Direct Registration]] System ([[DRS]]) Transfer Requests 
Transfer Agents use the Approve (Update) function to transfer [[DRS]] [[shares]] from a [[transfer agent]]'s account to a [[Broker]]'s account at [[DTCC]]. 
Background 
Before such a transfer takes place: 
• An [[investor]] will have asked their [[Broker]] to move [[shares]] from a [[DRS]] account at a [[transfer agent]] to the [[Broker]]'s account. 
One of the following events then takes place:  
• The [[investor]] informs the [[transfer agent]] directly, OR 
• The [[investor]] informs the [[Broker]], who then informs the [[transfer agent]] (via [[Direct Registration]] System Profile Modification function (DRSP) in 
[[PTS]]/[[PBS]], or by other means). 
Note 
Only brokers who participate in the PSP Surety program can use DRSP.  
Lastly, before the [[transfer agent]] transfers the [[shares]] they must agree to the transfer, also via DRSP (or by letter or fax). 
  

---

## Page 16

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[Direct Registration]] System ([[DRS]]) 16 
View an Open [[DRS]] Transfer Request 
Use the following procedure to view an open [[DRS]] Transfer Request. The procedure assumes you can access the [[securities]] Processing functions in 
the [[PBS]] – Corporate Trust Services application. (See the Accessing Corporate Trust Services [[securities]] Functions topic.) 
1. From the list of [[securities]] Processing functions in the [[PBS]] – Corporate Trust Services application, click the [[Direct Registration]] System Profile 
Modification ([[participant]]) link. 
  
Figure 9: [[DRS]] Profile Modification ([[participant]]) function / link 

---

## Page 17

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[Direct Registration]] System ([[DRS]]) 17 
2. The [[Direct Registration]] System – Profile Modification by [[participant]] – Agent Menu page appears. The Main Menu section lists three options. 
Since we are looking to see if there are any open [[DRS]] transfer requests, in the Selection Criteria section enter “2” (Inquiry) in the [[Option]] field. 
3. The Status (O/A/R) field also accepts three options: O = Open Requests, A = Approve, and R = Rejected. We are looking for open items so 
enter “O” in the Status (O/A/R) field.  
Figure 10: Selection Criteria [[Option]] 
Figure 11: Selection Criteria Status (O/A/R) 

---

## Page 18

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[Direct Registration]] System ([[DRS]]) 18 
4. Leave all other fields blank and click Submit. 
5. If there are any open items they will be listed in the Transaction Summary List. In this example there is one open item. To view the details of the 
[[DRS]] transfer request, enter “S” in the Select field, then click Submit. 
 
Figure 12: Transaction Summary List 
6. In the Status Inquiry Detail section, match the [[CUSIP]], Tax [[ID]], and [[investor]]/[[DRS]] A/C at TA to the shareholder. 
 
 
  
Figure 13: Status Inquiry Detail 
Client identifiable information 
on screen captures in this 
example have been hidden. 
 

---

## Page 19

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[Direct Registration]] System ([[DRS]]) 19 
Approve (Update) a [[DRS]] Transfer Request 
Use the following procedure to approve a [[DRS]] Transfer Request. The procedure assumes you can access the [[securities]] Processing functions in the 
[[PBS]] – Corporate Trust Services application. (See the Accessing Corporate Trust Services [[securities]] Functions topic.) This procedure resumes 
where “View an Open Transfer Request” leaves off. 
1. After the [[DRS]] transfer has been approved, we need to go back into the [[DRS]] system to deliver the [[shares]] to the [[Broker]]. Once in the [[PBS]] – 
Corporate Trust Services application, click [[Direct Registration]] System Profile Modification ([[participant]]). 
  
Figure 14: [[DRS]] Profile Modification ([[participant]]) function / link 

---

## Page 20

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[Direct Registration]] System ([[DRS]]) 20 
2. In the Selection Criteria section of the Agent Menu, enter “1” (Approve/Reject Request) in the [[Option]] field to approve the [[DRS]] transfer request. 
3. Enter “O” in the Status field, leave all other fields blank and click Submit. 
 
Figure 15: Selection Criteria [[Option]] 
Figure 16: Selection Criteria Status (O/A/R) 

---

## Page 21

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[Direct Registration]] System ([[DRS]]) 21 
4. The Transaction Summary List appears. Verify the Transaction [[ID]] matches the printed [[DRS]] request to ensure you are not approving the wrong 
transaction request. Enter “S” in the Select field and click Submit.  
5. The Status Update Detail page opens, but this time with editable fields. To approve a [[DRS]], change the status to “A” (Approved). Then enter 
your name and your phone number in the Agent Contact field(s) and click Update. 
 
Figure 17: Transaction Summary List 
Figure 18: Status Update Detail 
Client identifiable information 
on screen captures in this 
example have been hidden. 
 

---

## Page 22

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[Direct Registration]] System ([[DRS]]) 22 
6. This brings up the Agent Menu showing a confirmation message in yellow at the top that reads “Update Successful For Transaction 
PXXXXXXXXXXXX.” 
Results of an Update in the [[DRS]] Function 
When a [[transfer agent]] creates an Update in the [[PTS]]/[[PBS]] [[DRS]] function, the following transactions occur at [[DTCC]]: 
1. A deposit for the [[shares]] in question is made for the [[transfer agent]] at [[DTCC]], using a Limited [[participant]] Account (LPA). 
2. A credit for the [[transfer agent]]'s Limited [[participant]] Account in [[DTCC]]'s [[FAST]] Balance. 
3. [[DTCC]] creates a Delivery Order delivery, debiting the [[transfer agent]]'s LPA free position. 
4. [[DTCC]] creates a Deliver Order receive, crediting the [[Broker]]'s free position. 
Note 
LPA's must have a zero balance in their free position at the close of business. 
  
Figure 19: Update Successful Confirmation Message 

---

## Page 23

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[Direct Registration]] System ([[DRS]]) 23 
Rejecting a Transaction 
If a [[Broker]] identifies a problem with a [[transfer agent]]'s [[DRS]] Update, the [[Broker]] will use the Delivery Order function to reject the transaction. When 
this occurs, [[DTCC]] runs a process known as the [[DO]] Sweep to reverse the transactions involved, leaving a zero balance in the [[transfer agent]]'s 
account.  
The following procedure explains how to reject such a transaction. The procedure assumes you can access the [[securities]] Processing functions in 
the [[PBS]] – Corporate Trust Services application. (See the Accessing Corporate Trust Services [[securities]] Functions topic.) 
1. From the list of [[securities]] Processing functions in the [[PBS]] – Corporate Trust Services application, click [[Direct Registration]] System. 
2. The [[Direct Registration]] System - Main Menu appears. In the [[Option]] drop-down menu, select “1 – Update” and click Submit. 
 
Figure 21: [[Direct Registration]] System - Main Menu 
  
Figure 20: [[Direct Registration]] System function / link 
Client identifiable information 
on screen captures in this 
example have been hidden. 
 

---

## Page 24

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[Direct Registration]] System ([[DRS]]) 24 
3. The [[Direct Registration]] System - Transaction Update page appears. Enter all applicable information. Required fields are indicated with a red 
asterisk (*). 
4. To validate the details you have entered, click Submit. 
5. If error messages appear, correct the error, and click Submit. 
6. When there are no additional errors found, click Update. 
  
All fields 
marked with a 
red asterisk (*) 
are required. 
Figure 22: [[Direct Registration]] System - Transaction Update 

---

## Page 25

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[Direct Registration]] System ([[DRS]]) 25 
View a [[DRS]] Transaction 
Use the following procedure to verify a [[DRS]] transaction. The procedure assumes you can access the [[securities]] Processing functions in the [[PBS]] – 
Corporate Trust Services application. (See the Accessing Corporate Trust Services [[securities]] Functions topic.) 
1.  From the list of [[securities]] Processing functions in the [[PBS]] – Corporate Trust Services application, click [[Direct Registration]] System. 
 
2. The [[Direct Registration]] System - Main Menu appears. In the [[Option]] drop-down menu, select “2 – Inquiry” and click Submit. 
3. The [[Direct Registration]] System - Transaction Inquiry page appears. In the fields provided, type the [[CUSIP]] and select a Process Date From 
and a Process Date To and click Submit. 
4. The Transaction Inquiry page displays the results, 11 rows at a time. Use the Next and Previous links to scroll through the results. 
5. To view additional details for a particular transaction, select “S - Additional Information” from the Select drop-down menu and click Submit. 
  


---

## Page 26

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[Direct Registration]] System ([[DRS]]) 26 
Verify a [[DRS]] Transfer Request 
Use the following procedure to verify a [[DRS]] Transfer Request. The procedure assumes you can access the [[securities]] Processing functions in the 
[[PBS]] – Corporate Trust Services application. (See the Accessing Corporate Trust Services [[securities]] Functions topic.) 
1. From the list of [[securities]] Processing functions in the [[PBS]] – Corporate Trust Services application, click [[Direct Registration]] System Profile 
Modification ([[participant]]). 
  
Figure 23: [[DRS]] Profile Modification ([[participant]]) function / link 

---

## Page 27

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[Direct Registration]] System ([[DRS]]) 27 
2. The [[Direct Registration]] System – Profile Modification by [[participant]] – Agent Menu page appears. In the Selection Criteria section enter “2” 
(Inquiry) in the [[Option]] field. 
3. Enter “A” (Approved) in the Status field. Click Submit. 
 
Figure 24: Selection Criteria [[Option]] 
Figure 25: Selection Criteria Status 
Client identifiable information 
on screen captures in this 
example have been hidden. 

---

## Page 28

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[Direct Registration]] System ([[DRS]]) 28 
4. The Transaction Summary List appears. It lists all approved [[DRS]] transfer requests from the previous month. Select the transaction you want to 
verify and enter “S” in the Select column. Click Submit.  
5. The Status Inquiry Detail for the selected [[DRS]] transaction appears. Once you have verified the status of the [[DRS]] transfer request, you must 
update the [[DRS]] system. Begin by selecting the Services Menu. 
  
Figure 26: Transaction Summary List 
Figure 27: Status Inquiry Detail – Services Menu 


---

## Page 29

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[Direct Registration]] System ([[DRS]]) 29 
6. This opens the Home page of the [[PBS]] – Corporate Trust Services application. From the list of [[securities]] Processing functions, click Direct 
Registration System. 
7. From the [[Direct Registration]] System – Main Menu, open the dropdown menu for the [[Option]] field.  
Figure 28: [[Direct Registration]] System function / link 
Figure 29: [[Direct Registration]] System - Main Menu 

---

## Page 30

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[Direct Registration]] System ([[DRS]]) 30 
8. Select 1 – Update from the menu. Click Submit. 
 
Figure 30: [[Direct Registration]] System - Main Menu [[Option]] 
9. The Transaction Form appears. Fill in the fields marked with a red asterisk (*) and click Update.   
All fields 
marked with a 
red asterisk (*) 
are required. 
Figure 31: [[DRS]] - Transaction Update 

---

## Page 31

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[Direct Registration]] System ([[DRS]]) 31 
10. A confirmation message in yellow that reads “Update Successful” will appear at the top of the screen. 
 
 
 
 
 
 
  
Figure 32: Transaction Update Confirmation 

---

## Page 32

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[FAST]] Balance Confirmations 32 
[[FAST]] BALANCE CONFIRMATIONS 
Confirm a [[FAST]] Balance 
Use the following procedure to confirm a [[FAST]] Balance. The procedure assumes you can access the [[securities]] Processing functions in the [[PBS]] – 
Corporate Trust Services application. (See the Accessing Corporate Trust Services [[securities]] Functions topic.) 
1. From the list of [[securities]] Processing functions in the [[PBS]] – Corporate Trust Services application, click [[FAST]] Balance Confirmations. 
  
Figure 33: [[securities]] Processing - [[FAST]] Balance Confirmations 

---

## Page 33

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[FAST]] Balance Confirmations 33 
2. The [[FAST]] Balance Confirmation System – Main Menu opens. Enter “7” (Balance Confirmation Update) in the [[Option]] field (required). 
3. Enter TA Number (required – may be prepopulated). 
4. Enter oldest day to sign off. Failing to [[DO]] so will generate error message: (No data available). 
5. Click Submit. 
 
 
 
Figure 34: [[FAST]] Balance Confirmation System 
Client identifiable information 
on screen captures in this 
example have been hidden. 

---

## Page 34

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[FAST]] SCL (Shipment Control List) Confirmation 34 
[[FAST]] SCL (SHIPMENT CONTROL LIST) CONFIRMATION 
Overview 
The [[FAST]] SCL Confirmation application allows the [[FAST]] [[transfer agent]] to confirm or reject an entire SCL or to [[DO]] a partial reject of one or more 
[[participant]] line items on an SCL. The system also allows the [[transfer agent]] to inquire about pending [[FAST]] deposit rejects and SCLs. 
When to Use 
Use [[FAST]] SCL Confirmation when you want to confirm or reject an SCL fully or partially and to inquire about pending [[FAST]] deposit rejects or SCLs. 
Confirm or Reject an SCL 
Use this procedure when you want to confirm or reject an SCL. The procedure assumes you can access the [[securities]] Processing functions in the 
[[PBS]] – Corporate Trust Services application. (See the Accessing Corporate Trust Services [[securities]] Functions topic.) 
1. From the list of [[securities]] Processing functions in the [[PBS]] – Corporate Trust Services application, click [[FAST]] SCL Confirmation. If prompted, 
type your User [[ID]] and password, and click Submit. 
2. The [[FAST]] SCL Confirmation - Main Menu appears. Type information in the following fields:  
• [[Option]]: Type “1”. 
Figure 35: [[securities]] Processing - [[FAST]] SCL Confirmation 

---

## Page 35

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[FAST]] SCL (Shipment Control List) Confirmation 35 
• TA Number: Type the [[transfer agent]] number. 
• [[CUSIP]]: Type the [[CUSIP]] number (optional). 
• SCL [[ID]]: Type the SCL identification number (optional). 
Note 
You must enter either the [[CUSIP]] number or the SCL [[ID]]. 
3. Click Submit. 
4. Type information in the following fields:  
• Issue Date: Type the global issue date for all the SCLs in mm/dd/yy format in the field.  
Note 
The issue date is not required if you are rejecting the SCL. 
• C/R: Type either “C” (confirm) or “R” (reject) in the field. 
• Reject Code: Type the appropriate reject code in the field if you entered R in the C/R field. 
• Issue Date: Type the issue date for this SCL only if it is not the same as the global issue date. 
5. Click Update. 
6. Type free form information in the Reason field. 
  

---

## Page 36

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[FAST]] SCL (Shipment Control List) Confirmation 36 
Reject or Partially Confirm SCL Line Items 
Use this procedure if you want to reject specific line items that are part of an SCL. The procedure assumes you can access the [[securities]] Processing 
functions in the [[PBS]] – Corporate Trust Services application. (See the Accessing Corporate Trust Services [[securities]] Functions topic.) 
1. From the list of [[securities]] Processing functions in the [[PBS]] – Corporate Trust Services application, click [[FAST]] SCL Confirmation. If prompted, 
type your User [[ID]] and password, and click Submit. 
2. The [[FAST]] SCL Confirmation – Main Menu appears. Type information in the following fields: 
• [[Option]]: Type “2”. 
• TA Number: Type the [[transfer agent]] number. 
• SCL [[ID]]: Type the SCL identification number. 
3. Click Submit. 
4. Type information in the following fields: 
• Issue Date: Type the global issue date for all the SCLs in mm/dd/yy format in the field. 
• Action: Type either “R” (reject line item), “P” (partially confirm a portion of the [[participant]] line item) or leave blank. 
Note 
Line items that are not rejected will be confirmed. 
• Reject Code: Type the reject code only if you entered R or P in the Action field. 
5. Click one of the following: 
• Submit (to validate the data) 
Figure 36: [[securities]] Processing - [[FAST]] SCL Confirmation 

---

## Page 37

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[FAST]] SCL (Shipment Control List) Confirmation 37 
• Update (to update the SCL 
6. If you entered R in the Action field and did not enter the reject code the [[participant]] Line Item Reject screen appears. 
a. Type a reason for the reject in free form in the Reason field and click Submit to update the SCL. 
7. If you entered P in the Action field the [[participant]] Line Item Reject screen appears requesting reject information.  
a. Type information in the following fields: 
o Quantity Rejected 
o Quantity Confirmed 
o Reason 
8. Click one of the following: 
• Click Submit to validate the information. 
• Click Update to update the information. 
 
  

---

## Page 38

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[FAST]] SCL (Shipment Control List) Confirmation 38 
View the Status of an SCL 
Use this procedure to obtain all the available information for an SCL. The procedure assumes you can access the [[securities]] Processing functions in 
the [[PBS]] – Corporate Trust Services application. (See the Accessing Corporate Trust Services [[securities]] Functions topic.) 
1. From the list of [[securities]] Processing functions in the [[PBS]] – Corporate Trust Services application, click [[FAST]] SCL Confirmation. If prompted, 
type your User [[ID]] and password, and click Submit. 
2. The [[FAST]] SCL Confirmation – Main Menu appears. Type information in the following fields: 
• [[Option]]: Type “4”. 
• TA Number: Type the [[transfer agent]] number. 
• [[CUSIP]]: Type the [[CUSIP]] number (optional) 
• SCL [[ID]]: Type the SCL identification number (optional) 
Note 
You must enter either the [[CUSIP]] number or the SCL [[ID]]. 
3. Click Submit. 
4. Type information in the following fields: 
• [[Option]]: Type “4”. 
• TA Number: Type the [[transfer agent]] number. 
• [[CUSIP]]: Type the [[CUSIP]] number (optional). 
• SCL [[ID]]: Type the SCL identification number (optional) 
Figure 37: [[securities]] Processing - [[FAST]] SCL Confirmation 

---

## Page 39

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[FAST]] SCL (Shipment Control List) Confirmation 39 
Note 
You must enter either the [[CUSIP]] number or the SCL [[ID]]. 
5. Click Submit. 
 
  

---

## Page 40

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[FAST]] SCL (Shipment Control List) Confirmation 40 
Confirm Full SCLs 
Use this procedure to confirm full [[FAST]] SCLs. The procedure assumes you can access the [[securities]] Processing functions in the [[PBS]] – Corporate 
Trust Services application. (See the Accessing Corporate Trust Services [[securities]] Functions topic.) 
1. From the list of [[securities]] Processing functions in the [[PBS]] – Corporate Trust Services application, click [[FAST]] SCL Confirmation. If prompted, 
type your User [[ID]] and password, and click Submit. 
2. The [[FAST]] SCL Confirmation – Main Menu appears. Type information in the following fields: 
• [[Option]]: Type “5”. 
3. TA Number: Type the [[transfer agent]] number. 
4. Click Submit. 
5. Type the global issue date for all the SCLs that are displayed in the Issue Date field in mm/dd/yy format. 
6. Click Submit to validate the information. 
Note 
You can wand up to 10 barcodes before clicking Submit. 
7. Click Confirm to confirm the SCLs. 
Note 
You can click Cancel Confirm if you want to cancel your confirmation. 
Figure 38: [[securities]] Processing - [[FAST]] SCL Confirmation 

---

## Page 41

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[FAST]] SCL (Shipment Control List) Confirmation 41 
Reject Full SCLs 
Use this procedure when you want to reject full [[FAST]] SCLs. The procedure assumes you can access the [[securities]] Processing functions in the [[PBS]] 
– Corporate Trust Services application. (See the Accessing Corporate Trust Services [[securities]] Functions topic.) 
1. From the list of [[securities]] Processing functions in the [[PBS]] – Corporate Trust Services application, click [[FAST]] SCL Confirmation. If prompted, 
type your User [[ID]] and password, and click Submit. 
2. The [[FAST]] SCL Confirmation – Main Menu appears. Type information in the following fields: 
• [[Option]]: Type “6”. 
• TA Number: Type the [[transfer agent]] number. 
3. Click Submit. 
4. Position your cursor next to a selected SCL [[ID]] and click Submit. 
5. Type “C” in the C field next to a selected line item to confirm the SCL. 
6. Click Submit to validate the information that you entered. 
7. Click Reject to reject the SCLs.  
Note  
You can click Cancel Reject if you want to cancel your reject. 
 
Figure 39: [[securities]] Processing - [[FAST]] SCL Confirmation 

---

## Page 42

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[FAST]] SCL (Shipment Control List) Confirmation 42 
Confirm or Reject [[FAST]] [[Underwriting]] SCLs 
Use this procedure when you want to confirm or reject an [[Underwriting]] [[FAST]] SCL. The procedure assumes you can access the [[securities]] 
Processing functions in the [[PBS]] – Corporate Trust Services application. (See the Accessing Corporate Trust Services [[securities]] Functions topic.) 
1. From the list of [[securities]] Processing functions in the [[PBS]] – Corporate Trust Services application, click [[FAST]] SCL Confirmation. If prompted, 
type your User [[ID]] and password, and click Submit. 
2. The [[FAST]] SCL Confirmation – Main Menu appears. Type “7” in the [[Option]] field. 
3. Type the [[transfer agent]] number in the TA Number field. 
4. Click Submit. 
5. Type one of the following in the C/R field next to a selected SCL: 
• “C” (to confirm) 
• “R” (to reject) 
6. Click Update. 
7. Type information in the following fields: 
• Contact 
• Phone 
• Comment 
8. Click Confirm. 
 
 
Figure 40: [[securities]] Processing - [[FAST]] SCL Confirmation 

---

## Page 43

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[FAST]] SCL (Shipment Control List) Confirmation 43 
Unconfirm Deposit SCLs 
Use this procedure when you want to unconfirm a deposit SCL.  
Note 
You can only confirm a deposit SCL with an activity code 102 or 103. In addition, these SCLs can only be unconfirmed within 48 hours of the time they were 
confirmed. 
The procedure assumes you can access the [[securities]] Processing functions in the [[PBS]] – Corporate Trust Services application. (See the Accessing 
Corporate Trust Services [[securities]] Functions topic.) 
1. From the list of [[securities]] Processing functions in the [[PBS]] – Corporate Trust Services application, click [[FAST]] SCL Confirmation. If prompted, 
type your User [[ID]] and password, and click Submit. 
2. The [[FAST]] SCL Confirmation – Main Menu appears. Type “8” in the [[Option]] field. 
3. Type the [[transfer agent]] number in the TA Number field. 
4. Click Submit to unconfirm the SCL. 
  
Figure 41: [[securities]] Processing - [[FAST]] SCL Confirmation 

---

## Page 44

Corporate Trust Services – [[securities]] Processing for [[FAST]] Agents 
[[FAST]] SCL (Shipment Control List) Confirmation 44 
Confirm a Partially Confirmed or Rejected SCL 
Use this procedure when you want to confirm a partially confirmed or previously rejected SCL.  
Note 
You can only confirm a deposit SCL with an activity code 102 or 103. In addition, these SCLs can only be unconfirmed within 48 hours of the time they were 
confirmed. 
The procedure assumes you can access the [[securities]] Processing functions in the [[PBS]] – Corporate Trust Services application. (See the Accessing 
Corporate Trust Services [[securities]] Functions topic.) 
1. From the list of [[securities]] Processing functions in the [[PBS]] – Corporate Trust Services application, click [[FAST]] SCL Confirmation. If prompted, 
type your User [[ID]] and password, and click Submit. 
2. The [[FAST]] SCL Confirmation – Main Menu appears. Type “9” in the [[Option]] field. 
3. Type the [[transfer agent]] number in the TA Number field. 
4. Click Submit. 
5. Position your cursor next to a selected SCL [[ID]] and click Submit. 
6. Type “C” in the C field next to a selected line item to confirm the SCL. 
7. Click Update SCL. 
 
 
Figure 42: [[securities]] Processing - [[FAST]] SCL Confirmation 

---

## Page 45

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 