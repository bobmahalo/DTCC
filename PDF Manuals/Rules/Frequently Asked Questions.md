---
title: "Frequently Asked Questions.pdf"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Frequently%20Asked%20Questions.pdf"
pages: 3
size: "117.2 KB"
category: "Rules"
ingested_on: "2026-06-05"
---

# Frequently Asked Questions.pdf

**Original File:** [Frequently Asked Questions.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Frequently%20Asked%20Questions.pdf)  
**Category:** Rules  
**Total Pages:** 3  
**File Size:** 117.2 KB  

---

## Page 1

1/30/24, 8:25 PM Frequently Asked Questions
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/end_of_day/faq.htm?Highlight=book entry 1/3
1. Does [[DTC]] provide [[EOD]] position for every security in their Security Master File?No; [[DTC]] only provides the [[EOD]] position for [[securities]] in which participants hold position in at [[DTC]].
2. Are all security classes included in the [[DTC]] End of Day ([[EOD]]) position file?The file includes all security classes except for Money Market Instruments (MMIs).
3. What does Registration/Certificate Type mean?
An [[investor]] can hold a security in three ways: Physical Certificate, [[street name]], or Direct. [[DTC]] “[[Cede & Co]]” only holds the portion of an [[issuer]]'s [[securities]] that are held in “StreetName”. [[issuer]]’s [[securities]] held by investors in either Physical Certificate form or Direct are not held at [[DTC]].
Physical Certificate: The security is registered in the final beneficiary’s name on the [[issuer]]'s books, and the final beneficiary receives an actual, hard copy [[Stock]] or bondcertificate representing ownership of the security.
"[[street name]]" Registration: The security is registered in the name of the final beneficiary’s brokerage firm on the [[issuer]]'s books, and the final beneficiary’s brokerage firmholds the security for the final beneficiary in "[[book-entry]]" form. "[[book-entry]]" means that the final beneficiary does not receive a certificate. Instead, the final beneficiary’s brokerkeeps a record in its books that the final beneficiary owns that particular security.
"Direct" Registration: The security is registered in the final beneficiary’s name on the [[issuer]]'s books, and either the company or its [[transfer agent]] holds the security for thefinal beneficiary in [[book-entry]] form. The "Direct RegistrationSystem" (also known as "[[DRS]]") allows investors to transfer [[securities]] held this way.
4. What does each Registration/Certification value mean?Certificate Type identifies the method by which the Certificate will be exercised. Registration type will be populated by the following 4 values: Book Entry Only ([[BEO]]), Registered,Bearer, or Interchangeable
Book Entry Only ([[BEO]]): [[DTC]] eligible [[securities]] for which (i) physical certificates are not available to investors and (ii) [[DTC]], through its [[nominee]], [[Cede & Co]]., will hold theentire balance of the offering, either at [[DTC]] or through a [[FAST]] Agent in [[DTC]]’s [[FAST]] Automated [[securities]] Transfer (“[[FAST]]”) program.
Bearer: Cash to whomever holds the paper. Note that Bearer instruments are dying off, as they are no longer allowed to be issued.
Interchangeable: A Bearer instrument that can become “registered” based on the [[issuer]]/agents prerogative to [[DO]] so (built into the terms of the security at issuance).
Registered: The security is only available in “registered” form (ownership rights exclusive to the entity that the [[transfer agent]] recognizes on its registrar).
5. Why are there blank registration types?This field is sourced from [[DTCC]]’s Security Master file. The registration type input was not a required input until 2018. Registration Type is a very reliable field, and is populated inthe [[Underwriting]] process as part of the [[CUSIP]] add. Issuers and Agents indicate whether or not a security is Book Entry, and [[Underwriting]] performs validation. If Book Entry Only,the [[issuer]] is required to submit a letter of representation requiring them to follow [[DTC]]’s rules and procedures. For MMI and Federal Reserve, the value is defaulted to ‘E’ BookEntry
6. Are Corporate Action events reflected in [[DTC]]’s End of Day Position?
Yes; [[DTC]]’s End of Day position can be impacted by any corporate action. The impact of a corporate action will be reflected in [[DTC]]’s End of Day position on its allocation orpayable date.

---

## Page 2

1/30/24, 8:25 PM Frequently Asked Questions
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/end_of_day/faq.htm?Highlight=book entry 2/3
7. Which corporate actions may have an impact on [[DTC]]’s End of Day position? Below is a list of corporate action events that may impact [[DTC]]’s End of Day position:
Automatic [[Dividend]] Reinvestment
Capital Gains Distribution
Cash [[Dividend]]
CD Early Redemption
Conversion
[[default]]
Distribution
[[Dividend]] with [[Option]]
Dutch Auction
Exchange Offer
Final Paydown
Full Call
Full Prerefunding
Interest
[[liquidation]]
Mandatory Exchange
Mandatory Put
Maturity
Merger
Name Change
Odd Lot Offer
Partial Call
Partial Defeasance Partial Mandatory Put
Partial Prerefunding
Pay in Kind
Plan of Reorganization
Principal
Put
Redemption of [[Warrants]]
Reorganization
Return of Capital
Reverse [[Stock]] Split
Rights Distribution
Rights Subscription
Sale Of Rights
Security Separation
Special [[Dividend]]
Spin-Off
[[Stock]] [[Dividend]]
[[Stock]] Split
Tender Offer
Termination
[[Warrants]] Exercise
Worthless
8. Are there other transactions other than Corporate Actions that could cause [[DTC]]’s End of Day position to change?
Yes, an example is through a [[DWAC]] transaction. [[DWAC]] - allows participants to instruct [[DTC]] regarding [[book-entry]] deposit and withdrawal transactions of eligible [[securities]] beingmade directly via a [[FAST]] [[transfer agent]]

---

## Page 3

1/30/24, 8:25 PM Frequently Asked Questions
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/end_of_day/faq.htm?Highlight=book entry 3/3
Back to Top
[[DTC]]’s End of Day Position vs [[shares]]/Amount Outstanding
1. Why might [[DTC]]’s End of Day positions differ from the [[shares]]/amount outstanding published by other third party vendors?
a. [[DTC]]’s End of Day position reflects only the portion of a security issuance held at [[DTC]], also known as “[[street name]]” Registrations. The others: Physical Certificate and “Direct”Registration aren’t held at [[DTC]]; therefore, if portions of a security issuance are held as physical certificates or are directly registered, they will not be included in [[DTC]]’s EODposition.
b. If a [[CUSIP]] is a 144A and [[Reg S]] security and the issue is split across 2 CUSIPs, [[DTC]]’s End of Day position is reflected in each of those CUSIPs instead of aggregated andreflected in 1 [[CUSIP]].
c. Non-[[FAST]] [[securities]] & redemption processing – For Non [[FAST]] [[securities]], [[DTC]]’s End of Day position may reflect full redemption or maturity events prior to or after theredemption date because of the way in which full redemption and maturity events for Non [[FAST]] [[securities]] are processed at [[DTC]]. The date on which [[DTC]] processes a letter oftransmittal for Non-[[FAST]] [[securities]] is the day in which the [[DTC]] End of Day position is removed from the report instead of on redemption date when the funds are allocatedand the position is taken to 0. Currently, of the approximately 1.26M [[securities]] covered in the [[DTC]] End of Day position report approximately 100,000 are Not [[FAST]] for whichthis may occur.
d. Principal Distribution Type - Some [[securities]] pay principal distributions based on a random lot or call lottery basis (Partial Call) and other [[securities]] pay principal on a pro-ratabasis. When a security repays principal on a [[Pro-Rata]] basis [[DTC]]’s End of Day position is NOT decremented so you will see the Original Issuance Amount populated.
e. There are fixed income instruments that have matured, yet there is still a [[DTC]] End of Day position. These [[securities]] may be in [[default]], bankruptcy, or [[custody]] service onlysecurities. If a security records an Event of [[default]] or the [[issuer]] files for Chapter 11 Bankruptcy, [[DTCC]] will retain position until the [[issuer]] reorganizes their funds as part of thecourt ruling and they pay off the balance either in full or partly but then write off what remains unpaid. [[DTC]]’s Security Master file field “First Payment Indicator” is updated witha value of “[[default]]” or “Payment Omitted” once [[DTCC]] receives a notice from the [[issuer]] or Trustee confirming an Event of [[default]] or that the [[issuer]] has filed for Chapter 11.
 
 