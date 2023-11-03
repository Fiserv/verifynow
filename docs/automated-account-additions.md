## Automated Account Addition

For eligible FIs, VerifyNow allows user to add accounts without providing information such as routing or account numbers. Instead, they may use Real-Time Verification and Addition, as described below.

#### When the Automated Account Flow is Triggered

The following flow is applicable when:
<div class="card-body">
<ul>
<li>Client has enabled RTVA via the DGF</li>

<li>Account and Routing Number are NOT passed in the API invoking the widget</li>

<li>RTVA is not FALSE in the API. Please see the <a href="../docs/?path=docs/verifynow-integration-guide.md">VerifyNow Integration Guide</a> for more details.</li>
</ul>
</div>


&nbsp;

<!-- theme: info -->
 
>**Note** <br/><br/>Even when RTVA is enabled, users can choose to add any account manually.

### See Also

[Add Account Manually](?path=docs/add-account-manually)<br/>
[Real-Time Verification and Addition](?path=docs/realtime-verification-additions.md)
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