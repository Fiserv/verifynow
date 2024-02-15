## Trial Deposit Verification

This method verifies customer’s access to an external bank account. Two small trial deposits and one trial debit (ACH Micro-Entries) are made to the external bank account and the customer is required to verify the two deposit amounts.  

> :memo: _**Note:** <br/>The amount of the debit is equal to the sum of the two deposits._

Shown below is an example of how Trial Deposit Verification works.

1. On Monday, VerifyNow makes two trial deposits and a trial debit to the funding account via ACH. 

2. On Tuesday, VerifyNow receives confirmation that the trial deposits/debit were made and then sends an e-mail message to the applicant, notifying them to look for the deposit amounts in the funding account and to return to the system to confirm the deposit amounts. 

3. On Wednesday, the applicant returns to the system and enters the deposit amounts. If the amounts reported by the applicant match the VerifyNow deposits, the applicant’s account ownership is verified.


> :memo: _**Note:** <br/>Trial deposit verification involves a minimum of two interactions from the client to the Fiserv VerifyNow system._

<center>

![Images](../../assets/images/td-sequence1.png)

<b>Trial Deposit Initiate Sequence</b>
</center>


<center>

![Images](../../assets/images/td-sequence2.png)

<b>Trial Deposit Verification Sequence</b>

</center>

## See Also
[Instant (Database) Verification](?path=docs/verifynow-account-verification-method/instant-verification.md)</br>
[Real-Time (using FI login) Verification](?path=docs/verifynow-account-verification-method/real-time-verification.md)

<div class="debit-card-button-container">
<div class="debit-card-left-button">
<a href="?path=docs/verifynow-account-verification-method.md">Back</a>
</div>
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
        right: 0;
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


