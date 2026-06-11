---
title: "Message Formats2.pdf"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Message%20Formats2.pdf"
pages: 36
size: "1082.9 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Message Formats2.pdf

**Original File:** [Message Formats2.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Message%20Formats2.pdf)  
**Category:** Other  
**Total Pages:** 36  
**File Size:** 1082.9 KB  

---

## Page 1

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 1/36
 eade essage  0
The next table describes the Header message, which is the initial message attached to every file type.
Table 14  [[issuer]] Message - D01
Position Length Format Field Name Description
1 – 3 3 Character Message Type Identifies the message type.The value is H01 (HeaderMessage).
4 – 9 6 Character MessageSequenceNumber
Identifies the sequencenumber within the messagetype. Initialized  to 000001.
10 – 17 8 Numeric File Date The date the file  wasprocessed in CCYYMMDDformat.
18 – 25 8 Character File Name The name of the file. Thevalues are provided in FileDescriptions and Acronyms.
26 – 300 273 Character Filler Reserved for future use.
International Message - I01
The next table describes the International Message, which is currently used exclusively for [[CSDS]] (Central Security
Depositories).
Table 15  [[issuer]] Message - D01
Position Length Format Field Name Description
1 – 3 3 Character Message Type The type of Message. Thevalue is I01 (International).
4 – 9 6 Numeric MessageSequence
Number
Identifies the sequencenumber within the
Message type. Initialized to000001.
10 – 10 1 Character MessageStatus Type Indicates if [[DTC]] is adding anew message or updating anexisting message.
A: Add
U: Update
M: Matured
11 – 19 9 Character Issue Identifier The 9-character CUSIPnumber.

---

## Page 2

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 2/36
Position Length Format Field Name Description
20 – 31 12 Character InternationalIdentifier(ISIN)
The 12-character ISIN(International SecuritiesIdentification Number) number,if available.
32 – 91 60 Character [[issuer]] Name The first occurrence of theformal [[issuer]] name
appearing on the Prospectusor Offering Statement that issupplied to [[DTC]] duringeligibility processing. Thisdescription provides aconsistent [[issuer]] name acrossthe issuance and issues. TheIssuer or Issuing Agent mayalso provide the description ifthe security does not gothrough the eligibility process(for example, for MBSsecurities).
92 – 94 3 Character [[issuer]] Countryof Origin The three-character ISOcountry code . The values arecontained in ISO CountryCodes.
95 – 95 1 Character Issue Type The type of security. Thevalues are:
1: [[Equity]]
5: Corporate Debt
7: Municipal Debt.
96 – 98 3 Character Sub-IssueType The type of issue or sub-issueused by [[DTC]] to classify asecurity. The values arecontained in [[DTC]] Sub-IssueTypes.
99 – 99 1 Character Deliver OrderChill ActivityFlag
Indicates whether the securityis eligible for [[DTC]] DeliverOrder activity. The values are:
Y: Yes
N: No
Blank: Not Applicable / Not Available
100 –
300
201 Character Filler Reserved for future use.
[[issuer]] Message - D01

---

## Page 3

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 3/36
The next table describes the [[issuer]] Message, which contains [[issuer]] information about the [[DTC]] search, as well as a short
description, state and domicile of issuance.
Table 16  [[issuer]] Message - D01
Position Length Format Field Name Description
1 – 3 3 Character Message Type The type of Message. Thevalue is D01 ([[issuer]]).
4 – 9 6 Numeric MessageSequenceNumber
Identifies the sequencenumber within the messagetype. This value is Initialized to000001.
10 – 10 1 Character MessageStatus Type Indicates whether [[DTC]] isadding a new Message orupdating an existing Message.
A: Add
U: Update
11 – 19 9 Character Issue Identifier The 9-character CUSIPnumber.
20 - 31 12 Character InternationalIdentifier The 12-character ISIN(International SecuritiesIdentification Number) number.
32 - 34 3 Character State ofIssuance The two-digit state code formunicipal and corporatesecurities issued in the UnitedStates, its territories andCanadian provinces. This fieldcontains the state code ofissuance for municipalsecurities, and the state codeof incorporation for corporatesecurities. The values arecontained in ISO United Statesand Canadian Provinces.
35 - 37 3 Character Country of
Issuance(IssuerCountry ofOrigin)
The three-digit ISO countrycode (for non-United
States and territory [[securities]]).The values are contained inISO Country Codes.

---

## Page 4

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 4/36
Position Length Format Field Name Description
38 - 97 60 Character [[issuer]] Name The first occurrence of theformal [[issuer]] name appearingon the Prospectus or OfferingStatement that is supplied toDTC during eligibilityprocessing. This descriptionprovides a consistent issuername across the issuance andissues. The [[issuer]] or IssuingAgent may also provide thedescription if the security doesnot go through the eligibilityprocess (for example, for MBSsecurities).
98 - 127 30 Character [[DTC]] Short
Description
The abbreviated securitydescription traditionally
supplied in [[DTC]] files.
128 –134 7 Character CorrespondingBase [[CUSIP]] Under the [[DTC]] MMI discountnumbering scheme program,issuers request dual base
CUSIPs from the CUSIPService Bureau. The baseCUSIPs are assigned andused based upon leap yearand subsequent even and oddyears.
These base [[CUSIP]] numbersallow the [[IPA]] to
seamlessly issue and processtransactions. TheCorresponding Base [[CUSIP]] isthe one associated with theselected security. Applicablefor MMI
[[securities]] only.
135 –135 1 Character Base CUSIPCheck Digit The check digit for the currentBase [[CUSIP]]. Applicable forMMI [[securities]] only

---

## Page 5

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 5/36
Position Length Format Field Name Description
136 -136
 
1
 
Character
 
Spanish Tax
WithholdingIndicator
Indicates whether the securityis subject to
Spanish Tax Withholdingregulations.
Y: Subject to Spanish TaxWithholding regulations.
Note: To limit Spanish taxwithholding, client name andcountry of residence will bedisclosed to theIssuer/Spanish Govt. DONOT PURCHASE IF YOUDO NOT CONSENT.
N: Blank: Not Applicable, Not Available
Under Spanish tax [[regulation]], investors in
preferred [[securities]], senior notes or
subordinated notes listed on an organized
market in an OECD country, with no tax
residency in Spain and not acting through
a permanent establishment in Spain, are
exempt from the Spanish Non-resident
Income Tax ("NRIT"), provided certain
information [[obligations]] relating to identity
and residence of beneficial owners entitled
to receive distributions are complied with.
If these information [[obligations]] are not
complied with, Spanish issuers have to
withhold the NRIT.
137 –300 164 Character Filler Reserved for future use.
Issuance Message - D02
The next table describes the Issuance Message, which contains issue date, currency, and issuance amount information.
Table 17  Issuance Message - D02
Position Length Format Field Name Description
1 – 3 3 Character Message Type The type ofMessage. Thevalue is D02(Issuance).
4 – 9 6 Numeric Message Sequence Number Identifies the sequence
number within the message
type. Initialized to 000001.

---

## Page 6

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 6/36
Position Length Format Field Name Description
10 – 10 1 Character Message Status
Type
Indicateswhether [[DTC]] isadding a new
message orupdating anexistingmessage.
A: Add
U: Update
11 – 19 9 Character Issue Identifier The 9-character [[CUSIP]]
number.
20 - 31 12 Character InternationalIdentifier (ISIN) The 12-characterISIN(InternationalSecuritiesIdentificationNumber) number.
32 – 39 8 Character Expected Issue
Date
Currently populated with
Dated Date The date
when the security is released
or sold
For [[Equity]] [[securities]] in
CCYYMMDD format.
For MMI- eligible
[[securities]] the Message
date is equivalent to the
issue date.
40 - 42 3 Character IssuanceCurrency The three-character ISOcurrency code ofthe certificate.The values arecontained in ISOCurrency Codes.
43 - 45 3 Character Income Currency The three-character ISO
currency code in which income
would be paid for a security.
The values are contained in
ISO Currency Codes.

---

## Page 7

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 7/36
Position Length Format Field Name Description
46 - 58 13 Numeric OriginalIssuance
Amount
The originaloffering amountthat does notinclude the overallotment ofshares in thenew issue. Thisamount typicallyapplies tomunicipals and isalways blank forMMI programs.In whole numberformat.
59 - 69 11 Numeric Offering [[shares]] The number of [[shares]] initially
issued for this security; for
[[Equity]] issues in whole number
format.
70 - 76 7 Numeric Offering Price The originaloffering shareprice; for [[Equity]]
issues in9(4)V9(3) format.
77 - 77 1 Character [[IPO]] Tracking Indicator A value that indicates whether
a lead manager requested [[IPO]]
tracking for this security.
Y: Yes
N: No
Blank: No Applicable /
Not Available
78 - 85 8 Numeric [[IPO]] Start Date The start date ofthe [[IPO]] tracking,in CCYYMMDDformat.
86 - 86 1 Character [[DTC]] Eligibility Indicator -
obsolete field, not supported
A value that indicates whether
the security is eligible for
[[DTC]]’s services.
Y: Yes
N: No
Blank: No Applicable /
Not Available

---

## Page 8

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 8/36
Position Length Format Field Name Description
87 - 94 8 Numeric ProspectusReceived The date thatDTC received aProspectus orOfferingStatement for agiven security.
Displayed inCCYYMMDDformat.
95 - 103 9 Numeric Minimum Denomination A numeric minimum
denomination for trading
(typically the number of [[shares]]
or [[Bonds]] or the principal
amount), in whole number
format.
104 - 112 9 Numeric MultipleDenomination A numericamount ofissuance foruniquelydenominatedsecurities, inwhole numberformat.
113 - 113 1 Character Issuance Indicator Indicates whether the
issuance is original or
secondary.  The values are:
O: Original
S: Secondary
Blank: Not Applicable /
Not Available
114 - 114 1 Character Issue StatusCode First PaymentIndicatorPossible values:
S: Short First Payment
L: Long First Payment
Y: Yearly
E: Payment Omitted
D: [[default]]
X: Extra Long
P: Possible [[default]]
Space: First Payment is
Regular/not
applicable/not available

---

## Page 9

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 9/36
Position Length Format Field Name Description
115-300 186 Character Filler Reserved for future use
Issue Message - D03
The next table describes the Issue Message, which contains specific information about:
coupon
maturity
registration
exchange
issue amount
amount outstanding
Table 18  Issue Message - D03
Position Length Format Field Name Description
1 - 3 3 Character Message Type The type of Message.The value is D03(Issue).
4 - 9 6 Numeric MessageSequence Number Identifies  the sequencenumber within themessage type.Initialized to 000001.
10 – 10 1 Character Message Status
Type
Indicates whether DTCis adding a new
message or updating anexisting message.
A: Add
U: Update
M: Matured
11 – 19 9 Character Issue Identifier The 9-character CUSIPnumber.
20 - 31 13 Character International
Identifier
The 12-character ISIN(International SecuritiesIdentification Number)number.

---

## Page 10

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 10/36
Position Length Format Field Name Description
32 - 44 13 Numeric Amount
Outstanding  -obsolete,defaulted tozeroes
The number ofsecurities (either paramount or [[shares]]) thatDTC “[[Cede & Co]]” islisted as the holder ofrecord, in whole numberformat. This informationis listed in par amountfor fixed incomesecurities and sharesfor [[Equity]] [[securities]].
45 - 51 7 Numeric Coupon/InterestRate The coupon or interestrate. This field does notappear for equitysecurities. The rate is in9(3)V9(6)format. Thefield  is zero-filled fordiscount program MMIsecurities and otherswithout a rate. Forvariable rate [[securities]],the value is indicated asone cent.
52 - 59 8 Numeric Maturity Date The maturity date inCCYYMMDD format.
60 - 67 8 Numeric Dated Date/ Dated Date - Date fromwhich Interest startsaccruing for debtinstruments inCCYYMMDD format:
68 - 68 1 Character Registration Type The registration type ofa security.
B: Bearer
E, U, X: Book Entry
A, D, I: Interchangeable
M, R: Fully Register
69 - 69 1 Character Taxable Indicator A value that indicateswhether the security issubject to federalincome taxes; formunicipal securitiesonly.
Y: Yes
N: No
Blank: Not Applicable / Not
Available

---

## Page 11

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 11/36
Position Length Format Field Name Description
70 - 70 1 Character Rule 144AIndicator A value that indicateswhether a security isissued under [[SEC]]  Rule144A as a privateplacement.
Y: Yes
N: No
Blank: Not Applicable / Not
Available
71 - 71 1 Character [[regulation]] SIndicator A value that indicateswhether the security issubject to [[regulation]] Sof the Federal ReserveBoard.
Y: Yes
N: No
Blank: Not Applicable / Not
Available
72 – 72 1 Character Rule 3c-7 Indicator A value that indicateswhether a security isrelying on theexemption from Section3(C.)(7) of theInvestment CompanyAct of 1940.
Y: Yes
N: No
Blank: Not Applicable / Not
Available
73 - 80 8 Numeric First Interest PayDate - defaulted tozeroes
The first interest paydate for a fixed incomesecurity, inCCYYMMDD format.
81 – 90 10 Character Ticker Symbol An arrangement ofcharacters (usuallyletters) representing aparticular security listedon an exchange orotherwise tradedpublicly. Only thePrimary ExchangeTicker Symbol isdisplayed.

---

## Page 12

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 12/36
Position Length Format Field Name Description
91 - 105 15 Character Exchange The exchange on whichthe security you wantinformation about islisted. The values are:
AMEX: American [[Stock]]
Exchange
[[NYSE]]: New York [[Stock]]
Exchange
[[OTC]]: Over the Counter
[[NASDAQ]]: National Association
of [[securities]] Dealers Automated
Quote.
106 - 115 10 Character Pool [[ID]] The identifier applied tomortgage-backedsecurities.
116 - 116 1 Character Global Issue A value that indicateswhether the securityuses foreign clearanceor [[settlement]].
Y: Yes
N: No
Blank: Not Applicable / Not
Available
117 - 117 1 Character Issue Type Identifies the type ofsecurity. The values are:
1: [[Equity]]
5: Corporate Debt
7: Municipal Debt
118 –120 3 Character Sub-Issue Type The type of issue orsub-issue used by DTCto classify a security.The values arecontained in .
Appendix I - [[DTC]] Sub-Issue Types.
121 - 121 1 Character Put Indicator A value that indicateswhether the issue has aput feature.
Y: Yes
N: No
Blank: Not Applicable / Not
Available

---

## Page 13

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 13/36
Position Length Format Field Name Description
122 - 122 1 Character Call Indicator A value that indicateswhether the issue issubject to a callredemption.
Y: Yes
N: No
Blank: Not Applicable / Not
Available
123 - 123 1 Character Sinking Fund
Indicator
A value that indicateswhether a sinking fundprovision applies to thissecurity.
Y: Yes
N: No
Blank: Not Applicable / Not
Available
124 - 124 1 Character PrerefundedIndicator A value that indicateswhether an issue hasfunds that have beenput aside to redeem theissue at its earliest calldate.
Y: Yes
N: No
Blank: Not Applicable / Not
Available
125 - 125 1 Character Principal
AmortizationIndicator
A value that indicateswhether the principal issubject to amortization.
Y: Yes
N: No
Blank: Not Applicable / Not
Available
126 - 126 1 Character Indexed PrincipalIndicator (MMIsOnly)
A value that indicateswhether the interestpayments are linked toan index.
Y: Yes
N: No
Blank: Not Applicable / Not
Available

---

## Page 14

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 14/36
Position Length Format Field Name Description
127 - 127 1 Character Renewable NoteIndicator (MMIsOnly)
A value that indicateswhether a MTN has arenewable feature.
Y: Yes
N: No
Blank: Not Applicable / Not
Available
128 - 128 1 Character Interest Step-upIndicator (MMIsOnly)
A value that indicateswhether the securityhas an interest ratestep-up feature.
Y: Yes
N: No
Blank: Not Applicable / Not
Available
129 - 129 1 Character Interest ResetIndicator (MMIsOnly)
A value that indicateswhether the securityhas a rate reset feature.
Y: Yes
N: No
Blank: Not Applicable / Not
Available
130 - 130 1 Character ChangeablePayment Indicator(MMIs Only)
A value that indicateswhether the securitycan modify the paymentamount or date.
Y: Yes
N: No
Blank: Not Applicable / Not
Available
131 - 143 13 Numeric Issue Amount The amount issuedspecific to this security,in whole number format.Often a subset of theOriginal Issuance.

---

## Page 15

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 15/36
Position Length Format Field Name Description
144 - 144 1 Character Foreign OrdinaryProcessingIndicator
A value that indicateswhether the security iseligible for foreignordinary processing.
Y: Yes
N: No
Blank: Not Applicable / Not
Available
145-146 2 Character MBS Product [[ID]] Describes the DifferentTypes of MBS
[[Bonds]]. For values, seeMBS Product [[ID]] Values.
147-148 2 Character MBS Category [[ID]] The Classification of thedifferent terms thatapply to MBS [[Bonds]].For values, see MBSProduct [[ID]] Values.
149-149 1 Character Tax Credit in Lieuof InterestIndicator
This field identifieswhether a security is aBuild America Bond thathas a Tax Creditfeature.
Y: Yes
N: No
150-150
 
1
 
Character
 
Tax Credit BondType
 
This field identifies thepayment featuresassociated with a TaxCredit security
1: Combo for redemption and tax
credit.
2: Combo for redemption, tax
credit and interest.
3: Strip for tax credit.
4: strip for redemption
5: Strip for redemption and
interest.
6: Strip for interest

---

## Page 16

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 16/36
Position Length Format Field Name Description
151-159 9 Numeric Tax Credit Rate This field will containthe actual Tax Creditrate for the security. Thefirst three digitsrepresent dollars. Thelast six digits in the fieldrepresent cents.
160-162 3 Numeric Tax Credit RecordDate – Number ofDays
This is the number ofdays the record date isgoing to be offset fromthe payment date.
163-163 1 Character Tax Credit RecordDate – Number ofDays -
Business/CalendarIndicator
This indicates whetherthe Record Date offsetis specified as numberof business or calendardays.
B: Business
C: Calendar
164-171 8 Character Tax Credit RecordDate – Fixed Date This is the two pre-established recorddates for the security.
The first four bytes contain the
first record date with a format
MMDD
The last four bytes contain the
second record date with the
same format MMDD.
Format MMDDMMDD
172-172 1 Character Tax CreditPaymentFrequency
This is the statedfrequency for paymentsfor the security.
1: Annual
2: Semi-annual
4: Quarterly,
8: Monthly
173-180 8 Character Tax Credit FirstPayment Date This is the date whenthe first interestpayment on this securityis due.
Format CCYYMMDD

---

## Page 17

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 17/36
Position Length Format Field Name Description
181-181 1 Character [[Stock]] for MaturityIndicator This field indicateswhether a bond has theoption to pay Maturityproceeds as Stockinstead of Cash.
Y: Yes
N: No
182-182 1 Character Extended MaturityIndicator This field indicateswhether a bond has theoption of extending itsstated Maturity Date.
Y: Yes
N: No
183-183 1 Character Sovereign DebtIndicator This field identifies abond as beingSovereign Debt, issuedby a non-US Sovereignentity.
Y: Yes
N: No
184 –300 117 Character Filler Reserved for future use.

---

## Page 18

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 18/36
Descriptive Message - D05
The next table details the Descriptive Message, which contains formal issuance description information derived from
[[DTC]]'s eligibility process. This description comes from the prospectus or offering filing. In some cases, this description is
supplied to [[DTC]] directly from contributors such as the MMI system, and therefore may not represent a formal description.
Table 19  Descriptive Message - D05
Position Length Format Field Name Description
1 - 3 3 Character MessageType The type of Message. Thevalue is D05 (Descriptive).
4 - 9 6 Numeric MessageSequenceNumber
Identifies the sequencenumber within themessage type. Initializedto 000001.
10 – 10 1 Character MessageStatus
Type
Indicates whether [[DTC]] isadding a new
message or updating anexisting message.
A: Add
U: Update
11 – 19 9 Character IssuerIdentifier The 9-character CUSIPnumber.
20 – 31 12 Character InternationalIdentifier The 12-character ISIN(International SecuritiesIdentification Number)number.
32 – 91 60 Character IssueDescription The security description,which is the formal Issuername appearing on theProspectus or OfferingStatement that is suppliedto [[DTC]] during eligibilityprocessing. The [[issuer]] or
Issuing Agent may alsoprovide the
description if the securitydoes not go through theeligibility process (forexample, for MBS
[[securities]]). This fieldconsists of the first of thefour lines (60 bytes each)of information.

---

## Page 19

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 19/36
Position Length Format Field Name Description
92 – 271 180 Character IssueDescription This field consists of thenext three of the four lines(60 bytes each) ofinformation.
272 –300 29 Character Filler Reserved for future use.

---

## Page 20

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 20/36
Depository Status Message - D06
The next table describes the Depository Status Message, which contains [[DTC]] processing and status information for the
security.
Table 20  Depository Status Message
Position Length Format Field Name Description
1 – 3 3 Character Message Type The type of Message. Thevalue is D06 (DepositoryStatus).
4 – 9 6 Numeric MessageSequence Number Identifies the sequencenumber within themessage type. Initializedto 000001.
10 – 10 1 Character Message StatusType Indicates whether [[DTC]] isadding a new message orupdating an existingmessage.
A: Add
U: Update
11 – 19 9 Character Issue Identifier The 9-character CUSIPnumber.
20 – 31 12 Character InternationalIdentifier The 12-character ISIN(International SecuritiesIdentification Number)number.
32 – 32 1 Character Same Day Fund
SettlementEligibility Indicator–obsolete field,not supported
A value that indicateswhether the security iseligible to settle in same-day funds.
Y: Yes
N: No
33 – 33 1 Character [[FAST]] COD & WT [[FAST]] COD & WT. A valuethat indicates if the issueis eligible for [[DTC]]'s FASTCOD & WT (Full [[FAST]])service.
Y: Yes, Full [[FAST]]
N: No, Not Full [[FAST]]

---

## Page 21

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 21/36
Position Length Format Field Name Description
34 – 34 1 Character [[Dividend]]
ReinvestmentService EligibilityIndicator
A value that indicateswhether the [[CUSIP]] iseligible for [[DTC]]'sDividend Reinvestmentservice.
Y: Yes
N: No
Blank: Not Applicable / Not
Available
35 – 35 1 Character [[custody]] ServiceEligibility Indicator A value that indicateswhether the [[CUSIP]] iseligible for [[DTC]]'s Custodyservice.
Y: Yes
N: No
Blank: Not Applicable / Not
Available
36 – 36 1 Character Federal Book- BookEntry EligibilityIndicator
A value that indicateswhether the [[CUSIP]] is FedBook eligible.Book
Y: Yes
N: No
Blank: Not Applicable / Not
Available
37 – 37 1 Character Direct RegistrationEligibility Indicator A value that indicateswhether the [[CUSIP]] iseligible for [[DTC]]'s DirectRegistration service.
Y: Yes
N: No
Blank: Not Applicable / Not
Available

---

## Page 22

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 22/36
Position Length Format Field Name Description
38 – 38 1 Character CommunicationsIssue Indicator A value that indicateswhether the issue is acommunications issue.
Y: Yes
N: No
Blank: Not Applicable / Not
Available
39 – 39 1 Character Deposit Activity
Chill Indicator
Indicates that this securityis locked from any
deposit activity at [[DTC]].
Y: Yes
N: No
40 – 40 1 Character Chill COD Indicates that this securityis locked from any
COD (Certificate ondemand) activity at [[DTC]].
Y: Yes
N: No
41 – 41 1 Character Chill WT Indicates that this securityis locked from any WT(withdrawals-by-transfer)activity at [[DTC]].
Y: Yes
N: No
42 – 42 1 Character Chill [[DO]] Indicates that this securityis locked from any
[[DO]] (Deliver Order)activity at [[DTC]].
Y: Yes
N: No

---

## Page 23

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 23/36
Position Length Format Field Name Description
43 – 43 1 Character Chill Segregation Indicates that this securityis locked from anysegregation activity atDTC.
Y: Yes
N: No
44 –44 1 Character Pledge ChillIndicator Indicates that this securityis locked from any pledgeactivity at [[DTC]].
Y: Yes
N: No
45 – 45 1 Character Thin IssueIndicator A value that indicateswhether the issue is a thinissue.
Y: Yes
N: No
Blank: Not Applicable / Not
Available
46 – 65 20 Character Reserved Reserved for future use.

---

## Page 24

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 24/36
Position Length Format Field Name Description
66 – 66 1 Character Fractional Dollars/Cents Eligible Indicates if the securitycan contain FractionalShare/amountcomponent.
Y: Yes
N: No
Blank: Not Applicable / Not
Available
A fractional share is a unitof [[Stock]] that is less thanone full share. Forexample., if a shareholderparticipates in a dividendreinvestment programand the dividends beingreinvested are notenough to purchase a fullshare at the market price,the shareholder will becredited with a fractionalshare until enoughdividends accrue topurchase one full share.
67 – 67 1 Character Segregation 100Number EligibilityIndicator
A value that indicateswhether the issue is asegregated 100 issue.
Y: Yes
N: No
Blank: Not Applicable / Not
Available
68 – 68 1 Character Auto CertificationEligibility Indicator A value that indicateswhether the issue iseligible for [[DTC]]'s autocertification program.
Y: Yes
N: No
Blank: Not Applicable / Not
Available

---

## Page 25

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 25/36
Position Length Format Field Name Description
69 – 69 1 Character Non-Transferable
Issue
Information about thestatus of whether asecurity can be moved ortransferred betweenparticipants.
70 – 70 1 Character Record DateWeekend/HolidayIndicator
Indicates the method bywhich the record date willbe adjusted if it falls on aholiday or weekend.
B: Before
A: After
Blank: Not Applicable / Not
Available
71 – 71 1 Character Record Date
Business/CalendarIndicator
Indicates whether theRecord Date offset isspecified as number ofbusiness or calendardays The values are:
B: Business
C: Calendar
Blank: Not Applicable / Not
Available
72 – 119 48 Character [[DTC]] Description(Long) The 48-character DTCissue description.
120 -139 20 Character [[DTC]] Description(Short) The 20-character DTCshort issue description,typically system-generated.
140 -147 8 Character Vault Location The location of securitiesheld by [[Cede & Co]].
148 -150 3 Character Coupon Number The next Coupon Number(applicable for Bearer andInterchangeablecertificates).

---

## Page 26

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 26/36
Position Length Format Field Name Description
151-151 1 Character Networking forEquities Indicator -obsolete???
Indicates whether thesecurity is eligible forDTCC's Networking forEquities program. :
N: Security is not eligible for the
Networking for Equities program.
Y: Security is eligible for the
Networking for Equities program.
152-152 1 Character [[FAST]] WT A value that indicates ifthe issue is eligible forDTC's [[FAST]] WT serviceonly.
Y: Yes
N: No
153-153 1 Character Book Entry OnlyBookSecurity DRSEligibility  Indicator
0: Security is eligible for "WT" in
statement form only at [[DTC]].
Certificates are available at the
[[transfer agent]].
1: Security is eligible for "WT" in
statement form only.
2: Security is [[DRS]] eligible but not
participating. Certificates only are
available.
Note: A “space” in thisfield indicates that theissue is not [[DRS]]-eligible.
154 -154 1 Character Filler Reserved for future use.

---

## Page 27

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 27/36
Position Length Format Field Name Description
155-155 1 Character [[OA]] Rate TimelinesAttestation Code
1: Conforming [[CUSIP]]
2, 3: Non conforming [[CUSIP]]
This field is applicableonly for Sub-Issue Type‘540’ CMO and ‘541’ [[ABS]]
Where:
Conforming means thatthis security is structuredin a way that makes itlikely for the final rate tobe calculated anddisseminated to [[DTC]] priorto the payable date.
-and-
Non-conforming meansthat this security isstructured in a way thatmakes it unlikely for thefinal rate to be calculatedand
disseminated to [[DTC]] priorto the payable date.
156-156
 
1
 
Character
 
[[CNS]] Eligibility
Indicator
 
Indicates whether asecurity is eligible forContinuous NetSettlement ([[CNS]]) throughNSCC.
Y: Yes
N: No
157-157 1 Character OFAC SanctionedIndicator Indicates if security isrestricted due to OFACsanctions.
Y: Yes
N: No

---

## Page 28

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 28/36
Position Length Format Field Name Description
158-158 1 Character Global LockIndicator This field indicates if thesecurity is frozen andglobally locked from anyactivity at [[DTC]].
Y: Yes, the Security is globally
locked.
N: No, the Security is not globally
locked.
159-159 1 Character Global LockReason This field provides areason for the GlobalLock.
Space: Security is not globally
locked. Reason is not applicable
0: [[DTCC]]-Applied Global Lock
1: [[DTCC]]-Applied Global Lock -
Compliance Related.
2-9: Reserved for future use.
160-207 48 Character Unit ComponentRatio Text Box Specifies the ratio ofunits to each of itscomponents. Applicablefor sub-issue types '780'[[Equity]] Unit’ (EquityIssue type) and '781'Debt Unit’ (CorporateBond Issue type)
208-208 1 Character Deposit Chill
Reason
This field provides areason for the DepositChill.
Space:  Security does not have
a Deposit Chill. Reason is not
applicable.
0: [[DTCC]]-Applied Deposit Chill.
1: [[DTCC]]-Applied Deposit Chill -
Compliance Related.
2-9: : Reserved for future use.

---

## Page 29

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 29/36
Position Length Format Field Name Description
209-209 1 Character 871(m)Transaction Indicates if the securityis subject to regulation871(m).
Valid values:
Y: yes
N: No
Space: Not applicable/ not
available
210-210 1 Character Contract Type Contract Type for871(m) Transaction.
Valid values:
S: Simple
C: Complex
Space: Not applicable
211-217 7 Numeric Delta The value of Delta forSimple Contract Type(the “delta” of aninstrument is a measureof the relationshipbetween changes invalue of the instrumentand changes in value ofthe underlying [[Stock]]).
Format: 9(1)V9(6)format, up to 6 decimalpoints.
Valid values: from0800000 (0.8) to1000000 (1.0) [[default]] =zeroes
218-300 83 Character Filler Reserved for future use.
Agent Message - A01
The next table describes the Agent Message, which identifies the agent(s) involved with the security. The agent identifier
is blank if an agent is not applicable for a given security.
Table 21  Agent Message - A01
Position Length Format Field Name Description

---

## Page 30

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 30/36
Position Length Format Field Name Description
1 - 3 3 Character Message Type The type of Message. Thevalue is A01 (Agent).
4 – 9 6 Numeric MessageSequence
Number
Identifies  the sequencenumber within the messagetype. Initialized to 000001.
10 – 10 1 Character MessageStatus Type Indicates whether [[DTC]] isadding a new message orupdating an existing message.
A: Add
U: Update
11 – 19 9 Character Issue Identifier The 9-character CUSIPnumber.
20 – 31 12 Character InternationalIdentifier The 12-character ISIN(International SecuritiesIdentification Number) number.
32 – 39 8 Character DDA Agent [[ID]] The identification number ofthe [[Dividend]] DisbursingAgents that are registered forthis security.
40 –40 1 Character MMI IndicatorFor PayingAgent
Indicates whether the PayingAgent is an MMI Paying Agent,and their identification numberis actually a [[participant]] [[ID]].The values are:
Y: Yes
N: No
Blank: Not Applicable / Not Available
41 – 48 8 Character Paying AgentID The identification numbers ofthe Paying Agents that areregistered for this security.
49 – 56 8 Character Transfer AgentID The identification numbers ofthe Transfer Agents that areregistered for this security.
57 – 64 8 Character RemarketingAgent [[ID]] The identification numbers ofthe Remarketing Agents thatare registered for this security.The Remarketing Agent [[ID]] isthe same as a [[participant]] [[ID]].

---

## Page 31

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 31/36
Position Length Format Field Name Description
65 – 72 8 Character RedemptionAgent [[ID]] The identification numbers ofthe Redemption Agents thatare registered for this security.
73 – 80 8 Character ConversionAgent
[[ID]] – obsolete,not populated
The identification numbers ofthe Conversion Agents that areregistered for this security.
81 – 88 8 Character InformationAgent [[ID]] –obsolete, notpopulated
The identification numbers ofthe Information Agents that areregistered for this security.
89 – 96 8 Character ExchangeAgent [[ID]]
– obsolete,not populated
The identification numbers ofthe Exchange Agents that areregistered for this security.
97 – 104 8 Character Trustee AgentID The identification numbers ofthe Trustee Agents that areregistered for this security.
105 –112 8 Character Tender AgentID The identification numbers ofthe Tender Agents that areregistered for this security.
113 –113 1 Character MMI IndicatorFor TheIssuing Agent
Indicators that are set by theIssuing Agent. They appearonly when the security is anMMI and are required becausethe Agent [[ID]] for MMIs isactually the [[participant]] [[ID]].
114 –121 8 Character Issuing Agent The names and identificationnumbers of the Issuing Agentsthat are registered for thissecurity. The Agents aregrouped by function.
122 –129 8 Character [[DTC]] T/A DropAgent [[ID]] The names and identificationnumbers of the [[DTC]] TransferAgents that are registered forthis security. The Agents aregrouped by function.
130 –137 8 Character ExternalCustodianAgent
The identification numbers ofthe External Custodian Agentsthat are registered for thissecurity.
138 –300 163 Character Filler Reserved for future use.

---

## Page 32

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 32/36
Agent Descriptive Message - A02
The next table describes the Agent Descriptive Message, which contains the [[DTC]] Agent [[ID]], firm name, and address.
Table 22  Agent Descriptive Message - A02
Position Length Format Field Name Description
1 – 3 3 Character MessageType Identifies the message type.The value is A02 (AgentDescriptive Master Message).
4 – 9 6 Character MessageSequenceNumber
Identifies the activity type ofthe Agent sorted in thealphabetical order. Initialized to000001.
10 – 10 1 Character MessageStatus
Type
Indicates whether [[DTC]] isadding a new
message or updating anexisting message. The valuesare:
A : Add
U: Update
11 – 19 9 Character Filler Reserved for future use.
20 – 31 12 Character Filler Reserved for future use.
32 – 39 8 Character Agent [[ID]] The [[DTC]] identification numberfor an agent.
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
90 – 137 48 Character AgentAddress 1 The street or suite address forthe agent.

---

## Page 33

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 33/36
Position Length Format Field Name Description
138 –185 48 Character AgentAddress 2 The street or suite address forthe agent.
186 –205 20 Character Agent City The city for the agent.
206 –208 3 Character Agent State The state of operation for theagent. For more information,see ISO United States andCanadian Provinces..
209 –211 3 Character Agent Country Country of operation for Agent.For more information, see ISOCountry Codes..
212 –220 9 Character Agent Zip The Postal Zip code.
221 –229 9 Number ABA Number The American BankersAssociation Number (if
applicable).
230 –234 5 Number Agent PostalCode The five-digit Postal Zip Code.
235-235 1 Character ParticipantAgent Flag Indicates whether the agent IDis also a [[participant]] [[ID]] in thecase of transfer or MMIAgents.
Y: Yes
N: No
Blank: No
236 –300 65 Character Filler Reserved for future use.

---

## Page 34

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 34/36
Limited Eligibility Message – L01
The next table describes the Limited Eligibility Message, which only appears in the LTDMST file.
Table 23  Limited Eligibility Message – L01
Position Length Format Field Name Description
1 - 3 3 Character Message Type The type of Message. Thevalue is L01 (Limited Elig).
4 - 9 6 Numeric MessageSequenceNumber
Identifies the sequencenumber within the messagetype. Initialized to 000001.
10 – 10 1 Character MessageStatus
Type
Indicates whether [[DTC]] isadding a new message orupdating an existing message.The values are:
A: Add
U: Update
11 – 19 9 Character Issue Identifier The 9-character CUSIPnumber.
20 – 31 12 Character InternationalIdentifier The 12-character ISIN(International SecuritiesIdentification Number) number.
32 – 32 1 Character LimitedEligibility flag Indicates whether or not thesecurity is a “Limited Eligibility”Security.
Y: Yes
N: No
Blank: N/A or not available
33 –35 3 Character Eligibility country 1 There can be up to fivecountries of eligibility. Thethree-digit ISO country code(for non- United States andterritory [[securities]]) as a 3-character code will be used.
The value will be spaces if nocountry is found.

---

## Page 35

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 35/36
Position Length Format Field Name Description
36 –38 3 Character Eligibility country
2
There can be up to fivecountries of eligibility.
The three-digit ISO countrycode (for non- United Statesand territory [[securities]]) as a 3-character code will be used.
The value will be spaces if nocountry is found.
39 –41 3 Character Eligibility country 3 There can be up to fivecountries of eligibility. Thethree-digit ISO country code(for non- United States andterritory [[securities]]) as a 3-character code will be used.
The value will  be spaces if nocountry is found.
42 –44 3 Character Eligibility country 4 There can be up to fivecountries of eligibility. Thethree-digit ISO country code(for non- United States andterritory [[securities]]) as a 3-character code will be used.
The value will be spaces if nocountry is found.
45 –47 3 Character Eligibility country
5
There can be up to fivecountries of eligibility.
The three-digit ISO countrycode (for non- United Statesand territory [[securities]]) as a 3char code will be used.
The value will be spaces if nocountry is found.
Trailer Message - T01
The next table describe the Trailer Message, which is the last message that is attached to every file type.
Table 24  Trailer Message - T01
Position Length Format Field Name Description
1 – 3 3 Character MessageType Identifies the messagetype. The value is T01(Trailer Message ).

---

## Page 36

1/30/24, 8:39 PM Message Formats
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/sec_mas_file_data_serv/basic_premium/msg_format.htm 36/36
Position Length Format Field Name Description
4 – 9 6 Character MessageSequenceNumber
Identifies the sequencenumber within themessage type. Initializedto 000001.
10 -17 8 Numeric TotalMessages The total number ofmessages on the file,including the header,detail, and trailer messagetypes.
18 - 300 283 Character Filler Reserved for future use.