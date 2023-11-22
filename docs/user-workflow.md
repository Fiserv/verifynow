# User workflow

<!-- type: tab -->
## New User

The workflow for creating a new user is as follows:

1.	The client system collects information from the user and sends it to VerifyNow.
2.	VerifyNow receives user information from the client system and performs two checks:

    <div class="card-body">
        <ul>
            <li>Data validation check:  If the data is valid, the process can continue to the next step. If the data is invalid, VerifyNow sends an SSO error back to the client system.</li>
            <li>User identity check: If the user is new, the process can continue to the next step. If the user is an existing user, VerifyNow checks the state to which the user must be returned. <a href="#tab-returning_user" >Returning User</a></li>
        </ul>
    </div>
&nbsp;

3.	If the user is new, VerifyNow creates a new user. If the user is an existing user, VerifyNow triggers the existing user workflow.

<center>

![image](../assets/images/user-workflow-flowchart.png)

&nbsp;

</center>

<!-- type: tab -->

## Returning User

For returning users (i.e., users who begin the verification process, leave, and then return to complete the process), the following scenarios would apply:

### Partners Using RTVA, RTV, Instant, and Trial Deposit

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

### Partners Using RTV, Instant, and Trial Deposit

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

### Partners Using Instant and Trial Deposit

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
</style>