---
title: "ETF Message Codes"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/etf221_message_codes_2021Oct28.pdf"
pages: 10
size: "641.9 KB"
category: "ETF"
ingested_on: "2026-06-05"
---

# ETF Message Codes

**Original File:** [etf221_message_codes_2021Oct28.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/etf221_message_codes_2021Oct28.pdf)  
**Category:** ETF  
**Total Pages:** 10  
**File Size:** 641.9 KB  

---

## Page 1

EXCHANGE TRADED FUND ([[ETF]])
MESSAGE CODES
OCTOBER 28, 2021


---

## Page 2

© 2021 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and 
the Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation.
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust 
& Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate 
legal entity, subject to the laws and regulations of the particular country or countries in which such entity operates. 
Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.
Doc Info: October 28, 2021 
Publication Code: ETF221
Service: Exchange Traded Fund ([[ETF]]) 
Title: Message Codes 

---

## Page 3

Message Codes and Descriptions 3
MESSAGE CODES AND DESCRIPTIONS
The following table shows the message code details and descriptions of the abbreviations used in the 
columns. New messages and file types for Phase 2 appear in red. These message codes are available after 
the specific initiative is deployed.
Message Types
l Reject = REJ = R
l Warning = WARN = W
l Informational = INFO = I
File Type
l C/R = Create/Redeem
l PCF = Portfolio Composition File
l Both = Information applies to both PCF
and Create/Redeem file types.
Message Description
l FX = Foreign exchange
Message 
Code
Message 
Type 
Record 
Type
Field File 
Type
Message Description
101 REJ 1 N/A Both [[ETF]] agent specified on the header record  was not found 
on the entity master file.
135 WARN 1 N/A Both Duplicate File Header  submitted. Second submission 
header will be discarded.
136 WARN 1 N/A Both Invalid Processing date or if processing date is not 
current date.
137 WARN 1 N/A Both Processing date on the header record does not match 
the expected processing date.  During primary cycle this 
is the current date and during the supplemental cycle it 
is the previous business date.
138 WARN 1 N/A Both Records that were found before the header record were 
not processed. 
170 INFO 1 N/A PCF No Carry Forward Portfolio. The agent does not have 
any portfolios that were carried forward today.
200 WARN 2 N/A PCF Redeem portfolio has not been submitted.
201 REJ 2 N/A Both Invalid [[NSCC]] Portfolio [[ID]]; Portfolio [[ID]] is not on the 
[[NSCC]] Master file.
202 REJ 2 N/A Both Associated Trading [[CUSIP]] not valid (not on the [[NSCC]] 
Master file).
203 REJ 2 N/A Both [[ETF]] agent number does not match the header record 
(on record type 1).
204 REJ 2 N/A Both [[ETF]] agent is not the agent for the portfolio.
225 REJ 2 N/A PCF Invalid Cash Only Indicator (any other input besides Y or 
space).
226 REJ 2 N/A PCF No components submitted for non-cash portfolio.
227 REJ 2 N/A PCF No components accepted for non-cash portfolio.
228 REJ 2 N/A PCF Weighted [[shares]] = 0 for all components in a non-cash 
portfolio.
[[ETF]] Message Codes

---

## Page 4

MessageCodesandDescriptions 4
Message 
Code
Message 
Type 
Record 
Type
Field File 
Type
Message Description
229 REJ 2 N/A C/R Portfolio not Create/Redeem eligible.
230 REJ 2 N/A PCF Duplicate portfolio header record (on record type 1) was 
submitted. The second header record was rejected.
231 REJ 2 N/A C/R Accepted transaction found with the same Transaction 
[[ID]].
232 REJ 2 N/A C/R Create/Redeem Cycle CD = [[EOD]]. Record rejected.
233 REJ 2 N/A PCF [[DO]] not publish Indicator is set on the master file for the 
portfolio.
234 REJ 2 N/A C/R [[settlement]] amount is negative. Instructions not 
processed.
235 REJ 2 N/A C/R [[settlement]] date set in the past for As-Of trade.
236 WARN 2 4 PCF Invalid Component Count.
237 WARN 2 4 PCF Component Count does not equal component count 
received by [[NSCC]].
238 WARN 2 N/A PCF Component Count set to number of components 
accepted by [[NSCC]]. This occurs when [[NSCC]] rejected 
some components.  [[NSCC]] will change the component 
count to the number of components that were accepted.
241 WARN 2 N/A PCF Prior day’s portfolio being used.
243 WARN 2 17 C/R Transaction time stamp not valid.
244 REJ 2 N/A Both Portfolio [[ID]] is not active.
245 WARN 2 18 C/R Recoded to 0 (new trade).
246 INFO 2 18 C/R Corrects a prior transaction.
247 INFO 2 18 C/R Reverses a prior transaction.
248 INFO 2 N/A C/R Provisionally accepted.
249 INFO 2 N/A C/R Original instruction pended.
250 REJ 2 N/A C/R Non-cash portfolio has no [[NSCC]] eligible components. 
251 INFO 2 N/A C/R Original instruction was provisionally accepted.
252 REJ 2 N/A C/R Pended transaction was rejected.
253 REJ 2 N/A C/R Instruction received prior to supplemental portfolio. 
254 REJ 2 N/A C/R Above maximum [[settlement]] amount.
255 REJ 2 N/A C/R Below threshold.
256 INFO 2 23 PCF Variable Fee Amount is not numeric.
257 INFO 2 24 PCF Baby Bond Cash Amount is not numeric.
258 INFO 2 25 PCF Fixed Income Face Value Adjustment is not numeric.
259 WARN 2 22 PCF [[ETF]] basket unit size is not numeric.
260 INFO 2 26 PCF Fund legal entity identifier (LEI) is invalid.
261 INFO 2 27 PCF Fund size is not numeric.
ETFMessageCodes

---

## Page 5

MessageCodesandDescriptions 5
Message 
Code
Message 
Type 
Record 
Type
Field File 
Type
Message Description
262 INFO 2 28 PCF Share Class Apportionment Ratio  is not numeric.
263 INFO 2 29 PCF Projected Transaction Fee is not numeric.
264 INFO 2 30 PCF Date for Projected Transaction Fee is invalid.
265 INFO 2 31 PCF Confirmed Transaction Fee is not numeric.
266 WARN 2 32 PCF Date for confirmed transaction fee is invalid.
267 REJ 2 19 PCF Cash only negotiated basket.
268 REJ 2 35 PCF [[NSCC]] Portfolio [[ID]] has Pricing Usage IND=Y.
269 WARN 2 N/A PCF Pricing portfolio has not been submitted.
270 INFO 2 5 PCF Estimated T-1 Cash Amount per Creation Unit is not 
numeric.
271 INFO 2 18 PCF Estimated Cash Value of [[Cash-in-Lieu]] components are 
not numeric.
272 INFO 2 7 PCF Net [[Asset]] Value per Creation Unit is not numeric.
273 INFO 2 9 PCF Estimated T-1 Cash Amount per [[ETF]] not numeric.
274 INFO 2 11 PCF Net [[Asset]] Value per [[ETF]] is not numeric.
275 INFO 2 13 PCF Total Cash Amount per Creation unit is not numeric.
276 INFO 2 15 PCF Total [[shares]] outstanding per [[ETF]] on T-1 are not 
numeric.
277 INFO 2 16 PCF [[Dividend]] amount per [[ETF]] on T-1 is not numeric.
278 INFO 2 20 PCF [[ETF]] Expense Ratio on T-1 is not numeric.
279 INFO 2 21 PCF Total Net [[Asset]] Value of [[ETF]] Fund on T-1 is not 
numeric.
280 INFO 2 12 C/R Invalid currency code, USD, substituted. 
281 INFO 2 2 C/R Rejected Transaction [[ID]] reprocessed. 
282 REJ 2 2 C/R Transaction [[ID]] is not provided.
283 REJ 2 N/A PCF Standard Portfolio for this basket was not found.
284 WARN 2 34 PCF Basket units outstanding are not numeric.
285 WARN 2 33 PCF Projected cash for pricing basket is not numeric.
286 WARN 2 35 PCF Pricing usage indicator is invalid.
287 WARN 2 N/A PCF Negotiated record is associated with a non-negotiated 
basket.
288 WARN 2 36 PCF Create Usage indicator is invalid.
289 WARN 2 37 PCF Redeem Usage indicator is invalid.
290 REJ 2 N/A C/R Negotiated portfolio was not found for the trade date and 
transaction [[ID]].
291 REJ 2 19 PCF Cash only pricing basket.
292 REJ 2 36 PCF [[NSCC]] Portfolio [[ID]] has Create Usage IND=Y.
293 REJ 2 37 PCF [[NSCC]] Portfolio [[ID]] has Redeem Usage IND=Y.
ETFMessageCodes

---

## Page 6

MessageCodesandDescriptions 6
Message 
Code
Message 
Type 
Record 
Type
Field File 
Type
Message Description
295 WARN 3 19 C/R [[Haircut]] percentage is invalid. 
296 WARN 2 N/A PCF Create portfolio has not been submitted.
297 REJ 2 N/A Both File header record (on record type 1) is invalid.
298 REJ 2 N/A Both File was received too late.
299 INFO 2 N/A C/R Provisionally accepted.
300 REJ 3 N/A PCF Portfolio Header Record (on record 2) was not found for 
the portfolio associated with the Component Record.
301 REJ 3 N/A C/R No components after removals.
302 REJ 3 3 Both Invalid Component [[ID]] Code.
303 REJ 3 N/A C/R SI ONLY = YES. Reject 03 record.
304 REJ 3 3 Both No component [[ID]] code submitted (blank).
305 REJ 3 5 PCF Component quantity is not numeric.
306 REJ 3 2 C/R No instruction records for the transaction [[ID]]. 
307 REJ 3 N/A C/R Instruction record is cash only.
308 REJ 3 N/A C/R Custom remove component is rejected.
310 REJ 3 4 C/R Component not in the portfolio.
311 REJ 3 4 Both Component [[ID]] has an invalid length or alignment.
312 REJ 3 4 PCF Component [[ID]] is not alphanumeric.
314 REJ 3 2 PCF [[NSCC]] Portfolio [[ID]] is invalid.
315 REJ 3 N/A Both File header is invalid
316 REJ 3 N/A Both File receiver is too late. 
317 REJ 3 N/A C/R Component is  cash in lieu (CIL). 03 Record is invalid.
318 WARN 3 N/A PCF Component provisionally accepted.
319 WARN 3 N/A PCF Security added after the Trade Date. The cash in lieu 
(CIL) indicator is set to X.
320 WARN 3 4 PCF Component [[ID]] Check digit is invalid.
336 WARN 3 7 PCF External [[settlement]] Date is prior to the Trade Date.
337 WARN 3 9 PCF Invalid value for the cash in lieu (CIL) indicator, indicator 
is set to space.
338 WARN 3 N/A PCF Cash in lieu (CIL) indicator applied by [[NSCC]] (set to X) 
on one or more components.
339 WARN 3 N/A PCF CIL indicator applied by [[NSCC]]/ set to X for [[CUSIP]] 
component not on the [[NSCC]] Master file.
340 WARN 3 N/A PCF CIL indicator is set to X for ISIN component, not on the 
[[NSCC]] Master file.
341 WARN 3 7 PCF Invalid External [[settlement]] Date.
344 WARN 3 N/A PCF CIL indicator is applied by [[NSCC]]/ set to X for short 
position component.
ETFMessageCodes

---

## Page 7

MessageCodesandDescriptions 7
Message 
Code
Message 
Type 
Record 
Type
Field File 
Type
Message Description
345 WARN 3 N/A PCF Component [[ID]] is no longer valid.  It has been deleted 
from the master table.
346 WARN 5 6 C/R Accrued interest is not required for the [[Equity]] 
component. 3 12 PCF
347 WARN 5 6 C/R Accrued interest is not provided for the fixed income 
component. 3 13 PCF
348 WARN 3 N/A PCF Baby [[Bonds]] not eligible for clearance. 
373 INFO 3 8 PCF Invalid new security indicator- set to space.
377 INFO 3 11 PCF WI mismatch. Using the value from the master tables.
378 WARN 3 12 PCF Nonstandard accrued interest is invalid. 
379 WARN 3 13 PCF Standard accrued interest is invalid. 
380 WARN 3 15 PCF Excluded From Pricing Quantity  is not numeric.
381 WARN 3 16 PCF Price amount on NAV date  is not numeric.
382 WARN 3 17 PCF Local Currency Code is invalid.
383 WARN 3 18 PCF Factor  value  is not numeric.
384 WARN 3 19 PCF Synthetics Currency Code is invalid.
385 WARN 3 20 PCF Synthetics Price Multiplier  is not numeric.
386 WARN 3 21 PCF Synthetics Contract Size  is not numeric.
387 WARN 3 22 PCF Synthetics Average Contract Price  is not numeric.
388 WARN 3 23 PCF FX Rates base currency is invalid. 
(FX = foreign exchange)
389 WARN 3 24 PCF FX rates currencies is invalid.
390 WARN 3 25 PCF FX Forward Currency Pair is invalid.
391 WARN 3 26 PCF FX Forward Value Date is invalid.
392 WARN 3 27 PCF FX Forward Quantity is not numeric.
393 WARN 3 28 PCF FX Forward Rate is not numeric.
394 WARN 3 29 PCF FX Forward Value is not numeric.
395 WARN 3 30 PCF FX Forward Currency is invalid.
396 WARN 3 31 PCF SWAPS Notional Value is not numeric.
397 WARN 3 32 PCF SWAPS Spread is not numeric.
398 WARN 3 33 PCF SWAPS Market Value is not numeric.
399 WARN 3 25 PCF Incomplete FX Forward Currency Pair Code. 
400 REJ 4 N/A PCF Custom record received for the Standard portfolio.
401 REJ 4 N/A PCF Custom record missing for the Custom portfolio.
402 WARN 2 N/A PCF Custom record missing for the Negotiated basket. 
403 REJ 5 3 C/R Component [[ID]] code is invalid. 
404 REJ 5 4 C/R Component [[ID]] cannot be blank.
ETFMessageCodes

---

## Page 8

MessageCodesandDescriptions 8
Message 
Code
Message 
Type 
Record 
Type
Field File 
Type
Message Description
405 REJ 5 2 C/R No instruction records for the Transaction [[ID]].
406 REJ 5 N/A C/R Instruction record is cash only.
407 REJ 5 4 C/R Invalid security.
408 REJ 5 N/A C/R Custom add component rejected.
409 REJ 5 5 C/R Component quantity is invalid. 
410 REJ 5 N/A C/R SI Only = Yes. Reject 05 record.
411 REJ 4 N/A PCF [[ETF]] agent does not have any relationships set up and 
submitted LIST in the distribution record.
412 REJ 4 N/A PCF There were no valid distribution records (record type 4) 
found. The distribution records submitted were rejected.
413 REJ 4 3 PCF Portfolio [[ID]] specified on the distribution record does not 
match the portfolio [[ID]] specified on the portfolio record 
(on record type 2).
414 REJ 4 N/A PCF [[NSCC]] Portfolio [[ID]] is invalid.
415 REJ 1 N/A Both File header is invalid.
416 REJ N/A N/A Both File received too late.
418 REJ 4 3 PCF All or List is not valid for the Negotiated basket. 
419 REJ 4 N/A PCF More than one Custom record for the Negotiated 
basket. 
420 WARN 2 N/A PCF No valid distribution record for the Negotiated basket. 
421 WARN 2 N/A PCF Only one custom record is required for the Negotiated 
basket. 
422 REJ 5 N/A PCF Updates to the subscriber are not allowed for the 
Negotiated portfolio.
434 REJ 4 3 PCF Unknown assignees (recipient of custom portfolio) on 
custom record.
437 WARN 4 N/A PCF There were one or more invalid distribution records 
submitted.
500 REJ 5 N/A PCF Portfolio header is missing from the Negotiated basket 
record.
501 REJ 5 N/A PCF Negotiated record missing for negotiated portfolio.
505 REJ 5 3 PCF Transaction [[ID]]  is not numeric.
506 REJ 5 3 PCF Transaction [[ID]] cannot be zero.
507 REJ 5 4 PCF Trade Date is invalid.
508 REJ 5 4 PCF Trade Date cannot be before T-2.
509 REJ 5 4 PCF Trade Date cannot be in the future.
510 REJ 5 N/A PCF Negotiated basket received too late.
512 REJ 5 N/A PCF No valid negotiated records.
514 REJ 5 2 PCF [[NSCC]] Portfolio [[ID]] is invalid.
ETFMessageCodes

---

## Page 9

MessageCodesandDescriptions 9
Message 
Code
Message 
Type 
Record 
Type
Field File 
Type
Message Description
515 REJ 5 N/A PCF File header is invalid.
516 REJ 5 N/A PCF File was received too late.
517 REJ 5 3 PCF Transaction [[ID]] was not provided.
518 REJ 5 1 PCF Invalid record type for the basket.
525 REJ 3 and 5 N/A C/R Missing instruction record.
531 REJ 5 3 PCF Update on the As Of Negotiated basket is not allowed.
537 REJ 5 N/A PCF More than one negotiated record.
541 REJ 2 10 C/R Extended [[settlement]] invalid for the Standard portfolio 
with Fixed Income components. 
542 WARN 5 6 C/R Accrued interest is invalid.
567 REJ 5 N/A PCF Cash only negotiated basket.
581 INFO 5 3 PCF Rejected transaction [[ID]] reprocessed.
582 REJ 5 N/A PCF Negotiated basket not Create/Redeem eligible.
600 WARN 2 N/A PCF All components are provisionally accepted.
601 WARN 2 N/A PCF One or more component is provisionally accepted.
602 REJ 3 and 5 4 C/R One or more components are not in the security master 
database (SMD). 
603 REJ 5 N/A C/R Order with baby [[Bonds]] not eligible for clearance. 
915 REJ 1 N/A C/R File header is invalid.
916 REJ N/A N/A C/R File received too late.
935 WARN 99 N/A Both No Trailer Record found.
937 WARN 99 3 Both Record count is not numeric.
938 WARN 99 N/A C/R Number of records send did not match the number of 
records received.
939 WARN 99 N/A PCF Additional records found after the trailer record were not 
processed.
998 REJ 99 N/A PCF PCF file was received too late and was rejected.
999 REJ 99 N/A Both Received one or more invalid records.
ETFMessageCodes

---

## Page 10

FOR MORE INFORMATION
Email [[DTCC]] Learning at:
CoreLearning@[[DTCC]].com
or visit us on the web at:
www.dtcclearning.com