---
title: "Message Formats.pdf"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Message%20Formats.pdf"
pages: 18
size: "1027.8 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Message Formats.pdf

**Original File:** [Message Formats.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Message%20Formats.pdf)  
**Category:** Other  
**Total Pages:** 18  
**File Size:** 1027.8 KB  

---

## Page 1

1/30/24, 8:28 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm?Highlight="Boo… 1/18
 eade essage  0
The next table describes the Header message, which is the initial message attached to every file type.
Table 14  [[issuer]] Message - D01
Position Length Format Field Name Description
1 – 3 3 Character Message Type Identifies the message type. The value is H01(Header Message).
4 – 9 6 Character Message Sequence Number Identifies the sequence number within themessage type. Initialized  to 000001.
10 – 17 8 Numeric File Date The date the file  was processed inCCYYMMDD format.
18 – 25 8 Character File Name The name of the file. The values are provided inFile Descriptions and Acronyms.
26 – 300 273 Character Filler Reserved for future use.
International Message - I01
The next table describes the International Message, which is currently used exclusively for [[CSDS]] (Central Security Depositories).
Table 15  [[issuer]] Message - D01
Position Length Format Field Name Description
1 – 3 3 Character Message Type The type of Message. The value is I01(International).
4 – 9 6 Numeric Message SequenceNumber Identifies the sequence number within theMessage type. Initialized to 000001.
10 – 10 1 Character Message Status Type Indicates if [[DTC]] is adding a new message orupdating an existing message.
A: Add
U: Update
M: Matured
11 – 19 9 Character Issue Identifier The 9-character [[CUSIP]] number.
20 – 31 12 Character International Identifier (ISIN) The 12-character ISIN (International SecuritiesIdentification Number) number, if available.
32 – 91 60 Character [[issuer]] Name The first occurrence of the formal [[issuer]] nameappearing on the Prospectus or OfferingStatement that is supplied to [[DTC]] duringeligibility processing. This description provides aconsistent [[issuer]] name across the issuance andissues. The [[issuer]] or Issuing Agent may alsoprovide the description if the security does notgo through the eligibility process (for example,for MBS [[securities]]).
92 – 94 3 Character [[issuer]] Country of Origin The three-character ISO country code . Thevalues are contained in ISO Country Codes.
95 – 95 1 Character Issue Type The type of security. The values are:
1: [[Equity]]
5: Corporate Debt
7: Municipal Debt.
96 – 98 3 Character Sub-Issue Type The type of issue or sub-issue used by [[DTC]] toclassify a security. The values are contained inDTC Sub-Issue Types.
99 – 99 1 Character Deliver Order Chill Activity Flag Indicates whether the security is eligible forDTC Deliver Order activity. The values are:
Y: Yes
N: No
Blank: Not Applicable / Not Available

---

## Page 2

1/30/24, 8:28 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm?Highlight="Boo… 2/18
Position Length Format Field Name Description
100 –300 201 Character Filler Reserved for future use.
[[issuer]] Message - D01
The next table describes the [[issuer]] Message, which contains [[issuer]] information about the [[DTC]] search, as well as a short description, state and domicile of issuance.
Table 16  [[issuer]] Message - D01
Position Length Format Field Name Description
1 – 3 3 Character Message Type The type of Message. The value is D01 ([[issuer]]).
4 – 9 6 Numeric Message Sequence Number Identifies the sequence number within themessage type. This value is Initialized to000001.
10 – 10 1 Character Message Status Type Indicates whether [[DTC]] is adding a newMessage or updating an existing Message.
A: Add
U: Update
11 – 19 9 Character Issue Identifier The 9-character [[CUSIP]] number.
20 - 31 12 Character International Identifier The 12-character ISIN (International SecuritiesIdentification Number) number.
32 - 34 3 Character State of Issuance The two-digit state code for municipal andcorporate [[securities]] issued in the United States,its territories and Canadian provinces. This fieldcontains the state code of issuance formunicipal [[securities]], and the state code ofincorporation for corporate [[securities]]. Thevalues are contained in ISO United States andCanadian Provinces.
35 - 37 3 Character Country ofIssuance ([[issuer]] Country of Origin) The three-digit ISO country code (for non-UnitedStates and territory [[securities]]). The values arecontained in ISO Country Codes.
38 - 97 60 Character [[issuer]] Name The first occurrence of the formal [[issuer]] nameappearing on the Prospectus or OfferingStatement that is supplied to [[DTC]] duringeligibility processing. This description provides aconsistent [[issuer]] name across the issuance andissues. The [[issuer]] or Issuing Agent may alsoprovide the description if the security does notgo through the eligibility process (for example,for MBS [[securities]]).
98 - 127 30 Character [[DTC]] ShortDescription The abbreviated security descriptiontraditionallysupplied in [[DTC]] files.
128 – 134 7 Character Corresponding Base [[CUSIP]] Under the [[DTC]] MMI discount numberingscheme program, issuers request dual baseCUSIPs from the [[CUSIP]] Service Bureau. Thebase CUSIPs are assigned and used basedupon leap year and subsequent even and oddyears.These base [[CUSIP]] numbers allow the [[IPA]] toseamlessly issue and process transactions. TheCorresponding Base [[CUSIP]] is the oneassociated with the selected security. Applicablefor MMIsecurities only.
135 – 135 1 Character Base [[CUSIP]] Check Digit The check digit for the current Base [[CUSIP]].Applicable for MMI [[securities]] only

---

## Page 3

1/30/24, 8:28 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm?Highlight="Boo… 3/18
Position Length Format Field Name Description
136 - 136 1 Character Spanish TaxWithholding Indicator Indicates whether the security is subject toSpanish Tax Withholding regulations.Y: Subject to Spanish Tax Withholdingregulations.Note: To limit Spanish tax withholding, clientname and country of residence will bedisclosed to the [[issuer]]/Spanish Govt. [[DO]] NOTPURCHASE IF YOU [[DO]] NOT CONSENT.
N: Blank: Not Applicable, Not Available Under Spanish taxregulation, investors in preferred [[securities]], senior notes orsubordinated notes listed on an organized market in an OECDcountry, with no tax residency in Spain and not acting through apermanent establishment in Spain, are exempt from the SpanishNon-resident Income Tax ("NRIT"), provided certain informationobligations relating to identity and residence of beneficial ownersentitled to receive distributions are complied with. If theseinformation [[obligations]] are not complied with, Spanish issuershave to withhold the NRIT.
137 – 300 164 Character Filler Reserved for future use.
Issuance Message - D02
The next table describes the Issuance Message, which contains issue date, currency, and issuance amount information.
Table 17  Issuance Message - D02
Position Length Format Field Name Description
1 – 3 3 Character Message Type The type of Message. Thevalue is D02 (Issuance).
4 – 9 6 Numeric Message Sequence Number Identifies the sequence number within themessage type. Initialized to 000001.
10 – 10 1 Character Message StatusType Indicates whether [[DTC]] isadding a newmessage or updating anexisting message.
A: Add
U: Update
11 – 19 9 Character Issue Identifier The 9-character [[CUSIP]] number.
20 - 31 12 Character InternationalIdentifier (ISIN) The 12-character ISIN(International SecuritiesIdentification Number)number.
32 – 39 8 Character Expected Issue
Date
Currently populated with Dated Date The date
when the security is released or sold
For [[Equity]] [[securities]] in CCYYMMDDformat.
For MMI- eligible [[securities]] the Messagedate is equivalent to the issue date.
40 - 42 3 Character Issuance Currency The three-character ISOcurrency code of thecertificate. The values arecontained in ISO CurrencyCodes.
43 - 45 3 Character Income Currency The three-character ISO currency code in whichincome would be paid for a security. The valuesare contained in ISO Currency Codes.
46 - 58 13 Numeric Original IssuanceAmount The original offering amountthat does not include theover allotment of [[shares]] inthe new issue. This amounttypically applies tomunicipals and is alwaysblank for MMI programs. Inwhole number format.

---

## Page 4

1/30/24, 8:28 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm?Highlight="Boo… 4/18
Position Length Format Field Name Description
59 - 69 11 Numeric Offering [[shares]] The number of [[shares]] initially issued for thissecurity; for [[Equity]] issues in whole number format.
70 - 76 7 Numeric Offering Price The original offering shareprice; for equityissues in 9(4)V9(3) format.
77 - 77 1 Character [[IPO]] Tracking Indicator A value that indicates whether a lead managerrequested [[IPO]] tracking for this security.
Y: Yes
N: No
Blank: No Applicable / Not Available
78 - 85 8 Numeric [[IPO]] Start Date The start date of the IPOtracking, in CCYYMMDDformat.
86 - 86 1 Character [[DTC]] Eligibility Indicator -
obsolete field, not supported
A value that indicates whether the security iseligible for [[DTC]]’s services.
Y: Yes
N: No
Blank: No Applicable / Not Available
87 - 94 8 Numeric Prospectus Received The date that [[DTC]] receiveda Prospectus or OfferingStatement for a givensecurity.Displayed in CCYYMMDDformat.
95 - 103 9 Numeric Minimum Denomination A numeric minimum denomination for trading(typically the number of [[shares]] or [[Bonds]] or theprincipal amount), in whole number format.
104 - 112 9 Numeric MultipleDenomination A numeric amount ofissuance for uniquelydenominated [[securities]], inwhole number format.
113 - 113 1 Character Issuance Indicator Indicates whether the issuance is original or
secondary.  The values are:
O: Original
S: Secondary
Blank: Not Applicable / Not Available
114 - 114 1 Character Issue Status Code First Payment IndicatorPossible values:
S: Short First Payment
L: Long First Payment
Y: Yearly
E: Payment Omitted
D: [[default]]
X: Extra Long
P: Possible [[default]]
Space: First Payment is Regular/notapplicable/not available
115-300 186 Character Filler Reserved for future use
Issue Message - D03
The next table describes the Issue Message, which contains specific information about:
coupon
maturity
registration
exchange
issue amount

---

## Page 5

1/30/24, 8:28 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm?Highlight="Boo… 5/18
amount outstanding
Table 18  Issue Message - D03
Position Length Format Field Name Description
1 - 3 3 Character Message Type The type of Message. The value is D03(Issue).
4 - 9 6 Numeric MessageSequence Number Identifies  the sequence number within themessage type. Initialized to 000001.
10 – 10 1 Character Message StatusType Indicates whether [[DTC]] is adding a newmessage or updating an existing message.
A: Add
U: Update
M: Matured
11 – 19 9 Character Issue Identifier The 9-character [[CUSIP]] number.
20 - 31 13 Character InternationalIdentifier The 12-character ISIN (International SecuritiesIdentification Number) number.
32 - 44 13 Numeric AmountOutstanding  -obsolete,defaulted tozeroes
The number of [[securities]] (either par amount orshares) that [[DTC]] “[[Cede & Co]]” is listed as theholder of record, in whole number format. Thisinformation is listed in par amount for fixedincome [[securities]] and [[shares]] for equitysecurities.
45 - 51 7 Numeric Coupon/InterestRate The coupon or interest rate. This field does notappear for [[Equity]] [[securities]]. The rate is in9(3)V9(6)format. The field  is zero-filled fordiscount program MMI [[securities]] and otherswithout a rate. For variable rate [[securities]], thevalue is indicated as one cent.
52 - 59 8 Numeric Maturity Date The maturity date in CCYYMMDD format.
60 - 67 8 Numeric Dated Date/ Dated Date - Date from which Interest startsaccruing for debt instruments in CCYYMMDDformat:
68 - 68 1 Character Registration Type The registration type of a security.
B: Bearer
E, U, X: Book Entry
A, D, I: Interchangeable
M, R: Fully Register
69 - 69 1 Character Taxable Indicator A value that indicates whether the security issubject to federal income taxes; for municipalsecurities only.
Y: Yes
N: No
Blank: Not Applicable / Not Available
70 - 70 1 Character Rule 144AIndicator A value that indicates whether a security isissued under [[SEC]]  [[Rule 144A]] as a privateplacement.
Y: Yes
N: No
Blank: Not Applicable / Not Available
71 - 71 1 Character [[regulation]] SIndicator A value that indicates whether the security issubject to [[Regulation S]] of the Federal ReserveBoard.
Y: Yes
N: No
Blank: Not Applicable / Not Available

---

## Page 6

1/30/24, 8:28 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm?Highlight="Boo… 6/18
Position Length Format Field Name Description
72 – 72 1 Character Rule 3c-7 Indicator A value that indicates whether a security isrelying on the exemption from Section 3(C.)(7)of the [[Investment Company Act]] of 1940.
Y: Yes
N: No
Blank: Not Applicable / Not Available
73 - 80 8 Numeric First Interest PayDate - defaulted tozeroes
The first interest pay date for a fixed incomesecurity, in CCYYMMDD format.
81 – 90 10 Character Ticker Symbol An arrangement of characters (usually letters)representing a particular security listed on anexchange or otherwise traded publicly. Onlythe Primary Exchange Ticker Symbol isdisplayed.
91 - 105 15 Character Exchange The exchange on which the security you wantinformation about is listed. The values are:
AMEX: American [[Stock Exchange]]
[[NYSE]]: [[New York Stock Exchange]]
[[OTC]]: Over the Counter
[[NASDAQ]]: [[National Association of Securities Dealers]] AutomatedQuote.
106 - 115 10 Character Pool [[ID]] The identifier applied to mortgage-backedsecurities.
116 - 116 1 Character Global Issue A value that indicates whether the securityuses foreign clearance or [[settlement]].
Y: Yes
N: No
Blank: Not Applicable / Not Available
117 - 117 1 Character Issue Type Identifies the type of security. The values are:
1: [[Equity]]
5: Corporate Debt
7: Municipal Debt
118 – 120 3 Character Sub-Issue Type The type of issue or sub-issue used by [[DTC]] toclassify a security. The values are contained in.Appendix I - [[DTC]] Sub-Issue Types.
121 - 121 1 Character Put Indicator A value that indicates whether the issue has aput feature.
Y: Yes
N: No
Blank: Not Applicable / Not Available
122 - 122 1 Character Call Indicator A value that indicates whether the issue issubject to a call redemption.
Y: Yes
N: No
Blank: Not Applicable / Not Available
123 - 123 1 Character Sinking FundIndicator A value that indicates whether a sinking fundprovision applies to this security.
Y: Yes
N: No
Blank: Not Applicable / Not Available
124 - 124 1 Character PrerefundedIndicator A value that indicates whether an issue hasfunds that have been put aside to redeem theissue at its earliest call date.
Y: Yes
N: No
Blank: Not Applicable / Not Available

---

## Page 7

1/30/24, 8:28 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm?Highlight="Boo… 7/18
Position Length Format Field Name Description
125 - 125 1 Character PrincipalAmortizationIndicator
A value that indicates whether the principal issubject to amortization.
Y: Yes
N: No
Blank: Not Applicable / Not Available
126 - 126 1 Character Indexed PrincipalIndicator (MMIsOnly)
A value that indicates whether the interestpayments are linked to an index.
Y: Yes
N: No
Blank: Not Applicable / Not Available
127 - 127 1 Character Renewable NoteIndicator (MMIsOnly)
A value that indicates whether a MTN has arenewable feature.
Y: Yes
N: No
Blank: Not Applicable / Not Available
128 - 128 1 Character Interest Step-upIndicator (MMIsOnly)
A value that indicates whether the security hasan interest rate step-up feature.
Y: Yes
N: No
Blank: Not Applicable / Not Available
129 - 129 1 Character Interest ResetIndicator (MMIsOnly)
A value that indicates whether the security hasa rate reset feature.
Y: Yes
N: No
Blank: Not Applicable / Not Available
130 - 130 1 Character ChangeablePayment Indicator(MMIs Only)
A value that indicates whether the security canmodify the payment amount or date.
Y: Yes
N: No
Blank: Not Applicable / Not Available
131 - 143 13 Numeric Issue Amount The amount issued specific to this security, inwhole number format. Often a subset of theOriginal Issuance.
144 - 144 1 Character Foreign OrdinaryProcessingIndicator
A value that indicates whether the security iseligible for foreign ordinary processing.
Y: Yes
N: No
Blank: Not Applicable / Not Available
145-146 2 Character MBS Product [[ID]] Describes the Different Types of MBSBonds. For values, see MBS Product IDValues.
147-148 2 Character MBS Category [[ID]] The Classification of the different terms thatapply to MBS [[Bonds]]. For values, see MBSProduct [[ID]] Values.
149-149 1 Character Tax Credit in Lieuof InterestIndicator
This field identifies whether a security is aBuild America Bond that has a Tax Creditfeature.
Y: Yes
N: No

---

## Page 8

1/30/24, 8:28 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm?Highlight="Boo… 8/18
Position Length Format Field Name Description
150-150 1 Character Tax Credit BondType 
This field identifies the payment featuresassociated with a Tax Credit security
1: Combo for redemption and tax credit.
2: Combo for redemption, tax credit and interest.
3: Strip for tax credit.
4: strip for redemption
5: Strip for redemption and interest.
6: Strip for interest
151-159 9 Numeric Tax Credit Rate This field will contain the actual Tax Credit ratefor the security. The first three digits representdollars. The last six digits in the field representcents.
160-162 3 Numeric Tax Credit RecordDate – Number ofDays
This is the number of days the record date isgoing to be offset from the payment date.
163-163 1 Character Tax Credit RecordDate – Number ofDays -Business/CalendarIndicator
This indicates whether the Record Date offsetis specified as number of business or calendardays.
B: Business
C: Calendar
164-171 8 Character Tax Credit RecordDate – Fixed Date This is the two pre-established record dates forthe security.
The first four bytes contain the first record date with a formatMMDD
The last four bytes contain the second record date with the sameformat MMDD.
Format MMDDMMDD
172-172 1 Character Tax CreditPaymentFrequency
This is the stated frequency for payments forthe security.
1: Annual
2: Semi-annual
4: Quarterly,
8: Monthly
173-180 8 Character Tax Credit FirstPayment Date This is the date when the first interest paymenton this security is due.Format CCYYMMDD
181-181 1 Character [[Stock]] for MaturityIndicator This field indicates whether a bond has theoption to pay Maturity proceeds as Stockinstead of Cash.
Y: Yes
N: No
182-182 1 Character Extended MaturityIndicator This field indicates whether a bond has theoption of extending its stated Maturity Date.
Y: Yes
N: No
183-183 1 Character Sovereign DebtIndicator This field identifies a bond as being SovereignDebt, issued by a non-US Sovereign entity.
Y: Yes
N: No
184 – 300 117 Character Filler Reserved for future use.

---

## Page 9

1/30/24, 8:28 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm?Highlight="Boo… 9/18
Descriptive Message - D05
The next table details the Descriptive Message, which contains formal issuance description information derived from [[DTC]]'s eligibility process. This description comes from theprospectus or offering filing. In some cases, this description is supplied to [[DTC]] directly from contributors such as the MMI system, and therefore may not represent a formal description.
Table 19  Descriptive Message - D05
Position Length Format Field Name Description
1 - 3 3 Character Message Type The type of Message. The value is D05(Descriptive).
4 - 9 6 Numeric MessageSequenceNumber
Identifies the sequence number within themessage type. Initialized to 000001.
10 – 10 1 Character MessageStatusType
Indicates whether [[DTC]] is adding a newmessage or updating an existing message.
A: Add
U: Update
11 – 19 9 Character [[issuer]] Identifier The 9-character [[CUSIP]] number.
20 – 31 12 Character InternationalIdentifier The 12-character ISIN (InternationalSecurities Identification Number) number.
32 – 91 60 Character IssueDescription The security description, which is the formalIssuer name appearing on the Prospectus orOffering Statement that is supplied to DTCduring eligibility processing. The [[issuer]] orIssuing Agent may also provide thedescription if the security does not gothrough the eligibility process (for example,for MBSsecurities). This field consists of the first ofthe four lines (60 bytes each) of information.
92 – 271 180 Character IssueDescription This field consists of the next three of thefour lines (60 bytes each) of information.
272 – 300 29 Character Filler Reserved for future use.

---

## Page 10

1/30/24, 8:28 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm?Highlight="Bo… 10/18
Depository Status Message - D06
The next table describes the Depository Status Message, which contains [[DTC]] processing and status information for the security.
Table 20  Depository Status Message
Position Length Format Field Name Description
1 – 3 3 Character Message Type The type of Message. The value is D06(Depository Status).
4 – 9 6 Numeric Message Sequence Number Identifies the sequence number within themessage type. Initialized to 000001.
10 – 10 1 Character Message Status Type Indicates whether [[DTC]] is adding a newmessage or updating an existing message.
A: Add
U: Update
11 – 19 9 Character Issue Identifier The 9-character [[CUSIP]] number.
20 – 31 12 Character International Identifier The 12-character ISIN (International SecuritiesIdentification Number) number.
32 – 32 1 Character Same Day FundSettlement Eligibility Indicator –obsolete field, not supported
A value that indicates whether the security iseligible to settle in same-day funds.
Y: Yes
N: No
33 – 33 1 Character [[FAST]] COD & WT [[FAST]] COD & WT. A value that indicates if theissue is eligible for [[DTC]]'s [[FAST]] COD & WT(Full [[FAST]]) service.
Y: Yes, Full [[FAST]]
N: No, Not Full [[FAST]]
34 – 34 1 Character DividendReinvestment Service EligibilityIndicator
A value that indicates whether the [[CUSIP]] iseligible for [[DTC]]'s [[Dividend]] Reinvestmentservice.
Y: Yes
N: No
Blank: Not Applicable / Not Available
35 – 35 1 Character [[custody]] Service Eligibility Indicator A value that indicates whether the [[CUSIP]] iseligible for [[DTC]]'s [[custody]] service.
Y: Yes
N: No
Blank: Not Applicable / Not Available
36 – 36 1 Character Federal [[book-entry]] Eligibility Indicator A value that indicates whether the [[CUSIP]] is FedBook eligible.
Y: Yes
N: No
Blank: Not Applicable / Not Available
37 – 37 1 Character [[Direct Registration]] Eligibility Indicator A value that indicates whether the [[CUSIP]] iseligible for [[DTC]]'s [[Direct Registration]] service.
Y: Yes
N: No
Blank: Not Applicable / Not Available

---

## Page 11

1/30/24, 8:28 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm?Highlight="Bo… 11/18
Position Length Format Field Name Description
38 – 38 1 Character Communications Issue Indicator A value that indicates whether the issue is acommunications issue.
Y: Yes
N: No
Blank: Not Applicable / Not Available
39 – 39 1 Character Deposit ActivityChill Indicator Indicates that this security is locked from anydeposit activity at [[DTC]].
Y: Yes
N: No
40 – 40 1 Character Chill COD Indicates that this security is locked from anyCOD (Certificate on demand) activity at [[DTC]].
Y: Yes
N: No
41 – 41 1 Character Chill WT Indicates that this security is locked from anyWT (withdrawals-by-transfer) activity at [[DTC]].
Y: Yes
N: No
42 – 42 1 Character Chill [[DO]] Indicates that this security is locked from anyDO (Deliver Order) activity at [[DTC]].
Y: Yes
N: No
43 – 43 1 Character Chill Segregation Indicates that this security is locked from anysegregation activity at [[DTC]].
Y: Yes
N: No
44 –44 1 Character Pledge Chill Indicator Indicates that this security is locked from anypledge activity at [[DTC]].
Y: Yes
N: No
45 – 45 1 Character Thin Issue Indicator A value that indicates whether the issue is a thinissue.
Y: Yes
N: No
Blank: Not Applicable / Not Available
46 – 65 20 Character Reserved Reserved for future use.

---

## Page 12

1/30/24, 8:28 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm?Highlight="Bo… 12/18
Position Length Format Field Name Description
66 – 66 1 Character Fractional Dollars/ Cents Eligible Indicates if the security can contain FractionalShare/amount component.
Y: Yes
N: No
Blank: Not Applicable / Not Available
A fractional share is a unit of [[Stock]] that is lessthan one full share. For example., if ashareholder participates in a dividendreinvestment program and the dividends beingreinvested are not enough to purchase a fullshare at the market price, the shareholder willbe credited with a fractional share until enoughdividends accrue to purchase one full share.
67 – 67 1 Character Segregation 100 Number EligibilityIndicator A value that indicates whether the issue is asegregated 100 issue.
Y: Yes
N: No
Blank: Not Applicable / Not Available
68 – 68 1 Character Auto Certification Eligibility Indicator A value that indicates whether the issue iseligible for [[DTC]]'s auto certification program.
Y: Yes
N: No
Blank: Not Applicable / Not Available
69 – 69 1 Character Non-TransferableIssue Information about the status of whether asecurity can be moved or transferred betweenparticipants.
70 – 70 1 Character Record Date Weekend/HolidayIndicator Indicates the method by which the record datewill be adjusted if it falls on a holiday orweekend.
B: Before
A: After
Blank: Not Applicable / Not Available
71 – 71 1 Character Record DateBusiness/Calendar Indicator Indicates whether the Record Date offset isspecified as number of business or calendardays The values are:
B: Business
C: Calendar
Blank: Not Applicable / Not Available
72 – 119 48 Character [[DTC]] Description (Long) The 48-character [[DTC]] issue description.
120 -139 20 Character [[DTC]] Description (Short) The 20-character [[DTC]] short issue description,typically system-generated.
140 -147 8 Character Vault Location The location of [[securities]] held by [[Cede & Co]].
148 -150 3 Character Coupon Number The next Coupon Number (applicable for Bearerand Interchangeable certificates).
151-151 1 Character Networking for Equities Indicator -obsolete??? Indicates whether the security is eligible forDTCC's Networking for Equities program. :
N: Security is not eligible for the Networking for Equities program.
Y: Security is eligible for the Networking for Equities program.

---

## Page 13

1/30/24, 8:28 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm?Highlight="Bo… 13/18
Position Length Format Field Name Description
152-152 1 Character [[FAST]] WT A value that indicates if the issue is eligible forDTC's [[FAST]] WT service only.
Y: Yes
N: No
153-153 1 Character Book Entry Only Security DRSEligibility  Indicator 0: Security is eligible for "WT" in statement form only at [[DTC]].Certificates are available at the [[transfer agent]].
1: Security is eligible for "WT" in statement form only.
2: Security is [[DRS]] eligible but not participating. Certificates onlyare available.
Note: A “space” in this field indicates that theissue is not [[DRS]]-eligible.
154 -154 1 Character Filler Reserved for future use.
155 -155 1 Character [[OA]] Rate Timelines Attestation Code 1: Conforming [[CUSIP]]
2, 3: Non conforming [[CUSIP]]
This field is applicable only for Sub-Issue Type‘540’ CMO and ‘541’ ABSWhere:Conforming means that this security isstructured in a way that makes it likely for thefinal rate to be calculated and disseminated toDTC prior to the payable date.-and-Non-conforming means that this security isstructured in a way that makes it unlikely for thefinal rate to be calculated anddisseminated to [[DTC]] prior to the payable date.
156-156 1 Character [[CNS]] EligibilityIndicator 
Indicates whether a security is eligible forContinuous Net [[settlement]] ([[CNS]]) throughNSCC.
Y: Yes
N: No
157-157 1 Character OFAC Sanctioned Indicator Indicates if security is restricted due to OFACsanctions.
Y: Yes
N: No
158-158 1 Character Global Lock Indicator This field indicates if the security is frozen andglobally locked from any activity at [[DTC]].
Y: Yes, the Security is globally locked.
N: No, the Security is not globally locked.
159-159 1 Character Global Lock Reason This field provides a reason for the Global Lock.
Space: Security is not globally locked. Reason is not applicable
0: [[DTCC]]-Applied Global Lock
1: [[DTCC]]-Applied Global Lock - Compliance Related.
2-9: Reserved for future use.
160-207 48 Character Unit Component Ratio Text Box Specifies the ratio of units to each of itscomponents. Applicable for sub-issue types'780' [[Equity]] Unit’ ([[Equity]] Issue type) and'781' Debt Unit’ (Corporate Bond Issue type)

---

## Page 14

1/30/24, 8:28 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm?Highlight="Bo… 14/18
Position Length Format Field Name Description
208-208 1 Character Deposit ChillReason This field provides a reason for the DepositChill.
Space:  Security does not have a Deposit Chill. Reason is notapplicable.
0: [[DTCC]]-Applied Deposit Chill.
1: [[DTCC]]-Applied Deposit Chill - Compliance Related.
2-9: : Reserved for future use.
209-209 1 Character 871(m) Transaction Indicates if the security is subject toregulation 871(m).Valid values:
Y: yes
N: No
Space: Not applicable/ not available
210-210 1 Character Contract Type Contract Type for 871(m) Transaction.Valid values:
S: Simple
C: Complex
Space: Not applicable
211-217 7 Numeric Delta The value of Delta for Simple Contract Type(the “delta” of an instrument is a measure ofthe relationship between changes in value ofthe instrument and changes in value of theunderlying [[Stock]]).Format: 9(1)V9(6) format, up to 6 decimalpoints.Valid values: from 0800000 (0.8) to 1000000(1.0) [[default]] = zeroes
218-300 83 Character Filler Reserved for future use.
Agent Message - A01
The next table describes the Agent Message, which identifies the agent(s) involved with the security. The agent identifier is blank if an agent is not applicable for a given security.
Table 21  Agent Message - A01
Position Length Format Field Name Description
1 - 3 3 Character Message Type The type of Message. The value is A01 (Agent).
4 – 9 6 Numeric MessageSequenceNumber
Identifies  the sequence number within themessage type. Initialized to 000001.
10 – 10 1 Character Message StatusType Indicates whether [[DTC]] is adding a newmessage or updating an existing message.
A: Add
U: Update
11 – 19 9 Character Issue Identifier The 9-character [[CUSIP]] number.
20 – 31 12 Character InternationalIdentifier The 12-character ISIN (International SecuritiesIdentification Number) number.
32 – 39 8 Character DDA Agent [[ID]] The identification number of the DividendDisbursing Agents that are registered for thissecurity.

---

## Page 15

1/30/24, 8:28 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm?Highlight="Bo… 15/18
Position Length Format Field Name Description
40 –40 1 Character MMI Indicator ForPaying Agent Indicates whether the Paying Agent is an MMIPaying Agent, and their identification number isactually a [[participant]] [[ID]]. The values are:
Y: Yes
N: No
Blank: Not Applicable / Not Available
41 – 48 8 Character Paying Agent [[ID]] The identification numbers of the Paying Agentsthat are registered for this security.
49 – 56 8 Character [[transfer agent]] [[ID]] The identification numbers of the TransferAgents that are registered for this security.
57 – 64 8 Character Remarketing AgentID The identification numbers of the RemarketingAgents that are registered for this security. TheRemarketing Agent [[ID]] is the same as aparticipant [[ID]].
65 – 72 8 Character Redemption AgentID The identification numbers of the RedemptionAgents that are registered for this security.
73 – 80 8 Character Conversion AgentID – obsolete, notpopulated
The identification numbers of the ConversionAgents that are registered for this security.
81 – 88 8 Character Information AgentID – obsolete, notpopulated
The identification numbers of the InformationAgents that are registered for this security.
89 – 96 8 Character Exchange Agent [[ID]]– obsolete, notpopulated
The identification numbers of the ExchangeAgents that are registered for this security.
97 – 104 8 Character Trustee Agent [[ID]] The identification numbers of the TrusteeAgents that are registered for this security.
105 – 112 8 Character Tender Agent [[ID]] The identification numbers of the Tender Agentsthat are registered for this security.
113 – 113 1 Character MMI Indicator ForThe Issuing Agent Indicators that are set by the Issuing Agent.They appear only when the security is an MMIand are required because the Agent [[ID]] for MMIsis actually the [[participant]] [[ID]].
114 – 121 8 Character Issuing Agent The names and identification numbers of theIssuing Agents that are registered for thissecurity. The Agents are grouped by function.
122 – 129 8 Character [[DTC]] T/A DropAgent [[ID]] The names and identification numbers of theDTC Transfer Agents that are registered for thissecurity. The Agents are grouped by function.
130 – 137 8 Character External CustodianAgent The identification numbers of the ExternalCustodian Agents that are registered for thissecurity.
138 – 300 163 Character Filler Reserved for future use.
Agent Descriptive Message - A02
The next table describes the Agent Descriptive Message, which contains the [[DTC]] Agent [[ID]], firm name, and address.
Table 22  Agent Descriptive Message - A02
Position Length Format Field Name Description
1 – 3 3 Character Message Type Identifies the message type. The value is A02(Agent Descriptive Master Message).
4 – 9 6 Character Message Sequence Number Identifies the activity type of the Agent sorted inthe alphabetical order. Initialized to 000001.

---

## Page 16

1/30/24, 8:28 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm?Highlight="Bo… 16/18
Position Length Format Field Name Description
10 – 10 1 Character Message StatusType Indicates whether [[DTC]] is adding a newmessage or updating an existing message. Thevalues are:
A : Add
U: Update
11 – 19 9 Character Filler Reserved for future use.
20 – 31 12 Character Filler Reserved for future use.
32 – 39 8 Character Agent [[ID]] The [[DTC]] identification number for an agent.
40 – 41 2 Character Agent Type Agent Type
1: [[transfer agent]]
2: Paying Agent (non-MMI and MMI)
3: Redemption Agent
4: DDA
5: Trustee
31: Tender Agent
32: Remarketing Agent
55: MMI Issuing Agent
42 – 89 48 Character Agent Name The firm name for the agent
90 – 137 48 Character Agent Address 1 The street or suite address for the agent.
138 – 185 48 Character Agent Address 2 The street or suite address for the agent.
186 – 205 20 Character Agent City The city for the agent.
206 – 208 3 Character Agent State The state of operation for the agent. For moreinformation, see ISO United States andCanadian Provinces..
209 – 211 3 Character Agent Country Country of operation for Agent. For moreinformation, see ISO Country Codes..
212 – 220 9 Character Agent Zip The Postal Zip code.
221 – 229 9 Number ABA Number The American Bankers Association Number (ifapplicable).
230 – 234 5 Number Agent Postal Code The five-digit Postal Zip Code.
235-235 1 Character [[participant]] Agent Flag Indicates whether the agent [[ID]] is also aParticipant [[ID]] in the case of transfer or MMIAgents.
Y: Yes
N: No
Blank: No
236 – 300 65 Character Filler Reserved for future use.

---

## Page 17

1/30/24, 8:28 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm?Highlight="Bo… 17/18
Limited Eligibility Message – L01
The next table describes the Limited Eligibility Message, which only appears in the LTDMST file.
Table 23  Limited Eligibility Message – L01
Position Length Format Field Name Description
1 - 3 3 Character Message Type The type of Message. The value is L01 (LimitedElig).
4 - 9 6 Numeric Message Sequence Number Identifies the sequence number within themessage type. Initialized to 000001.
10 – 10 1 Character Message StatusType Indicates whether [[DTC]] is adding a newmessage or updating an existing message. Thevalues are:
A: Add
U: Update
11 – 19 9 Character Issue Identifier The 9-character [[CUSIP]] number.
20 – 31 12 Character International Identifier The 12-character ISIN (International SecuritiesIdentification Number) number.
32 – 32 1 Character Limited Eligibility flag Indicates whether or not the security is a“Limited Eligibility” Security.
Y: Yes
N: No
Blank: N/A or not available
33 –35 3 Character Eligibility  country 1 There can be up to five countries of eligibility.The three-digit ISO country code (for non-United States and territory [[securities]]) as a 3-character code will be used.The value will be spaces if no country is found.
36 –38 3 Character Eligibility  country2 There can be up to five countries of eligibility.The three-digit ISO country code (for non-United States and territory [[securities]]) as a 3-character code will be used.The value will be spaces if no country is found.
39 –41 3 Character Eligibility  country 3 There can be up to five countries of eligibility.The three-digit ISO country code (for non-United States and territory [[securities]]) as a 3-character code will be used.The value will  be spaces if no country is found.
42 –44 3 Character Eligibility  country 4 There can be up to five countries of eligibility.The three-digit ISO country code (for non-United States and territory [[securities]]) as a 3-character code will be used.The value will be spaces if no country is found.
45 –47 3 Character Eligibility  country5 There can be up to five countries of eligibility.The three-digit ISO country code (for non-United States and territory [[securities]]) as a 3char code will be used.The value will be spaces if no country is found.
Trailer Message - T01
The next table describe the Trailer Message, which is the last message that is attached to every file type.
Table 24  Trailer Message - T01
Position Length Format Field Name Description
1 – 3 3 Character Message Type Identifies the message type. The value isT01 (Trailer Message ).

---

## Page 18

1/30/24, 8:28 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm?Highlight="Bo… 18/18
Back to Top
Position Length Format Field Name Description
4 – 9 6 Character Message SequenceNumber Identifies the sequence number within themessage type. Initialized to 000001.
10 -17 8 Numeric Total Messages The total number of messages on the file,including the header, detail, and trailermessage types.
18 - 300 283 Character Filler Reserved for future use.