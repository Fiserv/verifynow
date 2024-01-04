## Instant (Risk Database) Verification

This method provides instant bank account ownership verification using the Early Warning Services (EWS) account services and/or other available databases.

VerifyNow performs instant account verification using the Customer Information/Magnetic Ink Character Recognition (MICR) Match component of a check printer’s database. This service matches the user’s name and the account information with information in the database.

 > :memo: _**Note:** <br/>The instant account verification service only verifies Demand Deposit Account (DDA) accounts. Savings, money market, and brokerage accounts are ineligible for account verification via this service._

 &nbsp;
 
> :memo: _**Note:** <br/>The instant account verification service only verifies accounts with Routing Transit Number  (RTN)s listed in the MICR Table._

Instant verification is performed using the provided customer information and account details and the Early Warning Services (EWS) Account Ownership Authentication(AOA) database. EWS houses data contributed by various financial institutions with data elements including account holder names, address, tax ID, and additional elements leveraged that it uses to authenticate account ownership claims. EWS data is limited by the number of financial institutions that contribute to the product. EWS requires that clients contribute to the product to be allowed to use it.

<center>

![Images](../../assets/images/instant-verification-process-flow.png)

<b>Instant Verification Process Flow</b>

</center>

<center>

![Images](../../assets/images/instant-verification-sequence.png)

<b>Instant Verification Sequence</b>

</center>

### Step-by-Step Instruction for Instant Verification
1. The client system collects account information from the user prior to initiating the widget. A sample screen is shown below:

<center>

![Images](../../assets/images/add-account.png)

</center>

2. The client system passes the information collected from the user to VerifyNow.

3. VerifyNow displays the Instant verification in-progress screen to the user as required.

<center>

<img width="400" height="150" src="https://raw.githubusercontent.com/Fiserv/VerifyNow/develop/assets/images/process-image.png">

</center>

4.  Instant verification is completed.

    a. If approved or denied, VerifyNow passes control back to the client system, along with the verification decision.

    b. If account ownership verification is inconclusive, Real-time verification or Trial Deposit verification can be initiated.

Click the Next button to see other verification methods.</br>

<div class="debit-card-button-container">
<div class="debit-card-left-button">
<a href="?path=docs/verifynow-account-verification-method.md">Back</a>
</div>
<div class="debit-card-right-button"><a href="?path=docs/verifynow-account-verification-method/real-time-verification.md">Next</a></div>
</div>

<style>
    .debit-card-button-container {
        position: relative;
        width: 100%;
        height: 30px;
        font-family: sans-serif;
        margin: 0px 15px;
    }
    .debit-card-left-button a,
    .debit-card-right-button a{
        position: absolute;
        display: inline;
        border: 0px;
        background: rgb(255, 102, 0);
        color: rgb(255, 255, 255);
        padding: 8px 22px;
        cursor: pointer;
        border-radius: 4px;                                
        text-align: center;
        text-decoration: none;
        transition: all 0.3s ease;
    }
    .debit-card-left-button a{ 
        left: 0;
    }
    .debit-card-right-button a{
        right: 10%;
    }
    .debit-card-left-button a:hover,
    .debit-card-right-button a:hover {
        color: #f60;
        background-color: white;
        border: 2px solid #f60;
    }
    .confirm-button {
        padding: 2px;
        font-weight: bold;
    }
</style>