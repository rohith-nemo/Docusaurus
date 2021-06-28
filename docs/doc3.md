---
id: doc3
title: Signin
---
## Signing in to get "token"
EndPoint:
```
https://app.gonemo.io:5007/api/signin
```
Required Fields:
```
email; 
password;
```

Response Payload:
It contains token and refresh token which we HAVE to send it in the headers under "token" and "refreshToken".
```
{"token":"Random Token",
"refresh_token":"Random Refresh Token"}
```

## Using "refresh_token"
Send the refresh_token under refreshToken in the following api.
EndPoint:
```
https://app.gonemo.io:5007/api/refresh
```
Required Fields:
```
refreshToken;
```

Response Payload:
It contains token. Once the Refresh token expires after 30 days, user has to signin again to get fresh refreshToken
```
{"token":"Random Token"}
```

