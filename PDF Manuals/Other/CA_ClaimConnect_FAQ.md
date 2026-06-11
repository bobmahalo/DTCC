---
title: "ClaimConnect™ Project FAQs"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/CA_ClaimConnect_FAQ.pdf"
pages: 7
size: "457.9 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# ClaimConnect™ Project FAQs

**Original File:** [CA_ClaimConnect_FAQ.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/CA_ClaimConnect_FAQ.pdf)  
**Category:** Other  
**Total Pages:** 7  
**File Size:** 457.9 KB  

---

## Page 1

 
1 
FAQs 
CLAIMCONNECT™ 
ClaimConnect™ Project Q&A 
AUGUST 21, 2019 
Q1 What are the browser requirements for this application? 
A1 To achieve the best user experience on ClaimConnect™, it is recommended that users utilize Google 
Chrome. The application will be available on IE 11, however, some features may not display well with 
future releases. 
Q2 Does the ClaimConnect™ application only work for [[DTC]]-eligible items? 
A2 No – the security in the claim does not need to be [[DTC]]-eligible. However, both you and your contra 
party need to be [[DTC]] Participants, and the underlying claim must be in USD. 
Q3 What are the fees associated with using the application? 
A3 Total fees will equal $1.85. There is no fee for initially submitting a claim. Once the claim is matched, 
each side of the claim will be charged $1.75. Additionally, a $0.10 fee per made side will be applied to 
process the SPO in [[settlement]]. The SPO charge is an existing [[settlement]] fee. 
Q4 Will there be a fee for aged ClaimConnect™ items that remain unaffirmed in the 
system after a period of time? 
A4 [[DTC]] is currently working with the industry to help establish best practices as they relate to Participants 
responding to a claim against them in a timely fashion. The end result of these discussions may be 
some type of disincentive fee; however, more feedback is needed from the Industry. 
Q5 Can I cancel claims with an OPEN status? 
A5 No. An Open / Matched claim will be settled on the agreed-upon [[settlement]] date. If a claim was 
submitted, matched, and settled in error, another claim can be submitted to reverse the transaction.  
Q6 What is the minimum amount of cash for which I can submit a claim? 
A6 Currently, the minimum for claims is $0.01. Based on feedback from the industry, [[DTCC]] can 
investigate the possibility of adding a minimum threshold for certain types of claims.  
Q7 What is the threshold for supervisory approval? 
A7 The system’s [[default]] is set to one penny, but you will be able to define the amount yourself. 

---

## Page 2

 
2 
FAQs 
Q8 If I submit a claim that exceeds my account's debit threshold, that claim will go for 
approval. In the meantime, if I make a modification to that claim prior to my 
manager approving it, what will happen in that case? 
A8 Since this is a real-time matching system, if a claim goes into an approval bucket but a manager has 
not approved it, any changes that are made to the claim will not be made, and the original claim, if 
approved, would be potentially matched. The approver would then need to reject the modified claim 
after approving the first claim. After that, the user could cancel that claim or resubmit a new one to 
apply the proper modifications that their contra party is aware of. 
Q9 I see that we can set an auto-approval amount, but can we set an amount for 
secondary approval? For example, for claims above a certain amount? 
A9 No. At this time, there is no secondary approval feature in ClaimConnect™. 
Q10 Is there a status for claims that are not made at [[DTC]] [[settlement]] due to lack of 
funds (for example, over debit cap)? 
A10 Not currently. Future releases of the application will account for this. 
Q11 Will the application support non-USD currencies? 
A11 Not currently. Expansion of the application to support foreign currency claims will be investigated 
based on industry requests. 
Q12 Am I able to bundle a number of claims to a specific contra party through the 
application? 
A12 Yes, if you and the contra party on the other side of the claim agree to key data, such as (but not 
limited to) [[CUSIP]], Event Type, and Amount. 
Q13 What is an API? What does it have to [[DO]] with the ClaimConnect™ application? 
A13 An API is an “application programming interface.” The API will allow for the pushing (submission) of 
claims and pulling (inquiries) of claim data. In the future, the ClaimConnect™ application will use APIs 
that will eliminate the need for clients to manually enter and search upon claims. 
Q14 Can I sort my claim search results by contra party? 
A14 Yes. You can sort by any column heading in the Search results, including contra party. You can also 
filter the results by any criteria you choose. 

---

## Page 3

 
3 
FAQs 
Q15 If my firm is claiming the funds from a contra firm, should we choose Credit or 
Debit in the below field? 
 
A15 If your firm is due the funds, you should choose “Credit.” 
Q16 Is this system a substitute for doing SPO charges? 
A16 Yes. ClaimConnect™ systematically creates SPOs. 
Q17 Does this initiative branch out to all SPOs? 
A17 This is a special type of SPO that is different from any other SPO. ClaimConnect™ is the only 
application that generates this particular SPO. For example, ClaimConnect™ SPOs will bypass RAD 
but are subject to risk controls (i.e., you will need to be in a credit position in your [[collateral]] monitor). 
Q18 Can we add a [[settlement]] (SPO) code based on event type so that the systems at 
the client’s shop know where to route the information based on that code? 
A18 There are other ways to map these SPOs to your system. They include a new SPO Reason Code, 
source, claim control number [[ID]], and claim-specific narrative that clients can use to differentiate these 
claims from other payment order activities.   
Q19 Will items that settle be mapped to the correct internal account? Where will the 
money land on a [[participant]] level? 
A19 It will be a new SPO Reason Code and would go to the [[DTC]] [[participant]] [[settlement]] Account. 
Participants will need to ensure mapping to their internal accounts based on the  SPO Reason Code. 


---

## Page 4

 
4 
FAQs 
Q20 Is there a daily deadline to settle SPOs? 
A20 3:00 p.m. is the last time to close a claim. 
Q21 If I make a modification to an already-approved claim prior to the claim being 
matched, [[DO]] I need to have the claim approved again? Is this true for a money 
decrease as well as a money increase? 
A21 If the claim has been modified and the debit claim amount is either equal to or greater than the 
account's debit threshold, the claim will need to be approved again. If the claim that has been 
previously approved has an amount less than the account's debit threshold, the claim will not need to 
be reapproved again; however, there will be a note sent in an approver e-mail alert noting that this 
transaction has been submitted without going through approvals.  
Q22  If I cancel a claim that was already approved, does that need to go back to 
approvals? 
A22 All canceled claims that were previously approved will need to be reapproved again.  
Q23 Will there be S2 or S8 cutoffs for the SPOs? 
A23 ClaimConnect™ will be using a different set of reason codes, not S2 or S8. Three o’clock p.m. is the 
last time [[DTC]] will send a slice of claim data to [[settlement]] for processing. 
Q24 If I miss the S2 cutoff (11:00 a.m.) time, and the claim is already approved, what 
should I [[DO]]? Should I initiate a new claim? 
A24 You [[DO]] not need to initiate a new claim. There will be 6 slices of [[settlement]] throughout the day, 
beginning at 8:30 a.m. and ending at 3:00 p.m. If, for example, you submit a claim at 9:00 a.m. and 
you have selected the feature “Settle Upon Match,” and your contra party goes into that claim and 
affirms it at 9:40, that SPO will automatically go out in the 10:00 a.m. [[settlement]] slice. An affirmation at 
11:15 means that the SPO will go out at noon, etc. Anything submitted after 3:00 p.m. will go into the 
next business day’s [[settlement]] slice at 8:30 a.m. 
Q25 [[DO]] both parties need to submit claims in order for the system to match? 
A25 No. When a party receives an advisory claim, they can affirm the transaction to match the claim. 
Q26: What is an Advisory Claim? 
A26: An advisory claim is a claim that has been submitted against you that you need to take some type of 
action on.  

---

## Page 5

 
5 
FAQs 
Q27 How [[DO]] we know which fields are matched on? 
A27 The Quick Guide presents a table of all fields that are used in the matching process. Future 
enhancements will provide a tool tip to determine if an exact match is required for claims submitted by 
both parties to match.  
Q28 Can we have tooltips for each field? I want to know everything I can about each 
field. 
A28 Tooltips for particular fields are already being planned. The development team will look into expanding 
the scope of the tooltips. In addition, context-sensitive Help will be available for key pages in the 
application. You will be able to access the general Help from any page in the application. 
Q29 How will I be able to use ClaimConnect™ for all of my contra parties? 
A29 After the Important Notice went out, firms outside the workgroup were made aware of this 
development project. Clients are our best advocates. Please mention your participat ion in this test 
group to everyone with whom you [[DO]] business; the service will only work if everyone participates. We 
will participate in broader Marketing activities in order to draw more interest from the [[DTCC]] side. 
Q30 Is the Dashboard displayed in real-time? 
A30 Yes, but not like a [[Stock]] ticker feed. You have to either refresh the page or navigate away and come 
back.  
Q31 Where are the open claims? Debits? Credits? 
A31 When performing a search, you can limit your results to a particular state that the claim is in. 
You can then filter your search results by any status, including Open (i.e., matched and waiting for 
[[settlement]]). 
Q32 How long will the Claims data be archived? 
A32 The initial roll-out of ClaimConnect™ will store data for two years. Additional data compliance efforts 
performed by [[DTCC]] may extend that range based on data retainment policies.  
Q33 Is there functionality in the Dashboard to see how many claims you received in a 
day? A month? A year? 
A33 The dashboard will provide users with a snapshot of their claim activity at a moment in time. There will 
be historical information available related to how long a claim has been open based on certain claim 
states. 

---

## Page 6

 
6 
FAQs 
Q34 Is there a way to route ClaimConnect™ e-mail alerts to particular people in my 
company? 
A34 Yes. The Client Profile functionality allows you to add a recipient to an e-mail alert list address based 
on an event type group. Select the Client Profile – Manage [[Option]] on the Client Profile menu, click 
Add Contact, and select “Email Alert.”  
Q35 If the client contact at our firm leaves and someone else takes over, is there a 
specific group we would contact to make updates to the contact information? 
A35 You would [[DO]] it yourself using the Client Profile – Manage [[Option]] on the Client Profile menu. 
Q36 When I subscribe to an email list via the Client Profile facility, when [[DO]] I get email 
messages? Can I change the timeline? 
A36 When you elect to receive e-mail alerts for an event group, you will receive an e-mail at 10:00 a.m. 
and/or 3:00 p.m. when claims have been submitted against you.  
You cannot change the e-mail timing, but you can go into ClaimConnect™ at any time and look at the 
claims that have been made against you. The information in ClaimConnect™ is available in real time. 
In addition, the e-mails will remain in the inbox that you have chosen. 
Q37 On the e-mail alert message, is it possible to see the claim amount as well as 
number of claims? 
A37 Not at the moment. However, the Dashboard displays claim amounts broken down by claims, 
advisories, DKs, canceled claims, debits, credits, etc. as well as in total. You can use the pie chart on 
the upper right of the Dashboard that contains the value information. 
Q38 Will there be reporting functionality for looking at the volume of 
submitted/accepted claims? 
A38 A report feature will be available in Q4. 
 

---

## Page 7

 
 
Copyright © 1999 - 2019 by The Depository Trust & Clearing Corporation (“[[DTCC]]”). 
 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Info: August 21, 2019  
Publication Code: CA120 
Service: ClaimConnect™ 
Title: ClaimConnect™ Project Q&A 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
