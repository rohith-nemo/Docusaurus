---
id: doc11
title: Forgot Password
---
## Step 1:
Email is your username,
Otp is sent to Mobile Number.

Call the following endpoint.

EndPoint:
```
https://app.gonemo.io:5007/api/forgotpasswordcode
```
Required Fields:
```
email;
```

## Step 2:
Otp is send to the verified mobile number or email.
Send the OTP under "verificationCode", and the new password under  "newPassword"

EndPoint:
```
https://app.gonemo.io:5007/api/confirmsignup
```
Required Fields:
```
email; 
verificationCode;
newPassword;
```
Response:
'Password confirmed!'
OR
'Password not confirmed!'
