<!-- 
type: tab 
titles: Before You Start, Know Our Standard API Structure, Make Your First API Call
-->



# Before You Start

<!-- theme: info -->

> #### Note 
>
> The current user journey enables developers to access to a range of  APIs on Verify Now. 

Before you start integration, it is important to register on the Fiserv Developer Studio to test the Verify Now APIs in the Sandbox environment. You may choose to test APIs using the <a href="?path=docs/getting-started/make-your-first-api-call.md#using-third-party-api-testing-tools" >Third-party API Testing Tools</a> of your choice.   However, registration is not required to learn about our APIs and reference documentations.
<!--

[![Video Thumbnail]][Video]  

-->

<!--[![Video Thumbnail]][Video1]  

[Video]: https://user-images.githubusercontent.com/81968767/231950346-2b13475d-f395-4b11-8a55-2d0c93f45813.mp4
[Video Thumbnail]: https://user-images.githubusercontent.com/81968767/232030323-bbde320a-2bf5-4e21-97c0-8fe1a8895913.png

[Video1]: https://github.com/Fiserv/banking-hub/assets/81706748/a776e7c8-bea8-410e-9529-43ca3968327d-->


## Register on Fiserv Developer Studio
This section describes the process to create an account on Fiserv Developer Studio to obtain credentials for sandbox testing.

### Creating an Account

Perform the following steps to create an account on Fiserv Developer Studio:
1.	From the top-right corner of the screen, click **Create account**
2.	Populate the required fields and click **Next**
3.	Follow the instructions on the screen to set up your account
4.	Sign in to your Fiserv Developer Studio account once it is activated.




<a href="#tab-know_our_standard_api_structure" >Next - Know Our Standard API Structure</a>



<!-- type: tab -->



# Know Our Standard API Structure 

This section describes a standard structure of request and response message of Verify Now RESTful APIs. 

## Request Message

All API requests must contain the following components:

*	[API Method](#api-method)
* [Request URL](#request-url)
*	[Request Header](#request-header)
*	[Request Body](#request-body)

For every API request, a response message is obtained that contains a response payload and the status of the API request.

### API Method

For security reasons, all API methods are set to POST or PUT, irrespective of the operation. 

### Request URL

Request URL is formed by appending Host URL and API path. 


<!-- theme: info -->
> **Request URL = Host URL + API path**


The API path along with the method (POST or PUT) is listed under the API Explorer section of that API on Fiserv Developer Studio. 
Refer the following example to construct a request URL for [**verify now**](../api/?type=post&path=/cashedgerws/verifynow/verify/v1)API:

![image](../assets/images/verifynowservice.png)


If host URL of the product is https://qa-ft.onefiserv.net/cashedgerws/verifynow/verify/v1, then request URL will be:

![image](../assets/images/verifynow_hostandrequest_url.png)




### Request Header
  
  
Header parameters are common for all API requests of Verify Now APIs. Header parameters are sent as  header parameter.

**Sample Header Example**
```
"requestHeaders": [
							{
								"key": "AdminUserName",
								"value": "string"								
							},
							{
								"key": "AdminPassword",
								"value": "string"	
							},
							{
								"key": "HomeId",
								"value": "string"								
							},
							{
								"key": "Content-Type",
								"value": "application/json"
							}
						]

```

### Request Body

The request body of an API changes based on the type of transaction being processed. Request body contains the detailed information that is required to perform a particular transaction.

**Request Payload** 

The following example shows the sample request payload for **verify now** API request.

```
{
  "VerifyNowRequest": {
    "requestId": "string",
    "profile": {
      "email": "string",
      "firstName": "string",
      "lastName": "string",
      "userId": "string"
    },
    "profileDetails": {
      "ssn": "string",
      "address": {
        "addressLine1": "string",
        "city": "string",
        "state": "string",
        "zipCode": "string"
      },
      "phoneNumber": "string"
    },
    "accountOwnershipVerification": {
      "instantVerification": {
        "enable": "string"
      },
      "trialDepositVerification": {
        "enable": "string"
      }
    }
  }
}
```


## Response Message

Upon a successful API request, a response payload is received. The response payload contains the status and the returned details of the requested API in JSON. The default response format is JSON. 


### Response Payload

The following example shows the sample response payload for **verify now** API request.

```
{
    "requestId" : "string",
    "token" : "string",
    "profileInfo" : {
        "profileId" : "string",
        "profileStatus" : "string"
    },
    "status" : {
        "statusCode" : "string",
        "statusDesc" : "string",
        "statusType" : "string"
}
}
```

To view the API documentation of **verify now** API in API Explorer, [click here](../api/?type=post&path=/cashedgerws/verifynow/verify/v1).



 [Next - Make Your First API Call](#tab-make_your_first_api_call) 



<!-- type: tab -->



# Make Your First API Call

This section describes the process to send an API request to the server and receive a response payload. To test the APIs, use the third-party API testing tool.

## Using Third-Party API Testing Tools

You can test our APIs in the Sandbox environment using third-party API testing tools, such as Postman, Apigee, JMeter and others.


<!-- theme: info -->
> #### Tip
>
> We recommend you to refer to the <a href="?path=docs/getting-started/know-our-standard-api-structure.md#know-our-standard-api-structure" title="Click to open">Know Our Standard API Structure</a> section to understand the API structure prior to testing the APIs in any third-party tool.


### Prerequisites
To make an API call, you need:
- An active user account on Fiserv Dev Studio


**Creating an account on Dev Studio**


To create an account on Fiserv Developer Studio, refer to the [Register on Fiserv Developer Studio](?path=docs/getting-started/before-you-start.md#register-on-fiserv-developer-studio) section. 


### Example
  
The following example illustrates the process to test an API using Postman application:
  
  
Postman is a client that lets you test RESTful APIs. If you are familiar with Postman, refer to the following steps to test Fiserv APIs in the sandbox environment. 
  
<!-- theme: info -->  
> #### Recommendation
>
> Keep the API documentation accessible to refer to the default request-payload for the request message. 



#### Prerequisite to run Postman collection


To  test an API using Postman application: 

1. Open a web or desktop application of Postman.
2.	Create a new HTTP request
3.	Set the API method to POST or PUT, as mentioned in the API document which you want to test 
    <!-- theme: info -->
    > #### Note
    >
    > API method of all Fiserv APIs is either set to POST or PUT for all operations.

4.	Insert the request URL     
5.	Add Header as new parameters under the **Headers** section and insert the <Header> value. <!--in JSON format--> 
6.	Insert the request-payload under the **Body** tab. Make sure that the **raw** radio button is activated and the text format is set to **JSON** 
  
    <kbd><img src="../assets/images/Jsonselection_body.png" width="70%" /></kbd><br>
    
    <!-- theme: info -->
    > #### Note
    >
    > Default request-payload can be copied from the API ExJSONplorer document and you may modify certain fields as mentioned in the documentation.
  
8.	Modify the field values in JSON code that you want to test 
9.	Click **Send**. API response is generated in the Response section

  
<!--kbd>
  <img src="https://user-images.githubusercontent.com/81968767/145146913-16d54888-1e48-46b7-99f5-64827a78e21f.gif" />
</kbd>-->

#### STEP 1:

Enter Host Url.

![image](../assets/images/Verifynow_Url.png)

#### STEP 2:

Enter Header values 

![image](../assets/images/verifynow_HeaderDetails.png)

#### STEP 3:

Request Payload

![image](../assets/images/Verifynow_Request.png)

#### STEP 4:

Response Payload

![image](../assets/images/Verifynow_Repsonse.png)
  
  

<!-- type: tab-end -->
