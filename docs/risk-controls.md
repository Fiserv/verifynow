
# Risk Controls

Clients can set reuse limits to mitigate the risk associated with reusing accounts. Prior to processing an account verification request, VerifyNow determines whether the new account violates any of the risk controls and returns a failure message if they do.

A. Clients can configure the following reuse limits: 

<div class="collapsible-container">
<div>
    <input type="checkbox" class="collapsible-checkbox" id="section1">
    <label class="label-expand" for="section1">Number of distinct users that can use the same account.</label>
    <div class="content-expand">
        <div class="content-body">
          <div class="content-left">
          a. The default is 2.<br>
          b. In the case of a joint account, each account holder counts as one user.<br>
          c. The count changes when a user is added and when a user is removed in the following situations:
        <div class="card-body">
        <ul>
        <li>All of a user’s profiles show the same account as deleted </li>
        <li>A user unsubscribes</li>
        </ul>
        </div>
        </div>
        </div>
        </div>
        </br>
    <input type="checkbox" class="collapsible-checkbox" id="section2">
    <label class="label-expand" for="section2">Number of profiles to which a user can add the same account.</label>
    <div class="content-expand">
        <div class="content-body">
        <div class="content-left">
        a. The default is 2.<br>
        b. In the case of a joint account, each account holder counts as one user.<br>
        c. The count changes when an account is added to a profile and removed in the following situations: 
        <div class="card-body">
        <ul>
        <li>An account is deleted from a profile </li>
        <li>A profile is unsubscribed
        </li>
        </ul>
        </div>
        </div>
    </div>
    </div> </br>
    <input type="checkbox" class="collapsible-checkbox" id="section3">
    <label class="label-expand" for="section3">Number of times the same account can be added to and deleted from a profile.</label>
    <div class="content-expand">
        <div class="content-body">
        <div class="content-left">
            a. The default is 3.<br>
            b. The number of trial deposit attempts carries the same limit. <br>
            c. Clients can change trial deposit limits at the user level for a particular account.
        </div>
    </div>
    </div> </br>
    <input type="checkbox" class="collapsible-checkbox" id="section4">
    <label class="label-expand" for="section4">Number of accounts that can be active for a profile.</label>
    <div class="content-expand">
        <div class="content-body">
        <div class="content-left">
            a. No default value <br>
            b. The count changes when an account is added to a profile and removed in the following situations:
        <div class="card-body">
        <ul>
        <li>An account is deleted from a profile </li>
        <li>A profile is unsubscribed
        </li>
        </ul>
        </div>
        </div>
    </div>
    </div>   
</div>
</div>
</br>
        
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
            
 





   