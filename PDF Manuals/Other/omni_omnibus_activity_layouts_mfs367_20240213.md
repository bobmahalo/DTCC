---
title: "Networking - Omni/SERV: Omnibus Activity Record Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/omni_omnibus_activity_layouts_mfs367_20240213.pdf"
pages: 33
size: "495.8 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Networking - Omni/SERV: Omnibus Activity Record Layouts

**Original File:** [omni_omnibus_activity_layouts_mfs367_20240213.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/omni_omnibus_activity_layouts_mfs367_20240213.pdf)  
**Category:** Other  
**Total Pages:** 33  
**File Size:** 495.8 KB  

---

## Page 1

 
 
 
Networking – Omni/SERV 
OMNIBUS ACTIVITY RECORD LAYOUTS 
FEBRUARY 13, 2024 
 

---

## Page 2

Omnibus Activity Record Layouts 
 
History of Changes 2 
 
TABLE OF CONTENTS 
History of Changes .............................................................................................................................................. 3 
Record Layouts .................................................................................................................................................... 4 
Omnibus Activity Records .................................................................................................................................. 5 
Omnibus Activity File – Header Record .............................................................................................................. 5 
Omnibus Activity File – Detail Record ................................................................................................................ 7 
Omnibus Activity File - Trailer Record ..............................................................................................................25 
Omnibus Activity File – Grand Total Trailer Record .........................................................................................27 
Input Records’ Layout ....................................................................................................................................... 28 
Omnibus Activity File Datatrak Header .............................................................................................................28 
Omnibus Activity File Datatrak Trailer ..............................................................................................................29 
Output Records’ Layout .................................................................................................................................... 30 
Omnibus Activity Output Header File (N00) .....................................................................................................30 
APPENDIX – Summary of Changes .................................................................................................................. 31 
Effective Q1, 2019 ............................................................................................................................................31 
Effective Q3, 2017 ............................................................................................................................................31 
Effective Q2, 2016 ............................................................................................................................................31 
Effective Q4, 2015 ............................................................................................................................................32 
Effective Q3, 2012 ............................................................................................................................................32 
 
 
 

---

## Page 3

Omnibus Activity Record Layouts 
 
History of Changes 3 
 
HISTORY OF CHANGES 
Effective Dates Description 
02/13/2024 Document rebranded with 2023 version. 
0815/2022 Document links changed 
03/25/2019 New reject code added – X8, See Important Notice a8658 Dated 12/16/2018 
07/24/2017 New field added – DSAMAT, See Important Notice a8408  
06/15/2016 New fields added: 
• Transaction Date Received – DSAOED  
• Transaction Time Received – DSAOET  
• Money Market [[Liquidity]] Fee/Redemption Gate Indicator – DSAMMI  
• Sub Account Aggregated Order Indicator – DSAAOI  
• Individual Money Market Fee/Redemption Gate – DSAIMI  
• Individual Aggregated Order Indicator – DSAIAO  
 
Field modified: 
• Filler – DSAPDC  
 
See Important Notice a8211  
10/13/2015 New field added – DSAPGI, Important Notice a8097  
08/13/2012 New field added – DSATAG, Important Notice a7470 
07/15/2011 Important Notice a7246 
06/14/2010 Creation of new Omnibus Activity and Position files, Important Notice a6948 Dated 02/18/2010 
 
 

---

## Page 4

Omnibus Activity Record Layouts 
 
Record Layouts 4 
 
RECORD LAYOUTS 
The following are Networking Omnibus Activity Record Layouts. The column headings are as follows:  
Field Name The name of the field 
Start The position in which the field starts 
End The position in which the field ends 
Len The length of the field in bytes 
Description Field description (format, valid values, conditional requirements, etc.) 
Reject  Code The Networking reject code value used indicates the reason the field is invalid.  
  
All fields are character format, alpha/numeric:  
• All dollar, price, and share fields include the decimal point, [[DO]] not include commas, and are right justified, 
blank-filled. 
• [[shares]]  are always 3 decimal places. 
• Dollar and share fields will include a stated negative sign if the transaction type is a debit to the balance. 
For example,  the dollars and [[shares]] sold on redemption will be negative as will a purchase reversal. 
• Prices can have from 0 to 9 decimal  positions 
• All dates are in ccyymmdd format. (March 15, 2022, for example, would be represented as 20220315) 
• Percent  fields include the decimal point and [[DO]] NOT include commas or the % sign 
 
 
 

---

## Page 5

Omnibus Activity Record Layouts 
 
Omnibus Activity Records 5 
 
OMNIBUS ACTIVITY RECORDS 
Omnibus Activity File – Header Record 
• Required record 
• Input from Firm to [[NSCC]] 
• Output from [[NSCC]] to Fund if accepted, to Firm if rejected 
 
The Omnibus Activity Header record is used to introduce a series of Omnibus Activity Detail records for a 
particular fund. 
Omnibus Activity File - Header Record 
Field Name Start End Len Description Opt/ 
Req 
Reject 
Code 
Record Type 
RECTYP 
1 3 3 ‘HDR’ – Header Record R 02 
Filler 
DSAHPD1 
4 64 61 Space O  
Filler 
DSAHCNT 
65 72 8 Space O  
Filler 
DSAHPD2 
73 560 488 Space O  
Submitting Firm Number 
DSAHFRM 
561 564 4 Must be valid [[NSCC]] [[participant]] 
Number 
R 03 
Filler 
DSAHFNM 
565 604 40 Firm Name O  
Filler 
DSAHDBN 
605 606 2 database number O  
Filler 
DSAHDBD 
607 614 8 database name O  
Receiving Fund Number 
DSAHRFND 
615 618 4 Must be valid [[NSCC]] [[participant]] 
Number 
R 04 
Filler 
DSAHPD3 
619 1075 457 Space O  

---

## Page 6

Omnibus Activity Record Layouts 
 
Omnibus Activity Records 6 
 
Field Name Start End Len Description Opt/ 
Req 
Reject 
Code 
Filler 
DSAHSIT 
1076 1078 3 [[ID]] O  
Event Name 
DSAHEVN 
1079 1086 8 Event Name that created the file 
The name of the event that created the 
file. 
O  
Last Production Date 
DSAHLPD 
1087 1094 8 ccyymmdd R K2 
Posting date 
DSAHPOS 
1095 1102 8 ccyymmdd 
Production Date. Posting date 
(PR3POS) of the PR3 detail records. 
R K2 
Current System Date 
DSAHSYD 
1103 1110 8 ccyymmdd R K2 
Filler 1111 1625 515 Space O  
[[NSCC]] Reject Indicator 1626 1626 1 Input: Space 
Output: 
0 = Accepted by [[NSCC]]  
 
1 = Rejected by [[NSCC]] 
R  
[[NSCC]] Reject Code 1 1627 1628 2 Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 2 1629 1630 2 Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 3 1631 1632 2 Input: Space 
Output: Reject code or space 
R  
 
  

---

## Page 7

Omnibus Activity Record Layouts 
 
Omnibus Activity Records 7 
 
Omnibus Activity File – Detail Record 
• Required record 
• Input from Firm to [[NSCC]] 
• Output from [[NSCC]] to Fund if accepted, to Firm if rejected 
 
Omnibus Activity File - Detail Record 
Field Name Start End Len Description 
ROA Group 
DSAROA 
1 20 20 ROA Group 
Account Number 
DSAACT 
21 40 20 The [[Broker]] [[ID]] number (BIN) for the client account. 
Pricing Rules 
DSARUL 
41 43 3 Pricing Rules 
Trade Date 
DSATRD 
44 51 8 ccyymmdd 
Trade Date 
Sort Order 
DSASRT 
52 53 2 Sort Order 
Fund Symbol 
DSAFND 
54 59 6 Fund [[ID]] used by the Firm. Normally Fund Symbol. 
Transaction Code 
DSACOD 
60 62 3 This is the Transaction Code of the Omnibus Service 
Provider. Contact the firm if you need the code description. 
Batch [[ID]] 
DSAIDN 
63 82 20 Batch [[ID]] 
Gross Amount Received 
DSARCV 
83 98 16 9999999999999.99 
Gross Amount Received on a purchase or [[Dividend]] 
reinvestment. Will be equal Gross Dollar Amount if no 
purchase fees. 
Purchase Fee 1 
DSAPF1 
99 114 16 9999999999999.99 
This fee is a general purchase fee, based on the amount 
stored in each fund’s fee table. 
Purchase Fee 2 
DSAPF2 
115 130 16 9999999999999.99 
This fee is for federal or NRA withholding on [[Dividend]] 
reinvestments. 

---

## Page 8

Omnibus Activity Record Layouts 
 
Omnibus Activity Records 8 
 
Field Name Start End Len Description 
Gross Dollar Amount 
DSAGRS 
131 146 16 9999999999999.99 
Gross Dollar Amount 
Dealer Commission Amount 
DSADLR 
147 162 16 9999999999999.99 
[[underwriter]] Commission Amount 
 
DSAUND 
163 178 16 9999999999999.99 
If the commission was indirect, fronted by the fund, the 
portion that was fronted is carried as a negative amount on 
an original purchase. 
Therefore, the total DSADLR + DSAUND is always the 
commission that was paid by the shareholder. 
FCA prior amount invested 
DSAFCA 
179 194 16 9999999999999.99 
FCA prior amount invested 
Net Dollar Amount 
DSANET 
195 210 16 9999999999999.99 
Net Dollar Amount 
NAV 
DSANAV 
211 226 16 9999999999999.99 
NAV 
Offer Price 
DSAOFF 
227 242 16 9999999999999.99 
Offer Price 
[[shares]] 
DSASHR 
243 259 17 9999999999999.999 
[[shares]] 
Resulting Share Balance 
DSABAL 
260 276 17 9999999999999.999 
If an account/fund has multiple transactions in a day, the 
resulting balance (DSABAL) is the balance after each 
transaction. The ending balance for the day will be on the 
record with the highest serial number (DSASER). 
[[Dividend]] Share Balance 
DSADIV 
277 293 17 9999999999999.999 
[[Dividend]] Share Balance 
Redemption Fee 1 
DSARF1 
294 309 16 9999999999999.99 
This is a general redemption fee, based on the amount stored 
in each fund's fee table. 
Redemption Fee 2 
DSARF2 
310 325 16 9999999999999.99 
This is a general redemption fee. 
Redemption Fee 3 
DSARF3 
326 341 16 9999999999999.99 
This is a general redemption fee. 

---

## Page 9

Omnibus Activity Record Layouts 
 
Omnibus Activity Records 9 
 
Field Name Start End Len Description 
Redemption Fee 4 
DSARF4 
342 357 16 9999999999999.99 
This is used for state tax withholding on redemptions. 
Redemption Fee 5 
DSARF5 
358 373 16 9999999999999.99 
This fee is for federal or NRA withholding on cash dividends 
or redemptions. 
Redemption Fee 6 
DSARF6 
374 389 16 9999999999999.99 
These fees are deducted from the proceeds of redemption. 
This fee is either a CDSC fee or a short-term trading (STR) 
fee. If the value in the DSARFN field (byte 1426) is 6, this is a 
short-term trading 
fee. Otherwise, this is a CDSC fee. 
Net Redemption Ck Amount 
DSANCK 
390 405 16 9999999999999.99 
Net Redemption Ck Amount 
Total Sales Charge Paid 
DSATOP 
406 412 7 Total Sales Charge Paid by the Shareholder 
Dealer Load Percent 
DSADLP 
413 419 7 If the commission was indirect for a Jumbo purchase and the 
commission was ‘blended,’ the dealer load % will be the 
starting breakpoint for blending. 
[[underwriter]] Load Percent 
DSAUNP 
420 426 7 [[underwriter]] Load % 
Serial Posting Number 
DSASER 
427 436 10 Serial posting number, which is a unique transaction [[ID]] 
assigned to every transaction. 
Account Trans Sequence Number 
DSAASQ 
437 442 6 Account Trans Sequence Number 
Account Trans Sub Sequence 
Number 
DSAASB 
443 444 2 Account Trans Sub Sequence Number 
Posting Date 
DSAPOS 
445 452 8 ccyymmdd 
Posting Date 
[[settlement]] Date 
DSASET 
453 460 8 ccyymmdd 
[[settlement]] Date 
[[Dividend]] Date 
DSADVD 
461 468 8 ccyymmdd 
[[Dividend]] Date 

---

## Page 10

Omnibus Activity Record Layouts 
 
Omnibus Activity Records 10 
 
Field Name Start End Len Description 
FROM/TO Account Number on 
Transfer 
DSAAC2 
469 482 14 The FROM or the TO account number on a transfer 
FROM/TO Account Number on 
Exchange 
DSAFD2 
483 488 6 The FROM or the TO fund [[ID]] on an exchange. 
[[Broker]] Of Record 
DSABRK 
489 493 5 [[Broker]] Of Record 
Branch Of Record 
DSABRN 
494 498 5 Branch Of Record 
Rep Of Record 
DSAREP 
499 513 15 Rep Of Record 
Management Company Code 
DSAMGT 
514 517 4 This is the Management Company Code of the Omnibus 
Service Provider. Contact the firm for specific information. 
Buy/Sell Indicator 
DSABOS 
518 518 1 Trade buy or sell indicator 
As-Of/Cancel Trade Indicator 
DSARAC 
519 519 1 As of or Cancel trade indicator 
DSAPGI 520 523 4 Program Indicator. 
DSAMAT 524 527 4 Managed Account Type 
Timer Of Record 
DSATIM 
528 532 5 Timer Of Record 
Timers Account Number 
DSATMA 
533 546 14 Timers ACCT Number 
Affiliate Of Record 
DSAAFF 
547 551 5 Affiliate Of Record 
Affiliates Account Number 
DSAAFA 
552 565 14 Affiliates ACCT Number 
Wholesaler Of Record 
DSAWHL 
566 570 5 Wholesaler Of Record 
As-Of Reason Code 571 574 4 As-of reason code, which is a user defined code that 
describes the reason why a transaction is processed as-of. 

---

## Page 11

Omnibus Activity Record Layouts 
 
Omnibus Activity Records 11 
 
Field Name Start End Len Description 
DSAREA 
Supplemental [[Asset]] Number 
DSASUP 
575 584 10 Supplemental [[Asset]] Number 
Filler 
DSANAM 
585 634 50 Space 
[[Dividend]] Number 
DSADVN 
635 640 6 [[Dividend]] Number 
Reconciliation Batch 
DSARCN 
641 655 15 Reconciliation Batch 
Contribution Year 
DSAYER 
656 659 4 Contribution Year 
Federal Withholding Percent 
DSAFWH 
660 664 5 99.99 
Federal Withholding Percent 
State Withholding Percent 
DSASWH 
665 669 5 99.99 
State Withholding Percent 
Adjust Available [[shares]] 
DSAAVL 
670 670 1 Y = Adjust for available [[shares]] 
Filler 
DSAPD4 
671 671 1 Pad Bytes 
Check Number 
DSACHK 
672 683 12 Check Number 
Load Table 
DSALDT 
684 686 3 Load Table 
Pricing Code 
DSAPRI 
687 687 1 Pricing Code. Valid values are: 
N = No load  
S = Share 
D = Dollar  
E = VIP 
V = Volume discount  
C = CDSC 
L = LOI 
P = Breakpoint  

---

## Page 12

Omnibus Activity Record Layouts 
 
Omnibus Activity Records 12 
 
Field Name Start End Len Description 
R = ROA 
I = Extended, already priced 
F = FCA purchase with blended rates  
X = Reversal 
Y = Reversal of FCA purchase 
Print Suppress Flag 
DSADEL 
688 688 1 Print Suppress Flag 
[[Liquidate]] All [[shares]] Flag 
DSALIQ 
689 689 1 [[Liquidate]] All [[shares]] Flag 
Adjustment Flag 
DSAADJ 
690 690 1 Adjustment Flag 
Pending Redemption [[shares]] Pass 
Over 
DSAOVR 
691 691 1 Pending Redemption [[shares]] Pass Over 
Share-Dollar Code 
DSASDI 
692 692 1 Share-Dollar Code 
Rounding Code 
DSARND 
693 693 1 Rounding Code 
A = CDSC - fee waived (round up) 
B = CDSC - fee waived (round down) 
D = Down - Round down to the next full share amount 
F = Full and fractional - [[DO]] not round [[shares]]; instead, use the 
number of [[shares]] calculated by dividing the dollar amount of 
the transaction by the price 
N = CDSC - net dollar transaction 
S = CDSC - share transaction, waive CDSC fee  
T = Net Dollar transaction 
U = Up - Round up to the next full share amount 
X = CDSC - Net dollar transaction, waive CDSC fee 
W = CDSC - Dollar transaction, waive CDSC fee 
Payment Method Code 
DSAPMT 
694 694 1 Payment Method Code 
Payee Number 
DSAPAY 
695 697 3 Payee Number 
 
 

---

## Page 13

Omnibus Activity Record Layouts 
 
Omnibus Activity Records 13 
 
Field Name Start End Len Description 
Blue Sky State 
DSASKY 
698 699 2 Blue Sky State 
NRA Country Code 
DSANRA 
700 701 2 Non-Resident Alien Country Code. Note that the code UC 
indicates a US citizen with a foreign address. 
Refer to the IRS w eb site and view a list of NRA country 
codes. 
Expense/Income Code 
DSAEXP 
702 703 2 Expense/Income Code 
Campaign [[ID]] 
DSACMP 
704 713 10 Campaign [[ID]] 
Account Type 
DSAMAS 
714 716 3 Contact the firm for their codes and descriptions. 
Original Serial Number Reversed 
DSARVS 
717 726 10 Original Serial Number Reversed. This is populated only for 
reversal transactions. 
Original ASQ Number Reverse 
DSARVQ 
727 732 6 Original ASQ Number Reverse. This is populated only for 
reversal transactions. 
Original ASB Number Reverse 
DSARVB 
733 734 2 Original ASB Number Reverse. This is populated only for 
reversal transactions. 
Journal Record Number Of Trade 
DSAJRC 
735 742 8 Journal Record Number Of This Trade 
Filler 
DSAPD1 
743 748 6 Space 
Certificate Number 
DSACER 
749 758 10 Certificate Number 
Wire Order Number 
DSAORD 
759 768 10 Wire Order Number 
ABA Number 
DSAABA 
769 777 9 ABA Number 
Contra Code 
DSACON 
778 780 3 Contra Code 
Commission Paid/Deducted 
DSACOM 
781 781 1 Commission Paid/Deducted 

---

## Page 14

Omnibus Activity Record Layouts 
 
Omnibus Activity Records 14 
 
Field Name Start End Len Description 
Transaction Type 
DSABIN 
782 784 3 Transaction Types: 
AR - Reversals & Adjustments  
CI - Certificate Issues 
CS - Certificate Surrenders  
DC - Dividends - Cash 
DL - Dollar-Only Transactions  
DR - Dividends - Reinvested  
FD - Redemptions - Full - Direct 
PC - Cancellations - W/O Purchases  
PD - Purchases - Direct 
PO - Purchases - Wire Orders 
PS - Settlements - Wire Order Purchases  
RC - Cancellations - Wire Order Redempts  
RD - Redemptions - Partial - Direct 
RO - Redemptions - Wire Orders 
RS - Settlements - Wire Order Redempts  
SH - Share-Only Transactions 
TP - Transfers - Purchase Side  
TR - Transfers - Redemption Side  
XP - Exchanges - Purchase Side 
XR - Exchanges - Redemption Side 
 
Ending numeric value 0-9 can be variable at the Firm 
database level. (For example: PD0, PD9, RD1, DR0, etc.) 
Input Screen 
DSASCR 
785 787 3 Input Screen 
Filler 
DSAERR 
788 791 4 Space 
Filler 
DSAMRK 
792 792 1 Space 
ROA Basis 
DSABAS 
793 808 16 9999999999999.99 
The dollar amount used to determine the breakpoint for a 
purchase. It is the “better of” an active LOI amount, the firm 
supplied ROA value (DSAROV) or the sub-accounting 
provider-calculated ROA value. If no value is supplied, this 
field is set to 0.00, right-justified. 

---

## Page 15

Omnibus Activity Record Layouts 
 
Omnibus Activity Records 15 
 
Field Name Start End Len Description 
LOI Amount 
DSALOI 
809 824 16 9999999999999.99 
LOI Amount 
Filler 
DSALNK 
825 825 1 Space 
Pricing Method 
DSAMTH 
826 826 1 Pricing Method 
Filler 
DSAPAD 
827 833 7 Space 
Additional Info in JN2 
DSAADD 
834 834 1 Additional Information In JN2. 
Contact the firm if you need the code descriptions 
Purchase Fee Code 1 
DSAPC1 
835 837 3 Transaction code that identifies the type of fee in this field. 
Contact the firm if you need the code descriptions. 
Purchase Fee Code 2 
DSAPC2 
838 840 3 Transaction code that identifies the type of fee in this field. 
Contact the firm if you need the code descriptions. 
Redemption Fee Code 1 
DSARC1 
841 843 3 Transaction code that identifies the type of fee in this field. 
Contact the firm if you need the code descriptions. 
Redemption Fee Code 2 
DSARC2 
844 846 3 Transaction code that identifies the type of fee in this field. 
Contact the firm if you need the code descriptions. 
Redemption Fee Code 3 
DSARC3 
847 849 3 Transaction code that identifies the type of fee in this field. 
Contact the firm if you need the code descriptions. 
Redemption Fee Code 4 
DSARC4 
850 852 3 Transaction code that identifies the type of fee in this field. 
Contact the firm if you need the code descriptions. 
Redemption Fee Code 5 
DSARC5 
853 855 3 Transaction code that identifies the type of fee in this field. 
Contact the firm if you need the code descriptions. 
Redemption Fee Code 6 
DSARC6 
856 858 3 Redemption Fee Code 6. Transaction code that identifies the 
type of fee in this field. Contact the firm if you need the code 
descriptions. 
ZIP Code 
DSAZIP 
859 868 10 ZIP Code 
State 
DSASTA 
869 870 2 State 

---

## Page 16

Omnibus Activity Record Layouts 
 
Omnibus Activity Records 16 
 
Field Name Start End Len Description 
Sort Name 
DSASNA 
871 882 12 Sort Name 
Withhold Type Code 
DSAWIT 
883 883 1 Withhold type code 
VIP Code 
DSAVIP 
884 884 1 An alpha value (A-Z), except N (not a VIP), identifies an 
account as a VIP and gives NAV pricing. A numeric value 1-9 
identifies an account as a VIP but does not give NAV pricing. 
The specific descriptions are defined by the firm. 
Social Code 
DSASOC 
885 886 2 Refer to the [[DTCC]] Learning Center for Social Codes at  
https://dtcclearning.com/documents/mutual-fund-
services-1/mfs-cross-product/codes-8/2498-social-
codes/file.html 
Suppress Mail 
DSAMAI 
887 887 1 Suppress Mail 
Dup Stmt Address 
DSADPS 
888 890 3 Dup Stmt address On File 
Telephone Redemptions 
DSATEL 
891 891 1 Tele Redemptions? 
Telephone Exchanges 
DSAEXC 
892 892 1 Tele Exchanges? 
Filler 
DSAPD2_1 
893 898 6 PAD 
Serial Number of Exchange 
/Transfer 
DSAPD2_SER2 
899 908 10 Serial Number of the other side of an exchange (XR/XP) or 
transfer (TR/TP) 
Filler 
DSAPD2_2 
909 912 4 PAD 
Network Control Indicator 
DSANCI 
913 913 1 Network Control Indicator 
External Control Number Type 
DSAXCT 
914 916 3 External Control Number Type 
Filler 
DSAPD9 
917 917 1 Space 

---

## Page 17

Omnibus Activity Record Layouts 
 
Omnibus Activity Records 17 
 
Field Name Start End Len Description 
External Control Number 
DSATCK 
918 937 20 External Control Number 
Dealer Account Number 
DSADLA 
938 957 20 Dealers Acct Number 
Purchase Code 
DSATA1 
958 958 1 Code to indicate if purchase is initial or subsequent. 
I = Initial 
S = Subsequent R = Reopen 
Source Of Funds Code 
DSATA2 
959 959 1 Source Of Funds Code 
Suppress Trans On Statement 
Indicator 
DSATA3 
960 960 1 Suppress Trans On Statement? 
NTF Flag 
DSATA4 
961 961 1 NTF Flag 
As-Of Correction Override to Error 
Account Processing DSATA5 
962 962 1 As of correction override to error account processing: 
B = bypass send to fund as of 
E = include in error account but send as of order 
Special Aggr Method 
DSATA6 
963 963 1 Special Aggr Meth 0-9, A-Z 
Transaction Attribute 7 
DSATA7 
964 964 1 Transaction Attribute 7, OMNIORDER Reportable Flag 
Transaction Attribute 8 
DSATA8 
965 965 1 Transaction Attribute 8 
Transaction Attribute 9 
DSATA9 
966 966 1 Transaction Attribute 9 
Transaction Attribute 10 
DSATA10 
967 967 1 Transaction Attribute 10 
Transaction Attribute 11 
DSATA11 
968 968 1 Transaction Attribute 11 
Systematics Disposition 
DSATA12 
969 969 1 Systematics Disposition: 
A = deactivate SWP/SPP 
B = move + deactivate SWP/SPP 

---

## Page 18

Omnibus Activity Record Layouts 
 
Omnibus Activity Records 18 
 
Field Name Start End Len Description 
C = move SWP/SPP - no deactivate  
D = move + deactivate SWP 
E = move SWP - no deactivate  
F = move + deactivate SPP 
G = move SPP - no deactivate 
H = move SWP/SPP if not active on target - deactivate 
SWP/SPP  
N or blank = no action 
Internal Control Number Type 
DSAICT 
970 972 3 Internal Control Number Type 
PHO = Telephone  
FAX = FAX 
BFS = Fund/SERV 
LOI = Letter of instruction  
FIL = Interface trade file  
WIR = Same-day wire 
ERC = Client trade that went through error account  
ERR = Offset to ERC in the error account 
ERD = Offset to cash div sell or reinvest div buy 
ERB = Offset to break cover trade 
Control Number Of Fund Order 
DSAICN 
973 988 16 Control number of fund order, f part of a fund order. 
OMNIORDER Sequence Number 
DSAOSQ 
989 989 1 OMNIORDER Sequence Number 
Filler 
DSAVDB_1 
990 997 8 Space 
[[NSCC]] Transaction Type Code 
DSAVDB_TRNTYP 
998 998 1 [[NSCC]] transaction type code submitted on the order. 
 
Valid values for this field can be found on the [[DTCC]] 
Fund/SERV Order 001 record layout 
 
https://dtcclearning.com/products-and-services/mutual-
fund-services/fund-serv.html  
 
Select “Fund/SERV® Record Layouts” under ON THIS 
PAGE, “Variable”, “Fund/SERV Variable Record Layouts 
– Part I” and navigate to Order Record 001 --> 
“Transaction Type” field in byte position 61. 

---

## Page 19

Omnibus Activity Record Layouts 
 
Omnibus Activity Records 19 
 
Field Name Start End Len Description 
Filler 
DSAVDB_1B 
999 1003 5 N/A Spaces 
IRA/DCP Indicator On Order 
DSAVDB_IRADCP 
1004 1004 1 IRA/DCP indicator submitted on the order. 
 
Valid values for this field can be found on the [[DTCC]] 
Fund/SERV Order 001 record layout 
 
https://dtcclearning.com/products-and-services/mutual-
fund-services/fund-serv.html 
 
Select “Record Layouts”, “Fund/SERV”, “Fund/SERV 
Variable Record Layouts – Part I” and navigate to Order 
Record 001 --> “[[Asset]] Type Indicator” field in byte 
position 160. 
Filler 
DSAVDB_2 
1005 1006 2 Space 
CDSC Waiver Reason Code On 
Order 
DSAVDB_CDSC_WVR_RSN 
1007 1007 1 CDSC waiver reason code submitted on the order. 
 
Valid values for this field can be found on the [[DTCC]] 
Fund/SERV Order 001 record layout 
 
https://dtcclearning.com/products-and-services/mutual-
fund-services/fund-serv.html  
— 
Select “Record Layouts”, “Fund/SERV”, “Fund/SERV 
Variable Record Layouts – Part I” and navigate to Order 
Record 001 --> “[[liquidation]] Indicator” field in byte 
position 267. 
NAV Reason Code On Order 
DSAVDB_NAV_RSN 
1008 1008 1 NAV reason code submitted on the order. 
 
Valid values for this field can be found on the [[DTCC]] 
Fund/SERV Order 001 record layout 
 
https://dtcclearning.com/products-and-services/mutual-
fund-services/fund-serv.html 
 
Select “Record Layouts”, “Fund/SERV”, “Fund/SERV 
Variable Record Layouts – Part I” and navigate to Order 
Record 001 --> “NAV Reason Code” field in byte position 
268. 

---

## Page 20

Omnibus Activity Record Layouts 
 
Omnibus Activity Records 20 
 
Field Name Start End Len Description 
IRA/529 [[liquidation]] Indicator 
DSAVDB_IRALIQ 
1009 1009 1 IRA/529 [[liquidation]] Indicator submitted on the order. 
 
Valid values for this field can be found on the [[DTCC]] 
Fund/SERV Order 001 record layout 
 
https://dtcclearning.com/products-and-services/mutual-
fund-services/fund-serv.html 
 
Select “Record Layouts”, “Fund/SERV”, “Fund/SERV 
Variable Record Layouts – Part I” and navigate to Order 
Record 001 --> “IRA/529 [[liquidation]] Indicator” field in 
byte position 354. 
Filler 
DSAVDB_3 
1010 1021 12 Space 
Number Of Days For SWP 
Resubmit 
DSARSB 
1022 1022 1 Number Of Days For SWP Resubmit 
[[Dividend]]/Capital Gain [[Option]] 
DSADCO 
1023 1023 1 '1'=CC (Cash/Cash) 
'2'=RR (Reinvest/Reinvest) 
'3'=CR(Cash/Reinvest)  
'4'=RC(Reinvest/Cash) 
[[settlement]] Date Override 
DSASOR 
1024 1024 1 'D' = RD Overridden For [[Broker]] Directed [[settlement]] 
'I' = PD Should Inherit Settle Date Of RD 
'P' = PD Should Be Assigned Trade Of RD Settle-1 
Fund Override Trade Date 
DSAFTD 
1025 1032 8 Fund Override Trade Date 
Override Share/Dollar Indicator 
DSAOSD 
1033 1033 1 Override Share/Dollar Indicator 
Trading Method 
DSATDM 
1034 1034 1 Trading Method 
Fee Indicator 
DSAFNF 
1035 1035 1 Fee/No Fee Indicator 
Prime Mix Sequence Number 
DSAPMS 
1036 1043 8 Prime Mix Sequence Number 
Mix Class 1044 1046 3 Mix Class 

---

## Page 21

Omnibus Activity Record Layouts 
 
Omnibus Activity Records 21 
 
Field Name Start End Len Description 
DSAPMC 
Allocation Percentage 
DSAPMA 
1047 1049 3 Allocation Percentage 
Number Of Original Transactions 
DSAPMO 
1050 1052 3 Number Of Original Transactions 
Prime Mix Pad 
DSAPMP 
1053 1055 3 Prime Mix Pad 
Filler 
DSAIVT 
1056 1058 3 Space 
Filler 
DSAIVS 
1059 1062 4 Space 
Filler 
DSAIVB 
1063 1094 32 Space 
Filler 
DSASST 
1095 1097 3 Space 
Representative name 
DSARN1 
1098 1137 40 Representative name 
Filler 
DSAHPAD 
1138 1146 9 Pad Bytes 
Filler 
DSAMPAD 
1147 1151 5 Pad Bytes 
Beneficiary Tax [[ID]] 
DSABTX 
1152 1162 11 Beneficiary Tax [[ID]]. This field may be left blank 
Omnibus Account Number 
Indicator 
DSAOAI 
1163 1163 1 DSA omnibus account indicator for DSABAN field 
(1164:1183). 
<blank> = DSABAN field is not populated. 
1 = DSABAN field contains the fund account number. 
2 = DSABAN field contains the [[Broker]] account number. 
Omnibus Account Number 
DSABAN 
1164 1183 20 DSAOAI field (1163:1163) setting indicates whether value is 
fund account number or [[Broker]] account number. 
Estimated Pricing Run 
DSAEST 
1184 1184 1 Estimated Pricing Run (Y/blank) 

---

## Page 22

Omnibus Activity Record Layouts 
 
Omnibus Activity Records 22 
 
Field Name Start End Len Description 
Filler 
DSAPD5 
1185 1185 1 Pad Bytes 
Clearing/Settling [[Broker]] 
DSACSB 
1186 1190 5 Clearing/Settling [[Broker]] 
Error Account Number 
DSAERA 
1191 1204 14 Error Acct Number 
Original Control Number 
DSAOCN 
1205 1224 20 Original Control Number 
Override withholding rate 
DSANOR 
1225 1230 6 Override withholding rate 
Basis Indicator 
DSABSI 
1231 1231 1 Basis Indicator 
Security Issue [[ID]] 
DSACUS 
1232 1240 9 Security Issue [[ID]] 
Currency Code 
DSACNC 
1241 1243 3 Currency Code 
E-Commerce User [[ID]] 
DSAEUI 
1244 1253 10 E-Commerce User [[ID]] 
Gross [[settlement]] Indicator 
DSAGSI 
1254 1254 1 Gross [[settlement]] Indicator 
JN3 File Indicator 
DSAJN3 
1255 1255 1 JN3 File Indicator (Y/N) 
Sub Load Table Number 
DSALVL 
1256 1258 3 Sub Load Table Number 
Breakpoint Number within Load 
Table 
DSABPN 
1259 1260 2 Breakpoint Number within Load Table 
Original ICN From OMNIORDER 
DSAOMN 
1261 1275 15 Original ICN from OMNIORDER 
Internal cross reference to link an error account cover trade 
back to an underlying client trade 
Account Cost Basis 
DSAESC 
1276 1291 16 9999999999999.99 
Account Cost Basis 

---

## Page 23

Omnibus Activity Record Layouts 
 
Omnibus Activity Records 23 
 
Field Name Start End Len Description 
Account Market Value 
DSAMKT 
1292 1307 16 9999999999999.99 
Account Market Value. Populated only for ESA accounts 
Calculated ROA Value 
DSAROS 
1308 1323 16 9999999999999.99 
Calculated ROA value 
[[Broker]]-Supplied ROA Value 
DSAROV 
1324 1339 16 9999999999999.99 
[[Broker]]-supplied ROA value 
Error Batch [[ID]] 
DSAEBI 
1340 1351 12 Error Batch [[ID]] 
Amount of Waived STR Fee 
DSAWST 
1352 1367 16 9999999999999.99 
Amount of Waived STR fee 
Exchange Differential Load Level 
DSAXLV 
1368 1368 1 Exchange differential load level 
Free [[Entitlement]] Dollars 
DSAFED 
1369 1384 16 9999999999999.99 
Free [[Entitlement]] Dollars 
Free [[Entitlement]] [[shares]] 
DSAFES 
1385 1401 17 9999999999999.999 
Free [[Entitlement]] [[shares]] 
STR Fee Rate 
DSARFR 
1402 1408 7 STR Fee Rate 
STR Fee Liable [[shares]] 
DSARFS 
1409 1425 17 9999999999999.999 
STR fee liable [[shares]] 
STR Fee Bucket Number 
DSARFN 
1426 1426 1 STR fee bucket number (RF Number) 
Tax [[ID]]/ SSN 
DSATAX 
1427 1437 11 Tax [[ID]] or SSN. The number is formatted with dashes (-). 
Transaction Date Received 
DSAOED 
1438 1445 8 Transaction Date Received. Non-business dates 
permitted.  
ccyymmdd format. 
Transaction Time Received 
DSAOET 
1446 1449 4 Transaction Time Received  
hhmm format (military time) 
Money Market [[Liquidity]] 
Fee/Redemption Gate Indicator 
DSAMMI 
1450 1450 1 Money Market [[Liquidity]] Fee/Redemption Gate Indicator. 
From the incoming order record. 
Valid values are B, F or <blank> 

---

## Page 24

Omnibus Activity Record Layouts 
 
Omnibus Activity Records 24 
 
Field Name Start End Len Description 
Sub Account Aggregated Order 
Indicator 
DSAAOI 
1451 1451 1 Sub Account Aggregated Order Indicator (Omnibus 
Trade) 
Individual Money Market 
Fee/Redemption Gate 
DSAIMI 
1452 1452 1 Individual Money Market Fee/Redemption Gate 
Individual Aggregated Order 
Indicator 
DSAIAO 
1453 1453 1 Individual Aggregated Order Indicator 
Filler 
DSAPDC 
1454 1473 20 Space 
TPA Number 
TPAID 
1474 1477 4 Third party administrator [[ID]] Number 
Bank/Trust [[ID]] Number 
TRSTID 
1478 1481 4 Bank/Trust [[ID]] Number 
Alternate ([[NSCC]]) Branch [[ID]] 
BRNALT 
1482 1490 9 Alternate ([[NSCC]]) Branch [[ID]] 
CIP Government [[ID]] type 
DSAGIT 
1491 1494 4 Free form description of the following [[ID]] field. 
CIP Government [[ID]] Number 
DSAGOV 
1495 1514 20 CIP Government [[ID]] Number 
User Defined Data 
DSAUSR 
1515 1601 87 User defined data 
Fund Symbol 
DSAUSR_FNDSYM 
1602 1607 6 Fund Symbol 
Fund [[ID]] at Fund 
DSAUSR_FNDFND 
1608 1613 6 Fund [[ID]] at Fund 
Representative last name 
DSAUSR_REPSNA 
1614 1623 10 Representative last name 
Filler 
DSAUSR_FILL2 
1624 1632 9 Space 
 

---

## Page 25

Omnibus Activity Record Layouts 
 
Omnibus Activity Records 25 
 
Omnibus Activity File - Trailer Record 
• Required record 
• Input from Firm to [[NSCC]] 
• Output from [[NSCC]] to Fund if accepted, to Firm if rejected 
 
The Omnibus Activity Trailer record is used to recap the Activity Detail records for a particular fund. 
 
Omnibus Activity File - Trailer Record 
Field Name Start End Len Description Opt/ 
Req 
Reject 
Code 
Record Type RECTYP 1 3 3 ‘TRL’ – Trailer Record R 02 
Filler 
DSATPD1 
4 64 61 Space O  
Total Activity Record Count 
DSATCNT 
65 72 8 99999999 
Number of records included in the file 
Total count of all detail records. No 
header or trailer records are included. 
O  
Filler 
DSATPD2 
73 560 488 Space O  
Submitting Firm Number 
DSATFRM 
561 564 4 Must be valid [[NSCC]] [[participant]] Number R 03 
Filler 
DSATFNM 
565 604 40 Space O  
Filler 
DSATPAD 
605 615 11 Space O  
Receiving Fund Number 
DSATRFND 
616 619 4 Must be valid [[NSCC]] [[participant]] Number R 04 
Filler 620 1625 1006 Space O  
[[NSCC]] Reject Indicator 
NSCC_REJ_IND 
1626 1626 1 Input: Space Output: 
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]] 
R  

---

## Page 26

Omnibus Activity Record Layouts 
 
Omnibus Activity Records 26 
 
Field Name Start End Len Description Opt/ 
Req 
Reject 
Code 
[[NSCC]] Reject Code 1 
NSCC_REJ_COD1 
1627 1628 2 Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 2 
NSCC_REJ_COD2 
1629 1630 2 Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 3 
NSCC_REJ_COD3 
1631 1632 2 Input: Space 
Output: Reject code or space 
R  
 
 
  

---

## Page 27

Omnibus Activity Record Layouts 
 
Omnibus Activity Records 27 
 
Omnibus Activity File – Grand Total Trailer Record 
Optional Input record from Firm to [[NSCC]] 
Required Output record from [[NSCC]] to Fund if accepted, to Firm if rejected. 
This record is used to recap all Omnibus Activity records, including headers and trailers, for a [[participant]]’s 
entire transmission. 
Omnibus Activity File – Grand Total Trailer Record 
Field Name Start End Len Description Opt/ 
Req 
Record Type 
DSARID 
1 3 3 ‘GRT’ – Grand Total Trailer Record R 
Filler 4 64 61 Space O 
Total Activity Record Count 
DSAGCN 
65 72 8 99999999 
Number of records included in the file (including 
Headers and Trailers) 
Total count of all records in the file except the 
DATATRAK header (HDR.S) and the DATATRAK 
trailer (END.S) 
R 
Filler 73 560 488 Space O 
Submitting Firm Number/ 
Recipient Number 
DSAGFRM 
561 564 4 Submitting Firm Number on Input from Firm to 
[[NSCC]]; 
Recipient Number on Output from [[NSCC]] to 
[[participant]] 
R 
Filler 565 1632 1068 Space O 
 

---

## Page 28

Omnibus Activity Record Layouts 
 
Input Records’ Layout 28 
 
INPUT RECORDS’ LAYOUT 
Omnibus Activity File Datatrak Header 
Input from Firm to [[NSCC]] 
Omnibus Activity File Datatrak Header 
Field Name Start End Len Type Description Opt/ 
Req 
Literal 1 5 5 A/N Value 'HDR.S' R 
DATATRAK SYSID 6 10 5 A/N Value ‘26943’ R 
Literal 11 16 6 A/N Value '.E00.C' R 
Originator 17 20 4 A/N Clearing/Settling firm number assigned by the 
[[NSCC]]. 
R 
Literal 21 22 2 A/N Value '.S' R 
Sub Originator 23 26 4 A/N Clearing/Settling firm number assigned by the 
[[NSCC]]. 
R 
Processing Date 27 34 8 N mmddccyy R 
File Description 35 59 25 A/N Value ‘NETW OMNI ACTIVITY INPUT’ R 
Multi Batch Indicator 60 60 1 A/N N = Not last batch  
Y = Last batch 
R 
Multi Batch Number 61 63 3 N  R 
Filler 64 1632 1569 A/N Space R 
 
  

---

## Page 29

Omnibus Activity Record Layouts 
 
Input Records’ Layout 29 
 
Omnibus Activity File Datatrak Trailer 
Input from Firm to [[NSCC]] 
Omnibus Activity File Datatrak Trailer  
Field Name Start End Len Type Description Opt/ 
Req 
Literal1 1 5 5 A/N Value 'END.S' R 
DATATRAK SYSID 6 10 5 A/N Value ‘26943' R 
Literal2 11 16 6 A/N Value '.E00.C' R 
Originator 17 20 4 A/N Clearing/settling firm number assigned by the 
[[NSCC]]. 
R 
Literal3 21 22 2 A/N Value '.S' R 
Sub Originator 23 26 4 A/N Clearing/settling firm number assigned by the 
[[NSCC]]. 
R 
Data File Record Count 
TOTAL_RECS 
27 33 7 N DATATRAK Header & Trailer not included in 
count 
Total count of all records in the file except the 
DATATRAK header (HDR.S) and the 
DATATRAK trailer (END.S). 
R Filler 34 1632 1599 A/N Space R 
 
 

---

## Page 30

Omnibus Activity Record Layouts 
 
Output Records’ Layout 30 
 
OUTPUT RECORDS’ LAYOUT 
Omnibus Activity Output Header File (N00) 
Omnibus Activity Output Header File (N00) 
Field Name Start End Len Type Description 
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N 00 = Output Header 
Sequence Number 4 5 2 A/N 01 
MRO Recipient Number 6 9 4 N  
Literal 10 20 11 A/N Value '11111111111' 
Transmission Date 21 28 8 N mmddccyy 
Autoroute File [[ID]] 29 36 8 A/N Value '02100943' 
Literal 37 54 18 A/N Value 'NETW OMNI ACTIVITY' 
Filler 55 1632 1578 A/N Space 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 31

Omnibus Activity Record Layouts 
 
APPENDIX – Summary of Changes 31 
 
APPENDIX – SUMMARY OF CHANGES 
Effective Q1, 2019 
Reject Codes 
The following new [[NSCC]] reject code will be utilized to reject transactions that fail O -code validation:  
Reject Code Description 
X8 [[participant]] is not valid for the Submitter and/or Product  
Effective Q3, 2017 
New Field 
Omnibus Activity File – Detail Record 
Field Name Start End Len Description 
DSAMAT 524 527 4 Managed Account Type 
 
Effective Q2, 2016 
New Fields 
Omnibus Activity File – Detail Record 
Field Name Start End Len Description 
Transaction Date Received 
DSAOED 
1438 1445 8 Transaction Date Received. Non-business dates permitted. 
ccyymmdd format. 
Transaction Time Received 
DSAOET 
1446 1449 4 Transaction Time Received hhmm format (military time) 
Money Market [[Liquidity]] 
Fee/Redemption Gate Indicator 
DSAMMI 
1450 1450 1 Money Market [[Liquidity]] Fee/Redemption Gate Indicator. 
From the incoming order record. 
Valid values are B, F or <blank> 
Sub Account Aggregated Order 
Indicator 
DSAAOI 
1451 1451 1 Sub Account Aggregated Order Indicator (Omnibus Trade) 
Individual Money Market 
Fee/Redemption Gate 
DSAIMI 
1452 1452 1 Individual Money Market Fee/Redemption Gate 

---

## Page 32

Omnibus Activity Record Layouts 
 
APPENDIX – Summary of Changes 32 
 
Field Name Start End Len Description 
Individual Aggregated Order 
Indicator 
DSAIAO 
1453 1453 1 Individual Aggregated Order Indicator 
 
Modified Field 
Omnibus Activity File – Detail Record 
Field Name Start End Len Description 
Filler 
DSAPDC 
1454 1473 20 Space 
 
Effective Q4, 2015 
New Field 
Omnibus Activity File – Detail Record 
Field Name Start End Len Description 
DSAPGI 520 523 4 Program Indicator. 
Effective Q3, 2012 
New Field 
Omnibus Activity File – Detail Record 
Field Name Start End Len Description 
DSATAG 520 523 4 User defined 

---

## Page 33

 
 
© 2024 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation [[DTCC]].  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: February 13, 2024 
Publication Code: MFS367 
Service: Networking – Omni/SERV 
Title: Omnibus Activity Record Layouts  
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 