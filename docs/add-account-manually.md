## Add Account Manually

The Add account manually flow uses a pre-defined waterfall of verification methods based on what verification methods are enabled for the client. The verification waterfall begins with Instant Verification followed by Real Time Verification (when the financial institution is eligible), then/or Trial Deposits.

<center>

 <img width="750" height="250" src="https://raw.githubusercontent.com/Fiserv/verifynow/develop/assets/images/rtv-processflow.png">

</center>

### When the Add Account Manually Flow is Triggered

The following flow is applicable when:
<div class="card-body">
<ul>
<li>Client has disabled RTVA or Account and Routing Number are passed in the API invoking the widget, or
User has selected “Add Account Manually” within the Automated Add Account flow. </li>
</ul>
</div>

### Step-by-Step Instruction for Add Account Manually Flow

1.	<b>Instant (Database) Verification</b> </br>
<div class="card-body" style="margin-left:30px">
<ul>
<li>
 The client system collects account information from the user prior to initiating the widget. The client system passes the information collected from the user to VerifyNow.
 </li>
 </ul>
 </div>

<center>
<img width="550" height="250" src="https://raw.githubusercontent.com/Fiserv/verifynow/develop/assets/images/addexternal-account.png"/>

</center>
                         
<div class="card-body" style="margin-left:30px">
<ul>
<li>
	Instant Verification will be attempted first when enabled and Instant Verification in progress screen is displayed 
        </li></ul></div>
<center>

<img width="550" height="250" src="https://raw.githubusercontent.com/Fiserv/verifynow/develop/assets/images/inprogress-screen.png"/>

</center>

<div class="card-body" style="margin-left:30px">
<ul>
<li>
If Instant Verification is inconclusive, VerifyNow offers the user the option to select the Real-time verification method or the Trial Deposit verification method.
</li></ul></div>

2.	<b>Real Time Verification</b>
<div class="card-body" style="margin-left:30px">
        <ul>
        <li>The user is asked to provide their username and password for the online banking portal where the user accesses their account or is given an option to manually verify using Trial Deposits</li>
        </ul>
        </div>
</br>
<center>

<img width="550" height="250" src="https://raw.githubusercontent.com/Fiserv/verifynow/develop/assets/images/transferfund-externalaccount.png">

</center>
</br>
        <div class="card-body" style="margin-left:30px">
        <ul>
        <li>If the user is verified, VerifyNow displays the Real-time verification in-progress screen to the user.</li>
        </ul>
        </div>

<center>

<img width="500" height="180" src="https://raw.githubusercontent.com/Fiserv/verifynow/develop/assets/images/checkingverification.png">

</center>
</br>   
        <div class="card-body" style="margin-left:30px">
        <ul>
        <li>Real-time verification is completed.</li>
        <li>VerifyNow passes control back to the client system, along with the verification decision.</li>
        <li>If the user is not approved, VerifyNow checks if the Trial Deposit verification method is available, and if available, gives the user the option to use Trial Deposit verification.</li>
        </ul>
        </div>
3.<b>Trial Deposit Verification</b>
                <div class="card-body" style="margin-left:30px">
                <ul>
                <li>To use Trial Deposit Verification, the user clicks the Send Me Two Deposits button.</li>
<center>

<img width="540" height="250" src="https://raw.githubusercontent.com/Fiserv/verifynow/develop/assets/images/verify-with-bank-deposit-new.png">

</center>
                <li>The user clicks the Done button to complete the process.</li>
<center>

<img width="550" height="250" src="https://raw.githubusercontent.com/Fiserv/verifynow/develop/assets/images/twodepositpage.png">

</center>
                </ul>
                </div>

</br>

## See Also
[Automated Account Addition](?path=docs/automated-account-additions.md)</br>
[User workflow](?path=docs/user-workflow.md)</br>
[Account Verification status/Exit points](?path=docs/account-verification-status.md)</br>
[CSS Integration](?path=docs/css-integration.md)

 <style>
    .card-body ul {
        list-style: none;
        padding-left: 20px;
    }
    .card-body ul li::before {
        content: "\2022";
        font-size: 1.0em;
        color: #f60;
        display: inline-block;
        width: 1em;
        margin-left: -1em;
    }
</style>