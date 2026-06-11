---
title: "Fund Settlement MRO Specification"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs178_fund_sett_mro_spec_20231024.pdf"
pages: 18
size: "355.0 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# Fund Settlement MRO Specification

**Original File:** [mbs178_fund_sett_mro_spec_20231024.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs178_fund_sett_mro_spec_20231024.pdf)  
**Category:** MBSD  
**Total Pages:** 18  
**File Size:** 355.0 KB  

---

## Page 1

 
Fixed Income Clearing Corporation 
FUND [[settlement]] MRO SPECIFICATION 
VERSION 1.2.0 
OCTOBER 24, 2023 
 

---

## Page 2

 
 
TABLE OF CONTENTS 
Introduction to the Documentation ..................................................................................................................... i 
Fund [[settlement]] MRO Specification .................................................................................................................... i 
Audience .............................................................................................................................................................. i 
Distribution ......................................................................................................................................................... i 
Related Materials ................................................................................................................................................. i 
JSON .................................................................................................................................................................. i 
[[FICC]] ................................................................................................................................................................... i 
Version Control Information ................................................................................................................................. i 
1. JSON Messaging Guidelines .......................................................................................................................... 2 
Overview ............................................................................................................................................................. 2 
Message Structure .............................................................................................................................................. 2 
Message Header ............................................................................................................................................... 2 
Blocks and Sub-blocks ...................................................................................................................................... 2 
Fields ................................................................................................................................................................. 3 
2. Communications .............................................................................................................................................. 4 
3. Detail Message Specifications ........................................................................................................................ 5 
Message Format Guidelines ............................................................................................................................... 5 
Formatting Rules ............................................................................................................................................... 5 
Message Rules ................................................................................................................................................ 5 
Message Field Rules ....................................................................................................................................... 5 
Formatting Conventions .................................................................................................................................... 6 
Funds [[settlement]] Message for End of Day ........................................................................................................ 7 
Appendix A: Message Samples ........................................................................................................................ 11 
 

---

## Page 3

Fund [[settlement]] MRO Specification 
 
Introduction to the Documentation 1 
INTRODUCTION TO THE DOCUMENTATION 
Fund [[settlement]] MRO Specification 
This document provides an overview of Funds [[settlement]] MRO specifications (output) that will be used to support 
MBS Fund [[settlement]]. 
Audience 
This document was written for systems and development personnel, including managers, analysts and 
programmers. It presumes readers are familiar with technical concepts and terms, understand JSON Messaging 
specifications and have a [[BASIC]] understanding of the products and services of the Mortgage Backed [[securities]] 
Division (MBSD) of the Fixed Income Clearing Corporation ([[FICC]]). 
Distribution 
MBSD Clearing Members 
Related Materials 
JSON 
The specifications are based on JSON messages. Readers are therefore strongly urged to refer to JSON user 
documentation to obtain a complete and comprehensive understanding of these message standards. JSON 
information (including many applicable message formats) can also be found at http://www.json.org/. 
[[FICC]] 
For additional information regarding RTTM®, readers can refer to documentation found on dtcclearning.com for 
MBSD. 
 
Version Control Information 
Date Version Number Name Description of Changes 
07/28/2022 1.0 E. Badalov Initial draft 
11/21/2022 1.1 E. Badalov Updated FAC in Appendix A from “factor_update_adjustment-
FAC":"0.00”, to “factor_update_adj-FAC":"0.00", 
10/24/2023 1.2 E.Badalov Updated Message Samples in Appendix A as follows: 
1) created timestamps to reflect the morning hours 
creation time 
2) [[settlement]] date to match the business date 
 

---

## Page 4

 
1.  JSON Messaging Guidelines 2 
1. JSON MESSAGING GUIDELINES 
This section of the document provides some background information that may be useful for interpreting the 
detailed message specifications that follow. 
Overview 
[[FICC]] has adopted the JSON message formats for machine readable output associated with MBS fund [[settlement]] 
instructions. [[FICC]] uses a proprietary network for communication between MBS and its Members. 
Message Structure 
JSON is a text format that is completely language independent but uses conventions that are familiar to virtually 
all modern programming languages. These properties make JSON an ideal data-interchange language. 
JSON message formats are constructed using a modular methodology based on the premise that information can 
be identified and programmed once, then reused wherever needed. Using this approach, data is configured into 
logical groups (i.e., TAG identified fields and blocks) according to business purpose.  
Message Header 
The Message Header contains the message identifier and is populated as a continuous string of data. 
Blocks and Sub-blocks 
A block may be defined as a group of fields containing related business information that is framed by start-of-
block and end-of-block designators. The use of a block is not restricted to any given message; it can be reused 
across a number of messages and combined with other blocks to fulfill a variety of business requirements.  
Each message generated by [[FICC]] contains one main block and several sub-blocks for each business line. These 
blocks may be mandatory or optional within a particular message, and are structured as follows: 
• A start-of-block designator (represented by the tag “ { ”), indicating the start of a group of related information. 
• An end-of-block designator (represented by the tag “ } ”), indicating the end of a group of related information. 
 
An information block may be further divided into sub-blocks containing groups of fields that further define the 
block. The structure of a sub-block is the same as that of a block, the difference being that it is “nested” or 
contained within the block. For example, each business line will contain the tag and the value of that tag would be 
sub-blocks of that business Details block. Sub-blocks, under certain circumstances, can be repeated in a block. 
  

---

## Page 5

 
1.  JSON Messaging Guidelines 3 
Fields 
At a minimum, each field is composed of an identifying tag and its associated field data with colon as a delimiter. 
A tag contains a start and end double-quote and will end with a colon (“ : ”). The field data also contains a start and 
end double-quote as a string value unless it is a start of sub-block as in the case of business line. The format for 
field data is a string of alpha-numerics. Each field is separated from the next field by a separator character 
comma (“ , ”). 

---

## Page 6

 
2.  Communications 4 
2. COMMUNICATIONS 
Members receive files containing JSON formatted records from [[DTCC]] via [[DTCC]]’s Common Data Transfer 
System (CDTS).  
Product IDs for each file: 
Filename Production UAT 
MBS [[EOD]] MRO 14016000 14986000 
 
 

---

## Page 7

Fund [[settlement]] MRO Specification 
3. Detail Message Specifications 5 
3. DETAIL MESSAGE SPECIFICATIONS 
This section contains the detailed specification for the Funds [[settlement]] Machine Readable Output (MRO). 
Message Format Guidelines 
Formatting Rules 
The following Message and Message Field rules apply to all messages in the Funds-Only [[settlement]] (FOS) 
Message Specification: 
Message Rules 
1. Direction: Messages are sent from [[FICC]] FOS. 
 
2. Variable Length: All messages can vary in length up to a maximum allowable number of characters per 
message type. 
 
3. Header: All messages begin with a standard fixed-length header that will identify the start of the message, 
business date and deposit account. 
 
4. Trailer: All messages end with a standard fixed-length trailer that identifies the end of the message. 
 
5. Message Fields: A message is composed of one or more message fields. 
 
6. Character Set: A-Z, a-z, 0-9, white space and the following punctuation " : / { } [ ] - " 
 
7. Field Delimiter: The field delimiter sequence is Carriage Return Line Feed , “CRLF” (ASCII Character 13, 
ASCII Character 10). This sequence immediately follows the data. 
Message Field Rules 
1. Field Tag: Each field begins with a field tag. 
 
2. Tag Delimiter: Each tag is prefixed and suffixed by the double-quote “ “ ” and ends with a colon “:” (e.g., 
“dep_acct”:). 
 
3. Field Data: Field data immediately follows the tag suffix delimiter. 
 
4. Data Format: Data conforms to format rules.    

---

## Page 8

Fund [[settlement]] MRO Specification 
3. Detail Message Specifications 6 
Formatting Conventions 
Please note that all the layouts for the JSON messages (included in this Section of the document) are 
organized using the following columns of data: 
 
Column Heading Description 
M/O/R The M/O/R column defines whether the field is always M- Mandatory, or is R – 
Mandatory if block is present or O- Optional block.  
Tag The Tag column defines the exact tag value that must precede the field. Tags are 
always delimited by “:” (meaning a “:” would be the character immediately before and 
after the tag). 
Field Description The Field Description column provides a text description of the purpose or use of a data 
field. 
Data Format The Data Format column specifies the size and characters allowed within a data field.  
 
The following characters may appear in the Data Format Column or in any discussion of data format and 
content: 
Character Meaning Example 
 
Example Usage 
a Upper Case Alpha Characters 6a ABCDEF 
c Alphanumeric Characters (upper case only) 6c AB12EF 
d Decimal Number (decimal period) 15d 2035.45 
e Space 1e (1blank space) 
n Numeric Characters 8n 19950131 
x Any Printable ASCII Symbol 20x Anytime & Anyplace 
/ The literal “/” as a separator 6a/2a AB12EF/NY 
[ ] Optional element format [/4c] [optional data] 
[-] Optional “sign” (negative) format [-] : “total_funds”:”-5.45” 
! Fixed length field 12!c ABCDEFGHIJKL 
 
All fields are, by definition, variable in length with a maximum field size specified, unless a fixed length format is 
defined by inclusion of the “!”, in which case the size specified is the fixed field size. In the case where the data 
value in the fixed length field is smaller than the field size specified, the data should be left justified with trailing 
blanks. 
 
 

---

## Page 9

Fund [[settlement]] MRO Specification 
3. Detail Message Specifications 7 
Funds [[settlement]] Message for End of Day 
This section includes the detailed specification for the end of day Funds [[settlement]] MRO message 
M/O/R Tag Field Description Data Format 
                                                                            Message Header 
M Fund_Settlement_EOD_Header_ Header will include date and destination 
account 
YYYYMMDD_8!c 
M  { Block Start  
M  “dep_acct”: MBS [[participant]] [[ID]] “8!c”, 
M  “created_ts”: Message Created Timestamp “YYYYMMDDHHMMSS”, 
 M “bus_dt”: Message Business Date  “YYYYMMDD”, 
M “stl_dt”: [[settlement]] Date  “YYYYMMDD”, 
M “total_funds”: Cash obligation that will be either 
credited (positive number) or debited 
(negative number) from deposit account. 
This is the sum of net totals of mbs_total 
“[-]15d”, 
O “mbs_funds”: MBS Funds details for each 
[[participant]]/aggregate as repeating block 
 
R  [ Repeat Block Start  
R  { Block Start  
R “part_agg”: MBS [[participant]]/aggregate [[ID]] “8c”, 
R “factor_update_adj-FAC”: Cash obligation that is associated with 
Factor Update adjustment payment for 
[[participant]]/aggregate  
“[-]15d”, 
R “principal-PRN”: Cash obligation that is associated with 
Principal payment for 
[[participant]]/aggregate  
“[-]15d”, 
R “interest-INT”: Cash obligation that is associated with 
Interest payment for 
[[participant]]/aggregate  
“[-]15d”, 
R “tmpg_charges-TMP”: Cash obligation that is associated with 
TMPG payment for [[participant]]/aggregate  
“[-]15d”, 
R “tmpg_financing_amount-TMF”: Cash obligation that is associated with 
TMPG finance payment for 
[[participant]]/aggregate  
“[-]15d”, 
R “cpr_claims-CPR”: Cash obligation that is associated with 
CPR claim payment for 
[[participant]]/aggregate  
“[-]15d”, 

---

## Page 10

Fund [[settlement]] MRO Specification 
3. Detail Message Specifications 8 
M/O/R Tag Field Description Data Format 
R “broker_commissions-CMS”: Cash obligation that is associated with 
[[Broker]] commissions payment for 
[[participant]]/aggregate  
“[-]15d”, 
R “tba_net_tap-TBA”: Cash obligation that is associated with 
TBA NET TAP payment for 
[[participant]]/aggregate  
“[-]15d”, 
R “do_not_allocate-DNA”: Cash obligation that is associated with 
DNA TAP payment for 
[[participant]]/aggregate  
“[-]15d”, 
R “reprice-RPC”: Cash obligation that is associated with 
TBA REPRICE TAP payment for 
[[participant]]/aggregate  
“[-]15d”, 
R “variance-VAR”: Cash obligation that is associated with 
VARIANCE TAP payment for 
[[participant]]/aggregate  
“[-]15d”, 
R “poolnet_tap-TAP”: Cash obligation that is associated with 
PoolNet TAP payment for 
[[participant]]/aggregate  
“[-]15d”, 
R “expanded_poolnet_tap-EXP”: Cash obligation that is associated with 
Expanded PoolNet TAP payment for 
[[participant]]/aggregate  
“[-]15d”, 
R “clearance_adjustment-CLA”: Cash obligation that is associated with 
Clearance adjustment TAP payment for 
[[participant]]/aggregate  
“[-]15d”, 
R “mbsd_billing_fee-FEE”: Cash obligation that is associated with 
MBS billing fee payment for 
[[participant]]/aggregate  
“[-]15d”, 
R “settlement_billing_charge-SMT”: Cash obligation that is associated with 
MBS [[settlement]] charge payment for 
[[participant]]/aggregate  
“[-]15d”, 
R “tba_int_exp-TEM”: Cash obligation that is associated with 
interest exposure on Failed TBA trades 
for [[participant]]/aggregate  
“[-]15d”, 
R “tba_int_exp_adj-ATM”: Cash obligation that is associated with 
adjustment to interest exposure on Failed 
TBA trades for [[participant]]/aggregate  
“[-]15d”, 
R “pool_int_exp-PEM”: Cash obligation that is associated with 
interest exposure on Failed Pool 
[[obligations]] for [[participant]]/aggregate  
“[-]15d”, 
R “pool_int_exp_adj-ALM”: Cash obligation that is associated with 
adjustment to interest exposure on Failed 
Pool [[obligations]] for 
[[participant]]/aggregate  
“[-]15d”, 

---

## Page 11

Fund [[settlement]] MRO Specification 
3. Detail Message Specifications 9 
M/O/R Tag Field Description Data Format 
R “pool_prin_adj-APM”: Cash obligation that is associated with 
adjustment to par on interest paid for 
[[participant]]/aggregate  
“[-]15d”, 
R “pool_fail_mtm-PFM”: Cash obligation that is associated with 
failing pool [[obligations]] [[mark-to-market]] 
payment for [[participant]]/aggregate  
“[-]15d”, 
R “tba_fwd_mtm-MTM”: Cash obligation that is associated with 
forward TBA trades [[mark-to-market]] 
payment for [[participant]]/aggregate  
“[-]15d”, 
R “pool_fail_int-PIM”: Cash obligation that is associated with 
accrued interest for current month on 
failed pool [[obligations]] for 
[[participant]]/aggregate  
“[-]15d”, 
R “tba_fail_int-TIM”: Cash obligation that is associated with 
accrued interest for current month on 
failed TBA trades for 
[[participant]]/aggregate  
“[-]15d”, 
R “tba_fail_mtm-MFM”: Cash obligation that is associated with 
failing TBA trades [[mark-to-market]] 
payment for [[participant]]/aggregate  
“[-]15d”, 
R “pool_tap_mtm-PTM”: Cash obligation that is associated with 
Pool TAP [[mark-to-market]] payment for 
[[participant]]/aggregate  
“[-]15d”, 
R “mark_return-MRR”: Cash obligation that is associated with 
net value of mark return from payment 
for [[participant]]/aggregate  
“[-]15d”, 
R “mark_return_interest-MRI”: Cash obligation that is associated with 
interest on net value of mark collected on 
payment for [[participant]]/aggregate  
“[-]15d”, 
R “margin_tap-MGN”: Cash obligation that is associated with 
[[Margin]] on future TAP payment for 
[[participant]]/aggregate  
“[-]15d”, 
R “margin_tap_return-MGR”: Cash obligation that is associated with 
[[Margin]] tap return from payment for 
[[participant]]/aggregate  
“[-]15d”, 
R “margin_tap_return_interest-MGI”: Cash obligation that is associated with 
interest on [[Margin]] tap collected on 
payment for [[participant]]/aggregate  
“[-]15d”, 
O “miscellaneous_adjustments”: Cash obligation that is associated with 
miscellaneous payment for 
[[participant]]/aggregate 
“[-]15d”, 
O “miscellaneous_reason”: Miscellaneous reason description “200x”, 
R “mbs_part_total”: MBS Net total for [[participant]]/aggregate “[-]15d” 

---

## Page 12

Fund [[settlement]] MRO Specification 
3. Detail Message Specifications 10 
M/O/R Tag Field Description Data Format 
R } Block End  [,] 
R ] Repeat Block End  
R } Block End   
                                                                        Message Trailer 
M Fund_Settlement_EOD_Trailer_ Trailer will include date and destination 
account 
 YYYYMMDD_8!c 
 

---

## Page 13

Fund [[settlement]] MRO Specification 
Appendix A: Message Samples 11 
APPENDIX A: MESSAGE SAMPLES 
a. Sample of [[EOD]] mro with two MBS aggregates for business date of Aug 30, 2018 
 
Fund_Settlement_EOD_Header_20180830_000PART1 
 { 
  "dep_acct":"000PART1", 
  "created_ts":"20180830053536", 
  "bus_dt":"20180830", 
  "stl_dt":"20180830", 
  "total_funds":"39000564.25", 
  "mbs_funds":[ 
        { 
          "part_agg":"MBSA1", 
          "factor_update_adj-FAC":"0.00", 
"principal-PRN":"0.00", 
"interest-INT":"0.00", 
"tmpg_charges-TMP":"0.00", 
"tmpg_financing_amount-TMF":"0.00", 
"cpr_claims-CPR":"0.00", 
"broker_commissions-CMS":"0.00", 
"tba_net_tap-TBA":"1000000.00", 
"do_not_allocate-DNA":"-23000.00", 
"reprice-RPC":"10000.00", 
"variance-VAR":"0.25", 
"poolnet_tap-TAP":"9000.00", 
"expanded_poolnet_tap-EXP":"4000.00", 
"clearance_adjustment-CLA":"0.00", 
"mbsd_billing_fee-FEE":"0.00", 
"settlement_billing_charge-SMT":"0.00", 

---

## Page 14

Fund [[settlement]] MRO Specification 
Appendix A: Message Samples 12 
"tba_int_exp-TEM":"0.00", 
"tba_int_exp_adj-ATM":"0.00", 
"pool_int_exp-PEM":"0.00", 
"pool_int_exp_adj-ALM":"0.00", 
"pool_prin_adj-APM":"0.00", 
"pool_fail_mtm-PFM":"0.00", 
"tba_fwd_mtm-MTM":"564.00", 
"pool_fail_int-PIM":"0.00", 
"tba_fail_int-TIM":"0.00", 
"tba_fail_mtm-MFM":"0.00", 
"pool_tap_mtm-PTM":"0.00", 
"mark_return-MRR":"0.00", 
"mark_return_interest-MRI":"0.00", 
"margin_tap-MGN":"0.00", 
"margin_tap_return-MGR":"0.00", 
"margin_tap_return_interest-MGI":"0.00", 
"mbs_part_total":"1000564.25"         
}, 
{ 
                  "part_agg":"MBSA2", 
"factor_update_adj-FAC":"0.00", 
"principal-PRN":"0.00", 
"interest-INT":"0.00", 
"tmpg_charges-TMP":"0.00", 
"tmpg_financing_amount-TMF":"0.00", 
"cpr_claims-CPR":"0.00", 
"broker_commissions-CMS":"0.00", 
"tba_net_tap-TBA":"0.00", 
"do_not_allocate-DNA":"0.00", 

---

## Page 15

Fund [[settlement]] MRO Specification 
Appendix A: Message Samples 13 
"reprice-RPC":"0.00", 
"variance-VAR":"0.00", 
"poolnet_tap-TAP":"0.00", 
"expanded_poolnet_tap-EXP":"0.00", 
"clearance_adjustment-CLA":"0.00", 
"mbsd_billing_fee-FEE":"0.00", 
"settlement_billing_charge-SMT":"0.00", 
"tba_int_exp-TEM":"0.00", 
"tba_int_exp_adj-ATM":"0.00", 
"pool_int_exp-PEM":"0.00", 
"pool_int_exp_adj-ALM":"0.00", 
"pool_prin_adj-APM":"0.00", 
"pool_fail_mtm-PFM":"0.00", 
"tba_fwd_mtm-MTM":"15000000.00", 
"pool_fail_int-PIM":"0.00", 
"tba_fail_int-TIM":"0.00", 
"tba_fail_mtm-MFM":"0.00", 
"pool_tap_mtm-PTM":"0.00", 
“mark_return-MRR":"0.00", 
"mark_return_interest-MRI":"0.00", 
"margin_tap-MGN":"23000000.00", 
"margin_tap_return-MGR":"0.00", 
"margin_tap_return_interest-MGI":"0.00", 
"mbs_part_total":"38000000.00"         
} 
  ]      
 } 
 Fund_Settlement_EOD_Trailer_20180830_000PART1 
 

---

## Page 16

Fund [[settlement]] MRO Specification 
Appendix A: Message Samples 14 
b. Sample of [[EOD]] mro with deposit account associated with one MBS account but there are no activities 
for business date of Aug 30, 2018 
 
Fund_Settlement_EOD_Header_20180830_000PART1 
 { 
  "dep_acct":"000PART1", 
  "created_ts":"20180830053536", 
  "bus_dt":"20180830", 
  "stl_dt":"20180830", 
  "total_funds":"0.00", 
  "mbs_funds":[ 
        { 
        "part_agg":"MBSA1", 
"factor_update_adj-FAC":"0.00", 
"principal-PRN":"0.00", 
"interest-INT":"0.00", 
"tmpg_charges-TMP":"0.00", 
"tmpg_financing_amount-TMF":"0.00", 
"cpr_claims-CPR":"0.00", 
"broker_commissions-CMS":"0.00", 
"tba_net_tap-TBA":"0.00", 
"do_not_allocate-DNA":"0.00", 
"reprice-RPC":"0.00", 
"variance-VAR":"0.00", 
"poolnet_tap-TAP":"0.00", 
"expanded_poolnet_tap-EXP":"0.00", 
"clearance_adjustment-CLA":"0.00", 
"mbsd_billing_fee-FEE":"0.00", 
"settlement_billing_charge-SMT":"0.00", 
"tba_int_exp-TEM":"0.00", 

---

## Page 17

Fund [[settlement]] MRO Specification 
Appendix A: Message Samples 15 
"tba_int_exp_adj-ATM":"0.00", 
"pool_int_exp-PEM":"0.00", 
"pool_int_exp_adj-ALM":"0.00", 
"pool_prin_adj-APM":"0.00", 
"pool_fail_mtm-PFM":"0.00", 
"tba_fwd_mtm-MTM":"0.00", 
"pool_fail_int-PIM":"0.00", 
"tba_fail_int-TIM":"0.00", 
"tba_fail_mtm-MFM":"0.00", 
"pool_tap_mtm-PTM":"0.00", 
"mark_return-MRR":"0.00", 
"mark_return_interest-MRI":"0.00", 
"margin_tap-MGN":"0.00", 
"margin_tap_return-MGR":"0.00", 
"margin_tap_return_interest-MGI":"0.00", 
"mbs_part_total":"0.00"         
} 
    ]    
 } 
 Fund_Settlement_EOD_Trailer_20180830_000PART1 
 

---

## Page 18

 
 
The Fund [[settlement]] MRO Specification (hereinafter, the "document") is provided as a convenience to Members and is for 
information purposes only. Although [[FICC]] may make this document available to Members, it shall be under no obligation to 
[[DO]] so, nor having once or more done so, shall [[FICC]] have a continuing obligation to make available this document or other 
related information of a certain type.  
[[FICC]] does not represent the accuracy, adequacy, timeliness, completeness, or fitness for any particular purpose 
of any information provided to Members in this document, which is provided as-is. [[FICC]] shall not be liable for any 
loss related to such information (or the act or process of providing such information) resulting directly or 
indirectly from mistakes, errors, or omissions, other than those caused directly by gross negligence or willful 
misconduct on the part of [[FICC]]. [[FICC]] shall not be liable for: (1) any loss resulting directly or indirectly from 
interruptions, delays, or defects arising from or related to providing this guide; and (2) any special, consequential, 
exemplary, incidental, or punitive damages.  
Further, the information contained in this document is subject to change. Members and other authorized users of the 
document will find the most current version of the document on [[DTCC]]’s Learning Center site, www.dtcclearning.com. [[FICC]] 
shall bear no responsibility for any losses associated with the failure of Members or other authorized users to follow [[FICC]]’s 
most current document. 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
Doc Date: October 24, 2023 
Publication Code: MBS178 
Service: Fixed Income Clearing 
 
For More Information 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
   