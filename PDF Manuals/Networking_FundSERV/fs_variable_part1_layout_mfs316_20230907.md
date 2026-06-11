---
title: "Fund/SERV - Variable Length Record Layouts (Part 1)"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_variable_part1_layout_mfs316_20230907.pdf"
pages: 200
size: "1425.5 KB"
category: "Networking_FundSERV"
ingested_on: "2026-06-05"
---

# Fund/SERV - Variable Length Record Layouts (Part 1)

**Original File:** [fs_variable_part1_layout_mfs316_20230907.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_variable_part1_layout_mfs316_20230907.pdf)  
**Category:** Networking_FundSERV  
**Total Pages:** 200  
**File Size:** 1425.5 KB  

---

## Page 1

 
 
 
Fund/SERV® 
VARIABLE LENGTH RECORD LAYOUTS (PART 1) 
SEPTEMBER 7, 2023 
 

---

## Page 2

Variable Length Record Layouts (Part 1) 
Summary of Changes 2 
 
HISTORY OF CHANGES 
Dates Important Notices 
September 7, 2023 Record has been rebranded and reviewed.  
March 10, 2023 • 529 Account Plan fields added to 018 and 019 records (effective May 15, 
2023).  
  Please see Important Notice:  
  a9267 P&S 8840 Dated February 10, 2023 
• Summary of Changes has been moved to back of document 
• Record has been rebranded 
Effective Date: March 28, 2022 Please see Important Notices: 
a9045 P&S 8618 & a9044 P&S 8617 Dated September 2, 2021 
December 7, 2021 Document links updated due to launch of new Learning Center 
Effective Date: March 25, 2019 Please see Important Notice: 
a8658 P&S a8233 Dated December 19, 2018 
Effective Date: November 20, 2017 Please see Important Notice: 
a8402 P&S 7977 Dated June 1, 2017 
Effective Date: September 26, 2016      Please see Important Notice: 
a8159 P&S 7734 Dated February 3, 2016 
Effective Date: February 29, 2016 Please see Important Notice: 
a8107 P&S 7682 Dated October 27, 2015 
Effective Date:  July 27, 2015 Please see Important Notice:  
a7997 P&S 7572 Dated March 12, 2015 
Effective Date:  April 27, 2015 Please see Important Notice:  
a7926 P&S 7501 Dated November 4, 2014 
Documentation Changes a7865  P&S 7435 Dated July 2, 2014 
Effective Date:  July 28, 2014 Please see Important Notice:  
a7701 P&S 7371 Dated May 15, 2014 (REVISED) 
a7701 P&S 7371 Dated March 17, 2014 
Effective Date:  November 18, 2013 Please see Important Notice:  
a7665 P&S 7235 Dated July 3, 2013 
Effective Date:  March 18, 2013 Please see Important Notice:  
a7472 P&S 7042 Dated August 16, 2012 (enhancement details) 
a7567 P&S 7137 Dated January 9, 2013 (revised dates) 
a7570 P&S 7140 Dated January 11, 2013 

---

## Page 3

Variable Length Record Layouts (Part 1) 
Summary of Changes 3 
 
Dates Important Notices 
Documentation Changes Please see Important Notice: 
a7592 P&S 7162 Dated March 1, 2013 
Effective Date:  April 23, 2012 Please see Important Notice:  
A7355 P&S 6925 Dated January 12, 2012 
Note: On 2/27/2012 a correction was made to 401 Records to reflect the 
changes that were made in accordance with Important Notice a6272 P&S 
5842.   
The Fund Account Indicator 4 (New Account – U.S. Tax Resident Living 
Abroad) has been added to Account Representative Name, Account 
Representative Number and Branch Identification Number fields as part of 
conditional requirements. 
Effective Date:  December 5, 2011 Please see Important Notice:  
a7256 P&S 6826 Dated July 29, 2011 
Effective Date:  October 17, 2011 Please see Important Notice:  
a7241 P&S 6811 Dated July 8, 2011 
Effective Date: June 13, 2011 Please see Important Notice:  
a7175 P&S 6745 Dated March 7, 2011 
Effective Date: January 18, 2011 Please see Important Notice:  
a7079 P&S 6650 Dated October 18, 2010 
Effective Date: November 22, 2010 Please see Important Notice:  
a7044 P&S 6615 Dated August 17, 2010 
Effective Date: December 7, 2009 Please see Important Notice:  
a6874 P&S 6444 Dated September 17, 2009 
Effective Date: October 5, 2009 Please see Important Notice:  
a6819 P&S 6389 Dated May 8, 2009  
Effective Date: December 1, 2008 Please see Important Notices:  
a6667 P&S 6237 Dated July 29, 2008 
a6653 P&S 6223 Dated July 7, 2008 
a6620 P&S 6190 Dated May 20, 2008 

---

## Page 4

Variable Length Record Layouts (Part 1) 
Summary of Changes 4 
 
TABLE OF CONTENTS 
Summary of Changes .......................................................................................................................................... 8 
Introduction .......................................................................................................................................................... 9 
1. General .................................................................................................................................................. 9 
2. Variable Length Format ......................................................................................................................... 9 
3. Control Number ....................................................................................................................................10 
4. Check Digit ...........................................................................................................................................10 
5. SSN/EIN Start Section Number ...........................................................................................................11 
Record Layouts .................................................................................................................................................. 14 
02.00.00 Fixed Record Layout Column Headings ............................................................................................14 
Record Type List ................................................................................................................................................ 16 
02.01.00 Record Type List ................................................................................................................................16 
Order (001) .......................................................................................................................................................... 19 
02.01.01 Order (001) ....................................................................................................................................19 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund 
Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund (140) ............................................... 39 
02.02.01 As-of Order (004)...........................................................................................................................39 
Extended Correction Transfer (200); Extended Correction Transfer Acknowledgment (201)  ................... 63 
02.03.01 Extended Correction Transfer (200) ..............................................................................................63 
Order Acknowledgment for Money Market Purchase (101); Firm Delete (102); Release to [[settlement]] (109); 
Registration Acknowledgment (112); Delete Pending Registration (Registered Ex -Fund/SERV) (113); 
Receiving Fund Exit from ToRA (214) .............................................................................................................. 67 
02.04.01 Order Acknowledgement for Money Market Purchase (101) ........................................................67 
Fund Reject (100); Fund Delete (108); Registration Rejection (114); Delete Pending Release to [[settlement]]; 
(Settled Ex-Fund/SERV) (129) ........................................................................................................................... 71 
02.05.01 Fund Reject (100) ..........................................................................................................................71 
Exchange Order (015) ........................................................................................................................................ 75 
02.06.01 Exchange Order (015) ...................................................................................................................75 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post S ettlement Exchange Cancellation 
(021) ..................................................................................................................................................................... 85 
02.07.01 Exchange Confirmation (016) ........................................................................................................85 

---

## Page 5

Variable Length Record Layouts (Part 1) 
Summary of Changes 5 
 
Appendix – Summary of Changes .................................................................................................................. 100 
Summary of Changes – effective Q2  05/15/2023.......................................................................................... 101 
1. New Data Field in Existing Record Sequence ...................................................................................101 
2. New Reject Code ........................................................................................................................................101 
Summary of Changes – effective Q1 03/28/2022 ........................................................................................... 102 
1. Requirements Changed for Existing Fields .......................................................................................102 
2. New Data Fields .................................................................................................................................107 
3. New Optional Record Type ................................................................................................................110 
4. New Reject Code ...............................................................................................................................110 
5. Notes Added to Existing Field ............................................................................................................110 
Summary of Changes – effective Q1 03/25/2019 ........................................................................................... 111 
Reject Codes ..................................................................................................................................................111 
Summary of Changes – effective Q4 11/20/2017 ........................................................................................... 112 
1. New Values Added to Existing Fields ................................................................................................112 
2. Requirements Changed for Existing Fields .......................................................................................117 
3. Modified Description of Existing Field ................................................................................................122 
Summary of Changes – effective Q3 09/26/2016 ........................................................................................... 123 
1. New Fields .........................................................................................................................................123 
2. Renamed Fields .................................................................................................................................124 
3. Requirements Changed for Existing Fields .......................................................................................126 
4. Reject Codes .....................................................................................................................................146 
5. Modified Description of Record Length (001, 004, & 003) .................................................................148 
Summary of changes – effective Q1 02/29/2016 ........................................................................................... 150 
Summary of changes – effective Q3 07/27/2015 ........................................................................................... 151 
Requirements Changed for Existing Field ......................................................................................................151 
Summary of changes – effective Q2 04/27/2015 ........................................................................................... 152 
Requirements Changed for Existing Fields ....................................................................................................152 
Summary of changes – effective Q3 07/02/2014 ........................................................................................... 153 
1. Documentation Changes ...................................................................................................................153 
Summary of changes – effective Q3 07/28/2014 ........................................................................................... 154 

---

## Page 6

Variable Length Record Layouts (Part 1) 
Summary of Changes 6 
 
1. New Fields .........................................................................................................................................154 
2. Reject Codes .....................................................................................................................................154 
3. Modified Description of Existing Fields ..............................................................................................154 
Summary of changes – effective Q4 11/18/2013 ........................................................................................... 156 
1. New Fields .........................................................................................................................................156 
2. Values or Comments Added to or Deleted from Existing Fields........................................................156 
3. Reject Codes .....................................................................................................................................161 
Summary of changes – effective Q1 3/18/2013 ............................................................................................. 162 
1. Values or Comments Added to or Deleted from Existing Fields........................................................162 
2. Requirements Changed for Existing Fields .......................................................................................168 
Summary of changes – effective Q1 2013 ..................................................................................................... 170 
1. Modified Description of Values of Existing Field ................................................................................170 
Summary of changes – effective Q2 4/23/2012 ............................................................................................. 172 
1. Values or Comments Added to or Deleted from Existing Fields........................................................172 
2. Requirements Changed for Existing Fields .......................................................................................173 
3. Reject Codes .....................................................................................................................................174 
Summary of changes – effective Q4 12/5/2011 ............................................................................................. 176 
1. New Fields .........................................................................................................................................176 
Summary of changes – effective Q4 10/17/2011 ........................................................................................... 177 
1. New Fields .........................................................................................................................................177 
2. Values or Comments Added to or Deleted from Existing Fields........................................................177 
3. Requirements Changed for Existing Fields .......................................................................................178 
Summary of changes – effective Q2 2011 ..................................................................................................... 179 
1. New Fields .........................................................................................................................................179 
2. Values or Comments Added to or Deleted from Existing Fields........................................................179 
Summary of changes – effective Q1 2011 ..................................................................................................... 181 
1. Record Changed from Optional to Optional Conditional ...................................................................181 
2. Renamed Fields .................................................................................................................................181 
3. Values or Comments Added to or Deleted From Existing Fields ......................................................182 
4. Requirements Changed for Existing Fields .......................................................................................184 

---

## Page 7

Variable Length Record Layouts (Part 1) 
Summary of Changes 7 
 
5. Reject Codes .....................................................................................................................................185 
Summary of changes – effective Nov 2010 ................................................................................................... 187 
1. New Fields .........................................................................................................................................187 
2. Record Changed from Optional to Optional Conditional ...................................................................187 
3. Renamed Fields .................................................................................................................................187 
4. Requirements Changed for Existing Fields .......................................................................................188 
5. Reject Codes .....................................................................................................................................189 
Summary of changes – effective Q4 2009 ..................................................................................................... 191 
1. New Fields .........................................................................................................................................191 
2. Renamed Fields .................................................................................................................................191 
3. Values or Comments Added to Existing Fields..................................................................................192 
Summary of changes – effective Q3 2009 ..................................................................................................... 195 
1. New Fields .........................................................................................................................................195 
2. Record Lengths Changed ..................................................................................................................195 
3. Renamed Fields .................................................................................................................................195 
4. Values or Comments Added to or Deleted from Existing Fields........................................................196 
5. Reject Codes .....................................................................................................................................198 
Summary of changes – effective Dec 2008 ................................................................................................... 199 
1. New Fields .........................................................................................................................................199 
2. New Values to Existing Fields ...........................................................................................................199 
 

---

## Page 8

Variable Length Record Layouts (Part 1) 
Summary of Changes 8 
 
SUMMARY OF CHANGES 
See the Appendix for the Summary of Changes. 
 

---

## Page 9

Variable Length Record Layouts (Part 1) 
Introduction 9 
 
INTRODUCTION 
1. General  
Some of Fund/SERV record layout features are:  
1. Fund/SERV records can be received or submitted in either of two formats: fixed length or variable length.  
Data received or submitted interactively (via MQM) must be in variable length format.  
This document describes Fund/SERV variable length record layouts.  
2. Only [[NSCC]] rejected transactions are being returned by [[NSCC]] to the originating [[participant]]. Accepted 
transactions are being sent to the contra [[participant]] only.  
3. Fund Number in input records is always an optional field. If fund number is not provided on input, it will be 
identified by Fund/SERV via the security issue. The contra side will always get the records with the fund 
number. 
Note: 
When a fund generates the control number (as in Fund Originated Order) the fund number within the control number 
is required.  
4. The term ‘firm’ throughout this document refers to dealer, [[Broker]], bank, etc. (not to be confused with 
‘fund’).  
5. When rejecting a transaction for more than one reason, Fund/SERV reports multiple reject codes via 
record type 120 (see section 02.25.01) which follows the rejected transaction back to the originating 
[[participant]]. 
 
2. Variable Length Format  
Each variable length transaction is one record. Bytes 1-11 are control information which consist of the following 
fields:  
1. Record Length (bytes 1-4)  
2. Physical Sequence Number (bytes 5-6)  
3. Logical Sequence Number (bytes 7-8)  
4. Originator Type (byte 9)  
5. Filler (for future use) (bytes 10-11)  
 
Every section of 93 bytes thereafter is identical to bytes 8 through 100 of the respective 100 byte fixed length 
record. 

---

## Page 10

3. Control Number  
Control number rules are as follows:  
6. Control number is 15 bytes long and is generated by the [[participant]] who submits the original transaction 
(firm for record type 001, fund for record type 007 etc.).  
7. Control number format is ‘ppppydddssssssc’ where:  
 
pppp = Originating [[participant]] (firm/fund/TPA/SP) [[NSCC]] number  
y = Last digit of year  
ddd = Julian date  
ssssss = Sequential number  
c = Check digit (using Modulus 10 Double Add Double algorithm. See item 4 below)  
Note: 
It is recommended that the Julian date 'yddd' reflects the order submission date (so it's easy to create unique control 
numbers). However, Fund/SERV does not force that.  
Control number for ACATS Transfer (record type 018) is 15 bytes long and is generated by Fund/SERV. The 
format is ‘catsaydddssssss’ where: 
catsa  = CATSA  
y  = Last digit of year  
ddd  = Julian date  
ssssss  = Sequential number 
4. Check Digit  
To calculate a check digit for the control number, using Modulus 10 Double Add Double algorithm, take the 
following steps:  
8. Assign a position number to each digit of the control number according to its position in the control 
number as follows: 
 
Odd position: the assigned position number is 1.  
Even position: the assigned position number is 2.  
 
9. Multiply each digit of the control number by its assigned position number.  
10. Sum the products up, but note the following: if a product is two digits long, add each digit separately to the 
sum.  
11. Subtract the last digit of the sum from 10. The last digit of the result (also called 10 Complement) is the 
check digit. 

---

## Page 11

Variable Length Record Layouts (Part 1) 
Introduction 11 
 
Example: 
1. First 14 bytes of control number: 13572028000037  
2. Assign position numbers: 12121212121212  
3. Multiply each digit of the control number by its assigned position number: 
1 * 1 = 1 
3 * 2 = 6 
5 * 1 = 5 
7 * 2 = 14 
2 * 1 = 2 
0 * 2 = 0 
2 * 1 = 2 
8 * 2 = 16 
0 * 1 = 0 
0 * 2 = 0 
0 * 1 = 0 
0 * 2 = 0 
3 * 1 = 3 
7 * 2 = 14  
4. Sum the products up: 
1 + 6 + 5 + 1 + 4 + 2 + 0 + 2 + 1 + 6 + 0 + 0 + 0 + 0 + 3 + 1 + 4 = 36  
5. Subtract the last digit of the sum from 10: 
10 - 6 = 4  
6. The check digit is 4 and the whole control number is: 135720280000374 
 
5. SSN/EIN Start Section Number 
A. Sections in Variable length layouts 
Variable length layouts are comprised of implicit sections. The first section is 104 bytes long. Every other 
section is 93 bytes long. For example, the start and end positions of the first 10 sections in a variable length 
layout are as follows: 
Section Number Start Position End Position Length 
1 1 104 104 
2 105 197 93 
3 198 290 93 
4 291 383 93 
5 384 476 93 
6 477 569 93 
7 570 662 93 
8 663 755 93 
9 756 848 93 

---

## Page 12

Variable Length Record Layouts (Part 1) 
Introduction 12 
 
Section Number Start Position End Position Length 
10 849 941 93 
… … … … 
 
B. SSN/EIN Start Section Number  
Field SSN/EIN Start Section Number is a two-byte field starting at position 97 in the following record layouts: 
Order (001) layout (section 02.01.01) 
As-Of Order (004)  (section 02.02.01) 
Exchange (015) layout (section 02.06.01) 
Correction (003) layout (section 02.29.01) 
 
The value in field SSN/EIN Start Section Number specifies the section number of the first SSN/EIN section in 
the incoming transaction. 
 
C. Figuring SSN/EIN Start Section Number  
Let’s say that: 
• N = Section number of the first SSN/EIN section in the incoming transaction 
• E = Position of the last byte of the suffixed item 
 
To calculate N when E is known (usually when creating the record), the following formula can be used:  
• N = ((E  –  11) / 93) + 1 
 
To find E when N is known (usually when reading the record) the following formula can be used:  
• E = ((N  –  1) * 93) + 11  
Example1: 
Creating an order (001) with 4 sections of the order layout and 2 SSN/EIN sections. 
a. Position of the last byte of the created order layout (E): 383 (see table above) 
b. Calculating the section number of the first SSN/EIN section (N): 
 N = ((E  –  11) / 93) + 1 = ((383  –  11) / 93) + 1 = (372 / 93) + 1 = 4 + 1 = 5 
c. The value in filed SSN/EIN Start Section Number should be 05.  
Note: 
The value in field Record Length of this order should be 0569, which is the combined length of the order item and the 
EIN/SSN suffix.  
 

---

## Page 13

Variable Length Record Layouts (Part 1) 
Introduction 13 
 
Example2: 
Reading an order (001) with 6 records of the order layout and one SSN/EIN record. 
a. Value in field SSN/EIN Start Section Number (N): 07  
b. Calculating the position of the last byte of the order layout (E): 
 E = ((N  –  1) * 93) + 11 = ((7  –  1) * 93) + 11 = (6 * 93) + 11 = 558 + 11 = 569 
c. Last position of the order layout is 569 
d. The EIN/SSN suffix starts at position 570. 
Note: 
The value in field Record Length of this order should be 0662, which is the combined length of the order item and the 
EIN/SSN suffix.  

---

## Page 14

Variable Length Record Layouts (Part 1) 
Record Layouts 14 
 
RECORD LAYOUTS  
02.00.00 Fixed Record Layout Column Headings 
The following are Fund/SERV Fixed Length Record Layouts. The column headings are as follows:  
Start - The position where the field starts. 
End - The position where the field ends. 
Len - The length of the field in bytes 
Type - The type of the field:  
A/N = Alphanumeric 
N = Numeric 
Field Name - The name of the field. 
Description - Field description (format, valid values, conditional requirements, etc.). 
Opt/Req - Indicates whether the field is optional or required: 
O = Optional  
R = Required  
OC = Generally optional, but required upon specified conditions 
RC = Generally required, but optional upon specified conditions   
Reject Code - The reject code which indicates that this field is invalid.  
Notes: 
• Alphanumeric type fields may include any character in the computer character set, but should not include unprintable 
characters such as Low-Value, High-Value, Comp-3 fields, etc., since these kind of characters may cause problems 
during transmission time.  
• Numeric type fields may include digits (0-9) only.  
• Required fields mean the following: 
a. Fields with specified list of values must have one of those values. 
b. Alphanumeric type fields without specified list of values may have any value as described in the first note above, but 
must not be spaces. 
c. Numeric type fields without a specified list of values must be numeric greater than zero. 
d. Fields with other requirements must follow these requirements (for example Firm Number must be valid and eligible 
for Fund/SERV).  
• Optional fields means the following: 
a. Fields with specified list of values must have one of those values or space. 
b. Alphanumeric type fields without specified list of values may have any value as described in the first note above. 
c. Numeric type fields without specified list of values must be numeric or space. 
d. Fields with other requirements must follow these requirements or may be space (for example Fund Number must be 
valid and eligible for Fund/SERV or may be space)  

---

## Page 15

Variable Length Record Layouts (Part 1) 
Record Layouts 15 
 
• All dates in the layouts have the format mmddccyy (except where otherwise indicated) where: 
mm = Month 
dd = Day in month 
cc = Century 
yy = Year in century 
Example: 
May 16, 2023 is represented as: 05162023 

---

## Page 16

Variable Length Record Layouts (Part 1) 
Record Type List 16 
 
RECORD TYPE LIST 
The following are Fund/SERV record types and the section numbers where their layouts are described in this 
document: 
02.01.00 Record Type List 
Record Type  Description  Section No.  
000 [[NSCC]] Output Header 02.20.01 
001 Order  02.01.01 
002 Defined Contribution Plan Information  02.15.01 
003 Correction  02.29.01 
004 As-Of Order  02.02.01 
005 Confirmation  02.02.01 
006 Reconfirmation  02.02.01 
007 Fund Originated Order  02.02.01 
009 Fund Originated As-of Order  02.02.01 
011 Cash Adjustment  02.08.01 
015 Exchange Order  02.06.01 
016 Exchange Confirmation  02.07.01 
017 Exchange Reconfirmation  02.07.01 
018 ACATS Transfer  02.11.01 
019 ACATS Transfer Acknowledgment/Rejection  02.12.01 
021 Post [[settlement]] Exchange Cancellation  02.07.01 
025 Correction Confirmation  02.29.01 
026 Post [[settlement]] Correction by Fund  02.29.01 
030 Interval Fund Acknowledgement 02.32.01 
070 Settling Trade Detail  02.23.01 
071 Settling Trade Trailer  02.24.01 
072 X-[[settlement]] Trade Detail  02.23.01 

---

## Page 17

Variable Length Record Layouts (Part 1) 
Record Type List 17 
 
Record Type  Description  Section No.  
073 X-[[settlement]] Trade Trailer  02.24.01 
074 Settling Trade Detail for TPA/Investment Agent/TPP 02.23.01 
075 Settling Trade Trailer for TPA/Investment Agent/TPP 02.24.01 
080 Pending ACATS Transfer Acknowledgment Reminder  02.17.01 
081 Order Not Acted Upon Reminder  02.17.01 
082 Deletion of Order Not Acted Upon Reminder  02.17.01 
083 Pending Registration Reminder  02.17.01 
084 Extended Correction Transfer Not Acted Upon Reminder 02.17.01 
085 Pending Release to [[settlement]] Reminder  02.17.01 
086 Pending Correction Confirmation Reminder  02.17.01 
087 Pending Registration Acknowledgment Reminder  02.17.01 
088 Pending Exchange Reconfirmation Reminder  02.17.01 
089 Post [[settlement]] Correction/Cancellation Not Acted Upon  02.17.01 
090 Retiring Participants  02.16.01 
091 Pending ToRA Acknowledgment Reminder  02.17.01 
092 Pending ToRA Confirmation Reminder  02.17.01 
100 Fund Reject  02.05.01 
101 Order Acknowledgment for Money Market Purchase  02.04.01 
102 Firm Delete  02.04.01 
108 Fund Delete  02.05.01 
109 Release to [[settlement]]  02.04.01 
112 Registration Acknowledgment  02.04.01 
113 Delete Pending Registration (registered ex-Fund/SERV)  02.04.01 
114 Registration Rejection  02.05.01 
120 Multiple Reject Codes  02.25.01 
129 Delete Pending Release to [[settlement]] (settled ex-Fund/SERV) 02.05.01 
139 Firm Exit 02.28.01 

---

## Page 18

Variable Length Record Layouts (Part 1) 
Record Type List 18 
 
Record Type  Description  Section No.  
140 Post [[settlement]] Cancellation by fund 02.02.01 
200 Extended Correction Transfer 02.03.01 
201 Extended Correction Transfer Acknowledgment 02.03.01 
210 Transfer of Retirement [[Asset]] (ToRA) 02.13.01 
211 ToRA Acknowledgment 02.14.01 
212 ToRA Confirmation 02.14.01 
213 ToRA Reconfirmation 02.14.01 
214 Receiving Fund Exit from ToRA 02.04.01 
400 Short Registration 02.09.01 
401 Full Registration 02.10.01 
999 Trailer - Firm/TPA/Investment Agent/TPP Input 02.18.01 
999 Trailer - Fund Input 02.19.01 
999 Trailer - [[NSCC]] Output 02.21.01 
GTT Grand Total Trailer 02.22.01 

---

## Page 19

Variable Length Record Layouts (Part 1) 
Order (001) 19 
 
ORDER (001) 
02.01.01 Order (001) 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Record Length 
 
1 4 4 N With no SSN/EIN Suffix: 
0290, 0383, 0476,  
0569, 0662 
 
0569 is required when “Redemption 
F
ee Indicator” is provided, “[[Asset]] 
Type Indicator” = Q, U, V or W, or 
“Market [[Liquidity]] Fee/Redemption 
Gate Indicator” is provided.  
With SSN/EIN Suffix: 
Up to 1685  
R 152 
Physical Sequence 
Number 
5 6 2 A/N 01 R 004 
Logical Sequence 
Number 
7 8 2 A/N 01 R 004 
Originator Type 9 9 1 A/N A = Investment Agent  
B = Firm 
T = TPA 
S = Service Provider for B = Firm 
P = Service Provider for T = TPA 
V = TPP (Third Party Provider)  
R 187 
Filler  10 11 2 A/N Space  R  
Firm Number 12 15 4 N  R 008 
Filler 16 18 3 A/N Space R  
Record Type 19 21 3 A/N 001 = Order R 002 
Test Indicator 22 22 1 A/N 0 = Production 
1 = Test  
R 122 
Filler 23 23 1 A/N Space  R  
Fund Number 24 27 4 N  O 100 
Filler 28 30 3 A/N Space R  
Security Issue Country 
Code 
31 32 2 A/N Space. For future use R  
Security Issue [[ID]] 33 41 9 A/N  R 007 

---

## Page 20

Variable Length Record Layouts (Part 1) 
Order (001) 20 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Security Issue Check 
Digit 
42 42 1 A/N Space. For future use R  
Security Issue Type 43 44 2 A/N Required if 24 (Money Market) 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value against 
the Fund/SERV Security master 
file. [[NSCC]] leverages the 
Fund/SERV Security master file to 
determine value and associated 
processing rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 
OC 150 
Control Number 45 59 15 A/N  R 005 
Correction Indicator 60 60 1 A/N Space R 006 
Transaction Type 61 61 1 A/N 0 = Single purchase 
1 = Letter of intent 
2 = Rights of accumulation 
3 = Net [[Asset]] value 
4 = Group purchase 
5 = CDSC [[liquidation]] 
8 = 529 [[participant]] Distribution  
9 = 529 Beneficiary Distribution 
A = 529 School Distribution 
B = 529 Rollover Distribution 
E = 529 In-State Plan Transfer 
Distribution 
F = 529 Registration Change 
 
Only 5, 8, 9, A, B, E or F are allowed 
if Transaction Code = “03” or “04” 
03 (Partial [[liquidation]])  
04 (Full [[liquidation]]) 
R 017 

---

## Page 21

Variable Length Record Layouts (Part 1) 
Order (001) 21 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Transaction Code 
 
62 63 2 A/N 01 = Initial purchase 
02 = Subsequent purchase 
03 = Partial [[liquidation]] 
04 = Full [[liquidation]] 
 
For Security Type = 48 (Interval Fund) 
future dated orders, only 03 and 04 
are allowed. 
R 018 
Submission Date 64 71 8 N mmddccyy R 101 
Trade Date 
 
72 79 8 N mmddccyy 
Future trade date is allowed if 
Security Type = 48 (Interval Fund) 
and Transaction Code = 03 (Partial 
[[liquidation]]) or 04 (Full [[liquidation]]). 
 
Best Practice: 
Trade Date for future dated Interval 
Fund repurchase orders should be 
populated with the Repurchase 
Pricing Date communicated by the 
Fund. 
R 016 
Book/Physical Share 
Indicator 
80 80 1 A/N 0 = Book [[shares]] - firm name 
1 = Book [[shares]] - customer name 
2 = Physical [[shares]]  
3 = Both book and physical [[shares]]  
Must be 0 or 1 for Money Market 
trades 
R 015 
PI Delivery Indicator 81 81 1 A/N Required for all purchases if 
Book/Physical Share Ind = 2. 
0 = Deliver to customer 
1 = Deliver to firm 
2 = Deliver to agent for firm 
OC 039 
Filler 82 82 1 A/N Space R  

---

## Page 22

Variable Length Record Layouts (Part 1) 
Order (001) 22 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
[[settlement]] Override 
Reason Code 
83 84 2 A/N Required (but must not be 04) if 
Anticipated [[settlement]] Date is 
provided. 
01 = Wrap fee account 
02 = 401K 
03 = Other 
04 = X-[[settlement]] 
05 = Section 529 Account - Qualified 
State Tuition Program 
06 = X-[[settlement]] offshore enhanced 
(allowed for Security Types 62 and 63 
only) 
07 = Refer to [[Asset]] Type Indicator 
Must be space for settling EUR and 
GBP transactions (Security Issue 
Type 63 only). 
OC 179 
[[NSCC]] Rejection 
Indicator 
85 85 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], multiple 
errors 
R  
[[NSCC]] Reject Code 86 88 3 A/N Input: Space  
Output: Reject code 
R  
TPA/Investment 
Agent/TPP Number 
89 92 4 A/N Required if: 
Originator Type = (T or P or A or V)  
OR  
Membership Identifier = 02 or 03.  
 
If Originator Type = T or P, then [[Asset]] 
Type Indicator must be F through O 
or S or T (indicating DCC&S) 
OC 188 
Service Provider Number 93 96 4 A/N Required if Originator Type = S or P OC 215 
SSN/EIN Start Section 
Number 
97 98 2 A/N See SSN/EIN Start Section Number 
in the Introduction section. 
Required if SSN/EIN Suffix is 
provided. Not allowed otherwise.  
OC 257 
Total SSN/EIN Sections 99 100 2 N Required if SSN/EIN Suffix is 
provided. Not allowed otherwise.  
OC 258 
Filler 101 104 4 A/N Space R  

---

## Page 23

Variable Length Record Layouts (Part 1) 
Order (001) 23 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Share Quantity 105 118 14 N 9,999,999,999.9999  
Optional if full [[liquidation]];  
Not allowed if Money Amount > 0  
RC 019 
Customer Account 
Number at Firm 
119 138 20 A/N Optional if [[settlement]] Override 
Reason Code = 04, 06 OR if 
Membership Identifier is provided.  
RC 020 
Fund Account Indicator 139 139 1 A/N 0 = New account – U.S.  
1 = New account – non U.S  
2 = Existing account – U.S. 
3 = Existing account – non-U.S.  
4 = New account – U.S. Tax Resident 
Living Abroad  
5 = Existing account – U.S. Tax 
Resident Living Abroad 
R 010 
Customer Account 
Number at Fund 
140 159 20 A/N Required for all non-networked 
liquidations  
(Network Control Ind = 0 and Trans 
Code = 03 or 04)  
OC 011 

---

## Page 24

Variable Length Record Layouts (Part 1) 
Order (001) 24 
 
[[Asset]] Type Indicator 160 160 1 A/N 0 = Not applicable 
1 = Current year payment 
2 = Prior year payment 
3 = IRA rollover 
4 = [[Asset]] transfer 
5 = Employee - prior year 
6 = Employee - current year 
7 = Employer - prior year 
8 = Employer - current year 
9 = Non-fund prototype IRA 
A = Non-fund qualified plan 
C = Salary Reduction Contribution D 
= 529 Current Year Contribution  
E = UGMA account transferred to 
Section 529 Account  
F = 529 Underlying Fund Trades 
G = Share Class Conversion 
H = Health Savings Account 
I = Insurance Fund Transactions 
J = Non-Qualified Retirement Plan 
K = Qualified Retirement Plan 
L = Omnibus [[Dividend]] Reconciliation 
M = Variable Annuity 
N = Wrap Program 
O = Defined Benefit Plan 
P = 529 Previous Year Contribution 
Q = 529 Rollover Contribution  
S = Omnibus Short-Term Capital Gain 
Reconciliation 
T = Omnibus Long-Term Capital Gain 
Reconciliation 
U = 529 In-State Plan Transfer 
 Contribution 
V = 529 Owner Change 
W = 529 Beneficiary Change-  
In-Family  
Note: 
D, P, Q, U, V and W indicate Section 
529 Plan. 
R 013 

---

## Page 25

Variable Length Record Layouts (Part 1) 
Order (001) 25 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Agent for Firm Number 161 164 4 A/N Required if the Originator Type = V 
(TPP) 
OC 271 
Network Control Indicator  165 165 1 A/N 0 = Non-networked  
3 = Matrix level 3  
4 = Matrix level 4 
R 047 
Fraction Indicator 166 166 1 A/N 0 = Round up 
1 = Round down 
2 = Issue fraction 
3 = Not applicable  
R 014 
Gross [[settlement]] 
Indicator 
167 167 1 A/N 0 = Not applicable 
1 = Settle net 
2 = Settle gross  
R 094 
Transaction Received 
Time 
168 173 6 N hhmmss Eastern Time 
000000 (midnight) to 235959 
 
Required when “Money Market 
[[Liquidity]] Fee/Redemption Gate 
Indicator” = ‘F’ (Fund). 
OC 168 
Membership Identifier 174 175 2 A/N 01 = Trust [[Member]] 
02 = Networking info required for 
TPA/Investment Agent 
03 = TPP (Third Party Provider) 
O 181 Filler  176 176 1 A/N Space R  
Transaction Payment 
Type Indicator 
177 177 1 A/N Required if [[settlement]] Override 
Reason Code = 04.  
1 = Shareholder wire 
2 = Shareholder ACH 
3 = Address of Record (AOR). 
3 allowed for [[liquidation]] (Transaction 
Code = 03 or 04) only  
OC 216 
Transaction Bank 
Account Number 
178 197 20 A/N Required if Transaction Payment 
Type Indicator = 1 or 2  
OC 142 

---

## Page 26

Variable Length Record Layouts (Part 1) 
Order (001) 26 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Money Amount 198 213 16 N 99,999,999,999,999.99 
Optional for non-Money Market trades 
if full [[liquidation]]; 
Not allowed for non-Money Market 
trades if Share Quantity > 0.  
This amount will be settled by [[NSCC]] 
for Money Market purchase if no 
confirmation has been received. 
RC 019 
Currency Indicator 214 216 3 A/N  O 110 
Anticipated [[settlement]] 
Date 
217 224 8 A/N mmddccyy 
For Security Issue Type = 63, 
Required if [[settlement]] Override 
Reason Code is space  
For other Security Types:  
12. Required if [[settlement]] Override 
Reason Code is provided and is 
not 04 or 06 (x-[[settlement]]).  
13. Not allowed if [[settlement]] 
Override Reason Code = 04.  
This field should not be populated 
when Security Type = 48, and 
Transaction Code = 03 (Partial 
[[liquidation]]) or 04 (Full [[liquidation]]). If 
populated, [[NSCC]] will [[default]] the 
value to 12319999 and pass the order 
to the Fund. 
OC 180 
Branch Identification 
Number 
225 233 9 A/N Optional under the following 
conditions: 
• Membership Identifier = 01 or 02 
and Agent for Firm Number is not 
provided. 
• Originator Type = V(TPP) 
RC 035 
Related Trade Indicator 234 234 1 A/N 0 = No 
1 = Yes 
R 065 
Related Trade Identifier 235 236 2 A/N Required if Related Trade Indicator = 
1 
OC 105 
Customer Name 237 256 20 A/N  R 063 
SSN/EIN Indicator 257 257 1 A/N 0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN  
R 102 
SSN/EIN Number 258 266 9 A/N  R 103 

---

## Page 27

Variable Length Record Layouts (Part 1) 
Order (001) 27 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
[[liquidation]] Indicator 267 267 1 A/N Required if Trans Type = 5 
(CDSC [[liquidation]]) 
1 = Gross 
2 = Net 
4 = Correction 
5 = Death 
6 = Disability 
7 = Mandatory distribution 
8 = Systematic withdrawal 
9 = Defined contribution 
A = Hardship 
B = No commission paid  
C = 529 Plan-Specific 
D = 529 Plan Account - Beneficiary 
Disability 
E = 529 Plan Account – Beneficiary 
Death 
F = 529 Plan Account – Beneficiary 
Scholarship 
Notes: 
• 4 through F should apply only to 
transactions with CDSC Waivers 
• C through F should only apply to 
Section 529 plans. 
OC 046 

---

## Page 28

Variable Length Record Layouts (Part 1) 
Order (001) 28 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
NAV Reason Code  268 268 1 A/N Required if Trans Type = 3. 
0 = Other 
1 = Net [[Asset]] value transfer 
2 = Repurchase 
3 = Employee 
4 = Error correction 
5 = Wrap fee account 
6 = NAV commissionable 
7 = Commissionable defined 
contribution plan 
8 = Non-commissionable defined 
contribution plan 
9 = Section 529 Account - Qualified 
State Tuition Program 
A = [[Dividend]] reinvestment trade 
B = Trust Company NAV per 
Agreement  
C = Refer to [[Asset]] Type Indicator  
D = Deminimis Amount Processed at 
NAV  
E = Self Directed Brokerage Account 
OC 104 
State of Sale (State 
Code)  
269 270 2 A/N Required for Transaction Codes  
 
01 (Initial purchase) 
02 (Subsequent purchase) 
OC 012 
Redemption Fee 
Indicator 
 
271 271 1 A/N 0 = Short-Term Redemption (STR) 
1 = STR with CDSC 
2 = Money Market [[Liquidity]] Fee  
3 = Money Market [[Liquidity]] Fee with 
CDSC 
O 248 

---

## Page 29

Variable Length Record Layouts (Part 1) 
Order (001) 29 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Short-Term Redemption 
Fee Waiver Indicator 
272 272 1 A/N 1 = STR waiver due to correction  
2 = Death  
3 = Disability  
4 = Mandatory distribution  
5 = Systematic withdrawal  
6 = Defined contribution  
7 = Hardship  
8 = Auto Rebalance  
9 = DC – Termination Distribution  
A = DC – Involuntary Distribution  
B = DC – Forfeitures  
C = DC – Loans  
D = DC – Excess Contributions 
E = Wrap Program  
F = Fund of Funds 
G = Divorce/QDRO  
H = Plan fees QDRO 
O 249 
Filler 273 276 4 A/N Space R  
Transaction ABA Routing 
Number 
277 285 9 A/N Required if Transaction Payment 
Type Indicator = 1 or 2  
OC 141 
De-minimis repurchase 
waiver code 
 
 
286 286 1 A/N blank or 0 = No;  
1 = Yes  
 
Allows Firms to indicate if an Interval 
Fund repurchase order is eligible for 
de-minimis treatment in accordance 
with the Fund’s prospectus. 
 
Should only be populated for an 
Interval Fund. 
O 286 
Filler 287 288 2 A/N Space R  

---

## Page 30

Variable Length Record Layouts (Part 1) 
Order (001) 30 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Omnibus Account 
Indicator 
289 289 1 A/N 0 = Not Omnibus Account 
1 = Omnibus Account 
2 = Omnibus B to A Conversion 
Purchase 
3 = Omnibus B to A Conversion 
Redemption 
4 = Omnibus Cash [[Dividend]] 
Redemption 
5 = Omnibus Reinvest [[Dividend]] 
Purchase 
6 = Omnibus Cash Capital Gain 
Redemption 
7 = Omnibus Reinvest Capital Gain 
Purchase 
O 234 
Trade Date Forward 
Indicator 
290 290 1 A/N 0 = Trade Date not forwarded  
1 = Trade Date forwarded  
Must be 1 if Trade Date not equal 
Submission Date.  
 
Trade Date forwarded is only 
allowed if: 
• Security Type = 48 (Interval 
Fund) and Transaction Code = 
03 (Partial [[liquidation]]) or 04 
(Full [[liquidation]]). 
• Security Type = 62 or 63 
OC 229 
Related Account Number 291 310 20 A/N  O  
Related Account Number 
Indicator 
311 311 1 A/N Required if Related Account Number 
is provided. 
1 = Fund 
2 = Firm 
3 = Customer  
OC 157 Related Account Security 
Issue Country Code 
312 313 2 A/N Space. For future use  R  
Related Account Security 
Issue [[ID]] 
314 322 9 A/N Required if Related Account Number 
is provided 
OC 107 
Related Account Security 
Issue Check Digit 
323 323 1 A/N Space. For future use R  

---

## Page 31

Variable Length Record Layouts (Part 1) 
Order (001) 31 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Country of Origin 
(Country Code) 
324 325 2 A/N Required for non-omnibus account 
(Omnibus Account Indicator = ‘0’ or 
space) if State of Sale (State Code) = 
‘FF’ 
OC 067 
Sales Charge Rate 326 329 4 N 9.999 O 025 
ROA/LOI Value 330 345 16 N 99,999,999,999,999.99  O 064 
LOI Number/Date 346 353 8 A/N  O  
IRA/529 [[liquidation]] 
Indicator 
354 354 1 A/N 0 = Not applicable 
1 = Distribution – premature 
2 = Distribution – disability 
3 = Distribution – death 
4 = Distribution – normal 
5 = Hardship withdrawal 
6 = Loan  
7 = Rollover 
8 = Adjust prior year excess 
9 = Adjust current year excess 
A = Qualified  
B = Non-Qualified  
C = Distribution – Non-Taxable 
D = 529 Owner Change 
E = 529 Beneficiary Change – In-
Family  
Notes: 
A and B are required if Transaction 
Type =  
8 = (529 [[participant]] Distribution) 
9 = (529 Beneficiary Distribution) 
A = (529 School Distribution) 
B = (529 Roll Over Distribution) 
 
C is required if Transaction Type = E 
(529 In-State Plan Transfer 
Distribution) 
D or E is required if Transaction Type 
= F (529 Registration Change) 
OC 106 
Short [[settlement]] 
Indicator 
355 355 1 A/N 0 = Not applicable 
1 = Short due to correction  
O 169 

---

## Page 32

Variable Length Record Layouts (Part 1) 
Order (001) 32 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Periodic Frequency 
Indicator 
356 356 1 A/N Required if [[liquidation]] Indicator = 8 or 
Program Transaction Indicator = 1. 
0 = Weekly  
1 = Monthly  
2 = Bi-monthly  
3 = Quarterly  
4 = Semiannual  
5 = Annual  
6 = Non-Periodic (Ad Hoc) 
OC 083 
Shareholder Date of Birth 357 364 8 N mmddccyy  
For 529 use this field for Beneficiary 
Date of Birth 
O 204 
Social Code 365 366 2 A/N Required when “Transaction 
Code” = 01 – Initial Purchase 
 
See Social Code List at 
https://dtcclearning.com/documents/m
utual-fund-services-1/mfs-cross-
product/codes-8/2498-social-
codes/file.html under General Codes. 
OC 128 

---

## Page 33

Variable Length Record Layouts (Part 1) 
Order (001) 33 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Beneficiary SSN/EIN 
Number 
367 375 9 A/N Required if [[Asset]] Type Indicator = D, 
E, P, Q, U, V, or W and Transaction 
Code = 01 or 02 
[[Asset]] Type Indicators 
D (529 Current Year Contribution)  
E (UGMA account transferred to 
Section 529 Account)  
P (529 Previous Year Contribution) 
Q (529 Rollover Contribution)  
U (529 In-State Plan Transfer 
Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change-In-
Family)  
 
Transaction Codes 
01 (Initial purchase) 
02 (Subsequent purchase) 
OC 103 
Beneficiary SSN/EIN 
Indicator 
376 376 1 A/N Required if Beneficiary SSN/EIN 
Number is provided. 
0 = Tax [[ID]] number 
1 = Social security number 
2 = Beneficiary TIN/EIN  
OC 102 Standard [[ID]] 377 382 6 A/N  O  
Program Transaction 
Indicator 
383 383 1 A/N 1 = Systematic Withdrawal Plan 
(SWP) 
2 = Target Date Fund [[liquidation]]  
3 = Systematic Contribution 
(SIP/PAC/PIP) 
4 = Rebalance Purchase (Systematic) 
5 = Rebalance Redemption 
(Systematic) 
O 259 
Account Representative 
Number 
384 392 9 A/N  O  
Account Representative 
Name 
393 407 15 A/N  O  
Confirm Number 408 419 12 A/N  O  
Memo Field 420 431 12 A/N  O  

---

## Page 34

Variable Length Record Layouts (Part 1) 
Order (001) 34 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
IRA Withholding 
Percentage 
432 436 5 N 99.999 O 158 
Non-Taxable Percentage 437 441 5 N 99.999 O 159 
Non-Taxable Money 
Amount 
442 457 16 N 99,999,999,999,999.99  O 160 
Closeout Fee Indicator 458 458 1 A/N 0 = [[DO]] not deduct  
1 = Deduct 
O 161 
LOI Indicator 459 459 1 A/N 0 = New 
1 = Existing  
O 162 
Original Control Number 460 474 15 A/N  O  
Original Correction 
Indicator 
475 475 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] 
correction/cancellation  
Space = No correction  
P not permitted if the Security Issue 
Type field value is 63 and [[settlement]] 
Override Reason Code field value is 
space. 
OC 164 
Filler 476 476 1 A/N Space  R  
Redemption Fee Rate 477 483 7 N 99.99999 
 
Not allowed if “Redemption Fee 
Indicator” is not provided. 
 
Required when “Redemption Fee 
Indicator” is populated with either ‘2’ 
(Money Market [[Liquidity]] Fee) or ‘3’ 
(Money Market [[Liquidity]] Fee with 
CDSC). 
Zero value is not allowed when this 
field is required and “Redemption Fee 
Indicator” = ‘2’ or ‘3’.  
 
If “Redemption Fee Indicator” = ‘0’ or 
‘1’, this field will be utilized to 
communicate a Short-Term 
Redemption (STR) Fee Rate. 
OC 250 

---

## Page 35

Variable Length Record Layouts (Part 1) 
Order (001) 35 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
STR Fee Share Quantity 484 497 14 N 9,999,999,999.9999 
 
Required when “Redemption Fee 
Indicator” is provided and 
“Redemption Fee Money Amount” = 0 
or Space. 
Not allowed if “Redemption Fee 
Indicator” is not provided or if 
“Redemption Fee Money Amount” > 
0. 
 
Not allowed when “Redemption Fee 
Indicator” is populated with either ‘2’ 
(Money Market [[Liquidity]] Fee) or ‘3’ 
(Money Market [[Liquidity]] Fee with 
CDSC).  
OC 251 
Redemption Fee Money 
Amount  
498 513 16 N 99,999,999,999,999.99 
 
Required when “Redemption Fee 
Indicator” is provided and “STR Fee 
Share Quantity” = 0 or Space. 
 
Not allowed if “Redemption Fee 
Indicator” is not provided or if “STR 
Fee Share Quantity” > 0. 
 
Required when “Redemption Fee 
Indicator” is populated with either ‘2’ 
(Money Market [[Liquidity]] Fee) or ‘3’ 
(Money Market [[Liquidity]] Fee with 
CDSC). 
Zero value is not allowed when this 
field is required. 
 
If “Redemption Fee Indicator” = ‘0’ or 
‘1’, this field will be utilized to 
communicate a Short-Term 
Redemption (STR) Fee Money 
Amount. 
OC 252 

---

## Page 36

Variable Length Record Layouts (Part 1) 
Order (001) 36 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Cost Basis Money 
Amount 
514 529 16 N Required if the [[Asset]] Type Indicator = 
Q, U, V or W. 
Q (529 Rollover Contribution)  
U (529 In-State Plan Transfer 
 Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change-  
In-Family)  
Format: 
99,999,999,999,999.99  
Zeros are allowed 
OC 261 
Earnings to Date Money 
Amount 
530 545 16 N Required if the [[Asset]] Type Indicator = 
Q. U, V or W. 
Q (529 Rollover Contribution)  
U (529 In-State Plan Transfer 
 Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change-  
In-Family)  
Format: 
99,999,999,999,999.99 
Zeros are allowed 
OC 262 
Negative Earnings to 
Date Indicator 
546 546 1 A/N N = Negative  
Spaces = Positive  
O 263 
Money Market [[Liquidity]] 
Fee/Redemption Gate 
Indicator  
547 547 1 A/N F = Fund.  
B = [[intermediary]] 
O 282 
Transaction Received 
Date  
548 555 8 A/N mmddccyy 
 
Required if the “Money Market 
[[Liquidity]] Fee/Redemption Gate 
Indicator” = F. 
OC 283 

---

## Page 37

Variable Length Record Layouts (Part 1) 
Order (001) 37 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Aggregated Order 
Indicator  
556 556 1 A/N Required if the “Money Market 
[[Liquidity]] Fee/Redemption Gate 
Indicator” = “F” or “B”. 
1 = Transactions are not aggregated  
2 = Transactions are aggregated by 
“like” orders (purchases separate 
from redemptions) 
3 = Transactions are net of purchases 
and redemptions 
4 = Unknown at time of placement 
OC 284 
Filler 557 569 13 A/N Space R  
[[intermediary]] Program  
Indicator – 1 
 
 
570 573 4 A/N Indicates the program, platform, or 
channel applicable to an account.  
Examples may include: 
• Program indicator for advisory 
accounts 
• Distribution channel applicable to 
the account (e.g., retail, RIA, etc.) 
• Retirement platform pertaining to 
the account 
Values are uniquely defined by each 
[[intermediary]]. 
O  
[[intermediary]] Program  
Indicator – 2 
 
574 577 4 A/N Further defines the program, platform, 
or channel applicable to an account.  
Values are uniquely defined by each 
[[intermediary]]. 
O  
Servicing Group [[ID]] 
 
 
578 586 9 A/N This field is used to communicate 
aggregated servicing relationships, or 
define additional relationships on 
accounts.  
Examples may include: 
• Consolidating (Super) Branches 
• Third-party administrators (TPAs) 
• Investment Advisers 
• Consultants 
This field does not replace the main 
branch field on the account. 
Values are uniquely defined by each 
[[intermediary]]. 
O  
Additional Relationship 
[[ID]] – 1 
 
 
587 606 20 A/N This field is used to communicate 
additional relationship details to 
further define servicing relationships 
between accounts. 
Values are uniquely defined by each 
[[intermediary]].  
O  

---

## Page 38

Variable Length Record Layouts (Part 1) 
Order (001) 38 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Additional Relationship 
[[ID]] – 2 
 
607 626 20 A/N This field is used to communicate 
additional relationship details to 
further define servicing relationships 
between accounts. 
Values are uniquely defined by each 
[[intermediary]]. 
O  
Filler 627 662 36 A/N Space R  

---

## Page 39

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 39 
 
AS-OF ORDER (004); CONFIRMATION (005); 
RECONFIRMATION (006); FUND ORIGINATED ORDER 
(007); FUND ORIGINATED AS-OF ORDER (009); POST 
[[settlement]] CANCELLATION BY FUND (140) 
02.02.01 As-of Order (004) 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Record Length 
 
 
1 4 4 N For record type 004 With no SSN/EIN 
Suffix: 
0290, 0383, 0476, 0569, 0662, 0755 
 
For record type 004 With SSN /EIN 
Suffix: 
Up to 1778  
For all other record types: 
0569, 0662, 0755 
 
0662 is required under the following 
conditions: 
• Redemption Fee Indicator is 
provided.  
• [[Asset]] Type is Q, U, V, or W 
(Optional for all other [[Asset]] Types. 
• Money Market [[Liquidity]] 
Fee/Redemption Gate Indicator is 
provided. 
0755 is required if [[intermediary]] Program 
Indicator, Servicing Group, and 
Additional Relationship information is 
provided. 
R 152 
Physical Sequence 
Number 
5 6 2 A/N 01 R 004 
Logical Sequence 
Number 
7 8 2 A/N 01 R 004 
Originator Type 9 9 1 A/N A = Investment Agent  
B = Firm 
F = Fund 
T = TPA  
V = TPP (Third Party Provider) 
R 187 
Filler  10 11 2 A/N Space  R  

---

## Page 40

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 40 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Firm Number 12 15 4 N  R 008 
Filler 16 18 3 A/N Space  R  
Record Type 19 21 3 A/N 004 = As-Of Order 
005 = Confirmation 
006 = Reconfirmation 
007 = Fund Originated Order 
009 = Fund Originated As-Of Order 
140 = Post [[settlement]] Cancellation by 
fund  
Record Type 140 not permitted if the 
Security Issue Type field value is 63 and 
[[settlement]] Override Reason Code field 
value is space. 
RC 002/275 
Test Indicator 22 22 1 A/N 0 = Production  
1 = Test  
R 122 
Filler 23 23 1 A/N Space R  
Fund Number 24 27 4 N  O 100 
Filler 28 30 3 A/N Space R  
Security Issue Country 
Code 
31 32 2 A/N Space. For future use R  
Security Issue [[ID]] 33 41 9 A/N  R 007 
Security Issue Check 
Digit 
42 42 1 A/N Space. For future use R  
Security Issue Type 43 44 2 A/N Required if 24 (Money Market) 
Notes: 
Input: With the exception of Security 
Issue Type = 24, [[NSCC]] does not 
validate the value against the 
Fund/SERV Security master file. 
[[NSCC]] leverages the Fund/SERV 
Security master file to determine 
value and associated processing 
rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 
OC 150 
Control Number 45 59 15 A/N  R 005 

---

## Page 41

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 41 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Correction Indicator 60 60 1 A/N Required for record type 140.  
Required for record type 005 if 
confirming post [[settlement]] cancellation.  
Not allowed otherwise. 
P = Post [[settlement]] cancellation 
P not permitted if the Security Issue 
Type field value is 63 and [[settlement]] 
Override Reason Code field value is 
space. 
OC 006 
Transaction Type 61 61 1 A/N 0 = Single purchase 
1 = Letter of intent 
2 = Rights of accumulation 
3 = Net [[Asset]] value 
4 = Group purchase 
5 = CDSC [[liquidation]] 
8 = 529 [[participant]] Distribution  
9 = 529 Beneficiary Distribution 
A = 529 School Distribution 
B = 529 Rollover Distribution 
E = 529 In-State Plan Transfer 
Distribution  
F = 529 Registration Change 
 
Only 5, 8, 9, A, B, E or F are allowed if 
Transaction Code = “03” or “04” 
03 (Partial [[liquidation]])  
04 (Full [[liquidation]]) 
R 017 

---

## Page 42

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 42 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Transaction Code 
 
 
62 63 2 A/N 01 = Initial purchase 
02 = Subsequent purchase 
03 = Partial [[liquidation]] 
04 = Full [[liquidation]] 
07 = Post [[settlement]] cancellation 
purchase 
08 = Post [[settlement]] cancellation 
[[liquidation]]. 
Must be 03 or 04 or 08 if Transaction 
Type = 5. 
07 and 08 allowed only if Correction 
Indicator = P. 
07 and 08 not permitted if the Security 
Issue Type field value is 63 and 
[[settlement]] Override Reason Code field 
value is space. 
 
For record types 005,006 
For Security Type = 48 (Interval Fund) 
future dated orders, only 03 and 04 are 
allowed. 
RC 018 
Submission Date 64 71 8 N mmddccyy  R 101 
Trade Date 
 
 
72 79 8 N mmddccyy 
 
For record types 005,006 
Future trade date is allowed if Security 
Type = 48 (Interval Fund) and 
Transaction Code = 03 (Partial 
[[liquidation]]) or 04 (Full [[liquidation]]). 
 
Best Practice: 
Trade Date for future dated Interval 
Fund repurchase orders should be 
populated with the Repurchase Pricing 
Date communicated by the Fund. 
R 016 
Book/Physical Share 
Indicator 
80 80 1 A/N 0 = Book [[shares]] - firm name 
1 = Book [[shares]] - customer name 
2 = Physical [[shares]] 
3 = Both book and physical [[shares]] 
Must be 0 or 1 for Money Market trades  
RC 015 

---

## Page 43

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 43 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
PI Delivery Indicator 81 81 1 A/N Required for all purchases if 
Book/Physical Share Ind = 2. 
0 = Deliver to customer 
1 = Deliver to firm 
2 = Deliver to agent for firm 
OC 039 
Filler 82 82 1 A/N Space R  
[[settlement]] Override 
Reason Code 
83 84 2 A/N Required (but must not be 04) if 
Anticipated [[settlement]] Date is provided.  
01 = Wrap fee account  
02 = 401K  
03 = Other  
04 = X-[[settlement]]  
05 = Section 529 Account - Qualified 
State Tuition Program  
06 = X-[[settlement]] offshore enhanced 
(allowed for Security Types 62 and 63 
only)  
07 = Refer to [[Asset]] Type Indicator 
Must be space for settling EUR and 
GBP transactions (Security Issue Type 
63 only). 
OC 179 
[[NSCC]] Rejection 
Indicator 
81 81 1 A/N Input: Space  
Output: 
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]]  
2 = Rejected by [[NSCC]], multiple errors 
R  
[[NSCC]] Reject Code 86 88 3 A/N Input: Space  
Output: Reject code 
R  
TPA/Investment 
Agent/TPP Number  
 
89 92 4 A/N Required if: 
Originator Type (T or A or V) 
OR 
Membership Identifier = 02 or 03. 
If Originator Type = T or P, then [[Asset]] 
Type Indicator must be F through O or S 
or T (indicating DCC&S). 
OC 188 
Service Provider 
Number 
93 96 4 A/N  O 215 

---

## Page 44

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 44 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
SSN/EIN Start Section 
Number 
97 98 2 A/N See SSN/EIN Start Section Number in 
the Introduction section. 
Required if SSN/EIN Suffix is provided. 
Not allowed otherwise.  
OC 257 
Total SSN/EIN Sections 99 100 2 N Required if SSN/EIN Suffix is provided. 
Not allowed otherwise. 
OC 258 
Filler 101 104 4 A/N Space R  
Share Quantity 105 118 14 N 9,999,999,999.9999  
Optional for record type 004 if full 
[[liquidation]]; 
Not allowed for record type 004 if Money 
Amount > 0 
RC 019 
Customer Account 
Number at Firm 
119 138 20 A/N Optional if [[settlement]] Override Reason 
Code = 04, 06 OR if Membership 
Identifier is provided.  
RC 020 
Fund Account Indicator 139 139 1 A/N 0 = New account – U.S. 
1 = New account – non-U.S.  
2 = Existing account – U.S. 
3 = Existing account – non-U.S.  
4 = New account – U.S. Tax Resident 
Living Abroad  
5 = Existing account – U.S. Tax 
Resident Living Abroad 
R 010 
Customer Account 
Number at Fund 
140 159 20 A/N Required for all non-networked 
liquidations (Network Control Ind = 0 
and Trans Code = 03, 04 or 08)  
OC 011 

---

## Page 45

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 45 
 
[[Asset]] Type Indicator 160 160 1 A/N 0 = Not applicable 
1 = Current year payment 
2 = Prior year payment 
3 = IRA rollover 
4 = [[Asset]] transfer 
5 = Employee - prior year 
6 = Employee - current year 
7 = Employer - prior year 
8 = Employer - current year 
9 = Non-fund prototype IRA 
A = Non-fund qualified plan 
C = Salary Reduction Contribution  
D = 529 Current Year Contribution  
E = UGMA account transferred to 
Section 529 Account  
F = 529 Underlying Fund Trades 
G = Share Class Conversion 
H = Health Savings Account 
I = Insurance Fund Transactions 
J = Non-Qualified Retirement Plan 
K = Qualified Retirement Plan 
L = Omnibus [[Dividend]] Reconciliation 
M = Variable Annuity 
N = Wrap Program 
O = Defined Benefit Plan 
P = 529 Previous Year Contribution 
Q = 529 Rollover Contribution  
S = Omnibus Short-Term Capital Gain 
Reconciliation 
T = Omnibus Long-Term Capital Gain 
Reconciliation 
U = 529 In-State Plan Transfer 
Contribution 
V = 529 Owner Change 
W = 529 Beneficiary Change-  
In-Family  
Note: 
D, P, Q, U, V and W indicate Section 
529 Plan. 
R 013 
Agent for Firm Number 161 164 4 A/N Required if Originator Type = V (TPP) OC 271 

---

## Page 46

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 46 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Network Control 
Indicator  
165 165 1 A/N 0 = Non-networked  
3 = Matrix level 3  
4 = Matrix level 4 
R 047 
Fraction Indicator 166 166 1 A/N 0 = Round up 
1 = Round down 
2 = Issue fraction 
3 = Not applicable  
R 014 
Gross [[settlement]] 
Indicator 
167 167 1 A/N 0 = Not applicable 
1 = Settle net 
2 = Settle gross 
R 094 
Transaction Received 
Time 
168 173 6 N hhmmss Eastern Time 
000000 (midnight) to 235959 
 
Required when “Money Market [[Liquidity]] 
Fee/Redemption Gate Indicator” = ‘F’ 
(Fund). 
 
For Record Types 005 and 006: 
Must contain the same value as 
provided by the firm on the Order 
transaction (record type 001or 004). 
[[NSCC]] will reject if a fund provided value 
is different from the value submitted by 
the firm. 
OC 168 
Membership Identifier 174 175 2 A/N 01 = Trust [[Member]] 
02 = Networking info required for 
TPA/Investment Agent 
03 = TPP (Third Party Provider) 
O 181 
Filler 176 176 1 A/N  R  
Transaction Payment 
Type Indicator 
177 177 1 A/N Required if [[settlement]] Override Reason 
Code = 04. 
1 = Shareholder wire 
2 = Shareholder ACH 
3 = Address of Record (AOR). 
3 allowed for [[liquidation]] (Transaction 
Code = 03 or 04) only  
OC 216 
Transaction Bank 
Account Number  
178 197 20 A/N Required if Transaction Payment Type 
Indicator = 1 or 2  
OC 142 

---

## Page 47

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 47 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Money Amount 198 213 16 N 99,999,999,999,999.99  
Optional for record type 004 if full 
[[liquidation]];  
Not allowed for record type 004 if Share 
Quantity > 0  
RC 019 
Currency Indicator 214 216 3 A/N  O 110 
Anticipated [[settlement]] 
Date 
217 224 8 A/N mmddccyy  
For Security Issue Type = 63, Required 
if [[settlement]] Override Reason Code is 
space . 
For other Security Types:  
1. Required if [[settlement]] Override 
Reason Code is provided and is 
not 04 or 06 (x-[[settlement]] 
domestic).  
2. Not allowed if [[settlement]] Override 
Reason Code = 04.  
OC 180 
Branch Identification 
Number 
225 233 9 A/N Optional under the following conditions: 
• Membership Identifier = 01 or 02 and 
Agent for Firm Number is not 
provided. 
• Originator Type = V(TPP) 
RC 035 
Related Trade Indicator 234 234 1 A/N 0 = No 
1 = Yes 
R 065 
Related Trade Identifier 235 236 2 A/N Required if Related Trade Indicator = 1 OC 105 
Customer Name 237 256 20 A/N  R 063 
SSN/EIN Indicator 257 257 1 A/N 0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN  
R 102 
SSN/EIN Number 258 266 9 A/N  R 103 

---

## Page 48

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 48 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
[[liquidation]] Indicator 
 
267 267 1 A/N Required if Trans Type = 5. 
1 = Gross 
2 = Net 
4 = Correction  
5 = Death 
6 = Disability 
7 = Mandatory distribution 
8 = Systematic withdrawal 
9 = Defined contribution 
A = Hardship 
B = No commission paid  
C = 529 Plan-Specific 
D = 529 Plan Account - Beneficiary 
Disability 
E = 529 Plan Account – Beneficiary 
Death 
F = 529 Plan Account – Beneficiary 
Scholarship 
Notes: 
• 4 through F should apply only to 
transactions with CDSC Waivers 
• C through F should only apply to 
Section 529 plans. 
OC 046 

---

## Page 49

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 49 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
NAV Reason Code  268 268 1 A/N Required if Trans Type = 3. 
0 = Other 
1 = Net [[Asset]] value transfer 
2 = Repurchase 
3 = Employee 
4 = Error correction 
5 = Wrap fee account 
6 = NAV commissionable 
7 = Commissionable defined 
contribution plan 
8 = Non-commissionable defined 
contribution plan  
9 = Section 529 Account - Qualified 
State Tuition Program 
A = [[Dividend]] reinvestment trade 
B = Trust Company NAV per Agreement  
C = Refer to [[Asset]] Type Indicator  
D = Deminimis Amount Processed at 
NAV  
E = Self Directed Brokerage Account 
OC 104 
State of Sale (State 
Code)  
269 270 2 A/N Required for Transaction Codes  
 
01 (Initial purchase) 
02 (Subsequent purchase) 
OC 012 
Redemption Fee 
Indicator 
271 271 1 A/N 0 = Short-Term Redemption (STR) 
1 = STR with CDSC 
2 = Money Market [[Liquidity]] Fee  
3 = Money Market [[Liquidity]] Fee with 
CDSC 
 
Values “0” and “1” are not allowed for 
record types 005 and 006 if this field 
was blank on the original Order 
transaction (record type 001 or 004). 
 
Values “2” and “3” are allowed for record 
types 005 and 006 if this field was blank 
on the original Order transaction (record 
type 001 or 004). 
 
Not allowed for record type 007 and 009. 
O 248 

---

## Page 50

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 50 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Short-Term Redemption 
Fee Waiver Indicator 
272 272 1 A/N 1 = STR waiver due to correction  
2 = Death  
3 = Disability  
4 = Mandatory distribution  
5 = Systematic withdrawal  
6 = Defined contribution  
7 = Hardship  
8 = Auto Rebalance  
9 = DC – Termination Distribution  
A = DC – Involuntary Distribution  
B = DC – Forfeitures  
C = DC – Loans  
D = DC – Excess Contributions 
E = Wrap Program  
F = Fund of Funds 
G = Divorce/QDRO  
H = Plan fees QDRO 
O 249 
Filler  273 273 1 A/N Space  R  
As-Of Indicator 274 274 1 A/N Required for record type 004. 
0 = Not applicable 
1 = Correction only 
2 = Correction 
3 = Rebill  
OC 108 

---

## Page 51

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 51 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
As-Of Reason Code 275 276 2 A/N Required for record type 004.  
01 = Incorrect Firm/Fund Account 
Number  
02 = Incorrect Share Quantity/Dollar 
Quantity  
03 = Incorrect security issue [[ID]] 
04 = Customer renege  
05 = Incorrect Sales Charge Breakpoint  
07 = Blue sky violation  
09 = Delay in Firm Trade Transmission 
10 = With Fund’s Permission 
11 = Resubmitted Fund/SERV Reject 
12 = DCC&S (see [[Asset]] Type Indicator) 
13 = Distribution Reversal 
14 = Prospectus Violation 
Note: 
The values ‘00’, ‘06’ and ‘08’ have been 
removed. 
OC 109 
Transaction ABA 
Routing Number 
277 285 9 A/N Required if Transaction Payment Type 
Indicator = 1 or 2 
OC 141 
Filler 286 288 3 A/N Space  R  
Omnibus Account 
Indicator 
289 289 1 A/N 0 = Not Omnibus Account 
1 = Omnibus Account 
2 = Omnibus B to A Conversion 
Purchase 
3 = Omnibus B to A Conversion 
Redemption 
4 = Omnibus Cash [[Dividend]] 
Redemption 
5 = Omnibus Reinvest [[Dividend]] 
Purchase 
6 = Omnibus Cash Capital Gain 
Redemption 
7 = Omnibus Reinvest Capital Gain 
Purchase  
O 234 

---

## Page 52

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 52 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Trade Date Forward 
Indicator 
290 290 1 A/N 0 = Trade Date not forwarded 
1 = Trade Date forwarded 
 
For record types 005 and 006: 
‒ Must be same as on original order  
‒ Trade Date forwarded is only 
allowed if: 
• Security Type = 48 (Interval Fund) 
and Transaction Code = 03 
(Partial [[liquidation]]) or 04 (Full 
[[liquidation]]). 
• Security Type = 62 or 63 
OC 229 
Related Account 
Number  
291 310 20 A/N  O  
Related Account 
Number Indicator 
311 311 1 A/N Required if Related Account Number is 
provided.  
1 = Fund 
2 = Firm  
3 = Customer 
OC 157 Related Account 
Security Issue Country 
Code  
312 313 2 A/N Space. For future use  R  
Related Account 
Security Issue [[ID]]  
314 322 9 A/N Required if Related Account Number is 
provided  
OC 107 
Related Account 
Security Issue Check 
Digit 
323 323 1 A/N Space. For future use  R  
Country of Origin 
(Country Code)  
324 325 2 A/N Required for non-omnibus account 
(Omnibus Account Indicator = ‘0’ or 
space) if State of Sale (State Code) = 
‘FF’  
OC 067 
Sales Charge Rate 326 329 4 N 9.999 
Must be provided (but allowed to be 
zero) for purchase (Transaction Code = 
'01', '02' or '07') if Load Type Indicator = 
1.  
OC 025 
ROA/LOI Value 330 345 16 N 99,999,999,999,999.99  O 064 
LOI Number/Date 346 353 8 A/N  O  

---

## Page 53

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 53 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
IRA/529 [[liquidation]] 
Indicator 
354 354 1 A/N 0 = Not applicable 
1 = Distribution – premature 
2 = Distribution – disability 
3 = Distribution – death 
4 = Distribution – normal 
5 = Hardship withdrawal 
6 = Loan  
7 = Rollover 
8 = Adjust prior year excess 
9 = Adjust current year excess 
A = Qualified  
B = Non-Qualified  
C = Distribution – Non-Taxable 
D = 529 Owner Change 
E = 529 Beneficiary Change – In-Family  
Notes: 
A and B are required if Transaction Type 
=  
8 = (529 [[participant]] Distribution) 
9 = (529 Beneficiary Distribution) 
A = (529 School Distribution) 
B = (529 Roll Over Distribution 
 
C is required if Transaction Type = E 
(529 In-State Plan Transfer Distribution) 
D or E is required if Transaction Type = 
F (529 Registration Change) 
OC 106 
Short [[settlement]] 
Indicator  
355 355 1 A/N 0 = Not applicable 
1 = Short due to correction  
O 169 
Periodic Frequency 
Indicator 
356 356 1 A/N Required if [[liquidation]] Indicator = 8 or 
Program Transaction Indicator = 1. 
0 = Weekly  
1 = Monthly  
2 = Bi-monthly  
3 = Quarterly  
4 = Semiannual  
5 = Annual  
6 = Non-Periodic (Ad Hoc) 
OC 083 

---

## Page 54

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 54 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Shareholder Date of 
Birth  
357 364 8 N mmddccyy  
For 529 use this field for Beneficiary 
Date of Birth  
O 204 
Social Code 365 366 2 A/N Required when: 
- “Transaction 
Code”= 01 – Initial Purchase AND 
-“Record Type” is one of the following: 
• 004 – As-of Order 
• 005 – Confirmation 
• 006 – Reconfirmation 
See Social Code List at 
https://dtcclearning.com/documents/mut
ual-fund-services-1/mfs-cross-
product/codes-8/2498-social-
codes/file.html under General Codes. 
OC 128 
Beneficiary SSN/EIN 
Number 
367 375 9 A/N Required if [[Asset]] Type Indicator = D, E, 
P, Q U, V, or W and Transaction Code = 
01 or 02 
[[Asset]] Type Indicators 
D (529 Current Year Contribution)  
E (UGMA account transferred to Section 
529 Account)  
P (529 Previous Year Contribution) 
Q (529 Rollover Contribution)  
U (529 In-State Plan Transfer 
Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change-In-Family) 
 
Transaction Codes 
01 (Initial purchase) 
02 (Subsequent purchase) 
OC 103 
Beneficiary SSN/EIN 
Indicator 
376 376 1 A/N Required if Beneficiary SSN/EIN 
Number is provided. 
0 = Tax [[ID]] number 
1 = Social security number 
2 = Beneficiary TIN/EIN  
OC 102 Standard [[ID]] 377 382 6 A/N  O  

---

## Page 55

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 55 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Program Transaction 
Indicator 
383 383 1 A/N 1 = Systematic Withdrawal Plan (SWP) 
2 = Target Date Fund [[liquidation]]  
3 = Systematic Contribution 
(SIP/PAC/PIP) 
4 = Rebalance Purchase (Systematic) 
5 = Rebalance Redemption (Systematic) 
O 259 
Account Representative 
Number 
384 392 9 A/N  O  
Account Representative 
Name 
393 407 15 A/N  O  
Confirm Number 408 419 12 A/N   O  
Memo Field 420 431 12 A/N   O  
IRA Withholding 
Percentage 
432 436 5 N 99.999  O 158 
Non-Taxable 
Percentage 
437 441 5 N 99.999  O 159 
Non-Taxable Money 
Amount 
442 457 16 N 99,999,999,999,999.99  O 160 
Closeout Fee Indicator 458 458 1 A/N 0 = [[DO]] not deduct 
1 = Deduct 
O 161 
LOI Indicator 459 459 1 A/N 0 = New 
1 = Existing  
O 162 
Original Control 
Number 
460 474 15 A/N  O  
Original Correction 
Indicator  
475 475 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] 
correction/cancellation 
Space = No correction  
P not permitted if the Security Issue 
Type field value is 63 and [[settlement]] 
Override Reason Code field value is 
space. 
O 164 
Filler 476 476 1 A/N Space R  
Withholding Amount 477 492 16 N 99,999,999,999,999.99  O 113 

---

## Page 56

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 56 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Withholding Type  493 493 1 A/N Required if Withholding Amount > 0. 
1 = Tefra backup 
2 = Tefra pension 
3 = Foreign withholding 
OC 114 
Fee Amount 494 501 8 N 999,999.99  O 115 
Fee Type 502 502 1 A/N Required if Fee Amount > 0. 
1 = [[liquidation]] fee  
2 = Other  
OC 116 
Amount Due 503 518 16 N 99,999,999,999,999.99  
Optional for record type 004.  
This amount will be settled by [[NSCC]]  
RC 026 
Price Per Share 519 530 12 N 999,999.999999  
Optional for record type 004  
RC 027 
Loss/Gain Amount 531 538 8 N 999,999.99  O 031 
Loss/Gain Indicator 539 539 1 A/N Required if Loss/Gain Amount > 0.  
0 = Loss 
1 = Gain 
OC 117 
Firm Concession 540 548 9 N 9,999,999.99  O 044 
Accrual Amount 549 564 16 N 99,999,999,999,999.99  O 111 
Accrual Indicator 565 565 1 A/N Required if Accrual Amount > 0.  
0 = Included in Amount Due 
1 = Paid via Cash Adjustment 
2 = Paid outside system  
OC 112 
Debit/Credit Indicator 566 567 2 A/N Required if Correction Indicator = P. Not 
allowed otherwise. 
DB = Debit firm 
CR = Credit firm 
[[NSCC]] will settle Amount Due according 
to this indicator rather than Transaction 
Code.  
OC 034 

---

## Page 57

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 57 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Breakpoint Change 
Reason Code 
568 568 1 A/N 1 = ROA value at fund 
2 = LOI at fund  
3 = The higher of cost or market value at 
fund 
4 = Jumbo Pricing 
5 = Wrap Account 
6 = NAV Account 
7 = Amount Processed at NAV  
O 246 
Load Type Indicator 569 569 1 A/N 0 = Other 
1 = Front-End Load 
Required (except for record type 004) for 
purchase (Transaction Code = ‘01’, ‘02’ 
or ’07’). 
OC 247 
Redemption Fee Rate 570 576 7 N 99.99999  
 
Not allowed if “Redemption Fee 
Indicator” is not provided. 
 
Required when “Redemption Fee 
Indicator” is populated with either ‘2’ 
(Money Market [[Liquidity]] Fee) or ‘3’ 
(Money Market [[Liquidity]] Fee with 
CDSC). 
 
Zero value is not allowed when this field 
is required and “Redemption Fee 
Indicator” =2 or 3. 
 
If “Redemption Fee Indicator” = 0 or 1, 
this field will be utilized to communicate 
a Short-Term Redemption (STR) Fee 
Rate. 
OC 250 

---

## Page 58

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 58 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
STR Fee Share 
Quantity  
577 590 14 N 9,999,999,999.9999 
 
For all record types: 
Not allowed if “Redemption Fee 
Indicator” is not provided. 
 
For record type 004: 
Required when “Redemption Fee 
Indicator” is provided and “Redemption 
Fee Money Amount” = 0 or Space. 
Not allowed if “Redemption Fee Money 
Amount” > 0 
 
For record types 005 and 006: 
If zero or Space, and “Redemption Fee 
Indicator” is provided, will not override 
the “STR Fee Share Quantity” in the 
database. 
 
For all record types 
Not allowed when “Redemption Fee 
Indicator” is populated with either ‘2’ 
(Money Market [[Liquidity]] Fee) or ‘3’ 
(Money Market [[Liquidity]] Fee with 
CDSC). 
OC 251 

---

## Page 59

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 59 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Redemption Fee Money 
Amount  
591 606 16 N 99,999,999,999,999.99 
 
For all record types: 
Not allowed if “Redemption Fee 
Indicator” is not provided. 
Required when “Redemption Fee 
Indicator” is populated with either ‘2’ 
(Money Market [[Liquidity]] Fee) or ‘3’ 
(Money Market [[Liquidity]] Fee with 
CDSC).  
Zero value is not allowed when this field 
is required. 
 
For record type 004: 
Required when “Redemption Fee 
Indicator” is provided and “STR Fee 
Share Quantity” = 0 or Space. 
Not allowed if “STR Fee Share Quantity” 
> 0 
 
For record types 005 and 006: 
Required when “Redemption Fee 
Indicator” is provided. 
 
For all record types: 
If “Redemption Fee Indicator” = 0 or 1, 
this field will be utilized to communicate 
a Short-Term Redemption (STR) Fee 
Money Amount. 
OC 252 
Cost Basis Money 
Amount 
607 622 16 N Required if the [[Asset]] Type Indicator = 
Q, U, V or W. 
Q (529 Rollover Contribution) 
U (529 In-State Plan Transfer 
Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change-In-Family)  
Format: 
99,999,999,999,999.99 
Zeros are allowed 
OC 261 

---

## Page 60

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 60 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Earnings to Date Money 
Amount 
623 638 16 N Required if the [[Asset]] Type Indicator = 
Q, U, V or W. 
Q (529 Rollover Contribution) 
U (529 In-State Plan Transfer 
Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change-In-Family)  
Format: 
99,999,999,999,999.99 
Zeros are allowed 
OC 262 
Negative Earnings to 
Date Indicator 
639 639 1 A/N N = Negative  
Spaces = Positive  
O 263 
Money Market [[Liquidity]] 
Fee/Redemption Gate 
Indicator  
640 640 1 A/N F = Fund.  
B = [[intermediary]] 
 
For Record Types 005 & 006: Must 
contain the same value as provided on 
the Order transaction (001, 004).  
[[NSCC]] will reject if a fund provided value 
is different from the value submitted by 
the firm. 
 
Not allowed for record types 007 and 
009. 
O 282 
Transaction Received 
Date 
641 648 8 A/N mmddccyy 
 
Required if the “Money Market [[Liquidity]] 
Fee/Redemption Gate Indicator” = “F”. 
 
For Record Types 005 & 006: Must 
contain the same value as provided on 
the Order transaction (001, 004).  
[[NSCC]] will reject if a fund provided value 
is different from the value submitted by 
the firm. 
 
Not allowed for record types 007 and 
009. 
OC 283 

---

## Page 61

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 61 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Aggregated Order 
Indicator  
649 649 1 A/N Required if the “Money Market [[Liquidity]] 
Fee/Redemption Gate Indicator” = “F” or 
“B”. 
• 1 = Transactions are not aggregated  
• 2 = Transactions are aggregated by 
“like” orders (purchases separate 
from redemptions) 
• 3 = Transactions are net of 
purchases and redemptions 
• 4 = Unknown at time of placement 
 
For Record Types 005 & 006 
Must contain the same value as 
provided on the Order transaction (001, 
004).  
[[NSCC]] will reject if a fund provided value 
is different from the value submitted by 
the firm. 
 
Not allowed for record types 007 and 
009. 
OC 284 
Filler  650 662 13 A/N Space R  
[[intermediary]] Program 
Indicator – 1 
 
 
663 666 4 A/N Indicates the program, platform, or 
channel applicable to an account.  
 
Examples may include: 
• Program indicator for advisory 
accounts 
• Distribution channel applicable to the 
account (e.g., retail, RIA, etc.) 
• Retirement platform pertaining to the 
account 
Values are uniquely defined by each 
[[intermediary]]. 
O  
[[intermediary]] Program 
Indicator – 2 
 
 
667 670 4 A/N Further defines the program, platform, or 
channel applicable to an account. 
 
Values are uniquely defined by each 
[[intermediary]]. 
O  

---

## Page 62

Variable Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 62 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Servicing Group [[ID]] 
 
 
671 679 9 A/N This field is used to communicate 
aggregated servicing relationships, or 
define additional relationships on 
accounts. 
 
Examples may include: 
• Consolidating (Super) Branches 
• Third-party administrators (TPAs) 
• Investment Advisers 
• Consultants 
This field does not replace the main 
branch field on the account. 
 
Values are uniquely defined by each 
[[intermediary]]. 
O  
Additional Relationship 
[[ID]] – 1 
 
680 699 20 A/N This field is used to communicate 
additional relationship details to further 
define servicing relationships between 
accounts. 
 
Values are uniquely defined by each 
[[intermediary]].  
O  
Additional Relationship 
[[ID]] – 2 
 
 
700 719 20 A/N This field is used to communicate 
additional relationship details to further 
define servicing relationships between 
accounts. 
 
Values are uniquely defined by each 
[[intermediary]]. 
O  
Filler 720 755 36 A/N Space R  

---

## Page 63

Variable Length Record Layouts (Part 1) 
Extended Correction Transfer (200); Extended Correction Transfer Acknowledgment (201) 63 
 
EXTENDED CORRECTION TRANSFER (200); EXTENDED 
CORRECTION TRANSFER ACKNOWLEDGMENT (201) 
02.03.01 Extended Correction Transfer (200) 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Record Length 1 4 4 N 0290 R 152 
Physical Sequence 
Number 
5 6 2 A/N 01 R 004 
Logical Sequence 
Number  
7 8 2 A/N 01 R 004 
Originator Type  9 9 1 A/N A = Investment Agent 
B = Firm 
F = Fund 
T = TPA  
V = TPP (Third Party Provider) 
R 187 
Filler 10 11 2 A/N Space  R  
Firm Number 12 15 4 N Filler  R 008 
Filler 16 18 3 A/N Space  R  
Record Type  19 21 3 A/N 200 = Extended Correction Transfer 
201 = Extended Correction Transfer 
Acknowledgment 
R 002 
Test Indicator 22 22 1 A/N 0 = Production  
1 = Test 
R 122 
Filler 23 23 1 A/N Space R  
Fund Number 24 27 4 N  O 100 
Filler 28 30 3 A/N Space R  
Security Issue Country 
Code 
31 32 2 A/N Space. For future use R  
Security Issue [[ID]] 33 41 9 A/N   R 007 
Security Issue Check 
Digit 
42 42 1 A/N Space. For future use R  

---

## Page 64

Variable Length Record Layouts (Part 1) 
Extended Correction Transfer (200); Extended Correction Transfer Acknowledgment (201) 64 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Security Issue Type 43 44 2 A/N Required if 24 (Money Market) 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value against 
the Fund/SERV Security master 
file. [[NSCC]] leverages the 
Fund/SERV Security master file to 
determine value and associated 
processing rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 
OC 150 
Control Number  45 59 15 A/N  R 005 
Filler 60 60 1 A/N Space  R  
Transaction Type  61 61 1 A/N 1 = Transfer to new account  
2 = Transfer to existing account  
R 017 
Extended Correction 
Reason Code  
62 63 2 A/N 01 = Incorrect Firm/Fund Account 
Number  
02 = Incorrect Share Quantity/Dollar 
Quantity  
03 = Incorrect security issue [[ID]] 
04 = Customer renege  
05 = Incorrect Sales Charge 
Breakpoint  
07 = Blue sky violation  
09 = Delay in Firm Trade 
Transmission 
10 = With Fund’s Permission 
11 = Resubmitted Fund/SERV Reject 
12 = DCC&S (see [[Asset]] Type 
Indicator) 
13 = Distribution Reversal 
14 = Prospectus Violation 
Note: 
The values ‘06’ and ‘08’ have been 
removed. 
R 109 
Submission Date 64 71 8 N mmddccyy  R 101 
Original Trade Date  72 79 8 N mmddccyy  R 016 

---

## Page 65

Variable Length Record Layouts (Part 1) 
Extended Correction Transfer (200); Extended Correction Transfer Acknowledgment (201) 65 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Book/Physical Share 
Indicator 
80 80 1 A/N 1 = Transfer book [[shares]] to book 
[[shares]] 
2 = Transfer book [[shares]] to physical 
[[shares]] O  
R 015 
PI Delivery Indicator 81 81 1 A/N Required for all purchases if 
Book/Physical Share Ind = 2. 
0 = Deliver to customer 
1 = Deliver to firm 
2 = Deliver to agent for firm  
O 039 Filler 82 84 3 A/N Space R  
[[NSCC]] Rejection 
Indicator 
85 85 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], multiple 
errors  
R  
[[NSCC]] Reject Code  86 88 3 A/N Input: Space 
Output: Reject code  
R  
TPA/Investment 
Agent/TPP Number 
89 92 4 A/N Required if: 
Originator Type = (T or A or V) 
OR  
Membership Identifier = 02 or 03 
OC 188 
Filler  93 104 12 A/N Space R  
Original Share 
Quantity  
105 118 14 N 9,999,999,999.9999  R 019 
Debit Account Number  119 138 20 A/N  R 118 
Debit Account 
Indicator  
139 139 1 A/N 1 = Fund 
2 = Firm  
R 119 
Credit Account 
Number  
140 159 20 A/N Required for transfer to existing 
account  
OC 120 
Credit Account 
Indicator  
160 160 1 A/N Required if Credit Account Number is 
provided. 
1 = Fund 
2 = Firm  
OC 121 
Agent for Firm 
Number  
161 164 4 A/N Required if Originator Type = V 
(TPP) 
OC 271 

---

## Page 66

Variable Length Record Layouts (Part 1) 
Extended Correction Transfer (200); Extended Correction Transfer Acknowledgment (201) 66 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Network Control 
Indicator  
165 165 1 A/N 0 = Non-networked  
3 = Matrix level 3  
4 = Matrix level 4 
R 047 
Fraction Indicator 166 166 1 A/N 1 = Transfer fraction 
2 = [[liquidation]] fraction  
R 014 
Filler 167 173 7 A/N Space R  
Membership Identifier 174 175 2 A/N 01 = Trust [[Member]] 
02 = Networking info required for 
TPA/Investment Agent  
03 = TPP (Third Party Provider) 
O 181 
Filler  176 197 22 A/N Space  R  
Original Control 
Number  
198 212 15 A/N Required if Confirm Number is not 
provided  
OC 163 
Original Correction 
Indicator  
213 213 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] 
correction/cancellation 
Space = No correction 
O 164 
Confirm Number 214 225 12 A/N  O  
Filler  226 290 65 A/N Space R  

---

## Page 67

Variable Length Record Layouts (Part 1) 
Order Acknowledgment for Money Market Purchase (101); Firm Delete (102); Release to [[settlement]] (109); Registration Acknowledgment (112); Delete Pending 
Registration (Registered Ex-Fund/SERV) (113); Receiving Fund Exit from ToRA (214) 67 
 
ORDER ACKNOWLEDGMENT FOR MONEY MARKET 
PURCHASE (101); FIRM DELETE (102); RELEASE TO 
[[settlement]] (109); REGISTRATION 
ACKNOWLEDGMENT (112); DELETE PENDING 
REGISTRATION (REGISTERED EX-FUND/SERV) (113); 
RECEIVING FUND EXIT FROM TORA (214) 
For record type 214, Firm means Receiving Fund, and Fund means Delivering Fund  
02.04.01 Order Acknowledgement for Money Market Purchase (101) 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Record Length 1 4 4 N 0104, 0197 
(Must be 0197 for record types 
101, 109, 112, and 113) 
Record length for Record Type 102 
must be 0197 if Originator Type = 
V 
R 152 
Physical Sequence 
Number 
5 6 2 A/N 01  R 004 
Logical Sequence 
Number 
7 8 2 A/N 01 R 004 
Originator Type 9 9 1 A/N A = Investment Agent  
B = Firm 
F = Fund 
T = TPA 
V = Third Party Provider (TPP) 
R 187 
Filler 10 11 2 A/N Space R  
Firm Number 12 15 4 N  R 008 
Filler 16 18 3 A/N Space R  

---

## Page 68

Variable Length Record Layouts (Part 1) 
Order Acknowledgment for Money Market Purchase (101); Firm Delete (102); Release to [[settlement]] (109); Registration Acknowledgment (112); Delete Pending 
Registration (Registered Ex-Fund/SERV) (113); Receiving Fund Exit from ToRA (214) 68 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Record Type  19 21 3 A/N 101 = Order Acknowledgment for 
Money Market Purchase 
102 = Firm Delete 
109 = Release to [[settlement]] 
112 = Registration 
Acknowledgment 
113 = Delete Pending Registration 
(registered ex-Fund/SERV) 
214 = Receiving Fund Exit from 
ToRA 
R 002 
Test Indicator 22 22 1 A/N 0 = Production  
1 = Test  
R 122 
Filler 23 23 1 A/N Space  R  
Fund Number 24 27 4 N  O 100 
Filler 28 30 3 A/N Space R  
Security Issue Country 
Code 
31 32 2 A/N Space. For future use  R  
Security Issue [[ID]] 33 41 9 A/N  R 007 
Security Issue Check 
Digit 
42 42 1 A/N Space. For future use  R  
Security Issue Type 43 44 2 A/N Required if 24 (Money Market), 
except for record type 214. 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value 
against the Fund/SERV Security 
master file. [[NSCC]] leverages the 
Fund/SERV Security master file 
to determine value and 
associated processing rules. 
Output: [[NSCC]] populates with 
the value in the Fund/SERV 
Security master file. 
OC 150 
Control Number 45 59 15 A/N  R 005 

---

## Page 69

Variable Length Record Layouts (Part 1) 
Order Acknowledgment for Money Market Purchase (101); Firm Delete (102); Release to [[settlement]] (109); Registration Acknowledgment (112); Delete Pending 
Registration (Registered Ex-Fund/SERV) (113); Receiving Fund Exit from ToRA (214) 69 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Correction Indicator 60 60 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] 
correction/cancellation 
Space = No correction  
RC 006 
Filler  61 63 3 A/N Space  R  
Submission Date  64 71 8 N mmddccyy  R 101 
Certificate Date  72 79 8 N mmddccyy  
Required for record types 112 and 
113 when last trade update reflects 
physical [[shares]] (Book/Physical 
Share Ind = 2 or 3).  
Not allowed for other record types  
OC 037 
Filler  80 80 1 A/N Space  R  
PI Delivery Indicator 81 81 1 A/N Required for record types 112 and 
113 when last trade update reflects 
physical [[shares]] (Book/Physical 
Share Ind = 2 or 3). Not allowed for 
other record types.  
0 = Deliver to customer 
1 = Deliver to firm 
2 = Deliver to agent for firm  
OC 039 
Filler 82 84 3 A/N Space R  
[[NSCC]] Rejection 
Indicator 
85 85 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], multiple 
errors  
R  
[[NSCC]] Reject Code 86 88 3 A/N Input : Space 
Output: Reject code 
R  
TPA/Investment 
Agent/TPP Number 
89 92 4 A/N Required if Originator Type = T or 
A or V 
OC 188 
Service Provider Number 93 96 4 A/N  O 215 
Filler 97 104 8 A/N Space R  

---

## Page 70

Variable Length Record Layouts (Part 1) 
Order Acknowledgment for Money Market Purchase (101); Firm Delete (102); Release to [[settlement]] (109); Registration Acknowledgment (112); Delete Pending 
Registration (Registered Ex-Fund/SERV) (113); Receiving Fund Exit from ToRA (214) 70 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Certificate Number 105 114 10 A/N Required for record types 112 and 
113 when last trade update reflects 
physical [[shares]] (Book/Physical 
Share Ind = 2 or 3). Not allowed for 
other record types  
OC 038 
Filler 115 139 25 A/N Space  R  
Customer Account 
Number 
140 159 20 A/N Required for record types 101, 
109, 112 and 113  
OC 011 
Customer Account 
Number Indicator  
160 160 1 A/N Required if Customer Account 
Number is provided.  
1 = Fund 
2 = Firm  
OC 048 
Agent for Firm Number  161 164 4 A/N Required if Originator Type = V 
(TPP)  
OC 271 
Network Control 
Indicator  
165 165 1 A/N Required for record types 101, 
109, 112 and 113. 
0 = Non-networked  
3 = Matrix level 3  
4 = Matrix level 4 
OC 047 Filler 166 167 2 A/N Space  R  
Transaction Received 
Time 
168 173 6 N hhmmss Eastern Time 
Ignored for any record type other 
than 101.  
000000 (midnight) to 235959  
O 168 
Fund Reject Code 174 176 3 A/N Allowed only Record Type 214 with 
the following values: 
710 – Minimum purchase amount 
not met at Receiving Fund  
711 – Maximum purchase amount 
exceeded at Receiving Fund 
 
Not allowed for all other record 
types. 
O 264 
Filler 177 197 21 A/N Space  R  

---

## Page 71

Variable Length Record Layouts (Part 1) 
Fund Reject (100); Fund Delete (108); Registration Rejection (114); Delete Pending Release to [[settlement]]; (Settled Ex-Fund/SERV) (129) 71 
 
FUND REJECT (100); FUND DELETE (108); 
REGISTRATION REJECTION (114); DELETE PENDING 
RELEASE TO [[settlement]]; (SETTLED EX-FUND/SERV) 
(129) 
When ToRA related (ToRA Indicator = ‘1’ or ‘2’), Firm means Receiving Fund, and Fund means 
Delivering Fund  
02.05.01 Fund Reject (100) 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Record Length 1 4 4 N 0104, 0197 
(Must be 0197 if Fund Rejection 
Indicator = 2 or Fund Reject Code 
= “704” on Fund Reject Record 
“100” only). 
R 152 
Physical Sequence 
Number 
5 6 2 A/N 01 R 004 
Logical Sequence 
Number 
7 8 2 A/N 01 R 004 
Originator Type 9 9 1 A/N F = Fund R 187 
Filler 10 11 2 A/N Space  R  
Firm Number 12 15 4 N  R 008 
Filler  16 18 3 A/N Space  R  
Record Type 19 21 3 A/N 100 = Fund Reject 
108 = Fund Delete  
114 = Registration Rejection  
129 = Delete Pending Release to 
[[settlement]] (settled  
ex-Fund/SERV)  
R 002 
Test Indicator 22 22 1 A/N 0 = Production 
1 = Test 
R 122 
Filler 23 23 1 A/N Space R  
Fund Number 24 27 4 N  O 100 
Filler 28 30 3 A/N Space R  

---

## Page 72

Variable Length Record Layouts (Part 1) 
Fund Reject (100); Fund Delete (108); Registration Rejection (114); Delete Pending Release to [[settlement]]; (Settled Ex-Fund/SERV) (129) 72 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Security Issue Country 
Code 
31 32 2 A/N Space. For future use  R  
Security Issue [[ID]] 33 41 9 A/N   R 007 
Security Issue Check 
Digit 
42 42 1 A/N Space. For future use R  
Security Issue Type  43 44 2 A/N Required if 24 (Money Market), 
except if ToRA Indicator = 1 or 2. 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value 
against the Fund/SERV Security 
master file. [[NSCC]] leverages the 
Fund/SERV Security master file 
to determine value and 
associated processing rules. 
Output: [[NSCC]] populates with 
the value in the Fund/SERV 
Security master file. 
OC 150 
Control Number 45 59 15 A/N   R 005 
Correction Indicator 60 60 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] 
correction/cancellation 
Space = No correction 
 
R 006 
Filler 61 63 3 A/N Space  R  
Submission Date 64 71 8 N mmddccyy R 101 
ToRA (Transfer of 
Retirement [[Asset]]) 
Indicator 
72 72 1 A/N 1 = ToRA related (submitted by 
the receiving fund) 
2 = ToRA related (submitted by 
the delivering fund) 
Space = Not ToRA related  
R 186 
Filler 73 75 3 A/N Space  R  
Fund Reject Indicator 76 76 1 A/N 1 = Single error 
2 = Multiples errors 
R 153 
Fund Reject Code 77 79 3 A/N  R 022 
Filler 80 84 5 A/N Space R  

---

## Page 73

Variable Length Record Layouts (Part 1) 
Fund Reject (100); Fund Delete (108); Registration Rejection (114); Delete Pending Release to [[settlement]]; (Settled Ex-Fund/SERV) (129) 73 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
[[NSCC]] Rejection 
Indicator 
85 85 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], multiple 
errors 
R  
[[NSCC]] Reject Code 86 88 3 A/N Input : Space 
Output: Reject code  
R  
TPA/Investment 
Agent/TPP Number 
89 92 4 A/N  O 188 
Service Provider 
Number 
93 96 4 A/N  O 215 
Filler 97 104 8 A/N Space  R  
Fund Reject Code 2 105 107 3 A/N Required if Fund Rejection 
Indicator = 2  
OC 022 
Fund Reject Code 3 108 110 3 A/N  O 022 
Fund Reject Code 4 111 113 3 A/N  O 022 
Fund Reject Code 5 114 116 3 A/N  O 022 
Fund Reject Code 6 117 119 3 A/N  O 022 
Fund Reject Code 7 120 122 3 A/N  O 022 
Fund Reject Code 8 123 125 3 A/N  O 022 
Fund Reject Code 9 126 128 3 A/N  O 022 

---

## Page 74

Variable Length Record Layouts (Part 1) 
Fund Reject (100); Fund Delete (108); Registration Rejection (114); Delete Pending Release to [[settlement]]; (Settled Ex-Fund/SERV) (129) 74 
 
Field Name  Start End Len Type Description  Opt/Req Reject 
Code 
Delivering Fund Plan 
Type 
129 129 1 A/N Required if the Fund Reject Code 
= “704” 
0 = IRA 
1 = IRA Rollover 
2 = SEP IRA 
3 = 403B 
4 = Roth IRA 
5 = Simple IRA 
6 = Education IRA 
7 = SARSEP 
8 = Roth Conversion IRA 
9 = Traditional to Roth Conversion 
IRA 
A = Inherited Traditional IRA 
B = Inherited Roth IRA 
C = Inherited Roth Conversion 
IRA 
D= Account Type Is Not ToRA 
Eligible  
OC 265 
Filler 130 197 68 A/N Space  R  

---

## Page 75

Variable Length Record Layouts (Part 1) 
Exchange Order (015) 75 
 
EXCHANGE ORDER (015) 
02.06.01 Exchange Order (015) 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
Record Length 1 4 4 N With no SSN/EIN Suffix: 
0383, 0476 
With SSN/EIN Suffix: 
Up to 1499  
R 152 
Physical Sequence 
Number 
5 6 2 A/N 01  R 004 
Logical Sequence 
Number 
7 8 2 A/N 01  R 004 
Originator Type 9 9 1 A/N A = Investment Agent 
B = Firm 
T = TPA 
S = Service Provider for B = Firm 
P = Service Provider for T = TPA 
V = TPP (Third Party Provider) 
R 187 
Filler 10 11 2 A/N Space R  
Firm Number 12 15 4 N  R 008 
Filler 16 18 3 A/N Space  R  
Record Type 19 21 3 A/N 015 = Exchange Order  
Not permitted if the Security Issue 
Type field value is 63 and 
[[settlement]] Override Reason Code 
field value is space. 
RC 002/275 
Test Indicator 22 22 1 A/N 0 = Production  
1 = Test 
R 122 
Filler 23 23 1 A/N Space  R  
Fund Number  24 27 4 N   O 100 
Filler 28 30 3 A/N Space  R  
Security Issue Country 
Code  
(Exch From) 
31 32 2 A/N Space. For future use  R  

---

## Page 76

Variable Length Record Layouts (Part 1) 
Exchange Order (015) 76 
 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
Security Issue [[ID]]  
(Exch From) 
33 41 9 A/N   R 007 
Security Issue Check 
Digit  
(Exch From) 
42 42 1 A/N Space. For future use  R  
Security Issue Type 
(Exch From) 
43 44 2 A/N Required if 24 (Money Market)  
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value 
against the Fund/SERV Security 
master file. [[NSCC]] leverages the 
Fund/SERV Security master file 
to determine value and 
associated processing rules. 
Output: [[NSCC]] populates with 
the value in the Fund/SERV 
Security master file. 
OC 150 
Control Number 45 59 15 A/N   R 005 
Filler 60 60 1 A/N Space R  
Transaction Type  61 61 1 A/N 6 = Exchange to new account 
7 = Exchange to existing account  
C = Voluntary Cross Class 
Exchange to new account 
D = Voluntary Cross Class 
Exchange to existing account 
R 017 
Transaction Code 62 63 2 A/N 05 = Full exchange 
06 = Partial exchange 
R 018 
Submission Date 64 71 8 N mmddccyy R 101 
Trade Date 72 79 8 N mmddccyy R 016 
Book/Physical Share 
Indicator 
80 80 1 A/N 1 = Exchange from book [[shares]] to 
book [[shares]] 
2 = Exchange from book [[shares]] to 
physical [[shares]]  
R 015 

---

## Page 77

Variable Length Record Layouts (Part 1) 
Exchange Order (015) 77 
 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
PI Delivery Indicator 81 81 1 A/N Required if Book/Physical Share 
Indicator = 2. 
0 = Deliver to customer 
1 = Deliver to firm  
2 = Deliver to agent for firm  
OC 039 
Filler 82 82 1 A/N Space  R  
[[settlement]] Override 
Reason Code 
83 84 2 A/N Required (but must not be 04) if 
Anticipated [[settlement]] Date is 
provided.  
01 = Wrap fee account 
02 = 401K 
03 = Other 
04 = X-[[settlement]] 
05 = Section 529 Account - 
Qualified State Tuition Program 
06 = X-[[settlement]] offshore 
enhanced (allowed for Security 
Types 62 and 63 only) 
OC 179 
[[NSCC]] Rejection 
Indicator 
85 85 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], multiple 
errors 
R  
[[NSCC]] Reject Code 86 88 3 A/N Input: Space 
Output: Reject code  
R  
TPA/Investment 
Agent/TPP Number 
89 92 4 A/N Required if: 
Originator Type = (T or P or A or V) 
OR  
Membership Identifier = 02 or 03. 
OC 188 
Service Provider 
Number  
93 96 4 A/N Required if Originator Type = S or 
P  
OC 215 
SSN/EIN Start Section 
Number 
97 98 2 A/N See SSN/EIN Start Section 
Number in the Introduction section. 
Required if SSN/EIN Suffix is 
provided. Not allowed otherwise. 
OC 257 
Total SSN/EIN Sections 99 100 2 N Required if SSN/EIN Suffix is 
provided. Not allowed otherwise.  
OC 258 
Filler 101 104 4 A/N Space R  

---

## Page 78

Variable Length Record Layouts (Part 1) 
Exchange Order (015) 78 
 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
Exch From Share 
Quantity  
105 118 14 N 9,999,999,999.9999  
Required if Transaction Code = 06 
and Exch From Money Amount = 0 
 
OC 019 
Customer Account 
Number at Firm 
119 138 20 A/N Optional if [[settlement]] Override 
Reason Code = 04 or 06 or if 
Membership Identifier is provided.  
RC 020 
New Registration 
Indicator 
139 139 1 A/N 0 = No registration required 
1 = Registration required for 
Exchange To  
R 040 
Exch From Account 
Number at Fund 
140 159 20 A/N Required if Network Control Ind (for 
From Account) = 0  
OC 011 
Filler 160 160 1 A/N Space  R  
Agent for Firm Number 161 164 4 A/N Required if Originator Type = V 
(TPP) 
OC 271 
Network Control 
Indicator (for the From 
Account)  
165 165 1 A/N 0 = Non-networked  
3 = Matrix level 3  
4 = Matrix level 4 
R 047 
Fraction Indicator 166 166 1 A/N 1 = Issue fraction 
2 = [[liquidation]] fraction  
R 014 
Filler  167 167 1 A/N Space R  
Transaction Received 
Time 
168 173 6 N  
hhmmss Eastern Time 
000000 (midnight) to 235959 
 
Required when “Money Market 
[[Liquidity]] Fee/Redemption Gate 
Indicator” = ‘F’ (Fund). 
OC 168 
Membership Identifier 174 175 2 A/N 01 = Trust [[Member]] 
02 = Networking info required for 
TPA/Investment Agent  
03 = TPP (Third Party Provider) 
O 181 
Filler 176 197 22 A/N Space R  
Exch From Money 
Amount 
198 213 16 N 99,999,999,999,999.99 Required if 
Transaction Code = 06 and Exch 
From Share Quantity = 0  
OC 019 

---

## Page 79

Variable Length Record Layouts (Part 1) 
Exchange Order (015) 79 
 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
Exch From Currency 
Indicator 
214 216 3 A/N   O 110 
Anticipated [[settlement]] 
Date 
217 224 8 A/N mmddccyy 
Required if [[settlement]] Override 
Reason Code is provided and is 
not 04 or 06 (x-[[settlement]]).  
Not allowed if [[settlement]] Override 
Reason Code = 04. 
OC 180 Branch Identification 
Number 
225 233 9 A/N Optional under the following 
conditions: 
• Membership Identifier = 01 or 
02, and Agent for Firm Number 
is not provided 
• Originator Type = V (TPP)  
RC 035 
Related Trade Indicator 234 234 1 A/N 0 = No 
1 = Yes 
R 065 
Related Trade Identifier 235 236 2 A/N Required if Related Trade Indicator 
= 1 
OC 105 
Customer Name 237 256 20 A/N   R 063 
Exch From Sales 
Charge Rate 
257 260 4 N 9.999  O 025 
As-Of Indicator 261 261 1 A/N 0 = Regular Exchange 
1 = As-Of Exchange  
O 021 
Discount Type  262 262 1 A/N 1 = Letter of intent 
2 = Rights of accumulation 
3 = Net [[Asset]] value 
O 208 
Filler 263 267 5 A/N Space R  

---

## Page 80

Variable Length Record Layouts (Part 1) 
Exchange Order (015) 80 
 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
NAV Reason Code 268 268 1 A/N Required if Discount Type = 3.  
0 = Other  
1 = Net [[Asset]] value transfer  
2 = Repurchase 
3 = Employee 
4 = Error correction 
5 = Wrap fee account 
6 = NAV commissionable 
7 = Commissionable defined 
contribution plan 
8 = Non-commissionable defined 
contribution plan 
9 = Section 529 Account - Qualified 
State Tuition Program 
A = [[Dividend]] reinvestment trade 
B = Trust Company NAV per 
Agreement  
D = Deminimis Amount Processed 
at NAV  
E = Self Directed Brokerage 
Account 
OC 104 
As-Of Reason Code 269 270 2 A/N Required if As-Of Indicator = 1 
01 = Incorrect Firm/Fund Account 
Number  
02 = Incorrect Share 
Quantity/Dollar Quantity  
03 = Incorrect security issue [[ID]] 
04 = Customer renege  
05 = Incorrect Sales Charge 
Breakpoint  
07 = Blue sky violation  
09 = Delay in Firm Trade 
Transmission 
10 = With Fund’s Permission 
11 = Resubmitted Fund/SERV 
Reject 
12 = DCC&S (see [[Asset]] Type 
Indicator) 
13 = Distribution Reversal 
14 = Prospectus Violation 
OC 109 

---

## Page 81

Variable Length Record Layouts (Part 1) 
Exchange Order (015) 81 
 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
Redemption Fee 
Indicator 
271 271 1 A/N 0 = Short-Term Redemption (STR) 
1 = STR with CDSC 
2 = Money Market [[Liquidity]] Fee  
3 = Money Market [[Liquidity]] Fee 
with CDSC 
O 248 
Short-Term Redemption 
Fee Waiver Indicator  
272 272 1 A/N 1 = STR waiver due to correction  
2 = Death  
3 = Disability  
4 = Mandatory distribution  
5 = Systematic withdrawal  
6 = Defined contribution  
7 = Hardship  
8 = Auto Rebalance  
9 = DC – Termination Distribution  
A = DC – Involuntary Distribution  
B = DC – Forfeitures  
C = DC – Loans  
D = DC – Excess Contributions 
E = Wrap Program  
F = Fund of Funds 
G = Divorce/QDRO 
H = Plan fees QDRO 
O 249 
Filler 273 289 17 A/N Space R  
Trade Date Forward 
Indicator 
290 290 1 A/N 0 = Trade Date not forwarded 
1 = Trade Date forwarded  
Must be 1 if Trade Date is later 
than Submission Date.  
OC 229 
Security Issue Country 
Code (Exch To) 
291 292 2 A/N Space. For future use  R  
Security Issue [[ID]]  
(Exch To) 
293 301 9 A/N   R 041 
Security Issue Check 
Digit (Exch To) 
302 302 1 A/N Space. For future use R  

---

## Page 82

Variable Length Record Layouts (Part 1) 
Exchange Order (015) 82 
 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
Security Issue Type 
(Exch To) 
303 304 2 A/N Required if 24 (Money Market) 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value 
against the Fund/SERV Security 
master file. [[NSCC]] leverages the 
Fund/SERV Security master file 
to determine value and 
associated processing rules. 
Output: [[NSCC]] populates with 
the value in the Fund/SERV 
Security master file. 
OC 150 
Exch To Account 
Number  
305 324 20 A/N Required if Transaction Type = 7 
(Exchange to existing account 
number) or  
D (Voluntary Cross Class 
Exchange to existing account 
number) 
OC 011 
Exch To Account 
Number Indicator 
325 325 1 A/N Required if Exch To Account 
Number is provided.  
1 = Fund 
2 = Firm  
OC 048 
Network Control 
Indicator (for the To 
Account ) 
326 326 1 A/N 0 = Non-networked  
3 = Matrix level 3  
4 = Matrix level 4 
R 047 
Exch To Sales Charge 
Rate 
327 330 4 N 9.999  O 025 
ROA/LOI Value 331 346 16 N 99,999,999,999,999.99  O 064 
LOI Number/Date 347 354 8 A/N   O  
State of Sale  
(State Code)  
355 356 2 A/N Required for all exchanges R 012 
Money Market [[Liquidity]] 
Fee/Redemption Gate 
Indicator  
357 357 1 A/N F = Fund.  
B = [[intermediary]] 
O 282 
Transaction Received 
Date  
358 365 8 A/N mmddccyy 
 
Required if the “Money Market 
[[Liquidity]] Fee/Redemption Gate 
Indicator” = F. 
OC 283 

---

## Page 83

Variable Length Record Layouts (Part 1) 
Exchange Order (015) 83 
 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
Aggregated Order 
Indicator  
366 366 1 A/N Required if the “Money Market 
[[Liquidity]] Fee/Redemption Gate 
Indicator” = “F” or “B”. 
• 1 = Transactions are not 
aggregated  
• 2 = Transactions are 
aggregated by “like” orders 
(purchases separate from 
redemptions) 
• 3 = Transactions are net of 
purchases and redemptions 
• 4 = Unknown at time of 
placement 
OC 284 
Filler 367 376 10 A/N Space  R  
Standard [[ID]]  377 382 6 A/N  O  
Program Transaction 
Indicator 
383 383 1 A/N 1 = Systematic Exchange O 259 
Account Representative 
Number 
384 392 9 A/N  O  
Account Representative 
Name  
393 407 15 A/N  O  
Confirm Number 408 419 12 A/N   O  
Memo Field 420 439 20 A/N   O  
Redemption Fee Rate 440 446 7 N 99.99999 
 
Not allowed if “Redemption Fee 
Indicator” is not provided. 
 
Required when “Redemption Fee 
Indicator” is populated with either 
‘2’ (Money Market [[Liquidity]] Fee) or 
‘3’ (Money Market [[Liquidity]] Fee 
with CDSC). 
Zero value is not allowed when this 
field is required and “Redemption 
Fee Indicator” =2 or 3. 
 
If “Redemption Fee Indicator” = 0 
or 1, this field will be utilized to 
communicate a Short-Term 
Redemption (STR) Fee Rate. 
OC 250 

---

## Page 84

Variable Length Record Layouts (Part 1) 
Exchange Order (015) 84 
 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
STR Fee Share 
Quantity  
447 460 14 N 9,999,999,999.9999 
Required when “Redemption Fee 
Indicator” is provided and 
“Redemption Fee Money Amount” 
= 0 or Space. 
Not allowed if “Redemption Fee 
Indicator” is not provided or if 
“Redemption Fee Money Amount” 
> 0. 
 
Not allowed when “Redemption 
Fee Indicator” is populated with 
either ‘2’ (Money Market [[Liquidity]] 
Fee) or ‘3’ (Money Market [[Liquidity]] 
Fee with CDSC). 
OC 251 
Redemption Fee 
Money Amount (old 
name STR Fee Money 
Amount)  
461 476 16 N 99,999,999,999,999.99 
Required when “Redemption Fee 
Indicator” is provided and “STR 
Fee Share Quantity” = 0 or Space.
 
Not allowed if “Redemption Fee 
Indicator” is not provided or if 
“STR Fee Share Quantity” > 0. 
 
Required when “Redemption Fee 
Indicator” is populated with either 
‘2’ (Money Market [[Liquidity]] Fee) 
or ‘3’ (Money Market [[Liquidity]] Fee 
with CDSC). 
Zero value is not allowed when 
this field is required. 
 
If “Redemption Fee Indicator” =0 
or 1, this field will be utilized to 
communicate a Short-Term 
Redemption (STR) Fee Money 
Amount. 
OC 252 

---

## Page 85

Variable Length Record Layouts (Part 1) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 85 
 
EXCHANGE CONFIRMATION (016); EXCHANGE 
RECONFIRMATION (017); POST [[settlement]] 
EXCHANGE CANCELLATION (021) 
02.07.01 Exchange Confirmation (016) 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
Record Length 1 4 4 N 0569, 0662 = No ‘To’ sections 
included 
0755 = ‘To’ sections #1 included 
0848 = ‘To’ sections #1 and #2  
0941 = ‘To’ sections #1, #2 and #3 
included  
1034 = ‘To’ sections #1, #2, #3, and 
#4 
1127 = ‘To’ sections #1, #2, #3, #4 
and #5 included  
R 152 
Physical Sequence 
Number 
5 6 2 A/N 01 R 004 
Logical Sequence 
Number 
7 8 2 A/N 01 R 004 
Originator Type 8 8 1 A/N F = Fund R 187 
Filler 10 11 2 A/N Space R  
Firm Number 12 15 4 N  R 008 
Filler 16 18 3 A/N Space R  
Record Type 19 21 3 A/N 016 = Exchange Confirmation  
017 = Exchange Reconfirmation 
021 = Post [[settlement]] Exchange 
Cancellation 
Not permitted if the Security Issue 
Type field value is 63 and [[settlement]] 
Override Reason Code field value is 
space. 
RC 002/275 
Test Indicator 22 22 1 A/N 0 = Production 
1 = Test 
R 122 
Filler 23 23 1 A/N Space R  

---

## Page 86

Variable Length Record Layouts (Part 1) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 86 
 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
Fund Number 24 27 4 N  O 100 
Filler 28 30 3 A/N Space R  
Security Issue Country 
Code  
(Exch From) 
31 32 2 A/N Space. For future use  R  
Security Issue [[ID]] 
(Exch From) 
33 41 9 A/N  R 007 
Security Issue Check 
Digit (Exch From) 
42 42 1 A/N Space. For future use R  
Security Issue Type 
(Exch From) 
43 44 2 A/N Required if 24 (Money Market) 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value against 
the Fund/SERV Security master 
file. [[NSCC]] leverages the 
Fund/SERV Security master file to 
determine value and associated 
processing rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 
OC 150 
Control Number 45 59 15 A/N  R 005 
Correction Indicator 60 60 1 A/N Required for record type 021.  
Not allowed for record type 017. 
P = Post [[settlement]] cancellation 
OC 006 
Transaction Type  61 61 1 A/N 6 = Exchange to new account 
7 = Exchange to existing account 
C = Voluntary Cross Class Exchange 
to new account 
D = Voluntary Cross Class Exchange 
to existing account 
R 017 
Transaction Code 62 63 2 A/N 05 = Full exchange 
06 = Partial exchange  
R 018 
Submission Date 64 71 8 N mmddccyy R 101 
Trade Date 72 79 8 N mmddccyy R 016 

---

## Page 87

Variable Length Record Layouts (Part 1) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 87 
 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
Book/Physical Share 
Indicator 
80 80 1 A/N 1 = Exchange from book [[shares]] to 
book [[shares]] 
2 = Exchange from book [[shares]] to 
physical [[shares]] 
R 015 
PI Delivery Indicator 81 81 1 A/N Required if Book/Physical Share 
Indicator = 2. 
0 = Deliver to customer  
1 = Deliver to firm 
2 = Deliver to agent for firm  
OC 039 Filler 82 82 1 A/N Space R  
[[settlement]] Override 
Reason Code 
83 84 2 A/N Not allowed if Correction Indicator = 
P. 
01 = Wrap fee account  
02 = 401K 
03 = Other 
04 = X-[[settlement]] 
05 = Section 529 Account – Qualified 
State Tuition Program 
06 = X-[[settlement]] offshore enhanced 
(allowed for Security Types 62 and 
63 only)  
O 179 
[[NSCC]] Rejection 
Indicator 
85 85 1 A/N Input: Space  
Output: 
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], multiple 
errors 
R  
[[NSCC]] Reject Code 86 88 3 A/N Input: Space  
Output: Reject code 
R  
TPA/Investment 
Agent/TPP Number 
89 92 4 A/N Required if Membership Identifier = 
02 or 03 
OC 188 
Service Provider 
Number 
93 96 4 A/N  O 215 
Filler 97 104 8 A/N Space R  
Exch From Share 
Quantity 
105 118 14 N 9,999,999,999.9999 
Required if Transaction Code = 06 
and Exch From Money Amount 
(Gross) = 0 
OC 019 

---

## Page 88

Variable Length Record Layouts (Part 1) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 88 
 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
Customer Account 
Number at Firm 
119 138 20 A/N Optional if [[settlement]] Override 
Reason Code = 04 or 06 or if 
Membership Identifier is provided.  
RC 020 
New Registration 
Indicator 
139 139 1 A/N 0 = No registration required  
1 = Registration required for 
Exchange To  
R 040 
Exch From Account 
Number at Fund 
140 159 20 A/N Required if Network Control Ind (for 
From Account) = 0  
OC 011 
Filler 160 160 1 A/N Space R  
Agent for Firm 
Number 
161 164 4 A/N  O  
Network Control 
Indicator (for the From 
Account)  
165 165 1 A/N 0 = Non-networked  
3 = Matrix level 3  
4 = Matrix level 4 
R 047 
Fraction Indicator 166 166 1 A/N 1 = Issue fraction 
2 = [[liquidation]] fraction 
R 014 
Filler 167 167 1 A/N Space R  
Transaction Received 
Time 
168 173 6 N  
hhmmss Eastern Time 
000000 (midnight) to 235959 
 
Required when “Money Market 
[[Liquidity]] Fee/Redemption Gate 
Indicator” = ‘F’ (Fund). 
 
For Record types 016 and 017 
Must contain the same value as 
provided on the Exchange 
transaction (record type 015).  
[[NSCC]] will reject if a fund provided 
value is different from the value 
submitted by the firm. 
OC 168 
Membership Identifier 174 175 2 A/N 01 = Trust [[Member]] 
02 = Networking info required for 
TPA/Investment Agent 
03 = TPP (Third Party Provider) 
 
O 181 
Filler 176 197 22 A/N Space R  

---

## Page 89

Variable Length Record Layouts (Part 1) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 89 
 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
Exch From Money 
Amount (Gross) 
198 213 16 N 99,999,999,999,999.99  
Required if Transaction Code = 06 
and Exch From Share Quantity = 0 
OC 019 
Exch From Currency 
Indicator (Gross) 
214 216 3 A/N  O 110 
Anticipated [[settlement]] 
Date 
217 224 8 A/N mmddccyy 
Required if [[settlement]] Override 
Reason Code is provided and is not 
= 04 (x-[[settlement]] domestic).  
Not allowed if [[settlement]] Override 
Reason Code = 04. 
OC 180 
Branch Identification 
Number 
225 233 9 A/N Optional under the following 
conditions if Membership Identifier = 
01 or 02 and Agent for Firm Number 
is not provided. 
RC 035 
Related Trade 
Indicator 
234 234 1 A/N 0 = No 
1 = Yes 
R 065 
Related Trade 
Identifier 
235 236 2 A/N Required if Related Trade Indicator = 
1 
OC 105 
Customer Name 237 256 20 A/N  R 063 
Exch From Sales 
Charge Rate 
257 260 4 N 9.999 O 025 
As-Of Indicator 261 261 1 A/N 0 = Regular Exchange 
1 = As-Of Exchange 
O 021 
Discount Type 262 262 1 A/N 1 = Letter of intent 
2 = Rights of accumulation 
3 = Net [[Asset]] value 
O 208 
Filler 263 267 5 A/N Space R  

---

## Page 90

Variable Length Record Layouts (Part 1) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 90 
 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
NAV Reason Code  268 268 1 A/N Required if Discount Type = 3.  
0 = Other 
1 = Net [[Asset]] value transfer 
2 = Repurchase 
3 = Employee  
4 = Error correction 
5 = Wrap fee account 
6 = NAV commissionable 
7 = Commissionable defined 
contribution plan 
8 = Non-commissionable defined 
contribution plan 
9 = Section 529 Account – Qualified 
State Tuition Program 
A = [[Dividend]] reinvestment trade 
B = Trust Company NAV per 
Agreement  
D = Deminimis Amount Processed at 
NAV  
E = Self Directed Brokerage Account 
OC 104 
As-Of Reason Code 269 270 2 A/N Required if As-Of Indicator = 1 
01 = Incorrect Firm/Fund Account 
Number  
02 = Incorrect Share Quantity/Dollar 
Quantity  
03 = Incorrect security issue [[ID]] 
04 = Customer renege  
05 = Incorrect Sales Charge 
Breakpoint  
07 = Blue sky violation  
09 = Delay in Firm Trade 
Transmission 
10 = With Fund’s Permission 
11 = Resubmitted Fund/SERV Reject 
12 = DCC&S (see [[Asset]] Type 
Indicator) 
13 = Distribution Reversal 
14 = Prospectus Violation 
OC 109 

---

## Page 91

Variable Length Record Layouts (Part 1) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 91 
 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
Redemption Fee 
Indicator 
271 271 1 A/N 0 = Short-Term Redemption (STR) 
1 = STR with CDSC 
2 = Money Market [[Liquidity]] Fee  
3 = Money Market [[Liquidity]] Fee with 
CDSC 
 
Values “0” and “1” are not allowed for 
record types 016 and 017 if this field 
was blank on the original Exchange 
transaction (record type 015). 
 
Values “2” and “3” are allowed for 
record types 016 and 017 if this field 
was blank on the original Exchange 
transaction (record type 015).  
O 248 
Short-Term 
Redemption Fee 
Waiver Indicator  
272 272 1 A/N 1 = STR waiver due to correction  
2 = Death  
3 = Disability  
4 = Mandatory distribution  
5 = Systematic withdrawal  
6 = Defined contribution  
7 = Hardship  
8 = Auto Rebalance  
9 = DC – Termination Distribution  
A = DC – Involuntary Distribution  
B = DC – Forfeitures  
C = DC – Loans  
D = DC – Excess Contributions 
E = Wrap Program  
F = Fund of Funds 
G = Divorce/QDRO  
H = Plan fees QDRO 
O 249 
Filler 273 289 17 A/N Space R  
Trade Date Forward 
Indicator 
290 290 1 A/N 0 = Trade Date not forwarded  
1 = Trade Date forwarded.  
For record type 016 and 017: 
Must be same as on original 
exchange  
OC 229 

---

## Page 92

Variable Length Record Layouts (Part 1) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 92 
 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
Security Issue Country 
Code  
(Exch To) 
291 292 2 A/N Space. For future use  R  
Security Issue [[ID]] 
(Exch To) 
293 301 9 A/N  R 041 
Security Issue Check 
Digit (Exch To) 
302 302 1 A/N Space. For future use  R  
Security Issue Type 
(Exch To) 
303 304 2 A/N Required if 24 (Money Market) 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value against 
the Fund/SERV Security master 
file. [[NSCC]] leverages the 
Fund/SERV Security master file to 
determine value and associated 
processing rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 
OC 150 
Exch To Account 
Number 
305 324 20 A/N Required if Book/Physical Share 
Indicator = 2  
OC 011 
Exch To Account 
Number Indicator 
325 325 1 A/N Required if Exch To Account Number 
is provided.  
1 = Fund 
2 = Firm 
OC 048 
Network Control 
Indicator (for the To 
Account)  
 
326 326 1 A/N 0 = Non-networked  
3 = Matrix level 3  
4 = Matrix level 4 
 
R 047 
Exch To Sales Charge 
Rate 
327 330 4 N 9.999 
Must be provided (but allowed to be 
zero) if Exch To Load Type Indicator 
= 1  
OC 025 
ROA/LOI Value 331 346 16 N 99,999,999,999,999.99  O 064 
LOI Number/Date 347 354 8 A/N  O  
State of Sale  
(State Code)  
355 356 2 A/N Required for all exchanges R 012 

---

## Page 93

Variable Length Record Layouts (Part 1) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 93 
 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
Money Market 
[[Liquidity]] 
Fee/Redemption Gate 
Indicator  
357 357 1 A/N F = Fund.  
B = [[intermediary]] 
 
For Record Types 016 & 017 
Must contain the same value as 
provided on the Exchange 
transaction (record type 015).  
[[NSCC]] will reject if a fund provided 
value is different from the value 
submitted by the firm. 
O 282 
Transaction Received 
Date  
358 365 8 A/N mmddccyy 
 
Required if the “Money Market 
[[Liquidity]] Fee/Redemption Gate 
Indicator” = F. 
 
For Record Types 016 & 017 
Must contain the same value as 
provided on the Exchange 
transaction (record type 015).  
[[NSCC]] will reject if a fund provided 
value is different from the value 
submitted by the firm. 
OC 283 
Aggregated Order 
Indicator  
366 366 1 A/N Required if the “Money Market 
[[Liquidity]] Fee/Redemption Gate 
Indicator” = “F” or “B”. 
• 1 = Transactions are not 
aggregated  
• 2 = Transactions are aggregated 
by “like” orders (purchases 
separate from redemptions) 
• 3 = Transactions are net of 
purchases and redemptions 
• 4 = Unknown at time of 
placement 
 
For Record Types 016 & 017 
Must contain the same value as 
provided on the Exchange 
transaction (record type 015).  
[[NSCC]] will reject if a fund provided 
value is different from the value 
submitted by the firm. 
OC 284 
Filler 367 376 10 A/N Space R  
Standard [[ID]] 377 382 6 A/N  O  

---

## Page 94

Variable Length Record Layouts (Part 1) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 94 
 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
Program Transaction 
Indicator 
383 383 1 A/N 1 = Systematic Exchange O 259 
Account 
Representative 
Number 
384 392 9 A/N  O  
Account 
Representative Name 
393 407 15 A/N  O  
Confirm Number 408 419 12 A/N  O  
Memo Field 420 439 20 A/N  O  
Redemption Fee Rate 440 446 7 N 99.99999  
 
Not allowed if “Redemption Fee 
Indicator” is not provided. 
 
Required when “Redemption Fee 
Indicator” is populated with either ‘2’ 
(Money Market [[Liquidity]] Fee) or ‘3’ 
(Money Market [[Liquidity]] Fee with 
CDSC). 
Zero value is not allowed when this 
field is required and “Redemption 
Fee Indicator” =2 or 3. 
 
If “Redemption Fee Indicator” = 0 or 
1, this field will be utilized to 
communicate a Short-Term 
Redemption (STR) Fee Rate. 
OC 250 
STR Fee Share 
Quantity 
447 460 14 N 9,999,999,999.9999 
 
For all record types 
Not allowed if “Redemption Fee 
Indicator” is not provided. 
 
For record types 016 and 017: 
If zero or Space, will not override the 
“STR Fee Share Quantity” in the 
database. 
 
For all record types 
Not allowed when “Redemption Fee 
Indicator” is populated with either ‘2’ 
(Money Market [[Liquidity]] Fee) or ‘3’ 
(Money Market [[Liquidity]] Fee with 
CDSC). 
O 251 

---

## Page 95

Variable Length Record Layouts (Part 1) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 95 
 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
Redemption Fee 
Money Amount (old 
name STR Fee Money 
Amount)  
461 476 16 N 99,999,999,999,999.99 
 
For all record types 
Not allowed if “Redemption Fee 
Indicator” is not provided. 
 
For record types 016 and 017: 
Required when “Redemption Fee 
Indicator” is provided. 
 
For all record types 
Required when “Redemption Fee 
Indicator” is populated with either ‘2’ 
(Money Market [[Liquidity]] Fee) or ‘3’ 
(Money Market [[Liquidity]] Fee with 
CDSC). 
Zero value is not allowed when this 
field is required. 
 
If “Redemption Fee Indicator” = 0 or 
1, this field will be utilized to 
communicate a Short-Term 
Redemption (STR) Fee Money 
Amount. 
OC 252 
Exch From Money 
Amount Due 
477 492 16 N 99,999,999,999,999.99 
This amount will be settled by [[NSCC]] 
as follows: 
If Correction Ind = space:  
Credit firm, debit fund; 
If Correction Ind = P:  
Debit firm, credit fund. 
R 026 
Exch From Currency 
Indicator Due 
493 495 3 A/N  O 110 
Invoke Indicator 496 496 1 A/N 1 = Yes (postpone [[settlement]] until 
reconfirmed) 
2 = No (settle Exchange).  
Must be 2 for record type 017 or if 
Correction Indicator = P  
R 043 Tefra Withholding 497 497 1 A/N 0 = No withholding 
1 = 20% withholding 
R 050 
Exch From Price Per 
Share 
498 509 12 N 999,999.999999  R 027 

---

## Page 96

Variable Length Record Layouts (Part 1) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 96 
 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
Filler 510 513 4 A/N Space  R  
Exch From Sales 
Charge Amount 
514 522 9 N 9,999,999.99 O 088 
Number of ‘To’ 
sections 
523 524 2 N 00-05  
Must correspond Record Length 
R 049 
Exch To Account 
Number #2 
525 544 20 A/N  O  
Exch To Account 
Number #2 Indicator 
545 545 1 A/N Required if Exch To Account Number 
#2 is provided. 
1 = Fund 
2 = Firm 
OC 048 
Exchange Fee 546 553 8 N 999,999.99 O 042 
Filler 554 567 14 A/N Space R  
Breakpoint Change 
Reason Code 
568 568 1 A/N 1 = ROA value at fund  
2 = LOI at fund  
3 = The higher of cost or market 
value at fund  
4 = Jumbo Pricing  
5 = Wrap Account  
6 = NAV Account 
7 = Amount Processed at NAV  
O 246 
Filler 569 569 1 A/N Space R  
Original Control 
Number 
570 584 15 A/N  O  
Original Correction 
Indicator 
585 585 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] 
correction/cancellation 
Space = No correction 
O 164 
Filler 586 662 77 A/N Space R  
Start of ‘To’ section #1 (required if Invoke Indicator = 2) 
Exch To Gross Money 
Amount 1 
663 678 16 N 99,999,999,999,999.99 R 019 
Exch To Money 
Amount Due 1 
679 694 16 N 99,999,999,999,999.99 R 026 

---

## Page 97

Variable Length Record Layouts (Part 1) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 97 
 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
Exch To Total Share 
Quantity 1 
695 708 14 N 9,999,999,999.9999  
Represents the total for the entire 
Exchange transaction. This is the 
settled quantity  
R 019 
Exch To Price Per 
Share 1 
709 720 12 N 999,999.999999 R 027 
Exch To Firm 
Concession 1 
721 729 9 N 9,999,999.99 O 044 
Exch To Total Money 
Amount Due 
730 745 16 N 99,999,999,999,999.99 Represents 
the total for the entire Exchange 
transaction.  
This amount will be settled by [[NSCC]] 
as follows: 
If Correction Ind = space:  
Debit firm, credit fund; 
If Correction Ind = P:  
Credit firm, debit fund. 
R 026 
Exch To Currency 
Indicator 
746 748 3 A/N  O 110 
Exch To Load Type 
Indicator  
749 749 1 A/N 0 = Other 
1 = Front-End Load 
R 247 
Filler 750 755 6 A/N Space R  
Start of ‘To’ section #2 (optional, used to report additional sales charge rate) 
Exch To Gross Money 
Amount 2 
756 771 16 N 99,999,999,999,999.99  R 019 
Exch To Money 
Amount Due 2 
772 787 16 N 99,999,999,999,999.99 R 026 
Exch To Total Share 
Quantity 2 
788 801 14 N 9,999,999,999.9999 R 019 
Exch To Price Per 
Share 2 
802 813 12 N 999,999.999999 R 027 
Exch To Firm 
Concession 2 
814 822 9 N 9,999,999.99 O 044 
Exch To Sales Charge 
Rate 2 
823 826 4 N 9.999 
Must be provided (but allowed to be 
zero) if Exch To Load Type Indicator 
= 1  
OC 025 

---

## Page 98

Variable Length Record Layouts (Part 1) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 98 
 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
Filler 827 848 22 A/N Space R  
Start of ‘To’ section #3 (optional, used to report additional sales charge rate) 
Exch To Gross Money 
Amount 3 
849 864 16 N 99,999,999,999,999.99 R 019 
Exch To Money 
Amount Due 3 
865 880 16 N 99,999,999,999,999.99 R 026 
Exch To Total Share 
Quantity 3 
881 894 14 N 9,999,999,999.9999 R 019 
Exch To Price Per 
Share 3 
895 906 12 N 999,999.999999 R 027 
Exch To Firm 
Concession 3 
907 915 9 N 9,999,999.99 O 044 
Exch To Sales Charge 
Rate 3 
916 919 4 N 9.999 
Must be provided (but allowed to be 
zero) if Exch To Load Type Indicator 
= 1  
OC 025 
Filler 920 941 22 A/N Space R  
Start of ‘To’ section #4 (optional, used to report additional sales charge rate) 
Exch To Gross Money 
Amount 4 
942 957 16 N 99,999,999,999,999.99 R 019 
Exch To Money 
Amount Due 4 
958 973 16 N 99,999,999,999,999.99 R 026 
Exch To Total Share 
Quantity 
974 987 14 N 9,999,999,999.9999 R 019 
Exch To Price Per 
Share 4 
988 999 12 N 999,999.999999 R 027 
Exch To Firm 
Concession 4 
1000 1008 9 N 9,999,999.99 O 044 
Exch To Sales Charge 
Rate 4 
1009 1012 4 N 9.999 
Must be provided (but allowed to be 
zero) if Exch To Load Type Indicator 
= 1  
OC 025 
Filler 1013 1034 22 A/N Space R  
Start of ‘To’ section #5 (optional, used to report additional sales charge rate) 

---

## Page 99

Variable Length Record Layouts (Part 1) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 99 
 
Field Name  Start End Len Type Description  Opt/ Req Reject 
Code 
Exch To Gross Money 
Amount 5 
1035 1050 16 N 99,999,999,999,999.99  R 019 
Exch To Money 
Amount Due 5 
1051 1066 16 N 99,999,999,999,999.99  R 026 
Exch To Total Share 
Quantity 5 
1067 1080 14 N 9,999,999,999.9999  R 019 
Exch To Price Per 
Share 5 
1081 1092 12 N 999,999.999999  R 027 
Exch To Firm 
Concession 5 
1093 1101 9 N 9,999,999.99  O 044 
Exch To Sales Charge 
Rate 5 
1102 1105 4 N 9.999  
Must be provided (but allowed to be 
zero) if Exch To Load Type Indicator 
= 1  
OC 025 
Filler 1106 1127 22 A/N Space R  
 
 

---

## Page 100

Variable Length Record Layouts (Part 1) 
Appendix – Summary of Changes 100 
 
APPENDIX – SUMMARY OF CHANGES 
The following Summary of Changes are listed in chronological order, starting with the most recent changes.  
 
 

---

## Page 101

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q2  05/15/2023 101 
 
SUMMARY OF CHANGES – EFFECTIVE Q2  05/15/2023 
1. New Data Field in Existing Record Sequence 
New Data Field  Location  Record Type Section  
IRS 529 Annual Strategy 
Change Counter 
start 825, end 825, 
length 1 
ACATS Transfer (018)  Section 02.11.01 
start 215, end 215, 
length 1 
ACATS Transfer Acknowledgement / 
Rejection (019) 
Section 02.12.01 
Earnings to Date Money 
Amount 
start 826, end 841, 
length 16 
ACATS Transfer (018) Section 02.11.01 
start 216, end 231, 
length 16 
ACATS Transfer Acknowledgement / 
Rejection (019) 
Section 02.12.01 
Negative Earnings to Date 
Indicator 
start 842, end 842, 
length 1 
ACATS Transfer (018) Section 02.11.01 
start 232, end 232, 
length 1 
ACATS Transfer Acknowledgement / 
Rejection (019) 
Section 02.12.01 
Cost  Basis Money Amount start 922, end 937, 
length 16 
ACATS Transfer (018) Section 02.11.01 
start 233, end 248, 
length 16 
ACATS Transfer Acknowledgement / 
Rejection (019) 
Section 02.12.01 
 
 
2. New Reject Code 
The following new [[NSCC]] reject code will be utilized to reject an invalid IRS 529 Annual Strategy Change Counter:  
Reject Code Description 
   287  IRS 529 Annual Strategy Change Counter is invalid 
 

---

## Page 102

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q1 03/28/2022 102 
 
SUMMARY OF CHANGES – EFFECTIVE Q1 03/28/2022 
1. Requirements Changed for Existing Fields 
Requirements have been changed for the following fields: 
Field Name Location Modified requirement 
Record Length Order record (001) 
 
start 1, end 4, length 4 
Before change 
With no SSN/EIN Suffix: 
0290, 0383, 0476,  
0569. 
 
0569 is required when “Redemption Fee Indicator” is 
pr
ovided, “[[Asset]] Type Indicator” = Q, U, V or W, or 
“Market [[Liquidity]] Fee/Redemption Gate Indicator” is 
provided. 
With SSN/EIN Suffix: 
Up to 1592  
 
After change 
With no SSN/EIN Suffix: 
0290, 0383, 0476,  
0569, 0662 
 
0569 is required when “Redemption Fee Indicator” is 
provided, “[[Asset]] Type Indicator” = Q, U, V or W, or 
“Market [[Liquidity]] Fee/ 
Redemption Gate Indicator” is provided.  
With SSN/EIN Suffix: 
Up to 1685 
 

---

## Page 103

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q1 03/28/2022 103 
 
Field Name Location Modified requirement 
 As-Of Order record (004) 
Confirmation (005) 
Reconfirmation (006) 
Fund Originated Order (007) 
Fund As-Of Originated Order 
(009) 
Post Cancellation by Fund 
(140) 
 
Before change 
For record type 004 With no SSN/EIN Suffix: 
0290, 0383, 0476, 0569, 0662 
For record type 004 With SSN/EIN Suffix: 
Up to 1685  
For all other record types: 
0569, 0662  
 
0662 is required under the following conditions: 
• Redemption Fee Indicator is provided.  
• [[Asset]] Type is Q, U, V, or W (Optional for all other 
[[Asset]] Types. 
Money Market [[Liquidity]] Fee/Redemption Gate 
Indicator is provided. 
 
After change 
For record type 004 With no SSN/EIN Suffix: 
0290, 0383, 0476, 0569, 0662, 0755 
For record type 004 With SSN/EIN Suffix: 
Up to 1685, 1778  
For all other record types: 
0569, 0662, 0755 
 
0662 is required under the following conditions: 
• Redemption Fee Indicator is provided.  
• [[Asset]] Type is Q, U, V, or W (Optional for all other 
[[Asset]] Types. 
Money Market [[Liquidity]] Fee/Redemption Gate 
Indicator is provided. 
 
0755 is required if [[intermediary]] Program 
Indicator, Servicing Group, and Additional 
Relationship information is provided. 
 Full Registration (401) Before change 
0383, 0476, 0569, 0662, 0755 
(With 0 payables/beneficiaries, Not allowed for 
Section 529 (Registration Type = 1)).  
0848, 0941, 1034, 1127  
(With 1 payable/beneficiary) 
1220, 1313, 1406, 1499  
(With 2 payables/beneficiaries) 
1592, 1685, 1778, 1871  
(With 3 payables/beneficiaries) 
1964, 2057, 2150, 2243  
(With 4 payables/beneficiaries) 

---

## Page 104

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q1 03/28/2022 104 
 
Field Name Location Modified requirement 
2336, 2429, 2522, 2615  
(With 5 payables/beneficiaries) 
2708, 2801, 2894, 2987  
(With 6 payables/beneficiaries) 
3080 
(record length must be 3080 if FATCA attributes are 
included) 
 
After change 
0383, 0476, 0569, 0662, 0755 
(With 0 payables/beneficiaries, Not allowed for 
Section 529 (Registration Type = 1)).  
0848, 0941, 1034, 1127  
(With 1 payable/beneficiary) 
1220, 1313, 1406, 1499  
(With 2 payables/beneficiaries) 
1592, 1685, 1778, 1871  
(With 3 payables/beneficiaries) 
1964, 2057, 2150, 2243  
(With 4 payables/beneficiaries) 
2336, 2429, 2522, 2615  
(With 5 payables/beneficiaries) 
2708, 2801, 2894, 2987  
(With 6 payables/beneficiaries) 
3080 
(record length must be 3080 if FATCA attributes are 
included) 
3173 
(record length must be 3173 if [[intermediary]] 
Program Indicator, Servicing Group, and 
Additional Relationship information is included) 

---

## Page 105

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q1 03/28/2022 105 
 
Field Name Location Modified requirement 
 Correction (003) 
Correction Confirmation (025) 
Post [[settlement]] Correction by 
Fund (026) 
Before change 
With no SSN/EIN Suffix: 
0290, 0383, 0476, 0569, 0662, 0755, 0848, 0941, 
1034, 1127, 1220 
 
(Must be 0569 or greater for all record types except 
003) 
 
0662 is required when “Redemption Fee Indicator” is 
provided or “[[Asset]] Type Indicator” = Q, U, V or W or 
“Money Market [[Liquidity]] Fee/Redemption Gate 
Indicator” is provided. 
 
After change 
With no SSN/EIN Suffix: 
0290, 0383, 0476, 0569, 0662, 0755, 0848, 0941, 
1034, 1127, 
1220, 1313 
(Must be 0569 or greater for all record types except 
003) 
 
0662 is required when “Redemption Fee Indicator” is 
provided or “[[Asset]] Type Indicator” = Q, U, V or W or 
“Money Market [[Liquidity]] Fee/Redemption Gate 
Indicator” is provided. 
 
1313 is required if [[intermediary]] Program 
Indicator, Servicing Group, and Additional 
Relationship information is provided. 
Transaction Code Order (001) 
Confirmation (005) 
Reconfirmation (006) 
Correction (003) 
Correction Confirmation (025) 
Before change 
01 = Initial purchase 
02 = Subsequent purchase 
03 = Partial [[liquidation]] 
04 = Full [[liquidation]] 
 
After change 
01 = Initial purchase 
02 = Subsequent purchase 
03 = Partial [[liquidation]] 
04 = Full [[liquidation]] 
 
For Security Type = 48 (Interval Fund) future 
dated orders, only 03 and 04 are allowed. 

---

## Page 106

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q1 03/28/2022 106 
 
Field Name Location Modified requirement 
Trade Date Order (001) 
Confirmation (005) 
Reconfirmation (006) 
Correction (003) 
Correction Confirmation (025) 
Before change 
mmddccyy 
 
After change 
mmddccyy 
Future trade date is allowed if Security Type = 48 
(Interval Fund) and Transaction Code = 03 
(Partial [[liquidation]]) or 04 (Full [[liquidation]]). 
 
Best Practice: 
Trade Date for future dated Interval Fund 
repurchase orders should be populated with the 
Repurchase Pricing Date communicated by the 
Fund. 
Anticipated [[settlement]] Date Order (001) 
Correction (003) 
Before change 
mmddccyy 
For Security Issue Type = 63, Required if [[settlement]] 
Override Reason Code is space 
For other Security Types: 
1. Required if [[settlement]] Override Reason Code 
is provided and is not 04 or 06 (x-[[settlement]]). 
2. Not allowed if [[settlement]] Override Reason 
Code = 04. 
 
After change 
mmddccyy 
 
For Security Issue Type = 63, Required if [[settlement]] 
Override Reason Code is space 
For other Security Types: 
1. Required if [[settlement]] Override Reason Code 
is provided and is not 04 or 06 (x-[[settlement]]). 
2. Not allowed if [[settlement]] Override Reason 
Code = 04. 
 
This field should not be populated when Security 
Type = 48, and Transaction Code = 03 (Partial 
[[liquidation]]) or 04 (Full [[liquidation]]). If populated, 
[[NSCC]] will [[default]] the value to 12319999 and pass 
the order to the Fund. 

---

## Page 107

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q1 03/28/2022 107 
 
Field Name Location Modified requirement 
Trade Date Forward Indicator Order (001) 
Confirmation (005) 
Reconfirmation (006) 
Correction (003) 
Correction Confirmation (025) 
Before change: 
0 = Trade Date not forwarded  
1 = Trade Date forwarded  
Must be 1 if Trade Date not equal Submission Date.  
 
After change: 
0 = Trade Date not forwarded  
1 = Trade Date forwarded  
Must be 1 if Trade Date not equal Submission Date.  
 
Trade Date forwarded is only allowed if: 
• Security Type = 48 (Interval Fund) and 
Transaction Code = 03 (Partial [[liquidation]]) or 
04 (Full [[liquidation]]). 
• Security Type = 62 or 63 
2. New Data Fields 
The following fields have been added to existing layouts: 
New Name Location Layout Section  
De-minimis repurchase waiver 
code 
 
start 286 end 286, 
length 1 
Order record (001)  Section 02.01.01 
 start 286 end 286, 
length 1 
Correction (003) 
 
Section 02.29.01 
[[intermediary]] Program 
Indicator – 1 
start 570, end 573, 
length 4 
Order record (001) Section 02.01.01 
start 663, end 666, 
length 4 
As-Of Order record (004) 
Confirmation (005) 
Reconfirmation (006) 
Fund Originated Order (007) 
Fund As-Of Originated Order 
(009) 
Post Cancellation by Fund (140) 
Section 02.02.01 
start 3081, end 3084, 
length 4 
Full Registration (401) Section 02.10.01 

---

## Page 108

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q1 03/28/2022 108 
 
New Name Location Layout Section  
start 1221, end 1224, 
length 4 
Correction (003) 
Correction Confirmation (025) 
Post [[settlement]] Correction by 
Fund (026) 
Section 02.29.01 
[[intermediary]] Program 
Indicator – 2 
start 574, end 577, 
length 4 
Order record (001) Section 02.01.01 
start 667, end 670, 
length 4 
As-Of Order record (004) 
Confirmation (005) 
Reconfirmation (006) 
Fund Originated Order (007) 
Fund As-Of Originated Order 
(009) 
Post Cancellation by Fund (140) 
Section 02.02.01 
start 3085, end 3088, 
length 4 
Full Registration (401) Section 02.10.01 
start 1225, end 1228, 
length 4 
Correction (003) 
Correction Confirmation (025) 
Post [[settlement]] Correction by 
Fund (026) 
Section 02.29.01 
Servicing Group [[ID]] start 578, end 586, 
length 9 
Order record (001) Section 02.01.01 
start 671, end 679, 
length 9 
As-Of Order record (004) 
Confirmation (005) 
Reconfirmation (006) 
Fund Originated Order (007) 
Fund As-Of Originated Order 
(009) 
Post Cancellation by Fund (140) 
Section 02.02.01 
start 3089, end 3097, 
length 9 
Full Registration (401) Section 02.10.01 
start 1229, end 1237, 
length 9 
Correction (003) 
Correction Confirmation (025) 
Post [[settlement]] Correction by 
Fund (026) 
Section 02.29.01 
Additional Relationship [[ID]] – 1 start 587, end 606, 
length 20 
Order record (001) Section 02.01.01 

---

## Page 109

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q1 03/28/2022 109 
 
New Name Location Layout Section  
start 680, end 699, 
length 20 
As-Of Order record (004) 
Confirmation (005) 
Reconfirmation (006) 
Fund Originated Order (007) 
Fund As-Of Originated Order 
(009) 
Post Cancellation by Fund (140) 
Section 02.02.01 
start 3098 end 3117, 
length 20 
Full Registration (401) Section 02.10.01 
start 1238, end 1257, 
length 20 
Correction (003) 
Correction Confirmation (025) 
Post [[settlement]] Correction by 
Fund (026) 
Section 02.29.01 
Additional Relationship [[ID]] – 2 start 607, end 626, 
length 20 
Order record (001) Section 02.01.01 
start 700, end 719, 
length 20 
As-Of Order record (004) 
Confirmation (005) 
Reconfirmation (006) 
Fund Originated Order (007) 
Fund As-Of Originated Order 
(009) 
Post Cancellation by Fund (140) 
Section 02.02.01 
start 3118 end 3137, 
length 20 
Full Registration (401) Section 02.10.01 
start 1258, end 1277, 
length 20 
Correction (003) 
Correction Confirmation (025) 
Post [[settlement]] Correction by 
Fund (026) 
Section 02.29.01 

---

## Page 110

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q1 03/28/2022 110 
 
3. New Optional Record Type 
Record Type Description Section 
030 Interval Fund Acknowledgement Record 02.32.01 
4. New Reject Code 
The following new [[NSCC]] reject code will be utilized to reject an invalid de-minimis repurchaser waiver code: 
Reject Code Description 
286  De-minimis repurchase waiver code is invalid 
5. Notes Added to Existing Field 
The following notes were added to the Security Issue Type field to describe existing functionality. This is a 
document update only and there are no changes to existing logic. 
Field Name Location Modified Description 
Security Issue Type  Record Types: 
001, 004/005/006/007/009/140, 003/025/026, 200/201, 
015, 016/017/021, 200/201, 400, 401, 011, 139, 
101/102/109/112/113/214, 100/108/114/129, 002. 
Required if 24 (Money Market) 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value against 
the Fund/SERV Security master file. 
[[NSCC]] leverages the Fund/SERV 
Security master file to determine 
value and associated processing 
rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 

---

## Page 111

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q1 03/25/2019 111 
 
SUMMARY OF CHANGES – EFFECTIVE Q1 03/25/2019 
Reject Codes 
The following new [[NSCC]] reject code will be utilized to reject transactions that fail Ocode validation:  
Reject Code Description 
285 [[participant]] is not valid for the Submitter and/or Product 

---

## Page 112

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q4 11/20/2017 112 
 
SUMMARY OF CHANGES – EFFECTIVE Q4 11/20/2017 
1. New Values Added to Existing Fields 
New values have been added to the following fields: 
Field Name Location Added Values and Updated Notes 
1.Transaction Type  Order record (001) 
 
As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Fund Originated Order record 
(007) 
Fund Originated As-Of Order 
record (009) 
Post [[settlement]] Cancellation 
by Fund record (140) 
 
Correction record (003) 
Correction Confirmation 
record (025) 
Post [[settlement]] Correction by 
Fund record (026) 
 
 
start 61, end 61, length 1 
Before change 
 
0 = Single purchase 
1 = Letter of intent 
2 = Rights of accumulation 
3 = Net [[Asset]] value 
4 = Group purchase 
5 = CDSC [[liquidation]] 
8 = 529 [[participant]] Distribution  
9 = 529 Beneficiary Distribution 
A = 529 School Distribution 
B = 529 Rollover Distribution 
 
(8 thru B only allowed if Transaction Code = “03” or 
“04”) 
 
After change 
 
0 = Single purchase 
1 = Letter of intent 
2 = Rights of accumulation 
3 = Net [[Asset]] value 
4 = Group purchase 
5 = CDSC [[liquidation]] 
8 = 529 [[participant]] Distribution  
9 = 529 Beneficiary Distribution 
A = 529 School Distribution 
B = 529 Rollover Distribution 
E = 529 In-State Plan Transfer Distribution 
F = 529 Registration Change 
 
Only 5, 8, 9, A, B, E or F are allowed if Transaction 
Code = “03” or “04” 
03 (Partial [[liquidation]])  

---

## Page 113

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q4 11/20/2017 113 
 
Field Name Location Added Values and Updated Notes 
04 (Full [[liquidation]]) 
[[Asset]] Type Indicator Order record (001) 
 
As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Fund Originated Order record 
(007) 
Fund Originated As-Of Order 
record (009) 
Post [[settlement]] Cancellation 
by Fund record (140) 
 
Correction record (003) 
Correction Confirmation 
record (025) 
Post [[settlement]] Correction by 
Fund record (026) 
 
start 160, end 160, length 1 
Before change 
 
0 = Not applicable 
1 = Current year payment 
2 = Prior year payment 
3 = IRA rollover 
4 = [[Asset]] transfer 
5 = Employee - prior year 
6 = Employee - current year 
7 = Employer - prior year 
8 = Employer - current year 
9 = Non-fund prototype IRA 
A = Non-fund qualified plan 
C = Salary Reduction Contribution  
D = 529 Current Year Contribution  
E = UGMA account transferred to Section 529 Account  
F = 529 Underlying Fund Trades 
G = Share Class Conversion 
H = Health Savings Account 
I = Insurance Fund Transactions 
J = Non-Qualified Retirement Plan 
K = Qualified Retirement Plan 
L = Omnibus [[Dividend]] Reconciliation 
M = Variable Annuity 
N = Wrap Program 
O = Defined Benefit Plan 
P = 529 Previous Year Contribution 
Q = 529 Rollover Contribution  
S = Omnibus Short-Term Capital Gain Reconciliation 
T = Omnibus Long-Term Capital Gain Reconciliation 
Note: 
D, P, and Q indicate Section 529 Plan. 
After change 
 
0 = Not applicable 
1 = Current year payment 

---

## Page 114

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q4 11/20/2017 114 
 
Field Name Location Added Values and Updated Notes 
2 = Prior year payment 
3 = IRA rollover 
4 = [[Asset]] transfer 
5 = Employee - prior year 
6 = Employee - current year 
7 = Employer - prior year 
8 = Employer - current year 
9 = Non-fund prototype IRA 
A = Non-fund qualified plan 
C = Salary Reduction Contribution  
D = 529 Current Year Contribution  
E = UGMA account transferred to Section 529 Account  
F = 529 Underlying Fund Trades 
G = Share Class Conversion 
H = Health Savings Account 
I = Insurance Fund Transactions 
J = Non-Qualified Retirement Plan 
K = Qualified Retirement Plan 
L = Omnibus [[Dividend]] Reconciliation 
M = Variable Annuity 
N = Wrap Program 
O = Defined Benefit Plan 
P = 529 Previous Year Contribution 
Q = 529 Rollover Contribution  
S = Omnibus Short-Term Capital Gain Reconciliation 
T = Omnibus Long-Term Capital Gain Reconciliation 
U = 529 In-State Plan Transfer Contribution 
V = 529 Owner Change 
W = 529 Beneficiary Change-In-Family  
Note: 
D, P, Q, U, V and W indicate Section 529 Plan. 
[[liquidation]] Indicator Order record (001) 
 
As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Fund Originated Order record 
(007) 
Fund Originated As-Of Order 
Before change 
 
Required if Trans Type = 5. 
1 = Gross 
2 = Net 
4 = Correction 

---

## Page 115

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q4 11/20/2017 115 
 
Field Name Location Added Values and Updated Notes 
record (009) 
Post [[settlement]] Cancellation 
by Fund record (140) 
 
Correction record (003) 
Correction Confirmation 
record (025) 
Post [[settlement]] Correction by 
Fund record (026) 
 
start 267, end 267, length 1 
5 = Death 
6 = Disability 
7 = Mandatory distribution 
8 = Systematic withdrawal 
9 = Defined contribution 
A = Hardship 
B = No commission paid  
Note: 
4 through B should apply only to transactions with 
CDSC Waivers 
After change 
 
Required if Trans Type = 5 
(CDSC [[liquidation]]) 
1 = Gross 
2 = Net 
4 = Correction 
5 = Death 
6 = Disability 
7 = Mandatory distribution 
8 = Systematic withdrawal 
9 = Defined contribution 
A = Hardship 
B = No commission paid  
C = 529 Plan-Specific 
D = 529 Plan Account – Beneficiary Disability 
E = 529 Plan Account – Beneficiary Death 
F = 529 Plan Account – Beneficiary Scholarship 
Notes: 
• 4 through F should apply only to transactions 
with CDSC Waivers 
• C through F should only apply to Section 529 
plans. 
IRA/529 [[liquidation]] Indicator Order record (001) 
 
As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Fund Originated Order record 
Before change 
 
0 = Not applicable 
1 = Distribution – premature 

---

## Page 116

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q4 11/20/2017 116 
 
Field Name Location Added Values and Updated Notes 
(007) 
Fund Originated As-Of Order 
record (009) 
Post [[settlement]] Cancellation 
by Fund record (140) 
 
Correction record (003) 
Correction Confirmation 
record (025) 
Post [[settlement]] Correction by 
Fund record (026) 
 
start 354, end 354, length 1 
2 = Distribution – disability 
3 = Distribution – death 
4 = Distribution – normal 
5 = Hardship withdrawal 
6 = Loan  
7 = Rollover 
8 = Adjust prior year excess 
9 = Adjust current year excess 
A = Qualified  
B = Non-Qualified  
 
A and B are required if Transaction Type = 8, 9, A or B 
 
After change 
 
0 = Not applicable 
1 = Distribution – premature 
2 = Distribution – disability 
3 = Distribution – death 
4 = Distribution – normal 
5 = Hardship withdrawal 
6 = Loan  
7 = Rollover 
8 = Adjust prior year excess 
9 = Adjust current year excess 
A = Qualified  
B = Non-Qualified  
C = Distribution – Non-Taxable 
D = 529 Owner Change 
E = 529 Beneficiary Change – In-Family  
Notes: 
A and B are required if Transaction Type =  
8 = (529 [[participant]] Distribution) 
9 = (529 Beneficiary Distribution) 
A = (529 School Distribution)  
B = (529 Roll Over Distribution 
C is required if Transaction Type = E (529 In-State 
Plan Transfer Distribution) 

---

## Page 117

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q4 11/20/2017 117 
 
Field Name Location Added Values and Updated Notes 
D or E is required if Transaction Type = F (529 
Registration Change) 
 
2. Requirements Changed for Existing Fields 
Requirements have been changed for the following fields: 
Field Name Location Modified requirement 
Record Length Order record (001) 
As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Fund Originated Order record 
(007) 
Fund Originated As-Of Order 
record (009) 
Post [[settlement]] Cancellation by 
Fund record (140) 
start 1, end 4, length 4 
Before change 
 
With no SSN/EIN Suffix: 
0290, 0383, 0476,  
0569. 
0569 is required when “Redemption Fee Indicator” is 
provided, “[[Asset]] Type Indicator” = Q, or “Market 
[[Liquidity]] Fee/Redemption Gate Indicator” is provided. 
 
With SSN/EIN Suffix: 
Up to 1592  
 
After change 
 
With no SSN/EIN Suffix: 
0290, 0383, 0476,  
0569. 
0569 is required when “Redemption Fee Indicator” is 
provided, “[[Asset]] Type Indicator” = Q, U, V or W, or 
“Market [[Liquidity]] Fee/Redemption Gate Indicator” is 
provided.  
With SSN/EIN Suffix: 
Up to 1592  

---

## Page 118

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q4 11/20/2017 118 
 
Field Name Location Modified requirement 
 As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Fund Originated Order record 
(007) 
Fund Originated As-Of Order 
record (009) 
Post [[settlement]] Cancellation by 
Fund record (140) 
 
start 1, end 4, length 4 
Before change 
 
For record type 004 Wit h no SSN/EIN Suffix: 
0290, 0383, 0476, 0569, 0662 
For record type 004 With SSN/EIN Suffix: 
Up to 1685  
For all other record types: 
0569, 0662  
0662 is required under the following conditions: 
• Redemption Fee Indicator is provided.  
• [[Asset]] Type is Q (Optional for all other [[Asset]] 
Types. 
Money Market [[Liquidity]] Fee/Redemption Gate 
Indicator is provided. 
 
After change 
 
For record type 004 With no SSN/EIN Suffix: 
0290, 0383, 0476, 0569, 0662 
 
For record type 004 With SSN /EIN Suffix: 
Up to 1685  
 
For all other record types: 
0569, 0662  
 
0662 is required under the following conditions: 
• Redemption Fee Indicator is provided.  
• [[Asset]] Type is Q, U, V, or W (Optional for all other 
[[Asset]] Types.) 
• Money Market [[Liquidity]] Fee/Redemption Gate 
Indicator is provided. 

---

## Page 119

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q4 11/20/2017 119 
 
Field Name Location Modified requirement 
Correction record (003) 
Correction Confirmation record 
(025) 
Post [[settlement]] Correction by 
Fund record (026) 
 
start 1, end 4, length 4 
Before change 
 
With no SSN/EIN Suffix: 
0290, 0383, 0476, 0569, 0662, 0755, 0848, 0941, 
1034, 1127, 
1220 
(Must be 0569 or greater for all record types except 
003) 
 
0662 is required when “Redemption Fee Indicator” is 
provided or “[[Asset]] Type Indicator” = Q, or “Money 
Market [[Liquidity]] Fee/Redemption Gate Indicator” is 
provided. 
 
After change 
 
With no SSN/EIN Suffix: 
0290, 0383, 0476, 0569, 0662, 0755, 0848, 0941, 
1034, 1127, 
1220 
(Must be 0569 or greater for all record types except 
003) 
 
0662 is required when “Redemption Fee Indicator” is 
provided or “[[Asset]] Type Indicator” = Q, U, V, W or 
“Money Market [[Liquidity]] Fee/Redemption Gate 
Indicator” is provided. 

---

## Page 120

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q4 11/20/2017 120 
 
Field Name Location Modified requirement 
Beneficiary SSN/EIN Number Order record (001) 
 
As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Fund Originated Order record 
(007) 
Fund Originated As-Of Order 
record (009) 
Post [[settlement]] Cancellation 
by Fund record (140) 
 
Correction record (003) 
Correction Confirmation record 
(025) 
Post [[settlement]] Correction by 
Fund record (026) 
 
start 367, end 375, length 9 
Before change 
 
Required if [[Asset]] Type Indicator = D, E, P or Q and 
Transaction Code = 01 or 02 
 
After change 
 
Required if [[Asset]] Type Indicator = D, E, P, Q, U, V, 
or W and Transaction Code = 01 or 02 
 
[[Asset]] Type Indicators 
D (529 Current Year Contribution)  
E (UGMA account transferred to Section 529 
Account)  
P (529 Previous Year Contribution) 
Q (529 Rollover Contribution)  
U (529 In-State Plan Transfer Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change-In-Family)  
 
Transaction Codes 
01 (Initial purchase) 
02 (Subsequent purchase) 

---

## Page 121

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q4 11/20/2017 121 
 
Field Name Location Modified requirement 
Cost Basis Money Amount Order record (001) 
 
start 514 end 529, length 16 
 
As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Fund Originated Order record 
(007) 
Fund Originated As-Of Order 
record (009) 
Post [[settlement]] Cancellation 
by Fund record (140) 
 
Correction record (003) 
Correction Confirmation record 
(025) 
Post [[settlement]] Correction by 
Fund record (026) 
 
start 607 end 622, length 16 
Before change 
 
Required if the [[Asset]] Type Indicator = Q. 
Format: 
99,999,999,999,999.99 
 
After change 
Required if the [[Asset]] Type Indicator = Q. U, V or W. 
Q (529 Rollover Contribution)  
U (529 In-State Plan Transfer Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change-In-Family)  
 
Format: 
99,999,999,999,999.99 
Zeros are allowed (added 9/25/2017) 
Earnings to Date Money Amount Order record (001) 
 
start 530, end 545, length 16 
 
As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Fund Originated Order record 
(007) 
Fund Originated As-Of Order 
record (009) 
Post [[settlement]] Cancellation by 
Fund record (140) 
 
Correction record (003) 
Correction Confirmation record 
(025) 
Post [[settlement]] Correction by 
Fund record (026) 
 
start 623, end 638, length 16 
Required if the [[Asset]] Type Indicator = Q. 
 
Format: 
99,999,999,999,999.99 
 
Required if the [[Asset]] Type Indicator = Q. U, V or W. 
Q (529 Rollover Contribution)  
U (529 In-State Plan Transfer Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change-In-Family)  
Format: 
99,999,999,999,999.99 
Zeros are allowed (added 9/25/2017) 

---

## Page 122

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q4 11/20/2017 122 
 
3. Modified Description of Existing Field 
Field Name Location Changes to Description 
Transaction Code  Order record (001) 
start 62, end 63, length 2 
Before change 
 
01 = Initial purchase 
02 = Subsequent purchase 
03 = Partial [[liquidation]] 
04 = Full [[liquidation]] 
Must be 03 or 04 if Transaction Type = 5 
 
After change 
01 = Initial purchase 
02 = Subsequent purchase 
03 = Partial [[liquidation]] 
04 = Full [[liquidation]] 
** Note: 
Transaction type 5 condition was moved to 
Transaction Type field to be consistent with other 
conditions 

---

## Page 123

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 123 
 
SUMMARY OF CHANGES – EFFECTIVE Q3 09/26/2016 
1. New Fields 
The following fields have been added to existing layouts: 
New Name Location Layout Section  
1. Money Market [[Liquidity]] 
Fee/Redemption Gate Indicator 
start 547, end 547, length 1 Order record (001) Section 02.01.01 
start 640, end 640, length 1 As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Post [[settlement]] Cancellation 
by Fund record (140) 
Section 02.02.01 
start 640, end 640, length 1 Correction record (003) 
Correction Confirmation record 
(025) 
Post [[settlement]] Correction by 
Fund record (026) 
Section 02.29.01 
start 357, end 357, length 1 Exchange Order record (015) Section 02.06.01 
start 357, end 357, length 1 Exchange Confirmation record 
(016) 
Exchange Reconfirmation 
record (017) 
Post [[settlement]] Exchange 
Cancellation record (021) 
Section 02.07.01 
2. Transaction Received Date start 548, end 555, length 8 Order record (001) Section 02.01.01 
start 641, end 648, length 8 As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Post [[settlement]] Cancellation 
by Fund record (140) 
Section 02.02.01 
start 641, end 648, length 8 Correction record (003) 
Correction Confirmation record 
(025) 
Post [[settlement]] Correction by 
Fund record (026) 
Section 02.29.01 
start 358, end 365, length 8 Exchange Order record (015) Section 02.06.01 
start 358, end 365, length 8 Exchange Confirmation record 
(016) 
Exchange Reconfirmation 
record (017) 
Post [[settlement]] Exchange 
Cancellation record (021) 
Section 02.07.01 
3. Aggregated Order Indicator start 556, end 556, length 1 Order record (001) Section 02.01.01 

---

## Page 124

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 124 
 
New Name Location Layout Section  
start 649, end 649, length 1 As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Post [[settlement]] Cancellation 
by Fund record (140) 
Section 02.02.01 
start 649, end 649, length 1 Correction record (003) 
Correction Confirmation record 
(025) 
Post [[settlement]] Correction by 
Fund record (026) 
Section 02.29.01 
start 366, end 366, length 1 Exchange Order record (015) Section 02.06.01 
start 366, end 366, length 1 Exchange Confirmation record 
(016) 
Exchange Reconfirmation 
record (017) 
Post [[settlement]] Exchange 
Cancellation record (021) 
Section 02.07.01 
2. Renamed Fields 
The following fields have been renamed: 
New Name Old Name Records Affected 
1. Transaction Received Time [[participant]] Processing Time Order record (001) 
As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Fund Originated Order record (007) 
Fund Originated As-Of Order record (009) 
Post [[settlement]] Cancellation by Fund record 
(140) 
Correction record (003) 
Correction Confirmation record (025) 
Post [[settlement]] Correction by Fund record (026) 
Exchange Order record (015) 
Exchange Confirmation record (016) 
Exchange Reconfirmation record (017) 
Post [[settlement]] Exchange Cancellation record 
(021) 
Order Acknowledgment for Money Market 
Purchase record (101) 
Firm Delete record (102) 
Release to [[settlement]] record (109) 
Registration Acknowledgment record (112) 
Delete Pending Registration (Registered Ex-
Fund/SERV) record (113) 
Receiving Fund Exit from ToRA record (214) 

---

## Page 125

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 125 
 
New Name Old Name Records Affected 
2. Redemption Fee Rate STR Fee Rate Order record (001) 
As-Of Order record (004) 
Confirmation record (005) Reconfirmation record 
(006) 
Fund Originated Order record (007) 
Fund Originated As-Of Order record (009) 
Post [[settlement]] Cancellation by Fund record 
(140) 
Correction record (003) 
Correction Confirmation record (025) 
Post [[settlement]] Correction by Fund record (026) 
Exchange Order record (015) 
Exchange Confirmation record (016) 
Exchange Reconfirmation record (017) 
Post [[settlement]] Exchange Cancellation record 
(021) 
3. Redemption Fee Money 
Amount 
STR Fee Money Amount Order record (001) 
As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Fund Originated Order record (007) 
Fund Originated As-Of Order record (009) 
Post [[settlement]] Cancellation by Fund record 
(140) 
Correction record (003) 
Correction Confirmation record (025) 
Post [[settlement]] Correction by Fund record (026) 
Exchange Order record (015) 
Exchange Confirmation record (016) 
Exchange Reconfirmation record (017) 
Post [[settlement]] Exchange Cancellation record 
(021) 

---

## Page 126

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 126 
 
3. Requirements Changed for Existing Fields 
Requirements have been changed for the following fields: 
Field Name Location Modified requirement 
1. Transaction Received Time 
(renamed from “[[participant]] 
Processing Time”) 
Order record (001) 
 
start 168, end 173, 
length 6 
Before change 
 
Optional 
 
hhmmss  
000000 (midnight) to 235959 
 
After change 
 
Optional Conditional 
 
hhmmss Eastern Time 
000000 (midnight) to 235959 
 
Required when “Money Market [[Liquidity]] 
Fee/Redemption Gate Indicator” = ‘F’ (Fund).  
 As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Fund Originated Order record 
(007) 
Fund Originated As-Of Order 
record (009) 
Post [[settlement]] Cancellation by 
Fund record (140) 
 
start 168, end 173, length 6 
Before change 
Optional 
 
hhmmss  
000000 (midnight) to 235959 
 
After change 
 
Optional Conditional 
 
hhmmss Eastern Time 
000000 (midnight) to 235959 
 
Required when “Money Market [[Liquidity]] 
Fee/Redemption Gate Indicator” = ‘F’ (Fund). 
 
For Record Types 005 and 006: 
Must contain the same value as provided by the 
firm on the Order transaction (record type 001or 
004). [[NSCC]] will reject if a fund provided value is 
different from the value submitted by the firm. 

---

## Page 127

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 127 
 
Field Name Location Modified requirement 
 Correction record (003) 
Correction Confirmation record 
(025) 
Post [[settlement]] Correction by 
Fund record (026) 
 
start 168, end 173, length 6 
Before change 
 
Optional 
 
hhmmss  
000000 (midnight) to 235959 
 
After change 
 
Optional Conditional 
 
hhmmss Eastern Time 
000000 (midnight) to 235959 
 
Required when “Money Market [[Liquidity]] 
Fee/Redemption Gate Indicator” = ‘F’ (Fund). 
 
Record Type 025: 
Must contain the same value as provided by the 
firm on the Correction transaction (record type 
003). [[NSCC]] will reject if a fund provided value is 
different from the value submitted by the firm. 
 Exchange Order record (015 
 
start 168, end 173, length 6 
Before change 
 
Optional 
 
hhmmss  
000000 (midnight) to 235959 
 
After change 
 
Optional Conditional 
 
hhmmss Eastern Time 
000000 (midnight) to 235959 
 
Required when “Money Market [[Liquidity]] 
Fee/Redemption Gate Indicator” = ‘F’ (Fund). 

---

## Page 128

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 128 
 
Field Name Location Modified requirement 
 Exchange Confirmation record 
(016) 
Exchange Reconfirmation 
record (017) 
Post [[settlement]] Exchange 
Cancellation record (021) 
 
start 168, end 173, length 6 
Before change 
 
Optional 
 
hhmmss  
000000 (midnight) to 235959 
 
After change 
 
Optional Conditional 
 
hhmmss Eastern Time 
000000 (midnight) to 235959 
 
Required when “Money Market [[Liquidity]] 
Fee/Redemption Gate Indicator” = ‘F’ (Fund). 
For Record types 016 and 017 
Must contain the same value as provided on the 
Exchange transaction (record type 015).  
[[NSCC]] will reject if a fund provided value is 
different from the value submitted by the firm. 
2. Redemption Fee Indicator Order record (001) 
start 271, end 271, length 1 
Before change 
 
0 = Short-Term Redemption (STR) Fee 
1 = STR Fee with CDSC 
 
After change 
 
0 = Short-Term Redemption (STR) 
1 = STR with CDSC 
2 = Money Market [[Liquidity]] Fee 
3 = Money Market [[Liquidity]] Fee with CDSC 

---

## Page 129

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 129 
 
Field Name Location Modified requirement 
 As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Fund Originated Order record 
(007) 
Fund Originated As-Of Order 
record (009) 
Post [[settlement]] Cancellation 
by Fund record (140) 
 
start 271, end 271, length 1 
Before change 
 
0 = Short-Term Redemption (STR) Fee 
1 = STR Fee with CDSC 
Not allowed for record types 005 and 006 if not 
provided with the original order. Not allowed for 
record type 007 and 009 
 
After change 
 
0 = Short-Term Redemption (STR) 
1 = STR with CDSC 
2 = Money Market [[Liquidity]] Fee  
3 = Money Market [[Liquidity]] Fee with CDSC 
 
Values “0” and “1” are not allowed for record 
types 005 and 006 if this field was blank on the 
original Order transaction (record type 001 or 
004). 
 
Values “2” and “3” are allowed for record types 
005 and 006 if this field was blank on the original 
Order transaction (record type 001 or 004). 
 
Not allowed for record types 007 and 009. 

---

## Page 130

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 130 
 
Field Name Location Modified requirement 
 Correction record (003) 
Correction Confirmation record 
(025) 
Post [[settlement]] Correction by 
Fund record (026) 
 
start 271, end 271, length 1 
Before change 
 
0 = Short-Term Redemption (STR) Fee 
1 = STR Fee with CDSC 
 
Not allowed for record type 025 if not provided with 
the Correction (record type 003). 
 
After change 
 
0 = Short-Term Redemption (STR) 
1 = STR with CDSC 
2 = Money Market [[Liquidity]] Fee  
3 = Money Market [[Liquidity]] Fee with CDSC 
 
Values “0” and “1” are not allowed for record 
type 025 if this field was blank on the original 
Correction transaction (record type 003). 
 
Values “2” and “3” are allowed for record type 
025 if this field was blank on the original 
Correction transaction (record type 003).  
Exchange Order record (015) 
 
start 271, end 271, length 1 
Before change 
 
0 = Short-Term Redemption (STR) Fee 
1 = STR Fee with CDSC 
 
After change 
 
0 = Short-Term Redemption (STR) 
1 = STR with CDSC 
2 = Money Market [[Liquidity]] Fee  
3 = Money Market [[Liquidity]] Fee with CDSC 

---

## Page 131

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 131 
 
Field Name Location Modified requirement 
 Exchange Confirmation record 
(016) 
Exchange Reconfirmation 
record (017) 
Post [[settlement]] Exchange 
Cancellation record (021) 
 
start 271, end 271, length 1 
Before change 
 
0 = Short-Term Redemption (STR) Fee 
1 = STR Fee with CDSC 
 
Not allowed for record types 016 and 017 if not 
provided with the original exchange. 
 
After change 
 
0 = Short-Term Redemption (STR) 
1 = STR with CDSC 
2 = Money Market [[Liquidity]] Fee  
3 = Money Market [[Liquidity]] Fee with CDSC 
 
Values “0” and “1” are not allowed for record 
types 016 and 017 if this field was blank on the 
original Exchange transaction (record type 015). 
 
Values “2” and “3” are allowed for record types 
016 and 017 if this field was blank on the original 
Exchange transaction (record type 015). 

---

## Page 132

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 132 
 
Field Name Location Modified requirement 
3 Redemption Fee Rate 
(renamed from “STR Fee Rate”) 
Order record (001) 
start 477, end 483, length 7 
Before change 
 
Optional 
 
99.99999  
Not allowed if Redemption Fee Indicator is not 
provided 
 
After change 
 
Optional Conditional 
 
99.99999 
 
Not allowed if “Redemption Fee Indicator” is not 
provided. 
 
Required when “Redemption Fee Indicator” is 
populated with either ‘2’ (Money Market [[Liquidity]] 
Fee) or ‘3’ (Money Market [[Liquidity]] Fee with 
CDSC). 
 
Zero value is not allowed when this field is 
required and Redemption Fee Indicator =’2’ or 
‘3’. 
 
If “Redemption Fee Indicator” = 0 or 1, this field 
will be utilized to communicate a Short-Term 
Redemption (STR) Fee Rate. 

---

## Page 133

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 133 
 
Field Name Location Modified requirement 
 As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Fund Originated Order record 
(007) 
Fund Originated As-Of Order 
record (009) 
Post [[settlement]] Cancellation by 
Fund record (140) 
 
start 570, end 576, length 7 
Before change 
 
Optional 
 
99.99999 
 
Not allowed if Redemption Fee Indicator is not 
provided  
 
After change 
 
Optional Conditional 
 
99.99999 
 
Not allowed if “Redemption Fee Indicator” is not 
provided. 
 
Required when “Redemption Fee Indicator” is 
populated with either ‘2’ (Money Market [[Liquidity]] 
Fee) or ‘3’ (Money Market [[Liquidity]] Fee with 
CDSC). 
Zero value is not allowed when this field is 
required and Redemption Fee Indicator =’2’ or ‘3’. 
 
If “Redemption Fee Indicator” = 0 or 1, this field 
will be utilized to communicate a Short-Term 
Redemption (STR) Fee Rate. 

---

## Page 134

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 134 
 
Field Name Location Modified requirement 
 Correction record (003) 
Correction Confirmation record 
(025) 
Post [[settlement]] Correction by 
Fund record (026) 
 
start 570, end 576, length 7 
Before change 
 
Optional 
 
99.99999 
 
Not allowed if Redemption Fee Indicator is not 
provided  
 
After change 
 
Optional Conditional 
 
99.99999 
 
Not allowed if “Redemption Fee Indicator” is not 
provided. 
 
Required when “Redemption Fee Indicator” is 
populated with either ‘2’ (Money Market [[Liquidity]] 
Fee) or ‘3’ (Money Market [[Liquidity]] Fee with 
CDSC). 
Zero value is not allowed when this field is 
required and Redemption Fee Indicator =’2’ or 
‘3’. 
If “Redemption Fee Indicator” = 0 or 1, this field 
will be utilized to communicate a Short-Term 
Redemption (STR) Fee Rate. 

---

## Page 135

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 135 
 
Field Name Location Modified requirement 
 Exchange Order record (015) 
 
start 440, end 446, length 7 
Before change 
 
Optional 
 
99.99999  
 
Not allowed if Redemption Fee Indicator is not 
provided 
 
After change 
 
Optional Conditional 
 
99.99999 
 
Not allowed if “Redemption Fee Indicator” is not 
provided. 
 
Required when “Redemption Fee Indicator” is 
populated with either ‘2’ (Money Market [[Liquidity]] 
Fee) or ‘3’ (Money Market [[Liquidity]] Fee with 
CDSC). 
Zero value is not allowed when this field is 
required and Redemption Fee Indicator =’2’ or 
‘3’. 
 
If “Redemption Fee Indicator” = 0 or 1, this field 
will be utilized to communicate a Short-Term 
Redemption (STR) Fee Rate. 

---

## Page 136

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 136 
 
Field Name Location Modified requirement 
 Exchange Confirmation record 
(016) 
Exchange Reconfirmation 
record (017) 
Post [[settlement]] Exchange 
Cancellation record (021) 
 
start 440, end 446, length 7 
Before change 
 
Optional 
 
99.99999 
 
Not allowed if Redemption Fee Indicator is not 
provided 
 
After change 
 
Optional Conditional 
 
99.99999 
 
Not allowed if “Redemption Fee Indicator” is not 
provided. 
 
Required when “Redemption Fee Indicator” is 
populated with either ‘2’ (Money Market [[Liquidity]] 
Fee) or ‘3’ (Money Market [[Liquidity]] Fee with 
CDSC). 
Zero value is not allowed when this field is 
required and Redemption Fee Indicator =’2’ or 
‘3’. 
 
If “Redemption Fee Indicator” = 0 or 1, this field 
will be utilized to communicate a Short-Term 
Redemption (STR) Fee Rate. 

---

## Page 137

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 137 
 
Field Name Location Modified requirement 
4 Redemption Fee Money 
Amount (renamed from STR 
Fee Money Amount) 
Order record (001) 
start 498, end 513, length 16 
Before change 
 
99,999,999,999,999.99 
Required when Redemption Fee Indicator is 
provided and STR Fee Share Quantity = 0 or Space. 
Not allowed if Redemption Fee Indicator is not 
provided or if STR Fee Share Quantity > 0 
 
After change 
 
99,999,999,999,999.99 
Required when “Redemption Fee Indicator” is 
provided and STR Fee Share Quantity = 0 or 
Space. 
 
Not allowed if Redemption Fee Indicator is not 
provided or if STR Fee Share Quantity > 0. 
 
Required when “Redemption Fee Indicator” is 
populated with either ‘2’ (Money Market [[Liquidity]] 
Fee) or ‘3’ (Money Market [[Liquidity]] Fee with 
CDSC). 
 
Zero value is not allowed when this field is 
required. 
 
If “Redemption Fee Indicator” = 0 or 1, this field 
will be utilized to communicate a Short-Term 
Redemption (STR) Fee Money Amount. 

---

## Page 138

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 138 
 
Field Name Location Modified requirement 
 As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Fund Originated Order record 
(007) 
Fund Originated As-Of Order 
record (009) 
Post [[settlement]] Cancellation 
by Fund record (140) 
 
start 591, end 606, length 16 
Before change 
 
99,999,999,999,999.99 
For all record types: 
Not allowed if Redemption Fee Indicator is not 
provided. 
For record type 004: 
Required when Redemption Fee Indicator is 
provided and STR Fee Share Quantity = 0 or Space. 
Not allowed if STR Fee Share Quantity > 0 
For record types 005 and 006: 
Required when Redemption Fee Indicator is 
provided. 
 
After change 
 
99,999,999,999,999.99 
 
For all record types: 
Not allowed if “Redemption Fee Indicator” is not 
provided. 
Required when “Redemption Fee Indicator” is 
populated with either ‘2’ (Money Market [[Liquidity]] 
Fee) or ‘3’ (Money Market [[Liquidity]] Fee with 
CDSC).  
Zero value is not allowed when this field is 
required. 
 
For record type 004: 
Required when “Redemption Fee Indicator” is 
provided and STR Fee Share Quantity = 0 or 
Space. 
Not allowed if STR Fee Share Quantity > 0. 
 
For record types 005 and 006: 
Required when “Redemption Fee Indicator” is 
provided. 
 
For all record types: 
If “Redemption Fee Indicator” = 0 or 1, this field 
will be utilized to communicate a Short-Term 
Redemption (STR) Fee Money Amount. 

---

## Page 139

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 139 
 
Field Name Location Modified requirement 
 Correction record (003) 
Correction Confirmation record 
(025) 
Post [[settlement]] Correction by 
Fund record (026) 
 
start 591, end 606, length 16 
Before change 
 
99,999,999,999,999.99 
For all record types: 
Not allowed if Redemption Fee Indicator is not 
provided. 
For record type 003: 
Required when Redemption Fee Indicator is 
provided and STR Fee Share Quantity = 0 or Space. 
For record type 025: 
Required when Redemption Fee Indicator is 
provided. 
 
After change 
 
99,999,999,999,999.99 
For all record types: 
 
Not allowed if Redemption Fee Indicator is not 
provided. 
 
For record type 003: 
Required when Redemption Fee Indicator is 
provided and STR Fee Share Quantity = 0 or 
Space. 
 
For record type 025: 
Required when Redemption Fee Indicator is 
provided. 
 
For all record types: 
Required when “Redemption Fee Indicator” is 
populated with either ‘2’ (Money Market [[Liquidity]] 
Fee) or ‘3’ (Money Market [[Liquidity]] Fee with 
CDSC). 
Zero value is not allowed when this field is 
required. 
 
If “Redemption Fee Indicator” = 0 or 1, this field 
will be utilized to communicate a Short-Term 
Redemption (STR) Fee Money Amount. 

---

## Page 140

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 140 
 
Field Name Location Modified requirement 
 Exchange Order record (015) 
 
start 461, end 476, length 16 
Before change 
 
99,999,999,999,999.99 
Required when Redemption Fee Indicator is 
provided and STR Fee Share Quantity = 0 or Space. 
Not allowed if Redemption Fee Indicator is not 
provided or if STR Fee Share Quantity > 0 
 
After change 
 
99,999,999,999,999.99 
Required when “Redemption Fee Indicator” is 
provided and STR Fee Share Quantity = 0 or 
Space.  
Not allowed if Redemption Fee Indicator is not 
provided or if STR Fee Share Quantity > 0. 
 
Required when “Redemption Fee Indicator” is 
populated with either ‘2’ (Money Market [[Liquidity]] 
Fee) or ‘3’ (Money Market [[Liquidity]] Fee with 
CDSC). 
Zero value is not allowed when this field is 
required. 
 
If “Redemption Fee Indicator” = 0 or 1, this field 
will be utilized to communicate a Short-Term 
Redemption (STR) Fee Money Amount. 

---

## Page 141

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 141 
 
Field Name Location Modified requirement 
Exchange Confirmation record 
(016) 
Exchange Reconfirmation 
record (017) 
Post [[settlement]] Exchange 
Cancellation record (021) 
 
start 461, end 476, length 16 
Before change 
 
99,999,999,999,999.99 
 
For all record types 
Not allowed if Redemption Fee Indicator is not 
provided. 
For record types 016 and 017: 
Required when Redemption Fee Indicator is 
provided. 
 
After change 
 
99,999,999,999,999.99 
 
For all record types 
Not allowed if Redemption Fee Indicator is not 
provided. 
 
For record types 016 and 017: 
Required when Redemption Fee Indicator is 
provided. 
 
For all record types: 
Required when “Redemption Fee Indicator” is 
populated with either ‘2’ (Money Market [[Liquidity]] 
Fee) or ‘3’ (Money Market [[Liquidity]] Fee with 
CDSC). 
Zero value is not allowed when this field is 
required. 
 
If “Redemption Fee Indicator” = 0 or 1, this field 
will be utilized to communicate a Short-Term 
Redemption (STR) Fee Money Amount. 

---

## Page 142

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 142 
 
Field Name Location Modified requirement 
5. STR Fee Share Quantity Order record (001) 
start 484, end 497, length 14 
Before change 
 
9,999,999,999.9999 
 
Required when Redemption Fee Indicator is provided 
and STR Fee Money Amount = 0 or Space. 
Not allowed if Redemption Fee Indicator is not 
provided or if STR Fee Money Amount > 0 
 
After change 
 
9,999,999,999.9999 
 
Required when Redemption Fee Indicator is 
provided and Redemption Fee Money Amount = 0 
or Space. 
Not allowed if Redemption Fee Indicator is not 
provided or if Redemption Fee Money Amount > 
0. 
 
Not allowed when “Redemption Fee Indicator” is 
populated with either ‘2’ (Money Market [[Liquidity]] 
Fee) or ‘3’ (Money Market [[Liquidity]] Fee with 
CDSC).  

---

## Page 143

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 143 
 
Field Name Location Modified requirement 
` As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Fund Originated Order record 
(007) 
Fund Originated As-Of Order 
record (009) 
Post [[settlement]] Cancellation 
by Fund record (140) 
 
start 577, end 590, length 14 
Before change 
 
9,999,999,999.9999 
 
For all record types: 
Not allowed if Redemption Fee Indicator is not 
provided. 
For record type 004: 
Required when Redemption Fee Indicator is 
provided and STR Fee Money Amount = 0 or Space. 
Not allowed if STR Fee Money Amount > 0 
For record types 005 and 006: 
If zero or Space, and Redemption Fee Indicator is 
provided, will not override the STR Fee Share 
Quantity in the database. 
 
After change 
 
9,999,999,999.9999 
 
For all record types: 
Not allowed if “Redemption Fee Indicator” is not 
provided. 
 
For record type 004: 
Required when “Redemption Fee Indicator” is 
provided and “Redemption Fee Money Amount” 
= 0 or Space. 
Not allowed if “Redemption Fee Money Amount” 
> 0. 
 
For record types 005 and 006: 
If zero or Space, and “Redemption Fee 
Indicator” is provided, will not override the STR 
Fee Share Quantity in the database. 
 
For all record types: 
Not allowed when “Redemption Fee Indicator” is 
populated with either ‘2’ (Money Market [[Liquidity]] 
Fee) or ‘3’ (Money Market [[Liquidity]] Fee with 
CDSC). 

---

## Page 144

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 144 
 
Field Name Location Modified requirement 
 Correction record (003) 
Correction Confirmation record 
(025) 
Post [[settlement]] Correction by 
Fund record (026) 
 
start 577, end 590, length 14 
Before change 
 
9,999,999,999.9999 
 
For all record types: 
Not allowed if Redemption Fee Indicator is not 
provided. 
For record type 003: 
Required when Redemption Fee Indicator is 
provided and STR Fee Money Amount = 0 or Space. 
For record type 025: 
If zero or Space, and Redemption Fee Indicator is 
provided, will not override the STR Fee Share 
Quantity in the database. 
 
After change 
 
9,999,999,999.9999 
 
For all record types: 
Not allowed if Redemption Fee Indicator is not 
provided. 
 
For record type 003: 
Required when Redemption Fee Indicator is 
provided and Redemption Fee Money Amount = 
0 or Space. 
 
For record type 025: 
If zero or Space, and Redemption Fee Indicator 
is provided, will not override the STR Fee Share 
Quantity in the database. 
 
For all record types: 
Not allowed when “Redemption Fee Indicator” is 
populated with either ‘2’ (Money Market [[Liquidity]] 
Fee) or ‘3’ (Money Market [[Liquidity]] Fee with 
CDSC). 

---

## Page 145

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 145 
 
Field Name Location Modified requirement 
 Exchange Order record (015) 
 
start 447, end 460, length 14 
Before change 
 
9,999,999,999.9999 
Required when Redemption Fee Indicator is 
provided and STR Fee Money Amount = 0 or Space. 
Not allowed if Redemption Fee Indicator is not 
provided or if STR Fee Money Amount > 0 
 
After change 
 
9,999,999,999.9999 
Required when Redemption Fee Indicator is 
provided and Redemption Fee Money Amount = 
0 or Space. 
Not allowed if Redemption Fee Indicator is not 
provided or if Redemption Fee Money Amount > 
0. 
 
Not allowed when “Redemption Fee Indicator” is 
populated with either ‘2’ (Money Market [[Liquidity]] 
Fee) or ‘3’ (Money Market [[Liquidity]] Fee with 
CDSC). 

---

## Page 146

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 146 
 
Field Name Location Modified requirement 
Exchange Confirmation record 
(016) 
Exchange Reconfirmation 
record (017) 
Post [[settlement]] Exchange 
Cancellation record (021) 
 
start 447, end 460, length 14 
Before change 
 
9,999,999,999.9999 
 
For all record types 
Not allowed if Redemption Fee Indicator is not 
provided. 
For record types 016 and 017: 
If zero or Space, will not override the STR Fee Share 
Quantity in the database. 
 
After change 
 
9,999,999,999.9999 
 
For all record types 
Not allowed if Redemption Fee Indicator is not 
provided. 
 
For record types 016 and 017: 
If zero or Space, will not override the STR Fee 
Share Quantity in the database. 
 
For all record types: 
Not allowed when “Redemption Fee Indicator” is 
populated with either ‘2’ (Money Market [[Liquidity]] 
Fee) or ‘3’ (Money Market [[Liquidity]] Fee with 
CDSC). 
4. Reject Codes 
The following new reject codes have been added: 
Reject Code Description 
282 Money Market [[Liquidity]] Fee/Redemption Gate Indicator invalid 
283 Transaction Received Date missing/invalid 
284 Aggregated Order Indicator missing/invalid 
 

---

## Page 147

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 147 
 
The descriptions of the following reject codes have been modified: 
Reject 
Code 
New Description Old Description 
168 Transaction Received Time missing/invalid [[participant]] Processing Time invalid 
250 Redemption Fee Rate missing/invalid STR Fee Rate invalid 
252 Redemption Fee Money Amount missing/invalid STR Fee Money Amount missing/invalid 

---

## Page 148

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 148 
 
5. Modified Description of Record Length (001, 004, & 003) 
 Description of Record Length has been modified for the record types listed in the following table.  
Field Name Record Type 
Location 
Modified Description 
 Record Length Order record (001)  
start 1 end 4, length 4  
Before change 
With no SSN/EIN Suffix: 
0290, 0383, 0476, 
0569. 
0569 is required when Redemption Fee Indicator is 
provided or [[Asset]] Type Indicator = Q 
With SSN/EIN Suffix: 
Up to 1592 
 
After change 
With no SSN/EIN Suffix: 
0290, 0383, 0476, 
0569. 
0569 i s required when Redemption Fee Indicator is 
provided, [[Asset]] Type Indicator = Q, or Money Market 
[[Liquidity]] Fee/Redemption Gate Indicator is 
provided.  
With SSN/EIN Suffix: 
Up to 1592 
 As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Post [[settlement]] Cancellation 
by Fund record (140) 
 
start 1 end 4, length 4  
Before change 
For record type 004 With no SSN/EIN Suffix: 
0290, 0383, 0476, 0569, 0662 
For record type 004 With SSN/EIN Suffix: 
Up to 1685 
For all other record types: 
0569, 0662 
0662 is required under the following conditions: 
• Redemption Fee Indicator is provided  
• [[Asset]] Type is Q (Optional for all other [[Asset]] Types 
 
After change 
 
For record type 004 With no SSN/EIN Suffix: 
0290, 0383, 0476, 0569, 0662 
For record type 004 With SSN/EIN Suffix: 
Up to 1685  
For all other record types: 
0569, 0662  
0662 is required under the following conditions: 
• Redemption Fee Indicator is provided  
• [[Asset]] Type is Q (Optional for all other [[Asset]] Types 
• Money Market [[Liquidity]] Fee/Redemption Gate 
Indicator is provided. 

---

## Page 149

Variable Length Record Layouts (Part 1) 
Summary of Changes – effective Q3 09/26/2016 149 
 
Field Name Record Type 
Location 
Modified Description 
 Correction record (003) 
Correction Confirmation 
record (025) 
Post [[settlement]] Correction by 
Fund record (026) 
 
start 1 end 4, length 4  
Before change 
 
With no SSN/EIN Suffix: 
0290, 0383, 0476, 0569, 0662, 0755, 0848, 0941, 
1034, 1127, 
1220 
(Must be 0569 or greater for all record types except 
003) 
 
0662 is required when Redemption Fee Indicator is 
provided or [[Asset]] Type Indicator = Q. 
 
After change 
 
With no SSN/EIN Suffix: 
0290, 0383, 0476, 0569, 0662, 0755, 0848, 0941, 
1034, 1127, 1220 
(Must be 0569 or greater for all record types except 
003) 
 
0662 is required when Redemption Fee Indicator is 
provided or [[Asset]] Type Indicator = Q, or Money 
Market [[Liquidity]] Fee/Redemption Gate Indicator is 
provided. 

---

## Page 150

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q1 02/29/2016 150 
 
SUMMARY OF CHANGES – EFFECTIVE Q1 02/29/2016 
Field Name Record Type & Location Before change After change 
Reminder Age  Reminders (080)  1-9998 = Reminder age (in business 
days) 
 
9999 = Pending period expired, 
original transaction deleted by 
Fund/SERV 
1-9998 = Reminder age (in 
business days) 
 
9999 = Pending period expired, 
original transaction deleted by 
Fund/SERV 
 
Effective 02/29/2016, 
Reminder 080 record with 
age 9999 will no longer be 
sent to Funds (Important 
Notice A8107).  

---

## Page 151

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q3 07/27/2015 151 
 
SUMMARY OF CHANGES – EFFECTIVE Q3 07/27/2015 
Requirements Changed for Existing Field 
Field Name Record Type & Location Modified requirement 
Social Code  Order Record (001) 
As-Of Order (004) 
Confirmation (005) 
Reconfirmation (006) 
Correction (003) 
Correction Confirmation (025) 
Post [[settlement]] Correction by 
Fund (026) 
 
Start 365, end 366, length 2 
Before change 
 
Optional 
 
After change 
 
Optional/Conditional 
 
Required when “Transaction 
Code” = 01  –  Initial Purchase 

---

## Page 152

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q2 04/27/2015 152 
 
SUMMARY OF CHANGES – EFFECTIVE Q2 04/27/2015 
Requirements Changed for Existing Fields 
Field Name Location Modified requirement 
State of Sale 
(State Code) 
Order Record (001) 
As-Of Order (004) 
Confirmation (005) 
Reconfirmation (006) 
Fund Originated Order (007) 
Fund Originated As-Of Order 
(009) 
Post [[settlement]] Cancellation by 
Fund (140) 
Correction (003) 
Correction Confirmation (025) 
Post [[settlement]] Correction by 
Fund (026) 
 
start 269, end 270, length 2 
Before change 
 
Required for new purchases 
 
After change 
 
Required for Transaction Codes 
 
01 (Initial purchase) 
02 (Subsequent purchase) 
State of Sale 
(State Code) 
Exchange Order (015) 
Exchange Confirmation (016) 
Exchange Reconfirmation (017) 
Post [[settlement]] Exchange 
Cancellation (021) 
 
start 355, end 356, length 2 
Before change 
 
Required for exchanges to new accounts 
Transaction Type: 
6 (Exchange to new account) 
C (Voluntary Cross Class Exchange to new account) 
 
After change 
 
Required for all exchanges 

---

## Page 153

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q3 07/02/2014 153 
 
SUMMARY OF CHANGES – EFFECTIVE Q3 07/02/2014 
1. Documentation Changes 
Fund/SERV Variable Record Layouts Part 3 – The Table of Contents has been modified to remove references 
to the following records: 
• Settling Trade Detail for non-USD [[settlement]] by Currency – Record 076 
• Settling Trade Detail for TPA/Investment Agent/TPP non-USD [[settlement]] by Currency – Record 078 
• Settling Trade Trailer for non-USD [[settlement]] by Currency – Record 077 
• Settling Trade Trailer for TPA/Investment Agent/TPP non-USD [[settlement]] by Currency – Record 079 

---

## Page 154

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q3 07/28/2014 154 
 
SUMMARY OF CHANGES – EFFECTIVE Q3 07/28/2014 
1. New Fields 
The following fields have been added to existing layouts: 
New Name Location Layout Section  
1. Secondary Social Security 
Number 
start 96, end 104, 
length 9 
ACATS Transfer record (018) Section 02.11.01 
2. Fund [[settlement]] Date start 89, end 96, 
length 8 
ACATS Transfer 
Acknowledgement/Rejection 
record (019) 
Section 02.12.01 
2. Reject Codes 
The following new reject code has been added for the Fund [[settlement]] Date: 
Reject Code Description 
280 Fund [[settlement]] Date is missing/invalid  
3. Modified Description of Existing Fields 
Field Name Location Changes to Description 
SSN/EIN Indicator start 167, end 167, length 1 Before change 
0 = Tax [[ID]] number  
1 = Social security number 
2 = [[investor]] TIN/EIN 
 
After change 
ACATS populates this field with one of the following 
values from the Fund Registration (FR) record: 
 
0 = Tax [[ID]] Number 
1 = Social Security Number 
2= [[investor]] EIN (Employee Identification Number) 
 
Exception: 
If ACATS does not receive an FR record, the [[default]] 
value for this field is ‘0’. 

---

## Page 155

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q3 07/28/2014 155 
 
Field Name Location Changes to Description 
SSN/EIN Number start 168, end 176, length 9 Before change 
<no description> 
 
After change 
ACATS populates this field with the SSN/EIN 
submitted on the FR by the receiver. 
Exceptions: 
For a PTF where the Fund is a receiver, if ACATS 
does not receive an FR record from the Firm, ACATS 
populates this field with the value in the ‘Receiving 
Customer’s Primary Social Security Number’ from the 
Transfer Initiation (TI) record. 
For a PTF where the Fund is a deliverer, if ACATS 
does not get a FR from the Firm, ACATS populates 
this field with the Receiving [[participant]]’s Tax [[ID]] 
number from the ACATS [[participant]] master file. 
For all other transfer types, if ACATS does not receive 
an FR record, ACATS populates this field with the 
Receiving [[participant]]’s Tax [[ID]] number from the 
ACATS [[participant]] master file. 
Customer SSN/EIN Number start 733, end 741, length 9 Before change 
<no description> 
 
After change 
ACATS populates this field with the value in the 
‘Receiving Customer’s Primary Social Security’ field 
from the TI record. This field is used for PTFs only, 
when Fund is either the deliverer or the receiver. 
The rule above is true in all circumstances, both when 
the receiver submits the FR record and when ACATS 
uses a [[default]] registration. 
Note: 
The value in the ‘Receiving Customer’s Primary Social 
Security Number’ on the TI record may be different 
from the SSN/EIN on the FR record. 

---

## Page 156

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q4 11/18/2013 156 
 
SUMMARY OF CHANGES – EFFECTIVE Q4 11/18/2013 
1. New Fields 
The following fields have been added to existing layouts: 
New Name Location Layout Section  
1. State of Sale (State Code) start 355, end 356, 
length 2 
Exchange Order record 015  Section 02.06.01 
2. State of Sale (State Code) start 355, end 356, 
length 2 
Exchange Confirmation (016), 
Exchange Reconfirmation (017), 
Post [[settlement]] Exchange 
Cancellation (021) 
Section 02.07.01 
3. Plan Account Number start 361, end 380, 
length 20 
Full Registration record 401 Section 02.10.01 
4. Plan Account Number 
Indicator 
start 381, end 381, 
length 1 
Full Registration record 401 Section 02.10.01 
5. Chapter 4 Status Code start 2988, end 2989, 
length 2 
Full Registration record 401 Section 02.10.01 
6. Global [[intermediary]] 
Identification Number 
start 2990, end 3014, 
length 25 
Full Registration record 401 Section 02.10.01 
7. Underlying Client’s Foreign 
Tax [[ID]] 
start 3015, end 3039, 
length 25 
Full Registration record 401 Section 02.10.01 
8. FATCA Override Special 
Rate 
start 3040, end 3044, 
length 5 
Full Registration record 401 Section 02.10.01 
2. Values or Comments Added to or Deleted from Existing Fields 
New values or comments have been added to the following fields: 
Field Name Location Added or Deleted Values or 
Comments 
1. Withhold Indicator  Full Registration (401) 
start 199, end 199, length 1  
Before change 
W9 indications 
0 = Certified (W-9 on file)  
1 = Failure to provide tin  
2 = Failure to certify tin  
3 = Notification of incorrect TIN from 
the Secretary of Treasury (Withhold 
due to B Notice) 
4 = Failure to certify backup 
withholding status  

---

## Page 157

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q4 11/18/2013 157 
 
Field Name Location Added or Deleted Values or 
Comments 
5 = Voluntary disclosure from payee of 
affirmative backup withholding status  
6 = Notification to commence Backup 
Withholding from Secretary of 
Treasury for underreporting [[Dividend]] 
and/or interest payments (Withhold 
due to C Notice) [[Dividend]] and/or 
interest payments  
7 = Applied for social security number  
8 = Exempt recipient  
9 = Account(s) subject to both B and 
C Notice Withholding 
W8 indications  
A = Uncertified foreign account (no 
W8 form on file-backup withholding 
necessary)  
B = Certified foreign [[Beneficial Owner]] 
account (from W8- BEN on file)  
C = Certified foreign [[intermediary]] 
account (form W8-IMY on file)  
D = Certified valid foreign account 
(form W8-ECI on file with ITIN)  
E = Certified foreign exempt account 
(form W8-EXP on file)  
F = W8 on file - no treaty rate claimed  
G = W8 Beneficiary with TIN on file 
 
After change 
W9 indications  
0 = Certified (W-9 on file)  
1 = Failure to provide tin  
2 = Failure to certify tin  
3 = Notification of incorrect TIN from 
the Secretary of Treasury (Withhold 
due to B Notice) 
4 = Failure to certify backup 
withholding status  
5 = Voluntary disclosure from payee of 
affirmative backup withholding status  
6 = Notification to commence Backup 
Withholding from Secretary of 
Treasury for underreporting [[Dividend]] 
and/or interest payments (Withhold 
due to C Notice) [[Dividend]] and/or 
interest payments  

---

## Page 158

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q4 11/18/2013 158 
 
Field Name Location Added or Deleted Values or 
Comments 
7 = Applied for social security number  
8 = Exempt recipient  
9 = Account(s) subject to both B and 
C Notice Withholding 
W8 indications  
A = Uncertified foreign account (no 
W8 form on file-backup withholding 
necessary)  
B = Certified foreign [[Beneficial Owner]] 
account (from W8- BEN on file)  
C = Certified foreign [[intermediary]] 
account (form W8-IMY on file)  
D = Certified valid foreign account 
(form W8-ECI on file with ITIN)  
E = Certified foreign exempt account 
(form W8-EXP on file)  
F = W8 on file - no treaty rate claimed  
G = W8 Beneficiary with TIN on file 
H = W-8BEN-E on file/documentary 
evidence 
I = Voluntary FATCA withholding - 
W-8BEN-E on file/documentary 
evidence 
J = W8-IMY or W-8BEN-E pending 

---

## Page 159

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q4 11/18/2013 159 
 
Field Name Location Added or Deleted Values or 
Comments 
W8 Qualified [[intermediary]] Indicator Full Registration (401) 
start 282, end 282, length 1 
Before change 
Required if Withhold Indicator = C. 
1 = QI (qualified [[intermediary]] - primary 
withholding)  
2 = QI (Qualified [[intermediary]] non-
withholding)  
3 = Non-QI (non-Qualified 
[[intermediary]] - nonwithholding, not the 
[[Beneficial Owner]])  
4 = Partnership (withholding)  
5 = Partnership (nonwithholding)  
6 = U. S. branch (nonwithholding)  
7 = Trust (withholding)  
8 = Trust (non-withholding) 
 
After change 
Required if Withhold Indicator = C. 
1 = QI (qualified [[intermediary]] - primary 
withholding)  
2 = QI (Qualified [[intermediary]] non-
withholding)  
3 = Non-QI (non-Qualified 
[[intermediary]] - nonwithholding, not the 
[[Beneficial Owner]])  
4 = Partnership (withholding)  
5 = Partnership (nonwithholding)  
6 = U. S. branch (nonwithholding)  
7 = Trust (withholding)  
8 = Trust (non-withholding)  
9 = Territory Financial Institution 

---

## Page 160

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q4 11/18/2013 160 
 
Field Name Location Added or Deleted Values or 
Comments 
Record Length  Full Registration (401) 
start 1, end 4, length 4 
Before change 
0383, 0476, 0569, 0662, 0755 
(With 0 payables/beneficiaries, Not 
allowed for Section 529 (Registration 
Type = 1)).  
0848, 0941, 1034, 1127  
(With 1 payable/beneficiary) 
1220, 1313, 1406, 1499  
(With 2 payables/beneficiaries) 
1592, 1685, 1778, 1871  
(With 3 payables/beneficiaries) 
1964, 2057, 2150, 2243  
(With 4 payables/beneficiaries) 
2336, 2429, 2522, 2615  
(With 5 payables/beneficiaries) 
2708, 2801, 2894, 2987  
(With 6 payables/beneficiaries) 
 
After change 
0383, 0476, 0569, 0662, 0755 
(With 0 payables/beneficiaries, Not 
allowed for Section 529 (Registration 
Type = 1)). 
0848, 0941, 1034, 1127  
(With 1 payable/beneficiary) 
1220, 1313, 1406, 1499  
(With 2 payables/beneficiaries) 
1592, 1685, 1778, 1871  
(With 3 payables/beneficiaries) 
1964, 2057, 2150, 2243  
(With 4 payables/beneficiaries) 
2336, 2429, 2522, 2615  
(With 5 payables/beneficiaries) 
2708, 2801, 2894, 2987  
(With 6 payables/beneficiaries) 
3080 
(record length must be 3080 if 
FATCA attributes are included) 
 

---

## Page 161

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q4 11/18/2013 161 
 
3. Reject Codes 
The following new reject codes have been added for the Plan Account Number Indicator:  
Reject Code Description 
277 Plan Account Number is missing/invalid  
278 Chapter 4 Status Code invalid 
279 FATCA Override Special Rate Invalid 

---

## Page 162

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q1 3/18/2013 162 
 
SUMMARY OF CHANGES – EFFECTIVE Q1 3/18/2013 
1. Values or Comments Added to or Deleted from Existing Fields 
New values or comments have been added to the following fields: 
Field Name Location Added or Deleted Values or Comments 
1. [[Asset]] Type Indicator Order Record (001) 
As-Of Order Record (004) 
Confirmation Record (005) 
Reconfirmation Record (006) 
Fund Originated Order Record 
(007) 
Fund Originated As-Of Order 
Record (009) 
Post [[settlement]] Cancellation 
by Fund Record (140) 
Correction Record (003) 
Correction Confirmation 
Record (025) 
Post [[settlement]] Correction by 
Fund Record (026) 
 
start 160, end 160, length 1 
Before change 
0 = Not applicable 
1 = Current year payment 
2 = Prior year payment 
3 = IRA rollover 
4 = [[Asset]] transfer 
5 = Employee - prior year 
6 = Employee - current year 
7 = Employer - prior year 
8 = Employer - current year 
9 = Non-fund prototype IRA 
A = Non-fund qualified plan 
C = Salary Reduction Contribution 
D = 529 Current Year Contribution 
E = UGMA account transferred to 
Section 529 Account 
F = 529 Underlying Fund Trades 
G = Share Class Conversion 
H = Health Savings Account 
I = Insurance Fund Transactions 
J = Non-Qualified Retirement Plan 
K = Qualified Retirement Plan 
L = Omnibus Distribution 
Reconciliation 
M = Variable Annuity 
N = Wrap Program 
O = Defined Benefit Plan 
P = 529 Previous Year Contribution 
Q = 529 Rollover Contribution 
Note: 
D, P and Q indicate Section 529 Plan. 
After change 

---

## Page 163

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q1 3/18/2013 163 
 
Field Name Location Added or Deleted Values or Comments 
0 = Not applicable 
1 = Current year payment 
2 = Prior year payment 
3 = IRA rollover 
4 = [[Asset]] transfer 
5 = Employee - prior year 
6 = Employee - current year 
7 = Employer - prior year 
8 = Employer - current year 
9 = Non-fund prototype IRA 
A = Non-fund qualified plan 
C = Salary Reduction Contribution 
D = 529 Current Year Contribution 
E = UGMA account transferred to 
Section 529 Account 
F = 529 Underlying Fund Trades 
G = Share Class Conversion 
H = Health Savings Account 
I = Insurance Fund Transactions 
J = Non-Qualified Retirement Plan 
K = Qualified Retirement Plan 
L = Omnibus [[Dividend]] Reconciliation 
M = Variable Annuity 
N = Wrap Program 
O = Defined Benefit Plan 
P = 529 Previous Year Contribution 
Q = 529 Rollover Contribution 
S = Omnibus Short-Term Capital Gain 
Reconciliation 
T = Omnibus Long-Term Capital Gain 
Reconciliation 
Note: 
D, P and Q indicate Section 529 Plan. 

---

## Page 164

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q1 3/18/2013 164 
 
Field Name Location Added or Deleted Values or Comments 
2. NAV Reason Code  Order Record (001) 
As-Of Order Record (004) 
Confirmation Record (005) 
Reconfirmation Record (006) 
Fund Originated Order 
Record (007) 
Fund Originated As-Of Order 
Record (009) 
Post [[settlement]] Cancellation 
by Fund Record (140) 
Correction Record (003) 
Correction Confirmation 
Record (025) 
Post [[settlement]] Correction 
by Fund Record (026) 
 
start 268, end 268, length 1 
Before change 
Required if Trans Type = 3.  
0 = Other  
1 = Net [[Asset]] value transfer  
2 = Repurchase  
3 = Employee  
4 = Error correction  
5 = Wrap fee account  
6 = NAV commissionable  
7 = Commissionable defined contribution plan  
8 = Non-commissionable defined contribution plan  
9 = Section 529 Account - Qualified State Tuition 
Program  
A = [[Dividend]] reinvestment trade  
B = Trust Company NAV per Agreement  
C = Refer to [[Asset]] Type Indicator  
D = Deminimis Amount Processed at NAV 
After change 
Required if Trans Type = 3.  
0 = Other  
1 = Net [[Asset]] value transfer  
2 = Repurchase  
3 = Employee  
4 = Error correction  
5 = Wrap fee account  
6 = NAV commissionable  
7 = Commissionable defined contribution plan  
8 = Non-commissionable defined contribution plan  
9 = Section 529 Account - Qualified State Tuition 
Program  
A = [[Dividend]] reinvestment trade  
B = Trust Company NAV per Agreement  
C = Refer to [[Asset]] Type Indicator  
D = Deminimis Amount Processed at NAV  
E = Self Directed Brokerage Account  

---

## Page 165

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q1 3/18/2013 165 
 
Field Name Location Added or Deleted Values or Comments 
3. NAV Reason Code Exchange Order Record 
(015) 
Exchange Confirmation 
Record (016) 
Exchange Reconfirmation 
Record (017) 
Post [[settlement]] Exchange 
Cancellation (021) 
 
start 268, end 268, length 1 
Before change 
Required if Trans Type = 3. 
0 = Other  
1 = Net [[Asset]] value transfer  
2 = Repurchase  
3 = Employee  
4 = Error correction  
5 = Wrap fee account  
6 = NAV commissionable  
7 = Commissionable defined contribution plan  
8 = Non-commissionable defined contribution plan  
9 = Section 529 Account - Qualified State Tuition 
Program  
A = [[Dividend]] reinvestment trade  
B = Trust Company NAV per Agreement  
D = Deminimis Amount Processed at NAV 
After change 
Required if Trans Type = 3.  
0 = Other  
1 = Net [[Asset]] value transfer  
2 = Repurchase  
3 = Employee  
4 = Error correction  
5 = Wrap fee account  
6 = NAV commissionable  
7 = Commissionable defined contribution plan  
8 = Non-commissionable defined contribution plan  
9 = Section 529 Account - Qualified State Tuition 
Program  
A = [[Dividend]] reinvestment trade  
B = Trust Company NAV per Agreement  
D = Deminimis Amount Processed at NAV  
E = Self Directed Brokerage Account 

---

## Page 166

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q1 3/18/2013 166 
 
Field Name Location Added or Deleted Values or Comments 
4. Transaction Type  Exchange Order Record 
(015) 
Exchange Confirmation 
Record (016) 
Exchange Reconfirmation 
Record (017) 
Post [[settlement]] Exchange 
Cancellation (021) 
 
start 61, end 61, length 1 
Before change 
6 = Exchange to new account  
7 = Exchange to existing account 
 
After change 
6 = Exchange to new account  
7 = Exchange to existing account 
C = Voluntary Cross Class Exchange to new 
account 
D = Voluntary Cross Class Exchange to existing 
account 
5. Network Control Indicator (for 
the From Account) 
Exchange Order Record (015) 
Exchange Confirmation 
Record (016) 
Exchange Reconfirmation 
Record (017) 
Post [[settlement]] Exchange 
Cancellation Record (021) 
 
start 165, end 165, length 1  
Before change 
0 = Non-networked  
1 = Matrix level 1  
2 = Matrix level 2  
3 = Matrix level 3  
4 = Matrix level 4 
 
After change 
0 = Non-networked  
3 = Matrix level 3  
4 = Matrix level 4 
6. Network Control Indicator (for 
the To Account) 
Exchange Order Record (015) 
 
start 326, end 326, length 1  
Before change 
0 = Non-networked 
1 = Matrix level 1 
Allowed only for Transaction 
Type = 7 
2 = Matrix level 2 
Allowed only for Transaction 
Type = 7 
3 = Matrix level 3 
4 = Matrix level 4 
 
After change 
0 = Non-networked  
3 = Matrix level 3  
4 = Matrix level 4 

---

## Page 167

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q1 3/18/2013 167 
 
Field Name Location Added or Deleted Values or Comments 
7. Network Control Indicator (for 
the To Account) 
Exchange Confirmation 
Record (016) 
Exchange Reconfirmation 
Record (017) 
Post [[settlement]] Exchange 
Cancellation Record (021) 
 
Record 4, start 43, end 43, 
length 1  
Before change 
0 = Non-networked 
1 = Matrix level 1 
Not allowed if Record Type = 016 or 017 
and Transaction Type = 6 
2 = Matrix level 2 
Not allowed if Record Type = 016 or 017 
and Transaction Type = 6 
3 = Matrix level 3 
4 = Matrix level 4 
After change 
0 = Non-networked  
3 = Matrix level 3  
4 = Matrix level 4 
8. Network Control Indicator  Order Record (001) 
As-Of Order Record (004) 
Confirmation Record (005) 
Reconfirmation Record (006) 
Fund Originated Order Record 
(007) 
Fund Originated As-Of Order 
Record (009) 
Post [[settlement]] Cancellation 
by Fund Record (140) 
Extended Correction Transfer 
(200) 
Extended Correction Transfer 
Acknowledgment (201) 
Order Acknowledgment for 
Money Market Purchase (101) 
Firm Delete Record (102) 
Release to [[settlement]] Record 
(109) 
Registration Acknowledgment 
Record (112) 
Delete Pending Registration 
Record (113) 
Receiving Fund Exit from 
ToRA Record (214) 
Correction Record (003) 
Correction Confirmation 
Record (025) 
Post [[settlement]] Correction by 
Fund Record (026) 
 
start 165, end 165, length 1  
Before change 
0 = Non-networked  
1 = Matrix level 1  
2 = Matrix level 2  
3 = Matrix level 3  
4 = Matrix level 4 
 
After change 
0 = Non-networked  
3 = Matrix level 3  
4 = Matrix level 4 
 

---

## Page 168

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q1 3/18/2013 168 
 
2. Requirements Changed for Existing Fields 
Requirements have been changed for the following fields: 
Field Name Location Modified requirement 
1 TPA/Investment Agent/TPP 
Number 
Order Record (001) 
Correction Record (003) 
Correction Confirmation Record 
(025) 
Post [[settlement]] Correction by 
Fund Record (026) 
 
start 89, end 92, length 4 
Before change 
 
Required if: 
Originator Type = (T or P or A or V) 
OR  
Membership Identifier = 02 or 03. 
If Originator Type = T or P, then [[Asset]] Type Indicator 
must be F through O (indicating DCC&S) 
 
After change 
 
Required if: 
Originator Type = (T or P or A or V)  
OR  
Membership Identifier = 02 or 03. 
If Originator Type = T or P, then [[Asset]] Type 
Indicator must be F through O or S or T 
(indicating DCC&S) 
2 TPA/Investment Agent/TPP 
Number 
As-Of Order Record (004) 
Confirmation Record (005) 
Reconfirmation Record (006) 
Fund Originated Order Record 
(007) 
Fund Originated As-Of Order 
Record (009) 
Post [[settlement]] Cancellation by 
Fund Record (140) 
 
start 89, end 92, length 4 
Before change 
 
Required if: 
Originator Type (T or A or V) 
OR 
Membership Identifier = 02 or 03. 
If Originator Type = T or P, then [[Asset]] Type Indicator 
must be F through O (indicating DCC&S). 
 
After change 
 
Required if: 
Originator Type (T or A or V) 
OR 
Membership Identifier = 02 or 03. 
If Originator Type = T or P, then [[Asset]] Type 
Indicator must be F through O or S or T 
(indicating DCC&S). 

---

## Page 169

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q1 3/18/2013 169 
 
Field Name Location Modified requirement 
3. Exch To Account Number Exchange Order Record (015) 
 
start 305, end 324, length 20 
Before change 
Required if Transaction Type = 7 
 
After change 
Required if Transaction Type = 7 (Exchange to 
existing account number), or D (Voluntary Cross 
Class Exchange to existing account number) 
4. Original Trade Date Extended Correction Transfer 
Record (200) 
Extended Correction Transfer 
Acknowledgment Record (201) 
 
start 72, end 79, length 8 
Before change 
Optional 
 
After change 
Required 

---

## Page 170

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q1 2013 170 
 
SUMMARY OF CHANGES – EFFECTIVE Q1 2013 
1. Modified Description of Values of Existing Field 
Description of values 3, 6, and 9 for Withholding Indicator is changed. 
Field Name Location Changes to Description 
Withhold Indicator Full Registration (401) 
ACATS Transfer (018) 
 
Start 199, end 199, length 1 
Before change 
 
W9 Indications 
0 = Certified (W-9 on file)  
1 = Failure to provide tin  
2 = Failure to certify tin  
3 = Notification of incorrect tin from the secretary of 
treasury  
4 = Failure to certify backup withholding status  
5 = Voluntary disclosure from payee of affirmative 
backup withholding status  
6 = Notification to commence backup withholding from 
secretary of treasury for underreporting [[Dividend]] 
and/or interest payments  
7 = Applied for social security number  
8 = Exempt recipient  
9 = Withhold due B/C notice  
W8 indications  
A = Uncertified foreign account (no W8 form on file-
backup withholding necessary)  
B = Certified foreign [[Beneficial Owner]] account (from 
W8- BEN on file)  
C = Certified foreign [[intermediary]] account (form W8-
IMY on file)  
D = Certified valid foreign account (form W8-ECI on 
file with ITIN)  
E = Certified foreign exempt account (form W8-EXP 
on file)  
F = W8 on file - no treaty rate claimed  
G = W8 Beneficiary with TIN on file 
 

---

## Page 171

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q1 2013 171 
 
Field Name Location Changes to Description 
After change 
W9 indications 
0 = Certified (W-9 on file)  
1 = Failure to provide tin  
2 = Failure to certify tin  
3 = Notification of incorrect TIN from the Secretary 
of Treasury (Withhold due to B Notice) 
4 = Failure to certify backup withholding status  
5 = Voluntary disclosure from payee of affirmative 
backup withholding status  
6 = Notification to commence Backup Withholding 
from Secretary of Treasury for underreporting 
[[Dividend]] and/or interest payments (Withhold due 
to C Notice) 
[[Dividend]] and/or interest payments  
7 = Applied for social security number  
8 = Exempt recipient  
9 = Account(s) subject to both B and C Notice 
Withholding 
W8 indications 
A = Uncertified foreign account (no W8 form on file-
backup withholding necessary)  
B = Certified foreign [[Beneficial Owner]] account (from 
W8- BEN on file)  
C = Certified foreign [[intermediary]] account (form W8-
IMY on file)  
D = Certified valid foreign account (form W8-ECI on 
file with ITIN)  
E = Certified foreign exempt account (form W8-EXP 
on file)  
F = W8 on file - no treaty rate claimed  
G = W8 Beneficiary with TIN on file 

---

## Page 172

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q2 4/23/2012 172 
 
SUMMARY OF CHANGES – EFFECTIVE Q2 4/23/2012 
1. Values or Comments Added to or Deleted from Existing Fields 
New values or comments have been added to the following fields: 
Field Name Location Added or Deleted Values or Comments 
1. Network Control 
Indicator 
Full Registration Record (401) 
Start 165, end 165, length 1 
Before change 
0 = Non-networked 
1 = Matrix level 1 
2 = Matrix level 2 
3 = Matrix level 3 
4 = Matrix level 4 
After change 
0 = Non-networked 
3 = Matrix level 3 
4 = Matrix level 4 
2. Network Control 
Indicator 
ACATS Transfer Record (018) 
Start 165, end 165, length 1 
Before change 
0 = Non-networked 
1 = Matrix level 1 
2 = Matrix level 2 
3 = Matrix level 3 
4 = Matrix level 4 
After change 
0 = Non-networked 
3 = Matrix level 3 
4 = Matrix level 4 
3. Network Control 
Indicator (Delivering Firm) 
ACATS Transfer Record (018) 
Start 636, end 636, length 1 
Before change 
0 = Non-networked 
1 = Matrix level 1 
2 = Matrix level 2 
3 = Matrix level 3 
4 = Matrix level 4 
After change 
0 = Non-networked 
3 = Matrix level 3 
4 = Matrix level 4 

---

## Page 173

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q2 4/23/2012 173 
 
Field Name Location Added or Deleted Values or Comments 
4. Network Control 
Indicator  
AACATS Transfer Acknowledgement/Rejection 
Record (019) 
Start 165, end 165, length 1 
Before change 
0 = Non-networked 
1 = Matrix level 1 
2 = Matrix level 2 
3 = Matrix level 3 
4 = Matrix level 4 
After change 
0 = Non-networked 
3 = Matrix level 3 
4 = Matrix level 4 
2. Requirements Changed for Existing Fields 
Requirements have been changed for the following fields: 
Field Name Location Modified requirement 
1. Network Control Indicator (for 
the To Account) 
Exchange Order Record (015) 
Start 326, end 326, length 1 
following condition has been added: 
 
1 = Matrix level 1 
Allowed only for Transaction Type = 7 
 
2 = Matrix level 2  
Allowed only for Transaction Type = 7 
2. Network Control Indicator (for 
the To Account) 
Exchange Order Confirmation 
Record (016) 
Exchange Order 
Reconfirmation Record (017)  
Start 326, end 326, length 1 
following condition has been added: 
 
1 = Matrix level 1  
Not allowed if Record Type = 016 or 017  
and Transaction Type = 6 
 
2 = Matrix level 2  
Not allowed if Record Type = 016 or 017  
and Transaction Type = 6 
3. Account Representative Name Full Registration Record (401) 
Start 222, end 236, 
 length 15 
Before change 
Required for new networked account (Network 
Control Ind = 1,2,3 or 4, and Fund Account Ind = 0 or 
1) 
 
After change 
Required for new networked account (Network 
Control Ind = 3 or 4, and Fund Account Ind = 0, 1 or 
4) 

---

## Page 174

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q2 4/23/2012 174 
 
Field Name Location Modified requirement 
4. Account Representative 
Number 
Full Registration Record (401) 
Start 237, end 245, length 9 
Before change 
Required for new networked account (Network 
Control Ind = 1,2,3 or 4, and Fund Account Ind = 0 or 
1) 
 
After change 
Required for new networked account (Network 
Control Ind = 3 or 4, and Fund Account Ind = 0, 1 or 
4) 
5. Branch Identification Number Full Registration Record (401) 
Start 246, end 254, 
 length 9 
Before change 
Required for new networked account (Network 
Control Ind = 1,2,3 or 4, and Fund Account Ind = 0 or 
1) 
 
After change 
Required for new networked account (Network 
Control Ind = 3 or 4, and Fund Account Ind = 0, 1 or 
4) 
 
Record layouts affected: 
Layout Location Field applied 
Order (001)  Section 02.01.01 1, 2, 3 
As-Of Order (004)… Section 02.02.01 1, 2, 3 
Full Registration (401)  Section 02.03.01 4 
Correction (003)… Section 02.29.01 1, 2 and 3 
3. Reject Codes 
The following reject codes have been renamed to match the newly renamed IRA/529 [[liquidation]] Indicator  
Reject Code Description 
106 IRA/529 [[liquidation]] Indicator missing/invalid  
 
The following new reject codes have been added for the Section 529 and ToRA fiel ds: 
Reject Code Description 
261 Cost Basis Money Amount missing/invalid  
262 Earnings To Date Money Amount missing/invalid 

---

## Page 175

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q2 4/23/2012 175 
 
Reject Code Description 
263 Negative Earnings To Date Indicator missing/invalid 
264 ToRA Fund Reject Code missing/invalid  
265 ToRA Delivering Fund Plan Type missing/invalid 
266 ToRA Uncollected [[shares]] missing/invalid 
 
The following new reject codes have been added. They can be used by the fund when rejecting Section 529 
transactions: 
Reject Code Description 
750 529 – Over Investment  
751 (Exchange) Investment [[Option]] Changes Exceed Two Times per Year 
752 529 [[Asset]] Type Indicator Referenced for Non-529 Plan Account 

---

## Page 176

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q4 12/5/2011 176 
 
SUMMARY OF CHANGES – EFFECTIVE Q4 12/5/2011 
1. New Fields 
The following fields have been added to existing layouts: 
New Name Location Layout Section  
1. Original Deliverer Customer 
Account Number 
start 177, end 196, 
length 20 
ACATS record 018  Section 02.11.01 

---

## Page 177

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q4 10/17/2011 177 
 
SUMMARY OF CHANGES – EFFECTIVE Q4 10/17/2011 
1. New Fields 
The following fields have been added to existing layouts: 
New Name Location Layout Section  
1. Underlying Firm Symbol 
(UFS) 
start 183, end 186, 
length 4 
Full Registration (401)  Section 02.10.01 
2. Values or Comments Added to or Deleted from Existing Fields 
New values or comments have been added to the following fields: 
Field Name Location Added or Deleted Values or Comments 
1. Delivering Fund Plan Type Fund Reject Record (100) 
start 129, end 129, length 1 
Before change 
Required if the Fund Reject Code = “704”  
0 = IRA  
1 = IRA Rollover  
2 = SEP IRA  
3 = 403B  
4 = Roth IRA  
5 = Simple IRA  
6 = Education IRA  
7 = SARSEP  
8 = Roth Conversion IRA  
9 = Traditional to Roth Conversion IRA  
A = Inherited Traditional IRA  
B = Inherited Roth IRA  
C = Inherited Roth Conversion IRA 
After change 
Required if the Fund Reject Code = “704”  
0 = IRA  
1 = IRA Rollover  
2 = SEP IRA  
3 = 403B  
4 = Roth IRA  
5 = Simple IRA  
6 = Education IRA  
7 = SARSEP  

---

## Page 178

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q4 10/17/2011 178 
 
Field Name Location Added or Deleted Values or Comments 
8 = Roth Conversion IRA  
9 = Traditional to Roth Conversion IRA  
A = Inherited Traditional IRA  
B = Inherited Roth IRA  
C = Inherited Roth Conversion IRA 
D = Account Type Is Not ToRA Eligible 
3. Requirements Changed for Existing Fields 
Requirements have been changed for the following fields: 
Field Name Location Modified requirement 
1. Beneficiary/Successor Owner 
Relationship Indicator (pertains 
to section related to 529 
Registration) 
start 789, end 789, length 1 a) following condition has been removed: 
Required if Beneficiary/Successor Owner Address 
[[Option]] of ‘C’ is provided 
 
b) requirement has been changed from 
Optional/Conditional to Optional 

---

## Page 179

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q2 2011 179 
 
SUMMARY OF CHANGES – EFFECTIVE Q2 2011 
1. New Fields 
The following fields have been added to existing layouts: 
New Name Location Layout Section  
1. Originating Receiver 
Customer Account Number at 
Firm  
start 547, end 566, length 20 ACATS Transfer (018) Section 02.11.01 
2. Originating Receiver Firm 
Number 
start 745, end 748, length 4 ACATS Transfer (018)  Section 02.11.01 
3. Originating Delivering Firm 
Number 
start 749, end 752, length 4 ACATS Transfer (018) Section 02.11.01 
2. Values or Comments Added to or Deleted from Existing Fields 
New values or comments have been added to the following fields: 
Field Name Location Added or Deleted Values or Comments 
1. Cost Basis [[Option]] Full Registration Record (401) Before change 
1 = Unknown  
2 = First in  
3 = Last in  
4 = Highest  
5 = Lowest  
6 = Owner 
 
After change 
0 = Unknown 
1 = FIFO (First In First Out) 
2 = LIFO (Last In First Out) 
3 = High Cost 
4 = Low Cost 
5 = Average Cost 
6 = Select Lot 

---

## Page 180

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q2 2011 180 
 
Field Name Location Added or Deleted Values or Comments 
2. Cost Basis [[Option]] ACATS Transfer (018) Before change 
1 = Unknown  
2 = First in  
3 = Last in  
4 = Highest  
5 = Lowest  
6 = Owner 
 
After change 
0 = Unknown 
1 = FIFO (First In First Out) 
2 = LIFO (Last In First Out) 
3 = High Cost 
4 = Low Cost 
5 = Average Cost 
6 = Select Lot 

---

## Page 181

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q1 2011 181 
 
SUMMARY OF CHANGES – EFFECTIVE Q1 2011 
1. Record Changed from Optional to Optional Conditional 
Record Location Current Requirement  Future Requirement 
Order Acknowledgment 
for Money Market 
Purchase (101)… 
Section 02.04.01 Record 2 is required for Record 
Types 101, 109, 112 and 113. 
Record 2 will now be required 
under the following conditions: 
• Record 101, 109, 112 and 
113 
• Record 102 if Originator Type 
= V (TPP).  
2. Renamed Fields 
The following fields have been renamed: 
New Name Old Name Location 
1. TPA/Investment Agent/TPP 
Number  
TPA/Investment Agent Number  record 1, start 85, end 88, length 4 
2. Firm or TPA/Investment 
Agent/TPP Number 
Firm or TPA/Investment Agent 
Number 
record 1, start 85, end 88, length 4 
3. Firm/TPA/SP/Investment 
Agent/TPP Number  
Firm/TPA/SP/Investment Agent 
Number  
record 1, start 8, end 11, length 4 
 
Record layouts affected: 
Layout Location Field applied 
Order (001)  Section 02.01.01  1 
As-Of Order (004)… Section 02.02.01 1 
Extended Correction Transfer 
(200)… 
Section 02.03.01 1 
Order Acknowledgment for Money 
Marker Purchase (101)…  
Section 02.04.01 1 
Fund Reject (100) Section 02.05.01 1 
Exchange Order (015)  Section 02.06.01 1 
Exchange Confirmation (016)... Section 02.07.01 1 
Cash Adjustment (011) Section 02.08.01 1 
Reminders (080)… Section 02.17.01 1 

---

## Page 182

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q1 2011 182 
 
Layout Location Field applied 
Firm/TPA/Investment Agent/TPP 
Input Trailer (999) 
Section 02.18.01 3 
Settling Trades Detail (070)… Section 02.23.01 2 
Multiple Reject Codes (120)… Section 02.25.01 1 
Firm Exit (139)  Section 02.28.01 1 
Correction (003)... Section 02.29.01 1 
Full Registration (401) Section 02.10.01 1 
Retiring [[participant]] (090) Section 02.16.01 1 
3. Values or Comments Added to or Deleted From Existing Fields 
New values or comments have been added to the following fields: 
Field Name Location Added or Deleted Values or Comments 
1. Originator Type start 9, end 9, length 1 V = TPP (Third Party Provider) 
2. Record Type start 19, end 21, length 3 Post-[[settlement]] Cancellation by Fund (140) or Post-
[[settlement]] Correction by Fund (026) is not permitted if 
the Security Issue Type field value is 63 and 
[[settlement]] Override Reason Code field value is 
space. 
3. Record Type  start 19, end 21, length 3 Exchange Order is not permitted if the Security Issue 
Type field value is 63 and [[settlement]] Override Reason 
Code field value is space. 
4. Record Type start 19, end 21, length 3 Exchange Confirmation, Exchange Reconfirmation 
and Post [[settlement]] Exchange Confirmation are not 
permitted if the Security Issue Type field value is 63 
and [[settlement]] Override Reason Code field value is 
space. 
5. Correction Indicator start 60, end 60, length 1 P not permitted if the Security Issue Type field value is 
63 and [[settlement]] Override Reason Code field value 
is space. 
6. Transaction Code  start 62, end 63, length 2 07 and 08 not permitted if the Security Issue Type field 
value is 63 and [[settlement]] Override Reason Code 
field value is space. 
7. Recipient Type start 88, end 88, length 1 V = TPP (Third Party Provider) 
8. Fund Account Indicator start 139, end 139, length 1 0 = New account – U.S.  
1 = New account – non-U.S.  
2 = Existing account – U.S.  

---

## Page 183

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q1 2011 183 
 
Field Name Location Added or Deleted Values or Comments 
3 = Existing account – non-U.S.  
9.Membership Identifier start 174, end 175, length 2 03 = Third Party Provider 
10. Branch Identification Number start 225, end 233, length 9  Optional under the following conditions: 
• Membership Identifier = 01 or 02 and Agent for 
Firm Number is not provided. 
• Originator Type = V(TPP) 
11. Original Correction Indicator start 475, end 475, length 1 P not permitted if the Security Issue Type field value is 
63 and [[settlement]] Override Reason Code field value 
is space. 
12. [[settlement]] Override Reason 
Code 
start 83, end 84, length 2 Must be space for settling EUR and GBP transactions 
(Security Issue Type 63 only). 
13. Anticipated [[settlement]] Date start 217, end 224, length 8 mmddccyy  
For Security Type 63: 
1. Required if [[settlement]] Override Reason Code is 
space 
14.Currency Indicator start 157, end 159, length 3 EUR or GBP 
15.Currency Indicator Debit  start 122, end 124, length 3 EUR or GBP 
16.Currency Indicator - Credit Record 2, start 66, end 68, 
length 3 
EUR or GBP 
17.Correction/Exchange 
Indicator 
start 60, end 60, length 1 P, Y and Z not permitted if the Security Issue Type 
field value is 63 and [[settlement]] Override Reason 
Code field value is space 
 
Record layouts affected: 
Layout Location Field applied 
Order (001) Section 02.01.01 1, 8, 9, 10, 11, 12 and 13 
As-Of Order (004)... Section 02.02.01 1, 2, 5, 6, 8, 9, 10, 11, 12 and 13  
Extended Correction Transfer 
(200)… 
Section 02.03.01 1 and 9 
Order Acknowledgment for Money 
Market Purchase (101)… 
Section 02.03.01 1 
Exchange Order (015) Section 02.06.01 1, 3 and 11 
Exchange Confirmation (016)… Section 02.07.01 4 and 9 
Cash Adjustment (011) Section 02.08.01 1 and 9 

---

## Page 184

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q1 2011 184 
 
Layout Location Field applied 
Full Registration (401)  Section 02.10.01 1 and 8 
Firm/TPA/Investment Agent/TPP 
Input Trailer (999) 
Section 02.18.01 1 
Settling Trade Detail (070)… Section 02.23.01 5,7,14, and 17 
Firm Exit (139) Section 02.28.01 1 
Correction (003)… Section 02.29.01 1, 2, 5, 6, 8, 9, 10, 11, 12 and 13 
Exchange Reconfirmation (017) Section 02.07.01 4 and 9 
Post-[[settlement]] Exchange 
Cancellation (021) 
Section 02.07.01 4 and 9 
Settling Trade Trailer (071)… Section 02.24.01 15 and 16 
4. Requirements Changed for Existing Fields 
Requirements have been changed for the following fields: 
Field Name Location Modified requirement 
1. TPA/Investment Agent/TPP 
Number 
start 89, end 92, length 4 Required if: 
Originator Type = (T or A or V) 
 
OR 
Membership Identifier = 02 or 03 
2. TPA/Investment Agent/TPP 
Number 
start 89, end 92, length 4 Required if: 
Originator Type = T or A or V 
3. TPA/Investment Agent/TPP 
Number 
start 89, end 92, length 4 Required if Originator Type = T or P or A or V 
4. TPA/Investment Agent/TPP 
Number 
start 89, end 92, length 4 Required if Originator Type = T or P or A or V 
OR 
Membership Identifier = 02 or 03 
5. TPA/Investment Agent/TPP 
Number 
start 89, end 92, length 4 Required if Membership Identifier = 02 or 03 
6. Firm or TPA/Investment 
Agent/TPP Number 
start 89, end 92, length 4 Firm Number when Recipient Type = T or V 
 
Otherwise, TPA/Investment Agent/TPP Number  
7. Agent for Firm start 161, end 164, length 4 Required if Originator Type = V 
8. Anticipated [[settlement]] Date start 217, end 224, length 8 mmddccyy  

---

## Page 185

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q1 2011 185 
 
Field Name Location Modified requirement 
For Security Issue Type = 63, Required if 
[[settlement]] Override Reason Code is space  
 
Record layouts affected: 
Layout Location Field applied 
Order (001)  Section 02.01.01  4,7 and 8 
As-Of Order (004)… Section 02.02.01 1,7 and 8 
Cash Adjustment (011) Section 02.08.01 1 
Full Registration (401) Section 02.10.01 3 and 7  
Settling Trades Detail (070)… Section 02.23.01 6 
Firm Exit (139) Section 02.28.01 3 
Correction (003)... Section 02.29.01 4,7 and 8 
Exchange Order (015) Section 02.06.01 4 and 7 
Exchange Confirmation (016) Section 02.07.01 5 
Extended Correction Transfer 
(200)… 
Section 02.03.01 1 and 7 
Order Acknowledgment for 
Money Market Purchases 
(101)… 
Section 02.03.01 2 and 7 
5. Reject Codes  
Fund/SERV 
The description of the following reject codes have been modified as part of the Third Party Provider 
Enhancements: 
Reject 
Code 
New Description Old Description 
188 TPA/Investment Agent/TPP missing/invalid TPA/Investment Agent missing/invalid 
189 TPA/Investment Agent/TPP not authorized for 
firm 
TPA/Investment Agent not authorized for firm 
 
The following new reject codes have been added for the Third-Party Provider and the Multi-Currency 
Enhancements: 

---

## Page 186

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q1 2011 186 
 
Reject Code Description 
271 Agent for Firm missing/invalid  
272 EUR/GBP Settling Trade Date is less than the current Processing Date 
273 Non-USD [[settlement]] Submitting [[participant]] Number missing/invalid 
274 Non-USD [[settlement]] Contra [[participant]] Number missing/invalid 
275 Record Type not allowed for EUR and GBP settling transaction 
276 Settling Firm missing/invalid  

---

## Page 187

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Nov 2010 187 
 
SUMMARY OF CHANGES – EFFECTIVE NOV 2010 
1. New Fields 
The following fields have been added to existing layouts: 
New Name Location Layout Section  
1. Age Based Indicator start 179, end 179, length 1 Full Registration (401)  Section 02.10.01 
2. Age Based Roll Exempt Indicator start 180, end 181 length 1 Full Registration (401)  Section 02.10.01 
3. Customer/Owner U.S. Resident 
Alien Indicator 
start 181. end 181 length 1 Full Registration (401)  Section 02.10.01 
4. Successor Owner Indicator start 182, end 182, length 1  Full Registration (401)  Section 02.10.01 
2. Record Changed from Optional to Optional Conditional 
Record Location Current Requirement  Future Requirement 
Order Acknowledgment 
for Money Market 
Purchase (101)… 
Section 02.04.01 (Record Length must be 0197 for 
record types 101, 109, 112, and 
113) 
(Must be 0197 for record types 
101, 109, 112, and 113) 
Record Length for 102 must be 
0197 if Originator Type = V 
3. Renamed Fields 
The following fields have been renamed: 
New Name Old Name Location 
1. Customer/Owner U.S. 
Citizenship Indicator 
(Effective Q1, 2011) 
Customer U.S. Citizenship 
Indicator 
start 177, end 177, length 1 
2. Beneficiary/Successor Owner 
Date of Birth 
Beneficiary Date of Birth start 756, end 763, length 8 
3. Beneficiary/Successor Owner 
Zip Code 
Beneficiary Zip Code start 776, end 786, length 11 
4. Beneficiary/Successor Owner 
Name End Line Indicator 
Beneficiary Name End Line 
Indicator 
start 787, end 787, length 1 
5. Beneficiary/Successor Owner 
Address [[Option]] 
Beneficiary Address [[Option]] start 788, end 788, length 1 
6. Beneficiary/Successor Owner 
Relationship Indicator  
Beneficiary Relationship Indicator start 789, end 789, length 1 

---

## Page 188

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Nov 2010 188 
 
New Name Old Name Location 
7. Beneficiary/Successor Owner 
SSN/EIN Number 
Beneficiary SSN/EIN Number start 792, end 800, length 9 
8. Beneficiary/Successor Owner 
SSN/EIN Indicator 
Beneficiary SSN/EIN Indicator start 801, end 801, length 1 
9. Beneficiary/Successor Owner 
U.S. Citizenship Indicator  
Beneficiary U.S. Citizenship 
Indicator 
start 817, end 817, length 1 
10. Payable/Beneficiary/ 
Successor Owner 1 
Name/Address Line 1  
Payable/Beneficiary 1 
Name/Address Line 1 
start 849, end 883, length 35 
11. Payable/Beneficiary/ 
Successor Owner 1 
Name/Address Line 2  
Payable/Beneficiary 1 
Name/Address Line 2 
start 884, end 918, length 35 
12. Payable/Beneficiary/ 
Successor Owner 1 
Name/Address Line 3  
Payable/Beneficiary 1 
Name/Address Line 3 
start 942, end 976, length 35 
13. Payable/Beneficiary/ 
Successor Owner 1 
Name/Address Line 4  
Payable/Beneficiary 1 
Name/Address Line 4 
start 977, end 1011, length 35 
14. Payable/Beneficiary/ 
Successor Owner 1 
Name/Address Line 5 
Payable/Beneficiary 1 
Name/Address Line 5 
start 1035, end 1069, length 35 
 
Record layouts affected: 
Layout Location Field applied 
Full Registration (401) Section 02.10.01 1 through 14 
4. Requirements Changed for Existing Fields 
Requirements have been changed for the following fields: 
Field Name Location Modified requirement 
1. Beneficiary/Successor Owner 
Zip Code 
start 776, end 786, length 11 Changed from Optional Conditional to Optional 
2. Beneficiary/Successor Owner 
Name End Line Indicator  
start 787, end 787, length 1 Required if Beneficiary/Successor Owner 
Name/Address is provided. 
3. Beneficiary/Successor Owner 
Address [[Option]] 
start 788, end 788, length 1 “G = Successor Trustee” was removed.  

---

## Page 189

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Nov 2010 189 
 
Field Name Location Modified requirement 
4. Beneficiary/Successor Owner 
Relationship Indicator  
start 789, end 789, length 1 Required if Beneficiary/Successor Owner Address 
[[Option]] of “C” is provided. 
 
“2 = Other” was changed to “2=Non-Relative”  
5. Beneficiary/Successor Owner 
SSN/EIN Number 
start 792, end 800, length 9 Required if Beneficiary/Successor Owner Address 
[[Option]] of “C” or “D” is provided. 
6. Beneficiary/Successor Owner 
SSN/EIN Indicator 
start 792, end 800, length 9 Required if Beneficiary/Successor Owner SSN/EIN 
Number is provided. 
7. Beneficiary/Successor Owner 
U.S. Citizenship Indicator  
start 801, end 801, length 1 Required if Beneficiary/Successor Owner Address 
[[Option]] is “C” or “D”  
8. Payable/Beneficiary/ 
Successor Owner 1 
Name/Address Line 3 
start 942, end 976, length 35 Changed from Optional Conditional to Optional 
9. Payable/Beneficiary/ 
Successor Owner 1 City  
start 1070, end 1102, length 
33 
Changed from Required to Required Conditional 
 
Optional if Successor Owner Indicator = 1 and 
Beneficiary/Successor Owner Address [[Option]] = “D”. 
Otherwise, this field is required. 
10. Payable/Beneficiary/ 
Successor Owner 1 State 
start 1103, end 1104, length 2 Changed from Required to Required Conditional 
 
Optional if Successor Owner Indicator = 1 and 
Beneficiary/Successor Owner Address [[Option]] = “D”. 
Otherwise, this field is required. 
 
Record layouts affected: 
Layout Location Field applied 
Full Registration (401) Section 02.10.01 1 through 10 
5. Reject Codes 
Fund/SERV 
The following reject codes have been changed as part of the Section 529, the Third- Party Provider and the 
Multi-Currency Enhancements: 
The description of the following reject code has been changed as part of the Third-Party Provider and Section 
529 Enhancements: 

---

## Page 190

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Nov 2010 190 
 
Reject 
Code 
New Description Old Description 
144 Payable/Beneficiary/Successor Owner Zip Code 
missing 
Payable Zip Code missing 
145 Payable/Beneficiary/Successor Owner Name End 
Line Indicator missing/invalid 
Payable Name End Line Indicator missing/invalid 
146 Payable/Beneficiary/Successor Owner Address 
[[Option]] missing/invalid 
Payable Address [[Option]] missing/invalid 
147 Payable/Beneficiary/Successor Owner 
Name/Address Line 1 missing 
Payable Name/Address Line 1 missing 
203 Beneficiary/Successor Owner Date of Birth 
missing/invalid 
Beneficiary Date of Birth missing/invalid 
205 Beneficiary/Successor Owner Relationship 
Indicator missing/invalid 
Beneficiary Relationship Indicator missing/invalid 
236 Customer/Owner U.S. Citizenship Indicator 
missing/invalid  
Customer U.S. Citizenship Indicator missing/invalid  
240 Beneficiary/Successor Owner U.S. Citizenship 
Indicator missing/invalid 
Beneficiary U.S. Citizenship Indicator missing/invalid 
242 Beneficiary/Successor Owner City missing Beneficiary City missing 
243 Beneficiary/Successor Owner State missing Beneficiary State missing 
244 Invalid number of 529 Beneficiaries/Successor 
Owners 
Invalid number of 529 Beneficiaries  
751 Exchange exceeds IRS Strategy change limit (Exchange) Investment [[Option]] Changes Exceed Two 
Times per Year 
 
The following new reject codes have been added for the Section 529, the Third-Party Provider and the Multi-
Currency Enhancements: 
Reject Code Description 
267 Section 529 Age Based missing/invalid 
268 Section 529 Age Based Roll Exempt missing/invalid 
269 Section 529 Customer/Owner U.S. Resident Alien Indicator missing/invalid  
270 Section 529 Successor Owner Indicator missing/invalid 

---

## Page 191

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q4 2009 191 
 
SUMMARY OF CHANGES – EFFECTIVE Q4 2009 
1. New Fields 
The following fields have been added to existing layouts: 
New Name Location Layout Section  
1. Cost Basis Money Amount start 514, end 529 length 16 Order (001)  Section 02.01.01 
 start 607, end 622, length 
16 
As-Of Order (004)… Section 02.02.01 
  Correction (015) Section 02.29.01 
2. Earnings to Date Money Amount start 530, end 545 length 16 Order (001)  Section 02.01.01 
 start 623, end 638 length 16 As-Of Order (004)… Section 02.02.01 
  Correction (015) Section 02.29.01 
3. Negative Earnings to Date 
Indicator 
start 546, end 546 length 1 Order (001)  Section 02.01.01 
 start 639, end 639 length 1 As-Of Order (004)… Section 02.02.01 
  Correction (015) Section 02.29.01 
4. Fund Reject Code  start 174, end 176 length 3 Receiving Fund Exit from 
ToRA (214)…  
Section 02.04.01  
5. Delivering Fund Plan Type start 129. end 129 length 1 Fund Reject (100)  Section 02.05.01 
6. Uncollected [[shares]] Amount  start 164, end 177, length 
14 
ToRA Acknowledgment 
(211)  
Section 02.14.01 
2. Renamed Fields 
The following fields have been renamed: 
New Name Old Name Location 
1. IRA/529 [[liquidation]] Indicator IRA [[liquidation]] Indicator start 354, end 354, length 1 
2. Original IRA/529 [[liquidation]] 
Indicator 
Original IRA [[liquidation]] Indicator start 1005, end 1005, length 1 
 

---

## Page 192

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q4 2009 192 
 
Record layouts affected: 
Layout Location Field applied 
Order (001)  Section 02.01.01 1 
As-Of Order (004)… Section 02.02.01 1 
Correction (003)… Section 02.29.01 1 and 2 
3. Values or Comments Added to Existing Fields 
New values have been added to from the following fields: 
Field Name Location Added or Deleted Values or Comments 
1. Transaction Type  start 61, end 61, length 1 0 = Single purchase 
1 = Letter of intent 
2 = Rights of accumulation 
3 = Net [[Asset]] value 
4 = Group purchase 
5 = CDSC [[liquidation]] 
8 = 529 [[participant]] Distribution  
9 = 529 Beneficiary Distribution 
A = 529 School Distribution 
B = 529 Rollover Distribution 
 
8 thru B only allowed if Transaction Code = “03” or 
“04” 
(Effective Q4, 2009) 

---

## Page 193

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q4 2009 193 
 
Field Name Location Added or Deleted Values or Comments 
2. [[Asset]] Type Indicator start 160, end 160, length 1 0 = Not applicable 
1 = Current year payment 
2 = Prior year payment 
3 = IRA rollover 
4 = [[Asset]] transfer 
5 = Employee - prior year 
6 = Employee - current year 
7 = Employer - prior year 
8 = Employer - current year 
9 = Non-fund prototype IRA 
A = Non-fund qualified plan 
C = Salary Reduction Contribution  
D = 529 Current Year Contribution  
E = UGMA account transferred to Section 529 Account  
F = 529 Underlying Fund Trades 
G = Share Class Conversion 
H = Health Savings Account 
I = Insurance Fund Transactions 
J = Non-Qualified Retirement Plan 
K = Qualified Retirement Plan 
L = Omnibus Distribution Reconciliation 
M = Variable Annuity 
N = Wrap Program 
O = Defined Benefit Plan 
P = 529 Previous Year Contribution 
Q = 529 Rollover Contribution  
 
Note: 
D, P and Q relate to Section 529 
(Effective Q4, 2009). 

---

## Page 194

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q4 2009 194 
 
Field Name Location Added or Deleted Values or Comments 
3. IRA/529 [[liquidation]] Indicator start 354, end 354, length 1 0 = Not applicable 
1 = Distribution – premature 
2 = Distribution – disability 
3 = Distribution – death 
4 = Distribution – normal 
5 = Hardship withdrawal 
6 = Loan  
7 = Rollover 
8 = Adjust prior year excess 
9 = Adjust current year excess 
A = Qualified  
B = Non-Qualified  
 
A and B are required when Transaction Type = 8, 9, A 
or B 
(Effective Q4, 2009) 
4. Beneficiary Address [[Option]]  start 788, end 788, length 1  A = Primary IRA Beneficiary  
B = Secondary IRA Beneficiary 
C = 529 Beneficiary 
D = 529 Successor Owner 
G = Successor Trustee 
  
(Effective Q4, 2009) 

---

## Page 195

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q3 2009 195 
 
SUMMARY OF CHANGES – EFFECTIVE Q3 2009 
1. New Fields 
The following fields have been added to existing layouts: 
New Name Location 
1. As-Of Reason Code  start 269 end 270 length 2 
2. As-Of Reason Code start 269, end 270 length 2 
3. As-Of Reason Code start 175, end 176 length 2 
 
Record layouts affected: 
Layout Location Field applied 
Exchange Order (015)  Section 02.06.01 1 
Exchange Confirmation (016)... Section 02.07.01 2 
Firm Exit (139)  Section 02.28.01 3 
2. Record Lengths Changed 
Layout Location Current Requirement  Future Requirement 
Firm Exit (139)  Section 02.28.01 The acceptable lengths are 104, 
197 and 290.  
The acceptable lengths will be 
197 and 290. 
3. Renamed Fields 
The following fields have been renamed: 
New Name Old Name Location 
1. As-Of Indicator Extended Correction Indicator start 274, end 274, length 1 
2. As-Of Reason Code  Extended Correction As-Of 
Reason Code 
start 275, end 276, length 2 
3. Correction Type Indicator Extended Correction Indicator start 274, end 274, length 1 
4. Correction Reason Code Extended Correction Reason 
Code 
start 275, end 276, length 2 
5. Original Correction Type 
Indicator 
Original Extended Correction 
Indicator 
start 921, end 921, length 1 

---

## Page 196

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q3 2009 196 
 
New Name Old Name Location 
6. Original Correction Reason 
Code 
Original Extended Correction As-
Of Reason Code 
start 922, end 923, length 2 
 
Record layouts affected: 
Layout Location Field applied 
As-Of Order (004)… Section 02.02.01 1 and 2 
Correction (003)… Section 02.29.01 3, 4, 5 and 6 
4. Values or Comments Added to or Deleted from Existing Fields 
New values have been added to or deleted from the following fields: 
Field Name Location Added or Deleted Values or Comments 
1. As-Of Reason Code  start 275, end 276, length 2 01 = Incorrect Firm/Fund Account Number  
02 = Incorrect Share Quantity/Dollar Quantity  
05 = Incorrect Sales Charge Breakpoint  
09 = Delay in Firm Trade Transmission 
10 = With Fund’s Permission 
11 = Resubmitted Fund/SERV Reject 
12 = DCC&S (see [[Asset]] Type Indicator) 
13 = Distribution Reversal 
14 = Prospectus Violation 
Note: 
The values ‘00’, ‘06’ and ‘08’ have been removed. 
2. Extended Correction Reason 
Code  
start 62, end 63, length 2 01 = Incorrect Firm/Fund Account Number  
02 = Incorrect Share Quantity/Dollar Quantity  
05 = Incorrect Sales Charge Breakpoint  
09 = Delay in Firm Trade Transmission 
10 = With Fund’s Permission 
11 = Resubmitted Fund/SERV Reject 
12 = DCC&S (see [[Asset]] Type Indicator) 
13 = Distribution Reversal 
14 = Prospectus Violation 
Note: 
The values ‘06’ and ‘08’ have been removed. 

---

## Page 197

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q3 2009 197 
 
Field Name Location Added or Deleted Values or Comments 
3. Correction Reason Code  start 275, end 276, length 2 01 = Incorrect Firm/Fund Account Number  
02 = Incorrect Share Quantity/Dollar Quantity  
05 = Incorrect Sales Charge Breakpoint  
09 = Delay in Firm Trade Transmission 
10 = With Fund’s Permission 
11 = Resubmitted Fund/SERV Reject 
12 = DCC&S (see [[Asset]] Type Indicator) 
13 = Distribution Reversal 
14 = Prospectus Violation 
Note: 
The values ‘00’, ‘06’ and ‘08’ have been removed. 
4. Original Correction Reason 
Code 
start 922, end 923, length 2 01 = Incorrect Firm/Fund Account Number  
02 = Incorrect Share Quantity/Dollar Quantity  
05 = Incorrect Sales Charge Breakpoint  
09 = Delay in Firm Trade Transmission 
10 = With Fund’s Permission 
11 = Resubmitted Fund/SERV Reject 
12 = DCC&S (see [[Asset]] Type Indicator) 
13 = Distribution Reversal 
14 = Prospectus Violation 
Note: 
The values ‘00’, ‘06’ and ‘08’ have been removed. 
 
Record layouts affected: 
Layout Location Field applied 
As-Of Order (004)… Section 02.02.01 1 
Extended Correction Transfer 
(200) … 
Section 02.03.01 2 
Correction (003)… Section 02.29.01 3 and 4 

---

## Page 198

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Q3 2009 198 
 
5. Reject Codes 
The following new reject codes have been added. They can be used by the fund when rejecting ToRA records.  
Reject Code Description 
701 SSN does not match 
702 Account number mismatch 
703 Account specified not invested in this Security Issue [[ID]] 
704 Plan Type mismatch 
705 Name mismatch 
706 [[shares]] held in Escrow 
707 Uncollected [[shares]] 
708 Amount Requested not available 
709 Stop Code on Account  
710 Minimum purchase amount not met at the receiving fund 
711 Maximum purchase amount exceeded at the receiving fund 

---

## Page 199

Variable Length Record Layouts (Part 1) 
Summary of changes – effective Dec 2008 199 
 
SUMMARY OF CHANGES – EFFECTIVE DEC 2008 
1. New Fields 
The following fields have been added to existing layouts: 
New Name Location 
1. Customer SSN/EIN Number start 773, end 741, length 9 
2. ACATS Account Type start 742, end 743, length 2 
3. Gift/Donation Indicator start 744, end 744, length 1 
 
Record layouts affected: 
Layout Location Field applied 
ACATS Transfer (018) Section 02.11.01  1,2,3 
2. New Values to Existing Fields 
Note: 
This change is already in effect 
New values have been added to the following fields: 
Field Name Location New Values 
1. SSN/EIN Indicator start 167, end 167, length 1 2 = [[investor]] TIN/EIN 
 
Record layouts affected:  
Layout Location Field applied 
ACATS Transfer (018) Section 02.11.01  1 
 

---

## Page 200

© 2023 [[DTCC]]. All rights reserved. [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: September 7, 2023 
Publication Code: MFS316 
Service: Fund/SERV® 
Title: Variable Length Record Layouts (Part 1) 
 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 