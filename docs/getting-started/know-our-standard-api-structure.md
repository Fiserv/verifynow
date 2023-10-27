# Know Our Standard API Structure 

This section describes a standard structure of request and response message of Verify Now RESTful APIs. 

## Request Message

All API requests must contain the following components:

*	[API Method](#api-method)
* [Request URL](#request-url)
* [Access Token](#access-token)
*	[Request Header](#request-header)
*	[Request Body](#request-body)

For every API request, a response message is obtained that contains a response payload and the status of the API request.

### API Method

For security reasons, all API methods are set to POST or PUT, irrespective of the operation. 

### Request URL

Request URL is formed by appending Host URL and API path. 

<!-- theme: info -->
> **Request URL = Host URL + API path**


To get Host URL, go to API key section of your Workspace. The API path along with the method (POST or PUT) is listed under the API Explorer section of that API on Fiserv Developer Studio. 
Refer the following example to construct a request URL for [**Instant Verification**]<!--(../api/?type=post&path=/acctservice/acctmgmt/accounts)--> API:

![image](https://user-images.githubusercontent.com/81968767/224235588-d0eb8fd0-6408-475e-99ba-a0a7b06c95b2.png)


If host URL of the product is https://cert.api.fiservapps.com/banking/efx/v1/, then request URL will be:

![image](../assets/images/verifynow_hostandrequest_url.png)


### Access Token

An access token is used to authenticate your API build and allows you to use the Fiserv APIs securely. Verify Now API uses bearer access token, and API key and API secret are required to generate an access token. A generated access token is valid for approximately 15 minutes.
To generate an access token, refer to the [Generating Access Token](?path=docs/getting-started/before-you-start.md#generating-access-token) section.


### Request Header
  
  
Header parameters are common for all API requests of Verify Now APIs. Header parameters are sent as a JSON under EFXHeader header parameter.

For more information on EFXHeader and to view the list of all header parameters,<!--<a href="?path=docs/api-ref-EFX-header.md" title="Click to view the list of EFX header parameters"> click here</a>.-->

**Sample Header Example**
```
"EFXHeader": [
							{
								"key": "AdminUserName",
								"value": "string",
								"type": "text"
							},
							{
								"key": "AdminPassword",
								"value": "string",
								"type": "text"
							},
							{
								"key": "HomeId",
								"value": "string",
								"type": "text"
							},
							{
								"key": "Content-Type",
								"value": "application/xml",
								"type": "text"
							}
						]

```

### Request Body

The request body of an API changes based on the type of transaction being processed. Request body contains the detailed information that is required to perform a particular transaction.

**Request Payload** 

The following example shows the sample request payload for **Instant Verification** API request.

```
<VerifyNowRequest>
    <requestId>string</requestId>
    <profile>
        <email>string</email>
        <firstName>string</firstName>
        <lastName>string</lastName>
        <middleName/>
        <userId>string</userId>
    </profile>
    <profileDetails>
        <ssn>string</ssn>
        <address>
            <addressLine1>string</addressLine1>
            <city>string</city>
            <state>string</state>
            <zipCode>string</zipCode>
        </address>
        <phoneNumber>string</phoneNumber>
    </profileDetails>
    <accountOwnershipVerification>
        <instantVerification>
            <enable>string</enable>
        </instantVerification>
        <trialDepositVerification>
            <enable>string</enable>
        </trialDepositVerification>
    </accountOwnershipVerification>
</VerifyNowRequest>
```


## Response Message

Upon a successful API request, a response payload is received. The response payload contains the status and the returned details of the requested API in XML. The default response format is XML. 


### Response Payload

The following example shows the sample response payload for **Instant Verification** API request.

```
<VerifyNowResponse>
    <requestId>verifynowIn100</requestId>
    <token>string</token>
    <profileInfo>
        <profileId>string</profileId>
        <profileStatus>string</profileStatus>
    </profileInfo>
    <status>
        <statusCode>string</statusCode>
        <statusDesc>string</statusDesc>
        <statusType>string</statusType>
    </status>
</VerifyNowResponse>
```

To view the API documentation of **Instant Verification** API in API Explorer, [click here]<!--(../api/?type=post&path=/partyservice/parties/parties/secured/list).-->



[Next - Make Your First API Call](#tab-make_your_first_api_call)