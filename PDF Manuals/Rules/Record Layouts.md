---
title: "Record Layouts.pdf"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Record%20Layouts.pdf"
pages: 2
size: "122.5 KB"
category: "Rules"
ingested_on: "2026-06-05"
---

# Record Layouts.pdf

**Original File:** [Record Layouts.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Record%20Layouts.pdf)  
**Category:** Rules  
**Total Pages:** 2  
**File Size:** 122.5 KB  

---

## Page 1

1/30/24, 8:27 PM Record Layouts
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/end_of_day/rec_lay.htm?Highlight="Book Entry Only" 1/2
SFTP File Delivery Layout
This layout applies to both Equities and Fixed Income files.
SFTP File LayoutField Name Format Type DescriptionReport Date Date (YYYY-MM-DD) The date when the End of Day position is calculated, provided inYYYY-MM-DD formatCUSIP Alphanumeric A [[CUSIP]] is a nine-character alphanumeric code that identifies aNorth American financial security for the purposes of facilitatingclearing and [[settlement]] of trades.Sub Issue Type Numeric The proprietary [[DTCC]] method of classifying [[securities]] into sub-categories based on shared qualities and characteristics.Sub Issue Type Name Alphabetic A sub-issue further classifies an instrument
Security Description Alphanumeric Free form text indicating the security's general securitycharacteristics and [[issuer]].[[DTC]] End of DayPosition Numeric The number of [[securities]] (either par amount or [[shares]]) for whichDTC “[[Cede & Co]]” is listed as the holder of record, provided in wholenumber format. This value is listed by par amount for fixed incomesecurities and in [[shares]] for [[Equity]] [[securities]]. For Book Entry Onlysecurities, for which physical certificates are not available toinvestors, [[DTC]]'s End of Day Position reflects the entire balance orthe Amount/[[shares]] Outstanding of that security.Registration Type Alphabetic Identifies the method by which the certificate will be exercised:
Book Entry Only ([[BEO]])
Fully Registered
Bearer
Interchangeable (F/K/A Dematerialized)
Blank (see FAQs for details)
[[Regulation S]] Indicator Alphabetic Identifies the exemption through which corporations can issueunregistered [[securities]] to qualified foreign investors and foreigninstitutes. Available values:
Y: Yes
N: No
Blank: Not Applicable/Not Available
[[Rule 144A]] Indicator Alphabetic Identifies the exemption through which corporations can issueunregistered [[securities]] to qualified institutional buyers ([[QIB]]).Available values:
Y: Yes
N: No
Blank: Not Applicable/Not Available
Snowflake File Delivery Layout
This layout applies to both Equities and Fixed Income files.
Snowflake File LayoutField Name Format Type DescriptionREPORT DATE Date (YYYY-MM-DD) The date when the End of Day position is calculated, provided inYYYY-MM-DD formatCUSIP Alphanumeric A [[CUSIP]] is a nine-character alphanumeric code that identifies aNorth American financial security for the purposes of facilitatingclearing and [[settlement]] of trades.SUBISSUE TYPE Numeric The proprietary [[DTCC]] method of classifying [[securities]] into sub-categories based on shared qualities and characteristics.SUBISSUE TYPENAME Alphabetic A sub-issue further classifies an instrument
SECURITYDESCRIPTION Alphanumeric Free form text indicating the security's general securitycharacteristics and [[issuer]].

---

## Page 2

1/30/24, 8:27 PM Record Layouts
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/end_of_day/rec_lay.htm?Highlight="Book Entry Only" 2/2
Back to Top
Field Name Format Type DescriptionDTC END OF DAYPOSITION Numeric The number of [[securities]] (either par amount or [[shares]]) for whichDTC “[[Cede & Co]]” is listed as the holder of record, provided in wholenumber format. This value is listed by par amount for fixed incomesecurities and in [[shares]] for [[Equity]] [[securities]]. For Book Entry Onlysecurities, for which physical certificates are not available toinvestors, [[DTC]]'s End of Day Position reflects the entire balance orthe Amount/[[shares]] Outstanding of that security.REGISTRATION TYPE Alphabetic Identifies the method by which the certificate will be exercised:
Book Entry Only ([[BEO]])
Fully Registered
Bearer
Interchangeable (F/K/A Dematerialized)
Blank (see FAQs for details)
[[regulation]] SINDICATOR Alphabetic Identifies the exemption through which corporations can issueunregistered [[securities]] to qualified foreign investors and foreigninstitutes. Available values:
Y: Yes
N: No
Blank: Not Applicable/Not Available
RULE 144AINDICATOR Alphabetic Identifies the exemption through which corporations can issueunregistered [[securities]] to qualified institutional buyers ([[QIB]]).Available values:
Y: Yes
N: No
Blank: Not Applicable/Not Available