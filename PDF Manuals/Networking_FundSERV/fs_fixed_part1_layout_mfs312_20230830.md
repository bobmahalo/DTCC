---
title: "Fund/SERV Fixed Length Record Layouts (Part 1)"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_fixed_part1_layout_mfs312_20230830.pdf"
pages: 192
size: "1380.2 KB"
category: "Networking_FundSERV"
ingested_on: "2026-06-05"
---

# Fund/SERV Fixed Length Record Layouts (Part 1)

**Original File:** [fs_fixed_part1_layout_mfs312_20230830.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_fixed_part1_layout_mfs312_20230830.pdf)  
**Category:** Networking_FundSERV  
**Total Pages:** 192  
**File Size:** 1380.2 KB  

---

## Page 1

 
 
 
Fund/SERV® 
FIXED LENGTH RECORD LAYOUTS (PART 1) 
 
AUGUST 30, 2023 
 

---

## Page 2

Fixed Length Record Layouts (Part 1) 
History of Important Notices 2 
TABLE OF CONTENTS 
History of Important Notices ............................................................................................................................... 7 
Summary of Changes .......................................................................................................................................... 9 
Introduction ........................................................................................................................................................ 10 
1. General .............................................................................................................................................10 
2. Fixed Length Format ........................................................................................................................10 
3. Control Number ................................................................................................................................11 
4. Check Digit .......................................................................................................................................11 
5. SSN/EIN Start Sequence Number ...................................................................................................12 
Record Layouts .................................................................................................................................................. 14 
02.00.00 Fixed Record Layout Column Headings ............................................................................................14 
Record Type List ................................................................................................................................................ 16 
02.01.00 Record Type List ................................................................................................................................16 
Order (001) .......................................................................................................................................................... 19 
02.01.01 Order (001) Record 1 of 7..................................................................................................................19 
02.01.02 Order (001) Record 2 of 7..................................................................................................................23 
02.01.03 Order (001) Record 3 of 7..................................................................................................................26 
02.01.04 Order (001) Record 4 of 7..................................................................................................................31 
02.01.05 Order (001) Record 5 of 7..................................................................................................................35 
02.01.06 Order (001) Record 6 of 7..................................................................................................................37 
02.01.07 Order (001) Record 7 of 7..................................................................................................................40 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund 
Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund (140) ............................................... 42 
02.02.01 As-Of-Order (004) Record 1 of 8 .......................................................................................................42 
02.02.02 As-Of-Order (004) Record 2 of 8 .......................................................................................................47 
02.02.03 As-Of-Order (004) Record 3 of 8 .......................................................................................................50 
02.02.04 As-Of-Order (004) Record 4 of 8 .......................................................................................................56 
02.02.05 As-Of-Order (004) Record 5 of 8 .......................................................................................................60 
02.02.06 As-Of-Order (004) Record 6 of 8 .......................................................................................................61 
02.02.07 As-Of-Order (004) Record 7 of 8 .......................................................................................................63 

---

## Page 3

Fixed Length Record Layouts (Part 1) 
History of Important Notices 3 
02.02.08 As-Of-Order (004) Record 8 of 8 .......................................................................................................68 
Extended Correction Transfer (200); Extended Correction Transfer Acknowledgment (201)  ................... 70 
02.03.01 Extended Correction Transfer (200) Record 1 of 3 ...........................................................................70 
02.03.02 Extended Correction Transfer (200) Record 2 of 3 ...........................................................................73 
02.03.03 Extended Correction Transfer (200) Record 3 of 3 ...........................................................................74 
Order Acknowledgment for Money Market Purchase (101); Firm Delete (102); Release to [[settlement]] (109); 
Registration Acknowledgment (112); Delete Pending Registration (Registered Ex -Fund/SERV) (113); 
Receiving Fund Exit from ToRA (214) .............................................................................................................. 75 
02.04.01 Order Acknowledgement for Money Market Purchase (101) Record 1 of 2  .....................................75 
02.04.02 Order Acknowledgement for Money Market Purchase (101) Record 2 of 2  .....................................78 
Fund Reject (100); Fund Delete (108); Registration Rejection (114); Delete Pending Release to [[settlement]] 
(Settled Ex-Fund/SERV) (129) ........................................................................................................................... 80 
02.05.01 Fund Reject (100) Record 1 of 2 .......................................................................................................80 
02.05.02 Fund Reject (100) Record 2 of 2 .......................................................................................................83 
Exchange Order (015) ........................................................................................................................................ 85 
02.06.01 Exchange Order (015) Record 1 of 5 ................................................................................................85 
02.06.02 Exchange Order (015) Record 2 of 5 ................................................................................................88 
02.06.03 Exchange Order (015) Record 3 of 5 ................................................................................................90 
02.06.04 Exchange Order (015) Record 4 of 5 ................................................................................................93 
02.06.05 Exchange Order (015) Record 5 of 5 ................................................................................................95 
APPENDIX – SUMMARY OF CHANGES ........................................................................................................... 97 
Summary of Changes – effective Q2  05/15/2023............................................................................................ 98 
1. New Data Field in Existing Record Sequence .................................................................................98 
Summary of Changes–Effective Q1 03/28/2022 .............................................................................................. 99 
2. Requirements Changed for Existing Fields ......................................................................................99 
3. New Data Fields in New Optional Record Sequence ....................................................................101 
4. New Data Field in Existing Record Sequence ...............................................................................103 
5. New Optional Record Type ............................................................................................................103 
6. New Reject Code ...........................................................................................................................103 
7. Notes Added to Existing Field ........................................................................................................104 
Summary of Changes–Effective Q1 03/25/2019 ............................................................................................ 105 
Reject Codes ..................................................................................................................................................105 

---

## Page 4

Fixed Length Record Layouts (Part 1) 
History of Important Notices 4 
Summary of Changes–effective Q4 11/20/2017 ............................................................................................. 106 
1. New Values Added to Existing Fields ............................................................................................106 
2. Requirements Changed for Existing Fields ....................................................................................111 
3. Requirements Changed for Existing Records ................................................................................113 
4. Modified Description of Existing Field ............................................................................................114 
Summary of Changes–effective Q3 09/26/2016 ............................................................................................. 115 
1. New Fields ......................................................................................................................................115 
2. Renamed Fields .............................................................................................................................117 
3. Requirements Changed for Existing Fields ....................................................................................119 
4. Reject Codes ..................................................................................................................................139 
5. Requirements Changed for Existing Record Number ....................................................................140 
Summary of Changes–effective Q1 02/29/2016 ............................................................................................. 141 
Summary of changes–effective Q3 07/27/2015 ............................................................................................. 142 
1. Requirements Changed for Existing Field......................................................................................142 
2. Requirements Changed for Existing Record Number ....................................................................142 
Summary of changes–effective Q2 04/27/2015 ............................................................................................. 143 
Requirements Changed for Existing Fields ....................................................................................................143 
Summary of changes–effective Q3 07/02/2014 ............................................................................................. 144 
1. Documentation Changes ................................................................................................................144 
Summary of changes–effective Q3 07/28/2014 ............................................................................................. 145 
1. New Fields ......................................................................................................................................145 
2. Reject Codes ..................................................................................................................................145 
3. Modified Description of Existing Fields ..........................................................................................145 
Summary of changes–effective Q4 11/18/2013 ............................................................................................. 147 
1. New Fields ......................................................................................................................................147 
2. Values or Comments Added to or Deleted from Existing Fields ....................................................148 
3. Reject Codes ..................................................................................................................................150 
Summary of changes–effective Q1 3/18/2013 ............................................................................................... 151 
1. Values or Comments Added to or Deleted from Existing Fields ....................................................151 
2. Requirements Changed for Existing Fields ....................................................................................158 

---

## Page 5

Fixed Length Record Layouts (Part 1) 
History of Important Notices 5 
Summary of changes–effective Q1 2013 ....................................................................................................... 160 
1. Modified Description of Values of Existing Field ............................................................................160 
Summary of changes–effective Q2 04/23/2012 ............................................................................................. 162 
1. Values or Comments Added to or Deleted from Existing Fields ....................................................162 
2. Requirements Changed for Existing Fields ....................................................................................163 
Summary of changes–effective Q4 10/17/2011 ............................................................................................. 165 
1. New Fields ......................................................................................................................................165 
2. Values or Comments Added to or Deleted from Existing Fields ....................................................165 
3. Requirements Changed for Existing Fields ....................................................................................166 
Summary of changes–effective Q4 12/5/2011 ............................................................................................... 167 
1. New Fields ......................................................................................................................................167 
Summary of changes–effective Q2 2011 ....................................................................................................... 168 
1. New Fields ......................................................................................................................................168 
2. Values or Comments Added to or Deleted from Existing Fields ....................................................168 
Summary of changes–effective Q1 2011 ....................................................................................................... 170 
1. Record Changed from Optional to Optional Conditional ................................................................170 
2. Renamed Fields .............................................................................................................................170 
3. Values or Comments Added to or Deleted from Existing Fields ....................................................171 
4. Requirements Changed for Existing Fields ....................................................................................173 
5. Reject Codes ..................................................................................................................................174 
Summary of changes–effective Nov 2010 ..................................................................................................... 176 
1. New Fields ......................................................................................................................................176 
2. Renamed Fields .............................................................................................................................176 
3. Requirements Changed for Existing Fields ....................................................................................177 
4. Reject Codes ..................................................................................................................................178 
Summary of changes–effective Q4 2009 ....................................................................................................... 180 
1. New Fields ......................................................................................................................................180 
2. Record Changed from Optional to Optional Conditional ................................................................181 
3. Renamed Fields .............................................................................................................................182 
4. Values or Comments Added to or Deleted from Existing Fields ....................................................182 

---

## Page 6

Fixed Length Record Layouts (Part 1) 
History of Important Notices 6 
5. Reject Codes ..................................................................................................................................184 
Summary of changes–effective Q3 2009 ....................................................................................................... 186 
1. New Fields ......................................................................................................................................186 
2. Record Changed from Optional to Required ..................................................................................186 
3. Renamed Fields .............................................................................................................................187 
4. Values or Comments Added to or Deleted from Existing Fields ....................................................188 
5. Reject Codes ..................................................................................................................................190 
Summary of changes–effective Dec 2008 ..................................................................................................... 191 
1. New Fields ......................................................................................................................................191 
2. New Values to Existing Fields ........................................................................................................191 
 

---

## Page 7

Fixed Length Record Layouts (Part 1) 
History of Important Notices 7 
HISTORY OF IMPORTANT NOTICES 
Dates Important Notices 
August 30, 2023 
• Record has been rebranded and reviewed. 
March 10, 2023 
• 529 Account Plan fields added to 018 and 019 records (effective May  
15, 2023). 
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
Effective Date: September 26, 2016 Please see Important Notice: 
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
Documentation Changes Please see Important Notice: 
a7592 P&S 7162 Dated March 1, 2013 

---

## Page 8

Fixed Length Record Layouts (Part 1) 
History of Important Notices 8 
Dates Important Notices 
Effective Date:  April 23, 2012 Please see Important Notice:  
A735 P&S 6925 Dated January 12, 2012 
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

## Page 9

Fixed Length Record Layouts (Part 1) 
Summary of Changes 9 
SUMMARY OF CHANGES 
See the Appendix for the summary of changes. 
 

---

## Page 10

Fixed Length Record Layouts (Part 1) 
Introduction 10 
INTRODUCTION 
1. General 
Some of Fund/SERV record layout features are: 
• Fund/SERV records can be received or submitted in either of two formats: fixed length or variable length.  
Data received or submitted interactively (via MQM) must be in variable length format.  This document 
describes Fund/SERV fixed length record layouts. 
• Only [[NSCC]] rejected transactions are being returned by [[NSCC]] to the originating [[participant]]. Accepted 
transactions are being sent to the contra [[participant]] only. 
• Fund Number in input records is always an optional field. If fund number is not provided on input, it will be 
identified by Fund/SERV via the security issue. The contra side will always get the records with the fund 
number. 
Note: 
When a fund generates the control number (as in Fund Originated Order), the fund number within the control number is 
required. 
• The term ‘firm’ throughout this document refers to dealer, [[Broker]], bank, etc. (not to be confused with 
‘fund’). 
• When rejecting a transaction for more than one reason, Fund/SERV reports multiple reject codes via 
record type 120 (see section 02.25.01) which follows the rejected transaction back to the originating 
[[participant]]. 
2. Fixed Length Format 
Each fixed length transaction consists of one or more 100-byte long records. 
Each 100-byte long record starts with the following two fields: 
1. Physical Sequence Number (bytes 1-2) 
2. Logical Sequence Number (bytes 3-4) 
 
The physical sequence number of the first record in a submitted transaction must be 01 and should increase by 
1 from record to record within the transaction. 
The physical sequence number of the last record in a submitted transaction must start with 9.  
The logical sequence numbers within a submitted transaction must be in ascending order and cannot exceed 
the maximum allowed for that transaction (see record layouts). 
Example: 
The following are valid sequence numbers for registration: 
0101 0202 0303 0404 0507 0608 0709 9810 
Note: 
• The last physical sequence number is 98 (rather than 08) to indicate that it is the last physical record of this registration. 
• Logical sequence numbers 05 and 06 (optional records) are not included in this registration. 

---

## Page 11

Fixed Length Record Layouts (Part 1) 
Introduction 11 
3. Control Number 
Control number rules are as follows: 
1. Control number is 15 bytes long and is generated by the [[participant]] who submits the original transaction 
(firm for record type 001, fund for record type 007 etc.). 
2. Control number format is ‘ppppydddssssssc’ where:  
 
pppp = Originating [[participant]] (firm/fund/TPA/SP/investment agent) [[NSCC]] number  
y = Last digit of year  
ddd = Julian date  
ssssss = Sequential number  
c = Check digit (using Modulus 10 Double Add Double algorithm. See item 4 below)  
Note: 
It is recommended that the Julian date 'yddd' reflects the order submission date (so it's easy to create unique control 
numbers). However, Fund/SERV does not force that. 
Control number for ACATS Transfer (record type 018) is 15 bytes long and is generated by Fund/SERV. The 
format is ‘catsaydddssssss’ where:  
catsa = CATSA  
y = Last digit of year  
ddd = Julian date  
ssssss = Sequential number 
4. Check Digit 
To calculate a check digit for the control number, using Modulus 10 Double Add Double algorithm, take the 
following steps: 
1. Assign a position number to each digit of the control number according to its position in the control 
number as follows: 
• Odd position: the assigned position number is 1. 
• Even position: the assigned position number is 2. 
2. Multiply each digit of the control number by its assigned position number. 
3. Sum the products up but note the following: if a product is two digits long, add each digit separately to the 
sum. 
4. Subtract the last digit of the sum from 10. The last digit of the result (also called 10 Complement) is the 
check digit

---

## Page 12

Fixed Length Record Layouts (Part 1) 
Introduction 12 
 
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
10-6 = 4 
6. The check digit is 4 and the whole control number is: 135720280000374 
5. SSN/EIN Start Sequence Number 
Field SSN/EIN Start Sequence Number is a two-byte field starting at position 93 of record #1 in the following 
record layouts: 
Order (001) layout (Section 02.01.01) 
As-Of Order (004)  (Section 02.02.01) 
Exchange (015) layout (Section 02.06.01) 
Correction (003) layout (Section 02.29.01) 
The value in field SSN/EIN Start Sequence Number should be the same as the logical sequence number of the 
first SSN/EIN record. 

---

## Page 13

Fixed Length Record Layouts (Part 1) 
Introduction 13 
Example1: 
An order (001) with five records of the order layout and two SSN/EIN records. 
a. The physical and logical sequence numbers of the transaction are respectively: 
0101 = 1st order record 
 0202 = 2nd order record 
0303 = 3rd order record 
0404 = 4th order record 
0505 = 5th order record 
0606 = 1st SSN/EIN Record 
9707 = 2nd (also last) SSN/EIN Record 
b. The value in field SSN/EIN Start Sequence Number should be 06, which is the same as the logical sequence number of 
the first SSN/EIN record. 
Example2: 
An order (001) with records #1 through #4 and #6 of the order layout and one SSN/EIN record. 
a. The physical and logical sequence numbers of the transaction are respectively: 
0101 = 1st order record 
0202 = 2nd order record 
0303 = 3rd order record 
0404 = 4th order record 
0506 = 6th order record (note: optional record #5 is not provided) 
9607 = 1st (also last) SSN/EIN Record 
b. The value in field SSN/EIN Start Sequence Number should be 07, which is the same as the logical sequence number of 
the first (and last in this case) SSN/EIN record. 

---

## Page 14

Fixed Length Record Layouts (Part 1) 
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
Reject 
Code 
- The reject code which indicates that this field is invalid.  
Notes: 
• Alphanumeric type fields may include any character in the computer character set but should not include unprintable 
characters such as Low-Value, High-Value, Comp-3 fields, etc., since these kinds of characters may cause problems 
during transmission time. 
• Numeric type fields may include digits (0-9) only. 
• Required fields mean the following: 
a. Fields with specified list of values must have one of those values.  
b. Alphanumeric type fields without specified list of values may have any value as described in the first note above but 
must not be spaces.  
c. Numeric type fields without a specified list of values must be numeric greater than zero.  
d. Fields with other requirements must follow these requirements (for example Firm Number must be valid and eligible 
for Fund/SERV). 
• Optional fields mean the following:  
a. Fields with specified list of values must have one of those values or space.  
b. Alphanumeric type fields without specified list of values may have any value as described in the first note above.  
c. Numeric type fields without specified list of values must be numeric or space.  
d. Fields with other requirements must follow these requirements or may be space (for example Fund Number must be 
valid and eligible for Fund/SERV or may be space) 
• All dates in the layouts have the format mmddccyy (except where otherwise indicated) where:  
mm = Month  
dd = Day in month  

---

## Page 15

Fixed Length Record Layouts (Part 1) 
Record Layouts 15 
cc = Century  
yy = Year in century 
Example: 
November 23, 2023, is represented as: 11232023 

---

## Page 16

Fixed Length Record Layouts (Part 1) 
Record Type List 16 
RECORD TYPE LIST 
The following are Fund/SERV record types and the section numbers where their layouts are described in this 
document: 
02.01.00 Record Type List 
Record Type Description  Section No. 
000 [[NSCC]] Output Header 02.20.01 
001 Order 02.01.01 
002 Defined Contribution Plan Information 02.15.01 
003 Correction 02.29.01 
004 As-Of Order 02.02.01 
005 Confirmation 02.02.01 
006 Reconfirmation 02.02.01 
007 Fund Originated Order 02.02.01 
009 Fund Originated As-of Order 02.02.01 
011 Cash Adjustment 02.08.01 
015 Exchange Order 02.06.01 
016 Exchange Confirmation 02.07.01 
017 Exchange Reconfirmation 02.07.01 
018 ACATS Transfer 02.11.01 
019 ACATS Transfer Acknowledgment/Rejection 02.12.01 
021 Post [[settlement]] Exchange Cancellation 02.07.01 
025 Correction Confirmation 02.29.01 
026 Post [[settlement]] Correction by Fund 02.29.01 
030  Interval Fund Acknowledgement  02.31.01 
070 Settling Trade Detail 02.23.01 
071 Settling Trade Trailer 02.24.01 
072 X-[[settlement]] Trade Detail 02.23.01 
073 X-[[settlement]] Trade Trailer 02.24.01 

---

## Page 17

Fixed Length Record Layouts (Part 1) 
Record Type List 17 
Record Type Description  Section No. 
074 Settling Trade Detail for TPA/Investment Agent/TPP 02.23.01 
075 Settling Trade Trailer for TPA/Investment Agent/TPP 02.23.01 
080 Pending ACATS Transfer Acknowledgment Reminder 02.17.01 
081 Order Not Acted Upon Reminder 02.17.01 
082 Deletion of Order Not Acted Upon Reminder 02.17.01 
083 Pending Registration Reminder 02.17.01 
084 Extended Correction Transfer Not Acted Upon Reminder 02.17.01 
085 Pending Release to [[settlement]] Reminder 02.17.01 
086 Pending Correction Confirmation Reminder 02.17.01 
087 Pending Registration Acknowledgment Reminder 02.17.01 
088 Pending Exchange Reconfirmation Reminder 02.17.01 
089 Post [[settlement]] Correction/Cancellation Not Acted Upon 02.17.01 
090 Retiring Participants 02.16.01 
091 Pending ToRA Acknowledgment Reminder 02.17.01 
092 Pending ToRA Confirmation Reminder 02.17.01 
100 Fund Reject 02.05.01 
101 Order Acknowledgment for Money Market Purchase 02.04.01 
102 Firm Delete 02.04.01 
108 Fund Delete 02.05.01 
109 Release to [[settlement]] 02.04.01 
112 Registration Acknowledgment 02.04.01 
113 Delete Pending Registration (registered ex-Fund/SERV) 02.04.01 
114 Registration Rejection 02.05.01 
120 Multiple Reject Codes 02.25.01 
129 Delete Pending Release to [[settlement]] (settled ex-Fund/SERV) 02.05.01 
139 Firm Exit 02.28.01 
140 Post [[settlement]] Cancellation by fund 02.02.01 
200 Extended Correction Transfer 02.03.01 

---

## Page 18

Fixed Length Record Layouts (Part 1) 
Record Type List 18 
Record Type Description  Section No. 
201 Extended Correction Transfer Acknowledgment 02.03.01 
210 Transfer of Retirement [[Asset]] (ToRA) 02.13.01 
211 ToRA Acknowledgment 02.14.01 
212 ToRA Confirmation 02.14.01 
213 ToRA Reconfirmation 02.14.01 
214 Receiving Fund Exit from ToRA 02.04.01 
400 Short Registration 02.09.01 
401 Full Registration 02.10.01 
999 Trailer—Firm/TPA/Investment Agent/TPP Input 02.18.01 
999 Trailer—Fund Input 02.19.01 
999 Trailer—[[NSCC]] Output 02.21.01 
GTT Grand Total Trailer 02.22.01 

---

## Page 19

Fixed Length Record Layouts (Part 1) 
Order (001) 19 
ORDER (001) 
02.01.01 Order (001) Record 1 of 7 
Required 
Record 1 of 7 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 01 R 004 
Originator Type 5 5 1 A/N A = Investment Agent 
B = Firm 
T = TPA 
S = Service Provider for B = Firm 
P = Service Provider for T = TPA 
V = TPP (Third Party Provider) 
R 187 
Filler 6 7 2 A/N Space R  
Firm Number 8 11 4 N  R 008 
Filler 12 14 3 A/N Space R  
Record Type 15 17 3 A/N 001 = Order R 002 
Test Indicator 18 18 1 A/N 0 = Production 
1 = Test 
R 122 
Filler 19 19 1 A/N Space R  
Fund Number 20 23 4 N  O 100 
Filler 24 26 3 A/N Space R  
Security Issue Country 
Code 
27 28 2 A/N Space. For future use R  
Security Issue [[ID]]  29 37 9 A/N  R 007 
Security Issue Check 38 38 1 A/N Space. For future use R  

---

## Page 20

Fixed Length Record Layouts (Part 1) 
Order (001) 20 
Record 1 of 7 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Security Issue Type 39 40 2 A/N Required if 24 (Money Market) 
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
Control Number 41 55 15 A/N  R 005 
Correction Indicator  56 56 1 A/N Space R 006 
Transaction Type  57 57 1 A/N 0 = Single purchase 
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
Transaction Code 
 
58 59 2 A/N 01 = Initial purchase 
02 = Subsequent purchase 
03 = Partial [[liquidation]] 
04 = Full [[liquidation]] 
 
For Security Type = 48 (Interval 
Fund) future dated orders, only 03 
and 04 are allowed. 
R 018 

---

## Page 21

Fixed Length Record Layouts (Part 1) 
Order (001) 21 
Record 1 of 7 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Submission Date 60 67 8 N mmddccyy R 101 
Trade Date 
 
68 75 8 N mmddccyy 
 
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
76 76 1 A/N 0 = Book [[shares]]—firm name 
1 = Book [[shares]]—customer name 
2 = Physical [[shares]] 
3 = Both book and physical [[shares]] 
Must be 0 or 1 for Money Market 
trades 
R 015 
PI Delivery Indicator 77 77 1 A/N Required for all purchases if 
Book/Physical Share Ind = 2. 
0 = Deliver to customer 
1 = Deliver to firm 
2 = Deliver to agent for firm 
OC 039 
Filler 78 78 1 A/N Space R  
[[settlement]] Override 
Reason Code 
79 80 2 A/N Required (but must not be 04) if 
Anticipated [[settlement]] Date is 
provided. 
01 = Wrap fee account 
02 = 401K 
03 = Other 
04 = X-[[settlement]] 
05 = Section 529 Account—
Qualified State Tuition Program 
06 = X-[[settlement]] offshore 
enhanced (allowed for Security 
Types 62 and 63 only) 
07 = Refer to [[Asset]] Type Indicator 
Must be space for settling EUR and 
GBP transactions (Security Issue 
Type 63 only). 
OC 179 

---

## Page 22

Fixed Length Record Layouts (Part 1) 
Order (001) 22 
Record 1 of 7 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
[[NSCC]] Rejection 
Indicator 
81 81 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], multiple 
errors 
R  
[[NSCC]] Reject Code 82 84 3 A/N Input: Space 
Output: Reject code 
R  
TPA/Investment 
Agent/TPP Number  
85 88 4 A/N Required if: 
Originator Type = (T or P or A or V) 
OR 
Membership Identifier = 02 or 03. 
 
If Originator Type = T or P, then 
[[Asset]] Type Indicator must be F 
through O or S or T (indicating 
DCC&S) 
OC 188 
Service Provider 
Number 
89 92 4 A/N Required if Originator Type = S or P OC 215 
SSN/EIN Start 
Sequence Number 
93 94 2 A/N See SSN/EIN Start Sequence 
Number in the Introduction section. 
Required if SSN/EIN Suffix is 
provided. Not allowed otherwise.  
OC 257 
Total SSN/EIN Records 95 96 2 N Required if SSN/EIN Suffix is 
provided. Not allowed otherwise.  
OC 258 
Filler 97 100 4 A/N Space R  
 
 
  

---

## Page 23

Fixed Length Record Layouts (Part 1) 
Order (001) 23 
02.01.02 Order (001) Record 2 of 7 
Required 
Record 2 of 7 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 02 R 004 
Filler 5 7 3 A/N Space R  
Share Quantity 8 21 14 N 9,999,999,999.9999 
Optional if full [[liquidation]]; 
Not allowed if Money Amount > 0.  
RC 019 
Customer Account 
Number at Firm 
22 41 20 A/N Optional if [[settlement]] Override 
Reason Code = 04, 06 OR if 
Membership Identifier is provided.  
RC 020 
Fund Account Indicator 42 42 1 A/N 0 = New account–U.S. 
1 = New account–non-U.S. 
2 = Existing account–U.S. 
3 = Existing account–non-U.S. 
4 = New account–U.S. Tax Resident 
Living Abroad 
5 = Existing account–U.S. Tax 
Resident Living Abroad  
R 010 
Customer Account 
Number at Fund 
43 62 20 A/N Required for all non-networked 
liquidations 
(Network Control Ind = 0 and Trans 
Code = 03 or 04) 
OC 011 

---

## Page 24

Fixed Length Record Layouts (Part 1) 
Order (001) 24 
[[Asset]] Type Indicator 63 63 1 A/N 0 = Not applicable 
1 = Current year payment 
2 = Prior year payment 
3 = IRA rollover 
4 = [[Asset]] transfer 
5 = Employee—prior year 
6 = Employee—current year 
7 = Employer—prior year 
8 = Employer—current year 
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
W = 529 Beneficiary Change-In-
Family 
 
Note: 
D, P, Q, U, V and W indicate Section 
529 Plan.  
R 013 
Agent for Firm Number 64 67 4 A/N Required if Originator Type = V TPP 
(Third Party Provider) 
OC 271 

---

## Page 25

Fixed Length Record Layouts (Part 1) 
Order (001) 25 
Record 2 of 7 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Network Control 
Indicator 
68 68 1 A/N 0 = Non-networked 
3 = Matrix level 3 
4 = Matrix level 4 
R 047 
Fraction Indicator 69 69 1 A/N 0 = Round up 
1 = Round down 
2 = Issue fraction 
3 = Not applicable 
R 014 
Gross [[settlement]] 
Indicator 
70 70 1 A/N 0 = Not applicable 
1 = Settle net 
2 = Settle gross 
R 094 
Transaction Received 
Time 
71 76 6 N hhmmss Eastern Time 
000000 (midnight) to 235959 
 
Required when “Money Market 
[[Liquidity]] Fee/Redemption Gate 
Indicator” = ‘F’ (Fund). 
OC 168 
Membership Identifier 77 78 2 A/N 01 = Trust [[Member]] 
02 = Networking info required for 
TPA/Investment Agent 
03 = TPP (Third Party Provider) 
O 181 
Filler 79 79 1 A/N Space R  
Transaction Payment 
Type Indicator 
80 80 1 A/N Required if [[settlement]] Override 
Reason Code = 04. 
1 = Shareholder wire 
2 = Shareholder ACH 
3 = Address of Record (AOR). 
3 allowed for [[liquidation]] (Transaction 
Code = 03 or 04) only 
OC 216 
Transaction Bank 
Account Number 
81 100 20 A/N Required if Transaction Payment 
Type Indicator = 1 or 2 
OC 142 
 
 
  

---

## Page 26

Fixed Length Record Layouts (Part 1) 
Order (001) 26 
02.01.03 Order (001) Record 3 of 7 
Required 
Record 3 of 7 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 03 R 004 
Filler 5 7 3 A/N Space R  
Money Amount 8 23 16 N 99,999,999,999,999.99 
Optional for non-Money Market trades 
if full [[liquidation]]; 
Not allowed for non-Money Market 
trades if Share Quantity > 0. 
This amount will be settled by [[NSCC]] 
for Money Market purchase if no 
confirmation has been received. 
RC 019 
Currency Indicator 24 26 3 A/N  O 110 
Anticipated [[settlement]] 
Date 
 
27 34 8 A/N mmddccyy 
For Security Issue Type = 63, 
Required if [[settlement]] Override 
Reason Code is space 
 
For other Security Types: 
1. Required if [[settlement]] Override 
Reason Code is provided and is 
not 04 or 06 (x-[[settlement]]). 
2. Not allowed if [[settlement]] 
Override Reason Code = 04. 
 
This field should not be populated 
when Security Type = 48, and 
Transaction Code = 03 (Partial 
[[liquidation]]) or 04 (Full [[liquidation]]). If 
populated, [[NSCC]] will [[default]] the value 
to 12319999 and pass the order to the 
Fund. 
OC 180 
Branch Identification 
Number 
35 43 9 A/N Optional under the following 
conditions: 
• Membership Identifier = 01 or 02 
and Agent for Firm Number is not 
provided. 
• Originator Type = V(TPP) 
RC 035 

---

## Page 27

Fixed Length Record Layouts (Part 1) 
Order (001) 27 
Record 3 of 7 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Related Trade Indicator 44 44 1 A/N 0 = No 
1 = Yes 
R 065 
Related Trade Identifier 45 46 2 A/N Required if 
Related Trade Indicator = 1 
OC 105 
Customer Name 47 66 20 A/N  R 063 
SSN/EIN Indicator 67 67 1 A/N 0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN  
R 102 
SSN/EIN Number 68 76 9 A/N  R 103 
[[liquidation]] Indicator 77 77 1 A/N Required if Trans Type = 5. 
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
D = 529 Plan Account—Beneficiary 
Disability 
E = 529 Plan Account–Beneficiary 
Death 
F = 529 Plan Account–Beneficiary 
Scholarship 
Notes: 
• 4 through F should apply only to 
transactions with CDSC Waivers 
• C through F should only apply to 
Section 529 plans  
OC 046 

---

## Page 28

Fixed Length Record Layouts (Part 1) 
Order (001) 28 
Record 3 of 7 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
NAV Reason Code  78 78 1 A/N Required if Trans Type = 3. 
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
9 = Section 529 Account—Qualified 
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
 
79 80 2 A/N Required for Transaction Codes 
 
01 (Initial purchase) 
02 (Subsequent purchase) 
OC 012 
Redemption Fee 
Indicator  
81 81 1 A/N 0 = Short-Term Redemption (STR) 
1 = STR with CDSC 
2 = Money Market [[Liquidity]] Fee 
3 = Money Market [[Liquidity]] Fee with 
CDSC 
O 248 

---

## Page 29

Fixed Length Record Layouts (Part 1) 
Order (001) 29 
Record 3 of 7 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Short-Term Redemption 
Fee Waiver Indicator  
82 82 1 A/N 1 = STR waiver due to correction 
2 = Death 
3 = Disability 
4 = Mandatory distribution 
5 = Systematic withdrawal 
6 = Defined contribution 
7 = Hardship 
8 = Auto Rebalance 
9 = DC–Termination Distribution 
A = DC–Involuntary Distribution 
B = DC–Forfeitures 
C = DC–Loans 
D = DC–Excess Contributions 
E = Wrap Program 
F = Fund of Funds 
G = Divorce/QDRO 
H = Plan fees QDRO 
O 249 
Filler 83 86 4 A/N Space R  
Transaction ABA 
Routing Number 
87 95 9 A/N Required if Transaction Payment Type 
Indicator = 1 or 2 
OC 141 
De-minimis repurchase 
waiver code 
96 96 1 A/N Blank or 0 = No; 
1 = Yes 
 
Allows Firms to indicate if an Interval 
Fund repurchase order is eligible for 
de-minimis treatment in accordance 
with the Fund’s prospectus. 
 
Should only be populated for an 
Interval Fund. 
O 286 
Filler 97 98 2 A/N Space R  

---

## Page 30

Fixed Length Record Layouts (Part 1) 
Order (001) 30 
Record 3 of 7 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Omnibus Account 
Indicator 
99 99 1 A/N 0 = Not Omnibus Account 
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
100 100 1 A/N 0 = Trade Date not forwarded 
1 = Trade Date forwarded 
Must be 1 if Trade Date not equal 
Submission Date. 
 
Trade Date forwarded is only allowed 
if: 
• Security Type = 48 (Interval 
Fund) and Transaction Code = 
03 (Partial [[liquidation]]) or 04 
(Full [[liquidation]]). 
• Security Type = 62 or 63 
OC 229 
 
 
  

---

## Page 31

Fixed Length Record Layouts (Part 1) 
Order (001) 31 
02.01.04 Order (001) Record 4 of 7 
Required if any of the following fields in this record are required: 
• Country of Origin 
• IRA/529 [[liquidation]] Indicator 
• Periodic Frequency Indicator 
• Beneficiary SSN/EIN Number 
• Social Code (when “Transaction Code” =01) 
Record 4 of 7 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 04 R 004 
Filler 5 7 3 A/N Space R  
Related Account 
Number 
8 27 20 A/N  O  
Related Account 
Number Indicator 
28 28 1 A/N Required if Related Account Number 
is provided. 
1 = Fund 
2 = Firm 
3 = Customer 
OC 157 Related Account 
Security Issue Country 
Code 
29 30 2 A/N Space. For future use R  
Related Account 
Security Issue [[ID]] 
31 39 9 A/N Required if Related Account Number 
is provided 
OC 107 
Related Account 
Security Issue Check 
Digit 
40 40 1 A/N Space. For future use R  
Country of Origin 
(Country Code) 
41 42 2 A/N Required for non-omnibus account 
(Omnibus Account Indicator = ‘0’ or 
space) 
if State of Sale (State Code) = ‘FF’ 
OC 067 
Sales Charge Rate 43 46 4 N 9.999 O 025 
ROA/LOI Value 47 62 16 N 99,999,999,999,999.99 O 064 
LOI Number/Date 63 70 8 A/N  O  

---

## Page 32

Fixed Length Record Layouts (Part 1) 
Order (001) 32 
Record 4 of 7 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
IRA/529 [[liquidation]] 
Indicator 
71 71 1 A/N 0 = Not applicable 
1 = Distribution—premature 
2 = Distribution—disability 
3 = Distribution—death 
4 = Distribution—normal 
5 = Hardship withdrawal 
6 = Loan 
7 = Rollover 
8 = Adjust prior year excess 
9 = Adjust current year excess 
A = Qualified 
B = Non-Qualified 
C = Distribution–Non-Taxable 
D = 529 Owner Change 
E = 529 Beneficiary Change–In-
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
72 72 1 A/N 0 = Not applicable 
1 = Short due to correction 
O 169 

---

## Page 33

Fixed Length Record Layouts (Part 1) 
Order (001) 33 
Record 4 of 7 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Periodic Frequency 
Indicator 
73 73 1 A/N Required if [[liquidation]] Indicator = 8 or 
Program Transaction Indicator = 1 
0 = Weekly 
1 = Monthly 
2 = Bi-monthly 
3 = Quarterly 
4 = Semiannual 
5 = Annual 
6 = Non-Periodic (ad Hoc) 
OC 083 
Shareholder Date of 
Birth 
74 81 8 N mmddccyy 
For 529 use this field for Beneficiary 
Date of Birth 
O 204 
Social Code 82 83 2 A/N Required when “Transaction 
Code” = 01–Initial Purchase 
See Social Code List at 
https://dtcclearning.com/documents/m
utual-fund-services-1/mfs-cross-
product/codes-8/2498-social-
codes/file.html under Codes. 
OC 128 
Beneficiary SSN/EIN 
Number 
84 92 9 A/N Required if [[Asset]] Type Indicator = D, 
E, P, Q U, V or W and Transaction 
Code = 01 or 02 
[[Asset]] Type Indicators 
D (529 Current Year Contribution) 
E (UGMA account transferred to 
Section 529 Account) 
P (529 Previous Year Contribution) 
Q (529 Rollover Contribution) 
U (529 In–State Plan Transfer 
Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change- 
In-Family) 
 
Transaction Codes 
01 (Initial purchase) 
02 (Subsequent purchase 
OC 103 

---

## Page 34

Fixed Length Record Layouts (Part 1) 
Order (001) 34 
Record 4 of 7 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Beneficiary SSN/EIN 
Indicator 
93 93 1 A/N Required if Beneficiary SSN/EIN 
Number is provided. 
0 = Tax [[ID]] number 
1 = Social security number 
2 = Beneficiary TIN/EIN 
OC 102 
Standard [[ID]] 94 99 6 A/N  O  
Program Transaction 
Indicator 
100 100 1 A/N 1 = Systematic Withdrawal Plan 
(SWP) 
2 = Target Date Fund [[liquidation]] 
3 = Systematic Contribution 
(SIP/PAC/PIP) 
4 = Rebalance Purchase (Systematic) 
5 = Rebalance Redemption 
(Systematic) 
O 259 
 
 
  

---

## Page 35

Fixed Length Record Layouts (Part 1) 
Order (001) 35 
02.01.05 Order (001) Record 5 of 7 
Optional 
Record 5 of 7 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 05 R 004 
Filler 5 7 3 A/N Space R  
Account 
Representative 
Number 
8 16 9 A/N  O  
Account 
Representative Name 
17 31 15 A/N  O  
Confirm Number 32 43 12 A/N  O  
Memo Field 44 55 12 A/N  O  
IRA Withholding 
Percentage 
56 60 5 N 99.999 O 158 
Non-Taxable 
Percentage 
61 65 5 N 99.999 O 159 
Non-Taxable Money 
Amount 
66 81 16 N 99,999,999,999,999.99 O 160 
Closeout Fee Indicator 82 82 1 A/N 0 = [[DO]] not deduct 
1 = Deduct 
O 161 
LOI Indicator 83 83 1 A/N 0 = New 
1 = Existing 
O 162 
Original Control 
Number 
84 98 15 A/N  O  

---

## Page 36

Fixed Length Record Layouts (Part 1) 
Order (001) 36 
Record 5 of 7 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Original Correction 
Indicator 
99 99 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] 
correction/cancellation 
Space = No correction 
P not permitted if the Security Issue 
Type field value is 63 and [[settlement]] 
Override Reason Code field value is 
space. 
 
OC 164 
Filler 100 100 1 A/N Space R  
 
  

---

## Page 37

Fixed Length Record Layouts (Part 1) 
Order (001) 37 
02.01.06 Order (001) Record 6 of 7 
Required when Redemption Fee Indicator is provided or [[Asset]] Type Indicator = Q, U, V, or W.  
Optional for all other [[Asset]] Types. 
Record 6 of 7 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 06 R 004 
Filler 5 7 3 A/N Space R  
Redemption Fee Rate 8 14 7 N 99.99999 
 
Not allowed if “Redemption Fee 
Indicator” is not provided. 
 
Required when “Redemption Fee 
Indicator” is populated with either ‘2’ 
(Money Market [[Liquidity]] Fee) or ‘3’ 
(Money Market [[Liquidity]] Fee with 
CDSC). 
Zero value is not allowed when this 
field is required and “Redemption Fee 
Indicator” =’2’ or ‘3’. 
 
If “Redemption Fee Indicator” = 0 or 1, 
this field will be utilized to 
communicate a Short-Term 
Redemption (STR) Fee Rate. 
OC 250 
STR Fee Share 
Quantity  
15 28 14 N 9,999,999,999.9999 
 
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

---

## Page 38

Fixed Length Record Layouts (Part 1) 
Order (001) 38 
Record 6 of 7 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Redemption Fee 
Money Amount) 
29 44 16 N 99,999,999,999,999.99 
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
 
If “Redemption Fee Indicator” = 0 or 1, 
this field will be utilized to 
communicate a Short-Term 
Redemption (STR) Fee Money 
Amount. 
OC 252 
Cost Basis Money 
Amount  
45 60 16 N Required if the [[Asset]] Type Indicator = 
Q, U, V or W. 
Q (529 Rollover Contribution) 
U (529 In–State Plan Transfer 
Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change- 
In-Family) 
Format: 
99,999,999,999,999.99 
Zeros are allowed 
OC 261 
Earnings to Date 
Money Amount  
61 76 16 N Required if the [[Asset]] Type Indicator = 
Q, U, V or W. 
Q (529 Rollover Contribution) 
U (529 In–State Plan Transfer 
Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change- 
In-Family) 
Format: 
99,999,999,999,999.99 
Zeros are allowed 
OC 262 

---

## Page 39

Fixed Length Record Layouts (Part 1) 
Order (001) 39 
Record 6 of 7 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Negative Earnings to 
Date Indicator 
77 77 1 A/N N = Negative 
Spaces = Positive  
O 263 
Money Market [[Liquidity]] 
Fee/Redemption Gate 
Indicator 
78 78 1 A/N F = Fund. 
B = [[intermediary]] 
O 282 
Transaction Received 
Date 
79 86 8 A/N mmddccyy 
 
Required if the “Money Market 
[[Liquidity]] Fee/Redemption Gate 
Indicator” = F. 
OC 283 
Aggregated Order 
Indicator  
87 87 1 A/N Required if the “Money Market 
[[Liquidity]] Fee/Redemption Gate 
Indicator” = “F” or “B”. 
• 1 = Transactions are not 
aggregated 
• 2 = Transactions are aggregated 
by “like” orders (purchases 
separate from redemptions) 
• 3 = Transactions are net of 
purchases and redemptions 
• 4 = Unknown at time of placement 
OC 284 
Filler 88 100 13 A/N Filler R  
 
 
  

---

## Page 40

Fixed Length Record Layouts (Part 1) 
Order (001) 40 
02.01.07 Order (001) Record 7 of 7  
 
Optional 
Record 7 of 7  
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 07 R 004 
Filler 5 7 3 A/N Space R  
[[intermediary]] Program 
Indicator–1 
8 11 4 A/N Indicates the program, platform, or 
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
Indicator–2 
12 15 4 A/N Further defines the program, platform, 
or channel applicable to an account. 
Values are uniquely defined by each 
[[intermediary]].  
O  
Servicing Group [[ID]] 16 24 9 A/N This field is used to communicate 
aggregated servicing relationships or 
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
[[ID]]–1 
25 44 20 A/N This field is used to communicate 
additional relationship details to 
further define servicing relationships 
between accounts. 
Values are uniquely defined by each 
[[intermediary]].  
O  

---

## Page 41

Fixed Length Record Layouts (Part 1) 
Order (001) 41 
Record 7 of 7  
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Additional Relationship 
[[ID]]–2 
45 64 20 A/N This field is used to communicate 
additional relationship details to 
further define servicing relationships 
between accounts. 
Values are uniquely defined by each 
[[intermediary]]. 
O  
Filler 65 100 36 A/N Space R  
 

---

## Page 42

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 42 
AS-OF ORDER (004); CONFIRMATION (005); 
RECONFIRMATION (006); FUND ORIGINATED ORDER 
(007); FUND ORIGINATED AS-OF ORDER (009); POST 
[[settlement]] CANCELLATION BY FUND (140) 
02.02.01 As-Of-Order (004) Record 1 of 8 
Required 
Record 1 of 8 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Physical Sequence 
Number  
1 2 2 A/N  R 004 
Logical Sequence 
Number  
3 4 2 A/N 01  R 004 
Originator Type  5 5 1 A/N A = Investment Agent 
B = Firm 
F = Fund 
T = TPA 
V = TPP (Third Party Provider) 
R 187 
Filler  6 7 2 A/N Space  R  
Firm Number  8 11 4 N  R 008 
Filler  12 14 3 A/N Space  R  
Record Type  15 17 3 A/N 004 = As-Of Order 
005 = Confirmation 
006 = Reconfirmation 
007 = Fund Originated Order 
009 = Fund Originated As-Of Order 
140 = Post [[settlement]] Cancellation 
by fund 
Record Type 140 not permitted if the 
Security Issue Type field value is 63 
and [[settlement]] Override Reason 
Code field value is space 
RC 002/275 
Test Indicator  18 18 1 A/N 0 = Production 
1 = Test  
R 122 
Filler  19 19 1 A/N Space  R  

---

## Page 43

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 43 
Record 1 of 8 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Fund Number  20 23 4 N  O 100 
Filler  24 26 3 A/N Space  R  
Security Issue Country 
Code  
27 28 2 A/N Space. For future use  R  
Security Issue [[ID]]  29 37 9 A/N  R 007 
Security Issue Check 
Digit  
38 38 1 A/N Space. For future use  R  
Security Issue Type  39 40 2 A/N Required if 24 (Money Market) 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value 
against the Fund/SERV Security 
master file. [[NSCC]] leverages the 
Fund/SERV Security master file to 
determine value and associated 
processing rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 
OC 150 
Control Number  41 55 15 A/N  R 005 
Correction Indicator  56 56 1 A/N Required for record type 140. 
Required for record type 005 if 
confirming post [[settlement]] 
cancellation. 
Not allowed otherwise. 
P = Post [[settlement]] cancellation 
P not permitted if the Security Issue 
Type field value is 63 and 
[[settlement]] Override Reason Code 
field value is space  
OC 006 

---

## Page 44

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 44 
Record 1 of 8 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Transaction Type 57 57 1 A/N 0 = Single purchase 
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
Transaction Code 
 
58 59 2 A/N 01 = Initial purchase 
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
07 and 08 not permitted if the 
Security Issue Type field value is 63 
and [[settlement]] Override Reason 
Code field value is space 
 
For record types 005, 006 
For Security Type = 48 (Interval 
Fund) future dated orders, only 03 
and 04 are allowed. 
RC 018 
Submission Date  60 67 8 N mmddccyy  R 101 

---

## Page 45

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 45 
Record 1 of 8 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Trade Date 
 
68 75 8 N mmddccyy 
 
For record types 005, 006 
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
76 76 1 A/N 0 = Book [[shares]]—firm name 
1 = Book [[shares]]—customer name 
2 = Physical [[shares]] 
3 = Both book and physical [[shares]] 
Must be 0 or 1 for Money Market 
trades 
R 015 
PI Delivery Indicator  77 77 1 A/N Required for all purchases if 
Book/Physical Share Ind = 2. 
0 = Deliver to customer 
1 = Deliver to firm 
2 = Deliver to agent for firm  
OC 039 
Filler  78 78 1 A/N Space  R  
[[settlement]] Override 
Reason Code  
79 80 2 A/N Required (but must not be 04) if 
Anticipated [[settlement]] Date is 
provided. 
01 = Wrap fee account 
02 = 401K 
03 = Other 
04 = X-[[settlement]] 
05 = Section 529 Account—
Qualified State Tuition Program 
06 = X-[[settlement]] offshore 
enhanced (allowed for Security 
Types 62 and 63 only) 
07 = Refer to [[Asset]] Type Indicator 
Must be space for settling EUR and 
GBP transactions (Security Issue 
Type 63 only). 
OC 179 

---

## Page 46

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 46 
Record 1 of 8 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
[[NSCC]] Rejection 
Indicator  
81 81 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], multiple 
errors 
R  
[[NSCC]] Reject Code  82 84 3 A/N Input: Space 
Output: Reject code  
R  
TPA/Investment 
Agent/TPP Number 
85 88 4 A/N Required if: 
Originator Type (T or A or V) 
OR 
Membership Identifier = 02 or 03. 
If Originator Type = T or P, then 
[[Asset]] Type Indicator must be F 
through O or S or T (indicating 
DCC&S). 
OC 188 
Service Provider 
Number  
89 92 4 A/N  O 215 
SSN/EIN Start 
Sequence Number 
93 94 2 A/N See SSN/EIN Start Sequence 
Number in the Introduction section. 
Allowed for record type 004 only. 
Required if SSN/EIN Suffix is 
provided. Not allowed otherwise. 
OC 257 
Total SSN/EIN Records 95 96 2 N Allowed for record type 004 only. 
Required if SSN/EIN Suffix is 
provided. Not allowed otherwise.  
OC 258 
Filler 97 100 4 A/N Space R  
 
 
  

---

## Page 47

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 47 
02.02.02 As-Of-Order (004) Record 2 of 8 
Required 
Record 2 of 8 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Physical Sequence 
Number  
1 2 2 A/N  R 004 
Logical Sequence 
Number  
3 4 2 A/N 02  R 004 
Filler  5 7 3 A/N Space  R  
Share Quantity  8 21 14 N 9,999,999,999.9999 
Optional for record type 004 if full 
[[liquidation]]; 
Not allowed for record type 004 if 
Money Amount > 0  
RC 019 
Customer Account 
Number at Firm  
22 41 20 A/N Optional if [[settlement]] Override 
Reason Code = 04 or 06 OR if 
Membership Identifier is provided.  
RC 020 
Fund Account 
Indicator  
42 42 1 A/N 0 = New account–U.S. 
1 = New account–non-U.S. 
2 = Existing account–U.S. 
3 = Existing account–non-U.S. 
4 = New account–U.S. Tax Resident 
Living Abroad 
5 = Existing account–U.S. Tax 
Resident Living Abroad  
R 010 
Customer Account 
Number at Fund  
43 62 20 A/N Required for all non-networked 
liquidations 
(Network Control Ind = 0 and Trans 
Code = 03 or 04)  
OC 011 
[[Asset]] Type Indicator 
 
63 63 1 A/N 0 = Not applicable 
1 = Current year payment 
2 = Prior year payment 
3 = IRA rollover 
4 = [[Asset]] transfer 
5 = Employee—prior year 
6 = Employee—current year 
7 = Employer—prior year 
8 = Employer—current year 
9 = Non-fund prototype IRA 
R 013 

---

## Page 48

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 48 
Record 2 of 8 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
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
L = Omnibus [[Dividend]] 
Reconciliation 
M = Variable Annuity 
N = Wrap Program 
O = Defined Benefit Plan 
P = 529 Previous Year Contribution 
Q = 529 Rollover Contribution 
S = Omnibus Short-Term Capital 
Gain Reconciliation 
T = Omnibus Long-Term Capital 
Gain Reconciliation 
U = 529 In-State Plan Transfer 
Contribution 
V = 529 Owner Change 
W = 529 Beneficiary Change- 
In-Family 
Note: 
D, P, Q, U, V and W indicate Section 
529 Plan.  
Agent for Firm 
Number  
64 67 4 A/N Required if Originator Type = V 
(TPP). 
OC 271 
Network Control 
Indicator  
68 68 1 A/N 0 = Non-networked 
3 = Matrix level 3 
4 = Matrix level 4 
R 047 
Fraction Indicator  69 69 1 A/N 0 = Round up 
1 = Round down 
2 = Issue fraction 
R 014 

---

## Page 49

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 49 
Record 2 of 8 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
3 = Not applicable  
Gross [[settlement]] 
Indicator  
70 70 1 A/N 0 = Not applicable 
1 = Settle net 
2 = Settle gross  
R 094 
Transaction Received 
Time 
71 76 6 N hhmmss Eastern Time 
000000 (midnight) to 235959 
 
Required when “Money Market 
[[Liquidity]] Fee/Redemption Gate 
Indicator” = ‘F’ (Fund). 
 
Record Types 005 & 006: 
Must contain the same value as 
provided by the firm on the Order 
transaction (record type 001 or 004). 
[[NSCC]] will reject if a fund provided 
value is different from the value 
submitted by the firm.  
OC 168 
Membership Identifier  77 78 2 A/N 01 = Trust [[Member]] 
02 = Networking info required for 
TPA/Investment Agent 
03 = TPP (Third Party Provider) 
O 181 
Filler 79 79 1 A/N  R  
Transaction Payment 
Type Indicator  
80 80 1 A/N Required if [[settlement]] Override 
Reason Code = 04. 
1 = Shareholder wire 
2 = Shareholder ACH 
3 = Address of Record (AOR). 
3 allowed for [[liquidation]] (Transaction 
Code = 03 or 04) only  
OC 216 
Transaction Bank 
Account Number  
81 100 20 A/N Required if Transaction Payment 
Type Indicator = 1 or 2  
OC 142 
 
 
  

---

## Page 50

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 50 
02.02.03 As-Of-Order (004) Record 3 of 8 
Required 
Record 3 of 8 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number  
1 2 2 A/N  R 004 
Logical Sequence 
Number  
3 4 2 A/N 03  R 004 
Filler  5 7 3 A/N Space  R  
Money Amount  8 23 16 N 99,999,999,999,999.99 
Optional for record type 004 if full 
[[liquidation]]; 
Not allowed for record type 004 if 
Share Quantity > 0  
RC 019 
Currency Indicator  24 26 3 A/N  O 110 
Anticipated [[settlement]] 
Date  
27 34 8 A/N mmddccyy 
For Security Issue Type = 63, 
Required if [[settlement]] Override 
Reason Code is space 
 
For other Security Types: 
1. Required if [[settlement]] Override 
Reason Code is provided and is 
not 04 (x-[[settlement]] domestic). 
2. Not allowed if [[settlement]] 
Override Reason Code = 04. 
OC 180 
Branch Identification 
Number  
35 43 9 A/N Optional under the following 
conditions: 
• Membership Identifier = 01 or 02 
and Agent for Firm Number is not 
provided. 
• Originator Type = V(TPP) 
RC 035 
Related Trade 
Indicator  
44 44 1 A/N 0 = No 
1 = Yes  
R 065 
Related Trade 
Identifier  
45 46 2 A/N Required if 
Related Trade Indicator = 1  
OC 105 
Customer Name  47 66 20 A/N  R 063 

---

## Page 51

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 51 
Record 3 of 8 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
SSN/EIN Indicator  67 67 1 A/N 0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN  
R 102 
SSN/EIN Number  68 76 9 A/N  R 103 
[[liquidation]] Indicator  77 77 1 A/N Required if Trans Type = 5. 
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
D = 529 Plan Account—Beneficiary 
Disability 
E = 529 Plan Account–Beneficiary 
Death 
F = 529 Plan Account–Beneficiary 
Scholarship 
Notes: 
• 4 through F should apply only to 
transactions with CDSC Waivers 
• C through F should only apply to 
Section 529 plans. 
OC 046 

---

## Page 52

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 52 
Record 3 of 8 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
NAV Reason Code  78 78 1 A/N Required if Trans Type = 3. 
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
9 = Section 529 Account—Qualified 
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
79 80 2 A/N Required for Transaction Codes 
 
01 (Initial purchase) 
02 (Subsequent purchase) 
OC 012 

---

## Page 53

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 53 
Record 3 of 8 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Redemption Fee 
Indicator  
81 81 1 A/N 0 = Short-Term Redemption (STR) 
1 = STR with CDSC 
2 = Money Market [[Liquidity]] Fee 
3 = Money Market [[Liquidity]] Fee with 
CDSC 
 
Values “0” and “1” are not allowed for 
record types 005 and 006 if this field 
was blank on the original Order 
transaction (record type 001 or 004). 
 
Values “2” and “3” are allowed for 
record types 005 and 006 if this field 
was blank on the original Order 
transaction (record type 001 or 004). 
 
Not allowed for record types 007 and 
009. 
O 248 
Short-Term 
Redemption Fee 
Waiver Indicator  
82 82 1 A/N 1 = STR waiver due to correction 
2 = Death 
3 = Disability 
4 = Mandatory distribution 
5 = Systematic withdrawal 
6 = Defined contribution 
7 = Hardship 
8 = Auto Rebalance 
9 = DC–Termination Distribution 
A = DC–Involuntary Distribution 
B = DC–Forfeitures 
C = DC–Loans 
D = DC–Excess Contributions 
E = Wrap Program 
F = Fund of Funds 
G = Divorce/QDRO 
H = Plan fees QDRO 
O 249 
Filler 83 83 1 A/N Space R  

---

## Page 54

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 54 
Record 3 of 8 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
As-Of Indicator  84 84 1 A/N Required for record type 004. 
0 = Not applicable 
1 = Correction only 
2 = Correction 
3 = Rebill  
OC 108 
As-Of Reason Code  85 86 2 A/N Required for record type 004 
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
Note: 
The values ‘00’, ‘06’ and ‘08’ have 
been removed. 
OC 109 
Transaction ABA 
Routing Number  
87 95 9 A/N Required if 
Transaction Payment Type Indicator = 
1 or 2  
OC 141 
Filler  96 98 3 A/N Space  R  

---

## Page 55

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 55 
Record 3 of 8 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Omnibus Account 
Indicator  
99 99 1 A/N 0 = Not Omnibus Account 
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
100 100 1 A/N 0 = Trade Date not forwarded 
1 = Trade Date forwarded 
 
For record types 005 and 006: 
• Must be same as on original 
order 
• Trade Date forwarded is only 
allowed if: 
• Security Type = 48 
(Interval Fund) and 
Transaction Code = 03 
(Partial [[liquidation]]) or 
04 (Full [[liquidation]]). 
• Security Type = 62 or 63 
OC 229 
 
 
  

---

## Page 56

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 56 
02.02.04 As-Of-Order (004) Record 4 of 8 
Required if any of the following fields in this record are required: 
• Sales Charge Rate 
• Country of Origin (Record Type 004, 007 and 009) 
• IRA/529 [[liquidation]] Indicator 
• Periodic Frequency Indicator 
• Beneficiary SSN/EIN Number 
• Social Code (when “Transaction Code” = 01 & Record Type=004, 005 or 006) 
Record 4 of 8 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject Code 
Physical Sequence 
Number  
1 2 2 A/N  R 004 
Logical Sequence 
Number  
3 4 2 A/N 04  R 004 
Filler  5 7 3 A/N Space  R  
Related Account 
Number  
8 27 20 A/N  O  
Related Account 
Number Indicator  
28 28 1 A/N Required if Related Account Number 
is provided. 
1 = Fund 
2 = Firm 
3 = Customer  
OC 157 
Related Account 
Security Issue 
Country Code  
29 30 2 A/N Space. For future use  R  
Related Account 
Security Issue [[ID]]  
31 39 9 A/N Required if Related Account Number 
is provided  
OC 107 
Related Account 
Security Issue Check 
Digit  
40 40 1 A/N Space. For future use  R  
Country of Origin 
(Country Code)  
41 42 2 A/N Required for non-omnibus account 
(Omnibus Account Indicator = ‘0’ or 
space) 
if State of Sale (State Code) = ‘FF’  
OC 067 
Sales Charge Rate  43 46 4 N 9.999 
Must be provided (but allowed to be 
zero) for purchase (Transaction 
Code = '01', '02' or '07') if Load Type 
Indicator = 1.  
OC 025 

---

## Page 57

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 57 
Record 4 of 8 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject Code 
ROA/LOI Value  47 62 16 N 99,999,999,999,999.99  O 064 
LOI Number/Date  63 70 8 A/N  O  
IRA/529 [[liquidation]] 
Indicator 
71 71 1 A/N 0 = Not applicable 
1 = Distribution—premature 
2 = Distribution—disability 
3 = Distribution—death 
4 = Distribution—normal 
5 = Hardship withdrawal 
6 = Loan 
7 = Rollover 
8 = Adjust prior year excess 
9 = Adjust current year excess 
A = Qualified 
B = Non-Qualified 
C = Distribution–Non-Taxable 
D = 529 Owner Change 
E = 529 Beneficiary Change–In-
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
D or E is required if Transaction 
Type = F (529 Registration Change) 
OC 106 
Short [[settlement]] 
Indicator  
72 72 1 A/N 0 = Not applicable 
1 = Short due to correction  
O 169 

---

## Page 58

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 58 
Record 4 of 8 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject Code 
Periodic Frequency 
Indicator 
73 73 1 A/N Required if [[liquidation]] Indicator = 8 
or Program Transaction Indicator = 1
 
0 = Weekly 
1 = Monthly 
2 = Bi-monthly 
3 = Quarterly 
4 = Semiannual 
5 = Annual 
6 = Non-Periodic (ad Hoc) 
OC 083 
Shareholder Date of 
Birth  
74 81 8 N mmddccyy  O 204 
Social Code 82 83 2 A/N Required when: 
•  “Transaction Code” = 01–Initial 
Purchase AND 
• “Record type” is one of the 
following: 
o 004–As-of Order 
o 005–Confirmation 
o 006–Reconfirmation 
o  
See Social Code List at 
https://dtcclearning.com/documents/
mutual-fund-services-1/mfs-cross-
product/codes-8/2498-social-
codes/file.html under the Codes 
section. 
OC 128 
Beneficiary SSN/EIN 
Number  
84 92 9 A/N Required if [[Asset]] Type Indicator = 
D, E, Q, U, V, or W and Transaction 
Code = 01 or 02 
[[Asset]] Type Indicators 
D (529 Current Year Contribution) 
E (UGMA account transferred to 
Section 529 Account) 
P (529 Previous Year Contribution) 
Q (529 Rollover Contribution) 
U (529 In–State Plan Transfer 
Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change- 
In-Family) 
Transaction Codes 
01 (Initial purchase) 
02 (Subsequent purchase) 
OC 103 

---

## Page 59

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 59 
Record 4 of 8 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject Code 
Beneficiary SSN/EIN 
Indicator  
93 93 1 A/N Required if Beneficiary SSN/EIN 
Number is provided. 
0 = Tax [[ID]] number 
1 = Social security number 
2 = Beneficiary TIN/EIN  
OC 102 Standard [[ID]]  94 99 6 A/N  O  
Program Transaction 
Indicator 
100 100 1 A/N 1 = Systematic Withdrawal Plan 
(SWP) 
2 = Target Date Fund [[liquidation]] 
3 = Systematic Contribution 
(SIP/PAC/PIP) 
4 = Rebalance Purchase 
(Systematic) 
5 = Rebalance Redemption 
(Systematic) 
O 259 
 
 
  

---

## Page 60

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 60 
02.02.05 As-Of-Order (004) Record 5 of 8 
Optional 
Record 5 of 8 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Physical Sequence 
Number  
1 2 2 A/N  R 004 
Logical Sequence 
Number  
3 4 2 A/N 05  R 004 
Filler  5 7 3 A/N Space  R  
Account Representative 
Number  
8 16 9 A/N  O  
Account Representative 
Name  
17 31 15 A/N  O  
Confirm Number  32 43 12 A/N  O  
Memo Field  44 55 12 A/N  O  
IRA Withholding 
Percentage  
56 60 5 N 99.999  O 158 
Non-Taxable 
Percentage  
61 65 5 N 99.999  O 159 
Non-Taxable Money 
Amount  
66 81 16 N 99,999,999,999,999.99  O 160 
Closeout Fee Indicator  82 82 1 A/N 0 = [[DO]] not deduct 
1 = Deduct  
O 161 
LOI Indicator  83 83 1 A/N 0 = New 
1 = Existing  
O 162 
Original Control Number  84 98 15 A/N  O  
Original Correction 
Indicator  
99 99 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] 
correction/cancellation 
Space = No correction 
P not permitted if the Security 
Issue Type field value is 63 and 
[[settlement]] Override Reason Code 
field value is space. 
 
O 164 
Filler  100 100 1 A/N Space  R  
 

---

## Page 61

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 61 
02.02.06 As-Of-Order (004) Record 6 of 8 
Optional for record type 004 
Required for all other record types 
Record 6 of 8 
Field Name  
Start  End Len Type Description  Opt/ 
Req 
Reject Code 
Physical Sequence 
Number  
1 2 2 A/N  R 004 
Logical Sequence 
Number  
3 4 2 A/N 06  R 004 
Filler  5 7 3 A/N Space  R  
Withholding Amount  8 23 16 N 99,999,999,999,999.99  O 113 
Withholding Type  24 24 1 A/N Required if Withholding Amount > 
0. 
1 = Tefra backup 
2 = Tefra pension 
3 = Foreign withholding  
OC 114 
Fee Amount  25 32 8 N 999,999.99  O 115 
Fee Type  33 33 1 A/N Required if Fee Amount > 0. 
1 = [[liquidation]] fee 
2 = Other  
OC 116 
Amount Due  34 49 16 N 99,999,999,999,999.99 
Optional for record type 004. 
This amount will be settled by 
[[NSCC]]  
RC 026 
Price Per Share  50 61 12 N 999,999.999999 
Optional for record types 004  
RC 027 
Loss/Gain Amount  62 69 8 N 999,999.99  O 031 
Loss/Gain Indicator  70 70 1 A/N Required if Loss/Gain Amount > 0. 
0 = Loss 
1 = Gain  
OC 117 
Firm Concession  71 79 9 N 9,999,999.99  O 044 
Accrual Amount  80 95 16 N 99,999,999,999,999.99  O 111 

---

## Page 62

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 62 
Record 6 of 8 
Field Name  
Start  End Len Type Description  Opt/ 
Req 
Reject Code 
Accrual Indicator  96 96 1 A/N Required if Accrual Amount > 0. 
0 = Included in Amount Due 
1 = Paid via Cash Adjustment 
2 = Paid outside system  
OC 112 
Debit/Credit Indicator  97 98 2 A/N Required if Correction Indicator = 
P. 
Not allowed otherwise. 
DB = Debit firm 
CR = Credit firm 
[[NSCC]] will settle Amount Due 
according to this indicator rather 
than Transaction Code.  
OC 034 
Breakpoint Change 
Reason Code  
99 99 1 A/N 1 = ROA value at fund 
2 = LOI at fund 
3 = The higher of cost or market 
value at fund 
4 = Jumbo Pricing 
5 = Wrap Account 
6 = NAV Account 
7 = Amount Processed at NAV  
O 246 Load Type Indicator  100 100 1 A/N 0 = Other 
1 = Front-End Load 
Required (except for record type 
004) for purchase (Transaction 
Code = ‘01’, ‘02’ or ’07’).  
OC 247  
 
  

---

## Page 63

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 63 
02.02.07 As-Of-Order (004) Record 7 of 8 
Required when Redemption Fee Indicator is provided or [[Asset]] Type Indicator = Q, U, V, or W.  
Optional for all other [[Asset]] Types. 
Record 7 of 8 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 07 R 004 
Filler 5 7 3 A/N Space R  
Redemption Fee Rate 8 14 7 N 99.99999 
 
Not allowed if “Redemption Fee 
Indicator” is not provided. 
 
Required when “Redemption Fee 
Indicator” is populated with either ‘2’ 
(Money Market [[Liquidity]] Fee) or ‘3’ 
(Money Market [[Liquidity]] Fee with 
CDSC). 
Zero value is not allowed when this 
field is required and “Redemption 
Fee Indicator” = ‘2’ or ‘3’. 
 
If “Redemption Fee Indicator” = 0 or 
1, this field will be utilized to 
communicate a Short-Term 
Redemption (STR) Fee Rate. 
OC 250 

---

## Page 64

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 64 
Record 7 of 8 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
STR Fee Share 
Quantity  
15 28 14 N 9,999,999,999.9999 
 
For all record types: 
Not allowed if “Redemption Fee 
Indicator” is not provided. 
 
For record type 004: 
Required when “Redemption Fee 
Indicator” is provided and 
“Redemption Fee Money Amount” = 
0 or Space. 
Not allowed if “Redemption Fee 
Money Amount” > 0 
 
For record types 005 and 006: 
If zero or Space, and “Redemption 
Fee Indicator” is provided, will not 
override the “STR Fee Share 
Quantity” in the database. 
 
For all record types 
Not allowed when “Redemption Fee 
Indicator” is populated with either ‘2’ 
(Money Market [[Liquidity]] Fee) or ‘3’ 
(Money Market [[Liquidity]] Fee with 
CDSC). 
OC 251 

---

## Page 65

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 65 
Record 7 of 8 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Redemption Fee 
Money Amount  
29 44 16 N 99,999,999,999,999.99 
 
For all record types: 
Not allowed if “Redemption Fee 
Indicator” is not provided. 
Required when “Redemption Fee 
Indicator” is populated with either ‘2’ 
(Money Market [[Liquidity]] Fee) or ‘3’ 
(Money Market [[Liquidity]] Fee with 
CDSC). 
Zero value is not allowed when this 
field is required. 
 
For record type 004: 
Required when “Redemption Fee 
Indicator” is provided and “STR Fee 
Share Quantity” = 0 or Space. 
Not allowed if “STR Fee Share 
Quantity” > 0. 
 
For record types 005 and 006: 
Required when “Redemption Fee 
Indicator” is provided. 
 
For all record types: 
If “Redemption Fee Indicator” = 0 or 
1, this field will be utilized to 
communicate a Short-Term 
Redemption (STR) Fee Money 
Amount. 
OC 252 
Cost Basis Money 
Amount  
45 60 16 N Required if the [[Asset]] Type Indicator 
= Q U, V or W. 
Q (529 Rollover Contribution) 
U (529 In–State Plan Transfer 
Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change-In-
Family) 
Format: 
99,999,999,999,999.99 
Zeros are allowed 
OC 261 

---

## Page 66

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 66 
Record 7 of 8 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Earnings to Date 
Money Amount  
61 76 16 N Required if the [[Asset]] Type Indicator 
= Q, U, V or W. 
Q (529 Rollover Contribution) 
U (529 In–State Plan Transfer 
Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change-In-
Family) 
Format: 
99,999,999,999,999.99 
Zeros are allowed 
OC 262 
Negative Earnings to 
Date Indicator 
77 77 1 A/N N = Negative 
Spaces = Positive  
O 263 
Money Market 
[[Liquidity]] 
Fee/Redemption Gate 
Indicator  
78 78 1 A/N F = Fund. 
B = [[intermediary]] 
 
For Record Types 005 & 006: Must 
contain the same value as provided 
on the Order transaction (record 
type 001 or 004). [[NSCC]] will reject if 
a fund provided value is different 
from the value submitted by the firm. 
 
Not allowed for record types 007 and 
009. 
O 282 
Transaction Received 
Date  
79 86 8 A/N mmddccyy 
Required if the “Money Market 
[[Liquidity]] Fee/Redemption Gate 
Indicator” = “F”. 
 
For Record Types 005 & 006: Must 
contain the same value as provided 
on the Order transaction (record 
type 001 or 004). [[NSCC]] will reject if 
a fund provided value is different 
from the value submitted by the firm. 
 
Not allowed for record types 007 and 
009. 
OC 283 

---

## Page 67

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 67 
Record 7 of 8 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Aggregated Order 
Indicator  
87 87 1 A/N Required if the “Money Market 
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
 
For Record Types 005 & 006 Must 
contain the same value as provided 
on the Order transaction (record 
type 001 or 004). [[NSCC]] will reject if 
a fund provided value is different 
from the value submitted by the firm. 
 
Not allowed for record types 007 and 
009.  
OC 284 
Filler 88 100 13 A/N  R  
 
 
  

---

## Page 68

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 68 
02.02.08 As-Of-Order (004) Record 8 of 8 
Optional 
Record 8 of 8 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 08 R 004 
Filler 5 7 3 A/N Space R  
[[intermediary]] Program 
Indicator–1 
8 11 4 A/N Indicates the program, platform, or 
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
Indicator–2 
12 15 4 A/N Further defines the program, platform, 
or channel applicable to an account. 
Values are uniquely defined by each 
[[intermediary]].  
O  
Servicing Group [[ID]] 16 24 9 A/N This field is used to communicate 
aggregated servicing relationships or 
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
[[ID]]–1 
25 44 20 A/N This field is used to communicate 
additional relationship details to 
further define servicing relationships 
between accounts. 
Values are uniquely defined by each 
[[intermediary]].  
O  

---

## Page 69

Fixed Length Record Layouts (Part 1) 
As-Of Order (004); Confirmation (005); Reconfirmation (006); Fund Originated Order (007); Fund Originated As-Of Order (009); Post [[settlement]] Cancellation by Fund 
(140) 69 
Record 8 of 8 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Additional Relationship 
[[ID]]–2 
45 64 20 A/N This field is used to communicate 
additional relationship details to 
further define servicing relationships 
between accounts. 
Values are uniquely defined by each 
[[intermediary]].  
O  
Filler 65 100 36 A/N Space R  

---

## Page 70

Fixed Length Record Layouts (Part 1) 
Extended Correction Transfer (200); Extended Correction Transfer Acknowledgment (201) 70 
EXTENDED CORRECTION TRANSFER (200); EXTENDED 
CORRECTION TRANSFER ACKNOWLEDGMENT (201) 
02.03.01 Extended Correction Transfer (200) Record 1 of 3 
Required 
Record 1 of 3 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 01 R 004 
Originator Type 5 5 1 A/N A = Investment Agent  
B = Firm 
F = Fund 
T = TPA 
V = TPP (Third Party Provider) 
R 187 
Filler 6 7 2 A/N Space R  
Firm Number 8 11 4 N  R 008 
Filler 12 14 3 A/N Space R  
Record Type 15 17 3 A/N 200 = Extended Correction Transfer 
201 = Extended Correction Transfer 
Acknowledgment 
R 002 
Test Indicator 18 18 1 A/N 0 = Production 
1 = Test 
R 122 
Filler 19 19 1 A/N Space R  
Fund Number 20 23 4 N  O 100 
Filler 24 26 3 A/N Space R  
Security Issue 
Country Code 
27 28 2 A/N Space. For future use R  
Security Issue [[ID]] 29 37 9 A/N  R 007 
Security Issue Check 
Digit 
38 38 1 A/N Space. For future use R  

---

## Page 71

Fixed Length Record Layouts (Part 1) 
Extended Correction Transfer (200); Extended Correction Transfer Acknowledgment (201) 71 
Record 1 of 3 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Security Issue Type 39 40 2 A/N Required if 24 (Money Market) 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value 
against the Fund/SERV Security 
master file. [[NSCC]] leverages the 
Fund/SERV Security master file to 
determine value and associated 
processing rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 
OC 150 
Control Number 41 55 15 A/N  R 005 
Filler 56 56 1 A/N Space R  
Transaction Type 57 57 1 A/N 1 = Transfer to new account 
2 = Transfer to existing account 
R 017 
Extended Correction 
Reason Code 
58 59 2 A/N 01 = Incorrect Firm/Fund Account 
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
11 = Resubmitted Fund/SERV 
Reject 
12 = DCC&S (see [[Asset]] Type 
Indicator) 
13 = Distribution Reversal 
14 = Prospectus Violation 
Note: 
The values ‘06’ and ‘08’ have been 
removed. 
R 109 

---

## Page 72

Fixed Length Record Layouts (Part 1) 
Extended Correction Transfer (200); Extended Correction Transfer Acknowledgment (201) 72 
Record 1 of 3 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Submission Date 60 67 8 N mmddccyy R 101 
Original Trade Date  68 75 8 N mmddccyy R 016 
Book/Physical Share 
Indicator 
76 76 1 A/N 1 = Transfer book [[shares]] to book 
[[shares]] 
2 = Transfer book [[shares]] to physical 
[[shares]] 
R 015 
PI Delivery Indicator 77 77 1 A/N Required for all purchases if 
Book/Physical Share Ind = 2. 
0 = Deliver to customer 
1 = Deliver to firm 
2 = Deliver to agent for firm 
OC 039 Filler 78 80 3 A/N Space R  
[[NSCC]] Rejection 
Indicator 
81 81 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], multiple 
errors 
R  
[[NSCC]] Reject Code 82 84 3 A/N Input: Space 
Output: Reject code 
R  
TPA/Investment 
Agent/TPP Number 
85 88 4 A/N Required if: 
Originator Type = (T or A or V) 
OR 
Membership Identifier = 02 or 03. 
OC 188 
Filler 89 100 12 A/N Space R  
 
 
  

---

## Page 73

Fixed Length Record Layouts (Part 1) 
Extended Correction Transfer (200); Extended Correction Transfer Acknowledgment (201) 73 
02.03.02 Extended Correction Transfer (200) Record 2 of 3 
Required 
Record 2 of 3 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 02 R 004 
Filler 5 7 3 A/N Space R  
Original Share 
Quantity 
8 21 14 N 9,999,999,999.9999 R 019 
Debit Account 
Number 
22 41 20 A/N  R 118 
Debit Account 
Indicator 
42 42 1 A/N 1 = Fund 
2 = Firm 
R 119 
Credit Account 
Number 
43 62 20 A/N Required for transfer to existing 
account  
OC 120 
Credit Account 
Indicator 
63 63 1 A/N Required if Credit Account Number 
is provided. 
1 = Fund 
2 = Firm 
OC 121 
Agent for Firm 
Number  
64 67 4 A/N Required if Originator Type = V 
(TPP). 
OC 271 
Network Control 
Indicator  
68 68 1 A/N 0 = Non-networked 
3 = Matrix level 3 
4 = Matrix level 4 
R 047 
Fraction Indicator 69 69 1 A/N 1 = Transfer fraction 
2 = [[liquidation]] fraction  
R 014 
Filler 70 76 7 A/N Space R  
Membership Identifier 77 78 2 A/N 01 = Trust [[Member]] 
02 = Networking info required for 
TPA/Investment Agent 
03 = TPP (Third Party Provider) 
O 181 
Filler 79 100 22 A/N Space R  
 
 

---

## Page 74

Fixed Length Record Layouts (Part 1) 
Extended Correction Transfer (200); Extended Correction Transfer Acknowledgment (201) 74 
02.03.03 Extended Correction Transfer (200) Record 3 of 3 
Required 
Record 3 of 3 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Physical Sequence 
Number  
1 2 2 A/N  R 004 
Logical Sequence 
Number  
3 4 2 A/N 03 R 004 
Filler 5 7 3 A/N Space R  
Original Control 
Number  
8 22 15 A/N Required if Confirm Number is not 
provided  
OC 163 
Original Correction 
Indicator  
23 23 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] 
correction/cancellation 
Space = No correction  
O 164 
Confirm Number  24 35 12 A/N  O  
Filler 36 100 65 A/N Space R  

---

## Page 75

Fixed Length Record Layouts (Part 1) 
Order Acknowledgment for Money Market Purchase (101); Firm Delete (102); Release to [[settlement]] (109); Registration Acknowledgment (112); Delete Pending 
Registration (Registered Ex-Fund/SERV) (113); Receiving Fund Exit from ToRA (214) 75 
ORDER ACKNOWLEDGMENT FOR MONEY MARKET 
PURCHASE (101); FIRM DELETE (102); RELEASE TO 
[[settlement]] (109); REGISTRATION 
ACKNOWLEDGMENT (112); DELETE PENDING 
REGISTRATION (REGISTERED EX-FUND/SERV) (113); 
RECEIVING FUND EXIT FROM TORA (214) 
02.04.01 Order Acknowledgement for Money Market Purchase (101) 
Record 1 of 2 
Required 
Record 1 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 01 R 004 
Originator Type 5 5 1 A/N A = Investment Agent  
B = Firm 
F = Fund 
T = TPA 
V = Third Party Provider (TPP) 
R 187 
Filler 6 7 2 A/N Space R  
Firm Number 8 11 4 N  R 008 
Filler 12 14 3 A/N Space R  
Record Type 15 17 3 A/N 101 = Order Acknowledgment for 
Money Market Purchase 
102 = Firm Delete 
109 = Release to [[settlement]] 
112 = Registration Acknowledgment 
113 = Delete Pending Registration 
(registered ex-Fund/SERV) 
214 = Receiving Fund Exit from 
ToRA 
R 002 

---

## Page 76

Fixed Length Record Layouts (Part 1) 
Order Acknowledgment for Money Market Purchase (101); Firm Delete (102); Release to [[settlement]] (109); Registration Acknowledgment (112); Delete Pending 
Registration (Registered Ex-Fund/SERV) (113); Receiving Fund Exit from ToRA (214) 76 
Record 1 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Test Indicator 18 18 1 A/N 0 = Production 
1 = Test 
R 122 
Filler 19 19 1 A/N Space R  
Fund Number 20 23 4 N  O 100 
Filler 24 26 3 A/N Space R  
Security Issue 
Country Code 
27 28 2 A/N Space. For future use R  
Security Issue [[ID]] 29 37 9 A/N  R 007 
Security Issue Check 
Digit 
38 38 1 A/N Space. For future use R  
Security Issue Type 39 40 2 A/N Required if 24 (Money Market) 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value 
against the Fund/SERV Security 
master file. [[NSCC]] leverages the 
Fund/SERV Security master file to 
determine value and associated 
processing rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 
OC 150 
Control Number 41 55 15 A/N  R 005 
Correction Indicator 56 56 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] 
correction/cancellation 
Space = No correction 
RC 006 
Filler 57 59 3 A/N Space R  
Submission Date 60 67 8 N mmddccyy R 101 
Certificate Date 68 75 8 N mmddccyy 
Required for record types 112 and 
113 when last trade update reflects 
physical [[shares]] (Book/Physical 
Share Ind = 2 or 3). 
Not allowed for other record types 
OC 037 Filler 76 76 1 A/N Space R  

---

## Page 77

Fixed Length Record Layouts (Part 1) 
Order Acknowledgment for Money Market Purchase (101); Firm Delete (102); Release to [[settlement]] (109); Registration Acknowledgment (112); Delete Pending 
Registration (Registered Ex-Fund/SERV) (113); Receiving Fund Exit from ToRA (214) 77 
Record 1 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
PI Delivery Indicator 77 77 1 A/N Required for record types 112 and 
113 when last trade update reflects 
physical [[shares]] (Book/Physical 
Share Ind = 2 or 3). 
Not allowed for other record types. 
0 = Deliver to customer 
1 = Deliver to firm 
2 = Deliver to agent for firm 
OC 039 
Filler 78 80 3 A/N Space R  
[[NSCC]] Rejection 
Indicator 
81 81 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], multiple 
errors 
R  
[[NSCC]] Reject Code 82 84 3 A/N Input: Space 
Output: Reject code 
R  
TPA/Investment 
Agent/TPP Number 
85 88 4 A/N Required if Originator Type = T or A 
or V 
OC 188 
Service Provider 
Number 
89 92 4 A/N  O 215 
Filler 93 100 8 A/N Space R  
 
 
  

---

## Page 78

Fixed Length Record Layouts (Part 1) 
Order Acknowledgment for Money Market Purchase (101); Firm Delete (102); Release to [[settlement]] (109); Registration Acknowledgment (112); Delete Pending 
Registration (Registered Ex-Fund/SERV) (113); Receiving Fund Exit from ToRA (214) 78 
02.04.02 Order Acknowledgement for Money Market Purchase (101) 
Record 2 of 2 
Required for Record Types 101, 109, 112 and 113. Also required for Record Type 102 if Originator Type 
= V 
Record 2 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 02 R 004 
Filler 5 7 3 A/N Space R  
Certificate Number 8 17 10 A/N Required for record types 112 and 
113 when last trade update reflects 
physical [[shares]] (Book/Physical 
Share Ind = 2 or 3). 
Not allowed for other record types 
OC 138 
Filler 18 42 25 A/N Space R  
Customer Account 
Number 
43 62 20 A/N Required for record types 101, 109, 
112 and 113 
OC 111 
Customer Account 
Number Indicator 
63 63 1 A/N Required if Customer Account 
Number is provided. 
1 = Fund 
2 = Firm 
OC 048 
Agent for Firm 
Number 
64 67 4 A/N Required if Originator Type = V 
(TPP). 
OC 271 
Network Control 
Indicator  
68 68 1 A/N Required for record types 101, 109, 
112 and 113. 
0 = Non-networked 
3 = Matrix level 3 
4 = Matrix level 4 
OC 047 Filler 69 70 2 A/N Space R  
Transaction Received 
Time 
71 76 6 N hhmmss Eastern Time 
Ignored for any record type other 
than 101. 
000000 (midnight) to 235959 
O 168 

---

## Page 79

Fixed Length Record Layouts (Part 1) 
Order Acknowledgment for Money Market Purchase (101); Firm Delete (102); Release to [[settlement]] (109); Registration Acknowledgment (112); Delete Pending 
Registration (Registered Ex-Fund/SERV) (113); Receiving Fund Exit from ToRA (214) 79 
Record 2 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Fund Reject Code  77 79 3 A/N Allowed only Record Type 214 with 
the following values: 
710–Minimum purchase amount not 
met at Receiving Fund 
711–Maximum purchase amount 
exceeded at Receiving Fund 
Not allowed for all other record 
types. 
O 264 
Filler 80 100 22 A/N Space R  

---

## Page 80

Fixed Length Record Layouts (Part 1) 
Fund Reject (100); Fund Delete (108); Registration Rejection (114); Delete Pending Release to [[settlement]] (Settled Ex-Fund/SERV) (129) 80 
FUND REJECT (100); FUND DELETE (108); 
REGISTRATION REJECTION (114); DELETE PENDING 
RELEASE TO [[settlement]] (SETTLED EX-FUND/SERV) 
(129) 
02.05.01 Fund Reject (100) Record 1 of 2 
Required. 
When ToRA related (ToRA Indicator = ‘1’ or ‘2’), Firm means Receiving Fund, and Fund means 
Delivering Fund. 
Record 1 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 01 R 004 
Originator Type 5 5 1 A/N F = Fund R 187 
Filler 6 7 2 A/N Space R  
Firm Number 8 11 4 N  R 008 
Filler 12 14 3 A/N Space R  
Record Type 15 17 3 A/N 100 = Fund Reject 
108 = Fund Delete 
114 = Registration Rejection 
129 = Delete Pending Release to 
[[settlement]] (settled ex-Fund/SERV) 
R 002 
Test Indicator 18 18 1 A/N 0 = Production 
1 = Test 
R 122 
Filler 19 19 1 A/N Space R  
Fund Number 20 23 4 N  O 100 
Filler 24 26 3 A/N Space R  
Security Issue 
Country Code 
27 28 2 A/N Space. For future use R  
Security Issue [[ID]] 29 37 9 A/N  R 007 
Security Issue Check 
Digit 
38 38 1 A/N Space. For future use R  

---

## Page 81

Fixed Length Record Layouts (Part 1) 
Fund Reject (100); Fund Delete (108); Registration Rejection (114); Delete Pending Release to [[settlement]] (Settled Ex-Fund/SERV) (129) 81 
Record 1 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Security Issue Type 39 40 2 A/N Required if 24 (Money Market) 
except if ToRA Indicator = 1 or 2. 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value 
against the Fund/SERV Security 
master file. [[NSCC]] leverages the 
Fund/SERV Security master file to 
determine value and associated 
processing rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 
OC 150 
Control Number 41 55 15 A/N  R 005 
Correction Indicator 56 56 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] 
correction/cancellation 
Space = No correction 
R 006 
Filler 57 59 3 A/N Space R  
Submission Date 60 67 8 N mmddccyy R 101 
ToRA (Transfer of 
Retirement [[Asset]]) 
Indicator 
68 68 1 A/N 1 = ToRA related (submitted by the 
receiving fund) 
2 = ToRA related (submitted by the 
delivering fund) 
Space = Not ToRA related 
R 186 
Filler 69 71 3 A/N Space R  
Fund Reject Indicator 72 72 1 A/N 1 = Single error 
2 = Multiples errors 
R 153 
Fund Reject Code 73 75 3 A/N  R 022 
Filler 76 80 5 A/N Space R  
[[NSCC]] Rejection 
Indicator 
81 81 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], multiple 
errors 
R  

---

## Page 82

Fixed Length Record Layouts (Part 1) 
Fund Reject (100); Fund Delete (108); Registration Rejection (114); Delete Pending Release to [[settlement]] (Settled Ex-Fund/SERV) (129) 82 
Record 1 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
[[NSCC]] Reject Code 82 84 3 A/N Input: Space 
Output: Reject code 
R  
TPA/Investment 
Agent/TPP Number 
85 88 4 A/N  O 188 
Service Provider 
Number 
89 92 4 A/N  O 215 
Filler 93 100 8 A/N Space R  
 
 
  

---

## Page 83

Fixed Length Record Layouts (Part 1) 
Fund Reject (100); Fund Delete (108); Registration Rejection (114); Delete Pending Release to [[settlement]] (Settled Ex-Fund/SERV) (129) 83 
02.05.02 Fund Reject (100) Record 2 of 2 
Required if Fund Rejection Indicator = 2 or Fund Reject Code = “704” (Fund Reject Record “100” only). 
When ToRA related (ToRA Indicator = ‘1’ or ‘2’), Firm means Receiving Fund, and Fund means 
Delivering Fund. 
Record 2 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 02 R 004 
Filler 5 7 3 A/N Space R  
Fund Reject Code 2 8 10 3 A/N Required if Fund Rejection Indicator 
= 2 
OC 022 
Fund Reject Code 3 11 13 3 A/N  O 022 
Fund Reject Code 4 14 16 3 A/N  O 022 
Fund Reject Code 5 17 19 3 A/N  O 022 
Fund Reject Code 6 20 22 3 A/N  O 022 
Fund Reject Code 7 23 25 3 A/N  O 022 
Fund Reject Code 8 26 28 3 A/N  O 022 
Fund Reject Code 9 29 31 3 A/N  O 022 

---

## Page 84

Fixed Length Record Layouts (Part 1) 
Fund Reject (100); Fund Delete (108); Registration Rejection (114); Delete Pending Release to [[settlement]] (Settled Ex-Fund/SERV) (129) 84 
Record 2 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Delivering Fund Plan 
Type 
32 32 1 A/N Required if the Fund Reject Code = 
“704” 
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
C = Inherited Roth Conversion IRA 
D = Account Type Is Not ToRA 
Eligible 
OC 265 
Filler 33 100 68 A/N Space R  

---

## Page 85

Fixed Length Record Layouts (Part 1) 
Exchange Order (015) 85 
EXCHANGE ORDER (015) 
02.06.01 Exchange Order (015) Record 1 of 5 
Required 
Record 1 of 5 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 01 R 004 
Originator Type 5 5 1 A/N A = Investment Agent 
B = Firm 
T = TPA 
S = Service Provider for B = Firm 
P = Service Provider for T = TPA 
V = TPP (Third Party Provider) 
R 187 
Filler 6 7 2 A/N Space R  
Firm Number 8 11 4 N  R 008 
Filler 12 14 3 A/N Space R  
Record Type 15 17 3 A/N 015 = Exchange Order 
Not permitted if the Security Issue 
Type field value is 63 and 
[[settlement]] Override Reason Code 
field value is space 
RC 002/275 
Test Indicator 18 18 1 A/N 0 = Production 
1 = Test 
R 122 
Filler 19 19 1 A/N Space R  
Fund Number 20 23 4 N  O 100 
Filler 24 26 3 A/N Space R  
Security Issue 
Country Code (Exch 
From) 
27 28 2 A/N Space. For future use R  
Security Issue [[ID]] 
(Exch From) 
29 37 9 A/N  R 007 
Security Issue Check 
Digit (Exch From) 
38 38 1 A/N Space. For future use R  

---

## Page 86

Fixed Length Record Layouts (Part 1) 
Exchange Order (015) 86 
Record 1 of 5 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Security Issue Type 
(Exch From) 
39 40 2 A/N Required if 24 (Money Market) 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value 
against the Fund/SERV Security 
master file. [[NSCC]] leverages the 
Fund/SERV Security master file to 
determine value and associated 
processing rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 
OC 150 
Control Number 41 55 15 A/N  R 005 
Filler 56 56 1 A/N Space R  
Transaction Type  57 57 1 A/N 6 = Exchange to new account 
7 = Exchange to existing account 
C = Voluntary Cross Class 
Exchange to new account 
D = Voluntary Cross Class 
Exchange to existing account 
R 017 
Transaction Code 58 59 2 A/N 05 = Full exchange 
06 = Partial exchange 
R 018 
Submission Date 60 67 8 N mmddccyy R 101 
Trade Date 68 75 8 N mmddccyy R 016 
Book/Physical Share 
Indicator 
76 76 1 A/N 1 = Exchange from book [[shares]] to 
book [[shares]] 
2 = Exchange from book [[shares]] to 
physical [[shares]] 
R 015 
PI Delivery Indicator 77 77 1 A/N Required if Book/Physical Share 
Indicator = 2. 
0 = Deliver to customer 
1 = Deliver to firm 
2 = Deliver to agent for firm 
OC 039 
Filler 78 78 1 A/N Space R  

---

## Page 87

Fixed Length Record Layouts (Part 1) 
Exchange Order (015) 87 
Record 1 of 5 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
[[settlement]] Override 
Reason Code 
79 80 2 A/N Required (but must not be 04) if 
Anticipated [[settlement]] Date is 
provided. 
01 = Wrap fee account 
02 = 401K 
03 = Other 
04 = X-[[settlement]] 
05 = Section 529 Account—
Qualified State Tuition Program 
06 = X-[[settlement]] offshore 
enhanced (allowed for Security Type 
62 and 63 only) 
OC 179 
[[NSCC]] Rejection 
Indicator 
81 81 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], multiple 
errors 
R  
[[NSCC]] Reject Code 82 84 3 A/N Input: Space 
Output: Reject code 
R  
TPA/Investment 
Agent/TPP Number 
85 88 4 A/N Required if: 
Originator Type = (T or P or A or V) 
OR 
Membership Identifier = 02 or 03. 
OC 188 
Service Provider 
Number 
89 92 4 A/N Required if Originator Type = S or P OC 215 
SSN/EIN Start 
Sequence Number 
93 94 2 A/N See SSN/EIN Start Sequence 
Number in the Introduction section. 
Required if SSN/EIN Suffix is 
provided. Not allowed otherwise.  
OC 257 
Total SSN/EIN 
Records 
95 96 2 N Required if SSN/EIN Suffix is 
provided. Not allowed otherwise.  
OC 258 
Filler 97 100 4 A/N Space R  
 
 
  

---

## Page 88

Fixed Length Record Layouts (Part 1) 
Exchange Order (015) 88 
02.06.02 Exchange Order (015) Record 2 of 5 
Required 
Record 2 of 5 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 02 R 004 
Filler 5 7 3 A/N Space R  
Exch From Share 
Quantity 
8 21 14 N 9,999,999,999.9999 
Required if Transaction Code = 06 
and Exch From Money Amount = 0 
OC 019 
Customer Account 
Number at Firm 
22 41 20 A/N Optional if [[settlement]] Override 
Reason Code = 04 or 06 or if 
Membership Identifier is provided. 
RC 020 
New Registration 
Indicator 
42 42 1 A/N 0 = No registration required 
1 = Registration required for 
Exchange To 
R 040 
Exch From Account 
Number at Fund 
43 62 20 A/N Required if Network Control Ind (for 
From Account) = 0 
OC 011 
Filler 63 63 1 A/N Space R  
Agent for Firm 
Number 
64 67 4 A/N Required if Originator Type = V 
(TPP). 
OC 271 
Network Control 
Indicator (for the From 
Account)  
68 68 1 A/N 0 = Non-networked 
3 = Matrix level 3 
4 = Matrix level 4 
R 047 
Fraction Indicator 69 69 1 A/N 1 = Issue fraction 
2 = [[liquidation]] fraction 
R 014 
Filler 70 70 1 A/N Space R  
Transaction Received 
Time 
(renamed from 
“[[participant]] 
Processing Time”) 
71 76 6 N hhmmss Eastern Time 
000000 (midnight) to 235959 
 
Required when “Money Market 
[[Liquidity]] Fee/Redemption Gate 
Indicator” = ‘F’ (Fund). 
OC 168 

---

## Page 89

Fixed Length Record Layouts (Part 1) 
Exchange Order (015) 89 
Record 2 of 5 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Membership Identifier 77 78 2 A/N 01 = Trust [[Member]] 
02 = Networking info required for 
TPA/Investment Agent 
03 = TPP (Third Party Provider) 
O 181 
Filler 79 100 21 A/N Space R  
 
 
  

---

## Page 90

Fixed Length Record Layouts (Part 1) 
Exchange Order (015) 90 
02.06.03 Exchange Order (015) Record 3 of 5 
Required. 
Record 3 of 5 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 03 R 004 
Filler 5 7 3 A/N Space R  
Exch From Money 
Amount 
8 23 16 N 99,999,999,999,999.99 
Required if Transaction Code = 06 
and Exch From Share Quantity = 0 
OC 019 
Exch From Currency 
Indicator 
24 26 3 A/N  O 110 
Anticipated [[settlement]] 
Date 
27 34 8 A/N mmddccyy 
Required if [[settlement]] Override 
Reason Code is provided and is not 
04 or 06 (x-[[settlement]]). 
Not allowed if [[settlement]] Override 
Reason Code = 04. 
OC 180 
Branch Identification 
Number 
35 43 9 A/N Optional under the following 
conditions: 
Membership Identifier = 01 or 02 and 
Agent for Firm Number is not 
provided 
Originator Type = V (TPP) 
RC 035 
Related Trade 
Indicator 
44 44 1 A/N 0 = No 
1 = Yes 
R 065 
Related Trade 
Identifier 
45 46 2 A/N Required if Related Trade Indicator = 
1 
OC 105 
Customer Name 47 66 20 A/N  R 063 
Exch From Sales 
Charge Rate 
67 70 4 N 9.999 O 025 
As-Of Indicator 71 71 1 A/N 0 = Regular Exchange 
1 = As-Of Exchange 
O 021 
Discount Type 72 72 1 A/N 1 = Letter of intent 
2 = Rights of accumulation 
3 = Net [[Asset]] value 
O 208 

---

## Page 91

Fixed Length Record Layouts (Part 1) 
Exchange Order (015) 91 
Record 3 of 5 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Filler 73 77 5 A/N Space R  
NAV Reason Code  78 78 1 A/N Required if Discount Type = 3. 
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
9 = Section 529 Account—Qualified 
State Tuition Program 
A = [[Dividend]] reinvestment trade 
B = Trust Company NAV per 
Agreement 
D = Deminimis Amount Processed at 
NAV 
E = Self Directed Brokerage Account 
OC 104 
As-Of Reason Code  79 80 2 A/N Required if As-Of Indicator = 1 
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

## Page 92

Fixed Length Record Layouts (Part 1) 
Exchange Order (015) 92 
Record 3 of 5 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Redemption Fee 
Indicator  
81 81 1 A/N 0 = Short-Term Redemption (STR) 
1 = STR with CDSC 
2 = Money Market [[Liquidity]] Fee 
3 = Money Market [[Liquidity]] Fee with 
CDSC 
O 248 
Short-Term 
Redemption Fee 
Waiver Indicator  
82 82 1 A/N 1 = STR waiver due to correction 
2 = Death 
3 = Disability 
4 = Mandatory distribution 
5 = Systematic withdrawal 
6 = Defined contribution 
7 = Hardship 
8 = Auto Rebalance 
9 = DC–Termination Distribution 
A = DC–Involuntary Distribution 
B = DC–Forfeitures 
C = DC–Loans 
D = DC–Excess Contributions 
E = Wrap Program 
F = Fund of Funds 
G = Divorce/QDRO 
H = Plan fees QDRO 
O 249 
Filler 83 99 17 A/N Space R  
Trade Date Forward 
Indicator 
100 100 1 A/N 0 = Trade Date not forwarded 
1 = Trade Date forwarded 
Must be 1 if Trade Date is later than 
Submission Date. 
 
Trade Date forwarded is only allowed 
if Security Type = 62 or 63. 
OC 229 
 
 
  

---

## Page 93

Fixed Length Record Layouts (Part 1) 
Exchange Order (015) 93 
02.06.04 Exchange Order (015) Record 4 of 5 
Required 
Record 4 of 5 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 04 R 004 
Filler 5 7 3 A/N Space R  
02.01.07Security 
Issue Country Code 
(Exch To) 
8 9 2 A/N Space. For future use R  
Security Issue [[ID]] 
(Exch To) 
10 18 9 A/N  R 041 
Security Issue Check 
Digit (Exch To) 
19 19 1 A/N Space. For future use R  
Security Issue Type 
(Exch To) 
20 21 2 A/N Required if 24 (Money Market) 
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
Exchange To Account 
Number  
22 41 20 A/N Required if Transaction Type = 7 
(Exchange to existing account 
number) or 
D (Voluntary Cross Class Exchange 
to existing account number) 
OC 011 
Exch To Account 
Number Indicator 
42 42 1 A/N Required if Exch To Account Number 
is provided. 
1 = Fund 
2 = Firm 
OC 048 
Network Control 
Indicator (for the To 
Account) 
43 43 1 A/N 0 = Non-networked 
3 = Matrix level 3 
4 = Matrix level 4 
R 047 

---

## Page 94

Fixed Length Record Layouts (Part 1) 
Exchange Order (015) 94 
Record 4 of 5 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Exch To Sales Charge 
Rate 
44 47 4 N 9.999 O 025 
ROA/LOI Value 48 63 16 N 99,999,999,999,999.99 O 064 
LOI Number/Date 64 71 8 A/N  O  
State of Sale 
(State Code)  
72 73 2 A/N Required for all exchanges R 012 
Money Market 
[[Liquidity]] 
Fee/Redemption Gate 
Indicator  
74 74 1 A/N F = Fund. 
B = [[intermediary]] 
O 282 
Transaction Received 
Date  
75 82 8 A/N mmddccyy 
 
Required if the “Money Market 
[[Liquidity]] Fee/Redemption Gate 
Indicator” = F. 
OC 283 Aggregated Order 
Indicator  
83 83 1 A/N Required if the “Money Market 
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
OC 284 
Filler 84 93 10 A/N Space R  
Standard [[ID]] 94 99 6 A/N  O  
Program Transaction 
Indicator 
100 100 1 A/N 1 = Systematic Exchange O 259 
 
 
  

---

## Page 95

Fixed Length Record Layouts (Part 1) 
Exchange Order (015) 95 
02.06.05 Exchange Order (015) Record 5 of 5 
Required when Redemption Fee Indicator is provided. 
Record 5 of 5 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 04 R 004 
Filler 5 7 3 A/N Space R  
Account 
Representative 
Number 
8 16 9 A/N  O  
Account 
Representative Name 
17 31 15 A/N  O  
Confirm Number 32 43 12 A/N  O  
Memo Field 44 63 20 A/N  O  
Redemption Fee Rate 64 70 7 N 99.99999 
 
Not allowed if “Redemption Fee 
Indicator” is not provided. 
 
Required when “Redemption Fee 
Indicator” is populated with either ‘2’ 
(Money Market [[Liquidity]] Fee) or ‘3’ 
(Money Market [[Liquidity]] Fee with 
CDSC). 
Zero value is not allowed when this 
field is required, and “Redemption 
Fee Indicator” is = ‘2” or ‘3’. 
 
If “Redemption Fee Indicator” = 0 or 
1, this field will be utilized to 
communicate a Short-Term 
Redemption (STR) Fee Rate. 
OC 250 

---

## Page 96

Fixed Length Record Layouts (Part 1) 
Exchange Order (015) 96 
Record 5 of 5 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
STR Fee Share 
Quantity  
71 84 14 N 9,999,999,999.9999 
Required when “Redemption Fee 
Indicator” is provided and 
“Redemption Fee Money Amount” = 
0 or Space. 
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
Redemption Fee 
Money Amount  
85 100 16 N 99,999,999,999,999.99 
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
 
If “Redemption Fee Indicator” =0 or 
1, this field will be utilized to 
communicate a Short-Term 
Redemption (STR) Fee Money 
Amount. 
OC 252 
 
 

---

## Page 97

Fixed Length Record Layouts (Part 1) 
APPENDIX – SUMMARY OF CHANGES 97 
APPENDIX – SUMMARY OF CHANGES 
The following Summary of Changes are listed in chronological order, starting with the most recent changes. 

---

## Page 98

Fixed Length Record Layouts (Part 1) 
Summary of Changes – effective Q2  05/15/2023 98 
SUMMARY OF CHANGES – EFFECTIVE Q2  05/15/2023 
1. New Data Field in Existing Record Sequence 
New Data Field  Location  Record Type Section  
IRS 529 Annual Strategy 
Change Counter 
record 9, start 77, end 77, 
length 1 
ACATS Transfer (018)  Section 02.11.09 
record 3, start 25, end 25, 
length 1 
ACATS Transfer 
Acknowledgement / 
Rejection (019) 
Section 02.12.03 
Earnings to Date Money 
Amount 
record 9, start 78, end 93, 
length 16 
ACATS Transfer (018) Section 02.11.09 
record 3, start 26, end 41, 
length 16 
ACATS Transfer 
Acknowledgement / 
Rejection (019) 
Section 02.12.03 
Negative Earnings to Date 
Indicator 
record 9, start 94, end 94, 
length 1 
ACATS Transfer (018) Section 02.11.09 
record 3, start 42, end 42, 
length 1 
ACATS Transfer 
Acknowledgement / 
Rejection (019) 
Section 02.12.03 
Cost Basis Money Amount record 10, start 81, end 96, 
length 16 
ACATS Transfer (018) Section 02.11.10 
record 3, start 43, end 58, 
length 16 
ACATS Transfer 
Acknowledgement / 
Rejection (019) 
Section 02.12.03 
 
1. 
 NEW REJECT CODE 
      The following new [[NSCC]] reject code will be utilized to reject an invalid IRS 529 Annual Strategy Change Counter:  
Reject Code Description 
   287  IRS 529 Annual Strategy Change Counter is invalid 
 

---

## Page 99

Fixed Length Record Layouts (Part 1) 
Summary of Changes–Effective Q1 03/28/2022 99 
SUMMARY OF CHANGES–EFFECTIVE Q1 03/28/2022 
2. Requirements Changed for Existing Fields 
Description have been modified for the following fields: 
Field Name Location Modified Description 
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
(Interval Fund) and Transaction Code = 03 (Partial 
[[liquidation]]) or 04 (Full [[liquidation]]). 
 
Best Practice: 
Trade Date for future dated Interval Fund 
repurchase orders should be populated with the 
Repurchase Pricing Date communicated by the 
Fund. 

---

## Page 100

Fixed Length Record Layouts (Part 1) 
Summary of Changes–Effective Q1 03/28/2022 100 
Field Name Location Modified Description 
Anticipated [[settlement]] Date 
  
Order (001) 
Correction (003) 
Before change 
mmddccyy 
For Security Issue Type = 63, Required if [[settlement]] 
Override Reason Code is space 
For other Security Types: 
1. Required if [[settlement]] Override Reason Code is 
provided and is not 04 or 06 (x-[[settlement]]). 
2. Not allowed if [[settlement]] Override Reason Code = 
04. 
 
After change 
mmddccyy 
 
For Security Issue Type = 63, Required if [[settlement]] 
Override Reason Code is space 
For other Security Types: 
1. Required if [[settlement]] Override Reason Code is 
provided and is not 04 or 06 (x-[[settlement]]). 
2. Not allowed if [[settlement]] Override Reason Code = 
04. 
 
This field should not be populated when Security 
Type = 48, and Transaction Code = 03 (Partial 
[[liquidation]]) or 04 (Full [[liquidation]]). If populated, 
[[NSCC]] will [[default]] the value to 12319999 and pass 
the order to the Fund. 
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
 

---

## Page 101

Fixed Length Record Layouts (Part 1) 
Summary of Changes–Effective Q1 03/28/2022 101 
3. New Data Fields in New Optional Record Sequence 
New data fields added to a new Optional Sequence of existing record types. 
New Data Field  Location Record Type Section  
[[intermediary]] Program 
Indicator–1 
record 7, start 8, end 11, 
length 4 
Order (001)  Section 02.01.07 
record 8, start 8, end 11, 
length 4 
As-Of Order (004) 
Confirmation (005) 
Reconfirmation (006) 
Fund Originated Order (007) 
Fund Originated Order As-Of 
Order (009) 
Post [[settlement]] Cancellation by 
Fund (140) 
Section 02.02.08 
record 34, start 8, end 11, 
length 4 
Full Registration (401) Section 02.10.15 
record 14, start 8, end 11, 
length 4 
Correction (003) 
Correction Confirmation (025) 
Post [[settlement]] Correction by 
Fund (026) 
Section 02.29.14 
[[intermediary]] Program 
Indicator–2 
record 7, start 12, end 15, 
length 4 
Order (001) Section 02.01.07 
record 8, start 12, end 15, 
length 4 
As-Of Order (004) 
Confirmation (005) 
Reconfirmation (006) 
Fund Originated Order (007) 
Fund Originated Order As-Of 
Order (009) 
Post [[settlement]] Cancellation by 
Fund (140) 
Section 02.02.08 
record 34, start 12, end 15, 
length 4 
Full Registration (401) Section 02.10.15 
record 14, start 12, end 15, 
length 4 
Correction (003) 
Correction Confirmation (025) 
Post [[settlement]] Correction by 
Fund (026) 
Section 02.29.14 

---

## Page 102

Fixed Length Record Layouts (Part 1) 
Summary of Changes–Effective Q1 03/28/2022 102 
New Data Field  Location Record Type Section  
Servicing Group [[ID]] record 7, start 16, end 24, 
length 9 
Order (001) Section 02.01.07 
 record 8, start 16, end 24, 
length 9 
As-Of Order (004) 
Confirmation (005) 
Reconfirmation (006) 
Fund Originated Order (007) 
Fund Originated Order As-Of 
Order (009) 
Post [[settlement]] Cancellation by 
Fund (140) 
Section 02.02.08 
 record 34, start 16, end 24, 
length 9 
Full Registration record 401 Section 02.10.15 
 record 14, start 16, end 24, 
length 9 
Correction (003) 
Correction Confirmation (025) 
Post [[settlement]] Correction by 
Fund (026) 
Section 02.29.14 
Additional Relationship [[ID]]–1 record 7, start 25, end 44, 
length 20 
 Order (001) Section 02.01.07 
record 8, start 25, end 44, 
length 20 
As-Of Order (004) 
Confirmation (005) 
Reconfirmation (006) 
Fund Originated Order (007) 
Fund Originated Order As-Of 
Order (009) 
Post [[settlement]] Cancellation by 
Fund (140) 
 
Section 02.02.08 
record 34, start 25, end 44, 
length 20 
Full Registration record 401 Section 02.10.15 
record 14, start 25, end 44, 
length 20 
Correction (003) 
Correction Confirmation (025) 
Post [[settlement]] Correction by 
Fund (026) 
Section 02.29.14 

---

## Page 103

Fixed Length Record Layouts (Part 1) 
Summary of Changes–Effective Q1 03/28/2022 103 
New Data Field  Location Record Type Section  
Additional Relationship [[ID]]–2 record 7, start 45, end 64, 
length 20 
Order (001) Section 02.01.07 
record 8, start 45, end 64, 
length 20 
As-Of Order (004) 
Confirmation (005) 
Reconfirmation (006) 
Fund Originated Order (007) 
Fund Originated Order As-Of 
Order (009) 
Post [[settlement]] Cancellation by 
Fund (140) 
Section 02.02.08 
record 34, start 45, end 64, 
length 20 
Full Registration record 401 Section 02.10.15 
record 14, start 45, end 64, 
length 20 
Correction (003) 
Correction Confirmation (025) 
Post [[settlement]] Correction by 
Fund (026) 
Section 02.29.14 4. New Data Field in Existing Record Sequence 
New Data Field  Location  Record Type Section  
De-minimis repurchase waiver 
code 
record 3, start 96, end 96, 
length 1 
Order (001)  Section 02.01.03 
record 3, start 96, end 96, 
length 1 
Correction (003) Section 02.29.03 
5. New Optional Record Type 
Record Type Description Section 
030 Interval Fund Acknowledgement Record Section 02.31.01 
6. New Reject Code 
The following new [[NSCC]] reject code will be utilized to reject an invalid de-minimis repurchaser waiver code: 
Reject Code Description 
286  De-minimis repurchase waiver code is invalid 

---

## Page 104

Fixed Length Record Layouts (Part 1) 
Summary of Changes–Effective Q1 03/28/2022 104 
7. Notes Added to Existing Field 
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

## Page 105

Fixed Length Record Layouts (Part 1) 
Summary of Changes–Effective Q1 03/25/2019 105 
SUMMARY OF CHANGES–EFFECTIVE Q1 03/25/2019 
Reject Codes 
The following new [[NSCC]] reject code will be utilized to reject transactions that fail O -code validation: 
Reject Code Description 
285 [[participant]] is not valid for the Submitter and/or Product 

---

## Page 106

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q4 11/20/2017 106 
SUMMARY OF CHANGES–EFFECTIVE Q4 11/20/2017 
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
 
Record 1, start 57, end 57, 
length 1  
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
 
8 thru B only allowed if Transaction Code = “03” or 
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
04 (Full [[liquidation]]) 

---

## Page 107

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q4 11/20/2017 107 
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
 
Record 2, start 63, end 63, 
length 1 
Before change 
 
0 = Not applicable 
1 = Current year payment 
2 = Prior year payment 
3 = IRA rollover 
4 = [[Asset]] transfer 
5 = Employee—prior year 
6 = Employee—current year 
7 = Employer—prior year 
8 = Employer—current year 
9 = Non-fund prototype IRA 
A = Non-fund qualified plan 
C = Salary Reduction Contribution D = 529 Current 
Year Contribution 
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
2 = Prior year payment 
3 = IRA rollover 
4 = [[Asset]] transfer 
5 = Employee—prior year 

---

## Page 108

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q4 11/20/2017 108 
Field Name Location Added Values and Updated Notes 
6 = Employee—current year 
7 = Employer—prior year 
8 = Employer—current year 
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
U = 529 In–State Plan Transfer Contribution 
V = 529 Owner Change 
W = 529 Beneficiary Change-In-Family 
Note: 
D, P, Q, U, V and W indicate Section 529 Plan. 

---

## Page 109

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q4 11/20/2017 109 
[[liquidation]] Indicator Order record (001) 
 
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
 
Record 3 start 77, end 77, 
length 1 
Before change 
 
Required if Trans Type = 5. 
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
D = 529 Plan Account—Beneficiary Disability 
E = 529 Plan Account–Beneficiary Death 
F = 529 Plan Account–Beneficiary Scholarship 
Notes: 
• 4 through F should apply only to transactions with 
CDSC Waivers 
• C through F should only apply to Section 529 
plans. 

---

## Page 110

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q4 11/20/2017 110 
IRA/529 [[liquidation]] Indicator Order record (001) 
 
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
 
Record 4, start 71, end 71, 
length 1 
Before change 
 
0 = Not applicable 
1 = Distribution–premature 
2 = Distribution–disability 
3 = Distribution–death 
4 = Distribution–normal 
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
1 = Distribution–premature 
2 = Distribution–disability 
3 = Distribution–death 
4 = Distribution–normal 
5 = Hardship withdrawal 
6 = Loan 
7 = Rollover 
8 = Adjust prior year excess 
9 = Adjust current year excess 
A = Qualified 
B = Non-Qualified 
C = Distribution–Non-Taxable 
D = 529 Owner Change 
E = 529 Beneficiary Change–In-Family 
Notes: 
A and B are required if Transaction Type = 
8 = (529 [[participant]] Distribution) 
9 = (529 Beneficiary Distribution) 
A = (529 School Distribution) 
B = (529 Roll Over Distribution 

---

## Page 111

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q4 11/20/2017 111 
Field Name Location Added Values and Updated Notes 
C is required if Transaction Type = E (529 In-State 
Plan Transfer Distribution) 
D or E is required if Transaction Type = F (529 
Registration Change) 
2. Requirements Changed for Existing Fields 
Requirements have been changed for the following fields: 
Field Name Location Modified requirement 
Beneficiary SSN/EIN Number Order record (001) 
 
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
 
Record 4, start 84, end 92, 
length 9 
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
U (529 In–State Plan Transfer Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change-In-Family) 
 
Transaction Codes 
01 (Initial purchase) 
02 (Subsequent purchase) 

---

## Page 112

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q4 11/20/2017 112 
Field Name Location Modified requirement 
Cost Basis Money Amount Order record (001) 
 
Record 6, start 45, end 60, 
length 16 
 
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
 
Record 7 start 45, end 60, 
length 16 
Before change 
 
Required if the [[Asset]] Type Indicator = Q. 
 
Format: 
99,999,999,999,999.99 
 
After change 
 
Required if the [[Asset]] Type Indicator = Q. U, V or W. 
Q (529 Rollover Contribution) 
U (529 In–State Plan Transfer Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change-In-Family) 
 
Format: 
99,999,999,999,999.99 
Zeros are allowed (added 9/25/2017)  
Earnings to Date Money Amount Order record (001) 
Record 6, start 61, end 76, 
length 16 
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
Record 7, start 61, end 76, 
length 16 
Required if the [[Asset]] Type Indicator = Q. 
 
Format: 
99,999,999,999,999.99 
 
Required if the [[Asset]] Type Indicator = Q. U, V or W. 
Q (529 Rollover Contribution) 
U (529 In–State Plan Transfer Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change—In-Family) 
Format: 
99,999,999,999,999.99 
Zeros are allowed (added 9/25/2017) 

---

## Page 113

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q4 11/20/2017 113 
3. Requirements Changed for Existing Records 
Record Type Record Number Modified requirement 
Order (001)   Record 6 Before change 
Required when Redemption Fee Indicator is provided or 
[[Asset]] Type Indicator = Q 
 
Optional for all other [[Asset]] Types. 
 
After change 
 
Required when Redemption Fee Indicator is provided or 
[[Asset]] Type Indicator = Q, U, V or W. 
 
Optional for all other [[Asset]] Types. 
As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Fund Originated Order record 
(007) 
Fund Originated As-Of Order 
record (009) 
Post [[settlement]] Cancellation by 
Fund record (140) 
Record 7 Before change 
Required when Redemption Fee Indicator is provided or 
[[Asset]] Type Indicator = Q 
 
Optional for all other [[Asset]] Types. 
 
After change 
 
Required when Redemption Fee Indicator is provided or 
[[Asset]] Type Indicator = Q, U, V or W. 
 
Optional for all other [[Asset]] Types. 
Correction record (003) 
Correction Confirmation record 
(025) 
Post [[settlement]] Correction by 
Fund record (026 
Record 7 Before change 
Required when Redemption Fee Indicator is provided or 
[[Asset]] Type Indicator = Q 
 
Optional for all other [[Asset]] Types. 
 
After change 
 
Required when Redemption Fee Indicator is provided or 
[[Asset]] Type Indicator = Q, U, V or W. 
 
Optional for all other [[Asset]] Types. 

---

## Page 114

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q4 11/20/2017 114 
4. Modified Description of Existing Field 
Field Name Location Changes to Description 
Transaction Code  Order record (001) 
record 1, start 62, end 63, 
length 2 
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

---

## Page 115

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 115 
SUMMARY OF CHANGES–EFFECTIVE Q3 09/26/2016 
1. New Fields 
The following fields have been added to existing layouts: 
New Name Location Layout Section  
1. Money Market [[Liquidity]] 
Fee/Redemption Gate Indicator 
record 6, start 78, 
end 78, length 1 
Order record (001) Section 02.01.01 
record 7, start 78, 
end 78, length 1 
As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Post [[settlement]] Cancellation 
by Fund record (140) 
Section 02.02.01 record 7, start 78, 
end 78, length 1 
Correction record (003) 
Correction Confirmation record 
(025) 
Post [[settlement]] Correction by 
Fund record (026) 
Section 02.29.01 
record 4, start 74, 
end 74, length 1 
Exchange Order record (015) Section 02.06.01 
record 4, start 74, 
end 74, length 1 
Exchange Confirmation record 
(016) 
Exchange Reconfirmation 
record (017) 
Post [[settlement]] Exchange 
Cancellation record (021) 
Section 02.07.01 

---

## Page 116

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 116 
New Name Location Layout Section  
2. Transaction Received Date record 6, start 79, 
end 86, length 8 
Order record (001) Section 02.01.01 
record 7, start 79, 
end 86, length 8 
As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Post [[settlement]] Cancellation 
by Fund record (140) 
Section 02.02.01 
record 7, start 79, 
end 86, length 8 
Correction record (003) 
Correction Confirmation record 
(025) 
Post [[settlement]] Correction by 
Fund record (026) 
Section 02.29.01 record 4, start 75, 
end 82, length 8 
Exchange Order record (015) Section 02.06.01 
record 4, start 75, 
end 82, length 8 
Exchange Confirmation record 
(016) 
Exchange Reconfirmation 
record (017) 
Post [[settlement]] Exchange 
Cancellation record (021) 
Section 02.07.01 
3. Aggregated Order Indicator record 6, start 87, 
end 87, length 1 
Order record (001) Section 02.01.01 
record 7, start 87, 
end 87, length 1 
As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Post [[settlement]] Cancellation 
by Fund record (140) 
Section 02.02.01 record 7, start 87, 
end 87, length 1 
Correction record (003) 
Correction Confirmation record 
(025) 
Post [[settlement]] Correction by 
Fund record (026) 
Section 02.29.01 
record 4, start 83, 
end 83, length 1 
Exchange Order record (015) Section 02.06.01 
record 4, start 83, 
end 83, length 1 
Exchange Confirmation record 
(016) 
Exchange Reconfirmation 
record (017) 
Post [[settlement]] Exchange 
Cancellation record (021) 
Section 02.07.01 

---

## Page 117

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 117 
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
Post [[settlement]] Correction by Fund record 
(026) 
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

## Page 118

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 118 
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

---

## Page 119

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 119 
3. Requirements Changed for Existing Fields 
Requirements have been changed for the following fields: 
Field Name Location Modified requirement 
1 Transaction Received Time 
(renamed from “[[participant]] 
Processing Time”) 
Order record (001) 
 Record 2, start 71, end 76, 
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
 
 
Record 2, start 71, end 76, 
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
 
Record Types 005 & 006: 
Must contain the same value as provided by the 
firm on the Order transaction (record type 001 or 
004). [[NSCC]] will reject if a fund provided value is 
different from the value submitted by the firm. 

---

## Page 120

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 120 
Field Name Location Modified requirement 
 Correction record (003) 
Correction Confirmation record 
(025) 
Post [[settlement]] Correction by 
Fund record (026) 
 
Record 2, start 71, end 76, 
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
 
Record Type 025: 
Must contain the same value as provided by the 
firm on the Correction transaction (record type 
003). [[NSCC]] will reject if a fund provided value is 
different from the value submitted by the firm. 

---

## Page 121

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 121 
Field Name Location Modified requirement 
 Exchange Order record (015) 
 
Record 2, start 71, end 76, 
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
 Exchange Confirmation record 
(016) 
Exchange Reconfirmation 
record (017) 
Post [[settlement]] Exchange 
Cancellation record (021) 
 
Record 2, start 71, end 76, 
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
 
For Record types 016 and 017 
Must contain the same value as provided on the 
Exchange transaction (record type 015). 
[[NSCC]] will reject if a fund provided value is 
different from the value submitted by the firm. 

---

## Page 122

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 122 
Field Name Location Modified requirement 
2 Redemption Fee Indicator Order record (001) 
Record 3, start 81, end 81, 
length 1 
Before change 
 
0 = Short-Term Redemption (STR) Fee 
1 = STR Fee with CDSC 
 
After change 
 
0 = Short-Term Redemption (STR) 
1 = STR with CDSC 
2 = Money Market [[Liquidity]] Fee 
3 = Money Market [[Liquidity]] Fee with CDSC 
As-Of Order record (004) 
Confirmation record (005) 
Reconfirmation record (006) 
Fund Originated Order record 
(007) 
Fund Originated As-Of Order 
record (009) 
Post [[settlement]] Cancellation by 
Fund record (140) 
 
Record 3, start 81, end 81, 
length 1 
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

## Page 123

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 123 
Field Name Location Modified requirement 
Correction record (003) 
Correction Confirmation record 
(025) 
Post [[settlement]] Correction by 
Fund record (026) 
 
Record 3, start 81, end 81, 
length 1 
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
 
Record 3, start 81, end 81, 
length 1 
Before change 
 
0 = Short-Term Redemption (STR) Fee 
1 = STR Fee with CDSC 
 
After change 
 
0 = Short-Term Redemption (STR) 
1 = STR with CDSC 
2 = Money Market [[Liquidity]] Fee 
3 = Money Market [[Liquidity]] Fee with CDSC 

---

## Page 124

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 124 
Field Name Location Modified requirement 
Exchange Confirmation record 
(016) 
Exchange Reconfirmation 
record (017) 
Post [[settlement]] Exchange 
Cancellation record (021) 
 
Record 3, start 81, end 81, 
length 1 
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

## Page 125

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 125 
Field Name Location Modified requirement 
3 Redemption Fee Rate 
(renamed from “STR Fee Rate”) 
Order record (001) 
Record 6, start 8, end 14, 
length 7 
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

## Page 126

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 126 
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
 
Record 7, start 8, end 14, 
length 7 
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

## Page 127

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 127 
Field Name Location Modified requirement 
Correction record (003) 
Correction Confirmation record 
(025) 
Post [[settlement]] Correction by 
Fund record (026) 
 
Record 7, start 8, end 14, 
length 7 
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

## Page 128

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 128 
Field Name Location Modified requirement 
Exchange Order record (015) 
 
Record 5, start 64, end 70, 
length 7 
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

## Page 129

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 129 
Field Name Location Modified requirement 
Exchange Confirmation record 
(016) 
Exchange Reconfirmation 
record (017) 
Post [[settlement]] Exchange 
Cancellation record (021) 
 
Record 5, start 64, end 70, 
length 7 
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

## Page 130

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 130 
Field Name Location Modified requirement 
4 Redemption Fee Money 
Amount (renamed from STR 
Fee Money Amount) 
Order record (001) 
Record 6, start 29, end 44, 
length 16 
Before change 
 
99,999,999,999,999.99 
Required when Redemption Fee Indicator is provided 
and STR Fee Share Quantity = 0 or Space. 
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

## Page 131

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 131 
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
 
Record 7, start 29, end 44, 
length 16 
Before change 
 
99,999,999,999,999.99 
For all record types: 
Not allowed if Redemption Fee Indicator is not 
provided. 
For record type 004: 
Required when Redemption Fee Indicator is provided 
and STR Fee Share Quantity = 0 or Space. 
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

## Page 132

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 132 
Field Name Location Modified requirement 
Correction record (003) 
Correction Confirmation record 
(025) 
Post [[settlement]] Correction by 
Fund record (026) 
 
Record 7, start 29, end 44, 
length 16 
Before change 
 
99,999,999,999,999.99 
For all record types: 
Not allowed if Redemption Fee Indicator is not 
provided. 
For record type 003: 
Required when Redemption Fee Indicator is provided 
and STR Fee Share Quantity = 0 or Space. 
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

## Page 133

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 133 
Field Name Location Modified requirement 
Exchange Order record (015) 
 
Record 5, start 85, end 100, 
length 16 
 
Before change 
 
99,999,999,999,999.99 
Required when Redemption Fee Indicator is provided 
and STR Fee Share Quantity = 0 or Space. 
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
 
If “Redemption Fee Indicator”=0 or 1, this field 
will be utilized to communicate a Short-Term 
Redemption (STR) Fee Money Amount. 

---

## Page 134

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 134 
Field Name Location Modified requirement 
Exchange Confirmation record 
(016) 
Exchange Reconfirmation 
record (017) 
Post [[settlement]] Exchange 
Cancellation record (021) 
 
Record 5, start 85, end 100, 
length 16 
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
 
If “Redemption Fee Indicator”=0 or 1, this field 
will be utilized to communicate a Short-Term 
Redemption (STR) Fee Money Amount. 

---

## Page 135

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 135 
Field Name Location Modified requirement 
5. STR Fee Share Quantity Order record (001) 
Record 6, start 15, end 28, 
length 14 
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

## Page 136

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 136 
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
 
Record 7, start 15, end 28, 
length 14 
Before change 
 
9,999,999,999.9999 
 
For all record types: 
Not allowed if Redemption Fee Indicator is not 
provided. 
For record type 004: 
Required when Redemption Fee Indicator is provided 
and STR Fee Money Amount = 0 or Space. 
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
provided and “Redemption Fee Money Amount” = 
0 or Space. 
Not allowed if “Redemption Fee Money Amount” 
> 0. 
 
For record types 005 and 006: 
If zero or Space, and “Redemption Fee Indicator” 
is provided, will not override the STR Fee Share 
Quantity in the database. 
 
For all record types: 
Not allowed when “Redemption Fee Indicator” is 
populated with either ‘2’ (Money Market [[Liquidity]] 
Fee) or ‘3’ (Money Market [[Liquidity]] Fee with 
CDSC). 

---

## Page 137

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 137 
Field Name Location Modified requirement 
Correction record (003) 
Correction Confirmation record 
(025) 
Post [[settlement]] Correction by 
Fund record (026) 
 
Record 7, start 15, end 28, 
length 14 
Before change 
 
9,999,999,999.9999 
 
For all record types: 
Not allowed if Redemption Fee Indicator is not 
provided. 
For record type 003: 
Required when Redemption Fee Indicator is provided 
and STR Fee Money Amount = 0 or Space. 
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
provided and Redemption Fee Money Amount = 0 
or Space. 
 
For record type 025: 
If zero or Space, and Redemption Fee Indicator is 
provided, will not override the STR Fee Share 
Quantity in the database. 
 
For all record types: 
Not allowed when “Redemption Fee Indicator” is 
populated with either ‘2’ (Money Market [[Liquidity]] 
Fee) or ‘3’ (Money Market [[Liquidity]] Fee with 
CDSC). 

---

## Page 138

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 138 
Field Name Location Modified requirement 
Exchange Order record (015) 
 
Record 5, start 71, end 84, 
length 14 
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

## Page 139

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 139 
Field Name Location Modified requirement 
Exchange Confirmation record 
(016) 
Exchange Reconfirmation 
record (017) 
Post [[settlement]] Exchange 
Cancellation record (021) 
 
Record 5, start 71, end 84, 
length 14 
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

## Page 140

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q3 09/26/2016 140 
The descriptions of the following reject codes have been modified: 
Reject Code New Description Old Description 
168 Transaction Received Time missing/invalid [[participant]] Processing Time invalid 
250 Redemption Fee Rate missing/invalid STR Fee Rate invalid 
252 Redemption Fee Money Amount missing/invalid STR Fee Money Amount missing/invalid 
5. Requirements Changed for Existing Record Number 
Record Type Record Number Modified requirement 
Exchange Confirmation record 
(016) 
Exchange Reconfirmation record 
(017) 
Post [[settlement]] Exchange 
Cancellation record (021)  
Record 5 
Before change 
Optional 
 
After change 
 
Required when Redemption Fee Indicator is provided. 

---

## Page 141

Fixed Length Record Layouts (Part 1) 
Summary of Changes–effective Q1 02/29/2016 141 
SUMMARY OF CHANGES–EFFECTIVE Q1 02/29/2016 
Comment Added to Existing Field 
Field Name Record Type & Location Before change After change 
Reminder Age Reminders (080) 
Record 1 of 1, Part 3 
1-9998 = Reminder age (in business 
days) 
 
9999 = Pending period expired; 
original transaction deleted by 
Fund/SERV 
1-9998 = Reminder age (in 
business days) 
 
9999 = Pending period expired; 
original transaction deleted by 
Fund/SERV 
 
Effective 02/29/2016, Reminder 
080 record with age 9999 will 
no longer be sent to Funds 
(Important Notice a8107)  

---

## Page 142

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q3 07/27/2015 142 
SUMMARY OF CHANGES–EFFECTIVE Q3 07/27/2015 
1. Requirements Changed for Existing Field 
Field Name Record Type & Location Modified requirement 
Social Code  Order Record (001) 
As-Of Order (004) 
Confirmation (005) 
Reconfirmation (006) 
Correction (003) 
Correction Confirmation (025) 
Post [[settlement]] Correction by 
Fund (026) 
 
Record 4, start 82, end 83, 
length 2 
Before change 
 
Optional 
 
After change 
 
Optional/Conditional 
 
Required when “Transaction 
Code” = 01–Initial Purchase 
2. Requirements Changed for Existing Record Number 
Record Type Record Number Modified requirement 
Order Record (001) 
As-Of Order (004) 
Confirmation (005) 
Reconfirmation (006) 
Correction (003) 
Correction Confirmation (025) 
Post [[settlement]] Correction by 
Fund (026) 
 Record 4  Before change 
Required if any of the following fields in this record are 
required: 
• Country of Origin 
• IRA/529 [[liquidation]] Indicator 
• Periodic Frequency Indicator 
• Beneficiary SSN/EIN Number 
 
After change 
 
Required if any of the following fields in this record are 
required: 
• Country of Origin 
• IRA/529 [[liquidation]] Indicator 
• Periodic Frequency Indicator 
• Beneficiary SSN/EIN Number 
• Social Code (when “Transaction Code”=01) 

---

## Page 143

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q2 04/27/2015 143 
SUMMARY OF CHANGES–EFFECTIVE Q2 04/27/2015 
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
 
Record 3, start 79, end 80, 
length 2 
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
 
Record 4, start 72, end 73, 
length 2 
Before change 
 
Required for exchanges to new accounts 
Transaction Type: 
6 (Exchange to new account) 
C (Voluntary Cross Class Exchange to new account) 
 
After change 
 
Required for all exchanges 

---

## Page 144

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q3 07/02/2014 144 
SUMMARY OF CHANGES–EFFECTIVE Q3 07/02/2014 
1. Documentation Changes 
Fund/SERV Variable Record Layouts Part 3–The Table of Contents has been modified to remove references 
to the following records: 
• Settling Trade Detail for non-USD [[settlement]] by Currency–Record 076 
• Settling Trade Detail for TPA/Investment Agent/TPP non-USD [[settlement]] by Currency–Record 078 
• Settling Trade Trailer for non-USD [[settlement]] by Currency–Record 077 
• Settling Trade Trailer for TPA/Investment Agent/TPP non-USD [[settlement]] by Currency–Record 079 

---

## Page 145

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q3 07/28/2014 145 
SUMMARY OF CHANGES–EFFECTIVE Q3 07/28/2014 
1. New Fields 
The following fields have been added to existing layouts: 
New Name Location Layout Section  
1. Secondary Social 
Security Number 
record 1, start 92, end 100, 
length 9 
ACATS Transfer record (018) Section 02.11.01 
2. Fund [[settlement]] Date record 1, start 85, end 92, length 
8 
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
SSN/EIN Indicator record 2, start 70, end 70, 
length 1 
Before change 
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

## Page 146

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q3 07/28/2014 146 
Field Name Location Changes to Description 
SSN/EIN Number record 2, start 71, end 79, 
length 9 
Before change 
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
For all other transfer types, if ACATS does not 
receive an FR record, ACATS populates this field with 
the Receiving [[participant]]’s Tax [[ID]] number from the 
ACATS [[participant]] master file. 
Customer SSN/EIN Number record 8, start 78, end 86, 
length 9 
Before change 
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

## Page 147

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q4 11/18/2013 147 
SUMMARY OF CHANGES–EFFECTIVE Q4 11/18/2013 
1. New Fields 
The following fields have been added to existing layouts: 
New Name Location Layout Section  
1. State of Sale (State Code) record 4, start 72, end 73, length 
2 
Exchange Order record 015  Section 02.06.04 
2. State of Sale (State Code) record 4, start 72, end 73, length 
2 
Exchange Confirmation (016), 
Exchange Reconfirmation (017), 
Post [[settlement]] Exchange 
Cancellation (021) 
Section 02.07.03 
3. Plan Account Number record 4, start 78, end 97, length 
20 
Full Registration record 401 Section 02.10.04 
4. Plan Account Number 
Indicator 
record 4, start 98, end 98, length 
1 
Full Registration record 401 Section 02.10.04 
5. Chapter 4 Status Code record 33, start 8, end 9, length 
2 
Full Registration record 401 Section 02.10.14 
6. Global [[intermediary]] 
Identification Number 
record 33, start 10, end 34, 
length 25 
Full Registration record 401 Section 02.10.14 
7. Underlying Client’s Foreign 
Tax [[ID]] 
record 33, start 35, end 59, 
length 25 
Full Registration record 401 Section 02.10.14 
8. FATCA Override Special 
Rate 
record 33, start 60, end 64, 
length 5 
Full Registration record 401 Section 02.10.14 

---

## Page 148

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q4 11/18/2013 148 
2. Values or Comments Added to or Deleted from Existing Fields 
New values or comments have been added to the following fields: 
Field Name Location Added or Deleted Values or Comments 
1. Withhold Indicator  Full Registration (401) 
Record 3, start 9, end 9, 
length 1  
Before change 
W9 indications 
0 = Certified (W-9 on file) 
1 = Failure to provide tin 
2 = Failure to certify tin 
3 = Notification of incorrect TIN from the Secretary of 
Treasury (Withhold due to B Notice) 
4 = Failure to certify backup withholding status 
5 = Voluntary disclosure from payee of affirmative 
backup withholding status 
6 = Notification to commence Backup Withholding 
from Secretary of Treasury for underreporting 
[[Dividend]] and/or interest payments (Withhold due to C 
Notice) 
[[Dividend]] and/or interest payments 
7 = Applied for social security number 
8 = Exempt recipient 
9 = Account(s) subject to both B and C Notice 
Withholding 
W8 indications 
A = Uncertified foreign account (no W8 form on file-
backup withholding necessary) 
B = Certified foreign [[Beneficial Owner]] account (from 
W8-BEN on file) 
C = Certified foreign [[intermediary]] account (form W8-
IMY on file) 
D = Certified valid foreign account (form W8-ECI on 
file with ITIN) 
E = Certified foreign exempt account (form W8-EXP 
on file) 
F = W8 on file—no treaty rate claimed 
G = W8 Beneficiary with TIN on file 
 
After change 
W9 indications 
0 = Certified (W-9 on file) 
1 = Failure to provide tin 
2 = Failure to certify tin 
3 = Notification of incorrect TIN from the Secretary of 
Treasury (Withhold due to B Notice) 

---

## Page 149

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q4 11/18/2013 149 
Field Name Location Added or Deleted Values or Comments 
4 = Failure to certify backup withholding status 
5 = Voluntary disclosure from payee of affirmative 
backup withholding status 
6 = Notification to commence Backup Withholding 
from Secretary of Treasury for underreporting 
[[Dividend]] and/or interest payments (Withhold due to C 
Notice) 
[[Dividend]] and/or interest payments 
7 = Applied for social security number 
8 = Exempt recipient 
9 = Account(s) subject to both B and C Notice 
Withholding 
W8 indications 
A = Uncertified foreign account (no W8 form on file-
backup withholding necessary) 
B = Certified foreign [[Beneficial Owner]] account (from 
W8-BEN on file) 
C = Certified foreign [[intermediary]] account (form W8-
IMY on file) 
D = Certified valid foreign account (form W8-ECI on 
file with ITIN) 
E = Certified foreign exempt account (form W8-EXP 
on file) 
F = W8 on file—no treaty rate claimed 
G = W8 Beneficiary with TIN on file 
H = W-8BEN-E on file/documentary evidence 
I = Voluntary FATCA withholding—W-8BEN-E on 
file/documentary evidence 
J = W8-IMY or W-8BEN-E pending 

---

## Page 150

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q4 11/18/2013 150 
Field Name Location Added or Deleted Values or Comments 
W8 Qualified [[intermediary]] 
Indicator 
Full Registration (401) 
Record 3, start 92, end 92, 
length 1  
Before change 
Required if Withhold Indicator = C. 
1 = QI (qualified [[intermediary]]-primary withholding) 
2 = QI (Qualified [[intermediary]] non-withholding) 
3 = Non-QI (non-Qualified [[intermediary]]—non-
withholding, not the [[Beneficial Owner]]) 
4 = Partnership (withholding) 
5 = Partnership (non-withholding) 
6 = U. S. branch (non-withholding) 
7 = Trust (withholding) 
8 = Trust (non-withholding) 
 
After change 
Required if Withhold Indicator = C. 
1 = QI (qualified [[intermediary]]—primary withholding) 
2 = QI (Qualified [[intermediary]] non-withholding) 
3 = Non-QI (non-Qualified [[intermediary]]—non-
withholding, not the [[Beneficial Owner]]) 
4 = Partnership (withholding) 
5 = Partnership (non-withholding) 
6 = U. S. branch (non-withholding) 
7 = Trust (withholding) 
8 = Trust (non-withholding) 
9 = Territory Financial Institution 
3. Reject Codes 
The following new reject codes have been added for the Plan Account Number Indicator:  
Reject Code Description 
277 Plan Account Number is missing/invalid  
278 Chapter 4 Status Code invalid 
279 FATCA Override Special Rate Invalid 
 

---

## Page 151

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q1 3/18/2013 151 
SUMMARY OF CHANGES–EFFECTIVE Q1 3/18/2013 
1. Values or Comments Added to or Deleted from Existing Fields 
New values or comments have been added to the following fields: 
Field Name Location Added or Deleted Values or 
Comments 
1. [[Asset]] Type Indicator Order Record (001) 
As-Of Order Record (004) 
Confirmation Record (005) 
Reconfirmation Record (006) 
Fund Originated Order Record (007) 
Fund Originated As-Of Order Record 
(009) 
Post [[settlement]] Cancellation by Fund 
Record (140) 
Correction Record (003) 
Correction Confirmation Record (025) 
Post [[settlement]] Correction by Fund 
Record (026) 
 
Record 2, start 63, end 63, length 1 
Before change 
0 = Not applicable 
1 = Current year payment 
2 = Prior year payment 
3 = IRA rollover 
4 = [[Asset]] transfer 
5 = Employee-prior year 
6 = Employee-current year 
7 = Employer-prior year 
8 = Employer-current year 
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
 

---

## Page 152

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q1 3/18/2013 152 
Field Name Location Added or Deleted Values or 
Comments 
After change 
0 = Not applicable 
1 = Current year payment 
2 = Prior year payment 
3 = IRA rollover 
4 = [[Asset]] transfer 
5 = Employee-prior year 
6 = Employee-current year 
7 = Employer-prior year 
8 = Employer-current year 
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
L = Omnibus [[Dividend]] 
Reconciliation 
M = Variable Annuity 
N = Wrap Program 
O = Defined Benefit Plan 
P = 529 Previous Year Contribution 
Q = 529 Rollover Contribution 
S = Omnibus Short-Term Capital 
Gain Reconciliation 
T = Omnibus Long-Term Capital 
Gain Reconciliation 
Note: 
D, P and Q indicate Section 529 Plan. 

---

## Page 153

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q1 3/18/2013 153 
Field Name Location Added or Deleted Values or 
Comments 
2. NAV Reason Code Order Record (001) 
As-Of Order Record (004) 
Confirmation Record (005) 
Reconfirmation Record (006) 
Fund Originated Order Record (007) 
Fund Originated As-Of Order Record 
(009) 
Post [[settlement]] Cancellation by Fund 
Record (140) 
Correction Record (003) 
Correction Confirmation Record (025) 
Post [[settlement]] Correction by Fund 
Record (026) 
 
Record 3, start 78, end 78, length 1 
Before change 
Required if Trans Type = 3. 
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
9 = Section 529 Account-Qualified 
State Tuition Program 
A = [[Dividend]] reinvestment trade 
B = Trust Company NAV per 
Agreement 
C = Refer to [[Asset]] Type Indicator 
D = Deminimis Amount Processed at 
NAV 
 
After change 
Required if Trans Type = 3. 
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
9 = Section 529 Account-Qualified 
State Tuition Program 
A = [[Dividend]] reinvestment trade 
B = Trust Company NAV per 
Agreement 

---

## Page 154

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q1 3/18/2013 154 
Field Name Location Added or Deleted Values or 
Comments 
C = Refer to [[Asset]] Type Indicator 
D = Deminimis Amount Processed at 
NAV 
E = Self Directed Brokerage 
Account 
3. NAV Reason Code Exchange Order Record (015) 
Exchange Confirmation Record (016) 
Exchange Reconfirmation Record 
(017) 
Post [[settlement]] Exchange 
Cancellation (021) 
 
Record 3, start 78, end 78, length 1 
 
Before change 
Required if Trans Type = 3. 
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
9 = Section 529 Account—Qualified 
State Tuition Program 
A = [[Dividend]] reinvestment trade 
B = Trust Company NAV per 
Agreement 
D = Deminimis Amount Processed at 
NAV 
 

---

## Page 155

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q1 3/18/2013 155 
Field Name Location Added or Deleted Values or 
Comments 
After change 
Required if Trans Type = 3. 
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
9 = Section 529 Account—Qualified 
State Tuition Program 
A = [[Dividend]] reinvestment trade 
B = Trust Company NAV per 
Agreement 
D = Deminimis Amount Processed at 
NAV 
E = Self Directed Brokerage Account 
4. Transaction Type  Exchange Order Record (015) 
Exchange Confirmation Record (016) 
Exchange Reconfirmation Record 
(017) 
Post [[settlement]] Exchange 
Cancellation (021) 
 
Record 1, start 57, end 57, length 1 
Before change 
6 = Exchange to new account 
7 = Exchange to existing account 
 
After change 
6 = Exchange to new account 
7 = Exchange to existing account 
C = Voluntary Cross Class Exchange 
to new account 
D = Voluntary Cross Class Exchange 
to existing account 
5. Network Control Indicator (for the 
From Account) 
Exchange Order Record (015) 
Exchange Confirmation Record (016) 
Exchange Reconfirmation Record 
(017) 
Post [[settlement]] Exchange 
Cancellation Record (021) 
 
Record 2, start 68, end 68, length 1  
Before change 
0 = Non-networked 
1 = Matrix level 1 
2 = Matrix level 2 
3 = Matrix level 3 
4 = Matrix level 4 
 
 

---

## Page 156

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q1 3/18/2013 156 
Field Name Location Added or Deleted Values or 
Comments 
After change 
0 = Non-networked 
3 = Matrix level 3 
4 = Matrix level 4 
6. Network Control Indicator (for the To 
Account) 
Exchange Order Record (015) 
 
Record 4, start 43, end 43, length 1  
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
7. Network Control Indicator (for the To 
Account) 
Exchange Confirmation Record (016) 
Exchange Reconfirmation Record 
(017) 
Post [[settlement]] Exchange 
Cancellation Record (021) 
 
Record 4, start 43, end 43, length 1  
Before change 
0 = Non-networked 
1 = Matrix level 1 
Not allowed if Record Type = 016 or 
017 
and Transaction Type = 6 
2 = Matrix level 2 
Not allowed if Record Type = 016 or 
017 
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
Before change 
0 = Non-networked 
1 = Matrix level 1 

---

## Page 157

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q1 3/18/2013 157 
Field Name Location Added or Deleted Values or 
Comments 
Reconfirmation Record (006) 
Fund Originated Order Record (007) 
Fund Originated As-Of Order Record 
(009) 
Post [[settlement]] Cancellation by Fund 
Record (140) 
Extended Correction Transfer (200) 
Extended Correction Transfer 
Acknowledgment (201) 
Order Acknowledgment for Money 
Market Purchase (101) 
Firm Delete Record (102) 
Release to [[settlement]] Record (109) 
Registration Acknowledgment Record 
(112) 
Delete Pending Registration Record 
(113) 
Receiving Fund Exit from ToRA Record 
(214) 
Correction Record (003) 
Correction Confirmation Record (025) 
Post [[settlement]] Correction by Fund 
Record (026) 
 
Record 2, start 68, end 68, length 1  
2 = Matrix level 2 
3 = Matrix level 3 
4 = Matrix level 4 
 
After change 
0 = Non-networked 
3 = Matrix level 3 
4 = Matrix level 4 

---

## Page 158

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q1 3/18/2013 158 
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
 
 Record 1, start 85, end 88, 
length 4 
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
2. TPA/Investment Agent/TPP 
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
 
Record 1, start 85, end 88, 
length 4 
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

## Page 159

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q1 3/18/2013 159 
Field Name Location Modified requirement 
3. Exch To Account Number  Exchange Order Record (015) 
 
Record 4, start 22, end 41, 
length 20 
 
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
 
Record 1, start 68, end 75, 
length 8 
Before change 
Optional 
 
After change 
Required  

---

## Page 160

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q1 2013 160 
SUMMARY OF CHANGES–EFFECTIVE Q1 2013 
1. Modified Description of Values of Existing Field 
Description of values 3, 6, and 9 for Withholding Indicator is changed. 
Field Name Location Changes to Description 
Withhold Indicator Full Registration (401) 
ACATS Transfer (018) 
 
Record 3, start 9, end 9, 
length 1 
Before change 
 
W9 indications 
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
W8-BEN on file) 
C = Certified foreign [[intermediary]] account (form W8-
IMY on file) 
D = Certified valid foreign account (form W8-ECI on 
file with ITIN) 
E = Certified foreign exempt account (form W8-EXP 
on file) 
F = W8 on file—no treaty rate claimed 
G = W8 Beneficiary with TIN on file 
 
After change 
W9 indications 
0 = Certified (W-9 on file) 
1 = Failure to provide tin 
2 = Failure to certify tin 

---

## Page 161

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q1 2013 161 
Field Name Location Changes to Description 
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
W8-BEN on file) 
C = Certified foreign [[intermediary]] account (form W8-
IMY on file) 
D = Certified valid foreign account (form W8-ECI on 
file with ITIN) 
E = Certified foreign exempt account (form W8-EXP 
on file) 
F = W8 on file—no treaty rate claimed 
G = W8 Beneficiary with TIN on file 

---

## Page 162

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q2 04/23/2012 162 
SUMMARY OF CHANGES–EFFECTIVE Q2 04/23/2012 
1. Values or Comments Added to or Deleted from Existing Fields 
New values or comments have been added to the following fields: 
Field Name Location Added or Deleted Values or Comments 
1. Network Control 
Indicator 
Full Registration Record (401) 
Record 2, start 68, end 68, length 1 
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
Record 2, start 68, end 68, length 1 
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
Record 7, start 74, end 74, length 1 
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

## Page 163

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q2 04/23/2012 163 
Field Name Location Added or Deleted Values or Comments 
4. Network Control 
Indicator (Receiving Firm) 
ACATS Transfer Acknowledgement/Re 
Rejection Record (019) 
Record 2, start 68, end 68, length 1 
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
Record 4, start 43, end 43, 
length 1 
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
Record 4, start 43, end 43, 
length 1 
following condition has been added: 
 
1 = Matrix level 1 
Not allowed if Record Type = 016 or 017 
and Transaction Type = 6 
 
2 = Matrix level 2 
Not allowed if Record Type = 016 or 017 
and Transaction Type = 6 
3. Account Representative Name 
 
Full Registration Record (401) 
Record 3, start 32, end 46, 
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

## Page 164

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q2 04/23/2012 164 
Field Name Location Modified requirement 
4. Account Representative 
Number 
Full Registration Record (401) 
Record 3, start 47, end 55, 
length 9 
Before change 
Required for new networked account (Network 
Control Ind = 1,2,3 or 4, and Fund Account Ind = 0 or 
1) 
 
After change 
Required for new networked account (Network 
Control Ind = 3 or 4, and Fund Account Ind = 0, 1 or 
4) 
5. Branch Identification Number Full Registration Record (401) 
Record 3, start 56, end 64, 
length 9 
Before change 
Required for new networked account (Network 
Control Ind = 1,2,3 or 4, and Fund Account Ind = 0 or 
1) 
 
After change 
Required for new networked account (Network 
Control Ind = 3 or 4, and Fund Account Ind = 0, 1 or 
4) 

---

## Page 165

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q4 10/17/2011 165 
SUMMARY OF CHANGES–EFFECTIVE Q4 10/17/2011 
1. New Fields 
The following fields have been added to existing layouts: 
New Name Location Layout Section  
1. Underlying Firm Symbol 
(UFS) 
record 2, start 86, end 89, 
length 4 
Full Registration (401)  Section 02.10.01 
2. Values or Comments Added to or Deleted from Existing Fields 
New values or comments have been added to the following fields: 
Field Name Location Added or Deleted Values or Comments 
1. Delivering Fund Plan Type Fund Reject Record (100) 
Record 2, start 32, end 32, 
length 1 
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
8 = Roth Conversion IRA 

---

## Page 166

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q4 10/17/2011 166 
Field Name Location Added or Deleted Values or Comments 
9 = Traditional to Roth Conversion IRA 
A = Inherited Traditional IRA 
B = Inherited Roth IRA 
C = Inherited Roth Conversion IRA 
D = Account Type Is Not ToRA Eligible 
3. Requirements Changed for Existing Fields 
Requirements have been changed for the following fields: 
Field Name Location Modified requirement 
1. Beneficiary/Successor Owner 
Relationship Indicator 
(pertains to section related to 
529 Registration ) 
record 9B, start 41, end 41, 
length 1 
a) following condition has been removed: 
Required if Beneficiary/Successor Owner Address 
[[Option]] of ‘C’ is provided 
 
b) requirement has been changed from 
Optional/Conditional to Optional 

---

## Page 167

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q4 12/5/2011 167 
SUMMARY OF CHANGES–EFFECTIVE Q4 12/5/2011 
1. New Fields 
The following fields have been added to existing layouts: 
New Name Location Layout Section  
1. Original Deliverer Customer 
Account Number 
record 2, start 80, end 99, 
length 20 
ACATS record 018  Section 02.11.02 

---

## Page 168

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q2 2011 168 
SUMMARY OF CHANGES–EFFECTIVE Q2 2011 
1. New Fields 
The following fields have been added to existing layouts: 
New Name Location Layout Section  
1. Originating Receiver 
Customer Account Number at 
Firm  
record 6, start 78, end 97, length 
20 
ACATS Transfer (018) Section 02.11.01 
2. Originating Receiver Firm 
Number 
record 8, start 90, end 93, length 
4 
ACATS Transfer (018)  Section 02.11.01 
3. Originating Delivering Firm 
Number 
record 8, start 94, end 97, length 
4 
ACATS Transfer (018) Section 02.11.01 
2. Values or Comments Added to or Deleted from Existing Fields 
New values or comments have been added to the following fields: 
Field Name Location Added or Deleted Values or Comments 
1. Cost Basis [[Option]] Full Registration Record (401) 
Record 8, start 80, end 80, 
length 1 
Before change 
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

## Page 169

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q2 2011 169 
Field Name Location Added or Deleted Values or Comments 
2. Cost Basis [[Option]] ACATS Transfer (018) 
Record 10, start 80, end 80, 
length 1 
Before change 
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

## Page 170

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q1 2011 170 
SUMMARY OF CHANGES–EFFECTIVE Q1 2011 
1. Record Changed from Optional to Optional Conditional 
Record Location Current Requirement  Future Requirement 
Order Acknowledgment 
for Money Market 
Purchase (101) 
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
Exchange Confirmation (016)… Section 02.07.01 1 
Cash Adjustment (011) Section 02.08.01 1 
Reminders (080)… Section 02.17.01 1 

---

## Page 171

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q1 2011 171 
Layout Location Field applied 
Firm/TPA/Investment Agent/TPP 
Input Trailer (999) 
Section 02.18.01 3 
Settling Trades Detail (070)… Section 02.23.01 2 
Multiple Reject Codes (120)… Section 02.25.01 1 
Firm Exit (139)  Section 02.28.01 1 
Correction (003)… Section 02.29.01 1 
Full Registration (401) Section 02.10.01 1 
Retiring [[participant]] (090) Section 02.16.01 1 
3. Values or Comments Added to or Deleted from Existing Fields 
New values or comments have been added to the following fields: 
Field Name Location Added or Deleted Values or Comments 
1. Originator Type record 1, start 5, end 5, length 
1 
V = TPP (Third Party Provider) 
2. Record Type record 1, start 15, end 17, 
length 3 
Post-[[settlement]] Cancellation by Fund (140) or Post-
[[settlement]] Correction by Fund (026) is not permitted if 
the Security Issue Type field value is 63 and 
[[settlement]] Override Reason Code field value is 
space. 
3. Record Type  record 1, start 15, end 17, 
length 3 
Exchange Order is not permitted if the Security Issue 
Type field value is 63 and 
[[settlement]] Override Reason 
Code field value is space. 
4. Record Type record 1, start 15, end 17, 
length 3 
Exchange Confirmation, Exchange Reconfirmation 
and Post [[settlement]] Exchange Confirmation are not 
permitted if the Security Issue Type field value is 63 
and [[settlement]] Override Reason Code field value is 
space. 
5. Correction Indicator record 1, start 56, end 56, 
length 1 
P not permitted if the Security Issue Type field value is 
63 and [[settlement]] Override Reason Code field value 
is space. 
6. Transaction Code  record 1, start 58, end 59, 
length 2 
07 and 08 not permitted if the Security Issue Type field 
value is 63 and [[settlement]] Override Reason Code 
field value is space. 
7. Recipient Type record 1, start 84, end 84, 
length 1 
V = TPP (Third Party Provider) 
  

---

## Page 172

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q1 2011 172 
Field Name Location Added or Deleted Values or Comments 
8. Fund Account Indicator record 2, start 42, end 42, 
length 2 
0 = New account–U.S. 
1 = New account–non-U.S. 
2 = Existing account–U.S. 
3 = Existing account–non-U.S.  
9.Membership Identifier record 2, start 77, end 78, 
length 2 
03 = TPP (Third Party Provider) 
10. Anticipated [[settlement]] Date record 3, start 27, end 34, 
length 8 
mmddccyy 
For Security Type 63: 
Required if [[settlement]] Override Reason Code is 
space 
11. Branch Identification Number record 3, start 35, end 43, 
length 9  
Optional under the following conditions: 
• Membership Identifier = 01 or 02 and Agent for 
Firm Number is not provided. 
• Originator Type = V(TPP) 
12. Original Correction Indicator record 5, start 99, end 99, 
length 1 
P not permitted if the Security Issue Type field value is 
63 and [[settlement]] Override Reason Code field value 
is space. 
13. [[settlement]] Override Reason 
Code 
Record 1, start 79, end 80, 
length 2 
Must be space for settling EUR and GBP transactions 
(Security Issue Type 63 only). 
14.Currency Indicator Record 2, start 60, end 62, 
length 3 
EUR or GBP 
15.Currency Indicator—Debit Record 2, start 25, end 27, 
length 3 
EUR or GBP 
16.Currency Indicator—Credit Record 2, start 66, end 68, 
length 3 
EUR or GBP 
17.Correction/Exchange 
Indicator 
Record 1, start 56, end 56, 
length 1 
P, Y and Z not permitted if the Security Issue Type 
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

---

## Page 173

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q1 2011 173 
Layout Location Field applied 
Exchange Order (015) Section 02.06.01 1, 3 and 11 
Exchange Confirmation (016)… Section 02.07.01 4 and 9 
Cash Adjustment (011) Section 02.08.01 1 and 9 
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
record 1, start 85, end 88, 
length 4 
Required if: 
Originator Type = (T or A or V) 
OR 
Membership Identifier = 02 or 03 
2. TPA/Investment Agent/TPP 
Number 
record 1, start 85, end 88, 
length 4 
Required if: 
Originator Type = T or A or V 
3. TPA/Investment Agent/TPP 
Number 
record 1, start 85, end 88, 
length 4 
Required if Originator Type = T or P or A or V 
4. TPA/Investment Agent/TPP 
Number 
record 1, start 85, end 88, 
length 4 
Required if Originator Type = T or P or A or V 
OR 
Membership Identifier = 02 or 03 
5. TPA/Investment Agent/TPP 
Number 
record 1, start 85, end 88, 
length 4 
Required if Membership Identifier = 02 or 03 
6. Firm or TPA/Investment 
Agent/TPP Number 
record 1, start 85, end 88, 
length 4 
Firm Number when Recipient Type = T or V 
 
Otherwise, TPA/Investment Agent/TPP Number  

---

## Page 174

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q1 2011 174 
Field Name Location Modified requirement 
7. Agent for Firm Record 2, start 64, end 67, 
length 4 
Required if Originator Type = V 
8. Anticipated [[settlement]] Date record 3, start 27, end 34, 
length 8 
mmddccyy 
For Security Issue Type = 63, Required if [[settlement]] 
Override Reason Code is space  
 
Record layouts affected: 
Layout Location Field applied 
Order (001)  Section 02.01.01  4,7 and 8 
As-Of Order (004) Section 02.02.01 1,7 and 8 
Cash Adjustment (011) Section 02.08.01 1 
Full Registration (401) Section 02.10.01 3 and 7  
Settling Trades Detail (070) Section 02.23.01 6 
Firm Exit (139) Section 02.28.01 3 
Correction (003) Section 02.29.01 4,7 and 8 
Exchange Order (015) Section 02.06.01 4 and 7 
Exchange Confirmation (016) Section 02.07.01 5 
Extended Correction Transfer 
(200) 
Section 02.03.01 1 and 7 
Order Acknowledgment for 
Money Market Purchases (101) 
Section 02.03.01 2 and 7 
5. Reject Codes 
Fund/SERV 
The description of the following reject codes have been modified as part of the Third- Party Provider 
Enhancements: 
Reject 
Code 
New Description Old Description 
188 TPA/Investment Agent/TPP missing/invalid TPA/Investment Agent missing/invalid 
189 TPA/Investment Agent/TPP not authorized for 
firm 
TPA/Investment Agent not authorized for firm 
 

---

## Page 175

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q1 2011 175 
The following new reject codes have been added for the Third-Party Provider and the Multi-Currency 
Enhancements: 
Reject Code Description 
271 Agent for Firm missing/invalid  
272 EUR/GBP Settling Trade Date is less than the current Processing Date 
273 Non-USD [[settlement]] Submitting [[participant]] Number missing/invalid 
274 Non-USD [[settlement]] Contra [[participant]] Number missing/invalid 
275 Record Type not allowed for EUR and GBP settling transaction 
276 Settling Firm missing/invalid  

---

## Page 176

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Nov 2010 176 
SUMMARY OF CHANGES–EFFECTIVE NOV 2010 
1. New Fields 
The following fields have been added to existing layouts: 
New Name Location Layout Section  
3. Age Based Indicator record 2, start 82, end 82, length 
1 
Full Registration (401)  Section 02.10.01 
4. Age Based Roll Exempt 
Indicator 
record 2, start 83, end 83, length 
1 
Full Registration (401)  Section 02.10.01 
5. Customer/Owner U.S. 
Resident Alien Indicator 
record 2, start 84, end 84, length 
1 
Full Registration (401)  Section 02.10.01 
6. Successor Owner Indicator record 2, start 85, end 85, length 
1 
Full Registration (401)  Section 02.10.01 
2. Renamed Fields 
The following fields have been renamed: 
New Name Old Name Location 
1. Beneficiary/Successor Owner 
Date of Birth 
Beneficiary Date of Birth record 9b, start 8, end 15, length 8 
2. Beneficiary/Successor Owner 
Zip Code 
Beneficiary Zip Code record 9b, start 28, end 38, length 11 
3. Beneficiary/Successor Owner 
Name End Line Indicator 
Beneficiary Name End Line 
Indicator 
record 9b, start 39, end 39, length 1 
4. Beneficiary/Successor Owner 
Address [[Option]] 
Beneficiary Address [[Option]] record 9b, start 40, end 40, length 1 
5. Beneficiary/Successor Owner 
Relationship Indicator  
Beneficiary Relationship Indicator record 9b, start 41, end 41, length 1 
6. Beneficiary/Successor Owner 
SSN/EIN Number 
Beneficiary SSN/EIN Number record 9b, start 44, end 52, length 9 
7. Beneficiary/Successor Owner 
SSN/EIN Indicator 
Beneficiary SSN/EIN Indicator record 9b, start 53, end 53, length 1 
8. Beneficiary/Successor Owner 
U.S. Citizenship Indicator  
Beneficiary U.S. Citizenship 
Indicator 
record 9b, start 69, end 69, length 1 
9. Payable/Beneficiary/Successor 
Owner 1 Name/Address Line 1  
Payable/Beneficiary 1 
Name/Address Line 1 
record 10, start 8, end 42, length 35 
10. Payable/Beneficiary/Successor 
Owner 1 Name/Address Line 2  
Payable/Beneficiary 1 
Name/Address Line 2 
record 10, start 43, end 77, length 35 

---

## Page 177

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Nov 2010 177 
New Name Old Name Location 
11. Payable/Beneficiary/Successor 
Owner 1 Name/Address Line 3  
Payable/Beneficiary 1 
Name/Address Line 3 
record 11, start 8, end 42, length 35 
12. Payable/Beneficiary/Successor 
Owner 1 Name/Address Line 4  
Payable/Beneficiary 1 
Name/Address Line 4 
record 11, start 43, end 77, length 35 
13. Payable/Beneficiary/Successor 
Owner 1 Name/Address Line 5 
Payable/Beneficiary 1 
Name/Address Line 5 
record 12, start 8, end 42, length 35 
 
Record layouts affected: 
Layout Location Field applied 
Full Registration (401) Section 02.10.01 1 through 13 
3. Requirements Changed for Existing Fields 
Requirements have been changed for the following fields: 
Field Name Location Modified requirement 
1. Beneficiary/Successor Owner Zip 
Code 
record 9b, length 28, end 
38, length 11 
Changed Req/Opt from Optional Conditional to 
Optional. 
2. Beneficiary/Successor Owner 
Name End Line Indicator  
record 9b, length 39, end 
39, length 1 
Required if Beneficiary/Successor Owner 
Name/Address is provided. 
3. Beneficiary/Successor Owner 
Address [[Option]] 
record 9b, start 40, end 40, 
length 1 
Required if Beneficiary/Successor Owner Address 
[[Option]] of “C” is provided. 
4. Beneficiary/Successor Owner 
Relationship Indicator  
record 9b, start 41, end 41, 
length 1 
Required if Beneficiary/Successor Owner Address 
[[Option]] of “C” is provided. 
 
“2 = Other” was changed to “2=Non-Relative” 
5. Beneficiary/Successor Owner 
SSN/EIN Number 
record 9b, start 44, end 52, 
length 1 
Required if Beneficiary/Successor Owner Address 
[[Option]] of “C” or “D” is provided. 
6. Beneficiary/Successor Owner 
SSN/EIN Indicator 
record 9b, start 53, end 53, 
length 1 
Required if Beneficiary/Successor Owner SSN/EIN 
Number is provided. 
7. Beneficiary/Successor Owner 
U.S. Citizenship Indicator  
record 9b, start 69, end 69, 
length 1 
Required if Beneficiary/Successor Owner Address 
[[Option]] is “C” or “D”  
8. Payable/Beneficiary/Successor 
Owner 1 Name/Address Line 3 
record 11, start 8, end 42, 
length 35 
Change Req/Opt from Optional Conditional to 
Optional 

---

## Page 178

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Nov 2010 178 
Field Name Location Modified requirement 
9. Payable/Beneficiary/Successor 
Owner 1 City  
Record 12, start 43, end 75, 
length 33 
Change Req/Opt from Required to Required 
Conditional 
 
Optional if Successor Owner Indicator = 1 and 
Beneficiary/Successor Owner Address [[Option]] = “D”. 
Otherwise, this field is required. 
10. Payable/Beneficiary/Successor 
Owner 1 State  
Record 12, start 76, end 77, 
length 2 
Change Req/Opt from Required to Required 
Conditional 
 
Optional if Successor Owner Indicator = 1 and 
Beneficiary/Successor Owner Address [[Option]] = “D”. 
Otherwise, this field is required. 
 
Record layouts affected: 
Layout Location Field applied 
Full Registration (401) Section 02.10.01 1 through 10 
4. Reject Codes 
Fund/SERV 
The following reject codes have been changed as part of the Section 529 Enhancement: 
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

---

## Page 179

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Nov 2010 179 
Reject 
Code 
New Description Old Description 
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
 
The following new reject codes have been added for the Section 529 Enhancement:  
Reject Code Description 
267 Section 529 Age Based missing/invalid 
268 Section 529 Age Based Roll Exempt missing/invalid 
269 Section 529 Customer/Owner U.S. Resident Alien Indicator missing/invalid  
270 Section 529 Successor Owner Indicator missing/invalid 

---

## Page 180

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q4 2009 180 
SUMMARY OF CHANGES–EFFECTIVE Q4 2009 
1. New Fields 
The following fields have been added to existing layouts: 
New Name Location Layout Section  
1. Cost Basis Money Amount record 6, start 45, end 60, length 
16 
Order (001)  Section 02.01.01 
 record 7, start 45, end 60, length 
16 
As-Of Order (004)... Section 02.02.01 
  Correction (003)…  Section 02.29.01 
2. Earnings To Date Money 
Amount 
record 6, start 61, end 76, length 
16 
Order (001)  Section 02.01.01 
 record 7, start 61, end 76, length 
16 
As-Of Order (004)... Section 02.02.01 
  Correction (003)…  Section 02.29.01 
3. Negative Earnings To Date 
Indicator 
record 6, start 77, end 77, length 
1 
Order (001)  Section 02.01.01 
 record 7, start 77, end 77, length 
1 
As-Of Order (004)... Section 02.02.01 
  Correction (003)…  Section 02.29.01 
4. Fund Reject Code  record 2, start 77, end 79, length 
3 
Receiving Firm Exit from ToRA 
(214)… 
Section 02.04.01 
5. Delivering Fund Plan Type record 2, start 32, end 32, length 
1 
Fund Reject (100)… Section 02.05.01 
6. Uncollected [[shares]]  record 2, start 67, end 80, length 
14 
ToRA Acknowledgment (211)… Section 02.14.01 

---

## Page 181

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q4 2009 181 
2. Record Changed from Optional to Optional Conditional 
Record Location Current Requirement  Future Requirement 
Order (001) Section 02.01.01 Record 4 is required if the Country 
of Origin is required.  
Record 4 will now be required if 
one of the following fields are 
required: 
• Country of Origin 
• Periodic Frequency Indicator 
• IRA/529 [[liquidation]] Indicator 
• Beneficiary SSN/EIN Number  
Order (001) Section 02.01.01 Record 6 is required if the 
Redemption Fee Indicator is 
provided. It is not allowed if the 
Redemption Fee Indicator is not 
provided.  
Record 6 will now be required if 
the Redemption Fee Indicator is 
provided or the [[Asset]] Type 
Indicator = Q. 
As-Of Order (004) Section 02.02.01 Record 4 is required if the Sales 
Charge Rate is required or the 
Country of Origin is required (for 
Record Types 004, 007 and 009).  
Record 4 will now be required if 
one of the following fields are 
required: 
• Sales Rate Charge 
• Country of Origin (for Record 
Types 004, 007 and 009 only) 
• Periodic Frequency Indicator 
• IRA/529 [[liquidation]] Indicator 
• Beneficiary SSN/EIN Number  
Correction (003) Section 02.26.01 Record 4 is required if the Sales 
Charge Rate is required or the 
Country of Origin is required (for 
Record Type 003). 
Record 4 will now be required if 
one of the following fields are 
required: 
• Sales Rate Charge 
• Country of Origin (for Record 
Type 003 only) 
• Periodic Frequency Indicator 
• IRA/529 [[liquidation]] Indicator 
• Beneficiary SSN/EIN Number  
As-Of Order (004) 
Correction (003) 
Section 02.02.01 
Section 02.26.01 
Record 7 is required if the 
Redemption Fee Indicator is 
provided. It is not allowed if the 
Redemption Fee Indicator is not 
provided.  
Record 7 will now be required if 
the Redemption Fee Indicator is 
provided or the [[Asset]] Type 
Indicator = Q. 
Fund Reject (100) Section 02.05.01 Record 2 is required if the Fund 
Rejection Indicator = 2. 
 
Otherwise, this record type is 
optional. 
Record 2 will now be required if 
the Fund Rejection Indicator = 2 
or if Fund Reject Code = “704” 
(Fund Reject Record “100” only). 
 
Otherwise, this record type is 
optional. 

---

## Page 182

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q4 2009 182 
3. Renamed Fields 
The following fields have been renamed: 
New Name Old Name Location 
1. IRA/529 [[liquidation]] Indicator IRA [[liquidation]] Indicator record 4, start 71, end 71, length 1 
2. Original IRA/529 [[liquidation]] 
Indicator 
Original IRA [[liquidation]] Indicator record 11, start 71, end 71, length 1 
 
Record layouts affected: 
Layout Location Field applied 
Order (001)  Section 02.01.01 1 
As-Of Order (004)… Section 02.02.01 1 
Correction (003)… Section 02.29.01 1 and 2 
4. Values or Comments Added to or Deleted from Existing Fields 
New values have been added to the following fields: 
Field Name Location Added or Deleted Values or Comments 
1. Transaction Type  Record 1, start 57, end 57, 
length 1 
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
 
8 thru B only allowed if Transaction Code = “03” or 
“04” 

---

## Page 183

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q4 2009 183 
Field Name Location Added or Deleted Values or Comments 
2. [[Asset]] Type Indicator  Record 2, start 63, end 63, 
length 1 
0 = Not applicable 
1 = Current year payment 
2 = Prior year payment 
3 = IRA rollover 
4 = [[Asset]] transfer 
5 = Employee-prior year 
6 = Employee-current year 
7 = Employer-prior year 
8 = Employer-current year 
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
3. IRA/529 [[liquidation]] Indicator 
 
(Renamed from IRA [[liquidation]] 
Indicator, Effective Q4 2009) 
Record 4, start 71, end 71, 
length 1 
0 = Not applicable 
1 = Distribution-premature 
2 = Distribution-disability 
3 = Distribution-death 
4 = Distribution-normal 
5 = Hardship withdrawal 
6 = Loan 
7 = Rollover 
8 = Adjust prior year excess 
9 = Adjust current year excess 

---

## Page 184

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q4 2009 184 
Field Name Location Added or Deleted Values or Comments 
A = Qualified 
B = Non-Qualified 
 
A and B are required when Transaction Type = 8, 9, A 
or B 
(Effective Q4, 2009) 
4. Beneficiary Address [[Option]] 
Indicator 
Record 9B, start 40, end 40, 
length 1 
A = Primary IRA Beneficiary 
B = Secondary IRA Beneficiary 
C = 529 Beneficiary 
D = 529 Successor Owner 
G = Successor Trustee 
 
(Effective Q4, 2009) 
 
Record layouts affected: 
Layout Location Field applied 
Order (001) Section 02.01.01 1, 2 and 3 
As-Of Order (004)... Section 02.02.01 1, 2 and 3 
Full Registration (401) Section 02.10.01 4 
Correction (003)… Section 02.29.01 1, 2 and 3 
5. Reject Codes 
Fund/SERV 
The following reject code has been renamed to match the newly renamed IRA/529 [[liquidation]] Indicator:  
Reject Code Description 
106 IRA/529 [[liquidation]] Indicator missing/invalid  
 

---

## Page 185

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q4 2009 185 
The following new reject codes have been added for the Section 529 and ToRA Fields:  
Reject Code Description 
261 Cost Basis Money Amount missing/invalid  
262 Earnings To Date Money Amount missing/invalid 
263 Negative Earnings To Date Indicator missing/invalid 
264 ToRA Fund Reject Code missing/invalid  
265 ToRA Delivering Fund Plan Type missing/invalid 
266 ToRA Uncollected [[shares]] missing/invalid 
 
The following new reject codes have been added when the Fund(s) rejects the Section 529 transactions:  
Reject Code Description 
750 529–Over Investment  
751 (Exchange) Investment [[Option]] Changes Exceed Two Times per Year 
752 529 [[Asset]] Type Indicator Referenced for Non-529 Plan Account 

---

## Page 186

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q3 2009 186 
SUMMARY OF CHANGES–EFFECTIVE Q3 2009 
1. New Fields 
The following fields have been added to existing layouts: 
New Name Location 
1. As-Of Reason Code  record 3, start 79, end 80 length 2 
2. As-Of Reason Code record 3, start 79, end 80 length 2 
3. As-Of Reason Code record 2, start 78, end 79 length 2 
 
Record layouts affected: 
Layout Location Field applied 
Exchange Order (015)  Section 02.06.01 1 
Exchange Confirmation (016)... Section 02.07.01 2 
Firm Exit (139)  Section 02.28.01 3 
2. Record Changed from Optional to Required 
Layout Location Current Requirement  Future Requirement 
Firm Exit (139)  Section 02.28.01 Record 2 is required if Correction 
Indicator is equal to “P”. Otherwise, 
it is optional. 
Record 2 will now be required.  

---

## Page 187

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q3 2009 187 
3. Renamed Fields 
The following fields have been renamed: 
New Name Old Name Location 
1. As-Of Indicator Extended Correction Indicator record 3, start 84, end 84, length 1 
2. As-Of Reason Code  Extended Correction As-Of 
Reason Code 
record 3, start 85, end 86, length 2 
3. Correction Type Indicator Extended Correction Indicator record 3, start 84, end 84, length 1 
4. Correction Reason Code Extended Correction Reason 
Code 
record 3, start 85, end 86, length 2 
5. Original Correction Type 
Indicator 
Original Extended Correction 
Indicator 
record 10, start 80, end 80, length 1 
6. Original Correction Reason 
Code 
Original Extended Correction As-
Of Reason Code 
record 10, start 81, end 82, length 2 
 
Record layouts affected: 
Layout Location Field applied 
As-Of Order (004)… Section 02.02.01 1 and 2 
Correction (003)… Section 02.29.01 3, 4, 5 and 6 

---

## Page 188

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q3 2009 188 
4. Values or Comments Added to or Deleted from Existing Fields 
New values have been added to the following fields: 
Field Name Location Added or Deleted Values or Comments 
1. As-Of Reason Code  Record 3, start 85, end 86, 
length 2 
01 = Incorrect Firm/Fund Account Number 
02 = Incorrect Share Quantity/Dollar Quantity 
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
The values ‘00’, ‘06’ and ‘08’ have been removed. 
2. Extended Correction Reason 
Code 
Record 1, start 58, end 59, 
length 2 
01 = Incorrect Firm/Fund Account Number 
02 = Incorrect Share Quantity/Dollar Quantity 
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
The values ‘06’ and ‘08’ have been removed. 
3. Correction Reason Code Record 3, start 85, end 86, 
length 2 
01 = Incorrect Firm/Fund Account Number 
02 = Incorrect Share Quantity/Dollar Quantity 
03 = Incorrect security issue [[ID]] 
04 = Customer renege 
05 = Incorrect Sales Charge Breakpoint 

---

## Page 189

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q3 2009 189 
Field Name Location Added or Deleted Values or Comments 
07 = Blue sky violation 
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
Record 10, start 81, end 82, 
length 2 
01 = Incorrect Firm/Fund Account Number 
02 = Incorrect Share Quantity/Dollar Quantity 
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
The values ‘00’, ‘06’ and ‘08’ have been removed. 
 
Record layouts affected: 
Layout Location Field applied 
As-Of Order (004)… Section 02.02.01 1 
Extended Correction (200)… Section 02.03.01 2 
Correction (003)… Section 02.29.01 3 and 4 

---

## Page 190

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Q3 2009 190 
5. Reject Codes 
The following new reject codes have been added. They can be used by the fund when rejecting ToRA records.  
Reject 
Code 
Description 
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

## Page 191

Fixed Length Record Layouts (Part 1) 
Summary of changes–effective Dec 2008 191 
SUMMARY OF CHANGES–EFFECTIVE DEC 2008 
1. New Fields 
The following fields have been added to existing layouts: 
New Name Location 
1. Customer SSN/EIN Number record 8, start 78, end 86, length 9 
2. ACATS Account Type record 8, start 87, end 88, length 2 
3. Gift/Donation Indicator record 8, start 89, end 89, length 1 
 
Record layouts affected: 
Layout Location Field applied 
ACATS Transfer (018) Section 02.11.01  1,2,3 
2. New Values to Existing Fields 
Note: 
This change is already in effect 
New values have been added to the following fields: 
Field Name Location New Values 
1. SSN/EIN Indicator Record 2, start 70, end 70, 
length 1 
2 = [[investor]] TIN/EIN 
 
Record layouts affected: 
Layout Location Field applied 
ACATS Transfer (018) Section 02.11.01  1 

---

## Page 192

 
 
© 2023 [[DTCC]]. All rights reserved. [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: August 30, 2023 
Publication Code: MFS312 
Service: Fund/SERV® 
Title: Fixed Length Record Layouts (Part 1) 
   