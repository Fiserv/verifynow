
# Risk Controls

Clients can set reuse limits to mitigate the risk associated with reusing accounts. Prior to processing an account verification request, VerifyNow determines whether the new account violates any of the risk controls and returns a failure message if they do.

A. Clients can configure account reuse limits via back office tool  - Compass. 
        
B. A unique combination of Last Name, Social Security Number, and Date of Birth identify each user.

C. A unique combination of routing number, account number, and account type identify each account. 

D. Clients can submit a written request to Fiserv ePayments Customer Support to change reuse limits.


## See Also
[VerifyNow - Account Verification Methods](?path=docs/verifynow-account-verification-method.md)<br/>

<style>
    .card-body ul {
        list-style: none;
        padding-left: 20px;
    }
    .card-body ul li::before {
        content: "\2022";
        font-size: 1.5em;
        color: #f60;
        display: inline-block;
        width: 1em;
        margin-left: -1em;
    }
    .collapsible-container {
        width: 100%;
    }

    .collapsible-checkbox {
        display: none;
    }

    .label-expand {
        background-color: #777;
        color: white;
        cursor: pointer;
        padding: 18px;
        width: 100%;
        border: none;
        text-align: left;
        outline: none;
        font-size: 15px;
        display: block;
        position: relative;
    }
   .label-expand::after{
        content: '+';
        font-size: 22px;
        font-weight: bold;
        position: absolute;
        right: 12px;
        top: 8px;
    }
    input:checked + label::after {
        content: '-';
        font-size: 22px;
        right: 14px;
        top: 8px;
    }

    .collapsible-checkbox:checked+.label-expand {
        background-color: #555;
    }

    .content-expand {
        padding: 0 18px;
        display: none;
        overflow: hidden;
        background-color: #f1f1f1;
    }

    .collapsible-checkbox:checked+.label-expand+.content-expand {
        display: block;
    }

    .block-quote {
        padding: 1em;
        color: #6a737d;
        border-left: 0.375em solid #40a9ff;
        background: #e6f7ff;
        border-radius: 3px;
    }

    .content-left {
        width: 100%
    }

    .image-otp {
        width: 40%
    }

    .content-body {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 20px;
    }

    .image-center {
      display: block;
      margin-left: auto;
      margin-right: auto;
      width: 70%;
    }
    
    .card-body {
        margin: 20px;
    }
    .card-body ul {
        list-style: none;
        padding-left: 20px;
    }
    .card-body ul li::before {
        content: "\2022";
        font-size: 1em;
        color: #f60;
        display: inline-block;
        width: 1em;
        margin-left: -1em;
    }
</style>
            
 





   