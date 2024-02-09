## Instant (Database) Verification

This method provides instant bank account ownership or account status verification using the Fiserv proprietary data from FI systems of record / Early Warning Services (EWS) - account services. Clients can use either widget flow or light weight API flow (<a href="../api/?type=post&path=/cashedgerws/verifynow/ping">Refer to API Flow</a>) for Instant Verification.

 > :memo: _**Note:** <br/>The instant account verification service only verifies Demand Deposit Account (DDA) accounts. Savings, money market, and brokerage accounts are ineligible for account verification via this service._

 &nbsp;


<center>

<b>Instant Verification Process Flow (Widget flow)</b>

</center>

<center>

![Images](../../assets/images/instant-verification-sequence.png)

<b>Instant Verification Sequence</b>

</center>


<center>

![Images](../../assets/images/add-account-flow.png)

</center>



<center>

<img width="400" height="150" src="https://raw.githubusercontent.com/Fiserv/VerifyNow/develop/assets/images/process-image-flow.png">

</center>


&nbsp;

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