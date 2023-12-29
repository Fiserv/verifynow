# User workflow

<!-- 
type: tab 
titles: New User,Returning User
-->
## New User

The workflow for creating a new user is as follows:

1.	The client system collects information from the user and sends it to VerifyNow.
2.	VerifyNow receives user information from the client system and performs two checks:

    <div class="card-body">
        <ul>
            <li>Data validation check:  If the data is valid, the process can continue to the next step. If the data is invalid, VerifyNow sends an SSO error back to the client system.</li>
            <li>User identity check: If the user is new, the process can continue to the next step. If the user is an existing user, VerifyNow checks the state to which the user must be returned. See, <a href="#tab-returning_user" >Returning User</a></li>
        </ul>
    </div> &nbsp;
3.	If the user is new, VerifyNow creates a new user. If the user is an existing user, VerifyNow triggers the existing user workflow.

<center>

![image](../assets/images/user-workflow-flowchart.png)

&nbsp;

</center>

<!-- type: tab -->

## Returning User

For returning users (i.e., users who begin the verification process, leave, and then return to complete the process), the following scenarios would apply:

<div>
    <input type="checkbox" class="collapsible-checkbox" id="section1">
    <label class="label-expand" for="section1">Partners Using RTVA, RTV, Instant, and Trial Deposit</label>
    <div class="content-expand">
        When an account is present in SSO and in Compass:

<div class="card-body" style="padding-left:40px;">
            <ul>
                <li>If verification status is In Progress, the user is returned to the last page visited.</li>
                <li>If verification status is Approved, the user is returned to re-verify the account.</li>
            </ul>
        </div>
        When an account is present in SSO but absent in Compass:

<div class="card-body" style="padding-left:40px;">
            <ul>
                <li>If verification status is Not Applicable, the user is returned to the beginning of Account Verification.</li>
            </ul>
        </div>
        When an account is absent in SSO and but present in Compass:

<div class="card-body" style="padding-left:40px;">
            <ul>
                <li>If verification status is Approved, the user is returned to the RTVA page to re-start the process.</li>
                <li>If verification status is Not Applicable, the user is returned to the RTVA page to re-start the process.</li>
            </ul>
        </div>

When an account is absent in SSO and in Compass:

<div class="card-body" style="padding-left:40px;">
            <ul>
                <li>If verification status is Not Applicable, the user is returned to the RTVA page to re-start the process.</li>
            </ul>
        </div>
    </div>
    </div>
</br>
<div>
    <input type="checkbox" class="collapsible-checkbox" id="section2">
    <label class="label-expand" for="section2">Partners Using RTV, Instant, and Trial Deposit</label>
    <div class="content-expand">
    When an account is present in SSO and in Compass:

<div class="card-body" style="padding-left:40px;">
            <ul>
                <li>If verification status is In Progress, the user is returned to the last page visited.</li>
                <li>If verification status is Approved, the user is returned to re-verify the account.</li>
            </ul>
        </div>

When an account is present in SSO but absent in Compass:

<div class="card-body" style="padding-left:40px;">
            <ul>
                <li>If verification status is Not Applicable, the user is returned to the beginning of Account Verification.</li>
            </ul>
        </div>

When an account is absent in SSO and but present in Compass:

<div class="card-body" style="padding-left:40px;">
            <ul>
                <li>If verification status is In Progress, the user is returned to the Manual Account Addition page to re-start the process.</li>
            </ul>
        </div>

When an account is absent in SSO and in Compass:

<div class="card-body" style="padding-left:40px;">
            <ul>
                <li>If verification status is Approved, the user is returned to the Manual Account Addition page to re-start the process.</li>
                <li>If verification status is Not Applicable, the user is returned to the Manual Account Addition page to re-start the process.</li>
            </ul>
        </div>
        
</div>
</div>
</br>

<div>
    <input type="checkbox" class="collapsible-checkbox" id="section3">
    <label class="label-expand" for="section3">Partners Using Instant and Trial Deposit</label>
    <div class="content-expand">
    When an account is present in SSO and in Compass:

<div class="card-body" style="padding-left:40px;">
            <ul>
                <li>If verification status is In Progress, the user is returned to the last page visited.</li>
                <li>If verification status is Approved, the user is returned to re-verify the account.</li>
            </ul>
        </div>

When an account is present in SSO but absent in Compass:

<div class="card-body" style="padding-left:40px;">
            <ul>
                <li>If verification status is Not Applicable, the user is returned to the beginning of Account Verification.</li>
            </ul>
        </div>

When an account is absent in SSO and but present in Compass:

<div class="card-body" style="padding-left:40px;">
            <ul>
                <li>If verification status is Approved, the user is returned to the Manual Account Addition page to re-start the process.</li>
                <li>If verification status is In Progress, the user is returned to the Manual Account Addition page to re-start the process.</li>
            </ul>
        </div>

When an account is absent in SSO and in Compass:

<div class="card-body" style="padding-left:40px;">
            <ul>
                <li>If verification status is Not Applicable, the user is returned to the Manual Account Addition page to re-start the process.</li>
            </ul>
        </div>

        
</div>
</div>

<!-- type: tab-end -->

## See Also
[Automated Account Addition](?path=docs/automated-account-additions.md)</br>
[Add Account Manually](?path=docs/add-account-manually.md)</br>
[Account Verification status/Exit points](?path=docs/account-verification-status.md)</br>
[CSS Integration](?path=docs/css-integration.md)

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
        width: 50%
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
</style>