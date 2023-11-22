
# Widget Flow

The VerifyNow widget works like the VerifyNow APIs, but it reduces the complexity and therefore requires lesser resources involved in implementation. 

VerifyNow integration requires clients to perform three steps as outlined below for Widget based Integration.


1.	Invoke the Fiserv VerifyNow REST web service’s Verify operation to receive a unique token.

2.	Render the Fiserv widget as part of the client’s application user interface by using the unique token.

3.	Invoke the Fiserv VerifyNow web service’s Outcome operation to receive the verification decision after the widget gives control back to the client.


### How to Integrate VerifyNow Widget?

## Verify
The client application invokes the VerifyNow web service’s Verify operation with the expected elements for profile and account information. The client application receives a token and the status of the request from the VerifyNow system. The token will not be passed to the client application if there is any failure in processing the data received, such as failure in data validation and/or business-related validation. For more information, see [API Flow](?path=docs/api-flow.md).

## Widget Integration
The client is required to comply with the following integration points to use the Fiserv widget in their application’s user interface.

### JavaScript

The client’s application user interface to support the widget is required to include the following script hosted by the VerifyNow system. The widget takes care of all user interface level processing and data validation. Processing control will be given back to the client’s application by a JavaScript API call.

```
<script type="text/javascript" src="<Domain>/js/cashedge/navgra/verifynow/vnClient.js ?homeId=<FI_HOME_ID>"></script>
```

The Fiserv Client Manager will provide the value of FI_HOME_ID to the client at the time of onboarding.

### Hidden Variables

The client’s application user interface is expected to have the following hidden variables with the appropriate values for the expected functional flow. Samples are included after the variable descriptions.
<div class="card-body">
<ul>
<li><i>pidString</i> – Used for authentication and to refer to which user-specific account needs to be considered for verification. The value for this should be the token received from the Verify operation.</li>
<li><i>verifyOption</i> – Used to hold the value that identifies whether the verification call is new or for re-verification (user and account combination) for the account. Possible values for this variable could be “‘REVERIFY”’ or any other string. If the value is “REVERIFY”, the VerifyNow system will consider this to be a re-verification; otherwise, it will be considered a new verification call.</li>
<li><i>klURL</i> – Used keep the customer’s session alive in the client application.</li>
<li><i>cssURL</i> – Used to pass the client-hosted cssURL. This is required only when the client hosts the CSS.</li>
</ul>
</div>

### Samples
```
<input type="hidden" name="pidString" id="pidString" value="CE02#4#TNiA3Qj"/>

<input type="hidden" name="verifyOption" id="verifyOption" value="REVERIFY"/>

<input type="hidden" name="verifyOption" id="verifyOption" value=""/>

<input type="hidden" name="klURL" id="klURL" value="<<clientHostedURL>>"/> 

<input type="hidden" name="cssURL" id="cssURL" value="<<clientHostedCSS>>"/>

```

## Widget Placement

The client’s application is required to provide the expected space in their user interface to place the VerifyNow widget. This needs to happen through use of the `<div>` tag with the predefined ID (<b>vn_space</b>) associated with it. A sample could appear as:

```
<div id="vn_space" style="align:center; margin:5px; width:100%" align="center"> </div>
```

## Control Handover to Client Application

Application control will be transferred back to the client’s application from the VerifyNow system through a JavaScript API call hosted by the client application. Clients can incorporate their business flow inside of it. 
```
function onVnVerificationComplete(JSonResponse){

alert("UI Control is handed over to Client");

}
```
## Outcome

The client’s application receives the outcome of the verification through the Outcome operation with the token associated for the specific verification. The Outcome operation provides the detail, including verification types and their respective statuses along with the combined decision. Refer to the  [API Flow](?path=docs/api-flow.md) for more information.

## See Also
[Automated Account Addition](?path=docs/automated-account-additions.md)</br>
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
</style>


