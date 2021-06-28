---
id: doc12
title: Account Iteraction with ICICI
---

## Account Balance
This Endpoint is used to get the Account balance.

CORPID- Its the Corporate ID of your Corporate ICICI Account
USERID- Its the User ID of your Corporate ICICI Account
ACCOUNTNO- Its the Account Number of your Corporate ICICI Account

EndPoint:
```
https://app.gonemo.io:5007/api/AccountBalance
```
Required Fields:
```
Token in header under "token"

ACCOUNTNO;
CORPID;
USERID;
URN;
```
Response:
Account Balance is returned

## Account Statement
Use this endpoint to get your Account Statement.

FROMDATE - From date of the Statement
TODATE - To date of the Statement

EndPoint:
```
https://app.gonemo.io:5007/api/AccountStatement
```
Required Fields:
```
ACCOUNTNO;
FROMDATE;
TODATE;
CORPID;
USERID;
URN;
```
Response:
Statement of your transactions

