
## Returning User

For returning users (i.e., users who begin the verification process, leave, and then return to complete the process), the following scenarios would apply:

<b>Partners Using RTV, Instant, and Trial Deposit</b><br/>
<br/>
When an account is present in SSO and in Compass:
  
<div class="card-body"><ul><li>If verification status is In Progress, the user is returned to the last page visited.</li>
<li>If verification status is Approved, the user is returned to re-verify the account.</li>
</ul></div>

When an account is present in SSO but absent in Compass:
  
<div class="card-body"><ul><li>If verification status is Not Applicable, the user is returned to the beginning of Account Verification.</li>
</ul></div>


When an account is absent in SSO and but present in Compass:

<div class="card-body"><ul><li>If verification status is Approved, the user is returned to the RTVA page to re-start the process.</li>
<li>If verification status is Not Applicable, the user is returned to the RTVA page to re-start the process.</li>
</ul></div>

When an account is absent in SSO and in Compass:

<div class="card-body"><ul><li>If verification status is Not Applicable, the user is returned to the RTVA page to re-start the process.</li></ul></div> 

 <b>Partners Using RTV, Instant, and Trial Deposit</b>

 When an account is present in SSO and in Compass:

<div class="card-body"><ul><li>If verification status is In Progress, the user is returned to the last page visited.</li>
<li>If verification status is Approved, the user is returned to re-verify the account. 
</li></ul></div> 

When an account is present in SSO but absent in Compass:   
  
<div class="card-body"><ul><li>If verification status is Not Applicable, the user is returned to the beginning of Account Verification.</li></ul></div> 

When an account is absent in SSO and but present in Compass:

<div class="card-body"><ul><li>If verification status is In Progress, the user is returned to the Manual Account Addition page to re-start the process.</li></ul></div> 

When an account is absent in SSO and in Compass:

<div class="card-body"><ul><li>If verification status is Approved, the user is returned to the Manual Account Addition page to re-start the process.</li>

<li>If verification status is Not Applicable, the user is returned to the Manual Account Addition page to re-start the process.</li></ul></div>

<b>Partners Using RTV, Instant, and Trial Deposit</b>    

When an account is present in SSO and in Compass:

<div class="card-body"><ul><li>If verification status is In Progress, the user is returned to the last page visited.
</li><li>If verification status is Approved, the user is returned to re-verify the account. </li></ul></div>

When an account is present in SSO but absent in Compass:

<div class="card-body"><ul><li>If verification status is Not Applicable, the user is returned to the beginning of Account Verification.
</li></ul></div>

When an account is absent in SSO and but present in Compass:

<div class="card-body"><ul><li>If verification status is Approved, the user is returned to the Manual Account Addition page to re-start the process.</li>

<li>If verification status is In Progress, the user is returned to the Manual Account Addition page to re-start the process.
</li></ul></div>


 When an account is absent in SSO and in Compass:

<div class="card-body"><ul><li>If verification status is Not Applicable, the user is returned to the Manual Account Addition page to re-start the process.</li></ul></div>

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
