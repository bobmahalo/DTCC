A Deliver Order (DO) is a [[Book-entry]] movement of [[shares]] of a particular security between two [[DTC]] [[Participant]]s. The delivery program allows you to settle [[Securities]] transactions by making book entry deliveries to another participant's account. The securities are [[immobilized]] in DTC's [[Custody]], eliminating the need for physical movement of [[Physical Securities Certificates]]. DTC reduces the deliverer’s position and increases the receiver’s position without the need to move physical certificates. Deliveries can be made with or without the condition of money payment, depending on your delivery instructions. Once you enter a deliver order, it is routed for processing unless you have established secondary approval.

## What does Submitting a Deliver Order to DTC Do?

This function allows you to input instructions to deliver securities from your account to another DTC participant via book-entry. Submitting a DO does the following:

- Checks if you have a secondary transaction approval profile in place for the delivery and routes accordingly

- Adds the delivery to the receiver’s Receiver Authorized Delivery (RAD) queue as applicable

- Adds the delivery to the Money Market Instrument (MMI) Issuance queue awaiting issuance of the MMI item (turnaround DO's only).

- Validates the delivery against risk management controls

- Validates the delivery against net position in your general free account

- Reduces your general free account if the position is available, pends the transaction if the position is not available, or drops the transaction if the position is not available and Prevent Pend was requested

- Increases the receiving Participant's general free account

- Updates the settlement (dollar) amounts accordingly

- Supports straight-through processing of Depositary Receipt cancellations/release of ordinary shares by using a valid reason code.



