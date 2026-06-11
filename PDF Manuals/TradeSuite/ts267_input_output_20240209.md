---
title: "Input/Output Information"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ts267_input_output_20240209.pdf"
pages: 100
size: "747.6 KB"
category: "TradeSuite"
ingested_on: "2026-06-05"
---

# Input/Output Information

**Original File:** [ts267_input_output_20240209.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ts267_input_output_20240209.pdf)  
**Category:** TradeSuite  
**Total Pages:** 100  
**File Size:** 747.6 KB  

---

## Page 1

TradeSuiteID®
INPUT/OUTPUTINFORMATION
VERSION8.1
FEBRUARY09,2024

---

## Page 2

TABLEOFCONTENTS
Preface 5
Audience 5
ChangesinThisVersionoftheDocument 5
RelatedDocumentsandTraining 5
Questions? 5
1.Input/OutputInformationCodes 7
Introduction 7
ISOCountryCodes 7
ISOCurrencyCodes 15
MarketCodesandAbbreviations 21
Index(Benchmark)Codes 27
SettlementLocationCodes 28
CancellationReasonCodes 36
IneligibleConfirmationCodes 42
InteractiveFormatInputtoEODFormatOutputCodeConversion 46
Mortgage-BackedSecuritiesSpecificationCodes 48
Moody’sConversionCodesandRatings 49
Standard&Poor’sConversionCodesandRatings 51
SecurityNumberingSystems 52
ExpandedSecurityTypes 53
TransactionTypes 56
InteractiveFields 58
2.ProcessingProcedures 60
Input/OutputInformation
TableOfContents 2

---

## Page 3

Computer-to-ComputerFacility([[CCF]]) 60
BlockSpecification 60
MessagePrefixSpecification 61
MessageQuerying(MQ) 61
TradeSuiteID®ErrorCodes 61
3.AdditionalNotes 86
AffirmingPartyIndicator 86
InterestedParties 86
InterestedPartiesDerivedFromALERT® 86
New-FormatInput 86
OutputLocations 87
SettlementLocationofDTCorBRC 87
SettlementLocationofNFS 87
AllOtherSettlementLocations 88
A.SecurityNumberingSystemFormats 89
EfficiencyofChecking 89
ISINDefinition 89
ComputingCheck-Digits 90
ISINModulus10Double-Add-DoubleCheck-Digit 90
CUSIPModulus10Double-Add-DoubleCheck-Digit 91
NotesoftheCUSIPandISINComputations 94
SEDOLSecuritiesIdentifierCheck-Digit 94
Format 94
SignificanceoftheSeriesDigit 95
Input/OutputInformation
TableOfContents 3

---

## Page 4

CheckingaNumber 97
DerivingaCheck-Digit 98
Input/OutputInformation
TableOfContents 4

---

## Page 5

PREFACE
ThisdocumentdescribestheinputandoutputinformationrequiredfortheTradeSuiteID®service.
Audience
ThisdocumentisforinformationtechnologyprofessionalswhoareresponsibleforworkingwiththeIDinputand
output.
ChangesinThisVersionoftheDocument
Thisversionofthedocumentupdatesthefollowingtables:
l ISOCountryCodes
l ISOCurrencyCodes
l MarketCodesandAbbreviations
l SettlementLocationCodes
l CancellationReasonCodes
l IneligibleConfirmationCodes
l Mortgage-BackedSecuritiesSpecificationCodes
l Moody’sConversionCodes
l Standard&Poor’sConversionCodes
l TradeSuiteIDErrorCodes
ItalsoupdatesremovesthePaymentMethodIndicatorandPriceConversionsectionsfromAdditionalNotes.
RelatedDocumentsandTraining
Forrelateddocumentsandtraining,seeTradeSuiteID®ontheDTCCLearningCenter.
Questions?
TheClientCenterprovidesgeneralassistanceandtechnicalhelp.Visitto:
Input/OutputInformation
Preface 5

---

## Page 6

l Enteraservicerequestorcheckthestatusofanexistingservicerequest.
l Searchtheknowledgebase.
l Obtaincontactinformation.
Input/OutputInformation
Preface 6

---

## Page 7

1.INPUT/OUTPUTINFORMATIONCODES
Introduction
TradeSuiteIDsupportsthefollowingcodes:
l ISOCountryCodes
l ISOCurrencyCodes
l MarketCodesandAbbreviations
l Index(Benchmark)Codes
l SettlementLocationCodes
l CancellationReasonCodes
l IneligibleConfirmationCodes
l InteractiveFormatInputtoEODFormatOutputCodeConversion
l Mortgage-BackedSecuritiesSpecificationCodes
l Moody’sConversionCodesandRatings
l Standard&Poor’sConversionCodesandRatings
l SecurityNumberingSystems
l ExpandedSecurityTypes
l TransactionTypes
l InteractiveFields
ISOCountryCodes
TheTradeSuiteID®servicesupportscodesshowninTable1.1andmaintainedbyISOatISO3166Country
Codes.Foralistofcurrencycodes,seeTable1.2.
Country
Code
Alpha-3
Code
Numeric
Code
Country
Name
Abbreviated
CountryName
AD AND 020 Andorra ANDORRA
AE ARE 784 UnitedArabEmirates UNTDARABEM
Table1.1ISOCountryCodes
Input/OutputInformation
1.Input/OutputInformationCodes 7

---

## Page 8

Country
Code
Alpha-3
Code
Numeric
Code
Country
Name
Abbreviated
CountryName
AF AFG 004 Afghanistan AFGHANISTAN
AG ATG 028 AntiguaandBarbuda ANT.BARBUDA
AI AIA 660 Anguilla ANGUILLA
AL ALB 008 Albania ALBANIA
AM ARM 051 Armenia ARMENIA
AO AGO 024 Angola ANGOLA
AQ ATA 010 Antarctica ANTARCTICA
AR ARG 032 Argentina ARGENTINA
AS ASM 016 AmericanSamoa AMER.SAMOA
AT AUT 040 Austria AUSTRIA
AU AUS 036 Australia AUSTRALIA
AW ABW 533 Aruba ARUBA
AX ALA 248 ÅlandIslands ALANDISLAND
AZ AZE 031 Azerbaijan AZERBAIJAN
BA BIH 070 BosniaandHerzegovina BOSNIA-HERZE
BB BRB 052 Barbados BARBADOS
BD BGD 050 Bangladesh BANGLADESH
BE BEL 056 Belgium BELGIUM
BF BFA 854 BurkinaFaso BURKINAFASO
BG BGR 100 Bulgaria BULGARIA
BH BHR 048 Bahrain BAHRAIN
BI BDI 108 Burundi BURUNDI
BJ BEN 204 Benin BENIN
BL BLM 652 SaintBarthélemy STBARTHELEMY
BM BMU 060 Bermuda BERMUDA
BN BRN 096 BruneiDarussalam BRUNEI
BO BOL 068 Bolivia BOLIVIA
BQ BES 535 Bonaire,SintEustatiusandSaba BONAIRE
BR BRA 076 Brazil BRAZIL
BS BHS 044 Bahamas BAHAMAS
BT BTN 064 Bhutan BHUTAN
BV BVT 074 BouvetIsland BOUVETISLAN
Table1.1ISOCountryCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 8

---

## Page 9

Country
Code
Alpha-3
Code
Numeric
Code
Country
Name
Abbreviated
CountryName
BW BWA 072 Botswana BOTSWANA
BY BLR 112 Belarus BYELORUSSIA
BZ BLZ 084 Belize BELIZE
CA CAN 124 Canada CANADA
CC CCK 166 Cocos(Keeling)Islands COCOSISLNDS
CD COD 180 Congo,DemocraticRepublicofthe CONGODEM
CF CAF 140 CentralAfricanRepublic CENT.AF.REP
CG COG 178 Congo CONGO
CH CHE 756 Switzerland SWITZERLAND
CI CIV 384 Côted'Ivoire IVORYCOAST
CK COK 184 CookIslands COOKISLANDS
CL CHL 152 Chile CHILE
CM CMR 120 Cameroon UNTD.RP.CAMR
CN CHN 156 China CHINA
CO COL 170 Colombia COLOMBIA
CR CRI 188 CostaRica COSTARICA
CV CPV 132 CaboVerde CAPEVERDE
CW CUW 531 Curaçao CURACAO
CX CXR 162 ChristmasIsland CHRISTMASIS
CY CYP 196 Cyprus CYPRUS
CZ CZE 203 Czechia CZECHREPUBL
DE DEU 276 Germany "GERMANY,FR"
DJ DJI 262 Djibouti DJIBOUTI
DK DNK 208 Denmark DENMARK
DM DMA 212 Dominica DOMINICA
[[DO]] DOM 214 DominicanRepublic DOMINICANRP
DZ DZA 012 Algeria ALGERIA
EC ECU 218 Ecuador ECUADOR
EE EST 233 Estonia ESTONIA
EG EGY 818 Egypt EGYPT
EH ESH 732 WesternSahara WESTN.SAHARA
ER ERI 232 Eritrea ERITREA
Table1.1ISOCountryCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 9

---

## Page 10

Country
Code
Alpha-3
Code
Numeric
Code
Country
Name
Abbreviated
CountryName
ES ESP 724 Spain SPAIN
ET ETH 231 Ethiopia ETHIOPIA
FI FIN 246 Finland FINLAND
FJ FJI 242 Fiji FIJI
FK FLK 238 FalklandIslands(Malvinas) FALKLANDISL
FM FSM 583 Micronesia(FederatedStatesof) MICRONESIA
FO [[FRO]] 234 FaroeIslands FAEROEISLDS
FR FRA 250 France FRANCE
GA GAB 266 Gabon GABON
GB GBR 826 UnitedKingdom UK
GD GRD 308 Grenada GRENADA
GE GEO 268 Georgia GEORGIA
GF GUF 254 FrenchGuiana FR.GUIANA
GG GGY 831 Guernsey GUERNSEY
GH GHA 288 Ghana GHANA
GI GIB 292 Gibraltar GIBRALTAR
GL GRL 304 Greenland GREENLAND
GM GMB 270 Gambia GAMBIA
GN GIN 324 Guinea GUINEA
GP GLP 312 Guadeloupe GUADELOUPE
GQ GNQ 226 EquatorialGuinea EQ.GUINEA
GR GRC 300 Greece GREECE
GS SGS 239 SouthGeorgiaandtheSouthSandwichIslands SGSSI
GT GTM 320 Guatemala GUATEMALA
GU GUM 316 Guam GUAM
GW GNB 624 Guinea-Bissau GUINEABISSAU
GY GUY 328 Guyana GUYANA
HK HKG 344 HongKong HONGKONG
HM HMD 334 HeardIslandandMcDonaldIslands HEARD.MCDIS
HN HND 340 Honduras HONDURAS
HR HRV 191 Croatia CROATIA
HT HTI 332 Haiti HAITI
Table1.1ISOCountryCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 10

---

## Page 11

Country
Code
Alpha-3
Code
Numeric
Code
Country
Name
Abbreviated
CountryName
HU HUN 348 Hungary HUNGARY
[[ID]] IDN 360 Indonesia INDONESIA
IE IRL 372 Ireland IRELAND
IL ISR 376 Israel ISRAEL
IM IMN 833 IsleofMan ISLEOFMAN
IN IND 356 India INDIA
IO IOT 086 BritishIndianOceanTerritory BR.IND.OC.TR
IS ISL 352 Iceland ICELAND
IT ITA 380 Italy ITALY
JE JEY 832 Jersey JERSEYCI
JM JAM 388 Jamaica JAMAICA
JO JOR 400 Jordan JORDAN
JP JPN 392 Japan JAPAN
KE KEN 404 Kenya KENYA
KG KGZ 417 Kyrgyzstan KYRGYZSTAN
KH KHM 116 Cambodia DM.KAMPUCHEA
KI KIR 296 Kiribati KIRIBATI
KM COM 174 Comoros COMOROS
KN KNA 659 SaintKittsandNevis STKITTS.NEVIS
KR KOR 410 Korea,Republicof "KOREA,REP"
KW KWT 414 Kuwait KUWAIT
KY CYM 136 CaymanIslands CAYMANISLDS
KZ KAZ 398 Kazakhstan KAZAKHSTAN
LA LAO 418 LaoPeople'sDemocraticRepublic LAOP.DEM.R
LB LBN 422 Lebanon LEBANON
LC LCA 662 SaintLucia ST.LUCIA
LI LIE 438 Liechtenstein LIECHTENSTEI
LK LKA 144 SriLanka SRILANKA
LR LBR 430 Liberia LIBERIA
LS LSO 426 Lesotho LESOTHO
LT LTU 440 Lithuania LITHUANIA
LU LUX 442 Luxembourg LUXEMBOURG
Table1.1ISOCountryCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 11

---

## Page 12

Country
Code
Alpha-3
Code
Numeric
Code
Country
Name
Abbreviated
CountryName
LV LVA 482 Latvia LATVIA
LY LBY 434 Libya LIBYA
MA MAR 504 Morocco MOROCCO
MC MCO 492 Monaco MONACO
MD MDA 498 Moldova,Republicof MOLDOVA,REP
ME MNE 499 Montenegro MONTENEGRO
MF MAF 663 SaintMartin(Frenchpart) SAINT-MARTIN
MG MDG 450 Madagascar MADAGASCAR
MH MHL 584 MarshallIslands MARSHALLISL
MK MKD 807 NorthMacedonia MACEDONIA
ML MLI 466 Mali MALI
MM MMR 104 Myanmar MYANMAR
MN MNG 496 Mongolia MONGOLIA
MO MAC 446 Macao MACAU
MP MNP 580 NorthernMarianaIslands NORTHERNMAR
MQ MTQ 474 Martinique MARTINIQUE
MR MRT 478 Mauritania MAURITANIA
MS MSR 500 Montserrat MONTSERRAT
MT MLT 470 Malta MALTA
MU MUS 480 Mauritius MAURITIUS
MV MDV 462 Maldives MALDIVES
MW MWI 454 Malawi MALAWI
MX MEX 484 Mexico MEXICO
MY MYS 458 Malaysia MALAYSIA
MZ MOZ 508 Mozambique MOZAMBIQUE
NA NAM 516 Namibia NAMIBIA
NC NCL 540 NewCaledonia NEWCALEDNIA
NE NER 562 Niger NIGER
NF NFK 574 NorfolkIsland NORFOLKISLD
NG NGA 566 Nigeria NIGERIA
NI NIC 558 Nicaragua NICARAGUA
NL NLD 528 Netherlands NETHERLANDS
Table1.1ISOCountryCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 12

---

## Page 13

Country
Code
Alpha-3
Code
Numeric
Code
Country
Name
Abbreviated
CountryName
NO NOR 578 Norway NORWAY
NP NPL 524 Nepal NEPAL
NR NRU 520 Nauru NAURU
NU NIU 570 Niue NIUE
NZ NZL 554 NewZealand NEWZEALAND
OM OMN 512 Oman OMAN
PA PAN 591 Panama PANAMA
PE PER 604 Peru PERU
PF PYF 258 FrenchPolynesia FR.POLYNESIA
PG PNG 598 PapuaNewGuinea PAPUAN.GUIN
PH PHL 608 Philippines PHILIPPINES
PK PAK 586 Pakistan PAKISTAN
PL POL 616 Poland POLAND
PM SPM 666 SaintPierreandMiquelon STPIER.MIQU
PN PCN 612 Pitcairn PITCAIRNISL
PR PRI 630 PuertoRico PUERTORICO
PT PRT 620 Portugal PORTUGAL
PW PWL 585 Palau PALAU
PY PRY 600 Paraguay PARAGUAY
QA QAT 634 Qatar QATAR
RE REU 638 Réunion REUNION
RO ROU 642 Romania ROMANIA
RS SRB 688 Serbia SERBIA
RU RUS 643 RussianFederation RUSSIA
RW RWA 646 Rwanda RWANDA
SA SAU 682 SaudiArabia SAUDIARABIA
SB SLB 090 SolomonIslands SOLOMONISLS
SC SYC 690 Seychelles SEYCHELLES
SE SWE 752 Sweden SWEDEN
SG SGP 702 Singapore SINGAPORE
SH SHN 654 SaintHelena,AscensionandTristandaCunha ST.HELENA
SI SVN 705 Slovenia SLOVENIA
Table1.1ISOCountryCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 13

---

## Page 14

Country
Code
Alpha-3
Code
Numeric
Code
Country
Name
Abbreviated
CountryName
SJ SJM 744 SvalbardandJanMayen SVALBARDISL
SK SVK 703 Slovakia SLOVAKIA
SL SLE 694 SierraLeone SIERRALEONE
SM SMR 674 SanMarino SANMARINO
SN SEN 686 Senegal SENEGAL
SB SOM 706 Somalia SOMALIA
SR SUR 740 Suriname SURINAME
ST STP 678 SaoTomeandPrincipe SAOTOMEPRN
SV SLV 222 ElSalvador ELSALVADOR
SX SXM 534 SintMaarten(Dutchpart) SINTMAARTEN
SZ SWZ 748 Eswatini SWAZILAND
TC TCA 796 TurksandCaicosIslands TURKSCA.ISL
TD TCD 148 Chad CHAD
TF ATF 260 FrenchSouthernTerritories FRENCHSOUTHERN
TG TGO 768 Togo TOGO
TH THA 764 Thailand THAILAND
TJ TJK 762 Tajikistan TAJIKISTAN
TK TKL 772 Tokelau TOKELAU
TL TLS 626 Timor-Leste EASTTIMOR
TM TKM 795 Turkmenistan TURKMENISTAN
TN TUN 788 Tunisia,UnitedRepublicof TUNISIA
TO TON 776 Tonga TONGA
TR TUR 792 Turkey TURKEY
TT TTO 780 TrinidadandTobago TRINIDADTBG
TV TUV 798 Tuvalu TUVALU
TW TWN 158 Taiwan,ProvinceofChina TAIWAN
TZ TZA 834 Tanzania UNTD.RP.TANZ
UA UKR 804 Ukraine UKRAINE
UG UGA 800 Uganda UGANDA
UM UMI 581 UnitedStatesMinorOutlyingIslands USMINOR
US USA 840 UnitedStatesofAmerica USA
UY URY 858 Uruguay URUGUAY
Table1.1ISOCountryCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 14

---

## Page 15

Country
Code
Alpha-3
Code
Numeric
Code
Country
Name
Abbreviated
CountryName
UZ UZB 680 Uzbekistan UZBEKISTAN
VA VAT 336 HolySee HOLYSEE
VC VCT 670 SaintVincentandtheGrenadines ST.VINCTGRN
VE VEN 862 Venezuela(BolivarianRepublicof) VENEZUELA
VG VGB 092 VirginIslands(British) BR.VIRGINIS
VI VIR 850 VirginIslands(U.S.) US.VIRGINIS
VN VNM 704 VietNam VIETNAM
VU VUT 548 Vanuatu VANUATU
WF WLF 876 WallisandFutuna WALLISFUT.I
WS WSM 882 Samoa SAMOA
YE YEM 886 Yemen YEMEN
YT MYT 175 Mayotte MAYOTTE
ZA ZAF 710 SouthAfrica SOUTHAFRICA
ZM ZMB 894 Zambia ZAMBIA
ZW ZWE 716 Zimbabwe ZIMBABWE
Table1.1ISOCountryCodes(continued)
ISOCurrencyCodes
TheTradeSuiteID®servicesupportsthecurrencycodesshowninTable1.2andmaintainedbyISOatISO4217
CurrencyCodes.Foralistofcountrycodes,seecountrycodes,showninTable1.1.
CurrencyCode Description
AED UAEdirham
AFN Afghani
ALL Lek
AMD Armeniandram
ANG NetherlandsAntilleanguilder
AOA Kwanza
ARS Argentinepeso
AUD Australiandollar
AWG Arubanflorin
Table1.2ISOCurrencyCodes
Input/OutputInformation
1.Input/OutputInformationCodes 15

---

## Page 16

CurrencyCode Description
AZN Azerbaijanmanat
BAM Convertiblemark
BBD Barbadosdollar
BDT Taka
BGN Bulgarianlev
BHD Bahrainidinar
BIF Burundifranc
BMD Bermudiandollar
BND Bruneidollar
BOB Boliviano
BOV Mvdol
BRL Brazilianreal
BSD Bahamiandollar
BTN Ngultrum
BWP Pula
BYN Belarussianruble
BZD Belizedollar
CAD Canadiandollar
CDF Congolesefranc
CHE Wireuro
CHF Swissfranc
CHW Wirfranc
CLF Unidadesdeformento
CLP Chileanpeso
CNY Yuanrenminbi
COP Colombianpeso
COU UnidaddeValorreal
CRC CostaRicancolon
CVE CapeVerdeescudo
CZK Czechkoruna
DJF Djiboutifranc
DKK Danishkrone
Table1.2ISOCurrencyCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 16

---

## Page 17

CurrencyCode Description
DOP Dominicanpeso
DZD Algeriandinar
EGP Egyptianpound
ERN Nakfa
ETB Ethiopianbirr
EUR Euro
FJD Fijidollar
FKP FalklandIslandspound
GBP Poundsterling
GEL Lari
GHS Ghanacedi
GIP Gibraltarpound
GMD Dalasi
GNF Guineafranc
GTQ Quetzal
GYD Guyanadollar
HKD HongKongdollar
HNL Lempira
HTG Gourde
HUF Forint
IDR Rupiah
ILS NewIsraelishekel
INR Indianrupee
ISK Icelandkrona
JMD Jamaicandollar
JOD Jordaniandinar
JPY Yen
KES Kenyanshilling
KGS Som
KHR Riel
KMF Comorofranc
KRW Won
Table1.2ISOCurrencyCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 17

---

## Page 18

CurrencyCode Description
KWD Kuwaitidinar
KYD CaymanIslandsdollar
KZT Tenge
LAK Kip
LBP Lebanesepound
LKR Srilankarupee
LRD Liberiandollar
LSL Loti
LYD Libyandinar
MAD Moroccandirham
MDL Moldovanleu
MGA Malagasyariary
MGF Malagasyfranc
MKD Denar
MMK Kyat
MNT Tugrik
MOP Pataca
MRU Ouguiya
MUR Mauritiusrupee
MVR Rufiyaa
MWK Malawiankwacha
MXN Mexicanpeso
MXV MexicanUnidaddeInversion(udi)
MYR Malaysianringgit
MZN Mozambiquemetical
NAD Namibiadollar
NGN Naira
NIO Cordobaoro
NOK Norwegiankrone
NPR Nepaleserupee
NZD NewZealanddollar
OMR Rialomani
Table1.2ISOCurrencyCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 18

---

## Page 19

CurrencyCode Description
PAB Balboa
PEN Nuevosol
PGK Kina
PHP Philippinepeso
PKR Pakistanrupee
PLN Zloty
PYG Guarani
QAR Qataririal
RON Romanianleu
RSD Serbiadinar
RUB Russianrubie
RWF Rwandafranc
SAR Saudiriyal
SBD SolomonIslandsdollar
SCR Seychellesrupee
SEK Swedishkrona
SGD Singaporedollar
SHP St.helenapound
SLE Sierraleone
SOS Somalishilling
SRD Surinamdollar
STN Dobra
SVC ElSalvadorcolon
SZL Lilangeni
THB Baht
TJS Somoni
TMT Turkmenistannewmanat
TND Tunisiandinar
TOP Pa'anga
TRY Turkishlira
TTD TrinidadandTobagodollar
TWD NewTaiwandollar
Table1.2ISOCurrencyCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 19

---

## Page 20

CurrencyCode Description
TZS Tanzanianshilling
UAH Hryvnia
UAK Karbovanet
UGX Ugandashilling
USD USdollar
USN USdollar(nextday)
UYI UruguayPesoenUnidadesIndex
UYU Pesouruguayo
UZS Uzbekistansum
VES Bolivar
VND Vietnamdong
VUV Vatu
WST Tala
XAF Cfafrancbeac
XCD EastCaribbeandollar
XDR Sdr(specialdrawingright)
XOF Cfafrancbceao
XPF Cfpfranc
XSU Sucre
XUA Adbunitofaccount
YER Temenirial
ZAR Rand
ZMW Zambiankwacha
ZWL Zimbabwedollar
Table1.2ISOCurrencyCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 20

---

## Page 21

MarketCodesandAbbreviations
TheTradeSuiteID®servicesupportsthemarketcodesandmarketabbreviationsshowninTable1.3and
maintainedbyISOinISO10383:2012,Securitiesandrelatedfinancialinstruments--Codesforexchangesand
marketidentification(MIC).
Marketcode Exchange Abbreviation Area
95 Amex144A 144A USExchanges
16 AmexBasketTrade ABSK USExchanges
14 AveragePriceTrade AVGP USExchanges
03 BrokertoBrokerTrade BKEX USExchanges
18 CBOEBasketTrade CBSK USExchanges
05 ChicagoStockExchange CSE USExchanges
19 CincinnatiStockExchange CSX USExchanges
96 NASDPortal 144P USExchanges
04 NASDAQOMXBX(Boston) XBOS USExchanges
06 NASDAQOMXPHLX(Philadelphia) XPHL USExchanges
02 NewYorkStockExchange [[NYSE]] USExchanges
94 NYSE144A 144N USExchanges
01 NYSEAmexEquities ALTX USExchanges
15 NYSEBasketTrade NBSK USExchanges
07 [[Option]] EXER USExchanges
13 Other OTH USExchanges
09 OvertheCounter [[OTC]] USExchanges
17 OvertheCounterBasketTrade OBSK USExchanges
08 PacificStockExchange PSE USExchanges
10 Principal PRN USExchanges
12 Special SPC USExchanges
11 [[syndicate]] SYN USExchanges
51 SyndicateDirectedConcession SYDC USExchanges
52 SyndicateOverSubscribed SYOS USExchanges
Table1.3MarketCodesandAbbreviations
Input/OutputInformation
1.Input/OutputInformationCodes 21

---

## Page 22

Marketcode Exchange Abbreviation Area
53 SyndicateDirected/OverSubscribed SYDO USExchanges
90 StockBorrow SBOR USExchanges
91 StockLoan SLON USExchanges
AR NYSEARCA,INC ARCO USExchanges
92 StockLoanRecall SLRC USExchanges
[[ID]] InvestorsExchangeDark IEXD USExchanges
IG InvestorsExchange IEXG USExchanges
LT Long-TermStockExchange.Inc LTSE USExchanges
ME MEMX,INC MEMX USExchanges
MN MiamiInternationalSecuritiesExchange XMIO USExchanges
20 BATS XBAT USExchanges
26 BarclaysLiquidMarkets BARL USExchanges
27 C2 C20X USExchanges
29 NASDAQOMXPSX XPSX USExchanges
30 Knight KNIG USExchanges
48 LavaTrading(Citi) LAVA USExchanges
49 Tripleshot TSBX USExchanges
54 BarclaysATS BARX USExchanges
55 ITG-Posit ITGI USExchanges
80 DirectEdgeA EDGA USExchanges
81 DirectEdgeX EDGX USExchanges
93 StockLoanReturn SLRT USExchanges
25 BATSBYX YBAT USExchanges
97 InvestorsExchange IEXG USExchanges
98 InvestorsExchange-Dark IEXD USExchanges
PG Asuncion(Paraguay) PGUY Americas(ExcludingUS)
BG Bogota(Colombia) BGTA Americas(ExcludingUS)
BE BuenosAires(Argentina) BUEN Americas(ExcludingUS)
CA Caracas(Venezuela) CRCS Americas(ExcludingUS)
KS Kingston(Jamaica) KSTN Americas(ExcludingUS)
BO LaPaz(Bolivia) BOLV Americas(ExcludingUS)
Table1.3MarketCodesandAbbreviations(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 22

---

## Page 23

Marketcode Exchange Abbreviation Area
LI Lima(Peru) LIMA Americas(ExcludingUS)
24 MexicoCity(Mexico) MEXC Americas(ExcludingUS)
UR Montevideo(Uruguay) URGY Americas(ExcludingUS)
22 Montreal(Canada) MONT Americas(ExcludingUS)
PN PanamaCity(Panama) PNMA Americas(ExcludingUS)
TT PortofSpain(Trinidad/Tobago) TRTO Americas(ExcludingUS)
EC Quito(Ecuador) ECUA Americas(ExcludingUS)
RI RioDeJaneiro(Brazil) RIOD Americas(ExcludingUS)
RO Rosario(Argentina) ROSA Americas(ExcludingUS)
CO SanJose(CostaRica) COSR Americas(ExcludingUS)
HO SanPedroSula(Honduras) HOND Americas(ExcludingUS)
SS SanSalvador(ElSalvador) SANS Americas(ExcludingUS)
ST Santiago(Chile) STGO Americas(ExcludingUS)
SD SantoDomingo(DominicanRepublic) STOD Americas(ExcludingUS)
SP SaoPaulo(Brazil) SAPA Americas(ExcludingUS)
BD St.Michael(Barbados) BARB Americas(ExcludingUS)
21 Toronto(Canada) TORO Americas(ExcludingUS)
23 Vancouver(Canada) VANC Americas(ExcludingUS)
41 Amsterdam(Netherlands) AMST Europe
DE BorseFrankfurt-RegulierterMarket FRAA Europe
AT Athens(Greece) ATHN Europe
FI FirstNorthernFinland FNFI Europe
BR Barcelona(Spain) BRCL Europe
BL Bilbao(Spain) BILB Europe
SV Bratislava(Slovakia) SVKA Europe
32 Brussels(Belgium) BRUX Europe
BP Budapest(Hungary) BUDP Europe
33 Copenhagen(Denmark) DENM Europe
CR Croatia(Zagreb) CROA Europe
Table1.3MarketCodesandAbbreviations(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 23

---

## Page 24

Marketcode Exchange Abbreviation Area
38 Dublin(Ireland) DUBL Europe
34 EuropeanEconomicCommunity EECO Europe
37 Frankfurt(Germany) GERF Europe
46 Geneva(Switzerland) GEVA Europe
35 Helsinki(Finland) HELS Europe
PT Lisbon(Portugal) PORT Europe
SL Ljubljana(Slovenia) SLOV Europe
47 London(UnitedKingdom) LNDN Europe
40 Luxembourg(Luxembourg) LUXE Europe
43 Madrid(Spain) MADR Europe
39 Milan(Italy) ITMI Europe
MO Moscow(Russia) MOSC Europe
42 Oslo(Norway) OSLO Europe
36 Paris(France) PARI Europe
PR Porto(Portugal) PRTO Europe
CZ Prague(CzechRepublic) CZEC Europe
RK Reykjavik(Iceland) ICLA Europe
BU Sofia(Bulgaria) BULG Europe
SG St.Petersburg(Russia) STPT Europe
44 Stockholm(Sweden) STOK Europe
VL Valencia(Spain) VLCA Europe
VT virt-x Europe
31 Vienna(Austria) VIEN Europe
WZ Warsaw(Poland) WARZ Europe
45 Zurich(Switzerland) ZURH Europe
BN Bangalore(India) BNGL PacificBasin
BK Bangkok(Thailand) BNGK PacificBasin
BB Bombay(India) BMBY PacificBasin
Table1.3MarketCodesandAbbreviations(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 24

---

## Page 25

Marketcode Exchange Abbreviation Area
CL Colombo(SriLanka) CLMB PacificBasin
DH Dhaka(Bangladesh) DHKA PacificBasin
73 HongKong(HongKong) HONG PacificBasin
JK Jakarta(Indonesia) JKTA PacificBasin
KR Karachi(Pakistan) KRCH PacificBasin
76 KualaLumpur(Malaysia) MALY PacificBasin
78 Manila(Philippines) PHPS PacificBasin
72 Melbourne(Australia) MELB PacificBasin
ND NewDelhi(India) NDEL PacificBasin
75 Osaka(Japan) OSAK PacificBasin
SE Seoul(Korea) SEUL PacificBasin
SH Shanghai(China) SHGH PacificBasin
SZ Shenzhen(China) SHEN PacificBasin
79 Singapore(Singapore) SGPR PacificBasin
71 Sydney(Australia) SYDN PacificBasin
TP Taipei(Taiwan) TAIP PacificBasin
74 Tokyo(Japan) TOKY PacificBasin
77 Wellington(NewZealand) NEWZ PacificBasin
IC Abidjan(IvoryCoast) IVCT Africa/MiddleEast
GH Accra(Ghana) GHNA Africa/MiddleEast
AM Amman(Jordan) AMAN Africa/MiddleEast
BH Bahrain(Bahrain) BHRN Africa/MiddleEast
EG Cairo(Egypt) CIRO Africa/MiddleEast
CB Casablanca(Morocco) CSBL Africa/MiddleEast
BT Gaborone(Botswana) GBRN Africa/MiddleEast
ZI Harare(Zimbabwe) ZIMB Africa/MiddleEast
IS Istanbul(Turkey) ISTB Africa/MiddleEast
SA Johannesburg(SouthAfrica) JHNB Africa/MiddleEast
Table1.3MarketCodesandAbbreviations(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 25

---

## Page 26

Marketcode Exchange Abbreviation Area
KW Kuwait(Kuwait) KWAT Africa/MiddleEast
LA Lagos(Nigeria) LAGS Africa/MiddleEast
SW Mbabane(Swaziland) SWZL Africa/MiddleEast
OM Muscat(Oman) OMAN Africa/MiddleEast
NR Nairobi(Kenya) NRBI Africa/MiddleEast
PL PortLouis(Mauritius) PTLS Africa/MiddleEast
RY Riyadh(SaudiArabia) RYDH Africa/MiddleEast
TA Tel-Aviv(Israel) TLAV Africa/MiddleEast
TU Tunis(Tunisia) TUNS Africa/MiddleEast
ML Valleta(Malta) MLTA Africa/MiddleEast
NM Windhoek(Namibia) NMBA Africa/MiddleEast
Table1.3MarketCodesandAbbreviations(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 26

---

## Page 27

Index(Benchmark)Codes
Table1.4showsthecodesandgivestheshortnameforthecorrespondingmarketindex.
Code ShortName Description
00 Notspecified
01 A$SW Australiadollarswaprate
02 C$BA Canadiandollarbankersacceptances
03 C$CMT Canadiandollarconstantmaturitytreasury
04 CMT Constantmaturitytreasury
05 FFUND Federalfunds
06 GB$SW Sterling/U.S.dollarswaprate
07 GBSW Sterlingswaprate
08 JYCMT JapaneseYenconstantmaturitytreasury
09 JYLIB JapaneseYenLondoninterbankovernightrate
10 LIBOR U.S.dollarLondoninterbankovernightrate
11 NIKKE NIKKEI300index
12 PRIME Primerate
13 STLIB SterlingLondoninterbankovernightrate
14 US$SR U.S.dollarswaprate
15 INDU DowJonesindustrialaverage
16 $TRAN DowJonestransportationaverage
17 $UTIL DowJonesutilitiesaverage
18 $NDX NASDAQ100index
19 $COMPQ NASDAQcompositeindex
20 $NYA NYSEcompositeindex
21 $SPX S&P500stockindex
22 $MID S&P400midcapstockindex
23 $OEX S&P100stockindex
24 $IXCO NASDAQhightechnologyindex
25 $PSE PSEhightechnologyindex
26 $MSH MorganStanleyhightechindex
27 $SOX Semiconductorindex
Table1.4Index(Benchmark)Codes
Input/OutputInformation
1.Input/OutputInformationCodes 27

---

## Page 28

Code ShortName Description
28 $XMI AMEXmajormarketindex
29 $XAX AMEXcompositeindex
30 $TXSX-TC S&P/TSX60index
31 $TSX-TC S&P/TSXcompositeindex
32 $TSXC-TC S&P/TSX300cappedindex
33 $TNX 10yearT-noteinterestrate(X.10)
34 $TYX 30yearT-bondinterestrate(X.10)
35 $XAU PHLXgoldandsilverindex
36 $XOI AMEXoilandgas
37 $XVG Valuelineindex(geometric)
38 $RUI RUSSELL1000
39 $RUT RUSSELL2000
40 $RUA RUSSELL3000
SettlementLocationCodes
Table1.5showsthesettlementlocationswithallrelateddetails.
Code LocationDescription LocalBICID
AD ANDORRA
ADS ABUDHABISTOCKMARKET(ADSM) ADSEAEA1
AF AFGHANISTAN
AG ANTIGUAANDBARBUDA
AI ANGUILLA
AL ALBANIA
AM ARMENIA
AN NETH.ANTILLES
AO ANGOLA
AQ ANTARTICA
AR ARGENTINA
AS AMERICANSAMOA
AT AUSTRIA
AU AUSTRALIA
AUC AUSTRACLEARLIMITED ACLRAU2SXXX
Table1.5SettlementLocationCodes
Input/OutputInformation
1.Input/OutputInformationCodes 28

---

## Page 29

Code LocationDescription LocalBICID
AW ARUBA
AZ AZERBAIJAN
BA BOSNIA-HERZEGOVINA
BB BARBADOS
BD BANGLADESH
BE BELGIUM
BF BURKINAFASO
BG BULGARIA
BH BAHRAIN
BI BURUNDI
BJ BENIN
BM BERMUDA
BN BRUNEIDARUSSALAM
BNZ NEWZEALAND RBNZNZ22XXX
BO BOLIVIA
BR BRAZIL
BRC BROKERCUSTODY
BS BAHAMAS
BT BHUTAN
BV BOUVETISLAND
BW BOTSWANA
BY BELARUS
BZ BELIZE
CA CANADA
CBE CENTRALBANKOFEGYPT CBEGEGCXXXX
CBL COMPANHIABRASILEIRADELIQUIDACAOECUST CLCBBRRJXXX
CC COCOS(KEELING)ISLANDS
CD CONGOTHEDEMOCRATICREPUBLICOFTHE
CDS CANADIANDEPOSITORYFORSECURITIESLTD CDSLCATTXXX
CED CEDEL CEDELULLXXX
CF CENTRALAFRICANREPUBLIC
CG CONGO
CH SWITZERLAND
CHS CHESSASXSETTLEMENTANDTRANSFERCORP CAETAU21XXX
CI COTED'IVOIRE
Table1.5SettlementLocationCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 29

---

## Page 30

Code LocationDescription LocalBICID
CIK CIK(CAISSEINTERPROFESSIONNELLEDEDEPO) CIKBBEBBXXX
CK COOKISLANDS
CL CHILE
CM CAMEROON
CN CHINA
CO COLOMBIA
CR COSTARICA
CS CZECHOSLOVAKIA
CV CAPEVERDE
CX CHRISTMASISLAND
CY CYPRUS XCYSCY2NXXX
CZ CZECHREPUBLIC
DE GERMANY
DFM DUBAIFINANCIALMARKET(DFM) DFMTAEA1
DJ DJIBOUTI
DK DENMARK
DM DOMINICA
[[DO]] DOMINICANREPUBLIC CVDPDOSD
[[DTC]] DEPOSITORYTRUSTCOMPANY DTCYUS33XXX
DZ ALGERIA
EC ECUADOR
EE ESTONIA ECSDEE2XXXX
EG EGYPT
EH WESTERNSAHARA
ER ERITREA
ES SPAIN IBRCESMMXXX
ET ETHIOPIA
EUR EUROCLEAR MGTCBEBEXXX
FED THEFEDERALRESERVEBANK FRNYUS33XXX
FI FINLAND
FJ FIJI
FK FALKLANDISLANDS(MALVINAS)
FM MICRONESIA
FNB FIRSTNATIONALBANKOFCHICAGO-LONDON
FO FAEROEISLANDS
Table1.5SettlementLocationCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 30

---

## Page 31

Code LocationDescription LocalBICID
FR FRANCE
GA GABON
GB UNITEDKINGDOM
GD GRENADA
GE GEORGIA
GF FRENCHGUIANA
GG GUERNSEY,C.I.
GH GHANA
GI GIBRALTAR
GL GREENLAND
GM GAMBIA
GN GUINEA
GP GUADELOUPE
GQ EQUATORIALGUINEA
GR GREECE
GS S.GEORGIAANDTHES.SANDWICHISLANDSUK
GT GUATEMALA
GU GUAM
GW GUINEA-BISSAU
GY GUYANA
HK HONGKONG
HKS HONGKONGSECURITIESCLEARINGCO.LTD. XHKCHKH1XXX
HM HEARDANDMCDONALDISLANDS
HN HONDURAS
HR CROATIA
HT HAITI
HU HUNGARY
[[ID]] PTKUSTODIANSENTRALEFEKINDONESIAKSEI KSEIIDJA
IE IRELAND
IL ISRAEL
IM ISLEOFMAN
IN INDIA
IND S.D.INDEVAL,S.A.DEC.V. INDEMXMMXXX
IO BRITISHINDIANOCEANTERRITORY
IQ IRAQ
Table1.5SettlementLocationCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 31

---

## Page 32

Code LocationDescription LocalBICID
IS ICELAND
IT ITALY
JAS JASDEC JJSDJPJTXXX
JE JERSEY,C.I.
JM JAMAICA
JO JORDAN SEDCJOA1XXX
JP JAPAN
KCC KUWAITCLEARINGCOMPANYS.A.K.(KCC)
KE KENYA
KG KYRGYZSTAN
KH CAMBODIA
KI KIRIBATI
KM COMOROS
KN SAINTKITTSANDNEVIS
KR KOREA,REPUBLICOF
KW KUWAIT
KY CAYMANISLANDS
KZ KAZAKHSTAN
LA LAOPEOPLE'SDEMOCRATICREPUBLIC
LB LEBANON
LC SAINTLUCIA
LI LIECHTENSTEIN
LK SRILANKA
LR LIBERIA
LS LESOTHO
LT LITHUANIA CSDLLT22XXX
LU LUXEMBOURG
LV LATVIA
LY LIBYANARABJAMAHIRIYA
MA MOROCCO
MC MONACO
MD MOLDOVA,REPUBLICOF
MDV CAJADEVALORESS.A. CAVLARBAXXX
MG MADAGASCAR
MH MARSHALLISLANDS
Table1.5SettlementLocationCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 32

---

## Page 33

Code LocationDescription LocalBICID
MK MACEDONIA,FORMERYUGOSLAVREPUBLIC/S.EUR
ML MALI
MN MONGOLIA
MO MACAU
MP NORTHERNMARIANAISLANDS
MQ MARTINIQUE
MR MAURITANIA
MS MONTSERRAT
MT MALTA
MU MAURITIUS
MV MALDIVES
MW MALAWI
MX MEXICO
MY MALAYSIA
MZ MOZAMBIQUE
NA NAMIBIA
NC NEWCALEDONIA
NE NIGER
NEC NEDERLANDSCENTRALINSTITUTVOORGIRAAL NECINL2AXXX
NF NORFOLKISLAND
NFS NOTFORSETTLEMENT
NG NIGERIA
NI NICARAGUA
NL NETHERLANDS
NO NORWAY
NP NEPAL
NR NAURU
NT NEUTRALZONE(BETWEENSAUDIANDIRAQ)
NU NIUE
NZ NEWZEALAND XAUKNZ21XXX
OKB OESTERREICHISCHEKONTROLLBANKAG OEKOATWWXXX
OM OMAN
PA PANAMA
PE PERU
PEX PEXSETTLE PEXSPTP1XXX
Table1.5SettlementLocationCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 33

---

## Page 34

Code LocationDescription LocalBICID
PF FRENCHPOLYNESIA
PG PAPUANEWGUINEA
PH PHILIPPINES
PK PAKISTAN
PL POLAND
PM ST.PIERREANDMIQUELON
PN PITCAIRNISLAND
PR PUERTORICO
PS PALESTINIANTERRITORYOCCUPIEDMIDDLEE
PT INTERBOLSA IBLSPTPPXXX
PW PALAU
PY PARAGUAY
PZ PANAMACANALZONE
QA QATAR
QAT DOHASECURITIESMARKET DSMDQAQAXXX
RE REUNION
RO ROMANIA
ROM DEPOZITARULCENTRUMS.A. DECNROBUXXX
RU RUSSIA
RW RWANDA
SA SAUDIARABIA
SAD CENTRALDEPOSITORYLIMITED,THE
SB SOLOMONISLANDS
SC SEYCHELLES
SCD CENTRALDEPOSITORY(PTE)LIMITED,THE CDPLSGSGXXX
SCR CENTRALDEPOSITORY(PTD)LIMITED,THE
SE SWEDEN
SEG SISSEGAINTERSETTLEAG INSECHZZXXX
SER SERBIACSD CSDECSB1XXX
SG SINGAPORE XXXMASGSGSM
SH ST.HELENA
SI SLOVENIA
SJ SVALBARDANDJANMAYENISLANDS
SK SLOVAKIA
SKD CENTRALNYDEPOZITARCENNYCHPAPIEROVSR CSDSSKB1XXX
Table1.5SettlementLocationCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 34

---

## Page 35

Code LocationDescription LocalBICID
SL SIERRALEONE
SLK CENTRALNYDEPOZITARCENNYCHPAPIEROVSR, CSDSSKBAXXX
SM SANMARINO
SN SENEGAL
SO SOMALIA
SR SURINAME
ST SAOTOMEANDPRINCIPE
STR STRATE STRAZAJJXXX
SV ELSALVADOR
SVC SERVICIODECOMPENSACIONYLIQUIDACION SCLVESMMXXX
SZ SWAZILAND
TAD TADAWULSAUDISTOCKMARKET TSSMSAR1XXX
TC TURKSANDCAICOSISLANDS
TD CHAD
TF FRENCHSOUTHERNTERRITORIES
TG TOGO
TH THAILAND TSDCTHBKXXX
TJ TAJIKISTAN
TK TOKELAU
TKD CZECHNATIONALBANK CNBACZPPXXX
TM TURKMENISTAN
TN TUNISIA
TO TONGA
TP EASTTIMOR
TR TURKEY
TT TRINIDADANDTOBAGO
TV TUVALU
TW TAIWAN TDCCTWTPXXX
TZ TANZANIA,UNITEDREPUBLICOF
TZE TZENTRALENDEPOZITAR CEDPBGSF
UA UKRAINE NADUUAUKXXX
UAE U.A.E DIFXAEAAXXX
UEC UNIVERSALEXCHANGECORPORATIONLIMITED UNEXZAJJXXX
UG UGANDA UGBAUGKAXXX
UKR NATIONALDEPOSITORYSYSTEM IRSUUAUKXXX
Table1.5SettlementLocationCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 35

---

## Page 36

Code LocationDescription LocalBICID
UM UNITEDSTATESMINOROUTLYINGISLANDS
UNI UNIVYCPLC UNIYCZPP
US UNITEDSTATES
USE UGANDASECURITIESEXCHANGE XUGAUGK1XXX
UY URUGUAY
UZ UZBEKISTAN
VA VATICANCITYSTATE
VC SAINTVINCENTANDTHEGRENADINES
VE VENEZUELA CVVCVEA1
VG VIRGINISLANDS(BRITISH)
VI VIRGINISLANDS,U.S.
VN VIETNAM
VPC VP(THEDANISHSECURITIESCENTRE) VPDKDKKKXXX
VPS VARDEPAPPERSCENTRALENVPCAB VPCSSESSXXX
VU VANUATU
WF WALLISANDFUTUNAISLANDS
WS SAMOA
YE YEMEN,REPUBLICOF
YT MAYOTTEPACIFICBASIN
YU YUGOSLAVIA
ZA SOUTHAFRICA STRAZAJJXXX
ZM ZAMBIA BAZAZMLUXXX
ZR ZAIRE
ZW ZIMBABWE
Table1.5SettlementLocationCodes(continued)
CancellationReasonCodes
Thefollowingtableshowsthecancellationreasoncodes.
Code Description
000 Unspecifiedissue.
001 Incorrecttradedate.
002 Incorrectsettlementdate.
Table1.6CancellationReasonCodes
Input/OutputInformation
1.Input/OutputInformationCodes 36

---

## Page 37

Code Description
003 Incorrectsecuritynumber.
004 Incorrectsecuritynumbersystem.
005 Incorrectsecuritytype.
006 Incorrectsecuritydescription.
007 Incorrectsettlementtype.
008 Incorrectsettlementlocation.
009 Incorrectbuy/sell.
010 Incorrectshares/facevalue.
011 Incorrectprice.
012 Incorrectprincipalamount.
013 Incorrectinterest.
014 Incorrectcurrencycode.
015 Incorrectaverageprice.
016 Incorrectcommission.
017 Incorrectsplitindicator.
018 Incorrectsecurity(regulatory)fees.
019 Incorrectregistrationorshippingamount.
020 Incorrectresearchamount.
021 Incorrectcountrytax.
022 Incorrectothercharges.
023 Incorrectnetamount.
024 Incorrectaccountnumber.
025 Incorrectcommissionequivalent.
026 Incorrectinterestedparty#1.
030 Incorrectinterestedparty#2.
034 Incorrectinterestedparty#3.
038 Incorrectcustomer.
040 Incorrectrole.
041 Incorrectmarket.
042 Incorrectnetprice.
043 Incorrectaccounttype.
044 Incorrectalternatecurrency.
Table1.6CancellationReasonCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 37

---

## Page 38

Code Description
046 Incorrectalternatecurrencyrate.
047 Incorrectalternatenetamount.
048 Incorrectinstitution(investmentmanager).
049 Incorrectagent.
050 Incorrectinterestedparty.
051 BrokerSub-CustWrong
052 AgentSub-CustWrong
053 Amort/AccretFactorWrong
054 SpecialInstructionWrong
057 TickerSymbolWrong
058 AllocationWrong
059 Don'tKnowExecution
060 CommissionTypeWrong
062 InstitutionAcct#Wrong
063 IDStep-InBrokerWrong
064 DummyAllocationWrong
065 BranchOrExBrokerWrong
066 TransactionTypeWrong
067 Branch/BrokerNotifyWg
068 InstitutionRefIDWrong
069 SubmitInstitutionWrong
070 IDAgentWrong
071 IDAgentIntAcct#Wrong
072 PrincipalAmountWrong
073 IDBrokerOfCreditWrong
074 Non-IDBrcWrong
075 InstitutionNumberWrong
076 Non-IDStepinBkrWrong
077 StepinBkrNotifyIndWg
079 Step-OutReasonCode#1
080 Step-OutReasonCode#2
081 Step-OutReasonCode#3
Table1.6CancellationReasonCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 38

---

## Page 39

Code Description
082 Step-OutReasonText
085 BrokerOfCreditCom/Fee
086 NoeRefIdentifierWrong
087 InstOrderRoute#Wrong
088 Step-OutIndicatorWrong
089 DetRefIndentifierWrong
090 AllocationReasonCodeWg
100 DoNotKnow
101 DuplicateConfirm
102 Confirm/RebillSame
103 AllocationChange
104 WrongDelvInstruction
105 MultipleErroneousFields
106 AwaitingInstrToAffirm
107 TbaCancelDueToAlloc
108 TbaCancellation
109 PoolSubstitution
110 PoolCancellation
111 MbsMiscellaneousCancel
121 Long/ShortIndInvalid
122 CannotLocateSecurities
500 CurrentFaceWrong
501 Factor/EffectDateWrong
502 PoolNumberWrong
503 RelatedReferenceNumWrg
504 NumDaysAccruedIntWrng
505 YieldWrong
506 IssueDateWrong
507 RecordDateWrong
508 TradeTypeIndWrong
509 ClrAgtIntAcctNumWrng
510 InstitIntAcctNumWrong
Table1.6CancellationReasonCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 39

---

## Page 40

Code Description
511 InstOrderRoutNumWrong
512 AdditionalParty#4Wrong
513 AdditionalParty#5Wrong
514 Add'LPty#1AcctNumWrg
515 Add'LPty#2AcctNumWrg
516 Add'LPty#3AcctNumWrg
517 Add'LPty#4AcctNumWrg
518 Add'LPty#5AcctNumWrg
519 Add'LPty#6AcctNumWrg
520 Add'LPty#1Instr#1Wrg
521 Add'LPty#2Instr#1Wrg
522 Add'LPty#3Instr#1Wrg
523 Add'LPty#4Instr#1Wrg
524 Add'LPty#5Instr#1Wrg
525 Add'LPty#6Instr#1Wrg
526 Add'LPty#1Instr#2Wrg
527 Add'LPty#2Instr#2Wrg
528 Add'LPty#3Instr#2Wrg
529 Add'LPty#4Instr#2Wrg
530 Add'LPty#5Instr#2Wrg
531 Add'LPty#6Instr#2Wrg
532 SpecInSlot#01Wrong
533 SpecInSlot#02Wrong
534 SpecInSlot#03Wrong
535 SpecInSlot#04Wrong
536 SpecInSlot#05Wrong
537 SpecInSlot#06Wrong
538 SpecInSlot#07Wrong
539 SpecInSlot#08Wrong
540 SpecInSlot#09Wrong
541 SpecInSlot#10Wrong
542 SpecInSlot#11Wrong
Table1.6CancellationReasonCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 40

---

## Page 41

Code Description
543 SpecInSlot#12Wrong
544 SpecInSlot#13Wrong
545 SpecInSlot#14Wrong
546 SpecInSlot#15Wrong
547 SpecInSlot#16Wrong
560 ConfirmPurposeWrong
561 DeliveryMethodWrong
562 PriceTypeWrong
563 TradeTypeWrong
564 LegIdentifierWrong
565 CollateralTypeWrong
566 Tri-PartyAgentWrong
567 StartDateWrong
568 EndDate/MaturityDateWr
569 FinRateWrong
570 SecLendingFeeWrong
571 InterestDaysWrong
572 AccruedIntDueAtMatWg
573 [[Haircut]]%Wrong
574 RepoValueWrong
575 CurrYieldWrong
576 YieldToMatWrong
577 YieldToCall/RedemWrong
578 DatedDateWrong
579 MarkUp/DownSignWrong
580 MarkUp/DownWrong
581 IncorrectUsrDefCode
582 BkrPhone#Wrong
583 AllocSourceWrong
584 3RdPrtyRemunRecdWg
999 Other
Table1.6CancellationReasonCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 41

---

## Page 42

IneligibleConfirmationCodes
TradeinputsubmittedforDepositoryTrustCompany([[DTC]])settlementcangenerateineligibleconfirmationsfor
thereasonsshowninTable1.7.[[DTC]]-eligibilityisre-evaluatedduringaffirmationandend-of-dayprocessinguntil
andincludingS-1.WiththeintroductionofTradeSuiteIDnet,eligibilitystatuschangescanoccurintraday.If
eligibilitychangesbetweentradeinputandaffirmation(includingmatchedaffirmed),theaffirmedormatched
affirmedconfirmationshowsaneligibilitystatusdifferentfromwhatwaspreviouslyshown.
Attheendoftheday,thesystemalsore-evaluateseligibilityforconfirmations(“unaffirmed”or“matchedand/or
affirmed”)thatwerepreviouslyreported.Iftheeligibilitystatuschangesduringtheday,thesystemproducesa
ChangeofEligibilityConfirmation(positions3–8equalsCOELIGintheTransactionheader)aspartoftheend-of-
day([[EOD]])reports.Thisdoesnotincludeanyconfirmationsforwhicheligibilitywaspreviouslyreportedas
changedataffirmation.
Code1 Explanation
20 IDNetchangedtosettlingpredeterminedquantity(PDQ).
IDnettradeconfirmredeterminedtosettletrade-for-trade(PDQ).
21 IDNetchangedtoineligible.
IDNettradeconfirmredeterminedasineligible.
22 Inventorymanagementservices(IMS)cancelsclearingagentcancel.
IDNettradeconfirmcanceledinIMSbytheclearingagent.
23 IMScancelsclearingbrokercancel.
IDNettradeconfirmcanceledinIMSbyclearingbroker.
24 IMScancelsclearingbrokerexemption.
IDNettradeconfirmexemptedinIMSbytheclearingbroker.
25 IMSreject
IDNettradeconfirmrejectedinIMS.
26 ATPreject
IDNettradeconfirmrejectedinATP.
27 ATPdrop
IDNettradeconfirmdroppedinATP.
28 IMSunprocessedexemption.
IDNettradeconfirmunprocessedexemptioninIMS.
29 IMSclearingagentexemption.
IDNettradeconfirmexemptedinIMSbytheclearingagent.
Table1.7IneligibleConfirmationCodes
1SeeConfirmTradeOutputMessageSpecification,detailrecord1,positions916–925.
Input/OutputInformation
1.Input/OutputInformationCodes 42

---

## Page 43

Code1 Explanation
31 ClearingagentCNSineligible.
IDNettradeconfirmredeterminedthattheclearingagentCNSineligible.
32 ClearingbrokerCNSineligible.
IDNettradeconfirmredeterminedclearingbrokerCNSineligible.
60 CommitteeonUniformSecurityIdentificationProcedures([[CUSIP]])isCNSineligibleCUSIPnumber
isineligibleforCNSsettlement.
61 CUSIPineligible.
CUSIPnumberisineligibleforDTCsettlement.
62 CUSIPfrozen
CUSIPnumberisfrozen.
64 When-IssuedorWhen-Distributedtrade
Settlementcodeisoneofthefollowing:
2=When-Issued
3=When-Distributed
4=When-IssuedorWhen-Distributed
65 ClearingagentnotSDFS
ClearingagentbanknumberontheDTC-eligibilityfileisnotsettoSDFS,andthesecurityisan
SDFSissue.
66 ClearingbrokernotSDFS
Clearingbroker/dealernumberontheDTC-eligibilityfileisnotsettoSDFS,andthesecurityisan
SDFSissue.
67 CTMAFFIRMINT1INV
InterestedParty1intheM2iAffirmConfirmisinvalid
68 CTMAFFIRMINT2INV
InterestedParty2intheM2iAffirmConfirmisinvalid
74 Samedaytrade
Settlementdateequalsthetradedate.
75 Pastdatetrade
Confirmdateisgreaterthanthesettlementdateminus2(tradeinputwasenteredonorafterS-1;
therefore,thetradeisineligibleforautomatedsettlement).IfaffirmedaftertheS-1cutoff(11:30AM)
untilthesettlementdateat12:00PM,thetradewillbesenttoDTCasalateaffirmedtradeifitmeets
allothereligibilitycriteria.
78 Depositorychill
DeliveriesforthissecuritycannotbemadetoorfromaDTCparticipant.
Table1.7IneligibleConfirmationCodes(continued)
1SeeConfirmTradeOutputMessageSpecification,detailrecord1,positions916–925.
Input/OutputInformation
1.Input/OutputInformationCodes 43

---

## Page 44

Code1 Explanation
79 Agentparticipantchill
Participantisineligiblefordeliveryprocessingoreurocurrencydeliveryprocessing.
80 Brokerparticipantchill
ParticipantisineligiblefordeliveryprocessingorEurocurrencydeliveryprocessing.
81 Lateaffirm
TradewasaffirmedafterS-1cutoffandisineligibleforautomatedsettlement.TradeissenttoDTC
asaLateAffirmedTradewhenaffirmedbeforeafterS-1cutoff(11:30AM)until12:00PMonthe
settlementdate.t
822 Agentparticipantinvalid
ClearingagentisnotaDTCparticipant.
832 Brokerparticipantinvalid
ClearingbrokerisnotaDTCparticipant.
842 Securitytypeineligible
Securitytypechangedfromanequitytoabondorfromabondtoanequityforoldformattradeinput.
85 Agentbankineligible
AgentbankisineligibleforDTCprocessing.Thismessageisforold-formatinputonlyandresultsin
anineligibleconfirmforDTC-eligibletrades.Thisconditionwouldresultinatradeerroriftheinput
wassubmittedinnewformat.
86 Brokerconfirmnumbernotunique.
ThisisaninformativemessageanddoesnotaffectDTC-eligibility.Anold-formattradeinputwas
submittedwithaduplicatebroker/dealerconfirmnumber.Thisresultedintradeerror(codeGAAB
IAAOininteractiveformat).
87 Attempttocancelaffirmedtrade.
Thiscodeisgeneratedwhenabroker/dealersubmitsacancellationonatradeinputforanaffirmed,
matchedormatchedaffirmedconfirm.
88 Fractionalshares
Theconfirmationcontainsfractionalshares.
89 Trade-for-trade(PDQ)redeterminedtosettleIDNet.
Theconfirmwasinitiallydeterminedtosettletrade-for-trade(PDQ),butnowsettlingIDNet.
Table1.7IneligibleConfirmationCodes(continued)
1SeeConfirmTradeOutputMessageSpecification,detailrecord1,positions916–925.
2ThisconditiondoesnotoccurwhentheconfirmisinitiallyproducedbyDTC.Itcanonlyoccurduringaffirmation,match-
ing,orchangingtheeligibilityprocessing.
Input/OutputInformation
1.Input/OutputInformationCodes 44

---

## Page 45

Code1 Explanation
90 DTCtrade-for-tradeconfirmredeterminedtosettleCNS.
Confirmwasinitiallydeterminedtosettleasatrade-for-tradedeliveryatDTC;however,after
affirmation,DTCchangedtheCNSeligibilityoftheprimebroker,orNSCCchangedtheCNS
eligibilityofthesecurity;thedeliverysettleswithinCNS.
91 IPOinvalidagentaccount.
Thiscodeisusedforflipping,tonotifythepartiestothetradethatthesecurityisatrackinginitial
publicoffering([[IPO]])andthecustomerofthetradeisnotidentifiedorincorrectlyidentifiedbythe
agentinternalaccountnumber.Asaresult,thistradepotentiallycannotsettleatDTC.
92 TBAtrade
IneligibleforsettlementatDTC.
93 FBEparticipantchill
WhentheclearingbrokerorclearingagentarechilledontheDTCparticipantmasterfile.
94 CUSIPnotSDFS
95 CUSIPnotNDFS
96 SDFSineligible
97 Ineligiblebyrequest
98 CUSIPnotU.S.
99 Miscellaneous
InputofconfirmoccurredonorbeforeJune2,1994,anditwasineligiblebasedoneligibility
requirementsineffectbeforeJune2,1994.Thenewsystemdoesnotsupportacodetoidentify
theseolderrequirements;thesetradeswouldhavepreviouslybeenreportedascodes47,48,49,
50,52,53,56,or57.Theyareallreportedwithinthiscategory.
Table1.7IneligibleConfirmationCodes(continued)
1SeeConfirmTradeOutputMessageSpecification,detailrecord1,positions916–925.
Input/OutputInformation
1.Input/OutputInformationCodes 45

---

## Page 46

InteractiveFormatInputtoEODFormatOutputCode
Conversion
Table1.8showstheconversionfromcurrencycodesininteractiveformatinputtocurrencycodesinEODformat
output.
Note
Interactiveformatinputcontaininganyoftheabovecurrencycodesisconvertedtothecorrespondingnumeric
valueforreceiptbyend-of-dayformatusers.Allothercurrencycodesareconvertedto99(Other).
InteractiveFormat End-of-DayFormatDomestic
USD 01
GBP 02
FRF 03
CAD 04
CHF 05
XEU 06
DEM 07
AUD 08
NLG 09
HKD 10
SGD 11
ITL 12
KWD 13
NOK 14
AED 15
ARS 16
SAR 17
ESP 18
[[ATS]] 19
MXP 20
SEK 21
FIM 22
JPY 23
Table1.8CurrencyCodes
Input/OutputInformation
1.Input/OutputInformationCodes 46

---

## Page 47

InteractiveFormat End-of-DayFormatDomestic
ZAR 24
BEF 25
NZD 28
XXX 99
Table1.8CurrencyCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 47

---

## Page 48

Mortgage-BackedSecuritiesSpecificationCodes
Table1.9providesvaluesforspecificationcodes1–16:
l Tradeinputspecification,positions219–506ofrecord4.
l Tradeoutputspecification,positions249–536ofrecord4.
l FieldcodesGAC2inTable2.3.
Inthistable,theabbreviationsintheFielddefinitioncolumnstandforthefollowing:
l AL—alphabetic,left-justified.
l NU—numeric,right-justified.
l CH—character,left-justified.
l DT—dateinYYYYMMDDformat,left-justified.
Code Description
001 CollateralRegion
002 CollateralRegionExcluding
003 IssuanceRegionCode
004 IssuanceRegionExcludeCode
005 IssueDate-Earliest
006 IssueDate-Latest
007 MaturityDate-Earliest
008 MaturityDate-Latest
020 Pieces-MaximumNumberPerTrade
021 Pieces-MinimumNumberPerTrade
022 Pools-MaximumNumber
023 Pools-MinimumNumber
024 PoolsMaximumCurrentFaceValue
025 PoolsMinimumCurrentFaceValue
026 PoolsPerMillion-Maximum
027 PoolsPerMillion-Minimum
040 Variance(ForNon-BondMarketAssociation(Bma)Standards
Table1.9Mortgage-BackedSecuritiesSpecificationCodes
Input/OutputInformation
1.Input/OutputInformationCodes 48

---

## Page 49

Code Description
041 NoDownsideVariance(PopulateY)
050 WeightedAverageCoupon(Wac)Code-MaximumPercent(%)
051 WacCode-MinimumPercent(%)
052 WeightedAverageMaturity(Wam)Code-MaximumNumberOfMonths
053 WamCode-MinimumNumberOfMonths
054 WeightedAverageLoanAge(Wala)/CommercialAndGovernmentEntity(Cage)-Maximum
055 Wala/Cage-Minimum
060 Index
070 InterestRateCap-Maximum
071 InterestRateCap-Minimum
072 PaymentPercentageCap-Maximum
073 PaymentPercentageCap-Minimum
074 PeriodicCap-Maximum
075 PeriodicCap-Minimum
076 ResetDate-Earliest
077 ResetDate-Latest
100 Reasignment
999 FreeFormSpecification
Table1.9Mortgage-BackedSecuritiesSpecificationCodes(continued)
Moody’sConversionCodesandRatings
ThefollowingtableshowstheMoody’sconversioncodesandratings.
Position412–413 Rating
99 WR(Withdrawn)
96 Aaa*
95 Aaa
90 Aa1
85 Aa
84 Aa2
83 Aa3
Table1.10Moody’sConversionCodes
Input/OutputInformation
1.Input/OutputInformationCodes 49

---

## Page 50

Position412–413 Rating
75 A1
65 A
64 A2
63 A3
55 Baa1
45 Baa
44 Baa2
43 BAA3
40 Ba1
35 Ba
34 Ba2
33 Ba3
30 B1
25 B
24 B2
23 B3
22 Caa1
21 Caa
20 Caa2
19 VMIG4
18 VMIG3
17 VMIG2
16 VMIG1
15 CAA3
00 Non-rated
Table1.10Moody’sConversionCodes(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 50

---

## Page 51

Standard&Poor’sConversionCodesandRatings
Table1.11showstheStandard&Poor’s(S&P's)conversioncodesandratings.
Position417–418Code Rating
99 AAAL
96 AAA*
95 AAA
89 AAL
86 AA+
85 AA
84 AA-
80 WR
79 A-3
78 A-2
77 A-1
76 A+
75 A
74 A-
73 A-1+
72 A-1
71 A-1+
70 A-2
69 A-3
66 BBB+
65 BBB
64 BBB-
56 BB+
55 BB
54 BB-
47 B
00 Non-rated
46 B+
Table1.11Standard&Poor’sConversionCodes
Input/OutputInformation
1.Input/OutputInformationCodes 51

---

## Page 52

Position417–418Code Rating
45 B
44 B-
36 CCC
35 CCC
34 CCC
25 CC
24 E-1
23 E-2
22 E-3
21 E-4
20 E-5
15 C
14 C
11 U/R
6 D
5 D
4 SP-3
3 SP-2
2 SP-1
1 SP-1+
0 N/R
Table1.11Standard&Poor’sConversionCodes(continued)
SecurityNumberingSystems
Table1.12showsthesecuritynumberingcodes.Inthistable,ISINistheinternationalsecuritiesaccount
information.
Notes
l AddedCEDEL[Clearstream](CE),CommonCode(CEDEL/Euroclear)(XS),Spain(ES),andSweden(SE)
tothesecuritynumberingsystemcodes.
l Previously,LuxembourgandCEDEL(Clearstream)sharedthesamesecuritynumberingsystemcode
(LU).ThatcodeisnowusedexclusivelybyLuxembourgandCEDELhasthenewcode(CE).Thelengthof
thesecurityidentifieris07forLuxembourgand06forCEDEL.ThischangeshouldbenotedbecauseDTC
validatesthesecuritynumberingsystemcodeagainstthelengthofthesecurityidentifierstringentered.
Input/OutputInformation
1.Input/OutputInformationCodes 52

---

## Page 53

CodeandDescription SecurityLength
AT=Wertpapierkennummer(Austria) 06
AU=Australia 09
BE=SecretariatdesValeursMobilières-sum(Belgium) 08
BR=Brazil 09
CE=CEDEL(Clearstream) 06
CH=Valorennummer(Switzerland) 06
DE=Wertpapierkennummer(Germany) 06
DK=Fondskode(Denmark) 07
ES=Spain 08
EU=Euroclear 09
FR=SICOVAM(France) 06
GB=SEDOL(StockExchangeDailyOfficialList)(UnitedKingdom) 07
IE=Ireland 09
IS=ISIN 06
IT=CodiceUIC(Italy) 06
JP=QUICK(Japan) 09
LU=Luxembourg 07
MX=Mexico 09
NL=Netherlands 06
NO=Norway 06
RU=Reuters 12
SE=Sweden 06
US=[[CUSIP]](UnitedStates) 09
XS=CommonCode(CEDEL/Euroclear) 09
99=UserOriginated 12
Table1.12SecurityNumberingSystems
ExpandedSecurityTypes
Table1.13showsthesecuritytypesbytheiracronymsandmeanings.
Input/OutputInformation
1.Input/OutputInformationCodes 53

---

## Page 54

Acronym SecurityType Acronym SecurityType
[[ABS]] [[Asset]]-BackedSecurity GDS GovernmentDebtSecurities
[[ADR]] AmericanDepositoryReceipts GMR GinnieMaeREMICS
AGS Agencies GNM GinnieMae
BAS Banker'sAcceptances ITS IndexedTreasurySecurities
CDS CorporateDebtSecurities MBS Mortgage-BackedSecurities
CER RepresentativeCertificates MMI MoneyMarketInstruments
CMO CollateralizedMortgageObligation MSC Miscellaneous
COD CertificateofDeposit MTN MediumTermNotes
COL [[collateral]] MUN MunicipalBonds
CON ConvertibleBond NSD Non-U.S.SovereignDebt
CPA CommercialPaper OMB OtherMortgage-BackedSecurities
CPN Coupons OMM OtherMoneyMarketInstruments
CS1 U.S.CashWireNumber1 OPC OptionsContracts
CS2 U.S.CashWireNumber2 OPS OptionShares
CS3 U.S.CashWireNumber3 PRC PremiumContracts
CS4 U.S.CashWireNumber4 PRS PremiumShares
CS5 U.S.CashWireNumber5 RTE Rentes
CSH U.S.CashWire RTS Rights
DFI DTCOmnibus SHP Equities-PreferredShares
EBD Eurobonds SHS Equities([[shares]])
ECD EuroCD SLA StudentLoanMarketingAssociation
[[ECP]] EuroCP TBI TreasuryBills
ENT Euronotes TEM TaxExemptMoneyMarkets
FFI FixedIncomeOmnibus TRB TreasuryBonds
FIN FinancingTransaction TRN TreasuryNotes
FMR FreddieMacREMICS TRS TreasuryStrips
FNM FannieMae UNT Units
FNR FannieMaeREMICS WTS [[Warrants]]
FPA FaceorPrincipalorNominalAmount XCP TaxExemptCommercialPaper
FRM FreddieMac
Table1.13ExpandedSecurityTypes
Input/OutputInformation
1.Input/OutputInformationCodes 54

---

## Page 55

Table1.14showsparent/childrelationshipsoftheexpandedsecuritytypesusedformatchingpurposes.
ParentSecurityType ChildSecurityType
CDS(CorporateDebt) CDS(CorporateDebt)
CER(RepresentativeCertificates) CER(RepresentativeCertificates)
CON(ConvertibleBond) CON(ConvertibleBond)
COL([[collateral]]) COL([[collateral]])
CPN(Coupons) CPN(Coupons)
CSH(U.S.CashWire) CSH(U.S.CashWire)
CSH(U.S.CashWire) CS1(U.S.CashWireNumber1)
CSH(U.S.CashWire) CS2(U.S.CashWireNumber2)
CSH(U.S.CashWire) CS3(U.S.CashWireNumber3)
CSH(U.S.CashWire) CS4(U.S.CashWireNumber4)
CSH(U.S.CashWire) CS5(U.S.CashWireNumber5)
DFI(DTCOmnibus) DFI(DTCOmnibus)
EBD(Eurobonds) EBD(Eurobonds)
[[ECP]](EuroCP) [[ECP]](EuroCP)
ENT(Euronotes) ENT(Euronotes)
FFI(FixedIncomeOmnibus) FFI(FixedIncomeOmnibus)
FIN(FinancingTransaction) FIN(FinancingTransaction)
FPA(FaceorPrincipalorNominalAmount) FPA(FaceorPrincipalorNominalAmount)
GDS(GovernmentDebtSecurities) AGS(Agencies)
GDS(GovernmentDebtSecurities) GDS(GovernmentDebtSecurities)
GDS(GovernmentDebtSecurities) ITS(IndexedTreasurySecurities)
GDS(GovernmentDebtSecurities) SLA(StudentLoanMarketingAssociation)
GDS(GovernmentDebtSecurities) TBI(TreasuryBills)
GDS(GovernmentDebtSecurities) TRB(TreasuryBonds)
GDS(GovernmentDebtSecurities) TRN(TreasuryNotes)
GDS(GovernmentDebtSecurities) TRS(TreasuryStrips)
MBS(Mortgage-BackedSecurities) [[ABS]]([[Asset]]-BackedSecurities)
MBS(Mortgage-BackedSecurities) CMO(CollateralizedMortgageObligation)
MBS(Mortgage-BackedSecurities) FMR(FreddieMacREMICS)
MBS(Mortgage-BackedSecurities) FNM(FannieMae)
Table1.14ExpandedSecurityTypeParent/ChildRelationships
Input/OutputInformation
1.Input/OutputInformationCodes 55

---

## Page 56

ParentSecurityType ChildSecurityType
MBS(Mortgage-BackedSecurities) FNR(FannieMaeREMICS)
MBS(Mortgage-BackedSecurities) FRM(FreddieMac)
MBS(Mortgage-BackedSecurities) GMR(GinnieMaeREMICS)
MBS(Mortgage-BackedSecurities) GNM(GinnieMae)
MBS(Mortgage-BackedSecurities) MBS(Mortgage-BackedSecurities)
MBS(Mortgage-BackedSecurities) OMB(OtherMortgage-BackedSecurities)
MMI(MoneyMarketInstruments) BAS(Banker’sAcceptances)
MMI(MoneyMarketInstruments) COD(CertificateofDeposit)
MMI(MoneyMarketInstruments) CPA(CommercialPaper)
MMI(MoneyMarketInstruments) ECD(EuroCD)
MMI(MoneyMarketInstruments) MMI(MoneyMarketInstruments)
MMI(MoneyMarketInstruments) MTN(MediumTermNotes)
MMI(MoneyMarketInstruments) OMM(OtherMoneyMarketInstruments)
MSC(Miscellaneous) MSC(Miscellaneous)
MUN(MunicipalBonds) MUN(MunicipalBonds)
NSD(Non-U.S.SovereignDebt) NSD(Non-U.S.SovereignDebt)
OPC(OptionContracts) OPC(OptionContracts)
OPS(OptionShares) OPS(OptionShares)
PRC(PremiumContracts) PRC(PremiumContracts)
PRS(PremiumShares) PRS(PremiumShares)
RTE(Rentes) RTE(Rentes)
RTS(Rights) RTS(Rights)
SHS(Equities[[[shares]]]) [[ADR]](AmericanDepositoryReceipts)
SHS(Equities[[[shares]]]) SHP(Equities-PreferredShares)
SHS(Equities[[[shares]]]) SHS(Equities[[[shares]]])
SHS(Equities[[[shares]]]) WTS([[Warrants]])
TEM(Tax-ExemptMoneyMarkets) TEM(Tax-ExemptMoneyMarkets)
TEM(Tax-ExemptMoneyMarkets) XCP(Tax-ExemptCommercialPaper)
UNT(Units) UNT(Units)
Table1.14ExpandedSecurityTypeParent/ChildRelationships(continued)
TransactionTypes
Table1.15showsthetransactiontypes.
Input/OutputInformation
1.Input/OutputInformationCodes 56

---

## Page 57

Transactionname(num-
ber)
Description
NewConfirm(1) [[Broker]]/dealerconfirmnumbercannotbethesameasanactivetradeorcancellation.
Cancelation(3) Cancellationsrequire:
l Executingbroker/dealernumber
l [[Broker]]/dealerconfirmnumber(identifyingthecancellation)
l Originalbrokerconfirmnumber(identifyingtheconfirmtobecanceled)
l Cancellationreasoncode
TheTradeSuiteIDserviceignoresallotherfieldswithintheinputrecord.TheBroker/DealerConfirmNumber
field,whichidentifiesthecancellation(seePositions347–358),candifferfromtheBroker/DealerConfirm
Numberontheconfirmtobecanceled.EnsuretheOriginalBrokerConfirmNumberfield(seePositions209–
220)isthesameasintheexistingconfirmtobecanceled.Unlesstheoriginalconfirmationismatchedor
affirmed,thecancellationconfirmdeactivatestheoriginalconfirm.
Iftheconfirmtobecanceledismatchedoraffirmed,acancellationisgeneratedandtheCancellationAfter
Acknowledgmentfield(ontheOutputRecord)issettoY.Thiscancellationisonlyforinformativepurposes,
astheexistingmatchedoraffirmedconfirmremainsactiveandcansettle.
Resubmission(4) Thisactionwasnotimplemented.
Table1.15TransactionTypes
Input/OutputInformation
1.Input/OutputInformationCodes 57

---

## Page 58

InteractiveFields
Table1.16showstheinteractiveprocessingfieldsthatarenotsupportedbyoldend-of-dayformats.
Recordtype Fields
RecordType1 SplitCurrencyIndicator
QCExemptionIndicator
SettlementLocation
SecurityNumberingSystem
AlternateCurrencyConversionRate
AlternateCurrencyISOCode
AlternateCurrencyNetAmount
OriginalBrokerConfirmNumber
ConfirmProcessTime
DesignatedAffirmingPartyNumber
DesignatedAffirmingPartyType
ConfirmProcessDate
AdditionalParty#1Type
AdditionalParty#2Type
InstitutionContact
ALERTAccountFoundIndicator
CancelationAfterAcknowledgment
MatchedIndicator
MatchingVariance
VarianceDirection
Amortized/AccretedFactor
AdditionalParty#3Type
AdditionalParty#3Number
AdditionalParty#3Account
AdditionalParty#3Line1
AdditionalParty#3Line2
Table1.16InteractiveFields
Input/OutputInformation
1.Input/OutputInformationCodes 58

---

## Page 59

Recordtype Fields
RecordType2 SubjecttoFederalTax
AlternateMinimumTax
AdditionalParty#3Name
OriginalInputSecurityNumberingSystem
OriginalInputSecurityIdentifier
[[CUSIP]]/CANSSecurityNumberingSystem
[[CUSIP]]/CANSSecurityIdentifier
Table1.16InteractiveFields(continued)
Input/OutputInformation
1.Input/OutputInformationCodes 59

---

## Page 60

2.PROCESSINGPROCEDURES
Thissectionexplainstheprocessingproceduresandtradeinputcodes.Processingproceduresdependon
whethertheComputer-to-ComputerFacility([[CCF]])orMessageQuerying(MQ)isinuse.
Computer-to-ComputerFacility([[CCF]])
Computer-to-ComputerFacility([[CCF]])processingisdoneintwostages:
1. Thesign-onisvalidatedwiththedataenteredtoensurethatthesubmittercanenterdatafortherecordsbeing
processedandthereceiptofthedataiswithintheappropriatetimeframe.Thiseditingisdonewhiletheuseris
ontheline.ThesubmitterreceivestheinputrecordreturnedwiththeFeedbackIndicatorsetto“?”andablock
(Table2.1below)indicatingspecificsappendedtotheendoftherecord.
2. ThesecondstageofCCFprocessingoccurswhentheusercompletesthetransmission.Thistypeofediting
consistsoffieldvalidation.Iferrorsarefoundatthispointinprocessing,amessageprefix(Table2.2onthe
nextpage)isappendedtothefrontoftherecordandtheblockisappendedtotheendoftherecord.The
recordisloggedtotheuser’smailboxforoutputreceipt.
BlockSpecification
Table2.1showstheblockspecification.
Position Length Format FieldnameFielddescription
1 8 Character Code1 Identifiesthefieldandthereasonwhythefieldiserroneous.Ineachcode,
l Firstfourcharactersidentifythefield.
l Nextfourcharactersidentifythereasonwhythefieldis
erroneous
Forcodevalues,seeTable2.3onpage 62.
9 8 Character Code2
17 8 Character Code3
25 8 Character Code4
33 8 Character Code5
Table2.1BlockSpecification
Input/OutputInformation
2.ProcessingProcedures 60

---

## Page 61

MessagePrefixSpecification
Table2.2showsthemessageprefixspecificationappendedtothefrontoftherecordforCCF.
Position Length Format Fieldname Validate Description
1 1 Character Filler - Reserved.Donotuse.
1 1 Character MessageFlag - O=currentdaymessage
R=currentdayreprint
U=currentdaymessagerequestedoutofsequence
Y=priordaymessage.
3 1 Character Filler - Reserved.Donotuse.
4 10 Character DestinationID - Identifierofmessagequeuethemessagewasreceivedfrom(=8-
characterusersign-onplus2-characterdestination).
14 1 Character Filler - (Constantvalue).
15 6 Numeric Message
SequenceNum-
ber
- UniquemessagesequencenumberassignedbyDTC’sMessage
DeliverySystemforeachDestinationID(seePosition4).
Table2.2MessagePrefixSpecification
Formoreinformation,seetheInterfaceControlManager.
MessageQuerying(MQ)
ForMessageQuerying(MQ),theprocesseshappenwhiletheuserisontheline.Therefore,onlytheblockis
returned.Forafulldescriptionoftheblockandmessageprefix,seetheInterfaceControlManager.
TradeSuiteID®ErrorCodes
Thecombinationofthefieldcodeandreasoncodeformulatesthecode.Tradeinputsthatcontainoneormoreof
theseerrorsarereturnedtothesubmitterinthesamemedia.Noconfirmationisproduced.
Table2.3showsthetradeinputcodesalphabeticallybyfieldcodeandthenbyreasoncode.
Input/OutputInformation
2.ProcessingProcedures 61

---

## Page 62

FieldcodeReasonCode Descriptions
AAAA 9AAA TransactionPrefix
Transactionheaderisnotequaltooneoftheacceptablevalues.
9AAE Informationinthetransactionheaderisinvalid.
9AAN TransactionheadertypeisineligibleforIDprocessing.
AAAB 9AAE TransactionType
Transactiontypedoesnotequal:
1=New
3=Cancellation
4=Resubmission
IABG Recordtypeindicatedinthetransactionheaderisinvalid.
AAAI 9AAE Production/TestIndicator
Headerforproduction/testindicatorisnotequaltoanacceptablevalues.
9ABC Production/testindicatorisinvalidormissing.
IAA3 Production/testindicatorisnotequaltooneoftheacceptablevalues.
AAAJ 9AAE HeaderRecordSuffix
Headersuffixisinvalid.
IAB6 Recordsuffixisnotequaltooneoftheacceptablevalues.
AAAK 9AAE VersionNumber
Versionnumberisnotequaltooneoftheacceptablevalues.
IAB6 Invalidversionnumberforstep-outprocessing.
IABG Headerversionnumberisinvalid.
AZZZ 9AA6 TransactionRecord
Transactionrecordisaduplicate.
9AAA Transactiondatarecordisinvalid.
9AAE Cancellationrecordcontainedinvaliddata.
9AAI Datarecordisinaninvalidformat.
9ZZZ Relatedrecordinerror.
IADY Securitytyperequiresrecord4.
IAET REPOfieldsmissing.
Table2.3TradeSuiteIDErrorCodes
Input/OutputInformation
2.ProcessingProcedures 62

---

## Page 63

FieldcodeReasonCode Descriptions
BAAA 9AAF SettlementDate
Settlementdateisnotnumeric.
9AAJ Settlementdateis:
l Notwithintwoyearsofthecurrentdate.
l InvalidsettlementdateforDTC.
l Invalidcalendardate.
l Equaltozero.
9AAK Settlementdateisbeforethetradedate.
9ADI Settlementdateisafterthecutoff.
BAAB 9AAJ TradeDate
Tradedateis:
l Notnumeric
l Lessthanzero
l Invalidcalendardate
IAAF TradedateisgreaterthanthecurrentdateforsettlementintheUS.
IAAG Tradedateexceedsthecurrentdate,U.S.EasternTime,bymorethanoneday.
IAAH Tradedateislessthanthecurrentdateminus250settlementdays.
BAAI IAEK MaturityDate
Maturitydateisinvalid.
BABM 9AAA FactorEffectiveDate
Factoreffectivedateisaninvaliddayoftheyear.
BABN 9AAA IssueDate
Issuedateisaninvaliddayoftheyear.
BABO 9AAA DeliveryDate
Deliverydateisaninvaliddayoftheyear.
BABP 9AAA OptionExpirationDate
Optionexpirationdateisaninvaliddayoftheyear.
BABQ 9AAA RecordDate
Recorddateisaninvaliddayoftheyear.
Table2.3TradeSuiteIDErrorCodes(continued)
Input/OutputInformation
2.ProcessingProcedures 63

---

## Page 64

FieldcodeReasonCode Descriptions
CAA1 9AAA [[Broker]]-ExecutingBrokerIdentifier
Invalidexecutingbroker,brokerID,orbusinessidentifiercode(BIC).
9AAF [[Broker]],executingbrokerIDnotnumeric.
9AAN [[Broker]]/ExecutingBrokernotIDeligible.
IAA4 Rejectionnotsentbytheexecutingbroker.
IAAE Brokerinvalidforacknowledgment.
IABI Commonallocationrejectionwithdetailmatch.
CAA2 9AAN ClearingBrokerIdentifier
ClearingbrokerisineligibleforIDprocessing.
IAAE Clearingbrokerinvalidforacknowledgment.
CAA3 9AAA Step-inBroker/DealerIdentifier
IDstep-inbrokerBICisinvalid.
9AAF IDstep-inbrokernotnumeric.
9AAN Step-inbrokerisanineligibleID.
IAAE Step-inbrokerinvalidforacknowledgment.
CAA5 IAAE Custodian/AgentIdentifier
Custodianbanknotturnedonforhuboutput.
IAEV Custodian/agentnotahubuser.
CAA6 IAEO Custodian/agentidentifiercustomerbankisspaces.
Table2.3TradeSuiteIDErrorCodes(continued)
Input/OutputInformation
2.ProcessingProcedures 64

---

## Page 65

FieldcodeReasonCode Descriptions
CAAA 9AAA InstitutionIdentifier
InstitutionBICnumberisinvalid.
9AAE Institutionnumberdoesnotequalthesubmittinginstitution.
9AAF Institutionnumberisnotnumeric.
9AAN InstitutionisinvalidorineligibleforIDprocessing.
9ABB InstitutionnumberwasnotfoundintheDTCdatabase.
9ABG Institutionupdatesarenotpermitted.
9ABM Institutionisnotpermittedtosubmitthismessagetype.
IAAE Institutionelectednottoreceiveoutput.
IAAL Nomatchcouldbemadetotheinstitution,theaccountnumberismissingor
accountnotfoundontheALERT®platform.
IAAW Notdestinedformatchinganddidnotelecttonotifythebrokerorbranch.
IABE [[Institutions]]/Bnoteligible.
IABJ Attemptrejectedaftermatchingisnotallowed
IAER InstitutionIDisunauthorizedfortheaccountnumber.
CAAB 9AAF ExecutingBroker/DealerIdentifier
Branchorexecutingbroker/dealeridentifiernumberisnotnumeric.
9AAN Executingbroker/dealerisineligibleforIDprocessing.
9ABB Executingbroker/dealernumbernotfoundintheDTCdatabase.
9ABM Brokerisaninvalidsubmitterforthismessagetype.
9BA4 Executingbroker/dealernotsetupforInteroperability
IAA4 Brokerisnotpermittedtorejectthismessagetype.
IAAE Branchorbrokerelectednottoreceivetheoutput.
IABE BrokerisineligibleforIDprocessing.
IABI Rejectionduetoatleastonedetailrecordhasalreadymatched.
CAAC 9AAN AffirmingpartyIdentifier
AffirmingpartyisineligibleforIDprocessing.
IAAB Affirmingpartynumberisinvalid.
IAAC Affirmingpartyisnotonthetrademessage.
IAAD Affirmingpartyisnotaninstitution,agent,orcustomer.
IDEJ Invalidreverseaffirmingparty.
Table2.3TradeSuiteIDErrorCodes(continued)
Input/OutputInformation
2.ProcessingProcedures 65

---

## Page 66

FieldcodeReasonCode Descriptions
CAAE 9AAN [[Broker]]/dealersub-custodianidentifier
[[Broker]]/dealersub-custodianisineligibleforIDprocessing.Otherwise,ifnot
provided,enterspacesorzeros.
CAAF 9AAN Step-inBroker/DealerIdentifier
IDstep-inbroker/dealerisineligibleforIDprocessing.
IAAE Step-inbrokeranditsclearingbrokerelectednottoreceiveInstitutionalInstruc-
tions(IIs),andthenotifyindicatorisequaltoY.
CAAG 9AAN AgentSub-Custodian
Agentsub-custodianisineligibleforIDprocessing.Otherwise,ifnotprovided,
enterspacesorzeros.
9BA4 ClearagentnotsetupforInteroperability
CAAH 9AA5 AgentIdentifier
IDagentnumberisinvalidorblank.
9AAF IDagentnumberisnotnumeric.
9AAN AgentnumberisineligibleforIDprocessing.
9ABB AgentnumberwasnotfoundintheDTCdatabase.
9ABG Agentupdatenotallowed.
9ABM Agentinvalidsubmitterforthismessagetype.
9ADF Agentisprimebroker.
9BA4 AgentnotsetupforInteroperability
IABE AgentS/Bineligible.
CAAI 9AAN InterestedParty#1Identifier
Interestedparty#1isineligibleforIDprocessing.Otherwise,ifnotprovided,enter
spacesorzeros.
9ABB InterestedpartyIDnumberwasnotfoundintheDTCdatabase.
9ABG Interestedparty#1updatenotallowed.
9ABM Interestedparty#1notpermittedtosubmitthismessagetype.
9BA4 Interestedpart1notsetupforInteroperability
IABE InterestedpartyS/Bineligible.
CAAJ 9AAN IssuingAgentIdentifier
IssuingagentnumberisineligibleforIDprocessing.
9ABB IssuingagentnumberwasnotfoundintheDTCdatabase.
IABE IssuingagentS/Bineligible.
Table2.3TradeSuiteIDErrorCodes(continued)
Input/OutputInformation
2.ProcessingProcedures 66

---

## Page 67

FieldcodeReasonCode Descriptions
CAAN 9AA6 IDBrokerofCreditIdentifier
DuplicateIDbrokerofcredit.
9AAA IDbrokerofthecreditidentifierorBICisinvalid.
9AAF IDbrokerofcreditidentifiernumberisnotnumeric.
9AAN IDbrokerofthecreditidentifiernumberisineligibleforIDprocessing.
CAAO 9AAN InterestedParty#2Identifier
Interestedparty#2isineligibleforIDprocessingorisinvalid.Otherwise,ifnot
provided,enterspacesorzeros.
9ABG Interestedparty#2identifierupdatenotallowed.
9BA4 Interestedparty2notsetupforInteroperability
CAAP 9AAN InterestedParty#3Identifier
Interestedparty#3isineligibleforIDprocessingorisinvalid.Otherwise,ifnot
provided,enterspacesorzeros.
9ABG Interestedparty#3identifierupdatenotallowed.
9BA4 Interestedparty3notsetupforInteroperability
CAAQ 9AAA SubmittingInstitution
SubmittinginstitutionBICorIDisinvalid.
9AAN SubmittinginstitutionisineligibleforIDprocessing.
IAAE SubmittinginstitutionelectednottoreceivetheIIrejection.
IACF Commonrecordnotfound.
IAER SubmittinginstitutionIDnotauthorizedforACRNM.
IAEV InstitutionnotaHubuser
CAAR 9AAA BranchOfficeIdentifier
BranchIDnumberisinvalid.
9ABB Branchandbrokerunrelated.
CAAS 9AAE Non-IDStep-inBroker
WhenspecifyingtheIDstep-inbroker,enterspacesforthenon-IDstep-inbroker.
CAAU 9AA5 IDAgentInternalAccountNumber
IDagentinternalaccountnumberwasnotentered.
Table2.3TradeSuiteIDErrorCodes(continued)
Input/OutputInformation
2.ProcessingProcedures 67

---

## Page 68

FieldcodeReasonCode Descriptions
CAAY 9AAN ClearingBrokerIdentifier
ClearingbrokerisineligibleforIDprocessing.
9BA4 ClearingbrokernotsetupforInteroperability
IABH Clearingbrokerisinactive.
IAAE ClearingbrokerelectednottoreceiveIIs.
CABB 9AAN CustomerIdentifier
CustomeridentifierisineligibleforIDprocessing.Otherwise,ifnotprovided,
enterspacesorzeros.
9ABG Customeridentifierisnotallowed.
9ABM Customeridentifierisaninvalidsubmitter.
CABC 9ANN SubmitterIdentifier
Submitterisnotpartytothetrade.
IAAB Submitterisnotanaffirmingagent.
CACE 9AAA AdditionalParty#4
Additionalparty#4isinvalidforadomesticsettlementlocation([[DTC]],BRC,FED,
U.S.).
9AAN Additionalpartynumber4isineligibleforIDprocessing.Otherwise,ifnot
provided,enterspacesorzeros.
CACF 9AAA AdditionalParty#5
Additionalparty#5isinvalidforadomesticsettlementlocation([[DTC]],BRC,FED,
U.S.).
9AAN Additionalpartynumber5isineligibleforIDprocessing.Otherwise,ifnot
provided,enterspacesorzeros.
CACG 9AAA GenericTBA
GenericTBA(TradeType=01)containedapoolnumber.
9ABD SpecifiedPoolTrade(TradeType=11)oraGenericPoolTrade(TradeType=
12)wasmissingasecuritynumberorapoolnumber.
CAGJ 9AA5 DetailReferenceIdentifier
Detailreferenceidentifiercontainsspaces.
IAAN Detailreferenceidentifierinthedetailallocationrecordwithinthesetof
allocationsisaduplicateandnotunique.
Table2.3TradeSuiteIDErrorCodes(continued)
Input/OutputInformation
2.ProcessingProcedures 68

---

## Page 69

FieldcodeReasonCode Descriptions
DAA3 9AAF TotalAllocationShares/FaceValue
Totalallocationshares/facevalueisnotnumeric.
9AAH Forregulartrades,thetotalshares/facevaluemustbegreaterthanzero.
9AAI Totalsharesinaninvalidformat.
IAA2 Commonallocationunequaltothedetailallocation.
IABB Totalshares/facevalueunequaltooriginal.
DAA4 9AAF ExecutingBrokerFee
Executingbrokerfeeisnotnumeric.
DAA5 9AAF CommissionEquivalent
CommissionEquivalentisnotnumeric.
DAA7 9AAF Commission
Commissionisnotnumeric.
DAA8 9AAF AllocatedShares/FaceValueforThisTransaction
Allocatedshares/facevalueforthistransactionisnotnumeric.
9AAH Allocatedshares/facevalueforthistransactionisequaltozero.
IAA5 Allocatedshares/facevalueforthistransactionisinvalid.
DAA9 9AAF ResearchAmount
Researchamountisnotnumeric.
9AAI Researchamountinvalidformat
DAAA 9AAF [[shares]]/FaceValue
QuantityofsecuritiesfacevalueisnotnumericintheDTCsettlementsystems
andonlyappliestoinputwithaDTCsettlementlocation.
9AAH Quantityofsecuritiesfacevalueisgreaterthanzero.
IAAI [[shares]]/facevaluecontainsfractionalshares.Thisappliesonlytotheinputwith
DTCsettlementlocation.
IAAJ [[shares]]/facevalueinthebroker/dealertradeinputforDTCisgreaterthan
999,999,999.ThisisthemaximumvalueacceptableforprocessingintheDTC
settlementsystemsandonlyappliestoinputwithaDTCsettlementlocation.
DAAD 9AAF Price
Priceisnotnumeric.
9AAH Priceisgreaterthanzeroforregulartrades.
Table2.3TradeSuiteIDErrorCodes(continued)
Input/OutputInformation
2.ProcessingProcedures 69

---

## Page 70

FieldcodeReasonCode Descriptions
DAAE 9AAF NetAmount
Netamount(proceeds)isnotnumeric.
9AAH Netamount(proceeds)aregreaterthanzeroforregulartrades.
9AAI Invalidformatforthenetamount.
IAAK Amount(proceeds)onthebroker/dealertradeinputforDTCisgreaterthan
$999,999,999.99.
ThesearethemaximumvaluesacceptableforprocessingintheDTCsettlement
systemsandonlyapplytotheinputwithaDTCorBRCsettlementlocation.
DAAF 9AAF PrincipalAmount
Principalamountisnotnumeric.
9AAH Principalisgreaterthanzeroforregulartrades.
9AAI Invalidprincipalformat.
DAAH 9AAF OtherCharges
Otherchargesarenotnumeric.
9AAI Invalidformatforothercharges.
DAAI 9AAF Interest
Interestisnotnumeric.
9AAI Interestinvalidformat
DAAJ 9AAE Commission
Commissionisgreaterthan100percent.
9AAF Commissionisnotnumeric.
9AAI Invalidcommissionformat.
DAAK 9AAF NetPrice
Netpriceisnotnumeric.
DAAL 9AAF Registration/Shipping
Registration/shippingorfeesarenotnumeric.Spacesareonlyacceptablefor
non-numericvalue.
9AAI Feesinvalidformat
DAAM 9AAF AlternateNetAmount
Alternatenetamountisnotnumeric.
Table2.3TradeSuiteIDErrorCodes(continued)
Input/OutputInformation
2.ProcessingProcedures 70

---

## Page 71

FieldcodeReasonCode Descriptions
DAAO 9AAF Country/FederalTax
Countryorfederaltaxisnotnumeric.
9AAI Invalidformatforthecountryorfederaltax.
DAAP 9AAE ActualPrice
BothactualandnetpricearezerosforRegularWaytrades.
9AAF Actualpriceisnotnumeric.
9AAH ActualpriceisgreaterthanzeroforRegularWaytrades.
9AAI Actualpriceinvalidformat
DAAQ 9AAF AveragePrice
Averagepriceisnotnumeric.
9AAH Averagepriceisgreaterthanzero.
DABE 9AAF CurrentFaceValue
Currentfacevalueisnotnumeric.
DABG 9AAF GoodDeliveryMillions
Gooddeliverymillionsvalueisnotnumeric.
DABH 9AAF NumberofDaysAccruedInterest
Numberofdaysaccruedinterestisnotnumeric.
DABI 9AAF NumberofPools
Numberofpoolsvalueisnotnumeric.
DAGB 9AAF OriginalTradePar
Originaltradeparisnotnumeric.
EAA6 9AAE Step-inBrokerNotifyIndicator
Step-inbrokernotifyindicatornotequaltoY/N.
EAAA 9AAE Buy/SellIndicator
Buy/sellindicatorisnotequaltooneoftheacceptablevalues
EAAB 9AAE BrokerNotifyIndicator
Brokernotifyindicatorvalueisnotequaltooneofthevalues.
IAAW Nomatchandnodistribution.
EAAC 9AAE SplitCurrencySettlementIndicator
Splitcurrencysettlementindicatormustequaloneofthefollowingvalidvalues:
l Y=Yes
l N=No
Table2.3TradeSuiteIDErrorCodes(continued)
Input/OutputInformation
2.ProcessingProcedures 71

---

## Page 72

FieldcodeReasonCode Descriptions
EAE5 9AAA TradeType
Tradetypemustequaloneofthefollowingvalidvalues:
l 01=GenericTBA
l 02=SpecifiedTBA
l 03=SpecifiedPoolTBA
l 11=SpecifiedPool
l 12=GenericPool
l 50=OtherMortgage-backedsecurity
9ABD Tradetypeindicatormissingoninput.
IAEF SpecifiedTBA(TradeType=02)didnotcontainanyspecifications.Aspecified
TBAmustcontainatleastonespecification.
IAEH SpecifiedPooltrade(TradeType=11)didnotcontainanyspecifications;a
specifiedpooltrademustcontainatleastonespecification.
EAEB 9AAA Long/ShortIndicator
Indicatormustequaloneofthefollowingvalidvalues:
l L=SellLong
l S=SellShort
l E=SellShortExempt
l Space=NotAvailableorApplicable
FAAA 9AAF ConversionRate
Conversionrateisnotnumeric.
FAAB 9AAF Amortized/AccretedFactor
Amortized/accretedfactorisnotnumeric.
GAAA 9ABB CUSIPNumber
CannotfindCUSIPnumber.
IOFC SecurityOFACblock
GAAB 9AAA [[Broker]]/DealerConfirmNumber
Invalidbroker/dealerconfirmnumber.
IAAO [[Broker]]/dealerconfirmnumbernotuniquefornewandresubmittedconfirmations
(Transactiontype=1and4).
Table2.3TradeSuiteIDErrorCodes(continued)
Input/OutputInformation
2.ProcessingProcedures 72

---

## Page 73

FieldcodeReasonCode Descriptions
GAAC 9AAE Role
Rolemustequaloneofthefollowingvalidvalues:
l 1=Executingbroker/dealeractsasagentforcustomer(AGNT).
l 2=Executingbroker/dealeractsasprincipalfortheirownaccount(PRIN).
l 3=Executingbroker/dealeractsasagentforapersonotherthanthecus-
tomer(OTHR).
l 4=Executingbroker/dealeractsasagentforboththecustomerand
anotherperson(CUST).
l 5=Averagepricetrade;thebroker/dealeractsasprincipalforsomeexe-
cutionsandagentforothersinthetransaction(AVGR).
l 6=Executingbroker/dealeractsasbothprincipalandagentinthetrans-
action(PRAG).
l 7=Executingbroker/dealeractsasprincipal,agent,andagentforanother
personinthetransaction(PAGC).
l 8=Crossingasagent-Executingbroker/dealeriscrossingtransactionas
agentonbehalfofthecustomer(CAGN).
l 9=Crossingasprincipal-Executingbroker/dealeriscrossingtransaction
asprincipalforhisownaccount(CPRN).
l A=Actingasrisklessprincipal-Partyistradingasarisklessprincipal.That
is,theordertobuy(sell)hasbeencontemporaneouslyoffsetbyanorderto
sell(buy)withanotherparty(RISP).
GAAD 9AAE SettlementTypeCode
Settlementtypecodemustequaloneofthefollowingvalidvalues:
l 1=RegularWay
l 2=When-Issued
l 3=When-Distributed
l 4=When-IssuedorWhen-Distributed
Table2.3TradeSuiteIDErrorCodes(continued)
Input/OutputInformation
2.ProcessingProcedures 73

---

## Page 74

FieldcodeReasonCode Descriptions
GAAE 9AA5 SecurityType
Securitytypeisblankwhenintendedformatchingandthesecurityisineligibleat
[[DTC]].
9AAA Tradecontainedmortgage-backedsecurityinformation,butthesecuritytypeis
anunacceptablevalue.Thesecuritytypemustequaloneofthefollowingvalid
values:
l [[ABS]]=AssetBackedSecurities
l CMO=CollateralizedMortgageObligation
l FMR=FreddieMacREMICS
l FNM=FannieMae
l FNR=FannieMaeREMICS
l FRM=FreddieMAC
l MBS=Mortgage-BackedSecurities
l GMR=GinnieMaeREMICS
l GNM=GinnieMae
l OMB=OtherMortgage-BackedSecurities
9AAE Securitytypeisnotequaltooneoftheacceptablevalues.
9ABE Securitytypeisrequired.
IAEZ FINorCOLsecuritytyperequiresrecord5and6.
Table2.3TradeSuiteIDErrorCodes(continued)
Input/OutputInformation
2.ProcessingProcedures 74

---

## Page 75

FieldcodeReasonCode Descriptions
GAAF 9AA5 Securityidentifiedisblank(spaces)whenintendedformatching.
9AAO ISIN
l ISOcountrycodeisinvalid.
l Internationalcheck-digitisinvalid.
l IfthesettlementlocationisDTC,thecountrycodeisUS.Ifthecountry
codeisUS,useavalidCUSIPcheck-digit.
l IfthecountrycodeisGB,thefirsttwopositionsafterthecountrycodeis
zeroandtheSEDOLcheck-digitisvalid.
9AAP [[CUSIP]]
l ISOcountrycodeisnotblank.
l Internationalcheck-digitisnotblank.CUSIPcheck-digitisinvalid.
9AAQ SEDOL
l ISOcountrycodeisnotblank.
l Internationalcheck-digitisnotblank.
l Firsttwodigitsofthesecuritynumberarenotzeros.
l SEDOLcheck-digitisinvalid.
9ABE Securitynumberwasnotentered.
IAA6 Enteroneofthefollowingthreefieldsthatidentifythesecurity:
l Securityidentifier
l Tickersymbol
l Securitydescription
GAAG 9AAA CancellationReasonCode
Invalidcancellationreasoncode.
9AAE Cancellationreasoncodeisnotequaltooneoftheacceptablevalues.Formore
information,seeCancellationReasonCodes
9AAI Invalidreasonformat.
9ABS Enteredmorethanonecancellationreasoncode.
GAAH 9AA6 CorrectionReasonCode
Correctionreasoncodesrepeated-duplicatetransaction.
9AAE Correctionreasoncodeinvaliddatatype.
Table2.3TradeSuiteIDErrorCodes(continued)
Input/OutputInformation
2.ProcessingProcedures 75

---

## Page 76

FieldcodeReasonCode Descriptions
GAAI 9AAE CurrencyCode
Currencycodeisnotequaltooneoftheacceptablevalues.
IAAP CurrencycodeisnotequaltoUSD.
Note:ThiscurrencycoderestrictionappliesonlytoinputwithaDTCsettlement
location.
GAAJ 9AAA DTCControlNumber
InvalidDTCcontrolnumber.
9ABB DTCcontrolnumbernotfoundintheDTCdatabase.
IAAS Tradealreadyreversed.
IAAT Tradealreadycanceled.
IAAU Tradealreadyaffirmed
IAAV Tradecannotbeaffirmedbecauseofaffirmationreversal,primebroker
disaffirmation,oranadministrativecancellation.Submitanewtrade.
IAAZ Tradenotfound.AtleastoneDTC/IDcontrolnumber,executingbroker/dealer,or
[[Broker]]/dealerconfirmnumberforacancellation,correction,oraffirmationdoes
notmatchanexistingtrade.
IAEI Reverseaffirmationwassubmittedonatradethatisnotaffirmed.
GAAK 9ABD AdviceofCancellationorCorrection(AOCC)
Correctionrecipientismissing.
GAAL 9ABD Cancellationrecipientmissing.
GAAM 9AAE MarketCode
Marketcodeisnotequaltooneoftheacceptablevalues.Formoreinformation,
seeMarketCodesandAbbreviations.
9AAI Marketcodeformatinvalid.
GAAN 9AAE AccountType
Accounttypemustequaloneofthefollowingvalidvalues:
l 02=Cash
l 05=Short
l 09=[[Margin]]
l 99=Other
GAAP 9AAE SecurityNumberingSystem
Securitynumberingsystemcodeisnotequaltooneoftheacceptablevalues.
Showninmessagesasfielddescription.
Table2.3TradeSuiteIDErrorCodes(continued)
Input/OutputInformation
2.ProcessingProcedures 76

---

## Page 77

FieldcodeReasonCode Descriptions
GAAR 9AAE AlternateCurrencyCode
Alternatecurrencycodeisnotequaltooneoftheacceptablevalues.Formore
information,seeISOCountryCodes
IAAQ To/Fromcurrenciesareprovidedandthealternaterateornetamountare
missing.
AlternateCurrencyfieldisblank.
GAAS 9AAA SettlementLocation
Settlementlocationisinvalid.
9AAE Settlementlocationisnotequaltooneoftheacceptablevalues.
9ABB Settlementlocationwasnotfound.
IAAR TradedesignatedforDTCsettlementbutcontainedsub-[[Custodians]],depositories
(otherthanDTC)accountsorbranchIDnumbers(USphysicalsettlements).
IOFC SettlementlocationOFACblocked
GAAT IAA1 InstitutionBlockReferenceNumber
Institutionblockreferencenumberwasalreadycanceled.
IAA3 Institutionblockreferencenumberisinvalid.
IAA4 Institutionblockreferencenumberisnotequaltooriginalallocation.
IAAN Institutionreferencenumberisnotunique.
IABD Institutionblockreferencewasalreadyrejected.
GAAV 9AAE [[Broker]]/DealerReferenceNumber
Branchorexecutingbrokerreferencenumberhasspaces.
IAA1 Noticeofexecutionorinstitutionblockreferencenumberwasalreadycanceled.
IAA4 DTCcouldnotmatchtheoriginalbrokerreferencenumberforarejectora
cancel.
IAAN Brokerreferencenumbernotunique.
IABD Noticeofexecutionwasalreadyrejected.
GAAW 9AAA OriginalBroker/DealerReferenceNumber
Originalbroker/dealerreferencenumberisinvalid.
IAA1 Tradeisalreadymarkedasacancellation.
IAAZ Tradenotfound.Executingbrokerandoriginalbrokerconfirmnumberfora
cancellationdoesnotmatchanexistingtrade.
Table2.3TradeSuiteIDErrorCodes(continued)
Input/OutputInformation
2.ProcessingProcedures 77

---

## Page 78

FieldcodeReasonCode Descriptions
GABI 9AAE RejectReasonCode
Rejectreasoncodeisinvalid.
GABL 9AAA AllocationCommissionTypeIndicator
AllocationcommissiontypeindicatorisequaltoUnknown.Brokercommission
feeandbrokerofcreditcommissionfeesaregreaterthanzero.
9AAE Allocationcommissiontypeinvalid.
GABN 9AAE TransactionType
IImessagetypenotequaltoAllocation(institutioninput),CommonCancellation
(institutioninput),Substitution(institutioninput),orCommonRejection([[Broker]]
input).
IABH MQvalidonlyforrejection.
IABK TransactiontypeinvalidforMQ.
IACG Onlytransaction1or4canbesubmittedwithatrailer.
GABO 9AAE DataType
Datatypeisinvalid.
9ABR Step-outrecordsubmittedwithcommonrecord?
IAA7 Detailrecordsubmittedwithoutacorrespondingcommonrecord.
IAA8 Nodetailrecordtype.
IABC Detailrecordsaresubmittedforcancellationsorrejections;transactiontype3or
5.
IABG Step-outpartmissingininputwhencancelingastepped-outdetailorstep-out
partfoundininputwhencancelinganallocationwhichisnotsteppedout.
IACH Traileralreadyexists.
GABP 9AAE SubstitutionIndicator
Messagetypemustequaloneofthefollowingvalidvalues:
l O–Original
l C–Cancellation
l S–Substitution
l R–Replacement
9AEH Canceledforincompleteallocation.
IAA9 SubstitutionindicatornotequaltoOfortransactiontype1(Allocation).
IABA SubstitutionindicatorisnotequaltoCorSfortransactiontype4(Substitution).
Table2.3TradeSuiteIDErrorCodes(continued)
Input/OutputInformation
2.ProcessingProcedures 78

---

## Page 79

FieldcodeReasonCode Descriptions
GABQ 9AAE InstitutionInternalAccountNumber
Institutioninternalaccountnumberisspaces.
GABV 9AAE Step-outreasoncode3
Step-outreasoncode3isnotequaltooneoftheacceptablevalues.Formore
information,seetheinstitutioninstructioninputoroutputspecifications.
GABW 9AAE Step-OutReasonCode1
Step-outreasoncode1isnotequaltooneoftheacceptablevalues.Formore
information,seetheinstitutioninstructioninputoroutputspecifications.
GABX 9AAE Step-OutReasonCode2
Step-outreasoncode2isnotequaltooneoftheacceptablevalues.Formore
information,seetheinstitutioninstructioninputoroutputspecifications.
GABY 9AAA Step-OutReasonCode3
Submittedtypeisinvalidforstep-outprocessing.
9AAE Step-outreasoncode3isnotequaltooneoftheacceptablevalues.Formore
information,seetheinstitutioninstructioninputoroutputspecifications.
GAC2 9ABB SpecificationCodenotfound
Specificationdidnotequalanacceptablevalue.
GAC2 9ADY SpecificationCode100Invalid
Reassignmentspecificationdidnotequalanacceptablevalue.
GAC2 IACD SpecificationCode001Invalid
Collateralregionspecificationisnotalphabeticortoolong.
GAC2 IACE SpecificationCode002Invalid
Collateralregionexcludedspecificationisnotalphabeticortoolong.
GAC2 IACF SpecificationCode060Invalid
Indexspecificationistoolong.
GAC2 IACG SpecificationCode070Invalid
Interestratecap-maximumspecificationistoolong.
GAC2 IACH SpecificationCode071Invalid
Interestratecap-minimumspecificationistoolong.
GAC2 IACI SpecificationCode005Invalid
Issuedate-earliestspecificationisaninvaliddayoftheyearorwastoolong.
GAC2 IACJ SpecificationCode006Invalid
IssueDate-Latestspecificationisaninvaliddayoftheyearorwastoolong.
Table2.3TradeSuiteIDErrorCodes(continued)
Input/OutputInformation
2.ProcessingProcedures 79

---

## Page 80

FieldcodeReasonCode Descriptions
GAC2 IACK SpecificationCode003Invalid
Issuanceregioncodespecificationisnotalphabeticorwastoolong.
GAC2 IACL SpecificationCode004Invalid
Issuanceregioncodeexcludespecificationisnotalphabeticorwastoolong.
GAC2 IACM SpecificationCode007Invalid
Maturitydate-earliestspecificationisaninvaliddayoftheyearoristoolong.
GAC2 IACN SpecificationCode008Invalid
Maturitydate-latestspecificationisaninvaliddayoftheyearorwastoolong.
GAC2 IACO SpecificationCode072Invalid
Paymentpercentagecap-maximumspecificationwastoolong.
GAC2 IACP SpecificationCode073Invalid
Paymentpercentagecap-minimumspecificationwastoolong.
GAC2 IACQ SpecificationCode074Invalid
Periodiccap-maximumspecificationwastoolong.
GAC2 IACR Specificationcode075Invalid
Periodiccap-minimumspecificationwastoolong.
GAC2 IACS Specificationcode020Invalid
Pieces-maximumnumberspecificationwasnotnumericorwastoolong.
GAC2 IACT Specificationcode021Invalid
Pieces-minimumnumberspecificationwasnotnumericorwastoolong.
GAC2 IACU Specificationcode022Invalid
Pools-maximumnumberspecificationwasnotnumericorwastoolong.
GAC2 IACV Specificationcode023Invalid
Pools-minimumnumberspecificationwasnotnumericorwastoolong.
GAC2 IACW Specificationcode024Invalid
Pools-maximumfacevaluespecificationwastoolong.
GAC2 IACX Specificationcode025Invalid
Pools-minimumfacevaluespecificationwastoolong.
GAC2 IACZ Specificationcode076Invalid
Resetdate-earliestspecificationwasaninvaliddayoftheyearorwastoolong.
GAC2 IADA Specificationcode077Invalid
Resetdate-latestspecificationwasaninvaliddayoftheyearorwastoolong.
Table2.3TradeSuiteIDErrorCodes(continued)
Input/OutputInformation
2.ProcessingProcedures 80

---

## Page 81

FieldcodeReasonCode Descriptions
GAC2 IADG Specificationcode050Invalid
WACcode–maximumpercentagespecificationwastoolong.
GAC2 IADH Specificationcode051Invalid
WACcode–minimumpercentagespecificationwastoolong.
GAC2 IADI Specificationcode052Invalid
WAMcode–maximumpercentagespecificationwastoolong.
GAC2 IADJ Specificationcode053Invalid
WAMcode–minimumpercentagespecificationwastoolong.
GAC2 IADM Specificationcode036Invalid
Monthtorollspecificationwasnotnumericorwastoolong.
GAC2 IADN Specificationcode999Invalid
Freeformspecificationwastoolong.
GAC2 IADQ Specificationcode026Invalid
Poolspermillion-minimumspecificationwastoolong.
GAC2 IADR Specificationcode027Invalid
Freeformspecificationwastoolong.
GAC2 IADS Specificationcode040Invalid
Nodownsidevariance(populateY)specificationwastoolong.
GAC2 IADT Specificationcode041Invalid
Variance(fornon-BMAstandardvariance)specificationwastoolong.
GAC2
IADU
Specificationcode052Invalid
WAMcode–maximumnumberofmonthsspecificationwastoolong.
GAC2 IADV Specificationcode053Invalid
WAMcode–minimumnumberofmonthsspecificationwastoolong.
GAC2 IADW Specificationcode054Invalid
Weightedaverageloanage(WALA)/CommercialAndGovernmentEntity
(CAGE)–maximumspecificationwastoolong.
GAC2 IADX Specificationcode055Invalid
WALA/CAGE–minimumspecificationwastoolong.
GACE 9AAE CountryCode
Invalidcountrycode.
9AAA Invalidcountrycode.
Table2.3TradeSuiteIDErrorCodes(continued)
Input/OutputInformation
2.ProcessingProcedures 81

---

## Page 82

FieldcodeReasonCode Descriptions
HACY 9AAE YieldInvalid
TheYieldwasnotnumeric.
HACZ 9AAF TerminatorValueInvalid
TheTerminatorvaluewasnotnumeric.
HADA 9AAA PossibleDuplicateFieldInvalid
The'PossibleDuplicate'fieldwasnotvalid;itmustcontaineitheraspaceoranX.
HADI 9AAA EPNTimeInvalid
The'EPNTime'fieldwasnotvalid;itmustbeeithernumericandinmilitary
format.
HADS 9AAA MBSinformationinvalid
IDCT 9BA4 M2iUSDIConfirmscanonlybeaffirmedthroughCTM
IDTS 9BA4 PreventCTMfromaffirmingnon-M2iconfirms
TAAA 9AAA ConfirmPurpose
Confirmpurposeisinvalidbecausethevalueenteredisunknown.
TAAB 9AAA DeliveryMethod
Deliverymethodisinvalid.Itisamandatoryfieldandtheenteredvalueis
unknown.
9ABD Deliverymethodismissing.Enteravalidvalue.
TAAD 9AAA PriceType
Pricetypevalueenteredisunknown.
TAAE 9AAA Tradeexecutiontime
Invalidtradeexecutiontime.EnterthetradeexecutiontimeinHH:MM:SSformat.
TAAF 9AAA TradeType
Invalidtradetype.Itisamandatoryfieldandtheenteredvalueisunknown.
9ABD Tradetypeismissing.Enteravalidvalue.
TAAG 9AAA Legidentifier
Invalidlegidentifier.Itisamandatoryfieldandtheenteredvalueisunknown.
9ABD Legidentifierismissing.Enteravalidvalue.
TAAH 9AAA CollateralType
Invalidcollateraltype.Itisamandatoryfieldandtheenteredvalueisunknown.
9ABD Collateraltypeismissing.Enteravalidvalue.
Table2.3TradeSuiteIDErrorCodes(continued)
Input/OutputInformation
2.ProcessingProcedures 82

---

## Page 83

FieldcodeReasonCode Descriptions
TAAI 9AAF NumberofPiecesofCollateral
Enterednumberofpiecesofcollateralarenotnumeric.Enteravalidvalue
between000–999.
TAAJ 9AAF FINRate
Ifsupplied,enteranumericFINrate.
TAAK 9AAF Seclendfee
Onlynumericvaluescanpopulatethisfield.
TAAL 9AAA AccrualMethod
Accrualmethodvalueenteredisunknownmakingitinvalid.
TAAM 9AAF InterestDays
Onlynumericvaluescanpopulatethisfield.
TAAN 9AAF AccruedInterestDue
Onlynumericvaluescanpopulatethisfield.
TAAO 9AAA Index
Indexvalueenteredisunknownmakingitinvalid.
TAAP 9AAF SpreadtoBench
Onlynumericvaluescanpopulatethisfield.
TAAQ 9AAF MarginRate
Onlynumericvaluescanpopulatethisfield.
TAAR 9AAF SubstitutionVar
Onlynumericvaluescanpopulatethisfield.
TAAS 9AAF REPOValue
Onlynumericvaluescanpopulatethisfield.
TAAT 9AAF PremiumAmt
Onlynumericvaluescanpopulatethisfield.
TAAU 9AAF LookBackDays
Onlynumericvaluescanpopulatethisfield.
TAAV 9AAF CallDelay
Onlynumericvaluescanpopulatethisfield.
TAAW 9AAA BlockTradeIndicatorInvalid
Ifablocktrade,thevaluemust=B.Ifnotablocktrade,thevalueshouldbea
space( ).
TAAX 9ADD SIPCMember
OnlyYorN,oraspace( )entryisacceptableforthisfield.
Table2.3TradeSuiteIDErrorCodes(continued)
Input/OutputInformation
2.ProcessingProcedures 83

---

## Page 84

FieldcodeReasonCode Descriptions
TAAY 9ADD FINRAMember
OnlyYorN,oraspace( )entryisacceptableforthisfield.
TAAZ 9ADD NYSEMember
OnlyYorN,oraspace( )entryisacceptableforthisfield.
TBAA 9ADD MarketMaker
OnlyYorN,oraspace( )entryisacceptableforthisfield.
TBAB 9AAA StartDate
Startdateisaninvaliddateoftheyear.
TBAC 9AAA EndDate/MaturityDate
Enddateisaninvaliddateoftheyearorspacesforanopenenddate.
TBAD 9AAA FINRateSign
Validvalueof+,-,orspace( )wasnotenteredmakingitinvalid.
TBAE 9AAA FINRateType
ValidvalueofF,V,orspace( )wasnotenteredmakingitinvalid.
TBAF 9AAA InterestDaysSign
Validvalueof+,-,orspace( )wasnotenteredmakingitinvalid.
TBAG 9AAA AccruedInterestDueatMaturitySign
Validvalueof+,-,orspace( )wasnotenteredmakingitinvalid.
TBAH 9AAA SpreadtoBenchmarkSign
Validvalueof+,-,orspace( )wasnotenteredmakingitinvalid.
TBAI 9AAA SubstitutionType
ValidvalueofP,M,orspace( )wasnotenteredmakingitinvalid.
TBAJ 9AAA REPOFill
ValidvalueofF,C,orspace( )wasnotenteredmakingitinvalid.
TBAK 9AAA 1stInterestCleanupDate
Firstinterestcleanupdateisaninvaliddayoftheyear.
TBAL 9AAA 1stRateResetDate
Firstrateresetdateisaninvaliddateoftheyear.
TBAM 9AAA 1stFlexRepaymentDate
Firstflexiblerepaymentdateisaninvaliddayoftheyear.
TBAO 9AAA Record6
Record6invalidfornon-financingtrade.
Table2.3TradeSuiteIDErrorCodes(continued)
Input/OutputInformation
2.ProcessingProcedures 84

---

## Page 85

FieldcodeReasonCode Descriptions
TBAQ 9ABB User-DefinedDisclosureCode
User-defineddisclosurecodewasnotfoundinthedisclosurerepository.Ensure
thecodesuppliedoninputisanexactmatchtoacoderesidingonthedisclosure
repositoryconformingwiththeallowedvaluesentered(A–Zand0–9inupperor
lowercase).
TBAR 9AAA ConfirmDisclosureBypassIndicator
Confirmdisclosurebypassindicatorisinvalid.A“B”toBypassenrichmentor
space( )toenrichwasexpected.
TBAS 9AAA MarkUp/MarkDownSign
Validvalueof+,-,orspace(   )wasnotenteredmakingitinvalid.
TBAT 9AAF MarkUp/MarkDown
Onlynumericvaluescanpopulatethisfield.
TBAU 9AAA 3rdPartyRemunerationReceived
Invalidthird-partyremunerationreceived.EnteravalidvalueofY,N,orspace( ).
TBAV 9AAA AllocationSource
Allocationsourcemustbeoneofthefollowingvalidvalues:
l 1=OASYS
l 2=TradeXPress(TradeWeb)
l 3=FIX
l 4=Market/Axess
l 5=Manual(phoneorfax)
l Space=Notsupplied
Table2.3TradeSuiteIDErrorCodes(continued)
Input/OutputInformation
2.ProcessingProcedures 85

---

## Page 86

3.ADDITIONALNOTES
Thissectionprovidesinformationabouttheprocessingnotesandinterestedparties.
AffirmingPartyIndicator
Theaffirmingpartyindicatornowcontainssixvalues(0–5).Inthenewsystem,theinterestedpartyorcustomer
canaffirmtrades.Anewvalue(5)wasaddedtoindicatethiscondition.Thefieldforold-formatoutputuser
containsa1(AffirmedByInstitution)whenthecustomerorinterestedpartyaffirmsthetrade.
InterestedParties
Thesystemprovidesinterestedpartyandsettlementinformation,asenteredontradeinputorderivedfromthe
ALERT®servicethroughtheCTMM2iserviceaspartofmatchenrichmentfeature.Amaximumofthreeadditional
partiescanappearonconfirmationoutput.
InterestedPartiesDerivedFromALERT®
Thefollowingidentifiespotentialsourcesfortheseinterestedpartiesandtheorderinwhichtheyappearonoutput:
InterestedParties:Enterinformationinuptothreeinterestedpartyfields,includingInterestedPartyInternal
AccountNumbers,ontheTradeSuiteIDconfirm.DesignatetheinterestedpartyID#1asanaffirmingpartyifthe
institutiondesignatesinterestedpartyID#1astheaffirmingpartyontheALERTserviceandisalsoutilizing
TradeMatch.ThisconditioncanonlyoccurthroughTradeMatchandmatchenrichment.TradeMatchmatch
enrichmentappendstheinterestedpartyinformationtotheTradeSuiteIDconfirmfromtheALERTservice.
New-FormatInput
Thesystemisdesignedsothatallsettlementandcustomer/interestedpartyinformationcanbederivedfromthe
ALERTplatformthroughtheTradeMatchsystemsaspartofmatchenrichmentfeatures.[[Broker]]/dealerscanalso
continuetoinputintwofields,asfollows:
l SettlementlocationsintheU.S.([[DTC]],BRC,US,FED):uptothreeinterestedparties
l SettlementlocationoutsidetheU.S.:twosub-[[Custodians]],nointerestedparties.Firstisthebrokersub-cus-
todianfollowedbyagentsub-custodian
Input/OutputInformation
3.AdditionalNotes 86

---

## Page 87

OutputLocations
Thissectiondescribesdifferentoutputlocation.
SettlementLocationofDTCorBRC
TradeSuiteIDconfirmationsdonotneedtoshowsettlementinstructionsforsettlementlocationsofDTCorBRC.
Allthreeadditionalpartyfieldsareavailableforcustomerandinterestedpartyinformationintheorderorsubmitted
ontradeinput.
SettlementLocationofNFS
DuetothedynamicnatureofREPOtransactions,agreatdealoffieldflexibilityisrequiredtopresentREPO
confirmations.OnefeatureoftheTradeSuiteIDserviceprocessingistostageaffirmedtradesforsettlementif
depositoryrequirementsaremet.Currently,thisonlyappliestoDTC-eligibletrades.Tofacilitateexpanded
capabilities,thiscanchangetoallowfortheFixedIncomeClearingCorporation([[FICC]])netting/settlementsofthe
FederalReserveBank-eligible(FRB)securitiesinthefuture,anewsettlementlocationfieldof“NFS”(notfor
[[settlement]])wascreated.
Manyrepurchasetrades,regulartrades,andmaintenanceactivitiestheTradeSuiteIDservicesupportsdonot
settleattheFED,[[DTC]],oranydepositorybutaresettledusingFFWire,checks,orothercollateral.These
transactionscaninclude,butarenotlimitedto:
l Tri-party
l Hold-in-[[custody]]
l Roll-overs
l CorrectedREPOtradeconfirmationsaftersubstitutions
l Securitylendingrepricing
l Tradepair-offs
l Roundrobins
ItisappropriateforthesetypesoftransactionstousetheNFSvalueasthesettlementlocationsinceadepository
settlementisnotimplied.
Input/OutputInformation
3.AdditionalNotes 87

---

## Page 88

AllOtherSettlementLocations
Forallothersettlementlocations,settlementinformationisrequiredontheconfirm.However,tomaximizethe
usefulnessofthethreeavailablefields,settlementinformationisshownfromtheperspectiveoftheother(contra)
side.Settlementinformationincludes:sub-[[Custodians]],depositoryaccount,andbranchinformation.
Theconfirmationrecipient’ssub-custodianisonlyusediftwointerestedpartiesoracustomerandaninterested
partyarenotdisplayedinstead.Table3.1showstherelationshipofanIDusertoitsassociatedsub-custodian.
IDuser YourSub-Custodian ContraSub-Custodian
Institution,agent,customer,orinter-
ested-partycustodian
Agentsub-custodian Brokersub-custodian
[[Broker]] Brokersub-custodian Agentsub-custodian
Table3.1IDUser/Sub-CustodianRelationship
Forexample,aninstitutionhasrecordedcustomerandtwointerestedpartiesontheALERTservice.Theconfirm
totheinstitutionshowsthebroker’ssub-custodian,customer,andinterestedpartynumber1.Theconfirmstothe
agentandtheinterestedpartiesarethesame.Theconfirmtothebrokershowstheagent’ssub-custodian,
customer,andinterestedpartynumber1.
Ifthereisonlyoneinterestedparty,theconfirmsshowthecontrasub-custodianinthefirstadditionalpartyfield,
theinterestedpartyinthesecondandtheothersub-custodianinthethird.Therefore,hereistheorderforfillingthe
threeadditionalpartyfieldsforallsettlementlocations,otherthanDTCandBRC.
1. ContraSub-Custodian
2. Customer(IDornon-[[ID]])
3. InterestedParty#1
4. InterestedParty#2
5. InterestedParty#3
6. YourSub-Custodian
Toidentifythetypeofeachadditionalparty,seepositions819,820,and821.
Input/OutputInformation
3.AdditionalNotes 88

---

## Page 89

A.SECURITYNUMBERINGSYSTEMFORMATS
Thissectiondescribestheformatsforsecuritynumbering.
EfficiencyofChecking
Onaverage,forevery10,000numberschecked,fivenumberspassthetestbuttheyareincorrectduetomultiple
errorsthatcancelout.Thisisbecausetheweightsandmodulususedinthecheckarenotaccurate.Themethod
wasselectedbysecuritiesindustryrepresentativesin1967becausetheyrequiredthatthecheck-digitbenumeric
andincrementuniformlywiththesixthdigit.Whiletherearegoodreasonsforignoringthisrequirementand
selectingdifferentweightsandmodulus,securitiesindustryrepresentativesdecidedthattheimprovementsin
checkingwhichwouldbebroughtaboutbyachangewouldnotbejustifiedbecauseofthedisruptionthatthe
changewouldcause.
ISINDefinition
ISINisacodethatuniquelyidentifiesaspecificsecuritiesissue.Itconsistsof:
l Aprefix,consistingofa2-lettercountrycode(seeISO3166)ofthecountrywheretheissuerofsecurities,other
thandebtsecurities,islegallyregisteredor,intheabsenceofregistration,inwhichhe/shehaslegaldomicile.
o FordebtsecuritiesissuedafterthedateofpublicationofthethirdeditionoftheInternationalStandard,
theagencyinthecountryoftheleadmanagerfortheparticularissueallocatestheISIN,exceptunder
conditionsdeterminedbytheleadmanager.AninternationalclearingsystemcanallocatetheISINinthe
samecapacityasanationalagency.
o FordebtsecuritiesissuedbeforethedateofpublicationofthethirdeditionoftheInternationalStandard,
theagencyinthecountryofthemainpayingagentallocatestheISIN.Theissuerofdepositaryreceiptsis
thebodywhichhasissuedthem,notthebodywhichissuedthesecuritiestheyrepresent.Therefore,the
countrycodeoftheissuerofthedepositaryreceiptsisused.
l Thebasicnumber,whichis9-characters(lettersand/ordigits)inlength.Wheretheexistingnationalnumber
consistsofninecharacters,thisisthenumbertobeused.Wherethenationalnumberconsistsoffewerthan
ninecharacters,thisalsoisusedwithzerosinsertedinfrontofthenationalnumber.Whereanationalcheck-
digitexists,itisregardedaspartofthebasicnumberwithintheninecharacters.
l Acheck-digitcomputedaccordingtothemodulus10double-add-doubleformuladescribedinISINModulus
10Double-Add-DoubleCheck-Digitonthenextpage.
Input/OutputInformation
A.SecurityNumberingSystemFormats 89

---

## Page 90

ComputingCheck-Digits
Thissectiondescribeshowtocompute:
l ISINmodulus10double-add-doublecheck-digit
l CUSIPmodulus10double-add-doublecheck-digit
l SEDOLsecuritiesidentifiercheck-digit
ISINModulus10Double-Add-DoubleCheck-Digit
Step1
Assignalphabeticcharactersanumericvalue.TheletterAis10.Thevalueofeachsubsequentletteristhe
precedingletter’svalueincrementedby1:
A = 10 G = 16 M = 22 S = 28 Y = 34
B = 11 H = 17 N = 23 T = 29 Z = 35
C = 12 I = 18 O = 24 U = 30
D = 13 J = 19 P = 25 V = 31
E = 14 K = 20 Q = 26 W = 32
F = 15 L = 21 R = 27 X = 33
Step2
Doublethevalueofalternatedigitsbeginningwiththefirstright-handdigit(loworder),includingzeros.
Step3
AddtheindividualdigitscomposingtheproductsobtainedinStep2andeachoftheunaffecteddigitsintheoriginal
number.
Step4
SubtractthetotalobtainedinStep3fromthenexthighernumberendingin0.(Thisistheequivalentofcalculating
thetenscomplementoftheloworderdigit[unitdigit]ofthetotal.)IfthetotalobtainedinStep3isanumberending
inzero(30,40,andsoforth),thecheckdigitis0.
Input/OutputInformation
A.SecurityNumberingSystemFormats 90

---

## Page 91

US 3 8 3 8 8 3 1 0 5
30 28 3 8 3 8 8 3 1 0 5
21 21 2 1 2 1 2 1 2 1 2
60 48 6 8 6 8 16 3 2 0 10
Example1W.R.GraceandCo.[[shares]](fromInternationalOrganizationforStandardizationPublication
#6166,FourthEdition,December15,1987)
6 + 0 + 4 + 8 + 6 + 8 + 6 + 8 + 1 + 6 + 3 + 2 + 0 + 1 + 0 = 59
Checkdigit1/60
JP 0 0 0 0 0 6 5 0 1
19 25 0 0 0 0 0 6 5 0 1
21 21 2 1 2 1 2 1 2 1 2
29 45 0 0 0 0 0 6 10 0 2
ExampleA.2HitachiLtd.[[shares]]
2 + 9 + 4 + 5 + 0 + 0 + 0 + 0 + 0 + 6 + 1 + 0 + 0 + 2 = 29
Checkdigit1/30
US 4 5 9 0 5 6 D G 9
30 28 5 9 0 5 6 13 16 9
21 21 2 1 2 1 2 1 21 21 2
60 48 8 5 18 0 10 6 23 26 18
ExampleA.3InternationalBankforReconstructionandDevelopment(Worldbank)151/8%due15
Dec.1991(fromInternationalOrganizationforStandardizationPublication#6166,FourthEdition,
December15,1987).
6 +0+4+8+8+5+1+8+0+1+0+6+2+3+2+6+1+8= 69
Checkdigit1/70
CUSIPModulus10Double-Add-DoubleCheck-Digit
Input/OutputInformation
A.SecurityNumberingSystemFormats 91

---

## Page 92

TheCUSIPcheck-digitisbasedonthemodulus10double-add-doubletechnique(seeISINModulus10Double-
Add-DoubleCheck-Digit).ExampleA.4showsthecalculationofamodulus10double-add-doublecheck-digit
(fromtheCUSIPDirectory,1993,preparedfortheCUSIPAgencybyStandard&Poor’sCorporation,Copyright
1993,AmericanBankersAssociation).
8 3 7 6 4 9 1 2
x1/8 x2/6 x1/7 x2/12 x1/4 x2/12 x1/1 x2/4
ExampleA.4Issuernumber837649issuenumber12.
Thus:
8+ 6+7+ 1+2 +4+1 +8+ 1+4= 42
Thecomplementofthelastdigitofthesumbecomesthecheck-digit.Thecomplementof2is8.Therefore,the
CUSIPnumberwiththecheck-digitwouldappearas:
837649128
InExampleA.5,alphabeticcharactersareassignedanumericvaluetocalculatethecheck-digit.TheletterAis10.
Thevalueofeachsubsequentletteristhevalueoftheprecedingletterincrementedby1.
A=10 B=11 C=12 D=13 E=14 F=15 G=16 H=17
I=18 J=19 K=20 L=21 M=22 N=23 O=24 P=25
Q=26 R=27 S=28 T=29 U=30 V=31 W=32 X=33
Y=34 Z=35 . (period)=36 @=37
#=38(PPNSystem-PrivatePlacementNumber)
ExampleA.5Alphabeticcharactersassignedanumericvalue
IssuerNumber392690IssueNumberQT
3 9 2 6 9 0 Q T (Q=26,T=29)
x1/3 x2/18 x1/2 x2/12 x1/9 x2/0 x1/26 x2/58
Thus:
3+ 1+8+ 2+1 +2+9 +0+ 2+6+ 5+8 =47
Thecomplementofthelastdigitofthesumbecomesthecheck-digit.Thecomplementof7is3.Therefore,the
CUSIPnumberwiththecheck-digitwouldappearas:
Input/OutputInformation
A.SecurityNumberingSystemFormats 92

---

## Page 93

392690QT3
Input/OutputInformation
A.SecurityNumberingSystemFormats 93

---

## Page 94

NotesoftheCUSIPandISINComputations
AlthoughtheCUSIPandISINcheck-digitroutinesaresimilar,theydifferinthemannerinwhichtheymultiplythe
numericvalueassignedtoaletter(AthroughZ).
TheCUSIPalgorithmmultipliesthe2-positionnumberassignedtoaletterbyasinglenumber.Therefore,aT
convertsto29andismultipliedbyeither2or1,dependingonwheretheletterwasplacedintheCUSIP.In
ExampleA.5onpage 92,Tismultipliedby2foraproductof58.Bothdigitsareaddedindependentlytothe
calculation,addingavalueof13(5+8)tothesum.
TheISINalgorithmmultipliesthe2-positionnumberassignedtoaletterbytwonumbers.Therefore,aTwould
convertto29andthetenscolumnwouldbemultipliedby1andtheunitscolumnby2(or2and1)dependingon
whereitwasplacedintheCUSIP.InExampleA.5onpage 92,thefollowingmultiplicationoccurs:(2x1)+(9x
2).Allresultingdigits(threeinthisexample)areaddedindependentlytothecalculation,addingavalueof11
(2+1+8)tothesum.
SEDOLSecuritiesIdentifierCheck-Digit
Thefollowingtopicsdescribetheformatforthesecuritiesidentifiercheckdigitandthesignificanceoftheseries
digit.
Format
Asevendigitcodenumberisallocatedtogiveeverysecurityinthesystemauniqueidentification.Formore
information,seetheSEDOL CodeStructuresectionoftheSEDOLMasterfileTechnicalSpecification.
l Firstdigitofthesevendigitsiscalledtheseriesdigit.Formoreinformation,seeSignificanceoftheSeriesDigit.
l Middlefivedigitsareallocatedtotherange00001–99998sothatthenumericsequenceofthesedigitscor-
respondsapproximatelytothealphabeticsequenceofthesecuritywithinaseriesdigit.Thereisnocor-
respondenceinsequencebetweenthedifferentseries.
l Lastofthesevendigitsisamodulus-tencheck-digit.
Input/OutputInformation
A.SecurityNumberingSystemFormats 94

---

## Page 95

Thenormalformatforprintingthenumberis0-123-457.Breakingthenumberintosmallgroupslikethisreduces
theriskoftranscriptions.
SignificanceoftheSeriesDigit
TableA.1describesthesignificanceoftheseriesdigit(firstposition).Notethattheseriesdigitdoesnotinclude
classificationofsecuritiesbygeographicalarea.Thecountryofincorporationandotherclassificationcodesare
usedinstead.Normally,anewcodenumberisnotallocatedtoasecuritybecauseitscurrentseriesdigitis
inappropriate.
Digit Description
0 Officiallycodedsecuritythatsatisfiesoneormoreofthefollowingconditions:
l Ithasafull,UnlistedSecuritiesMarketorThirdMarketListing.
l ItisregisteredintheBritishIslesorGibraltarbutisnotlistedonTheStockExchange.
l ItislistedbyanorganizationincorporatedintheBritishIslesorGibraltarandnotlistedorregisteredelsewhere.
1 PrivatelycodedsecurityforaUser’sinternalprocedures.TheStockExchangeusesthisseriesforspecialtestitems,but
informationaboutsuchitemsisnotpublished.
2 Officiallycodedsecuritythatsatisfiesoneormoreofthefollowingconditions:
l ItislistedonanexchangeintheAmericancontinentalarea.
l ItisregisteredintheAmericancontinentalareabutisnotlistedthereoronTheStockExchange.
l ItisissuedbyanorganizationincorporatedintheAmericancontinentalareaandnotlistedorregisteredelsewhere.
l ADRsarelistedonTheStockExchange.
3 ReservedforfutureusebyTheStockExchange.
4 Officiallycodedsecuritythatsatisfiesoneormoreofthefollowingconditions:
l ItislistedonastockexchangeintheEuropeancontinentalarea(countriesotherthantheBritishIslesandGibraltar).
l ItisregisteredintheEuropeancontinentalareabutisnotlistedorregisteredelsewhere.
l ItisissuedbyanorganizationincorporatedintheEuropeancontinentalareaandnotlistedorregisteredelsewhere.
5 ReservedforfutureusebyTheStockExchange.
TableA.1SEDOLSeriesDigitExplanation
Input/OutputInformation
A.SecurityNumberingSystemFormats 95

---

## Page 96

Digit Description
6 Officiallycodedsecuritythatsatisfiesoneormoreofthefollowingconditions:
l ItislistedonastockexchangeintheAfrican,Australian,FarEastern,orothercontinentalareas.
l Itisregistered,butnotlistedintheAfrican,Australian,FarEastern,orothercontinentalareasnorisitlistedonThe
StockExchange.
l ItisissuedbyanorganizationincorporatedintheAfrican,Australian,FarEasternorothercontinentalareasandnotlis-
tedorregisteredelsewhere.
7 ReservedforfutureusebyTheStockExchange.
8 OfficiallycodedsecuritythatTheStockExchangehasruledshallbecodedinthisseries,notwithstandingitseligibilityfor
codinginanotherseries.Blocksofthisseriesarereservedforspecifictypesofsecurities.Thefollowingblocksarecurrently
inuse:
8400000–8449995Tradedoptions
8500007–8549981Tradedoptions
8600004–8649999Tradedoptions
8700595–8999995Tradedoptions
8101228–8201485ReservedforExcel
8450005–8499990ReservedforExcel
8550002–8599986ReservedforExcel
8650009–8700584ReservedforExcel
8000013–8101206Unlistedlocalauthoritymortgages
8201504–8399993Securitiesmasterfile
9 Privatelycodeditemthatcannotbeconsideredasecurity,secondarysecurity,orspecialitem.Thestockexchangeusesthis
seriesfortextitemsthatareprintedindirectoriesandcodebooks.Suchnumbersarenotpublished;therefore,theprivate
allocationsofusersareinnowayrestricted.
BuildingSocietyNumbers.Thefollowingnumbersinthe9-serieshavebeenpublishedbybuildingsocietiesontheinterest
taxcounterfoils:
9-102-004to9-104-992
Note:Avoidallocatingnumbersinthebuildingsocietyrangesothatyoudonotconfuseyourownprivatelyallocated
numberswiththebuildingsocietiesnumbers.Futurebuildingsocietiesnumbersareallocatedinthe0-seriesiftheitemisa
particularclassofshareordeposit.
TableA.1SEDOLSeriesDigitExplanation(continued)
Input/OutputInformation
A.SecurityNumberingSystemFormats 96

---

## Page 97

CheckingaNumber
Tocheckthatanumberisreportedcorrectly,eachdigitismultipliedbyaweightandtheresultsareadded.The
weightusedforeachdigitissetoutasfollows:
Digit Weight
1st(series) 1
2nd 3
3rd 1
4th 7
5th 3
6th 9
7th 1
TableA.2DigitWeight
Ifthesumoftheresultsisamultipleof10,thenumberisconsideredcorrect,otherwiseitisincorrect.ExampleA.6
andExampleA.7showtheapplicationofthemethod.
Digit Weight Product
0 1 0
1 3 3
2 1 2
3 7 21
4 3 12
5 9 45
7 1 7
Sum=90
ExampleA.6Numberreportedas0-123-4570
Sincethesumisamultipleof10,thenumberisquotedcorrectly.
Input/OutputInformation
A.SecurityNumberingSystemFormats 97

---

## Page 98

Digit Weight Product
0 1 0
1 3 3
2 1 2
5 7 35
4 3 12
5 9 45
7 1 7
Sum=104
ExampleA.7Numberreportedas0-125-457
Becausethesumisnotamultipleof10,thenumberisquotedincorrectly.
DerivingaCheck-Digit
Toderiveacheck-digitforanumber:
1. Multiplyeachofthesixdigitsbythecorrespondingweight.
2. Addtheresultsanddividetheanswerby10.
3. Subtracttheremainderfrom10,unlessitis0.
l Iftheremainderisgreaterthan0,thecheck-digitisthedifferencebetweentheremainderand10.
l Iftheremainder=0,thecheckdigit=0.
ExampleA.8andExampleA.9showtheapplicationofthemethod.
Digit Weight Product
0 1 0
1 3 3
2 1 2
3 7 21
4 3 12
5 9 45
Sum=83
ExampleA.8Number0-123-457
Input/OutputInformation
A.SecurityNumberingSystemFormats 98

---

## Page 99

Remainderondivisionby10=3;therefore,thecheck-digit=7.
Digit Weight Product
0 1 0
1 3 3
0 1 0
1 7 7
0 3 0
0 9 0
Sum=10
ExampleA.9Number0-101-00?
Remainderondivisionby10=0.Therefore,thecheck-digit=0.
Input/OutputInformation
A.SecurityNumberingSystemFormats 99

---

## Page 100

©2024Allrightsreserved.[[DTCC]],[[DTCC]](Stylized)andFinancialMarkets.Forward.areregisteredandunregistered
trademarksofTheDepositoryTrust&ClearingCorporationDTCC.Theservicesdescribedhereinareprovidedunder
the“[[DTCC]]”brandnamebycertainaffiliatesofTheDepositoryTrust&ClearingCorporation(“[[DTCC]]”).DTCCitself
doesnotprovidesuchservices.Eachoftheseaffiliatesisaseparatelegalentity,subjecttothelawsandregulationsof
theparticularcountryorcountriesinwhichsuchentityoperates.Pleaseseewww.[[DTCC]].comformoreinformationon
[[DTCC]],itsaffiliatesandtheservicestheyoffer.
DocDate:February09,2024
PublicationCode:TS267
Service:TradeSuiteID
Title:Input/OutputInformation
ForMoreInformation
EmailDTCCLearningat:
DTCCLearning@[[DTCC]].com
orvisitusonthewebat:
www.dtcclearning.com