CCF-II (Computer-to-Computer Facility II)

- **An updated version:** CCF-II is a newer file format that uses a different record structure compared to the original CCF.
- **Header and trailer records:** CCF-II files include both a header and a trailer record, which bookend the detailed records. This newer structure provides more robust data integrity checks.
- **Coexistence with CCF:** DTCC supports both CCF and CCF-II, and participants can use either format to access various functions, including the Branch Deposit Services Securities Information Center (BDSSIC) and Collateral Loan Closing Balances (COLOAN).

DTCC and its subsidiaries use these transmission protocols to facilitate the post-trade clearing and settlement process. While modern interfaces, such as web applications and APIs, are now widely used, DTCC continues to support legacy formats like CCF for participants who have integrated their back-end systems using these older formats.

Using these systems, participants can send and receive files containing data related to: 

- **Trade confirmations:** Records of matched and compared trades.
- **Settlement balances:** Daily reports detailing net money obligations (debits or credits) at the end of the day.
- **Position records:** Information on securities movements, such as deposits and withdrawals.
- **Corporate actions:** Notifications about corporate action events, such as dividend payments and reorganizations.