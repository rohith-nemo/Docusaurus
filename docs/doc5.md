---
id: doc5
title: Registration with ICICI
---

## Step 1:Registration
This Endpoint is used to Register ourseleves with ICICI. Without this registration no transaction can take place.

CORPID- Its the Corporate ID of your Corporate ICICI Account
USERID- Its the User ID of your Corporate ICICI Account
ALIASID- Its the Alias ID of your Corporate ICICI Account

EndPoint:
```
https://app.gonemo.io:5007/api/Registration
```
Required Fields:
```
Token in header under "token"

CORPID;
USERID;
ALIASID;
```
Response:
You recieve a Unique Reference Number aka URN which is unique to your account and stored in our database. It is used for all interactions with icici.
If you were already registered before and then deregistered in between and registered again,your previous URN is updated to your new URN.

## Step 2: Confirm the request from your Corporate Account
Once the Registration api is called, a request is sent to your icici corporate account to Link your account with NEMO. Please confirm your request. 

After Confirming use the below api to know your Registration Status.

EndPoint:
```
https://app.gonemo.io:5007/api/RegistrationStatus
```
Required Fields:
```
CORPID;
USERID;
URN;
```
Response:
Status of your Registration.


## Deregister
After Confirming use the below api if you want to Deregister from NEMO.

EndPoint:
```
https://app.gonemo.io:5007/api/Deregistration
```
Required Fields:
```
CORPID;
USERID;
URN;
```
Response:
Your status of deregistration will appear.

## WorkSpace table
All the credentials of the ICICI account such as CORPID,USERID,URN is stored here. Use the following endpoints to view the data.
> You can have multiple workspaces linked to your single Nemo Account.

Endpoints:

(Send Token)
GET:

https://app.gonemo.io:5007/api/workspace/viewlist

POST:(create)

https://app.gonemo.io:5007/api/workspace

UPDATE:

https://app.gonemo.io:5007/api/workspace

DELETE:

https://app.gonemo.io:5007/api/workspace

> Carefull while deleting as you data about transactions maybe affected if deleted



