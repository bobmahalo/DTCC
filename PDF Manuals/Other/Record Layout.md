---
title: "Record Layout.pdf"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Record%20Layout.pdf"
pages: 1
size: "72.6 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Record Layout.pdf

**Original File:** [Record Layout.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Record%20Layout.pdf)  
**Category:** Other  
**Total Pages:** 1  
**File Size:** 72.6 KB  

---

## Page 1

1/30/24, 8:28 PM Record Layout
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/end_of_day/rec_lay_2.htm?Highlight="Book Entry Only" 1/1
Back to Top
Position Length Format Field Name Description
1 9 character [[CUSIP]] A [[CUSIP]] is a nine-characteralphanumeric code that identifiesa North American financialsecurity for the purposes offacilitating clearing andsettlement of trades.
11-13 3 character Sub-IssueType The proprietary [[DTCC]] method ofclassifying [[securities]] into sub-categories based on sharedqualities and characteristics.
15-34 20 character ShortDescription Free form text describing asecurity.
36-83 48 character Long Description Free form text indicating generalsecurity characteristics andissuer.
85-97 13 Numeric The number of [[securities]] (eitherpar amount or [[shares]]) for whichDTC “[[Cede & Co]]” is listed as theholder of record, in wholenumber format. This value islisted in par amount for fixedincome [[securities]] and in sharesfor [[Equity]] [[securities]].
For Book Entry Only [[securities]],for which physical certificates arenot available to investors,reflects the entire balance or theAmount/[[shares]] Outstanding ofthat security.
Notes
If a [[CUSIP]] is a 144A and [[Reg S]] security and the issue is split across twoCUSIPs, will be represented in each of those CUSIPs, instead of beingaggregated into a single [[CUSIP]]. A security's [[EOD]] position can be impacted by any corporate action.Corporate actions are reflected in [[DTC]]'s End of Day position on theallocation of payable date.