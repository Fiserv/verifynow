
# Risk Controls

Clients can set reuse limits to mitigate the risk associated with reusing accounts. Prior to processing an account verification request, VerifyNow determines whether the new account violates any of the risk controls and returns a failure message if they do.

A. Clients can configure the following reuse limits: 

1. Number of distinct users that can use the same account. 

    a. The default is 2. 

    b. In the case of a joint account, each account holder counts as one user.
    
    c. The count changes when a user is added and when a user is removed in the following situations:
        <div class="card-body">
        <ul>
        <li>All of a user’s profiles show the same account as deleted </li>
        <li>A user unsubscribes</li>
        </ul>
        </div>

2. Number of profiles to which a user can add the same account.

    a. The default is 2.

    b. In the case of a joint account, each account holder counts as one user. 

    c. The count changes when an account is added to a profile and removed in the following situations: 
        <div class="card-body">
        <ul>
        <li>An account is deleted from a profile </li>
        <li>A profile is unsubscribed
        </li>
        </ul>
        </div>
3. Number of times the same account can be added to and deleted from a profile.

    a. The default is 3. 

    b. The number of trial deposit attempts carries the same limit. 

    c. Clients can change trial deposit limits at the user level for a particular account.

4. Number of accounts that can be active for a profile.

    a. No default value 

    b. The count changes when an account is added to a profile and removed in the following situations:
        <div class="card-body">
        <ul>
        <li>An account is deleted from a profile </li>
        <li>A profile is unsubscribed
        </li>
        </ul>
        </div>
        
B. A unique combination of Last Name, Social Security Number, and Date of Birth identify each user.

C. A unique combination of routing number, account number, and account type identify each account. 

D. Clients can submit a written request to Fiserv ePayments Customer Support to change reuse limits.

## See Also
[VerifyNow - Account Verification Methods](?path=docs/verifynow-account-verification-method.md)<br/>

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
            
 





   