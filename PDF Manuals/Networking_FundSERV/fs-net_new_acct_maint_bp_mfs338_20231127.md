---
title: "FS & Networking - New Account / Account Maintenance Transparency Enhancements – Best Practices"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs-net_new_acct_maint_bp_mfs338_20231127.pdf"
pages: 25
size: "500.9 KB"
category: "Networking_FundSERV"
ingested_on: "2026-06-05"
---

# FS & Networking - New Account / Account Maintenance Transparency Enhancements – Best Practices

**Original File:** [fs-net_new_acct_maint_bp_mfs338_20231127.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs-net_new_acct_maint_bp_mfs338_20231127.pdf)  
**Category:** Networking_FundSERV  
**Total Pages:** 25  
**File Size:** 500.9 KB  

---

## Page 1

 
 
 
Fund/SERV & Networking 
NEW ACCOUNT / ACCOUNT MAINTENANCE 
TRANSPARENCY ENHANCEMENTS – BEST 
PRACTICES 
NOVEMBER 27, 2023 
 

---

## Page 2

 
CHANGE HISTORY 
Dates Changes 
November 27, 2023 Document rebranded and reviewed.  
October 3, 2022 Best Practices Published. 

---

## Page 3

 
 
TABLE OF CONTENTS 
1. Background ...................................................................................................................................................... 4 
Introduction ......................................................................................................................................................... 4 
2. Summary of Enhancements ............................................................................................................................ 5 
3. Field Names & Descriptions ............................................................................................................................ 6 
4. Implementation Considerations ..................................................................................................................... 7 
5. Fund/SERV & Networking– Best Practices ................................................................................................... 8 
Fund/SERV Order (001), Correction (003), As of Order (004), Registration (401), and Confirm (005,006,025) 
Records ............................................................................................................................................................... 8 
Networking Account Conversion/Update (A/B/T50, A/B/T/51) Records ...........................................................12 
6. Use Cases ....................................................................................................................................................... 13 
Fund/SERV Use Cases ....................................................................................................................................13 
Use Case # 1: Non-Omnibus Account (Initial Purchase) ................................................................................14 
Use Case # 2: Non-Omnibus Account (Subsequent Transaction) .................................................................15 
Use Case # 3: Omnibus and Super Omnibus Account (Initial Purchase – Aggregated Order) ......................16 
Use Case # 4: Omnibus Account (Initial Purchase – Order is not aggregated) ..............................................16 
Use Case # 5 - Trust Networked Account (Initial Purchase) ...........................................................................18 
Use Case # 6 - Trust Networked Account (Subsequent Transaction – DCIO Plan Level) .............................19 
Networking (B50/B51) Use Cases ....................................................................................................................20 
Use Case # 1: Non-Omnibus Account (B50 Account Conversion – Sequence # 38) ....................................21 
Use Case # 2: Non-Omnibus Account (B51 Account Update) / No change to field attributes on Sequence #38
 .........................................................................................................................................................................22 
Use Case # 3: Non-Omnibus Account (B51 Account Update) / Update to attribute on Sequence # 38  ........22 
Use Case # 4: Non-Omnibus Account (B51 Account Update) / Attribute on Sequence # 38 no longer applies
 .........................................................................................................................................................................23 
Use Case # 5: Non-Omnibus Account (B51 Account Update) / Multiple attributes on Sequence. # 38, one of 
which no longer applies ...................................................................................................................................24 
 

---

## Page 4

New Account / Account Maintenance Transparency Enhancements – Best Practices 
Background 4 
1. BACKGROUND 
Introduction 
Funds require further transparency into advisory programs, platforms, distribution channels, retirement 
programs and servicing relationships of trust-networked accounts, [[intermediary]] accounts not held in omnibus, 
and in certain instances omnibus accounts where the information is not being provided through the 
Omni/SERV Activity and Position files. This information is necessary for [[intermediary]] oversight, fee 
reconciliation, and internal reporting. The process to obtain the information is a highly manual and fragmented 
process.  
The ICI [[Broker]]/Dealer Advisory Committee, in conjunction with the ICI New Account/Account Maintenance 
Working Group (Working Group), identified enhancements to the [[NSCC]] Fund/SERV
® and Networking services 
to allow intermediaries to provide Funds the necessary transparency in a streamlined, automated, and more 
timely manner.  These enhancements are consistent with how similar information is provided today for omnibus 
subaccounts through the Omni/SERV Activity and Position files.   
 
 
 

---

## Page 5

New Account / Account Maintenance Transparency Enhancements – Best Practices 
Summary of Enhancements 5 
2. SUMMARY OF ENHANCEMENTS 
 
Key Dates Summary of Changes 
Summary of Fund/SERV® 
enhancements, effective 
March 28, 2022. 
 
Important Notice a9045 
 
Addition of the following optional fields to the Fund/SERV 001, 003/025, 
004/005/006, and 401 records: 
 
• [[intermediary]] Program Indicator 1 
• [[intermediary]] Program Indicator 2 
• Servicing Group [[ID]] 
• Additional Relationship [[ID]] 1 
• Additional Relationship [[ID]] 2 
 
Summary of Networking 
enhancements, effective 
March 28, 2022. 
 
Important Notice a9045 
 
Addition of the following optional fields to the Account Conversion/Update 
(A/B/T50, A/B/T/F51), Sequence # 38 record: 
 
• [[intermediary]] Program Indicator 1 
• [[intermediary]] Program Indicator 2 
• Servicing Group [[ID]] 
• Additional Relationship [[ID]] 1 
• Additional Relationship [[ID]] 2 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 6

New Account / Account Maintenance Transparency Enhancements – Best Practices 
Field Names & Descriptions 6 
3. FIELD NAMES & DESCRIPTIONS  
Following are the field names and descriptions encompassed in the enhancement :   
Field Name Type Description 
[[intermediary]] Program 
Indicator – 1 
4 bytes 
A/N 
Optional 
Indicates the program, platform, or channel applicable to an account.  Examples 
may include: 
• Program indicator for advisory accounts 
• Distribution channel applicable to the account (e.g., retail, RIA, etc.)  
• Retirement platform pertaining to the account 
 
Values are uniquely defined by intermediaries. 
[[intermediary]] Program 
Indicator – 2 
4 bytes 
A/N 
Optional 
Further defines the program, platform, or channel applicable to an account. 
 
Values are uniquely defined by intermediaries. 
Servicing Group [[ID]] 9 bytes 
A/N 
Optional 
This field is used to communicate aggregated servicing relationships or define 
additional relationships on accounts.  Examples may include: 
• Consolidating (Super) Branches 
• Third-party administrators (TPAs) 
• Investment Advisers 
• Consultants 
 
This field does not replace the main branch field on the account. 
 
Values are uniquely defined by intermediaries. 
Additional Relationship 
[[ID]] – 1 
20 bytes 
A/N 
Optional 
 
This field is used to communicate additional relationship details to further define 
servicing relationships between accounts. 
 
Values are uniquely defined by intermediaries. 
Additional Relationship 
[[ID]] – 2 
20 bytes 
A/N 
Optional 
This field is used to communicate additional relationship details to further define 
servicing relationships between accounts. 
 
Values are uniquely defined by intermediaries. 
 
  
 

---

## Page 7

New Account / Account Maintenance Transparency Enhancements – Best Practices 
Implementation Considerations 7 
4. IMPLEMENTATION CONSIDERATIONS 
1. Values provided in the [[intermediary]] Program Indicator, Servicing Group [[ID]], and Additional Relationship [[ID]] 
fields are uniquely defined by each [[intermediary]] and communicated to the Funds directly outside of the 
[[NSCC]].  Prior to passing information in these fields, intermediaries should communicate with Funds to 
ensure they have the necessary values and descriptions that will be provided in these fields and that the 
Funds and their service providers are prepared to receive the values through Fund/SERV
® and 
Networking. 
2. The [[intermediary]] Program Indicator, Servicing Group [[ID]], and Additional Relationship [[ID]] fields are 
optional.  
[[NSCC]] will not edit against values provided in these fields as each value is uniquely defined by 
intermediaries - values provided in these fields and accepted by [[NSCC]] will be passed to the Fund.  Since 
these are optional fields, Funds should be prepared to receive records with these fields populated, blank, 
or a combination thereof.  Considerations should also be given to these fields being populated with 
spaces between characters. 
3. Intermediaries should strongly consider sending Networking B51 maintenance records to add the 
applicable [[intermediary]] Program Indicator, Servicing Group [[ID]], and Additional Relationship [[ID]] field values 
to existing accounts prior to passing any subsequent attribute updates. 
4. Account Establishment and Maintenance Updates – (Fund/SERV / Networking)  
Intermediaries can establish networked accounts on the books of the Fund through the [[NSCC]] by 
leveraging either of the following options: 
a. Fund/SERV 401 Full Registration record, which accompanies an initial purchase order  
b. Networking B50 Account Conversion record    
After the account is established, intermediaries provide account maintenance updates through the 
Networking B51 Update record.   Accordingly, after the account is established all account maintenance 
updates to the [[intermediary]] Program Indicator, Servicing Group [[ID]], and Additional Relationship [[ID]] fields 
should be submitted through the Networking B51 Update Record, Sequence # 38.   
Sequence # 38 of the B51 Update Record should only be provided by the [[intermediary]] when there 
are changes to an attribute.   When provided, Sequence # 38 should be populated with all current 
attribute values. 
5. Orders (Fund/SERV) 
The [[intermediary]] Program Indicator, Servicing Group [[ID]], and Additional Relationship [[ID]] fields can be 
provided on the trade (Fund/SERV 001, 003, 004 order records) and, as previously mentioned in #4 
above, through the Fund/SERV 401 Full Registration record at the time of an initial purchase.   
a. The Working Group agreed values provided on the Fund/SERV order records are attributes of the 
trade and should not overwrite values on the corresponding account record.  These values may 
be provided on an initial purchase and well as subsequent transactions, if applicable.    
b. The only instance a Fund/SERV 401 Full Registration record should be populated with values in the 
[[intermediary]] Program Indicator, Servicing Group [[ID]], and Additional Relationship [[ID]] fields is during 
the initial purchase, and only if the account was not previously established through the Networking 
B50 Account Conversion record.  If the account was previously established and a Fund/SERV 401 
record is submitted on an order with these fields populated, the Working Group agreed the values 
should be ignored. 
c. Values provided on the Fund/SERV order should be populated by Funds on the applicable confirm 
record (005, 006, 025). 
 
 

---

## Page 8

New Account / Account Maintenance Transparency Enhancements – Best Practices 
Fund/SERV & Networking– Best Practices 8 
5. FUND/SERV & NETWORKING– BEST PRACTICES  
This section provides Best Practices for populating the [[intermediary]] Program Indicator, Servicing Group [[ID]], 
and Additional Relationship [[ID]] fields in the Fund/SERV® and Networking records. 
Important Notes: 
• [[NSCC]] will not edit against values provided in these fields as each value is uniquely defined by 
intermediaries.  
• The Working Group agreed the [[intermediary]] Program Indicator, Servicing Group [[ID]], and Additional 
Relationship [[ID]] values provided on the Fund/SERV order are mutually exclusive of the values on the 
account record:  
o Values provided on the Fund/SERV Order (001, 003, 004) are attributes of the trade and should not 
overwrite values on the corresponding account record. 
o Values provided on the account record are attributes of the account and should not overwrite values 
on the corresponding Fund/SERV order.  
• After an account has been established, all account maintenance updates to the [[intermediary]] Program 
Indicator, Servicing Group [[ID]], and Additional Relationship [[ID]] values should be provided through the 
Networking Account Update (B51) record (see Networking Use Case #2).  If the account was previously 
established and a Fund/SERV 401 record is submitted on an order with these fields populated, the Working 
Group agreed the values should be ignored. 
 
Fund/SERV Order (001), Correction (003), As of Order (004), 
Registration (401), and Confirm (005,006,025) Records  
[[intermediary]] Program Indicator – 1 
Non-Omnibus Accounts Omnibus and Super Omnibus Accounts Trust Networked Accounts 
• Initial purchase  
should be populated on the 
respective order record 
(001, 003, 004), if 
applicable. 
should be populated on the Full 
Registration (401) record, if 
applicable, only if the 
account was not previously 
established through the 
Networking B50 Account 
Conversion Record. 
• Subsequent purchase 
should be populated on the 
respective order record 
(001, 003, 004), if 
applicable.   
If a Full Registration Record 
(401) is submitted with a 
subsequent purchase in lieu 
of a Short Registration 
(400), the 401 record 
should not be populated.  
The Working Group agreed 
in the event the 401 record 
is submitted and the 
• Should not be populated if trades are 
aggregated.  Program indicators on 
subaccounts should be provided through 
the Omni/SERV Activity and Position files 
(DSAPGI/DSPPGI fields, respectively).
 
 
• Should be populated for individual 
shareholder trades, if applicable, only if 
the information is not provided through 
the Omni/SERV files or alternative 
transparency solutions.  
 
For an individual shareholder trade, the 
Best Practices under the ‘Non-Omnibus 
Accounts’ section apply, with the 
exception of the 401 Full Registration, 
which should not be populated for any 
purchase order since this information 
should be provided through the 
Omni//SERV files or alternative 
transparency solutions. 
May be populated for plan level 
accounts, if applicable, when 
trades are not aggregated 
across underlying plans.    
Should not be populated if the 
information is provided through 
the Omni/SERV files or 
alternative transparency 
solutions. 
When populating the fields: 
• the Best Practices under the 
‘Non-Omnibus Accounts’ 
section should be followed. 
• the ‘Omnibus Account 
Indicator’ field on the 
Fund/SERV Order (001), As 
of Order (004), or Correction 
(003), should be populated 
with a value of ‘1’ (Omnibus 
Account) to signify the 
transaction applies to the 
omnibus account. 

---

## Page 9

New Account / Account Maintenance Transparency Enhancements – Best Practices 
Fund/SERV & Networking– Best Practices 9 
Non-Omnibus Accounts Omnibus and Super Omnibus Accounts Trust Networked Accounts 
attributes are populated, the 
values should be ignored. 
• Redemption 
should be populated on the 
respective order record 
(001, 003, 004), if 
applicable. 
• Confirmation 
If provided on the order, should 
be populated on the 
applicable confirm record 
(005, 006, 025). 
 
[[intermediary]] Program Indicator – 2 
Non-Omnibus Accounts Omnibus and Super Omnibus Accounts Trust Networked Accounts 
• Initial purchase  
should be populated on the 
respective order record 
(001, 003, 004), if 
applicable. 
should be populated on the Full 
Registration (401) record, if 
applicable, only if the 
account was not previously 
established through the 
Networking B50 Account 
Conversion Record. 
 
• Subsequent purchase 
should be populated on the 
respective order record 
(001, 003, 004), if 
applicable.   
If a Full Registration Record 
(401) is submitted with a 
subsequent purchase in lieu 
of a Short Registration 
(400), the 401 record 
should not be populated.  
The Working Group agreed 
in the event the 401 record 
is submitted and the 
attributes are populated, the 
values should be ignored. 
 
• Redemption 
should be populated on the 
respective order record 
(001, 003, 004), if 
applicable. 
 
• Confirmation: 
• Should not be populated if trades are 
aggregated.  Program indicators on 
subaccounts should be provided through 
the Omni/SERV Activity and Position files 
(DSAMAT/DSPMAT fields, respectively). 
 
• Should be populated for individual 
shareholder trades, if applicable, only if 
the information is not provided through the 
Omni/SERV files or alternative 
transparency solutions. 
 
For an individual shareholder trade, 
the Best Practices under the ‘Non-
Omnibus Accounts’ section apply, 
with the exception of the 401 Full 
Registration, which should not be 
populated for any purchase order 
since this information should be 
provided through the Omni//SERV 
files or alternative transparency 
solutions. 
May be populated for plan level 
accounts, if applicable, when 
trades are not aggregated 
across underlying plans.   
Should not be populated if the 
information is provided through 
the Omni/SERV files or 
alternative transparency 
solutions. 
 
When populating this field: 
• the Best Practices under the 
‘Non-Omnibus Accounts’ 
section should be followed. 
• the ‘Omnibus Account 
Indicator’ field on the 
Fund/SERV Order (001), As 
of Order (004), or Correction 
(003), should be populated 
with a value of ‘1’ (Omnibus 
Account) to signify the 
transaction applies to the 
omnibus account. 

---

## Page 10

New Account / Account Maintenance Transparency Enhancements – Best Practices 
Fund/SERV & Networking– Best Practices 10 
Non-Omnibus Accounts Omnibus and Super Omnibus Accounts Trust Networked Accounts 
If provided on the order, should 
be populated on the 
applicable confirm record 
(005, 006, 025). 
 
 
Servicing Group [[ID]] 
Non-Omnibus Accounts Omnibus and Super Omnibus 
Accounts 
Trust Networked Accounts 
• Initial purchase  
should be populated on the 
respective order record (001, 
003, 004), if applicable. 
should be populated on the Full 
Registration (401) record, if 
applicable, only if the account 
was not previously established 
through the Networking B50 
Account Conversion Record. 
 
• Subsequent purchase 
should be populated on the 
respective order record (001, 
003, 004), if applicable.   
If a Full Registration Record (401) 
is submitted with a subsequent 
purchase in lieu of a Short 
Registration (400), the 401 
record should not be 
populated.  The Working 
Group agreed in the event the 
401 record is submitted and 
the attributes are populated, 
the values should be ignored. 
 
• Redemption 
should be populated on the 
respective order record (001, 
003, 004), if applicable. 
 
Should not be populated if trades are 
aggregated.  Servicing Group IDs on 
subaccounts should be provided through 
the Omni/SERV Activity and Position files 
(BRNALT/DSPABR fields, respectively).  
 
Should be populated for individual 
shareholder trades, if applicable, only if 
the information is not provided through 
the Omni/SERV files or alternative 
transparency solutions. 
For an individual shareholder trade, the 
Best Practices under the ‘Non-Omnibus 
Accounts’ section apply, with the 
exception of the 401 Full Registration, 
which should not be populated for any 
purchase order since this information 
should be provided through the 
Omni//SERV files or alternative 
transparency solutions. 
May be populated for plan level 
accounts, if applicable, when 
trades are not aggregated across 
underlying plans.    
Should not be populated if the 
information is provided through 
the Omni/SERV files or alternative 
transparency solutions. 
 
When populating this field: 
• the Best Practices under the 
‘Non-Omnibus Accounts’ 
section should be followed. 
• the ‘Omnibus Account 
Indicator’ field on the 
Fund/SERV Order (001), As of 
Order (004), or Correction 
(003), should be populated 
with a value of ‘1’ (Omnibus 
Account) to signify the 
transaction applies to the 
omnibus account. 

---

## Page 11

New Account / Account Maintenance Transparency Enhancements – Best Practices 
Fund/SERV & Networking– Best Practices 11 
Non-Omnibus Accounts Omnibus and Super Omnibus 
Accounts 
Trust Networked Accounts 
• Confirmation: 
If provided on the order, should be 
populated on the applicable 
confirm record (005, 006, 025). 
 
 
Additional Relationship Indicator [[ID]] 1 and 2 
Non-Omnibus Accounts Omnibus and Super Omnibus 
Accounts 
Trust Networked Accounts 
• Initial purchase  
should be populated on the 
respective order record (001, 
003, 004), if applicable. 
should be populated on the Full 
Registration (401) record, if 
applicable, only if the account 
was not previously 
established through the 
Networking B50 Account 
Conversion Record. 
 
• Subsequent purchase 
should be populated on the 
respective order record (001, 
003, 004), if applicable.   
If a Full Registration Record (401) 
is submitted with a 
subsequent purchase in lieu 
of a Short Registration (400), 
the 401 record should not 
be populated.  The Working 
Group agreed in the event the 
401 record is submitted and 
the attributes are populated, 
the values should be ignored. 
 
• Redemption 
should be populated on the 
respective order record (001, 
003, 004), if applicable. 
 
• Confirmation: 
If provided on the order, should 
be populated on the 
applicable confirm record 
(005, 006, 025). 
• Should not be populated if trades are 
aggregated. Relationship information 
on subaccounts should be provided 
through the Omni/SERV Activity and 
Position files.  
 
• Should be populated for individual 
shareholder trades, if applicable, only 
if the information is not provided 
through the Omni/SERV files or 
alternative transparency solutions. 
 
For an individual shareholder 
trade, the Best Practices under 
the ‘Non-Omnibus Accounts’ 
section apply, with the exception 
of the 401 Full Registration, 
which should not be populated 
for any purchase order since 
this information should be 
provided through the Omni//SERV 
files or alternative transparency 
solutions. 
May be populated for plan level 
accounts, if applicable, when 
trades are not aggregated across 
underlying plans.    
Should not be populated if the 
information is provided through 
the Omni/SERV files or 
alternative transparency 
solutions. 
 
When populating this field: 
• the Best Practices under the 
‘Non-Omnibus Accounts’ 
section should be followed. 
• the ‘Omnibus Account 
Indicator’ field on the 
Fund/SERV Order (001), As 
of Order (004), or Correction 
(003), should be populated 
with a value of ‘1’ (Omnibus 
Account) to signify the 
transaction applies to the 
omnibus account. 
 

---

## Page 12

New Account / Account Maintenance Transparency Enhancements – Best Practices 
Fund/SERV & Networking– Best Practices 12 
Networking Account Conversion/Update (A/B/T50, A/B/T/51) Records 
Non-Omnibus Accounts Omnibus and Super Omnibus 
Accounts 
Trust Networked Accounts 
B50 – Sequence # 38 
Should be populated, if applicable   
 
B51 – Sequence # 38 
• Should only be provided by the 
[[intermediary]] when there are changes to an 
attribute.   When provided, Seq. # 38 should 
be populated with all current attribute values. 
 
When communicating changes, if an 
attribute no longer applies, the 
applicable attribute field should be 
populated with a ‘blank’ to signify the 
attribute no longer applies. 
 
Funds should be prepared to receive 
Seq. # 38 with the attribute fields 
populated, blank, or a combination 
thereof.  
 
• Should not be provided when there are no 
changes to the attributes. 
 
B50 and B51 – Sequence # 38 
Should not be populated. The 
information should be provided 
through the Omni/SERV Activity & 
Position files or alternative 
transparency solutions. 
 
 
B50 and B51 – Sequence # 38 
May be populated for plan level 
accounts, if applicable, when 
plan account information is not 
aggregated across underlying 
plans.  
Should not be populated if the 
information is provided through 
the Omni/SERV files or 
alternative transparency 
solutions. 
If populated, the Best Practices 
under the ‘Non-Omnibus 
Accounts’ section should be 
followed. 
 
 
 

---

## Page 13

New Account / Account Maintenance Transparency Enhancements – Best Practices 
Use Cases 13 
6. USE CASES  
This section provides use cases demonstrating Best Practices for populating the [[intermediary]] Program 
Indicator, Servicing Group [[ID]], and Additional Relationship [[ID]] fields.   
 
Fund/SERV Use Cases 
Following is a summary of Best Practices for populating the fields in Fund/SERV®: 
Non-Omnibus Accounts Omnibus and Super Omnibus 
Accounts 
Trust Networked Accounts 
• Initial purchase  
should be populated on the respective 
order record (001, 003, 004), if 
applicable. 
should be populated on the Full 
Registration (401) record, if 
applicable, only if the account was 
not previously established through 
the Networking B50 Account 
Conversion Record. 
 
• Subsequent purchase 
should be populated on the respective 
order record (001, 003, 004), if 
applicable. 
 
If a Full Registration Record (401) is 
submitted with a subsequent 
purchase in lieu of a Short 
Registration (400), the 401 record 
should not be populated.  The 
Working Group agreed in the event 
the 401 record is submitted and 
the attributes are populated, the 
values should be ignored. 
 
• Redemption 
should be populated on the respective 
order record (001, 003, 004), if 
applicable. 
 
• Confirmation: 
If provided on the order, should be 
populated on the applicable 
confirm record (005, 006, 025). 
• Should not be populated if 
trades are aggregated.  The 
information should be provided 
through the Omni/SERV 
Activity & Position files 
(Omni/SERV files). 
 
• Should be populated for 
individual shareholder trades, 
if applicable, only if the 
information is not provided 
through the Omni/SERV files 
or alternative transparency 
solutions. 
 
For an individual shareholder 
trade, the Best Practices under 
the ‘Non-Omnibus Accounts’ 
section apply, with the 
exception of the 401 Full 
Registration, which should 
not be populated for any 
purchase order since this 
information should be provided 
through the Omni//SERV files 
or alternative transparency 
solutions. 
May be populated for plan level 
accounts, if applicable, when 
trades are not aggregated across 
underlying plans.    
Should not be populated if the 
information is provided through 
the Omni/SERV files or 
alternative transparency 
solutions. 
 
When populating this field: 
• the Best Practices under the 
‘Non-Omnibus Accounts’ 
section should be followed. 
• the ‘Omnibus Account 
Indicator’ field on the 
Fund/SERV Order (001), As 
of Order (004), or Correction 
(003), should be populated 
with a value of ‘1’ (Omnibus 
Account) to signify the 
transaction applies to the 
omnibus account. 
Important Notes 
• In the Use Cases that follow, there are instances where not all the [[intermediary]] Program Indicator, 
Servicing Group [[ID]], and Additional Relationship [[ID]] attributes apply.  In a scenario where multiple attributes 
apply; all applicable fields should be populated.  
• Best Practices for populating a Correction (003) and As of Order (004) follow the same guidelines depicted 
in the Use Cases for an Order (001). 

---

## Page 14

New Account / Account Maintenance Transparency Enhancements – Best Practices 
Use Cases 14 
• Values provided on the Fund/SERV order should be populated by Funds on the applicable confirm record 
(005, 006, 025). 
• The Working Group agreed the attributes provided on the Fund/SERV order should not overwrite values on 
the account record. 
 
 
Fund/SERV Use Cases 
Use Case 1 - Non-Omnibus Account (Initial Purchase) 
Use Case 2 - Non-Omnibus Account (Subsequent Transaction) 
Use Case 3 - Omnibus and Super Omnibus Account (Initial Purchase – Aggregated Order) 
Use Case 4 - Omnibus Account (Initial Purchase – Order is not aggregated) 
Use Case 5 - Trust Networked Account (Initial Purchase) 
Use Case 6 - Trust Networked Account (Subsequent Transaction- DCIO Plan Level) 
 
Use Case # 1: Non-Omnibus Account (Initial Purchase) 
• [[intermediary]] ‘ABC’ and Fund ‘XWY’ are in a networking level 3 arrangement.    
• [[intermediary]] ABC submits an Order (001) for an initial purchase, along with a Full Registration (401) 
record. 
• The trade and account are part of [[intermediary]] ABC’s ‘Retail Brokerage’ program. 
• [[intermediary]] ABC previously provided Fund XWY a description of all values that would be passed in the 
[[intermediary]] Program Indicator fields, with RETB indicating ‘Retail Brokerage’.  
• The account was not previously established via the Networking B50 Account Conversion record.  
 
 
Best Practice:  
RETB should be populated in the [[intermediary]] Program Indicator – 1 field on both the Order (001) and Full 
Registration (401) records.   
 
Important Reminder: 
If the account was previously established via the Networking B50 Account Conversion record, the values 
should not be populated in the Full Registration (401) record.  If the account was previously established and a 
Fund/SERV 401 record is submitted with these fields populated, the Working Group agreed the values should 
be ignored. 
 
 

---

## Page 15

New Account / Account Maintenance Transparency Enhancements – Best Practices 
Use Cases 15 
Order (001) and Full Registration (401) Records   
Field Name Value 
[[intermediary]] Program Indicator – 1 RETB 
[[intermediary]] Program Indicator – 2 blank 
Servicing Group [[ID]] blank 
Additional Relationship [[ID]] – 1 blank 
Additional Relationship [[ID]] – 2 blank 
 
Use Case # 2: Non-Omnibus Account (Subsequent Transaction) 
• [[intermediary]] ‘ABC’ and Fund ‘XWY’ are in a networking level 3 arrangement.    
• [[intermediary]] ABC submits an Order (001) for a subsequent transaction (e.g., purchase or redemption)  
• The trade applies to [[intermediary]] ABC’s ‘Retail Brokerage’ program. 
• [[intermediary]] ABC previously provided Fund XWY a description of all values that would be passed in the 
[[intermediary]] Program Indicator fields, with RETB indicating ‘Retail Brokerage’.  
 
 
Best Practice:  
RETB should be populated in the [[intermediary]] Program Indicator – 1 field on the Order (001) to indicate the 
trade applies to the program. 
 
Important Reminders: 
In instances where a Full Registration (401) record is submitted with a subsequent purchase in lieu of a Short 
Registration (400) record, the 401 record should not be populated with attribute values since the account 
has already been established.  The Working Group agreed in the event the 401 record is submitted and the 
attributes are populated, the values should be ignored. 
 
Order (001) Record   
Field Name Value 
[[intermediary]] Program Indicator – 1 RETB 
[[intermediary]] Program Indicator – 2 blank 
Servicing Group [[ID]] blank 
Additional Relationship [[ID]] – 1 blank 

---

## Page 16

New Account / Account Maintenance Transparency Enhancements – Best Practices 
Use Cases 16 
Field Name Value 
Additional Relationship [[ID]] – 2 blank 
 
Use Case # 3: Omnibus and Super Omnibus Account (Initial Purchase – 
Aggregated Order) 
• [[intermediary]] ‘ABC’ and Fund ‘XWY’ are in an omnibus arrangement.    
• The trade and account are part of [[intermediary]] ABC’s ‘Retail Brokerage’ program. 
• [[intermediary]] ABC provides the information through the Omni/SERV files 
• [[intermediary]] ABC submits an aggregated Order (001) for an initial purchase, along with a Full Registration 
(401) record. 
• [[intermediary]] ABC previously provided Fund XWY a description of all values that would be passed in the 
[[intermediary]] Program Indicator fields, with RETB indicating ‘Retail Brokerage’.  
 
Best Practice:  
RETB should not be populated in the [[intermediary]] Program Indicator – 1 field on Order (001) or Full 
Registration (401) since this is an aggregated omnibus account order.  The information should be provided 
through the Omni/SERV files or alternate transparency solutions. 
 
This Best Practice also applies to subsequent transactions (e.g., purchases and redemptions). The attributes 
should not be populated for an aggregated omnibus account order – all activity should be provided 
through the Omni/SERV files or alternate transparency solutions.  
Order (001) and Full Registration (401) Records   
Field Name Value 
[[intermediary]] Program Indicator – 1 blank 
[[intermediary]] Program Indicator – 2 blank 
Servicing Group [[ID]] blank 
Additional Relationship [[ID]] – 1 blank 
Additional Relationship [[ID]] – 2 blank 
 
Use Case # 4: Omnibus Account (Initial Purchase – Order is not aggregated) 
• [[intermediary]] ‘ABC’ and Fund ‘XWY’ are in an omnibus arrangement.  Although operating in an omnibus 
environment, [[intermediary]] ABC may not aggregate all orders.  
• [[intermediary]] ABC does not aggregate the order and submits an initial purchase Order (001) reflecting an 
individual shareholder sub-account, along with a Full Registration (401) record. 

---

## Page 17

New Account / Account Maintenance Transparency Enhancements – Best Practices 
Use Cases 17 
• The trade and account are part of [[intermediary]] ABC’s ‘Retail Brokerage’ program. 
• [[intermediary]] ABC previously provided Fund XWY a description of all values that would be passed in the 
[[intermediary]] Program Indicator fields, with RETB indicating ‘Retail Brokerage’.  
• [[intermediary]] ABC does not provide the order information through the Omni/SERV files or alternative 
transparency solutions. 
 
Best Practice:  
• RETB should be populated in the [[intermediary]] Program Indicator – 1 field on the Order (001). 
• RETB should not be populated in the Full Registration (401) record, since this is an omnibus account,  and 
any account maintenance updates should be provided through the Omni/SERV files or alternate 
transparency solutions. 
 
 
This Best Practice also applies for subsequent transactions (e.g., purchases and redemptions).    
Important Reminder: 
If the attribute values are being provided through the Omni/SERV files or alternate transparency solutions, they 
should not be populated on the Order (001) or Full Registration (401) records.  
 
 
Order (001)  
Field Name Value 
[[intermediary]] Program Indicator – 1 RETB 
[[intermediary]] Program Indicator – 2 blank 
Servicing Group [[ID]] blank 
Additional Relationship [[ID]] – 1 blank 
Additional Relationship [[ID]] – 2 blank 
 
 
Full Registration (401) Records   
Field Name Value 
[[intermediary]] Program Indicator – 1 blank 
[[intermediary]] Program Indicator – 2 blank 
Servicing Group [[ID]] blank 
Additional Relationship [[ID]] – 1 blank 
Additional Relationship [[ID]] – 2 blank 

---

## Page 18

New Account / Account Maintenance Transparency Enhancements – Best Practices 
Use Cases 18 
 
 
Use Case # 5 - Trust Networked Account (Initial Purchase) 
• [[intermediary]] ‘ABC’ is the Trust on the account and submits a plan level Order (001) for an initial purchase, 
along with a Full Registration (401) record. 
• [[intermediary]] ABC does not disclose the underlying dealer and advisor on the account, instead listing their 
[[default]] dealer. 
• The underlying dealer and advisor on the account are - ‘Your Plan Advisors’ and ‘Rep. [[ID]] 007/John Doe’, 
respectively. 
• [[intermediary]] ABC does not provide the information through the Omni/SERV files or alternative 
transparency solutions. 
• The account was not previously established via the Networking B50 Account Conversion record.  
• The initial purchase is specific to a particular plan (not aggregated across plans).  
 
 
Best Practice:  
• “Your Plan Advisors’ and ‘Rep. [[ID]] 007/John Doe’ should be populated in the Additional Relationship [[ID]] 
fields on the Order (001) record to communicate the underlying investment advisor information.  This Best 
Practice also applies for subsequent transactions (e.g., purchases and redemptions).  
• “Your Plan Advisors’ and ‘Rep. [[ID]] 007/John Doe’ should be populated in the Additional Relationship [[ID]]  
fields on the Full Registration (401) record to communicate the underlying investment advisor information. 
• The ‘Omnibus Account Indicator’ field should be populated with a value of ‘1’ (Omnibus Account) to signify 
the transaction applies to the omnibus account. 
 
 
Important Reminders: 
 
• If the account was previously established via the Networking B50 Account Conversion record, the  values 
should not be populated in the Full Registration (401) record.  If the account was previously established and 
a Fund/SERV 401 record is submitted with these fields populated, the Working Group agreed the values 
should be ignored. 
• If the attribute values are being provided through the Omni/SERV files or alternate transparency solutions, 
they should not be populated on the Order (001) or Full Registration (401) records. 
 
 
 

---

## Page 19

New Account / Account Maintenance Transparency Enhancements – Best Practices 
Use Cases 19 
Order (001) and Full Registration (401) Records   
Field Name Value 
[[intermediary]] Program Indicator – 1 blank 
[[intermediary]] Program Indicator – 2 blank 
Servicing Group [[ID]] blank 
Additional Relationship [[ID]] – 1 Your Plan Advisors 
Additional Relationship [[ID]] – 2 007/John Doe 
Omnibus Account Indicator 1 (Omnibus Account) 
 
Use Case # 6 - Trust Networked Account (Subsequent Transaction – DCIO 
Plan Level) 
• [[intermediary]] ‘ABC’ is the Trust on the account and submits a plan level Order (001) for a subsequent 
transaction (e.g., purchase or redemption). 
• The trade applies to [[intermediary]] ABC’s ‘Advisory – Variable Annuity’ program. 
• [[intermediary]] ABC previously provided Fund XWY a description of all values that would be passed in the 
[[intermediary]] Program Indicator fields, with AVA indicating ‘Advisory – Variable Annuity’.  
• [[intermediary]] ABC does not provide the information through the Omni/SERV files or alternative 
transparency solutions. 
• The subsequent transaction is specific to a particular plan (not aggregated across plans).  
 
Best Practice:  
• ‘AVA’ should be populated in the [[intermediary]] Program Indicator – 1 field on the Order (001). 
• The ‘Omnibus Account Indicator’ field should be populated with a value of ‘1’ (Omnibus Account) to signify 
the transaction applies to the omnibus account. 
 
Important Reminders: 
• If the attribute values are being provided through the Omni/SERV files or alternate transparency solutions, 
they should not be populated on the Order (001).   
• In instances where a Full Registration (401) record is submitted with a subsequent purchase in lieu of a 
Short Registration (400) record, the 401 record should not be populated with attribute values since the 
account has already been established and all account maintenance updates should be provided through the 
Networking B51 Account Update record.  If the account was previously established and a Fund/SERV 401 
record is submitted, the Working Group agreed the values should be ignored. 
 
 
 
 

---

## Page 20

New Account / Account Maintenance Transparency Enhancements – Best Practices 
Use Cases 20 
Order (001) Record   
Field Name Value 
[[intermediary]] Program Indicator – 1 AVA 
[[intermediary]] Program Indicator – 2 blank 
Servicing Group [[ID]] blank 
Additional Relationship [[ID]] – 1 blank 
Additional Relationship [[ID]] – 2 blank 
Omnibus Account Indicator 1 (Omnibus Account) 
 
Networking (B50/B51) Use Cases 
Following is a summary of Best Practices for populating the Networking B50/51 fields: 
Non-Omnibus Accounts Omnibus Accounts and Super 
Omnibus 
Trust Networked Accounts 
B50 – Sequence # 38 
Should be populated, if applicable   
 
B51 – Sequence # 38 
• Should only be provided by the 
[[intermediary]] when there are changes 
to an attribute.   When provided, Seq. 
# 38 should be populated with all 
current attribute values. 
 
When communicating changes, if 
an attribute no longer applies, the 
applicable attribute field should be 
populated with a ‘blank’ to signify 
the attribute no longer applies. 
 
Funds should be prepared to 
receive Seq. # 38 with the attribute 
fields populated, blank, or a 
combination thereof.  
 
• Should not be provided when there 
are no changes to the attributes. 
 
B50 and B51 – Sequence # 38 
Should not be populated. The 
information should be provided 
through the Omni/SERV Activity & 
Position files or alternative 
transparency solutions. 
 
 
B50 and B51 – Sequence # 38 
May be populated for plan level 
accounts, if applicable, when 
plan account information is not 
aggregated across underlying 
plans.  
 
Should not be populated if the 
information is provided through 
the Omni/SERV files or 
alternative transparency 
solutions. 
 
If populated, the Best Practices 
under the ‘Non-Omnibus 
Accounts’ section should be 
followed. 
 
 
 

---

## Page 21

New Account / Account Maintenance Transparency Enhancements – Best Practices 
Use Cases 21 
Important Notes: 
• In the Use Cases that follow, there are instances where not all the [[intermediary]] Program Indicator, 
Servicing Group [[ID]], and Additional Relationship [[ID]] attributes apply.  In a scenario where multiple attributes 
apply, all applicable fields should be populated.  
• When the B51 Update Sequence # 38 record is provided to communicate account attribute updates, it is 
important the following Best Practices are adhered to:  
 
o The B51 Update record should only be provided by the [[intermediary]] when there are changes to an 
attribute.   When provided, Seq. # 38 should be populated with all current attribute values.  
o A previously communicated attribute that no longer applies should be populated with a ‘blank’ to 
indicate the attribute no longer applies. 
 
 
Networking Use Cases 
Use Case 1 - Non-Omnibus Account (B50 Account Conversion)  
Use Case 2 - Non-Omnibus Account (B51 Account Update) / No change to attributes on Seq. # 38 
Use Case 3 - Non-Omnibus Account (B51 Account Update) / Update to attribute on Seq. # 38 
Use Case 4 - Non-Omnibus Account (B51 Account Update) / Attribute on Seq. # 38 no longer applies 
Use Case 5 - Non-Omnibus Account (B51 Account Update) / Multiple attributes on Seq. # 38, one of 
which no   longer applies  
 
Use Case # 1: Non-Omnibus Account (B50 Account Conversion – Sequence # 
38) 
• [[intermediary]] ‘ABC’ and Fund ‘XWY’ are in a networking level 3 arrangement.    
• [[intermediary]] ABC submits a Networking B50 Account Conversion to establish the account . 
• The account is part of [[intermediary]] ABC’s ‘Retail Brokerage’ program. 
• [[intermediary]] ABC previously provided Fund XWY a description of all values that would be passed in the 
[[intermediary]] Program Indicator fields, with RETB indicating ‘Retail Brokerage’.  
 
Best Practice:  
RETB should be populated in the [[intermediary]] Program Indicator – 1 field on Seq. # 38 of the Account 
Conversion/Update (B50) record.   
 
 

---

## Page 22

New Account / Account Maintenance Transparency Enhancements – Best Practices 
Use Cases 22 
Account Conversion (B50) Record, Seq. # 38 
Field Name Value 
[[intermediary]] Program Indicator – 1 RETB 
[[intermediary]] Program Indicator – 2 blank 
Servicing Group [[ID]] blank 
Additional Relationship [[ID]] – 1 blank 
Additional Relationship [[ID]] – 2 blank 
 
Use Case # 2: Non-Omnibus Account (B51 Account Update) / No change to 
field attributes on Sequence #38 
• [[intermediary]] ‘ABC’ and Fund ‘XWY’ are in a networking level 3 arrangement.    
• [[intermediary]] ABC submits a Networking B51 to update the ‘[[Dividend]] Code’ (located on Seq. # 1) on 
the account. 
• [[intermediary]] ABC previously passed a B50 record with RETB populated in the [[intermediary]] Program 
Indicator – 1 field, which is the only existing attribute on the account. 
• The account is still part of [[intermediary]] ABC’s ‘Retail Brokerage’ (RETB) program and there is no 
change to the other field attributes ([[intermediary]] Program Indicator - 2, Servicing Group [[ID]], Additional 
Relationship [[ID]] 1 and 2) in Sequence #38. 
 
 
Best Practice:  
Sequence #38 should not be submitted with the B51 since there are no changes to the [[intermediary]] 
Program Indicator 1 and 2, Servicing Group [[ID]], Additional Relationship [[ID]] 1 and 2 values.  
 
Use Case # 3: Non-Omnibus Account (B51 Account Update) / Update to 
attribute on Sequence # 38 
• [[intermediary]] ‘ABC’ and Fund ‘XWY’ are in a networking level 3 arrangement.    
• [[intermediary]] ABC submits a Networking B51 to add Servicing Group [[ID]] ‘1234’ on the account.   
• [[intermediary]] ABC previously passed a B50 record with RETB populated in the [[intermediary]] Program 
Indicator – 1 field.  
• The account is still part of [[intermediary]] ABC’s ‘Retail Brokerage’ (RETB) program. 
 
 

---

## Page 23

New Account / Account Maintenance Transparency Enhancements – Best Practices 
Use Cases 23 
Best Practice:  
• ‘1234’ should be populated in the Servicing Group [[ID]] field on Seq. # 38 of the Account Update (B51) 
record. 
• RETB should also be populated in the [[intermediary]] Program Indicator – 1 field on Seq. # 38 of the Account 
Update (B51) record to indicate RETB still applies to the account 
 
 
 
Account Update (B51) Record, Sequence # 38   
Field Name Value 
[[intermediary]] Program Indicator – 1 RETB 
[[intermediary]] Program Indicator – 2 blank 
Servicing Group [[ID]] 1234 
Additional Relationship [[ID]] – 1 blank 
Additional Relationship [[ID]] – 2 blank 
 
Important Reminder: 
When the B51 Sequence #38 is provided, all current attribute values should be populated to indicate the 
attribute still applies to the account. 
 
Use Case # 4: Non-Omnibus Account (B51 Account Update) / Attribute on 
Sequence # 38 no longer applies 
• [[intermediary]] ‘ABC’ and Fund ‘XWY’ are in a networking level 3 arrangement.    
• [[intermediary]] ABC previously passed a B50 record with RETB populated in the [[intermediary]] Program 
Indicator – 1 field.  
• The account is no longer part of [[intermediary]] ABC’s ‘Retail Brokerage’ (RETB) program. 
• There are no other attributes associated with the account. 
 
Best Practice:    
A ‘blank’ value should be passed in the [[intermediary]] Program Indicator – 1 field on Seq. # 38 of the Account 
Update (B51) record to indicate the attribute no longer applies.   
 
Account Update (B51) Record, Sequence # 38   
Field Name Value 
[[intermediary]] Program Indicator – 1 blank 

---

## Page 24

New Account / Account Maintenance Transparency Enhancements – Best Practices 
Use Cases 24 
Field Name Value 
[[intermediary]] Program Indicator – 2 blank 
Servicing Group [[ID]] blank 
Additional Relationship [[ID]] – 1 blank 
Additional Relationship [[ID]] – 2 blank 
 
Use Case # 5: Non-Omnibus Account (B51 Account Update) / Multiple 
attributes on Sequence. # 38, one of which no longer applies 
• [[intermediary]] ‘ABC’ and Fund ‘XWY’ are in a networking level 3 arrangement.    
• [[intermediary]] ABC previously passed a B50 record with RETB populated in the [[intermediary]] Program 
Indicator – 1 field and ‘1234’ populated in the Servicing Group [[ID]] field. 
• The account is no longer part of [[intermediary]] ABC’s ‘Retail Brokerage’ (RETB) program. 
• The account is still part of ABC’s ‘1234’ Servicing Group. 
 
Best Practice: 
• A ‘blank’ value should be passed in the [[intermediary]] Program Indicator – 1 field on Seq. # 38 of the 
Account Update (B51) record to indicate the RETB attribute no longer applies.   
• ‘1234 should be populated in the Servicing Group [[ID]] field on Sequence # 38 of the Account Update (B51)  
record to indicate ‘1234’ still applies to the account. 
 
 
 
Account Update (B51) Record, Sequence # 38   
Field Name Value 
[[intermediary]] Program Indicator – 1 blank 
[[intermediary]] Program Indicator – 2 blank 
Servicing Group [[ID]] 1234 
Additional Relationship [[ID]] – 1 blank 
Additional Relationship [[ID]] – 2 blank 
 
 
 

---

## Page 25

 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation [[DTCC]].  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: November 27, 2023 
Publication Code: MFS338 
Service: Fund/SERV® & Networking 
Title: New Account / Account Maintenance Transparency Enhancements – Best Practices  
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 