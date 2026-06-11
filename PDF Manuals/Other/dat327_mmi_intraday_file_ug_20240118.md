---
title: "Security Master File Data - MMI IntraDay Securities File Specification"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/dat327_mmi_intraday_file_ug_20240118.pdf"
pages: 28
size: "281.2 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Security Master File Data - MMI IntraDay Securities File Specification

**Original File:** [dat327_mmi_intraday_file_ug_20240118.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/dat327_mmi_intraday_file_ug_20240118.pdf)  
**Category:** Other  
**Total Pages:** 28  
**File Size:** 281.2 KB  

---

## Page 1

SecurityMasterFileData
MMIINTRADAYFILEUSERGUIDE
JANUARY18,2024

---

## Page 2

TABLEOFCONTENTS
Summary 3
FileDelivery 4
DeliveryMethod 4
DeliveryTimes 4
MMIIntradaySecuritiesFileStructure 5
HeaderRecord 5
DataRecordLayout 7
TrailerRecord 26
Sub-IssueTypes 27

---

## Page 3

SUMMARY
TheMMIIntradaySecuritiesFileisaconsolidationoftheexistingMMIMSTandMMIECMfilesintoa
comprehensivefile,improvingthequalityoftheMMIReferenceFile.AnalysisoftheSMFDatabase,the
MMIMST,andtheMMIECMfilewereconductedinordertocomeupwiththebest-in-classdataelements,
inparticular,shorttermMMIwithone-andtwo-daymaturities.DuetoDTCCupdatesoccurringat7:30PM
EST,manyMMItradesfail.Basedonmarketfeedback,thisfilewillbeavailableintra-day,enablinggreater
STPandincreasedbackofficeefficiency. DTCCcurrentlyhastwoMMImasterfilesthatcontaincommon
anddisparatedataelements.DTCChasreviewedbothfilesandhavecomeupwithasetoffieldsfora
newfilethatbridgesthegapsbetweenthem.
SecurityMasterFileData- MMIIntraDayFileUserGuide
Summary 3

---

## Page 4

FILEDELIVERY
DeliveryMethod
SFTP
DeliveryTimes
FileName/Number DeliveryTimes
IntradayFile–02772483 l Every30minutes,startingat8:00AMESTthrough4:00PMEST
l 7:30PMEST(aftercompletionoftheDTCEndofDayPositioncal-
culationprocess)
MonthlyMasterFile–
02772482
Monthly,onthelastSaturdayofthemonth,afterwhichitisavailablefortwoweeks
Note
Eachfileslicewillbecumulative,meaningthatitwillcontainallofthedatafromthepreviousslices.The
fileswillnotbedelta-onlyfiles.TheEndofDayfilewillbeacumulativefileofALLpreviousslices.
SecurityMasterFileData- MMIIntraDayFileUserGuide
FileDelivery 4

---

## Page 5

MMIINTRADAYSECURITIESFILE
STRUCTURE
HeaderRecord
TheHeadermessageprovidesdetailsregardingthefile,creationdate,andtotalnumberofrecords.
FieldName Length Start End Type Comments
HeaderID 6 1 6 A/N Always=1TRANS
ApplicationDate 8 7 14 NUM CCYYMMDD
Reserved 2 15 16 Donotuse
ProductNumber 3 17 19 NUM
ProductDescription 20 20 39 A/N Alphaproductdescription
Reserved 3 40 42 Donotuse
Reserved 1 43 43 Donotuse
Multi-cycle
Transmissioncounter
2 44 45 A/N l 01-99:Logicalmulti-cyclecount
ofthejobsent
l Spaces:Notmulti-cycle
PossdupeIndicator 1 46 46 A/N l Space:Originaltransmission
l 1:PossibleduplicatebyDTCC
ProductID 8 47 54 NUM 8-digitcodeissuedbyDTCCtoidentifythe
reportorfile
HeaderRecord
SecurityMasterFileData- MMIIntraDayFileUserGuide
MMIIntradaySecuritiesFileStructure 5

---

## Page 6

FieldName Length Start End Type Comments
Application’smulti-cycle
counter
2 55 56 NUM l 1,2,…97:Applicationsthat
providemorethanoneoutputper
dayhaveasequentialnumber
foreachoutput.Thefinaloutput
cyclenumberforaday=98.
l Space=Notmulticycle
RecipientID 7 57 63 A/N Thiscodeisassignedtothedestinationof
thistransmission.Itnormallybeginswith
four-digitbrokerIDnumber.
Constant 1 64 64 NUM Always=0(zeros).
ContainsothervaluesforDTCCinternal
distribution.
RecordCount 9 65 73 NUM Numberofdatarecordsorprintlinesthat
follow
SenderID 4 74 77 A/N Always=[[DTCC]]
Constant 3 78 80 A/N Always=CDT
Lastfieldofthe80-byteRJEheader
Reserved 1 81 81 Donotuse
DateCreated 8 82 89 A/N MMDDCCYY
Reserved 3 90 92 Donotuse
TimeCreated 5 93 97 A/N HH:MM
Reserved 4 98 101 Donotuse
Constant 3 102 104 A/N Always=RDT
Reserved 1 105 105 Donotuse
DateReleased 8 106 113 A/N MMDDCCYY
Filetransmissiondate
HeaderRecord(continued)
SecurityMasterFileData- MMIIntraDayFileUserGuide
MMIIntradaySecuritiesFileStructure 6

---

## Page 7

FieldName Length Start End Type Comments
Reserved 3 114 116 Donotuse
TimeReleased 5 117 121 A/N HH:MM
Filetransmissiontime
Reserved 12 122 133 Donotuse
Filler N 133 N Donotuse–paddingtomatchfilerecord
size
HeaderRecord(continued)
DataRecordLayout
ThenexttabledescribesthefileformatinwhichDTCsecurityreferencedataisprovided.
FieldName Description Values [[default]]
Value
Format Length
MessageStatus
Type
l Indicatesif
DTCisadding
anewmes-
sageorupdat-
inganexisting
message.
l Indicatesthe
typeof
update,orthat
thisisa
Master
record.
l A:MasterFile
record(formas-
terfileonly)
l A:Add
l U:Update
l M:Matured(for
deltafilesonly)
Mandatory character 1
[[CUSIP]] A9-character
alphanumericcode
thatidentifiesaNorth
Americanfinancial
securityforthe
purposesoffacilitating
clearingand
settlementoftrades/
Mandatory character 9
DataRecordLayout
SecurityMasterFileData- MMIIntraDayFileUserGuide
MMIIntradaySecuritiesFileStructure 7

---

## Page 8

FieldName Description Values [[default]]
Value
Format Length
IssueType Identifiesthehigh-
levelfinancial
instrument
classification,suchas
[[Equity]],Corporate
Bond,orMuniBond.
l 1:[[Equity]]
l 5:Corporate
Bond,
l 7:Municipal
Bond
Mandatory character 1
Sub-IssueType TheproprietaryDTCC
methodofclassifying
securitiesintosub-
categoriesbasedon
sharedqualitiesand
characteristics.
Mandatory character 3
ShortDescription Free-formtext
describingasecurity.
Mandatory character 20
LongDescription Free-formtext
indicatingthegeneral
security
characteristicsand
[[issuer]].
Mandatory character 48
InterestRatetype AClassification
Schemethat
distinguishesbetween
InterestRate
Conditionsaccording
tothenatureofthe
interest.
l F
l V
Space character 1
InterestRate Thechargeforthe
privilegeofborrowing
moneyviafinancial
instrumentissuance,
expressedas
percentagerate.
Zeroes numeric 9
DataRecordLayout(continued)
SecurityMasterFileData- MMIIntraDayFileUserGuide
MMIIntradaySecuritiesFileStructure 8

---

## Page 9

FieldName Description Values [[default]]
Value
Format Length
Interestpayment
type
Asetoffinancial
instrument
characteristics
referringtothe
amountandtimingfor
repaymentofprincipal
andinterest.
l I
l D
l P
Space character 1
DatedDate Datefromwhich
Interestfordebt
instrumentsstarts
accruing.
FormatisCCYYMMDD. ‘00000000’ character 8
MaturityDate IdentifiesaProduct's
maturity(enddate),
whichdetermines
whenallliabilities
mustbepaid.
FormatisCCYYMMDD. ‘00000000’ character 8
ExtendedMaturity
Indicator
IdentifiesaProduct
ActivityEvent,which
definesanextension
tothematuritydate.
l Y
l N
l space
Space character 1
Prerefunded
Indicator
Avaluethatindicates
whetheranissuehas
fundsthathavebeen
putasidetoredeem
theissueatitsearliest
calldate.
l Y
l N
l space
Space character 1
DataRecordLayout(continued)
SecurityMasterFileData- MMIIntraDayFileUserGuide
MMIIntradaySecuritiesFileStructure 9

---

## Page 10

FieldName Description Values [[default]]
Value
Format Length
MMIMaturityDate Thedateonwhichthe
maturityproceedsare
dueandpayable.
l IftheExtend-
ableMatur-
ityInd(Pos
104)=Y,the
maturityis
theOriginal
Maturity
l IftheExtend-
ableMatur-
ityInd=N,
thisfield
reflectsFinal
Maturity
Date.
FormatisCCYYMMDD. ‘00000000’ character 8
Serial/Term
Indicator
Indicateshowthis
securitywillmature.
l S:serial
l T:term
Space character 1
EX-DTCIssuance
DepositIndicator
Indicatesifthe
securityisbeing
depositedbymeansof
anMMIissuance
instructionthatwasin
existence(EX-[[DTC]])
priortosubmissionof
theissuance
instruction.
l Y
l N
l space
Space character 1
DataRecordLayout(continued)
SecurityMasterFileData- MMIIntraDayFileUserGuide
MMIIntradaySecuritiesFileStructure 10

---

## Page 11

FieldName Description Values [[default]]
Value
Format Length
Corresponding
BaseCUSIP
UndertheDTCMMI
discountnumbering
schemeprogram,
issuersrequestdual
baseCUSIPsfromthe
CUSIPService
Bureau.Thebase
CUSIPsareassigned
andusedbasedupon
leapyearand
subsequentevenand
oddyears.These
baseCUSIPnumbers
allowtheIPAto
seamlesslyissueand
processtransactions.
TheCorresponding
BaseCUSIPisthe
oneassociatedwith
theselectedsecurity. 
Space character 6
BondCUSIP
Number
TheCUSIPnumberof
thelong-termbond
underlyinga
VRDO/CPprogram.
Space character 9
Minimum
Denomination
Wherefinancial
MarketInstruments
aredenominatedina
designatedValue
Currency,the
Minimum
Denominationdefines
minimumamountthat
maybetraded.
Zeroes numeric 9
Incremental
Denomination
Amountor
incrementalnumberof
Sharesforthe
Securityissue.
Zeroes numeric 9
DataRecordLayout(continued)
SecurityMasterFileData- MMIIntraDayFileUserGuide
MMIIntradaySecuritiesFileStructure 11

---

## Page 12

FieldName Description Values [[default]]
Value
Format Length
ForeignCurrency
Indicator
Indicatesifthe
securityis
denominatedina
currencyotherthan
USD(USDollars.)
l N
l Y
2”-FullFast character 1
USDollar
PaymentOption
Indicator
Indicatesiftheincome
and/orprincipal
paymentsmustbe
madeintheforeign
currencytheissueis
denominatedin.Ifnot
applicable,fieldis
blank.
l N
l Y
Space character 1
Certificate
Currency
Currencyinwhichthe
certificateisissuedor
denominated.The
formatfollowstheISO
Standardcurrency
code.
Space character 3
[[book-entry]]/Global
Code
Aprogramthatisalso
eligibleinnon-US
depositories.
l N
l Y
Space character 1
TypeofCertificate Identifiestheformof
holdingofthesecurity.
Values:
l B:Bearer
l E,U,X:Book
Entry
l A,D,I:Inter-
changeable
l M,R:Fully
Registered
Space character 1
Stateof
Incorporation
IssuerStateof
Incorporation/
Space character 2
DataRecordLayout(continued)
SecurityMasterFileData- MMIIntraDayFileUserGuide
MMIIntradaySecuritiesFileStructure 12

---

## Page 13

FieldName Description Values [[default]]
Value
Format Length
BondType Indicatesthatasecurity
isageneralobligation
bondorarevenuebond.
l G:generaloblig-
ationbond
l R:revenuebond
l D:double-
barreled
Space character 1
RegulationS
Indicator
Theexemption
throughwhich
corporationscanissue
unregistered
securitiestoqualified
foreigninvestorsand
foreigninstitutes.
l N
l Y
Space character 1
144AIndicator Theexemptionthrough
whichcorporationscan
issueunregistered
securitiestoqualified
institutionalbuyers
([[QIB]]).
l N
l Y
Space character 1
3(c)7Indicator AAvaluethat
indicateswhethera
securityisrelyingon
theexemptionfrom
Section3(C.)(7)ofthe
InvestmentCompany
Actof1940.
l N
l Y
Space character
FastIndicator Avaluethatindicates
whetherasecurityiseli-
gibleforFastsystem,
whensecuritiesdepos-
itedatDTCareheldina
consolidatedpositionat
theTA,therebyspeed-
ingupthesecuritytrans-
ferprocess.
l 0:-NotFast
l 1:FastWT(Half
[[FAST]])
l 2:FullFast
N/A character 1
ChillDeposit Avaluethatindicates
whetherthissecurity
islockedfromany
depositactivityat
[[DTC]].
l N
l Y
N/A character 1
DataRecordLayout(continued)
SecurityMasterFileData- MMIIntraDayFileUserGuide
MMIIntradaySecuritiesFileStructure 13

---

## Page 14

FieldName Description Values [[default]]
Value
Format Length
ChillCOD Avaluethatindicates
whetherthissecurityis
lockedfromanyCOD
(Certificateondemand)
activityatDTC.
l N
l Y
N/A character 1
ChillDO Avaluethatindicates
whetherthissecurity
islockedfromanyDO
(DeliverOrder)activity
atDTC.
l N
l Y
N/A character 1
ChillPledge Avaluethatindicates
whetherthissecurityis
lockedfromanypledge
activityatDTC.
l N
l Y
N/A character 1
ChillSEG Avaluethatindicates
whetherthissecurity
islockedfromany
segregationactivityat
[[DTC]].
l N
l Y
N/A character 1
ChillDepository Avaluethatindicates
whetherthattheinter
Depositorydeliveryfunc-
tionischilled.
l N
l Y
N/A character 1
ChillReason
(DepositChill
Reason)
Reasonforaction,the
reasonfortheDeposit
Chill.
Valuesarespaceandfrom
0to9:
l Space:The
Securitydoesnot
haveaDeposit
Chill.Reasonis
notapplicable.
l 0:[[DTCC]]-Applied
DepositChill.
l 1:[[DTCC]]-
AppliedDeposit
Chill-Com-
plianceRelated.
l 2-9:Reservedfor
futureuse.
Space character 1
DataRecordLayout(continued)
SecurityMasterFileData- MMIIntraDayFileUserGuide
MMIIntradaySecuritiesFileStructure 14

---

## Page 15

FieldName Description Values [[default]]
Value
Format Length
IssuerCountry Specifiesthecountryin
whichtheissuerofaFin-
ancialmarketinstru-
mentisregistered.
Space character 3
Countryof
[[settlement]]
Currency
Alwaysdefaultsto
USAbecauseMMIs
SettleinUSDollars.
'USA' 'USA' character 3
PrincipalIndexe
Indicator
Indicateswhetherthe
principalpaymentsare
determinedviaaspe-
cificindex(forexample,
aforeigncurrencyor
commodityprice).
l N
l Y
Space character 3
Principal
Amortization
Indicateswhetherif
thesecurityhas
periodicamortization
ofprincipalpayments.
l 0:InterestOnly
l 1:Principaland
Interest
l 2:PrincipalOnly
N/A character 1
AccretionIndicator Identifiessecuritiesthat
accrueinterestpriorto
makinganyincomepay-
ments.
l N
l Y
Space character 1
DataRecordLayout(continued)
SecurityMasterFileData- MMIIntraDayFileUserGuide
MMIIntradaySecuritiesFileStructure 15

---

## Page 16

FieldName Description Values [[default]]
Value
Format Length
Calculation
Method
Indicatesthetypeof
formulatobeusedfor
calculatingincome
payments.
l 01:ActualDays
elapsed/360-
dayyear
l 02:30Day
Month/360-day
year
l 03:ActualDays
elapsed/Actual
Days
l 04:DTCIAMCP
Formula
l 05:ActualDays/
365
l 06:=ActualDays
/366
Note:IftheMMIissuance
instructionspecifiesActual
Days/365or366,DTCwill
translatetoActualDays/
366whenthedateddate
fallsinaleapyear
Space character 2
AccrualPeriodType Indicatesthetypeofpay-
abledateaccrual,which
willbeusedtodeterm-
inethenumberofdays
intheincomepayment
calculation.
l R:Recordto
recorddate
l P:Payableto
payabledate
Space character 1
PaymentAccrual
MeasureType
Indicatesthemethod
forcalculatingthe
numberofdaysinthe
incomeaccrual
period.
l A:Actualpay-
menttoactual
payment.
l P:Targetedpay-
menttotargeted
payment.
Space character 1
ChangeableInterest
PaymentFrequency
Indicator
Indicateswhetherthe
securityhasafeature
allowingachangeinthe
frequencyofInterest
payments.
l N
l Y
Space character 1
DataRecordLayout(continued)
SecurityMasterFileData- MMIIntraDayFileUserGuide
MMIIntradaySecuritiesFileStructure 16

---

## Page 17

FieldName Description Values [[default]]
Value
Format Length
InterestPayment
FrequencyType
Indicatestheperiodic
interestpayment
frequencytype(units
ofmeasure).
l Y:Year
l M:month
l W:Week
l D:Day
Space character 3
InterestPayment
FrequencyNumber
Inconjunctionwith
Interestpaymentfre-
quencyintervaltype,
thisfieldindicatesthe
periodicInterestpay-
mentfrequency.For
example,apayment
intervalnumberof90
withapaymentinterval
typeofD[ays]=90
days.
Space character 3
InterestPayment
RecordDate
NumberofDays
(#ofdaysrecorddate
precedespaydate):
Thetotalnumberof
daysthattherecord
dateprecedesthe
targetedInterest
paymentdate.Note:
ThisfieldandtheFirst
andSecondIncome
PaymentRecordDate
fieldsaremutually
exclusive
Space character 3
InterestPayment
RecordDateBusi-
ness/CalendarIndic-
ator
Identifiesthecalendarto
beusedforcomputing
thenumberofdaysfor
payment,ortherecord
dateifthepreviousfield
isused.
l B:Business
Days
l C:Calendar
Days
Space character 1
TargetedFirst
InterestPayment
Date
Thetargeteddateon
whichtheholderofthe
securityisscheduledto
receivethefirstinterest
payment.
FormatisMMDD. '0000' character 4
ActualFirst
InterestPayment
Date
Thedateonwhichthe
issuerofthesecurity
isscheduledmakethe
firstinterestpayment.
FormatisCCYYMMDD. '00000000' character 8
DataRecordLayout(continued)
SecurityMasterFileData- MMIIntraDayFileUserGuide
MMIIntradaySecuritiesFileStructure 17

---

## Page 18

FieldName Description Values [[default]]
Value
Format Length
InterestPayment
DayofMonth(DOM)
Inconjunctionwiththe
InterestPaymentDOM
Business/Calendar
Indicator,thisfieldwill
determinetheInterest
paymentday.
1-31 Space character 2
InterestPayment
DOMBusi-
ness/CalendarIndic-
ator
Thevalueinthisfield
specifiesthedayof
monthcountand
worksinconjunction
withtheInterest
PaymentDayof
Monthfieldto
determinetheInterest
paymentday.
Forexample,ifthe
Payment
Business/Calendar
IndicatorisC,the
PaymentDayofthe
Monthis1,the
PaymentIntervalType
isM,andtheand
PaymentInterval
Numberis6.Interest
Paymentsaremade
every6monthsonthe
firstCalendarDayof
theInterestPayment
Month.
l B:Business
Days
l C:Calendar
Days
Space character 1
InterestPayment
WeekofMonth
(WOM)
Inconjunctionwiththe
InterestPaymentDayof
Weekfield,thisfield
determinestheIncome
InterestpaymentWeek
oftheMonth.
l 1:Firstweek
l 2:Secondweek
l 3:Thirdweek
l 4:Fourthweek
Space character 1
DataRecordLayout(continued)
SecurityMasterFileData- MMIIntraDayFileUserGuide
MMIIntradaySecuritiesFileStructure 18

---

## Page 19

FieldName Description Values [[default]]
Value
Format Length
InterestPayment
DayofWeek
(DOW)
Inconjunctionwiththe
InterestPayment
WeekofMonthfield,
thisfielddetermines
theInterestpayment
DayOftheWeek.For
example,iftheIncome
PaymentDayOf
Weekis01
(Monday)andthe
InterestPayment
WeekofMonthis1,
theInterestPayments
aremadeonthefirst
Mondayofevery
month.
l 01:Monday
l 02:Tuesday
l 03:Wednesday
l 04:Thursday
l 05:Friday
Space character 2
Step-upRateIndic-
ator
Indicateswhethera
bondpaysaninitial
couponrateforthefirst
period,andthena
highercouponratefor
subsequentperiods.
l N
l Y
Space character 1
Step-upInterest
Rate
Therateatwhich
subsequentfuture
couponpaymentsare
receivedatahigher,
predetermined
amountthanprevious
orcurrentperiods.
Zeroes numeric 9
InterestPayment
per$1,000(1stPay-
ment/AtMaturity)
Thedollaramount
earnedper$1,000face
amount.Paymentswill
occuronthefirst
Interestpaymentdate.
(6decimalpositions
implied.)
Zeroes numeric 15
InterestRateReset
Indicator
Indicatesifthespreador
spreadmultiplierfora
variableratesecurity
canberesetatthe
optionoftheIssuer.For
afixedratesecurity,
indicatesifthefixedrate
canbereset.
l N
l Y
Space character 1
DataRecordLayout(continued)
SecurityMasterFileData- MMIIntraDayFileUserGuide
MMIIntradaySecuritiesFileStructure 19

---

## Page 20

FieldName Description Values [[default]]
Value
Format Length
InterestRate
ResetFrequency
type
Inconjunctionwiththe
InterestRateReset
FrequencyNumber,
indicatesthelengthof
timeusedtoresetthe
rate.
l Y:Year
l M:month
l W:Week
l D:Days
space character 1
InterestRateReset
FrequencyNumber
Inconjunctionwiththe
InterestRateResetFre-
quencyType,thisfield
determinestheperiodic
ratechange.For
example,aratereset
intervalnumberof90
witharateresetinterval
typeofD(days)indic-
atesarateresetevery
90days.
Space character 3
LIBORIndexed
InterestPayment
Indicator
LIBORIndexed
InterestPayment
Indicator
l N
l Y
Space character 1
InterestPayment
IndexMaturityInter-
valType
Thetimelengthofthe
indexusedtoresetthe
index.
l Y:Year
l M:month
l W:Week
l D:Days
Space character 1
InterestPayment
IndexMaturityUnits
Thenumberofindex
maturityunits(00-99)
representingthelength
oftimeusedtoresetthe
indexinconjunctionwith
theInterestPayment
IndexMaturityInterval
Type.Forexamle,if
IndexMaturityInterval
TypeisD(days)and
IndexMaturityInterval
Numberis90,theindex
isresetevery90days.
'00' character 2
LIBORIndexed
PrincipalPayment
Indicator
LIBORIndexed
InterestPayment
Indicator.
l N
l Y
Space character 1
DataRecordLayout(continued)
SecurityMasterFileData- MMIIntraDayFileUserGuide
MMIIntradaySecuritiesFileStructure 20

---

## Page 21

FieldName Description Values [[default]]
Value
Format Length
NumberofDaysSet-
tlementofPrincipal
PaymentAfterMatur-
ity
Thenumberofdays
afterthematuritydate
onwhichthefinalprin-
cipalpaymentwillbe
made.
Space character 2
FinalPrincipalPay-
mentCalendar/
BusinessDayIndic-
ator
IdentifiestheCalendar
tobeusedforcom-
putingthenumberof
daysforthefinalprin-
cipalpayment.
l B:Business
Days
l C:Calendar
Days
Space character 1
NumberofDaysSet-
tlementofIncome
PaymentAfterMatur-
ity
Thenumberofdays
afterthematuritydate
onwhichthefinal
incomepaymentwillbe
made.
Space character 2
FinalIncomePay-
mentCalendar/
BusinessDayIndic-
ator
IdentifiestheCalendar
tobeusedforcom-
putingthenumberof
daysforthefinalincome
payment.
l B:Business
Days
l C:Calendar
Days
Space character 1
FinalAccrualPeriod
Measure
IndicatesifaCDor
depositnoteprogram’s
finalpaymentperiod
endsonitsactual(A)or
targeted(T)maturity
date.
l A:Accrual
l T:Targeted
Space character 1
VariableRatetype Typeofvariableinterest
rate.
l 00:Notapplic-
able
l 01:Periodicauc-
tionrate
l 02:Selectauc-
tionrate
l 03:Tenderrate
l 04:Variable
demandrate
l 05:Variable
moderate
l 06:Passthrough
l 07:Othervari-
ablerate
Space character 2
DataRecordLayout(continued)
SecurityMasterFileData- MMIIntraDayFileUserGuide
MMIIntradaySecuritiesFileStructure 21

---

## Page 22

FieldName Description Values [[default]]
Value
Format Length
IndexName NameoftheIndexused
todeterminetherate.
Space character 15
SpreadSign(+/-) Identifiesthesign(plus
orminus)showingthe
positiveornegative
spreadpercentage.
l Space:Not
applicable.
l +:Positive
spread.
l -:Negative
spread
Space character 1
SpreadRate Identifiestheper-
centagespread,from
000.000000%to
100.000000%.
Zeroes numeric 0
VariableRate
IncomeIndexName
-Part1
Identifiesthenameof
theindexonwhichthe
incomepaymentwillbe
based(firstpartof
name).
Space character 72
VariableRate
IncomeIndexName
-Part2
Identifiesthenameof
theindexonwhichthe
incomepaymentwillbe
based(secondpartof
name).
Space character 72
PaymentCurrency Currencyusedfor
interestorredemption
payments.Theformat
allowsISOStandardcur-
rencycodes.
Space character 3
StockforMaturity
Indicator
Indicateswhethera
Bondhastheoptionto
payMaturityproceeds
asStockinsteadofas
Cash.
l N
l Y
Space character 1
RenewableNote
Indicator(MMIs
Only)
Indicateswhethera
medium-termnoteis
renewable(hasaVRRN
provision).
l N
l Y
Space character 1
TaxableIndicator Avaluethatindicates
whetherthesecurityis
subjecttofederal
incometaxes;formuni-
cipalsecuritiesonly.
l N
l Y
Space character 1
TaxCreditinLieuof
InterestIndicator
DataRecordLayout(continued)
SecurityMasterFileData- MMIIntraDayFileUserGuide
MMIIntradaySecuritiesFileStructure 22

---

## Page 23

FieldName Description Values [[default]]
Value
Format Length
CallIndicator Aflagthatindicates
whetheraBondcanbe
redeemedbytheissuer
priortomaturity.
l N
l Y
Space charter 1
NumberofDaysfor
CallNotice
Numberofdays
requiredforcallnoti-
fication.
Space charter 3
CallPricePer-
centage ThePercentageofpar
paidifthesecurityis
calledonthefirstcall
date.(3decimal
positionsareimplied).
l N
l Y
Zeros numeric 9
SinkingFundIndic-
ator Aflagthatindicates
whethertheBondisa
sinkingFundissue.
Theissuermakes
periodicpaymentstoa
trustee,whoretires
partoftheissueby
purchasingthebonds
intheopenmarket.
l N
l Y
Space character 1
PUTOptionIndic-
ator Aflagthatindicates
whethertheholder
hastheright,butnot
theobligation,to
demandearly
repaymentofthe
principal.
l N
l Y
Space character 1
PUTUponDeath
Indicator Aflagthatindicates
whethertheholder
hastheright,butnot
theobligation,to
demandearly
repaymentofthe
principaliftheholder
ofthesecuritydies.
l N
l Y
Space character 1
DataRecordLayout(continued)
SecurityMasterFileData- MMIIntraDayFileUserGuide
MMIIntradaySecuritiesFileStructure 23

---

## Page 24

FieldName Description Values [[default]]
Value
Format Length
PUTFrequency
Type Frequencyof
repaymentoption.
Note:Onlyavailableif
theRepaymentPut
OptionIndicator
(Position102)=Y..
l 1:Annual
l 2:Semi-annual
l 3:Bi-monthly
l 4:Quarterly
l 5:Bi-annually
l 8:=Monthly
l I:Irregular
l O:OneTime
Only
l U:Undefined
Space character 1
EndPutOptionDateThelastdateonwhicha
securitycanbe
redeemedbytheholder
priortoitsmaturity.
Formatisccyymmdd '00000000' character 8
IssuerAcronym TheDTCdesignation
usedtoidentifytheMMI
[[issuer]].Itisthesameas
theStockExchangeor
Over-The-Counterticker
symbolwhereavailable.
Mandatory character 4
IssuerName Thefirstoccurrenceof
theformalIssuername
appearingonthePro-
spectusorOffering
Statementthatissup-
pliedtoDTCduringeli-
gibilityprocessing.This
descriptionprovidesa
consistentissuername
acrosstheissuanceand
issues.TheIssueror
IssuingAgentmayalso
providethedescriptionif
thesecuritydoesnotgo
throughtheeligibilitypro-
cess,forexample,for
forMBSsecurities..
Mandatory character 22
IssuerContact(1)
Name&Address
TheNameandAddress
oftheFirstIssuercon-
tact
Space character 48
IssuerContact(1)
PhoneNumber
Thephonenumberthe
FirstIssuercontact.T
Space character 18
DataRecordLayout(continued)
SecurityMasterFileData- MMIIntraDayFileUserGuide
MMIIntradaySecuritiesFileStructure 24

---

## Page 25

FieldName Description Values [[default]]
Value
Format Length
IssuerContact(2)
Name&Address
TheNameandAddress
ofSecondIssuercon-
tact
Space character 48
IssuerContact(2)
PhoneNumber
Thephonenumberof
theSecondIssuercon-
tact.
Space character 18
ProgramRank Therankofthepro-
gram.Itidentifiesthepri-
orityofclaimsonassets
comparedtoother
debts.
Space character 2
ProgramType [[DTC]]-assigneddes-
ignationidentifyingthe
sectionoftheSecurities
Actof1933underwhich
anMMIisexemptfrom
SECregistration."R"sig-
nifiesaregisteredpro-
gram.
Space character 1
MarketCode Identifieswhetherthe
programispubliclyor
privatelyplace,aswell
asthemarketinwhichit
trades.
Space character 1
[[DTC]] EndofPositionEndofpositionheldat
[[DTCC]].Willonlybe
populatedfor:
l Subissue
type507
(Certificateof
Deposit)
l The7:30PM
files,withzer-
oesforthe
otherfiles.
Zeroes numeric 13
FirstCallDate Firstdateasecurity
canbecalled.
FormatCCYYMMDD ‘00000000’ character 8
DataRecordLayout(continued)
SecurityMasterFileData- MMIIntraDayFileUserGuide
MMIIntradaySecuritiesFileStructure 25

---

## Page 26

TrailerRecord
Forpurposesofinternalaudit,thetrailerrecordcontainsbalancingcontrolsthatverifyrecordcounts.
Position Length Format FieldName Description
1–3 3 Character MessageType Identifiesthemessagetype.ThevalueisT01(Trailer
Message).
4–9 6 Character Message
Sequence
Number
Identifiesthesequencenumberwithinthemessagetype.
Initializedto000001.
10-17 8 Numeric TotalMessagesThetotalnumberofmessagesonthefile,includingthe
header,detail,andtrailermessagetypes.
TrailerRecord
AsampletrailerrecordisT0100000100006747.
SecurityMasterFileData- MMIIntraDayFileUserGuide
MMIIntradaySecuritiesFileStructure 26

---

## Page 27

SUB-ISSUETYPES
Type SSITDescription
320 MMIMunicipalVRDOCP
330 MMIMunicipalCommercialPaper
502 MMIBankers'AcceptanceNoteBA
504 MMIInstitutionalCertificatesofDeposit
505 CertificatedMoneyMarketInstrument
506 CertificatedMoneyMarket-PeriodicPayer
507 CertificatesofDeposit
525 MMICorporateCommercialPaper
526 MMICorporateVRDOCP
530 MTNMediumTermNote
531 MMIDepositNote
532 MMIMedium-TermBankNote
533 MMIMediumTermNote
550 MMIShort-TermBankNote
Sub-IssueTypes
SecurityMasterFileData- MMIIntraDayFileUserGuide
Sub-IssueTypes 27

---

## Page 28

©2024.Allrightsreserved.[[DTCC]],[[DTCC]](Stylized)andFinancialMarkets.Forward.areregisteredandunregisteredtrademarks
ofTheDepositoryTrust&ClearingCorporationDTCC.Theservicesdescribedhereinareprovidedunderthe“[[DTCC]]”brandname
bycertainaffiliatesofTheDepositoryTrust&ClearingCorporation(“[[DTCC]]”).DTCCitselfdoesnotprovidesuchservices.Eachof
theseaffiliatesisaseparatelegalentity,subjecttothelawsandregulationsoftheparticularcountryorcountriesinwhichsuch
entityoperates.Pleaseseewww.[[DTCC]].comformoreinformationonDTCC,itsaffiliatesandtheservicestheyoffer.
DocDate:January18,2024
PublicationCode:DAT327
Service:SecurityMasterFileData
Title:MMIIntraDayFileUserGuide
ForMoreInformation
EmailDTCCLearningat:
DTCCLearning@[[DTCC]].com
orvisitusonthewebat:
www.dtcclearning.com