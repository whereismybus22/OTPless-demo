[![OTPless](https://d1j61bbz9a40n6.cloudfront.net/website/home/v4/logo/black_logo.svg)](https://otpless.com/platforms/javascript)

# Javascript Demo

## Steps to add OTPless SDK to your Website

1. **Add OTPLESS Sign in**

    > Add the following code to your sign up/ sign in page where you want to embed your sign in functionality.

    ```html
    <div id="otpless-login-page"></div>
    <script id="otpless-sdk" src="https://otpless.com/v2/headless.js"  data-appid="YOUR_APP_ID"></script>
    // Replace with your cid
    ```

2. **Retrieve User's Information**

    > Implement the following function to retrive the **user data** upon successful authentication of the user.

    ```html
    <script type="text/javascript">
        function otpless(otplessUser) {
            alert(JSON.stringify(otplessUser));
        }
    </script>
    ```

### Codes of Interest

- [OTPless-login-page](loginpage.html#L11) - login page
- [OTPless-script](loginpage.html#L13) - script to integrate OTPless SDK
- [Callback function](loginpage.html#L17) - callback function to retrieve user data

> Received User Data Format

```js
// otpless user Format
{
    "statusCode": 200,
    "success": true,
    "response": {
        "channel": "PHONE",
        "deliveryChannel": "WHATSAPP",
        "authType": "OTP",
        "requestId": "xxxxxxxxxxxxxxxx"
    }
}
```
