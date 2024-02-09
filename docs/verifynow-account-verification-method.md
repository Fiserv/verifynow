## VerifyNow - Account Verification Methods

The Account Ownership verification service verifies account ownership by checking whether an account provided by a user exists, whether the user owns the account, and whether the account is active and in good standing.

Account ownership verification is performed using the below three verification methods.  The client has the flexibility to specify at the home level and at the user level which account verification methods should be enabled. The specific verification method to be used for a user is passed by the client system in the verification request.

<table border="1">
<tr style="background-color:#bfbfbf">
<th>Verification Method</th>
<th>Description</th>
<th>User Interaction and Ease</th>
</tr>
<tr>
<td>Instant</td>
<td>Matches customer’s name and bank account information with information in a database.</td>
<td><b>No Interaction, High Ease</b> – User simply provides bank account information; does not need to take any other action.</td>
</tr>
<tr>
<td>Real-time</td>
<td>Matches customer’s name and bank account information (if provided) with harvested data from a financial institution’s website.</td>
<td><b>Minimum Interaction, High Ease</b> – User provides their respective financial institution(s) online account credentials and provides answers to questions for further authentication if required.</td>
</tr>
<tr>
<td>Trial Deposit</td>
<td>Posts micro deposits to a customer’s bank account. Deposit amount is verified by the customer.</td>
<td><b>Medium Interaction, Medium Ease</b> – User must initiate the trial deposit process and must return to verify the deposit amounts.</td>
</tr>
</table>

<div>Click the below images to know more about Account Verification Methods.
    <div class="account-body">
    <div class="debit-container">
        <input type="radio" name="dot" id="one">
        <input type="radio" name="dot" id="two">
        <div class="main-card-debit">
            <div class="cards-debit">
                <div class="card-debit">
                <div class="content-debit">
                    <div class="img-debit">
                        <img src="https://raw.githubusercontent.com/Fiserv/verifynow/develop/assets/images/instant_verification.png">
                    </div>
                    <div class="details">
                        <div class="name">Instant  (Database)  Verification</div>
                    </div>
                    <div class="media-icons">
                        <a href="?path=docs/verifynow-account-verification-method/instant-verification.md">Click View</a>
                    </div>
                </div>
                </div>
                <div class="card-debit">
                    <div class="content-debit">
                        <div class="img-debit">
                            <img src="https://raw.githubusercontent.com/Fiserv/verifynow/develop/assets/images/real-time-verification.png">
                        </div>
                        <div class="details">
                            <div class="name">Real-Time  (using FI login)  Verification</div>
                        </div>
                        <div class="media-icons">
                            <a href="?path=docs/verifynow-account-verification-method/real-time-verification.md">Click View</a>
                        </div>
                    </div>
                    </div>
                    <div class="card-debit">
                        <div class="content-debit">
                            <div class="img-debit">
                                <img src="https://raw.githubusercontent.com/Fiserv/verifynow/develop//assets/images/Trial-deposit.png">
                            </div>
                            <div class="details">
                                <div class="name">Trial Deposit Verification</div>
                            </div>
                            <div class="media-icons">
                                <a href="?path=docs/verifynow-account-verification-method/trial-deposit-verification.md">Click View</a>
                            </div>
                        </div>
                    </div> 
            </div> 
        </div>
    </div>
</div>
</div>

<style>
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: sans-serif;
    }
    .account-body {
        display: flex;
        min-height: 50vh;
        align-items: center;
        justify-content: center;
        background: #6a737d;
        background-position: center;
        background-size: cover;
        position: relative;
    }
    .account-body::before {
        z-index: 777;
        content: '';
        position: absolute;
        background: #FFFFFF;
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
    }
    .debit-container .main-card-debit {
        display: flex;
        justify-content: space-evenly;
        transition: 1s;
    }
    #two:checked~.main-card-debit {
        margin-left: -100%;
    }
    .debit-container .main-card-debit .cards-debit {
        width: calc(100% / 1 - 10px);
        display: flex;
        flex-wrap: wrap;
        margin: 0 20px;
        justify-content: space-between;
        position: relative;
    }
    .main-card-debit .cards-debit .card-debit {
        width: calc(100% / 3 - 10px);
        background: white;
        border-radius: 12px;
        padding: 30px;
        box-shadow: 0 5px 10px rgba(0, 0, 0, 0.75);
        transition: all 0.4s ease;
    }
    .main-card-debit .cards-debit .card-debit:hover {
        transform: translateY(-15px);
    }
    .cards-debit .card-debit .content-debit {
        width: 100%;
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
        padding-bottom:10px;
    position: absolute;
    }
    .details{
height: 150px;
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