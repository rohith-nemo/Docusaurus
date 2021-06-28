---
id: doc1
title: Signing Up
sidebar_label: Signup
---
## Step 1:
Email is your username,
Otp is sent to Mobile Number.

EndPoint:
```
https://app.gonemo.io:5007/api/signup
```
Required Fields:
```
email; 
mobile_number;
name;
password;
```

## Step 2:
Send the OTP under "code" field.

EndPoint:
```
https://app.gonemo.io:5007/api/confirmsignup
```
Required Fields:
```
email; 
password;
code;
```

## Resend OTP:
Call this api to resend the OTP.

EndPoint:
```
https://app.gonemo.io:5007/api/resend
```
Required Fields:
```
email; 
```


## Accounts table
All the credentials of the NEMO account is stored here. Use the following endpoints to view the data.

Endpoints:

(Send Token)

GET:

https://app.gonemo.io:5007/api/accounts

POST:(create)

https://app.gonemo.io:5007/api/accounts

UPDATE:

https://app.gonemo.io:5007/api/accounts

DELETE:

https://app.gonemo.io:5007/api/accounts

