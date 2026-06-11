---
title: "Activity 55B Relinquishment Book Entry.pdf"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Activity%2055B%20Relinquishment%20Book%20Entry.pdf"
pages: 1
size: "115.7 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Activity 55B Relinquishment Book Entry.pdf

**Original File:** [Activity 55B Relinquishment Book Entry.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Activity%2055B%20Relinquishment%20Book%20Entry.pdf)  
**Category:** Other  
**Total Pages:** 1  
**File Size:** 115.7 KB  

---

## Page 1

1/30/24, 8:23 PM Activity 55B Relinquishment Book Entry
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/ccf_reorg/55b_put_relinquish.htm?Highlight=book entry 1/1
Activity 55B: Relinquishment Book Entry
Position Length Format Field Name Field Description
44 8 Numeric VOI Entry Start Date CCYYMMDD first day that a Voluntary Offering Instruction can be entered through [[DTC]]
52 8 Numeric VOI Entry End Date CCYYMMDD last day that a Voluntary Offering Instruction can be entered through [[DTC]]
60 9 Character Contra [[CUSIP]] A temporary [[CUSIP]] number set up to complete a reorganization function.
69 2 Character Contra [[CUSIP]] Country Code International country code
71 1 Character Contra [[CUSIP]] Check Digit International check digit
72 20 Character Contra [[CUSIP]] Description (Free-form text) description of the contra [[CUSIP]] relevant to this envelope
92 8 Character Tender Agent 8-character identifier of agent accepting instructions on a voluntary offering
100 8 Numeric Payment Date CCYYMMDD date payment is expected/received
108 1 Character Puts Eligible Activity eligible for [[DTC]]'s "put" function Y = yes
N = no
109 40 Character Information Source (Free-form text) [[DTC]]'s source of information about a reorganization activity
149 8 Character Drop Agent 8-character identifier of third-party agent used when regular agent is not available
157 8 Character Filler [[DTC]] use only; [[DO]] not use
165 1 Character Comments Indicator Y = there are comments associated with the envelope [[ID]] N = comments [[DO]] not exist for the envelope [[ID]]
166 1 Character Envelope Status Indicator Status indicator of this envelope [[ID]] A = Active
P = Preliminary
167 20 Character Supervisor's Name (Free-form text) name of the area supervisor for this envelope [[ID]]
 
 
Activity 55B: Relinquishment Book Entry
Position Length Format Field Name Field Description
187 10 Character Supervisor's Phone Num Phone number of the area supervisor for this envelope [[ID]]
197 20 Character Clerk's Name (Free-form text) name of the clerk for this Envelope [[ID]]
217 10 Character Clerk's Phone Phone number of the clerk for this Envelope [[ID]]
227 8 Numeric Envelope Create Date CCYYMMDD date on which the envelope was created
235 1 Character Envelope Indicator A  =  added U = updated D = deleted
236 1 Character Recycle Cutoff Indicator A = anticipated early recycle cutoff E = early recycle cutoff
237 1 Character Withdrawal Privilege Values: ‘N’, ‘Y’
238 8 Numeric Comments Added/Last Update Dated CCYYMMDD the last date the comments were updated or added
246 1 Character FOSP
Indicator
‘0' = Security not eligible for FOSP processing ‘1' = Security eligible for FOSP processing
247 1104 Character Filler [[DTC]] use only; [[DO]] not use
 
 
 
Delete this text and replace it with your own content.