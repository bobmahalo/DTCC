---
title: "sdr_reject_code_reference_guide.pdf"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/sdr_reject_code_reference_guide.pdf"
pages: 21
size: "110.4 KB"
category: "Rules"
ingested_on: "2026-06-05"
---

# sdr_reject_code_reference_guide.pdf

**Original File:** [sdr_reject_code_reference_guide.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/sdr_reject_code_reference_guide.pdf)  
**Category:** Rules  
**Total Pages:** 21  
**File Size:** 110.4 KB  

---

## Page 1

Standardized Data Reporting (SDR) Reject Codes
SDR Reject Codes Quick Reference Guide
(Effective 04/23/2012)
                                                                                                                                                                                                                                                                                                                      
Format Keys-
Bold indicates Best Practices comments
Underline indicates specific sections of the Best Practices and Technical Overview to see for further information.
Italics  notes revisions and changes
Overview of Field Editing Rules-
(note-this section is excerpted from the Best Practices- Working Assumptions, Field Validation)
The Optional/Required Field indicates whether a field must be coded (Required), can be bypassed (Optional) or is dependent on conditions (OC or RC).  [[NSCC]] validates data supplied and 
the format is correct (when applicable) before sending through to the receiving party.  Below are the different coding options & [[obligations]]:
R = Required 
This field must be completed.  [[NSCC]] will validate the following criteria.  If coding is not completed properly the record will be rejected. 
• Information is accurate.  (i.e., a Firm Number must be valid & eligible [[NSCC]]#)  
• Correct Format must be followed (if specified).
• If options are offered in the Description field, [[NSCC]] will check that a legitimate value was used. 
O = Optional  
This field does not have to be completed.  However, if the field is utilized [[NSCC]] will check the following criteria are met.  If not, the record will be rejected.
• Correct Format must be followed (if specified).
• Information is accurate.
• If options are offered in the Description field, [[NSCC]] will check that a legitimate value was used. 
RC = Required/Conditional 
This indicates the field is generally required, but can be optional upon specific conditions.  If conditions exist, this field may be bypassed.  The Record Layouts will state what the conditions 
are.  [[NSCC]] will check the following criteria.  If coding is not completed properly the record will be rejected. 
• Correct Format must be followed (if specified).
• Information is accurate.
• If options are offered in the Description field, [[NSCC]] will check that a legitimate value was used. 
OC = Optional/Conditional  
This indicates the field is generally optional, but required upon specific conditions.  If conditions exist, these fields must be utilized.  The Record Layouts will state what the conditions are.  
[[NSCC]] will check the following criteria.  If coding is not completed properly the record will be rejected. 
• Correct Format must be followed (if specified).
• Information is accurate.
• If options are offered in the Description field, [[NSCC]] will check that a legitimate [[Option]] was used. 
1 of 21

---

## Page 2

Standardized Data Reporting (SDR) Reject Codes
Reject Code Text Description
Optional/
Required
[[NSCC]] 
or 
Firm
Format 
or 
Data
SDR 
Layouts
Field 
Location Comments/Best Practices
SDR 
Reject 
Code
This reject code is applied when 
the:
01
Originator Type Missing or 
Invalid
The Originator Type on the SDR 
records is missing or invalid. R [[NSCC]] Both
All SDR 
request 
forms 1-1
Required by [[NSCC]]. This denotes the originator of 
the records--Fund, Firm, Underlying Firm, or 
[[NSCC]].
02
Record Type Missing or 
Invalid
The Record Type of an SDR record 
is missing or invalid. R [[NSCC]] Both
All fund and 
firm SDR 
records 2-3
Required by [[NSCC]]. This indicates the type of each 
record in the set-Request, Acknowledgement, 
Detail, Summary, Trailer, etc.  Each record type 
has a required value--see the record layouts.
03
Sequence Number Missing or 
Invalid
The Sequence Number on an SDR 
record is incorrect or invalid. R [[NSCC]] Both
All fund and 
firm SDR 
records 4-5
Required by [[NSCC]]. Denotes the sequence of 
records in the set, particularly with Detail and 
Summary records, which have optional record 2's 
that can be provided in addition to record 1.  See 
the record layouts.
04
SDR Control Number Missing 
or Invalid
The SDR Control Number is 
missing or invalid on the SDR 
records. R [[NSCC]] Format
F20 
B/U21
B/U27
N28
6-20
6-20
6-20
6-20
Required by [[NSCC]].  Can indicate improper format 
of the number, or that the SDR # in the header and 
trailer of a set [[DO]] not match each other.
05
SDR Request Type Missing or 
Invalid
The SDR Request Type is missing 
or invalid on the SDR request. R [[NSCC]] Format F20 99-100
Required by [[NSCC]]. Indicates the specific type of 
SDR request being made--e.g. Fund Account level, 
Plan level, Stop Recurring, etc.  See Field 
Definitions in the Technical Overview.
06
Firm Number Missing or 
Invalid
The listed [[Broker]]/Dealer [[NSCC]] 
[[participant]] Number is missing or 
invalid on the SDR request or 
response. R [[NSCC]] Data
F20
B/U21
B/U27
21-24
21-24
21-24
Firm must be an [[NSCC]] [[participant]], and records 
must reference a valid [[NSCC]] Firm #.  Also can 
denote that the Firm # referenced in the header 
and trailer of a set [[DO]] not match. Note--the 
participating firm list is on the [[DTCC]] website, under 
Services List by Firm.
2 of 21

---

## Page 3

Standardized Data Reporting (SDR) Reject Codes
Reject Code Text Description
Optional/
Required
[[NSCC]] 
or 
Firm
Format 
or 
Data
SDR 
Layouts
Field 
Location Comments/Best Practices
SDR 
Reject 
Code
07
Underlying Firm Number 
Missing or Invalid
The Underlying Firm Number on the 
SDR request or response is missing 
or invalid. OC Either Data
F20 
B/U21 
B/U25
B/U27
38-41
38-41
115-118
38-41
Required when the Underlying Firm Indicator is 
provided; must be a valid [[NSCC]] number. (the full 
list is available on the [[DTCC]] website, Wealth 
Management Services section, under Standardized 
Underlying Firm Symbol.
08
Underlying Firm Indicator 
Missing or Invalid
The Underlying Firm Indicator on 
the SDR request or response is 
missing or invalid. OC Either Data
F20
B/U21
B/U25
42-43
42-43
119-120
Required when providing Underlying Firm Number.  
Used to denote [[NSCC]] Number, [[OTC]] Symbol, or 
Underlying Firm Symbol.
09
Fund Number Missing or 
Invalid
The fund's [[NSCC]] [[participant]] 
Number on an SDR request or 
response is missing or invalid. R Either Data
F20
B/U21
B/U27
N28
25-28
25-28
25-28
25-28
Required by the [[NSCC]].  Full list is on the [[DTCC]] 
website, under Services List by Fund.
10
Fund Account Number 
Missing or Invalid
The Fund Account Number on the 
SDR request or response is missing 
or invalid. OC Either Data
F20
B/U21
44-63
44-63
This is the omnibus account number on the books 
of the Fund.
Required if Firm Account Number is not provided. 
(One or the other must be provided.)
Best Practice Clarification--Fund and Firm 
should clarify together if leading zeros in this 
number are required/accepted in requests, as 
different systems have different edits.
They should also clarify whether this or the 
Firm Account Number should be used in 
requests.
3 of 21

---

## Page 4

Standardized Data Reporting (SDR) Reject Codes
Reject Code Text Description
Optional/
Required
[[NSCC]] 
or 
Firm
Format 
or 
Data
SDR 
Layouts
Field 
Location Comments/Best Practices
SDR 
Reject 
Code
11
Firm Account Number Missing 
or Invalid
The Firm Account Number on the 
SDR request or response is missing 
or invalid. OC Either Data
F20
B/U21
64-83
64-83
This is the omnibus account number on the books 
of the Firm, which may not be the same number as 
the Fund Account Number on the Fund side.
Required if Fund Account Number is not provided.  
(One or the other must be provided.)
Best Practices Clarification--Fund and Firm 
should clarify together if this or Fund Account 
Number should be used, and if leading zeros 
are accepted or required, since different 
systems have different edits.
12 From Date Missing or Invalid
The "From" Date on the SDR 
request is missing or invalid. R [[NSCC]] Format F20 101-108
Required by [[NSCC]]. Specifies the start date of 
requested data.  See record layouts for valid date 
format.  Note--this cannot be a future date--only 
current day or historical. See Date Range 
Requests in the Best Practices.
13
Security Issue [[ID]] Missing or 
Invalid
The fund's Security Issue [[ID]] on an 
SDR request or response is missing 
or invalid. R Either Data
F20
B/U21
B/U27
29-37
29-37
29-37
Required by [[NSCC]]. This is the [[CUSIP]] number.  
The [[NSCC]] validates it by a calculation on the last 
digit.
14
Plan [[ID]]/[[investor]] Omnibus 
Account Number Missing or 
Invalid
The referenced Plan [[ID]]/[[investor]] 
Omnibus Account Number on an 
SDR request or response is missing 
or invalid.
O/C
O
R Either Data
F20
B/U24
B/U25
6-25
6-25
6-25
The Plan [[ID]]/[[investor]] Omnibus [[ID]] is used in Super 
Omnibus processing, both in indicating there are 
omnibus accounts within master omnibus accounts, 
and in sending subsequent SDR requests to 
specific plan or [[investor]] omnibus accounts.
4 of 21

---

## Page 5

Standardized Data Reporting (SDR) Reject Codes
Reject Code Text Description
Optional/
Required
[[NSCC]] 
or 
Firm
Format 
or 
Data
SDR 
Layouts
Field 
Location Comments/Best Practices
SDR 
Reject 
Code
15
Omnibus Account Indicator 
Missing or Invalid
The Omnibus Account Indicator on 
an SDR request or response is 
missing or invalid.
O/C
O/C
R [[NSCC]] Data
F20
B/U24
B/U25
26-26
26-26
26-26
Used to indicate the type of omnibus account--
either plan omnibus or [[investor]] omnibus--either in 
specific omnibus-level SDR requests, summary 
records for omnibus responses, or detail records 
showing what omnibus account is associated with 
an individual SSN of an underlying [[investor]].  This 
indicator must always accompany any request or 
response where the plan [[ID]]/[[investor]] omnibus 
account number field is populated.
16 SSN/TIN Missing or Invalid
The Social Security Number or Tax 
Identification Number on an SDR 
request or response is missing or 
invalid.
O
R Either Either
F20
B/U24
109-117
27-35
SSN/TIN is always required on Detail (B/U24) 
record responses.  It is optional on SDR requests.
17 Recurring Indicator Invalid
The Recurring Indicator on the SDR 
request is invalid. O [[NSCC]] Data F20 27-27
The Recurring Indicator on the SDR Request is 
used to indicate if the SDR request is for a 
recurring (ongoing) duration.  See the F20 record 
layout.
18 To Date Invalid
The "To" Date on the SDR request 
is invalid.  O [[NSCC]] Format F20 02 28-35
Optionally used on a Request, to specify the end 
date of a historical date range request for data.  
Note that date range requests should be limited 
to 90 days or less, and within the last year.  
Future dated requests are not allowed.  See the 
F20 record layout, and Date Range Requests in 
the Best Practices.
19
Includes Category 2 
Transactions Field Invalid
The Include Category 2 Transaction 
field on the SDR request is invalid. O [[NSCC]] Data F20 02 36-36
Indicates if the fund also wants applicable Category 
2 data to be included in the firm's response.  
Category 1 data only is assumed as the [[default]], 
unless this indicator is marked Yes.  See the F20 
02 record layout, and also the Best Practices, 
Category 1 and Category 2 Transactions.
5 of 21

---

## Page 6

Standardized Data Reporting (SDR) Reject Codes
Reject Code Text Description
Optional/
Required
[[NSCC]] 
or 
Firm
Format 
or 
Data
SDR 
Layouts
Field 
Location Comments/Best Practices
SDR 
Reject 
Code
20 RR Number Missing or Invalid
The Registered Representative 
Number on the SDR request is 
missing or invalid.
OC
O Either Data
F20 02
B/U24 02
37-45
21-29
Optionally used on both SDR requests and 
responses, (unless the SDR Request Type is 05, 
and then it is required on the request) and indicates 
the representative associated with the trade(s). 
Required if using SDR request type 05 (Rep Level 
SDR Request).
21 RR Branch Missing or Invalid
The Registered Representative 
Branch listed on the SDR request is 
missing or invalid. O (Both) Firm Data
F20 02
B/U24 02
46-54
30-38
Optionally used on both SDR requests and 
responses, and indicates the branch office 
associated with the registered representative of the 
trade(s).
22 RR Firm Missing or Invalid
The Registered Representative 
Firm is missing or invalid. O (Both) Firm Data
F20 02
B/U24 02
55-62
39-46
Optionally used on both SDR requests and 
responses, and indicates the firm affiliated with the 
named branch and registered representative of the 
trade(s).
23
Original SDR Control Number 
Missing or Invalid
The Original SDR Control Number 
on a Stop Recurring Request is 
missing or invalid. O Either Data F20 02 63-77
The original SDR Control Number is required when 
stopping a recurring request.  
24 Threshold Amount Invalid
The Threshold Amount specified in 
the SDR request is invalid. O Either Format F20 02 78-86
The Threshold Amount can be optionally specified 
on an SDR request, to indicate that the firm should 
only respond with trades that equal or exceed the 
dollar amount indicated.
Best Practice--validate as "transactions greater 
than or equal to the specified dollar amount."
6 of 21

---

## Page 7

Standardized Data Reporting (SDR) Reject Codes
Reject Code Text Description
Optional/
Required
[[NSCC]] 
or 
Firm
Format 
or 
Data
SDR 
Layouts
Field 
Location Comments/Best Practices
SDR 
Reject 
Code
25
Transaction Type Missing or 
Invalid
The Transaction Type on the SDR 
request or response is missing or 
invalid.
O
R [[NSCC]] Either
F20 02
B/U24 01
87-88
45-46
The Transaction Type is optional on SDR 
Requests, and can be used to indicate the Firm 
should only respond with trades of the type 
specified--either Buys or Sells.  
On SDR trade responses, the transaction type 
indicates the [[BASIC]] type of activity of each trade--
Buy, Sell, Exchange In, Exchange Out, etc.  See 
the F20 and B24 record layouts.
26
Fund/SERV Control Number 
Missing or Invalid
The Fund/SERV Control Number on 
the SDR request is missing.
OC
O Either Data
F20 01
B21 
84-98 
84-98
The Fund/SERV Control Number is required when 
the SDR Request Type is 04, Fund/SERV Control 
Number Request, and indicates that only trades for 
that omnibus [[NSCC]] transaction should be 
provided.  
It is also optionally found on the firm response, on 
the B21 header, but it is not edited.
27
SDR Response Number 
Missing or Invalid
The SDR Response Number of a 
Firm's response is missing. R (both) [[NSCC]] Data
B/U21
B/U27 01
101-115
42-56
The SDR Response Number is used by the firm to 
uniquely identify each response to an SDR 
Request.  The format is not mandated, but does 
have a Best Practices format.  See [[NSCC]] SDR 
Best Practices, SDR Response Number. The 
[[NSCC]] only validates that the field is populated.
28
Response Type Missing or 
Invalid
The firm's SDR Response Type on 
the response header is missing or 
invalid. R [[NSCC]] Data B/U21 99-100
The Response Type is used by the firm to indicate 
the specific type of response being provided--
Summary level, Detail level, Both, 
Acknowledgement, or Reject.  See the Technical 
Overview, SDR Response Data File Structure.
7 of 21

---

## Page 8

Standardized Data Reporting (SDR) Reject Codes
Reject Code Text Description
Optional/
Required
[[NSCC]] 
or 
Firm
Format 
or 
Data
SDR 
Layouts
Field 
Location Comments/Best Practices
SDR 
Reject 
Code
29
Partial Response Indicator 
Missing or Invalid
The firm's Partial Response 
Indicator on the response header is 
missing or invalid. O [[NSCC]] Data B/U21 116-116
The Partial Response Indicator is used by the firm 
to indicate the fulfillment level of the specific 
response being provided compared to the original 
SDR Request--Full/Final, Partial, or 
Incomplete/Final.  See the SDR Best Practices, 
SDR Reject Record, scenario 3, and Incomplete 
Responses.  Also see the Technical Overview, 
SDR Response Data.
30 Correction Indicator Invalid
The firm's Correction indicator on 
the response header is missing or 
invalid.  O [[NSCC]] Data B/U21 117-117
The Correction Indicator is used by the firm to 
indicate that this response is a correction to a 
previous response, and should replace the original 
response data.  See the Best Practices, Correction 
Indicator, and the Technical Overview, SDR 
Response Data, Response Data Definitions.
*
32
SSN/TIN Indicator Missing or 
Invalid
The firm's SSN/TIN Indicator on the 
Detail record is missing or invalid. R [[NSCC]] Data B/U24 01 36
The SSN/TIN indicator is used on Detail (B/U24) 
record responses, and indicates the type of TIN 
provided for the owner of the trade--0 for Tax [[ID]], 1 
for SSN, or 2 for [[investor]] TIN/EIN.
33 NAV Date Missing or Invalid
The Net [[Asset]] Value Date on the 
firm's response is missing or invalid. R [[NSCC]] Format
B/U24 01
B/U25 01
37-44
27-34
Required by [[NSCC]]. NAV Date is used on Detail 
and Summary response records to indicate the 
trade date of the transaction activity.
34 Transaction Code Invalid
The Transaction Code on the firm's 
Detail record is invalid. O [[NSCC]] Data B/U24 01 47-48
The Transaction Code is optionally used on B/U24 
Detail records, and provides a more specific 
transaction description than the Transaction Type 
field. See the B/U24 01 record layout for valid 
values.  
8 of 21

---

## Page 9

Standardized Data Reporting (SDR) Reject Codes
Reject Code Text Description
Optional/
Required
[[NSCC]] 
or 
Firm
Format 
or 
Data
SDR 
Layouts
Field 
Location Comments/Best Practices
SDR 
Reject 
Code
35
Transaction Category Missing 
or Invalid
The Transaction category on the 
firm's Detail record is missing or 
invalid. R [[NSCC]] Data B/U24 01 49-49
Required by [[NSCC]] on Detail records, and indicates 
if the transaction should be considered Category 1 
or 2.  Category 1 activities are [[participant]]-initiated 
or directed, and would be more suspect to scrutiny 
against market-timing policies.  Category 2 
transactions are more systematic, such as 
dividends or reinvestment activity.  A complete 
description of Transaction Category is provided in 
the SDR Best Practices User Guide, Category 1 
and Category 2 Transactions section.
36
Dollar Amount Missing or 
Invalid
The Dollar Amount on the firm's 
Detail Record is missing or invalid. RC [[NSCC]] Format B/U24 01 50-65
The Dollar Amount on the Detail Record is required 
by the [[NSCC]], unless the Transaction Type is 05 or 
06, or the Transaction Code is 07 or 52.
37
Share Amount Missing or 
Invalid
The Share Amount on the firm's 
Detail Record is missing or invalid. R [[NSCC]] Format B/U24 01 66-79
The Share Amount on the Detail Record is always 
required by the [[NSCC]].
38 Price Missing or Invalid
The Price on the firm's Detail record 
is missing or invalid. RC [[NSCC]] Format B/U24 01 80-91
Optional if Transaction Type is 05 or 06, or if 
Transaction Code is 07 or 52. Otherwise Required.
*
40 Contra Security [[ID]] Invalid Contra Security [[ID]] Invalid O Either Data B/U24 112-120
[[NSCC]] will validate this number using the [[CUSIP]] 
formula when this field is populated.  
41 STR Fee Amount Invalid
The Short Term Trader Redemption 
Fee amount on the firm's Detail 
record is invalid. O [[NSCC]] Format B/U24 02 6-12
See the B24 02 record layout.  This is a numeric 
field.
9 of 21

---

## Page 10

Standardized Data Reporting (SDR) Reject Codes
Reject Code Text Description
Optional/
Required
[[NSCC]] 
or 
Firm
Format 
or 
Data
SDR 
Layouts
Field 
Location Comments/Best Practices
SDR 
Reject 
Code
42 CDSC Amount Invalid
The Contingent Deferred Service 
Charge Amount on the firm's Detail 
Record is invalid. O [[NSCC]] Format B/U24 02 13-19
See the B24 02 record layout.  This is a numeric 
field.
43 Transaction Source Invalid
The Transaction Source on the 
firm's Detail Record is not a valid 
value. O [[NSCC]] Data B/U24 02 20-20
The Transaction Source is a code that defines who 
directed the transaction--the [[participant]], Plan, Rep, 
Record Keeper/Insurance Carrier, or Firm Cannot 
Determine.  See the record layouts for valid values, 
and the SDR Technical Overview, SDR Response 
Data: Transaction Source for more information.
*
47
Dollar Value of All [[participant]]/ 
Shareholder Buys Missing or 
Invalid
The Dollar Value of All [[participant]] 
Buys on the firm's Summary Record 
is missing or invalid. OC [[NSCC]] Format B/U25 01 35-50
At least one of the eight Dollar Value fields on the 
B25 Summary must be populated for the [[NSCC]] to 
accept the response.  The firm should provide as 
many of these Dollar Value fields as possible. 
See the B25 records 1 and 2 layouts, and a 
complete explanation is in the SDR Best Practices, 
Summary Data section.
48
Dollar Value of All [[participant]]/ 
Shareholder Sells Missing or 
Invalid
The Dollar Value of All [[participant]] 
Sells on the firm's Summary Record 
is missing or invalid. OC [[NSCC]] Format B/U25 01 51-66
At least one of the eight Dollar Value fields on the 
B25 Summary must be populated for the [[NSCC]] to 
accept the response.  The firm should provide as 
many of these Dollar Value fields as possible. 
See the B25 records 1 and 2 layouts, and a 
complete explanation is in the SDR Best Practices, 
Summary Data section.
49
Dollar Value of Category 1 
[[participant]]/ Shareholder Buys 
Missing or Invalid
The Dollar Value of Category 1 
[[participant]] Buys on the firm's 
Summary Record is missing or 
invalid. OC [[NSCC]] Format B/U25 01 67-82
At least one of the eight Dollar Value fields on the 
B25 Summary must be populated for the [[NSCC]] to 
accept the response.  The firm should provide as 
many of these Dollar Value fields as possible. 
See the B25 records 1 and 2 layouts, and a 
complete explanation is in the SDR Best Practices, 
Summary Data section.
10 of 21

---

## Page 11

Standardized Data Reporting (SDR) Reject Codes
Reject Code Text Description
Optional/
Required
[[NSCC]] 
or 
Firm
Format 
or 
Data
SDR 
Layouts
Field 
Location Comments/Best Practices
SDR 
Reject 
Code
50
Dollar Value of Category 1 
[[participant]]/ Shareholder Sells 
Missing or Invalid
The Dollar Value of Category 1 
[[participant]] Sells on the firm's 
Summary Record is missing or 
invalid. OC [[NSCC]] Format B/U25 01 83-98
At least one of the eight Dollar Value fields on the 
B25 Summary must be populated for the [[NSCC]] to 
accept the response.  The firm should provide as 
many of these Dollar Value fields as possible. 
See the B25 records 1 and 2 layouts, and a 
complete explanation is in the SDR Best Practices, 
Summary Data section.
51
Number of Category 1 
[[participant]]/ Shareholder Buys 
Invalid
The Number of Category 1 
[[participant]] Buys on the firm's 
Summary Record is invalid. O [[NSCC]] Format B/U25 01 99-106
See the B25 record 1 layout, and a complete 
explanation is in the SDR Best Practices, Summary 
Data section. The firm should provide as many 
of these Number Of fields as possible.
52
Number of Category 1 
[[participant]]/ Shareholder Sells 
Invalid
The number of Category 1 
[[participant]] Sells on the firm's 
Summary Record is invalid. O [[NSCC]] Format B/U25 01 107-114
See the B25 record 1 layout, and a complete 
explanation is in the SDR Best Practices, Summary 
Data section. The firm should provide as many 
of these Number Of fields as possible.
53 Social Code Missing or Invalid
The [[NSCC]] Social Code on either 
the firm's Detail or Summary 
request is invalid. O [[NSCC]] Data
B/U24 01
B/U25 01
121-122
121-122
Refer to the Social Code listing on [[NSCC]] website 
for valid values.
54
Dollar Value of All [[participant]]/ 
Shareholder Exchanges (Intra 
Fund Buy-Side) Missing or 
Invalid
The Dollar Value of All [[participant]] 
Exchanges (Intra Fund Buy Side) 
on the firm's Summary Record is 
missing or invalid OC [[NSCC]] Format B/U25 02 6-21
At least one of the eight Dollar Value fields on the 
B25 Summary must be populated for the [[NSCC]] to 
accept the response.  The firm should provide as 
many of these Dollar Value fields as possible. 
See the B25 records 1 and 2 layouts, and a 
complete explanation is in the SDR Best Practices, 
Summary Data section.
55
Dollar Value of All [[participant]]/ 
Shareholder Exchanges (Intra 
Fund Sell-Side) Missing or 
Invalid
The Dollar Value of All [[participant]] 
Exchanges (Intra Fund Sell Side) on 
the firm's Summary Record is 
missing or invalid. OC [[NSCC]] Format B/U25 02 22-37
At least one of the eight Dollar Value fields on the 
B25 Summary must be populated for the [[NSCC]] to 
accept the response.  The firm should provide as 
many of these Dollar Value fields as possible. 
See the B25 records 1 and 2 layouts, and a 
complete explanation is in the SDR Best Practices, 
Summary Data section.
11 of 21

---

## Page 12

Standardized Data Reporting (SDR) Reject Codes
Reject Code Text Description
Optional/
Required
[[NSCC]] 
or 
Firm
Format 
or 
Data
SDR 
Layouts
Field 
Location Comments/Best Practices
SDR 
Reject 
Code
56
Dollar Value of Category 1 
[[participant]]/ Shareholder 
Exchanges (Intra Fund Buy-
Side) Missing or Invalid
The Dollar Value of Category 1 
[[participant]] Exchanges (Intra Fund 
Buy Side) on the firm's Summary 
Record is missing or invalid. OC [[NSCC]] Format B/U25 02 38-53
At least one of the eight Dollar Value fields on the 
B25 Summary must be populated for the [[NSCC]] to 
accept the response.  The firm should provide as 
many of these Dollar Value fields as possible. 
See the B25 records 1 and 2 layouts, and a 
complete explanation is in the SDR Best Practices, 
Summary Data section.
57
Dollar Value of Category 1 
[[participant]]/ Shareholder 
Exchanges (Intra Fund Sell-
Side) Missing or Invalid
The Dollar Value of Category 1 
[[participant]] Exchanges (Intra Fund 
Sell Side) on the Summary Record 
is missing or invalid. OC [[NSCC]] Format B/U25 02 54-69
At least one of the eight Dollar Value fields on the 
B25 Summary must be populated for the [[NSCC]] to 
accept the response.  The firm should provide as 
many of these Dollar Value fields as possible. 
See the B25 records 1 and 2 layouts, and a 
complete explanation is in the SDR Best Practices, 
Summary Data section.
58
The Number of Category 1 
[[participant]]/ Shareholder 
Exchanges (Intra Fund Buy-
Side) is Invalid
The Number of Category 1 
[[participant]] Exchanges (Intra Fund 
Buy Side) on the firm's Summary 
Record is invalid. O [[NSCC]] Format B/U25 02 70-77
See the B25 record 1 layout, and a complete 
explanation is in the SDR Best Practices, Summary 
Data section. The firm should provide as many 
of these Number Of fields as possible.
59
Number of Category 1 
[[participant]]/ Shareholder 
Exchanges (Intra Fund Sell-
Side) Invalid
The Number of Category 1 
[[participant]] Exchanges (Intra Fund 
Sell Side) on the firm's Summary 
Record is invalid. O [[NSCC]] Format B/U25 02 78-85
See the B25 record 1 layout, and a complete 
explanation is in the SDR Best Practices, Summary 
Data section. The firm should provide as many 
of these Number Of fields as possible.
60
Number of [[shares]] in Plan/ 
[[investor]] Omnibus Account 
Invalid
Number of share in plan/[[investor]] 
omnibus account on the firm's 
Summary Record is invalid. O [[NSCC]] Format B/U25 02 86-99
See the B25 record 1 layout, and a complete 
explanation is in the SDR Best Practices, Summary 
Data section. The firm should provide as many 
of these Number Of fields as possible.
61 [[EOD]] Dollar Balance Invalid
The End of Day (Closing) Dollar 
Balance on the firm's Summary 
Record is invalid. O [[NSCC]] Format B/U25 02 100-115
See the B25 record 2 layout, and a complete 
explanation is in the SDR Best Practices, Summary 
Data section.
12 of 21

---

## Page 13

Standardized Data Reporting (SDR) Reject Codes
Reject Code Text Description
Optional/
Required
[[NSCC]] 
or 
Firm
Format 
or 
Data
SDR 
Layouts
Field 
Location Comments/Best Practices
SDR 
Reject 
Code
62
Total Detail Items Missing or 
Invalid
The Total Detail Items count 
provided in a firm's SDR response 
trailer is missing or invalid. R [[NSCC]] Format B/U27 01 75-83
The number specified in the trailer must equal the 
number of Detail records in the response set.
63
Total Summary Items Missing 
or Invalid
The total number of Summary 
records count in a firm's SDR 
response trailer is missing or 
invalid. R [[NSCC]] Format B/U27 01 84-92
The number specified in the trailer must equal the 
number of Summary records in the response set.
64
Total Records Missing or 
Invalid
The total number of records count 
in the SDR set (including header 
and trailer) trailer is missing or 
invalid. R [[NSCC]] Either
B/U27 01
B/F/N/U29
DataTrak 
Trailer
93-101
10-18
27-33
The number specified in this field in the trailer must 
equal the total number of all physical records in the 
response, including the header and trailer.  (Except 
in the DataTrak Trailer, where the header and 
trailer are not included in the total record count.)
*
66 Reject Code Invalid
The firm has provided a B/U23 
Reject response, but its Reject 
Code(s) is missing or invalid. R [[NSCC]] Data B/U 23 6-13
See the SDR Reject Code List (or use this list) for 
the valid reject codes a firm can use.
67
Acknowledgment Indicator 
Missing or Invalid
The firm's acknowledgement 
indicator on their Acknowledgement 
record is missing or invalid. R [[NSCC]] Data B/U22 6-6
This indicator specifies if the firm will provide the 
response (0), or if the request will be forwarded to 
an Underlying Firm (1).
68
Anticipated Response Date 
Invalid
The Anticipated Response Date in 
the firm's Acknowledgement is 
invalid.  O [[NSCC]] Format B/U22 7-14
The firm is providing its anticipated response date 
to respond to an SDR request, but the format is 
invalid.  (Note- as a Best Practice, routine SDR 
requests should be responded to within 5 
business days, or 5-10 days if there is a chain 
of intermediaries involved.  See Best Practices, 
Response Time for Data Requests.) 
13 of 21

---

## Page 14

Standardized Data Reporting (SDR) Reject Codes
Reject Code Text Description
Optional/
Required
[[NSCC]] 
or 
Firm
Format 
or 
Data
SDR 
Layouts
Field 
Location Comments/Best Practices
SDR 
Reject 
Code
69
Anticipated Response File 
Frequency Invalid
The Anticipated Response 
Frequency in the firm's 
Acknowledgement is invalid. O [[NSCC]] Data B/U22 15-15
The Anticipated Response Frequency is an 
indicator in the firm's acknowledgement that 
indicates if the response is Full (satisfies all the 
request criteria) or Partial (satisfies a portion of the 
request criteria).
70 Record Missing
A fund or firm SDR file is missing 
required records. N/A [[NSCC]] N/A N/A N/A
SDR files must contain all applicable records 
required based on the file being submitted.  For 
instance, fund requests use an F20 01 record, and 
optionally an F20 02 record can also be provided, 
which contains additional request criteria.  No other 
records are required for the fund request.  If the 
[[NSCC]] received a fund request with only an F20 02 
record, it would be rejected back to the fund.
Firm responses must always contain all required 
records for the response, including a header and 
trailer.  If any of these are missing, the [[NSCC]] 
would reject the response.  Detail responses 
always contain a B24 01 record, and optionally an 
additional B24 02.  Firm responses with only a B24 
02 record would be rejected.  This same logic 
applies to Summary responses, in addition to 
required headers and trailers. See the Technical 
Overview, Select Validation Rules.
71
Date Range Not Supported
Description will be changed to 
"[[intermediary]] Does Not 
Maintain Data for Time Period 
Requested."
The firm does not maintain data for 
the time period defined by the From 
Date and To Date included in the 
request. N/A Firm N/A N/A N/A
The reject text will be changed as noted.
The firm's books [[DO]] not contain any reportable 
activity within the date range specified for the 
request criteria.
72
Recurring Request Not 
Supported
The firm's system does not support 
the ability to provide ongoing 
responses to recurring SDR 
requests. N/A Firm N/A N/A N/A
The fund and firm will need to agree on an 
alternative method of supplying the data for the 
criteria specified in the recurring request.
14 of 21

---

## Page 15

Standardized Data Reporting (SDR) Reject Codes
Reject Code Text Description
Optional/
Required
[[NSCC]] 
or 
Firm
Format 
or 
Data
SDR 
Layouts
Field 
Location Comments/Best Practices
SDR 
Reject 
Code
73
Invalid Request Type for 
Account
The Request Type of the SDR is 
invalid for the specified firm 
account. N/A Firm N/A N/A N/A
An example would be an Plan Level SDR request 
to a firm account that is not a Plan, or does not 
contain that Plan within it.
74
Named Firm Does Not Have 
Information
Description will be changed to 
"This Tier of [[intermediary]] 
Does Not Maintain Data 
Requested."
The firm specified in the request 
does not have the requested data.  
This indicates a chain-of-
intermediaries relationship, where 
the specified firm does not contain 
the record keeping system where 
the actual data resides. N/A Firm N/A N/A N/A
The reject code text will be changed as noted.
In a chain of [[intermediary]] relationships, the first-tier 
[[intermediary]] may not be able to act as the conduit 
to forward the request on to the appropriate 
underlying firm.  In this case, the firm should 
provide contact information to the fund for the 
actual underlying [[intermediary]] who does maintain 
the records.
This is described further in the SDR Best Practices, 
Chain of [[intermediary]] Relationships section.
75
Information Previously 
Provided
The firm is advising the fund that 
the data to satisfy the current 
request has already been provided 
to the fund- in a previous response 
to an earlier request. N/A Firm N/A N/A N/A
Funds should not make date range requests that 
have overlapping dates, to avoid redundant 
responses.  This is discussed further in the Date 
Range Requests section of the Best Practices 
guide.
76
Rep Level Request Not 
Supported
The firm does not support 
Representative Level SDR 
requests. N/A Firm N/A N/A N/A
The firm does not have the ability to segregate 
response data by Registered Representative.  
Since the firm cannot satisfy the request criteria, no 
data will be provided to the fund.
77
Transaction Type Search Not 
Supported
The firm does not support 
Transaction Type-specific SDR 
requests. N/A Firm N/A N/A N/A
The firm's response process does not have the 
functionality to segregate activity by Transaction 
Type.  (For example--Only Buys, or Only Sells.) 
Since the firm can not meet the request criteria, no 
data will be provided to the fund.
15 of 21

---

## Page 16

Standardized Data Reporting (SDR) Reject Codes
Reject Code Text Description
Optional/
Required
[[NSCC]] 
or 
Firm
Format 
or 
Data
SDR 
Layouts
Field 
Location Comments/Best Practices
SDR 
Reject 
Code
78
Fund/SERV Control Number 
Search Not Supported
The firm does not support 
Fund/SERV Control Number SDR 
requests. N/A Firm N/A N/A N/A
The firm's response process does not have the 
functionality to segregate activity by Fund/SERV 
Control Number.  Since the firm cannot meet the 
request criteria, no data will be provided to the 
fund.
79
Category 2 Transactions Not 
Supported
The firm does not support the ability 
to include Category 2 transactions 
in their SDR response. N/A Firm N/A N/A N/A
The firm's response process does not have the 
functionality to report Category 2 activity.  Since the 
firm cannot meet the request criteria, no data will 
be provided to the fund.  (See SDR Best Practices, 
Category 1 & Category 2 Transactions.)
80
Threshold Amount Not 
Supported
The firm does not support the ability 
to filter response data by a 
minimum dollar amount threshold. N/A Firm N/A N/A N/A
The firm's response process does not have the 
functionality to segregate activity by a threshold 
dollar amount.  Since the firm can not meet the 
request criteria, no data will be provided to the 
fund.
81
Account is Non-Omnibus 
(Single Shareholder)
The fund has submitted an SDR 
request to a non-omnibus account 
of a firm. N/A Firm N/A N/A N/A
The account identified in the request is not an 
omnibus account, therefore no SDR request is 
needed. The activity of this account is already on 
the Fund's recordkeeping system.
82
Underlying Firm Will Not 
Provide Information
An underlying firm will not be 
providing a response to the SDR 
request. N/A Firm N/A N/A N/A
This reject is provided by a first tier firm when the 
firm has forwarded a fund request to an underlying 
[[intermediary]], but the underlying [[intermediary]] has 
indicated they will not or cannot provide any data in 
response to the request.  
This may require further communication 
between the fund and the firm.
16 of 21

---

## Page 17

Standardized Data Reporting (SDR) Reject Codes
Reject Code Text Description
Optional/
Required
[[NSCC]] 
or 
Firm
Format 
or 
Data
SDR 
Layouts
Field 
Location Comments/Best Practices
SDR 
Reject 
Code
83
Response Provided Outside of 
[[NSCC]]
The firm is responding outside of 
the SDR process. N/A Firm N/A N/A N/A
A firm may receive a request through SDR, but 
deliver response data to the fund outside the SDR 
system.  This reject code is to advise the fund that 
the response was delivered outside of the SDR 
process.
84
Header Record Missing or 
Invalid The Header is missing or invalid. R [[NSCC]] N/A N/A N/A This is always required. See the records layouts.
85
Trailer Record Missing or 
Invalid The Trailer is missing or invalid. R [[NSCC]] N/A N/A N/A This is always required. See the records layouts.
86
Duplicate SDR Control 
Number
This SDR Control Number is a 
duplicate of a previous one. N/A Either Either N/A N/A
Each SDR Control Number must be unique, and 
follow the format in the record layouts.  This is 
described further in the Technical Overview, Field 
Definitions.
87
Record Type Not Compatible 
With Response Type
The SDR file contains records that 
[[DO]] not correspond with the type of 
SDR file. N/A [[NSCC]] N/A N/A N/A
For example, a firm has responded with an F20 
(SDR Request) record within its response.  This 
record would instead be used in a fund SDR 
request.  Another example would be a firm 
Acknowledgement response (B/U22) that also 
contained a B/U24 record (SDR Detail). See the 
Technical Overview, SDR Request Data File 
Structure, and SDR Response Data File Structure.
88
Total Acknowledgment Items 
Missing Or Invalid
The total of the number of 
Acknowledgment records contained 
in this response is missing or 
invalid.  This is a field in the Trailer 
record of the firm response. R [[NSCC]] Format B/U27 01 57-65
The Trailer record (B/U27) of any firm response 
must contain the total counts of each type of 
possible firm response record, even if the particular 
response does not contain them .  Zeroes are 
allowed, as these are required fields.  These trailer 
fields are counts for Total Acknowledgements, 
Total Rejects, Total Details, Total Summaries, and 
Total Records. 
17 of 21

---

## Page 18

Standardized Data Reporting (SDR) Reject Codes
Reject Code Text Description
Optional/
Required
[[NSCC]] 
or 
Firm
Format 
or 
Data
SDR 
Layouts
Field 
Location Comments/Best Practices
SDR 
Reject 
Code
89
Total Reject Items Missing Or 
Invalid
The total of the number of Reject 
records contained in this response 
is missing or invalid.  This is a 
required field in the Trailer record of 
the firm response. R [[NSCC]] Format B/U27 01 66-74
The Trailer record (B/U27) of any firm response 
must contain the total counts of each type of 
possible firm response record, even if the particular 
response does not contain them .  Zeroes are 
allowed, as these are required fields.  These trailer 
fields are counts for Total Acknowledgements, 
Total Rejects, Total Details, Total Summaries, and 
Total Records. 
90
Firm Number Does Not Match 
Firm Number On Original 
Request
The Firm Number in a firm's 
response header does not match 
the firm # specified in the original 
SDR request. R [[NSCC]] Data B/U21 01 21-24
The firm's response file to an SDR request has a 
different firm # from the original request.  The 
[[NSCC]] checks the firm response against the SDR 
reminder database, and if the SDR # is found, the 
B/U21 header fields are edited against those 
specified in the original request.  (The original SDR 
numbers are stored in the Reminder database for 
10 days.)
91
Fund Number Does Not Match 
Fund Number On Original 
Request
The Fund Number specified in a 
firm's response header does not 
match the fund # specified in the 
original SDR request. R [[NSCC]] Data B/U21 01 25-28
The firm's response file to an SDR request has a 
different fund # than the original request.  The 
[[NSCC]] checks the firm response against the SDR 
reminder database, and if the SDR # is found, the 
B/U21 header fields are edited against those 
specified in the original request. (The original SDR 
numbers are stored in the Reminder database for 
10 days.)
18 of 21

---

## Page 19

Standardized Data Reporting (SDR) Reject Codes
Reject Code Text Description
Optional/
Required
[[NSCC]] 
or 
Firm
Format 
or 
Data
SDR 
Layouts
Field 
Location Comments/Best Practices
SDR 
Reject 
Code
92
Underlying Firm Number Does 
Not Match Underlying Firm 
Number On Original Request
The Underlying Firm Number 
specified in a firm's response 
header does not match the 
underlying firm # specified in the 
original SDR request. O/C [[NSCC]] Data B/U21 01 38-41
The firm's response file to an SDR request has a 
different underlying firm # than the original request.  
The [[NSCC]] checks the firm response against the 
SDR reminder database, and if the SDR # is found, 
the B/U21 header fields are edited against those 
specified in the original request. (The original SDR 
numbers are stored in the Reminder database for 
10 days.)
93
Security Issue [[ID]] Does Not 
Match Security Issue [[ID]] On 
Original Request
The Security Issue [[ID]] specified in 
the firm's response header does not 
match the security issue [[ID]] on the 
original SDR request. R [[NSCC]] Data B/U21 01 29-37
The firm's response file to an SDR request has a 
different security issue [[ID]] than the original request.  
The [[NSCC]] checks the firm response against the 
SDR reminder database, and if the SDR # is found, 
the B/U21 header fields are edited against those 
specified in the original request. (The original SDR 
numbers are stored in the Reminder database for 
10 days.)
94
Additional Input Record Is 
Required For This Input Type
This reject code indicates that the 
[[NSCC]] has received an optional 
"record 02" on a fund request or 
firm response, without the 
accompanying and required record 
01 of the same type.  See 
"Comments" at the right for 
examples.  R [[NSCC]] N/A
F20 01&2
B/U24 01&2
B/U25 01&2 N/A
Examples of this would be:
A fund submitting an SDR Request with only the 
optional F20 02 record, and not the required F20 
01 record, or
a firm submitting an SDR Detail response with only 
an (optional) B24 02 record, and not the required 
B24 01 that must precede it, or
a firm submitting a SDR Summary response with 
only an (optional) B25 02 record, and not the 
required B25 01 that must precede it.
Or an SDR file that contains multiple occurrences 
of these errors. (Also note--sequence 01 and 02 
records must always be in their correct order to 
each other in the file.)
See the record layouts.
19 of 21

---

## Page 20

Standardized Data Reporting (SDR) Reject Codes
Reject Code Text Description
Optional/
Required
[[NSCC]] 
or 
Firm
Format 
or 
Data
SDR 
Layouts
Field 
Location Comments/Best Practices
SDR 
Reject 
Code
95
Duplicate Acknowledgment 
Record Between Header And 
Trailer
The firm has sent two identical 
acknowledgment records between a 
header and a trailer in their 
response. N/A [[NSCC]] N/A B/U22 N/A
Only one is allowed. See the Technical Overview, 
Acknowledgment Response, and also Select 
Validation Rules-Records between Header and 
Trailer.
96
Duplicate Reject Record 
Between Header And Trailer
The firm has sent two identical 
reject records between a header 
and a trailer in their response. N/A [[NSCC]] N/A B/U23 N/A
Only one is allowed.  See the Technical Overview, 
Select Validation Rules-Records between Header 
and Trailer.
97
Key Field On Trailer Does Not 
Match The Same Field On 
Header
The same required field on the 
firm's response header and trailer 
records contains different values. N/A [[NSCC]] Data B/U27 01 various
See record layouts to compare the corresponding 
fields on the Header and Trailer. The trailer fields 
must match the corresponding header ones.  
98 Unit Value Indicator Invalid
The Unit Value Indicator field on the 
firm's SDR Detail (B/U24) record is 
invalid.  O [[NSCC]] Data B/U24 01 123-123
The Unit Value Indicator on the firm's Detail record 
is invalid.  The valid values are 0 or Space=[[shares]], 
and 1=Units. 
99
Firm is Not [[Member]] of SDR 
service
A fund has sent a request to an 
[[NSCC]] [[participant]] firm, but the firm 
is not a [[Member]] of the SDR 
service. N/A [[NSCC]] Data F20 21-24
The firm must be an [[NSCC]] [[participant]] subscribed 
to the Networking SDR feature to participate in 
Standardized Data Reporting.  The list of 
participating firms is on the [[DTCC]] website, under 
Services by Firm. It is updated monthly.
A0
Fund is Not [[Member]] of SDR 
service
A firm has sent a response 
(unsolicited) to an [[NSCC]] [[participant]] 
fund but the fund does not use the 
SDR service. N/A [[NSCC]] Data B/U21 21-24
The fund must be an [[NSCC]] [[participant]] subscribed 
to the Networking SDR feature to participate in 
Standardized Data Reporting. The list of 
participating funds is on the [[DTCC]] website, under 
Services by Fund. It is updated monthly.
20 of 21

---

## Page 21

Standardized Data Reporting (SDR) Reject Codes
Reject Code Text Description
Optional/
Required
[[NSCC]] 
or 
Firm
Format 
or 
Data
SDR 
Layouts
Field 
Location Comments/Best Practices
SDR 
Reject 
Code
A1
Underlying Firm is Not 
[[Member]] of SDR service
The underlying firm specified in a 
fund request or a firm response is 
not a [[Member]] of the SDR service. N/A [[NSCC]] Data
F20 01
B/U21 01
38-41
38-41
The underlying firm must be an [[NSCC]] [[participant]] 
subscribed to the Networking SDR feature to 
participate in Standardized Data Reporting. The list 
of participating firms is on the [[DTCC]] website, 
under Services by Firm. It is updated monthly.
A2 Plan [[ID]] Requested is Closed
This will be a new reject code.
The plan referenced in the SDR 
request is closed on the firm's 
books. N/A Firm Data N/A N/A
The firm is notifying the fund that the plan 
referenced in the request is closed, and therefore 
has no activity to report.
A3
Requested Criteria Matched--
No Transaction Activity Exists
This will be a new reject code.
The firm and account information 
specified on the fund's request 
match to valid accounts on the 
firm's books, but there is no 
reportable activity matching the 
requested criteria. N/A Firm Data N/A N/A
This may require communication and clarification 
between the fund and firm.  If the fund is doing 
solicitations based on a calendar schedule or 
frequency, the firm may not have any reportable 
activity matching the request criteria.  If the 
fund is doing solicitations based on the 
omnibus account activity, they may need to 
work together to determine the request criteria 
and reportable activity that would satisfy it.
Note: The following reject codes will be permanently eliminated from the list effective April 23, 2012 (Important Notice# A 7355 P&S# 6925)
31 - Did not find data that matches the request **
39 - Tran [[ID]] is invalid
44 - Agent for Firm is invalid
45 - Plan Name is Invalid
46 - Customer Name is Invalid
65 - Reject Indicator Missing or Invalid
** Reject Code 31 has been replaced by A2 "Plan [[ID]] Requested is Closed," and A3 "Requested Criteria Matched--No Transaction Activity Exists."
21 of 21