## Instant Verification

This method provides instant bank account ownership verification using the Early Warning Services (EWS) account services and/or other available databases.



VerifyNow performs instant account verification using the Customer Information/MICR Match component of a check printer’s database. This service matches the user’s name and the account information with information in the database.
>**Note**<br/><br/>
 The instant account verification service only verifies DDA accounts. Savings, money market, and brokerage accounts are ineligible for account verification via this service.

 &nbsp;
 
>**Note**<br/><br/> The instant account verification service only verifies accounts with RTNs listed in the MICR Table.

Instant verification is performed using the provided customer information and account details and the Early Warning Services (EWS) AOA database. EWS houses data contributed by various financial institutions that it uses to authenticate account ownership claims. EWS data is limited by the number of financial institutions that contribute to the product. EWS requires that clients contribute to the product to be allowed to use it.

<center>

![Images](../../assets/images/instant-verification-process-flow.png)

</center>

<center>

![Images](../../assets/images/instant-verification-sequence.png)

</center>

### Step-by-Step Instruction for Instant Verification
1. The client system collects account information from the user prior to initiating the widget. A sample screen is shown below:

<center>

![Images](../../assets/images/add-account.png)

</center>

2. The client system passes the information collected from the user to VerifyNow.

3. VerifyNow displays the Instant verification in-progress screen to the user as required.

<center>

![Images](../../assets/images/process-image.png)

</center>

4.  Instant verification is completed.

    a. If approved or denied, VerifyNow passes control back to the client system, along with the verification decision.

    b. If account ownership verification is inconclusive, Real-time verification or Trial Deposit verification can be initiated.

## See Also
[Real Time Verification](?path=docs/verify-accounts-using-verifynow/real-time-verification.md)<br/>
[Trial Deposit Verification](?path=docs/verify-accounts-using-verifynow/trial-deposit-verification.md)<br/>
[Exit Points](?path=docs/exit-points.md)<br/>
[Account Verification Status](?path=docs/account-verification-status.md)<br/>
[Risk Controls](?path=docs/risk-controls.md)<br/>