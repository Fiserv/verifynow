## CSS Integration

VerifyNow uses a set of styles for the widget. These styles are defined by Fiserv and will be hosted either by Fiserv or by the client application. Clients will have the option to modify these styles according to their standards.

<div class="card-body">
<ul>
<li>If a client hosts the CSS, the Fiserv project/account manager will provide the base set of styles to the client to incorporate them into their CSS and provide the hosted URL to Fiserv to seed them as part of the product configuration.</li>

<li>If Fiserv is hosting, Fiserv will create a CSS file and point to it in the widget section.</li>
</ul>
</div>


## See Also
[Automated Account Addition](?path=docs/automated-account-additions.md)</br>
[Add Account Manually](?path=docs/add-account-manually.md)</br>
[User workflow](?path=docs/user-workflow.md)</br>
[Account Verification status/Exit points](?path=docs/account-verification-status.md)</br>

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
