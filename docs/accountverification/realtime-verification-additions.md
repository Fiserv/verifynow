## Real-Time Verification and Addition (RTVA)

When a user tries to add an account for the FI via RTVA, they provide credentials for logging into the external FI. The user is put through Multi-Factor Authentication (MFA). Then account-related information is successfully scraped, and the name is passed through risk rules for matching logic to determine whether the accounts should be displayed to the user or not. If the information fails the check, the user is sent to add the account manually (see <b> Adding Account Manually </b>).

The name that comes in SSO will be compared against the name scraped by Aggregation. Risk rules for name matching determine if the account information should be displayed to the user.
