
# Widget Flow

The VerifyNow widget works like the VerifyNow APIs, but it reduces the complexity and therefore requires lesser resources involved in implementation. 

VerifyNow integration requires clients to perform three steps as outlined below for Widget based Integration.


1.	Invoke the Fiserv VerifyNow REST web service’s Verify operation to receive a unique token.

2.	Render the Fiserv widget as part of the client’s application user interface by using the unique token.

3.	Invoke the Fiserv VerifyNow web service’s Outcome operation to receive the verification decision after the widget gives control back to the client.


### How to Integrate VerifyNow Widget?

<div>
    <input type="checkbox" class="collapsible-checkbox" id="section1">
    <label class="label-expand" for="section1">Verify</label>
    <div class="content-expand">

The client application invokes the VerifyNow web service’s Verify operation with the expected elements for profile and account information. The client application receives a token and the status of the request from the VerifyNow system. The token will not be passed to the client application if there is any failure in processing the data received, such as failure in data validation and/or business-related validation. For more information, see <a href="../docs/?path=docs/api-flow.md">API Flow</a>.
</br>

</div>
</div>
</br>
<div>
    <input type="checkbox" class="collapsible-checkbox" id="section2">
    <label class="label-expand" for="section2">Widget Integration</label>
    <div class="content-expand">
    The client is required to comply with the following integration points to use the Fiserv widget in their application’s user interface.

<h3>JavaScript</h3>

The client’s application user interface to support the widget is required to include the following script hosted by the VerifyNow system. The widget takes care of all user interface level processing and data validation. Processing control will be given back to the client’s application by a JavaScript API call.

```
<script type="text/javascript" src="<Domain>/js/cashedge/navgra/verifynow/vnClient.js ?homeId=<FI_HOME_ID>"></script>
```

The Fiserv Client Manager will provide the value of FI_HOME_ID to the client at the time of onboarding.

<h3>Hidden Variables</h3>

The client’s application user interface is expected to have the following hidden variables with the appropriate values for the expected functional flow. Samples are included after the variable descriptions.
<div class="card-body">
<ul>
<li><i>pidString</i> – Used for authentication and to refer to which user-specific account needs to be considered for verification. The value for this should be the token received from the Verify operation.</li>
<li><i>verifyOption</i> – Used to hold the value that identifies whether the verification call is new or for re-verification (user and account combination) for the account. Possible values for this variable could be “‘REVERIFY”’ or any other string. If the value is “REVERIFY”, the VerifyNow system will consider this to be a re-verification; otherwise, it will be considered a new verification call.</li>
<li><i>klURL</i> – Used keep the customer’s session alive in the client application.</li>
<li><i>cssURL</i> – Used to pass the client-hosted cssURL. This is required only when the client hosts the CSS.</li>
</ul>
</div>

<h3>Samples</h3>

```
<input type="hidden" name="pidString" id="pidString" value="CE02#4#TNiA3Qj"/>

<input type="hidden" name="verifyOption" id="verifyOption" value="REVERIFY"/>

<input type="hidden" name="verifyOption" id="verifyOption" value=""/>

<input type="hidden" name="klURL" id="klURL" value="<<clientHostedURL>>"/> 

<input type="hidden" name="cssURL" id="cssURL" value="<<clientHostedCSS>>"/>

```
</div>
</div>
</br>

<div>
    <input type="checkbox" class="collapsible-checkbox" id="section6">
    <label class="label-expand" for="section6">Widget Placement</label>
    <div class="content-expand">
The client’s application is required to provide the expected space in their user interface to place the VerifyNow widget. This needs to happen through use of the `<b>div</b>` tag with the predefined ID (<b>vn_space</b>) associated with it. A sample could appear as:

```
<div id="vn_space" style="align:center; margin:5px; width:100%" align="center"> </div>
```
</div>
</div>

</br>

<div>
    <input type="checkbox" class="collapsible-checkbox" id="section4">
    <label class="label-expand" for="section4">Control Handover to Client Application</label>
    <div class="content-expand">

Application control will be transferred back to the client’s application from the VerifyNow system through a JavaScript API call hosted by the client application. Clients can incorporate their business flow inside of it. 

```
function onVnVerificationComplete(JSonResponse){

alert("UI Control is handed over to Client");

}
```
</div>
</div>
</br>

<div>
    <input type="checkbox" class="collapsible-checkbox" id="section5">
    <label class="label-expand" for="section5">Outcome</label>
    <div class="content-expand">

The client’s application receives the outcome of the verification through the Outcome operation with the token associated for the specific verification. The Outcome operation provides the detail, including verification types and their respective statuses along with the combined decision. Refer to the <a href="../docs/?path=docs/api-flow.md">API Flow</a>.

</div>
</div>
</br>

<div class="debit-body">
    <div class="debit-container">
        <input type="radio" name="dot" id="one">
        <input type="radio" name="dot" id="two">
        <div class="main-card-debit">
            <div class="cards-debit">
                <div class="card-debit">
                <div class="content-debit">
                    <div class="img-debit">
                        <img src="https://raw.githubusercontent.com/Fiserv/verifynow/develop/assets/images/AutomatedAcctAddition.png" alt="automated-acct-addition">
                    </div>
                    <div class="details">
                        <div class="name">Automated Account Addition</div>
                    </div>
                    <div class="media-icons">
                        <a href="?path=docs/automated-account-additions.md">Click View</a>
                    </div>
                </div>
                </div>
                <div class="card-debit">
                    <div class="content-debit">
                        <div class="img-debit">
                            <img src="https://raw.githubusercontent.com/Fiserv/verifynow/develop/assets/images/add-acc-manually-icon.png">
                        </div>
                        <div class="details">
                            <div class="name">Add Account Manually</div>
                        </div>
                        <div class="media-icons">
                            <a href="?path=docs/add-account-manually.md">Click View</a>
                        </div>
                    </div>
                    </div>
                    <div class="card-debit">
                        <div class="content-debit">
                            <div class="img-debit">
                                <img src="https://raw.githubusercontent.com/Fiserv/verifynow/develop/assets/images/user-workflow.png">
                            </div>
                            <div class="details">
                                <div class="name">User workflow</div>
                            </div>
                            <div class="media-icons">
                                <a href="?path=docs/user-workflow.md">Click View</a>
                            </div>
                        </div>
                        </div>
            </div>
            <div class="cards-debit">
                <div class="card-debit">
                <div class="content-debit">
                    <div class="img-debit">
                        <img src="https://raw.githubusercontent.com/Fiserv/verifynow/develop/assets/images/acc-verification-status.png">
                    </div>
                    <div class="details">
                        <div class="name">Account Verification status/Exit points</div>
                    </div>
                    <div class="media-icons">
                        <a href="?path=docs/account-verification-status.md">Click View</a>
                    </div>
                </div>
             </div>
             <div class="card-debit">
                <div class="content-debit">
                    <div class="img-debit">
                        <img src="https://raw.githubusercontent.com/Fiserv/verifynow/develop/assets/images/css-integration.png">
                    </div>
                    <div class="details">
                        <div class="name">CSS Integration</div>
                    </div>
                    <div class="media-icons">
                        <a href="?path=docs/css-integration.md">Click View</a>
                    </div>
                </div>
             </div>
             <div class="card-debit" style= "visibility: hidden">
                <div class="content-debit">
                    <div class="img-debit" >
                        <img src="https://raw.githubusercontent.com/Fiserv/verifynow/develop/assets/images/edit-debit.png">
                    </div>
                    <div class="details">
                        <div class="name">CSS Integration</div>
                    </div>
                    <div class="media-icons">
                        <a href="?path=docs/css-integration.md">Click View</a>
                    </div>
                </div>
             </div>
            </div>
        </div>
        <div class="button-debit">
            <label for="one" class="active one"></label>
            <label for="two" class="two"></label>
        </div>
    </div>
</div>

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
     * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: sans-serif;
    }
    .debit-body {
        display: flex;
        min-height: 50vh;
        align-items: center;
        justify-content: center;
        background: #6a737d;
        background-position: center;
        background-size: cover;
        position: relative;
    }
    .debit-body::before {
        z-index: 777;
        content: '';
        position: absolute;
        background: #f1f1f1;
        width: 100%;
        height: 100%;
    }
    ::selection {
        background: #ff676d;
        color: white;
    }
    .debit-container{
        max-width: 950px;
        width: 100%;
        overflow: hidden;
        padding: 80px 0;
        z-index: 999;
        background: #ffffff;
    }
    .debit-container .main-card-debit {
        display: flex;
        justify-content: space-evenly;
        width: 200%;
        transition: 1s;
    }
    #two:checked~.main-card-debit {
        margin-left: -100%;
    }
    .debit-container .main-card-debit .cards-debit {
        width: calc(100% / 2 - 10px);
        display: flex;
        flex-wrap: wrap;
        margin: 0px 20px;
        justify-content: space-evenly;
        position: relative;
    }
    .main-card-debit .cards-debit .card-debit {
        width: calc(100% / 3 - 10px);
        background: white;
        border-radius: 10px;
        padding: 30px;
        box-shadow: 0 5px 10px rgba(0, 0, 0, 0.75);
        transition: all 0.4s ease;
    }
    .main-card-debit .cards-debit .card-debit:hover {
        transform: translateY(-15px);
    }
    .cards-debit .card-debit .content-debit {
        width: 95%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-align: center;
    }
    .cards-debit .card-debit .content-debit .img-debit {
        height: 130px;
        width: 130px;
        margin-bottom: 14px;
    }
    .card-debit .content-debit .img-debit img {
        height: 100%;
        width: 100%;
        border: 3px solid #f1f1f1;
        border-radius: 15%;
        object-fit: cover;
    }
    .card-debit .content-debit .name {
        font-size: 20px;
        font-weight: 500;
    }
    .card-debit .content-debit .desc {
        font-size: 20px;
        color: #ff676d;
    }
    .card-debit .content-debit .media-icons {
        margin-top: 10px;
        display: flex;
    }
    .media-icons{
        bottom: 8px;
    position: absolute;
    }
    .details{
height: 140px;
    }
    
    .media-icons a {
        text-align: center;
        line-height: 33px;
        height: 35px;
        width: 100px;
        margin: 0 4px;
        font-size: 18px;
        color: white;
        border-radius: 5%;
        text-decoration: none;
        border: 2px solid transparent;
        background: #f60;
        transition: all 0.3s ease;
    }
    .media-icons a:hover {
        color: #f60;
        background-color: white;
        border-color: #f60;
    }
    .debit-container .button-debit {
        width: 100%;
        display: flex;
        justify-content: center;
        margin: 20px;
    }
    .button-debit label {
        height: 15px;
        width: 15px;
        border-radius: 20px;
        background: #6a737d;
        margin: 0 4px;
        cursor: pointer;
        transition: all 0.5s ease;
    }
    .button-debit label.active {
        width: 35px;    
    }
    #one:checked~.button-debit .one {
        width: 35px;
    }
    #one:checked~.button-debit .two {
        width: 35px;
    }
    #two:checked~.button-debit .one {
        width: 15px;
    }
    #two:checked~.button-debit .two {
        width: 15px;
    }
    input[type="radio"]{
        display: none;
    }
    .block-quote {
        padding: 1em;
        color: #6a737d;
        border-left: 0.375em solid #40a9ff;
        background: #e6f7ff;
        border-radius: 3px;
    }
    .image-center {
      display: block;
      width: 70%;
      margin: 5px auto;
    }
    .confirm-button {
        padding: 2px;
        font-weight:bold;
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



