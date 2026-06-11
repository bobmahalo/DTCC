---
title: "Activity 65B_ Retainment Book Entry Record.pdf"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Activity%2065B_%20Retainment%20Book%20Entry%20Record.pdf"
pages: 2
size: "157.1 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Activity 65B_ Retainment Book Entry Record.pdf

**Original File:** [Activity 65B_ Retainment Book Entry Record.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Activity%2065B_%20Retainment%20Book%20Entry%20Record.pdf)  
**Category:** Other  
**Total Pages:** 2  
**File Size:** 157.1 KB  

---

## Page 1

1/30/24, 8:24 PM Activity 65B: Retainment Book Entry Record
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/ccf_reorg/65b_retainmentbook.htm?Highlight=book entry 1/2
Position Length Format Field Name Field Description
44 8 Numeric VOI Entry Start Date CCYYMMDD first day that a Voluntary Offering Instruction canbe entered through [[DTC]]
52 8 Numeric VOI Entry End Date CCYYMMDD last day that a Voluntary Offering Instruction canbe entered through [[DTC]]
60 9 Character Contra [[CUSIP]] A temporary [[CUSIP]] number set up to complete areorganization function.
69 2 Character Contra [[CUSIP]] CountryCode International country code
71 1 Character Contra [[CUSIP]] CheckDigit International check digit
72 20 Character Contra CUSIPDescription (Free-form text) description of the contra [[CUSIP]] relevant to thisenvelope
92 8 Character Tender Agent 8-character identifier of agent accepting instructions on avoluntary offering
100 8 Numeric Payment Date CCYYMMDD date payment is expected/received
108 1 Character Puts Eligible Activity eligible for [[DTC]]'s "put" function Y = yesN = no
109 1 Character Rate Including AccruedInterest Y = accrued interest included in payment via "puts" functionN = accrued interest not included in payment via "puts" function
110 40 Character Information Source (Free-form text) [[DTC]]'s source of information about areorganization activity
150 8 Character Remarketing Agent Not applicable
158 8 Character Drop Agent Not applicable
166 8 Character Filler [[DTC]] use only; [[DO]] not use
174 1 Character Comments Indicator Y = there are comments associated with the envelope [[ID]] N =comments [[DO]] not exist for the envelope [[ID]]
175 1 Character Envelope StatusIndicator Status indicator of this envelope [[ID]] A = activeP = preliminary
176 20 Character Supervisor's Name (Free-form text) name of the area supervisor for this envelopeID
196 10 Character Supervisor's Phone Num Phone number of the area supervisor for this envelope [[ID]]
206 20 Character Clerk's Name (Free-form text) name of the clerk for this Envelope [[ID]]
226 10 Character Clerk's Phone Phone number of the clerk for this Envelope [[ID]]
236 8 Numeric Envelope Create Date CCYYMMDD date on which the envelope was created
244 1 Character Envelope Indicator A  =  added U = updated D = deleted
245 1 Character Recycle Cutoff Indicator A = anticipated early recycle cutoff E = early recycle cutoff
246 1 Character Foreign Currency Eligible Y = the envelope is eligible to be paid out in foreign currencyN = the envelope is not eligible to be paid out in foreigncurrency
247 1 Character Foreign CurrencyMandatory Y = it is mandatory that the issue be paid out in foreigncurrencyN = it is not mandatory that the issue be paid out in foreigncurrency
248 8 Numeric Foreign Currency VOIStart Date CCYYMMDD first day to elect payment in foreign currency
256 8 Numeric Foreign Currency VOIEnd Date CCYYMMDD last day to elect payment in foreign currency
264 3 Character Foreign Currency Type aaa 3-letter foreign currency code (see Appendix B beginningon page 231)

---

## Page 2

1/30/24, 8:24 PM Activity 65B: Retainment Book Entry Record
https://dtcclearning.com/helpfiles_secure/data/cds_kinetics/Content/Topics/ccf_reorg/65b_retainmentbook.htm?Highlight=book entry 2/2
Position Length Format Field Name Field Description
267 1 Character MMI Indicator Y = security undergoing the reorganization activity is defined byDTC as a Money Market Instrument (MMI)N = not a Money Market Instrument
268 1 Character Withdrawal Privilege Values: ‘N’, ‘Y’
269 8 Numeric Comments Added/LastUpdate Dated CCYYMMDD the last date the comments were updated oradded
277 1 Character FOSPIndicator ‘0' = Security not eligible for FOSP processing ‘1' = Securityeligible for FOSP processing
278 1073 Character Filler [[DTC]] use only; [[DO]] not use