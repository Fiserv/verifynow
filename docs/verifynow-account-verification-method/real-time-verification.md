## Real-Time (using FI login) Verification

VerifyNow is pre-integrated to AllData Aggregation to provide real-time bank account ownership verification for users with online/mobile banking accounts. The user verifies their account in seconds by authenticating with their Financial Institution and consenting to share data for account verification via the log-in flow.

VerifyNow performs real-time account verification by comparing the user's first and last name and/or business name (and account number if applicable) with data collected from the financial institution that services the account. Ownership verification is completed using a robust proprietary, real-time name and account number matching service.

If account details are not passed in the request, user will be requested to add accounts found by Real Time Verification flow.

For clients that require access to the data collected from the financial institution for internal decisioning, analysis, or additional services, clients may choose to integrate to [AllData® Aggregation](/product/AllDataAggregation?branch=develop) directly in conjunction with VerifyNow for passive [Instant Verification](?path=docs/verifynow-account-verification-method/instant-verification.md).

The step-by-step instructions for user and account verification flow with Real-Time Verification and Addition (OAuth enabled) are shown in [Automated Account Addition](?path=docs/automated-account-additions.md) and Real-Time Verification in [Add Account Manually](?path=docs/add-account-manually.md).

Below sequence diagrams represent Real-Time Verification flows.

<center>

![Images](../../assets/images/VN%20diagram.png)

</center>

## See Also

[Instant (Database) Verification](?path=docs/verifynow-account-verification-method/instant-verification.md)
</br>
[Trial Deposit Verification](?path=docs/verifynow-account-verification-method/trial-deposit-verification.md)


<div class="debit-card-button-container">
<div class="debit-card-left-button">
<a href="?path=docs/verifynow-account-verification-method/real-time-verification.md">Back</a>
</div>
<div class="debit-card-right-button"><a href="?path=docs/verifynow-account-verification-method/trial-deposit-verification.md">Next</a></div>
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