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
<div class="card-body">
<ul>
<li> An active user account on Fiserv Dev Studio.</li>
</ul>
</div>

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
2.	Create a new HTTP request.
3.	Set the API method to POST or PUT, as mentioned in the API document which you want to test. 
    <!-- theme: info -->
    > #### Note
    >
    > API method of all Fiserv APIs is either set to POST or PUT for all operations.

4.	Insert the request URL.     
5.	Add Header as new parameters under the **Headers** section and insert the value in JSON format.
6.	Insert the request-payload under the **Body** tab. Make sure that the **raw** radio button is activated and the text format is set to **JSON**. 
  
    <kbd><img src="https://raw.githubusercontent.com/Fiserv/verifynow/develop/assets/images/Jsonselection_body.png" width="70%" /></kbd><br>
    
    <!-- theme: info -->
    > #### Note
    >
    > Default request-payload can be copied from the API Explorer document and you may modify certain fields as mentioned in the documentation.
  
7.	Modify the field values in JSON code that you want to test. 
8.	Click **Send**. API response is generated in the Response section.

<div class="collapsible-container">
<div>
   <input type="checkbox" class="collapsible-checkbox" id="section5">
    <label class="label-expand" for="section5">Step 1</label>
    <div class="content-expand">
    <p>Enter Host Url.</p>
    <img src="https://raw.githubusercontent.com/Fiserv/verifynow/develop/assets/images/Verifynow_Url.png">
    </div>
    </div>
    </br>
    <div>
    <input type="checkbox" class="collapsible-checkbox" id="section6">
    <label class="label-expand" for="section6">Step 2</label>
    <div class="content-expand">
    <p>Enter Header values.</p>
    <img src="https://raw.githubusercontent.com/Fiserv/verifynow/develop/assets/images/verifynow_HeaderDetails.png">
    </div>
    </div>
    </br>
    <div>
    <input type="checkbox" class="collapsible-checkbox" id="section7">
    <label class="label-expand" for="section7">Step 3</label>
    <div class="content-expand">
    <p>Request Payload.</p>
    <img src="https://raw.githubusercontent.com/Fiserv/verifynow/develop/assets/images/Verifynow_Request.png">
    </div>
    </div>
    </br>
    <div>
    <input type="checkbox" class="collapsible-checkbox" id="section8">
    <label class="label-expand" for="section8">Step 4</label>
    <div class="content-expand">
    <p>Response Payload.</p>
    <img src="https://raw.githubusercontent.com/Fiserv/verifynow/develop/assets/images/Verifynow_Repsonse.png">
    </div>
    </div>
    </br>
    </div>
    
<!--#### STEP 1:

Enter Host Url.

![image](../assets/images/Verifynow_Url.png)

#### STEP 2:

Enter Header values. 

![image](../assets/images/verifynow_HeaderDetails.png)

#### STEP 3:

Request Payload.

![image](../assets/images/Verifynow_Request.png)

#### STEP 4:

Response Payload.

![image](../assets/images/Verifynow_Repsonse.png)-->

<style>

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
    .markdown-body pre{
     background-color:#454545;
    }
</style>