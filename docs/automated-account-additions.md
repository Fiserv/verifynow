## Automated Account Addition

For eligible FIs, VerifyNow allows user to add accounts without providing information such as routing or account numbers. Instead, they may use Real-Time Verification and Addition, as described below.

<center>

![image](../assets/images/automated-account-flow.png)

&nbsp;

</center>


#### When the Automated Account Flow is Triggered

The following flow is applicable when:
<div class="card-body">
<ul>
<li>Client has enabled RTVA via the DGF</li>

<center>

<img src="https://raw.githubusercontent.com/Fiserv/VerifyNow/develop/assets/images/RTVA-enabled.png">

&nbsp;

</center>

<li>Account and Routing Number are NOT passed in the API invoking the widget</li>

<li>RTVA is not FALSE in the API.</li>
</ul>
</div>


&nbsp;

<!-- theme: info -->
 
>**Note** <br/><br/>Even when RTVA is enabled, users can choose to add any account manually.


When a user tries to add an account for the FI via RTVA, they provide credentials for logging into the external FI. The user is put through Multi-Factor Authentication (MFA). Then account-related information is successfully scraped, and the name is passed through risk rules for matching logic to determine whether the accounts should be displayed to the user or not. If the information fails the check, the user is sent to add the account manually (see [Add Account Manually](?path=docs/add-account-manually.md)).

The name that comes in SSO will be compared against the name scraped by Aggregation. Risk rules for name matching determine if the account information should be displayed to the user.

<div>
    <input type="checkbox" class="collapsible-checkbox" id="section1">
    <label class="label-expand" for="section1">Automated Account Addition Flow for Oath Users</label>
    <div class="content-expand">

&nbsp;

<!-- theme: info -->
 
>**Note** <br/><br/>The following steps are applicable to Financial Institutions that is Oath Enabled.

<center>

![image](../assets/images/oauth-enabled.png)

&nbsp;

</center>

1.	Click the appropriate icon, or type in the search box to choose the Financial Institution.

<div class="card-container">
        <div style="margin: 5px">
            <img src="https://raw.githubusercontent.com/Fiserv/VerifyNow/develop/assets/images/bank-list.png">
        </div>
        <div style="margin: 5px">
            <img src="https://raw.githubusercontent.com/Fiserv/VerifyNow/develop/assets/images/bank-search.png">
        </div>
</div>

2.	Once the respective financial institution is selected, the user will be navigated to the Oath authentication screen.

<center>

![Images](../assets/images/verify-instantly.png =300x300)

&nbsp;

</center>

3.	Click Authenticate.

4.	Enter the login credentials to sign-in.

<center>

![Images](../assets/images/fiserv-login.png =300x300)

&nbsp;

</center>

5.	Then the user is navigated to the multifactor authentication screen.

<center>

![Images](../assets/images/MFA.png =300x150)

&nbsp;

</center>

6.	Once the details are added, click Submit.

7.	Select the account in the Consent Page. 

<center>

![Images](../assets/images/consent-page.png =300x150)

&nbsp;

</center>

8.	Click Authorize.

9.	Pop-up screen appears as shown below.

<center>

![Images](../assets/images/window-autoclose-page.png =300x150)

&nbsp;

</center>

10.	Once the user successfully authenticates with the financial institution, they will need to choose which account(s) to add.

<center>

![Images](../assets/images/selecting-account-page.png =300x150)

&nbsp;

</center>

11.	Clicking the Add button will complete the verification flow.

    <div class="card-body">
    <ul>
    <li>Selecting “Add your account manually” will take the user to the add account manually flow. </li>
    </ul>
    </div>

</div>
</div>
</br>
<div>
    <input type="checkbox" class="collapsible-checkbox" id="section2">
    <label class="label-expand" for="section2">Automated Account Addition Flow for Non-Oath Users</label>
    <div class="content-expand">

&nbsp;

<!-- theme: info -->
 
>**Note** <br/><br/>The following steps are applicable to Financial Institutions that are not Oath Enabled.

<center>

![image](../assets/images/non-oauth-enabled.png)
&nbsp;

</center>

1.	Click the appropriate icon, or type in the search box to choose the Financial Institution.    

    <div class="card-container">
        <div style="margin: 5px">
            <img src="https://raw.githubusercontent.com/Fiserv/VerifyNow/develop/assets/images/bank-list.png">
        </div>
        <div style="margin: 5px">
            <img src="https://raw.githubusercontent.com/Fiserv/VerifyNow/develop/assets/images/bank-search.png">
        </div>
    </div>

2.	Here, the user will have the option of adding from their online banking website or adding an account manually.

<center>

![Images](../assets/images/add-account-manually.png =300x250)
&nbsp;

</center>

<div class="card-body">
        <ul>
            <li>To use Real-Time Verification and Addition, the user will enter the User ID and Password for their bank account and click the Submit button. </li>
            <li>To add an account manually, the user will click the Add Account Manually button. </li>
        </ul>
</div>

3.	Once the user successfully authenticates with the financial institution, they will need to choose which account(s) to add.

<center>

![Images](../assets/images/choose-bank-account.png =300x150)

&nbsp;

</center>

4.	Clicking the Add button will complete the verification flow.

    a.	Selecting “Add your account manually” will take the user to the add account manually flow.

</div>
</div>

### See Also

[Add Account Manually](?path=docs/add-account-manually.md)</br>
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
        font-size: 1.5em;
        color: #f60;
        display: inline-block;
        width: 1em;
        margin-left: -1em;
    }
    .card-container {
            display: flex;
            justify-content: space-between;
        }
        .card {
            border: 1px solid black;
            border-radius: 8px;
            margin: 5px;
            display: flex;
            flex-direction: column;
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