## VerifyNow - Account Verification Methods

The Account Ownership verification service verifies account ownership by checking whether an account provided by a user exists, whether the user owns the account, and whether the account is active and in good standing.

Account ownership verification is performed using the below three verification methods.
&nbsp;

<center>

![Images](../assets/images/verifynow-acc-verification-method.png =400x200)

</center>

&nbsp;


<!-- theme: info -->
 
>**Note** <br><br>
The client has the flexibility to specify at the home level and at the user level which account verification methods should be enabled. The specific verification method to be used for a user is passed by the client system in the verification request.

&nbsp;

<!-- theme: info -->
 
>**Note** <br><br>
A validation check is performed on the client request to confirm that it specifies the verification method to be used.


## See Also
[Instant (Risk Database) Verification](?path=docs/verifynow-account-verification-method/instant-verification.md)<br/>
[Real-Time (using FI login) Verification](?path=docs/verifynow-account-verification-method/real-time-verification.md)<br/>
[Trial Deposit Verification](?path=docs/verifynow-account-verification-method/trial-deposit-verification.md)<br/>