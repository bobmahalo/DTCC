---
title: "DVP Repo Collateral Substitution Examples Reference Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd187_dvp_repo_collateral_substitution_examples_reference_guide_20220425.pdf"
pages: 19
size: "736.6 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# DVP Repo Collateral Substitution Examples Reference Guide

**Original File:** [gsd187_dvp_repo_collateral_substitution_examples_reference_guide_20220425.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd187_dvp_repo_collateral_substitution_examples_reference_guide_20220425.pdf)  
**Category:** GSD  
**Total Pages:** 19  
**File Size:** 736.6 KB  

---

## Page 1

DVP Repo [[collateral]] 
Substitution Examples 
Reference Guide
Fixed Income Clearing Corporation
Government [[securities]] Division

---

## Page 2

The DVP Repo [[collateral]] Substitution Examples Reference Guide (hereinafter, the "document") is provided as a convenience to Members and is for 
information purposes only. Although [[FICC]] may make this document available to Members, it shall be under no obligation to [[DO]] so, nor having once or more 
done so, shall [[FICC]] have a continuing obligation to make available this document or other related information of a certain type.
[[FICC]] does not represent the accuracy, adequacy, timeliness, completeness, or fitness for any particular purpose of any information provided to Members in 
this document, which is provided as-is. [[FICC]] shall not be liable for any loss related to such information (or the act or process of providing such information) 
resulting directly or indirectly from mistakes, errors, or omissions, other than those caused directly by gross negligence or willful misconduct on the part of 
[[FICC]]. [[FICC]] shall not be liable for: (1) any loss resulting directly or indirectly from interruptions, delays, or defects arising from or related to providing this 
guide; and (2) any special, consequential, exemplary, incidental, or punitive damages. 
Further, the information contained in this document is subject to change. Members and other authorized users of the document will find the most current 
version of the document on [[DTCC]]’s Learning Center site, www.dtcclearning.com. [[FICC]] shall bear no responsibility for any losses associated with the 
failure of Members or other authorized users to follow [[FICC]]’s most current document.
Disclaimer

---

## Page 3

This document will provide examples of DVP Repo Substitution Notifications including:
Example # 1:   Sub Not Accepted – Replacement [[collateral]] Has Incorrect Par Denomination
Example # 2:   Sub Not Accepted – Cannot Create Multiple Tails
Example # 3:   Sub Not Accepted – Replacement [[collateral]] Has Invalid [[CUSIP]]
Example # 4:   Sub Not Accepted – Cannot Change Repo Rate on Replacement [[collateral]]
Example # 5:   Sub Accepted, Sub Not Processed – Current [[collateral]] Does Not Exist
Example # 6:   Sub Accepted, Sub Processed – Sub w/ Multiple Replacement [[collateral]] 
Example # 7:   Sub Accepted, Sub Processed – Sub w/ [[CUSIP]] Changing Only
Example # 8:   Sub Accepted, Sub Processed – Sub w/ Additional Tail
Example # 9: Sub Accepted, Sub Processed – Bulk Sub w/ Principal Changing
Example # 10: Sub Accepted, Sub Processed – Bulk Sub w/ Par Changing 
Example # 11: Sub Accepted, Sub Processed – Bulk Sub w/ Max Par Amount Allowed 
Example # 12: Sub Accepted, Sub Processed – Future Pending Sub 
Example # 13: Sub Accepted, Sub Processed – Subbing a “Tail” Only
Example # 14: Sub Accepted, Sub Processed – Sub w/ Par & Principal Changing
List of DVP Repo Substitution Notification Examples Included in this Guide
DVP Repo [[collateral]] Substitution Examples Reference Guide
3

---

## Page 4

Example # 1: Sub Not Accepted – Replacement [[collateral]] Has Incorrect Par Denomination
DVP Repo [[collateral]] Substitution Examples Reference Guide
4
Example 1. Substituting [[collateral]] with 
invalid par amount.
The system will not accept a 
notification where the replacement 
[[collateral]] has a par amount that is not 
eligible for [[settlement]] due to an invalid 
par minimum/multiple denomination. 

---

## Page 5

Example # 2: Sub Not Accepted – Cannot Create Multiple Tails
DVP Repo [[collateral]] Substitution Examples Reference Guide
5
Example 2. Substituting [[collateral]] with 
multiple tails.
The system will not accept a notification 
where the replacement [[collateral]] has 2 
tail pieces. The system will only accept a 
substitution notification where the 
replacement [[collateral]] has 1 tail. A trade 
with a par value of less than $50MM is 
considered a “tail”. 

---

## Page 6

Example # 3: Sub Not Accepted – Replacement [[collateral]] Has Invalid [[CUSIP]]
DVP Repo [[collateral]] Substitution Examples Reference Guide
6
Example 3. Substituting [[collateral]] with 
invalid security.
The system will not accept a 
notification where the replacement 
[[collateral]] has a security that is not 
eligible for [[settlement]] because the 
security is not set up in the security 
master file. 

---

## Page 7

Example # 4: Sub Not Accepted – Cannot Change Repo Rate on Replacement [[collateral]]
DVP Repo [[collateral]] Substitution Examples Reference Guide
7
Example 4. Substituting [[collateral]] with 
a mismatched contract repo rate.
The system will not accept a 
notification where there is an attempt to 
change the repo rate on the trade. The 
system does not permit the changing of 
the repo rate on the replacement 
[[collateral]].

---

## Page 8

Example # 5: Sub Accepted, Sub Not Processed – Current [[collateral]] Does Not Exist
DVP Repo [[collateral]] Substitution Examples Reference Guide
8
Example 5. Substituting [[collateral]] that 
is not currently in the system.
The system will not process (NP) a 
notification for current [[collateral]] that 
cannot be validated by the system. 
This example has the incorrect [[CUSIP]] 
entered in the [[CUSIP]] field for the 
current [[collateral]].
Note: This substitution 
was accepted by the 
system but not processed 
by the system.

---

## Page 9

Example # 6: Sub Accepted, Sub Processed – Sub w/ Multiple Replacement [[collateral]]
DVP Repo [[collateral]] Substitution Examples Reference Guide
9
Example 6. Substituting [[collateral]] for 
two different [[securities]].
The system can process a substitution 
notification where the replacement 
[[collateral]] has more than one security. 

---

## Page 10

Example # 7: Sub Accepted, Sub Processed – Sub w/ [[CUSIP]] Changing Only
DVP Repo [[collateral]] Substitution Examples Reference Guide
10
Example 7. Substitution of security only, 
no change to par or principal.
The system can process a substitution 
notification where the only the security 
changes.

---

## Page 11

Example # 8: Sub Accepted, Sub Processed – Sub w/ Additional Tail
DVP Repo [[collateral]] Substitution Examples Reference Guide
11
Example 8. Adding a tail to a repo 
transaction via repo substitution.
The system can process a substitution 
notification where the replacement 
[[collateral]] has one tail. 
Note: A trade with a par value of less 
than $50MM is considered a “tail”. 

---

## Page 12

Example # 9: Sub Accepted, Sub Processed – Bulk Sub w/ Principal Changing
DVP Repo [[collateral]] Substitution Examples Reference Guide
12
Example 10. Entering a “bulk” sub 
where the Principal is changing (Par 
Fill).  A “bulk” sub means a 
notification that is entered for 
multiple lots of 50MM in par. 
The system can process a 
substitution notification where the 
current & replacement [[collateral]] 
includes multiple lots of 50MM in 
par. A repo substitution notification 
can be entered with a max par of up 
to 400MM. 

---

## Page 13

Example # 10: Sub Accepted, Sub Processed – Bulk Sub w/ Par Changing
DVP Repo [[collateral]] Substitution Examples Reference Guide
13
Example 11. Entering a “bulk” sub 
where the Par is changing (Money 
Fill). A “bulk” sub means a 
notification that is entered for 
multiple lots of 50MM in par. 
The system can process a 
substitution notification where the 
current & replacement [[collateral]] 
includes multiple lots of 50MM in 
par. A repo substitution notification 
can be entered with a max par of up 
to 400MM. 

---

## Page 14

Example # 11: Sub Accepted, Sub Processed – Bulk Sub w/ Max Par Amount Allowed
DVP Repo [[collateral]] Substitution Examples Reference Guide
14
Example 12. Entering a max par sub. 
The system can process a substitution 
notification where the replacement 
[[collateral]] includes multiple lots of 
50MM up to 400MM. 

---

## Page 15

Example # 12: Sub Accepted, Sub Processed – Future Pending Sub 
DVP Repo [[collateral]] Substitution Examples Reference Guide
15
Example 12. Entering a sub for a 
future effective date. 
The system will accept a substitution 
notification for future processing if the 
effective business date is a future and 
valid business date. 

---

## Page 16

Example # 13: Sub Accepted, Sub Processed – Subbing a “Tail” 
DVP Repo [[collateral]] Substitution Examples Reference Guide
16
Example 14. Substituting a tail on a 
repo transaction.
The system can process a substitution 
notification on a repo transaction where 
the par is under $50MM. 

---

## Page 17

Example # 14: Sub Accepted, Sub Processed – Sub w/ Par & Principal Changing
DVP Repo [[collateral]] Substitution Examples Reference Guide
17
Example 15. Entering a sub to change 
the security, par and principal.
The system can process a substitution 
notification where the security, par and 
principal all change.

---

## Page 18

To access additional self-paced learning, 
how-to videos, guides and other 
documentation, visit:
www.dtcclearning.com
For all support services
www.[[DTCC]].com/client-center
18

---

## Page 19

© 2022 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation.
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself 
does not provide such services. Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in which 
such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.
Publication Code: 