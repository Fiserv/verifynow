## Automated Account Addition

For eligible FIs, VerifyNow allows user to add accounts without providing information such as routing or account numbers. Instead, they may use Real-Time Verification and Addition, as described below.

## Real-Time Verification and Addition (RTVA)

When a user tries to add an account for the FI via RTVA, they provide credentials for logging into the external FI. The user is put through Multi-Factor Authentication (MFA). Then account-related information is successfully scraped and the name is passed through risk rules for matching logic to determine whether or not the accounts should be displayed to the user. If the information fails the check, the user is sent to add the account manually (see [Add Account Manually](?path=docs/add-account-manually.md)).

The name that comes in SSO will be compared against the name scraped by Aggregation. Risk rules for name matching determine if the account information should be displayed to the user.

<center>

![image](../assets/images/automated_account_addition.png)

&nbsp;

</center>

## General Steps

Regardless of which verification method is used, the first few steps will be the same.

<h5 style="color:#ff6600">Note:</h5>

All forms of verification will not necessarily be available for all FIs. Users will have access to some or all verification methods, as applicable.

1.	Click the appropriate icon, or type in the search box.

<center>

![image](../assets/images/search-box.png)

&nbsp;

</center>

2.	Here, the user will have the option of adding from their online banking website or adding an account manually.

<center>

![image](../assets/images/add-account-manually1.png)

&nbsp;

</center>

3.  To use Real-Time Verification and Addition, the user will enter the User ID and Password for their bank account and click the Submit button.

<center>

![image](../assets/images/user-login-page.png)

&nbsp;

</center>

4.  User will need to choose to add an account fetched by Real Time Verification from external FI or user can choose to add an account manually if they are not able to find the account

<center>

![image](../assets/images/adding-external-account.png)

&nbsp;

</center>

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
        font-size: 1.1em;
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