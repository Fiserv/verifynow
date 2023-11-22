# Account Verification Status/Exit points

## Account Verification Status

The below table explains the different statuses of the account verification and their respective description for each status.

<table border="1">
<tr>
<th>Status</th>
<th>Description</th>
</tr>
<tr>
<td>Approved</td>
<td>Account was approved</td>
</tr>
<tr>
<td>In-progress</td>
<td>Account verification is in progress</td>
</tr>
<tr>
<td>Denied</td>
<td>Account verification failed</td>
</tr>
<tr>
<td>Inconclusive</td>
<td>Account is neither approved nor denied, but the account verification process has been completed</td>
</tr>
</table>

## Exit Points

The below information lists the exit points, once each of the verification method is completed.

Control is passed to the client system at the following points: 

<table border="1">
<tr>
<th>Verification Method</th>
<th>Verification Outcome</th>
<th>Verification Type</th>
<th>Description</th>
</tr>
<tr>
<td>Instant (Risk Database) Verification</td>
<td>Approved</td>
<td>Account Ownership</td>
<td>Account Ownership was verified successfully, using Instant (Risk Database) Verification. The user can proceed </td>
</tr>
<tr>
<td>Instant (Risk Database) Verification</td>
<td>Declined</td>
<td>Account Ownership</td>
<td>Account Ownership was not verified successfully, using Instant (Risk Database) Verification. The user cannot proceed, but can attempt ownership verification using another verification method.</td>
</tr>
<tr>
<td>Instant (Risk Database) Verification</td>
<td>Inconclusive</td>
<td>Account Ownership</td>
<td>Account Ownership could not be verified conclusively, using Instant (Risk Database) Verification. The user cannot proceed, but can attempt ownership verification using another verification method </td>
</tr>
<tr>
<td>Real-Time (using FI login) Verification</td>
<td>Approved</td>
<td>Account Ownership</td>
<td>Account Ownership was verified successfully, using Real-Time (using FI login) Verification. The user can proceed.</td>
</tr>
<tr>
<td>Real-Time (using FI login) Verification</td>
<td>Inconclusive / Failed</td>
<td>Account Ownership</td>
<td>Account Ownership was not verified successfully, using Real-Time (using FI login) Verification. The user cannot proceed, but can attempt ownership verification using another verification method.</td>
</tr>
<tr>
<td>Trial Deposit Verification</td>
<td>Approved</td>
<td>Account Ownership</td>
<td>Account Ownership was verified successfully, using Trial Deposit Verification. The user can proceed.</td>
</tr>
<tr>
<td>Trial Deposit Verification</td>
<td>Declined</td>
<td>Account Ownership</td>
<td>Account Ownership was not verified successfully, using Trial Deposit Verification. The user cannot proceed, but can attempt ownership verification using another verification method.</td>
</tr>
<tr>
<td>Trial Deposit Verification</td>
<td>Inconclusive</td>
<td>Account Ownership</td>
<td>Account Ownership could not be verified conclusively, using Trial Deposit Verification. The user cannot proceed, but can attempt ownership verification using another verification method </td>
</tr>
</table>


## See Also
[Automated Account Addition](?path=docs/automated-account-additions.md)</br>
[Add Account Manually](?path=docs/add-account-manually.md)</br>
[User workflow](?path=docs/user-workflow.md)</br>
[CSS Integration](?path=docs/css-integration.md)