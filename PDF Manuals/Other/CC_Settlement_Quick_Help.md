---
title: "ClaimConnect™ Settlement Quick Help"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/CC_Settlement_Quick_Help.pdf"
pages: 14
size: "581.5 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# ClaimConnect™ Settlement Quick Help

**Original File:** [CC_Settlement_Quick_Help.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/CC_Settlement_Quick_Help.pdf)  
**Category:** Other  
**Total Pages:** 14  
**File Size:** 581.5 KB  

---

## Page 1

 
 
 
 
 
CLAIMCONNECT™ 
[[settlement]] QUICK HELP 
VERSION 1.0 
SEPTEMBER 8, 2020 
 


---

## Page 2

 
 
© 2020 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
 
Doc Date: September 8, 2020 
Publication Code: CA133 
Service: ClaimConnect™ 
Title: [[settlement]] Quick Help 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
[[settlement]] in the ClaimConnect™ Service ....................................................................................................... 4 
Process Overview ............................................................................................................................................... 4 
[[settlement]] Timing ............................................................................................................................................... 4 
[[settlement]] Scenarios .......................................................................................................................................... 5 
Differentiating ClaimConnect™ SPOs from Other SPOs .................................................................................... 5 
Distinct Attributes of the SC Reason Code ....................................................................................................... 5 
Viewing Claim SPOs ......................................................................................................................................... 6 
Automated Output ................................................................................................................................................ 8 
PARTPO ............................................................................................................................................................. 8 
Mainframe Dual Host (MDH) Payment Order Output ......................................................................................... 8 
ISO 15022 Payment Order Output ..................................................................................................................... 8 
Sample Format .................................................................................................................................................. 9 
CDTS Output Examples .................................................................................................................................... 9 
Example 1: C202014900000584 - SETOUTO ................................................................................................ 9 
Example 2: C202014900000602 - SETOUTO .............................................................................................. 11 
To Find More Information or Begin Testing .................................................................................................... 13 
 

---

## Page 4

[[settlement]] Quick Help 
[[settlement]] in the ClaimConnect™ Service 4 
[[settlement]] IN THE CLAIMCONNECT™ SERVICE 
When cash claims are submitted to the ClaimConnect™ service, the claims settle at [[DTC]] via Security Payment 
Orders (SPOs). The SPO used for cash [[settlement]] is unique to the ClaimConnect™ service’s process. This 
distinct SPO helps Participants to differentiate these money movements so that they can be applied as 
Corporate Actions. This document describes how the ClaimConnect™ service’s [[settlement]] works. 
Process Overview 
After a claim has been matched and one of the following is true: 
a) The current date is the previously agreed-upon Claim [[settlement]] Date, or 
b) The Settle after Match flag has been agreed to be set 
 
…the claim will attempt to settle cash between both [[participant]] accounts that entered into the claim obligation.  
 
[[settlement]] Timing 
[[settlement]] of the ClaimConnect™ service’s SPOs only occurs on [[settlement]] days. [[settlement]] does not occur 
on [[NYSE]] holidays or bank holidays (e.g., Memorial Day and Veterans Day) in the U.S.  
Claims [[settlement]] happens at six points during the day. All times are given in Eastern Time: 
• 8:30 a.m.,  
• 10:00 a.m.,  
• 12:00 p.m.,  
• 1:00 p.m.,  
• 2:00 p.m., and  
• 3:00 p.m. 
  


---

## Page 5

[[settlement]] Quick Help 
[[settlement]] in the ClaimConnect™ Service 5 
[[settlement]] Scenarios 
Below are some examples of when a claim may settle after it is matched: 
Today is… A claim was affirmed… The SPO will occur at… 
Monday, April 20 Friday, April 17 with a [[settlement]] Date of 
Tuesday, April 21 
8:30 a.m. on Tuesday, April 21 
Monday, April 20 Monday, April 20th at 9:45 a.m. with the Settle 
After Match feature set to Y 
10:00 a.m. on Monday, April 20 
Memorial Day (Monday) Today at 12:15 p.m. with the Settle After Match 
feature set to Y 
on the next [[settlement]] Date 
(Tuesday) at 8:30 a.m. 
Monday, April 20 Auto-matched today at 3:01 p.m. with a Claim 
[[settlement]] Date of April 20 
Tuesday, April 21 at 8:30 a.m. 
Differentiating ClaimConnect™ SPOs from Other SPOs 
Since the submission of SPOs is a preexisting activity that occurs throughout the course of the day, [[DTCC]] 
repurposed the existing (but unused) reason code “SC” to help Participants recognize when an SPO 
represents a claim from the ClaimConnect™ service. The SC reason code now represents “ClaimConnect™ 
Cash Movement.” 
Distinct Attributes of the SC Reason Code 
• “807” is the Reason Code number on the [[settlement]] Web Activity Inquiry function. 
• This SPO will only come from the ClaimConnect™ service. It cannot be input via the [[settlement]] Web 
Payment Order function or via an inbound transmission. 
• This SPO is neither reclaimable nor is it able to be cancelled. It is a systematic move only and cannot be 
modified by a user once it goes to settle. 
• This SPO will always bypass the Receiver Authorized Deliverer (RAD) function since the Claim has 
previously been approved by both parties within the ClaimConnect™ service. 
Note:  
When you have claims settling, it is important that your [[settlement]], P&S, cashiering, and/or treasury areas are aware 
of the activities so that they can account for the cash movements. This is especially important when there are debits 
posting to your account as those debits are bypassing RAD. 
• Once this SPO is made (i.e., the cash has moved from one [[participant]] to another), the claim will be 
systematically closed in the ClaimConnect™ service. 
• If a ClaimConnect™ SPO is not made and drops, it will not be reintroduced. The claim must be instructed 
again in the ClaimConnect™ service.  
If you have subscribed to email alerts within the application, you will receive an alert notifying you of the 
dropped SPO. 

---

## Page 6

[[settlement]] Quick Help 
[[settlement]] in the ClaimConnect™ Service 6 
Viewing Claim SPOs 
1. Log on to [[settlement]] Web.  
2. On the Activity tab, select Activity Inquiry. 
3. Click Input [[participant]] [[ID]].  
4. Click Search. 
 
The detail page appears for the SPO you selected. 
 
Items of note on this page include: 
1. The Reason Code in [[settlement]] Web is always “807.” 
2. The Reason Code Description is always “ClaimConnect Cash Movement.” 
3. The unique Claim [[ID]] is found in the Obligation Warehouse Control Number field.  
If you are unsure what this activity represents, you can perform a Quick Search using the Claim [[ID]] in the 
ClaimConnect™ service to identify the details. 
4. The Source of the SPO is always “CCCM” (for “ClaimConnect™ Cash Movement”). 
5. Line 1 of the Text Comments includes a character string made up of: 
• The Claim Xref for the credit side of the claim (starting with the characters “CREF”), 
• The Claim Xref for the debit side of the claim (starting with the characters “DREF”), and  
• The unique Claim [[ID]] (starting with the characters “[[ID]]”). 
6. The end of Line 3 of the Text Comments includes the Reason Code of “SC,” which is unique to this SPO. 


---

## Page 7

[[settlement]] Quick Help 
[[settlement]] in the ClaimConnect™ Service 7 
With the exception of “RSN CD=SC,” the data in lines two and three is not applicable to the ClaimConnect™ 
process and is reserved for future use. 

---

## Page 8

[[settlement]] Quick Help 
Automated Output 8 
AUTOMATED OUTPUT 
Automated output is available for Participants who: 
• Wish to automate the claim SPO, or  
• Are already consuming an outbound payment order transmission 
 
…and wish to make changes to their systems to filter these SPOs to a distinct location.  
There are three different types of payment order outputs.  
PARTPO  
• This is a proprietary format machine-readable file specifically for payment order records.  
• It is available from 3:45 pm through 11:45 am the following day.  
• Please click here for the file layout.  
• The code SC is available in position 50. 
• The unique Claim [[ID]] takes up the first 16 bytes of the position 211 filler.  
• The Claim format begins with a ‘C’ and is followed by 15 digits, e.g. C123456789012345. 
Mainframe Dual Host (MDH) Payment Order Output 
• This is also a proprietary machine-readable output specifically for payment orders.  
• The file layout is found in the image below.  
• The two-byte code of “SC” is available in position 152 as per the example below. This allows you to 
differentiate claim payment orders on this file. 
 
ISO 15022 Payment Order Output 
• The ISO SPO output is the most flexible of the three output types.  
• These are ISO standard messages that cover payment orders.  
• They are also known as MT543 messages.  
• Participants use the SPO specifications that are available here.  


---

## Page 9

[[settlement]] Quick Help 
Automated Output 9 
• There are four places on the messages that contain information to help your systems identify this as an 
SPO representing a claim in the ClaimConnect™ service:  
o Field :20C::COMM contains the 16-byte Claim [[ID]] (same format as above). 
o Field :22F::SETR/DTCYREAS/ contains the Reason Code of “SC.” 
o Field :22F::STCO/DTCYISRC/ contains the value “CCCM” (for ClaimConnect Cash Movement).  
o Field: 70E:: SPRO// contains the 60-byte string containing the CREF(Credit Xef);DREF(Debit 
Xref);[[ID]](Claim [[ID]]). 
Sample Format  
CREF1234567890123456;DREF1234567890123456;ID1234567890123456 
CDTS Output Examples 
Example 1: C202014900000584 - SETOUTO 
{1:F0100008608XXXX0001000001}{2:O5480000000000DTCYUS33XXXX00000000002005280457N}{
3:{113:0301}{108:0001000001000000}{115:00000000000} 
}{4: 
:16R:GENL 
:20C::SEME//00000F                     
:23G:INST 
:98C::PREP//20200528045735 
:16R:LINK 
:20C::RELA//D7FC1CDD47634121 
:16S:LINK 
:16R:LINK 
:20C::COMM//C202014900000584 
:16S:LINK 
:16R:STAT 
:25D::SETT/DTCY/XPRS 
:16S:STAT 
:16S:GENL 
:16R:SETTRAN 

---

## Page 10

[[settlement]] Quick Help 
Automated Output 10 
:35B:ISIN  US050105CK94 
:36B::SETT//UNIT/0, 
:19A::SETT//USD78,45 
:97A::SAFE//00008608 
:22F::SETR/DTCYREAS/00SC 
:22H::REDE//DELI 
:22H::PAYM//APMT 
:22F::STCO/DTCYISRC/CCCM 
:22F::STCO/DTCYTXNT/OTHR 
:22F::STCO/DTCYACTV/0078 
:98A::EXSE//20200528 
:98A::SETT//20200528 
:70E::SPRO//CREFAP20200528114420;DREFAP20200528 
114418;IDC202014900000584                     
 
:16R:SETPRTY 
:95R::DEAG/DTCYPART/00008608 
:16S:SETPRTY 
:16R:SETPRTY 
:95R::REAG/DTCYPART/00008610 
:16S:SETPRTY 
:16R:SETPRTY 
:95P::PSET//DTCYUS33 
:16S:SETPRTY 
:16S:SETTRAN 
-} 
  

---

## Page 11

[[settlement]] Quick Help 
Automated Output 11 
Example 2: C202014900000602 - SETOUTO 
{1:F0100008608XXXX0001000001}{2:O5480000000000DTCYUS33XXXX00000000002005280457N}{
3:{113:0301}{108:0001000001000000}{115:00000000000} 
}{4: 
:16R:GENL 
:20C::SEME//00000F                     
:23G:INST 
:98C::PREP//20200528045736 
:16R:LINK 
:20C::RELA//D7FC1CDDC0B1E322 
:16S:LINK 
:16R:LINK 
:20C::COMM//C202014900000602 
:16S:LINK 
:16R:STAT 
:25D::SETT/DTCY/XPRS 
:16S:STAT 
:16S:GENL 
:16R:SETTRAN 
:35B:ISIN  US050105CK94 
:36B::SETT//UNIT/0, 
:19A::SETT//USD78,45 
:97A::SAFE//00008608 
:22F::SETR/DTCYREAS/00SC 
:22H::REDE//DELI 
:22H::PAYM//APMT 
:22F::STCO/DTCYISRC/CCCM 
:22F::STCO/DTCYTXNT/OTHR 

---

## Page 12

[[settlement]] Quick Help 
Automated Output 12 
:22F::STCO/DTCYACTV/0078 
:98A::EXSE//20200528 
:98A::SETT//20200528 
:70E::SPRO//CREFAP20200528123035;DREFAP20200528 
123032;IDC202014900000602                     
                     
:16R:SETPRTY 
:95R::DEAG/DTCYPART/00008608 
:16S:SETPRTY 
:16R:SETPRTY 
:95R::REAG/DTCYPART/00008610 
:16S:SETPRTY 
:16R:SETPRTY 
:95P::PSET//DTCYUS33 
:16S:SETPRTY 
:16S:SETTRAN 
-} 
  

---

## Page 13

[[settlement]] Quick Help 
To Find More Information or Begin Testing 13 
TO FIND MORE INFORMATION OR BEGIN TESTING 
Payment order output is available to test in [[DTCC]]’s PSE-U test environment.  
If you would like to speak to someone regarding connectivity or testing, please send an email to 
DTCsupport@[[DTCC]].com 
 

---

## Page 14

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 