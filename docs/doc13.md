---
id: doc13
title: Transactions with ICICI
---

## Step 1: Create a OTP and Unique id
This Endpoint is used to send OTP to the mobile number your Corporate account is linked to.

CORPID- Its the Corporate ID of your Corporate ICICI Account
USERID- Its the User ID of your Corporate ICICI Account
URN- Its the URN given when registeration with ICICI is completed.

EndPoint:
```
https://app.gonemo.io:5007/api/CreateOTP
```
Required Fields:
```
Token in header under "token"

CORPID;
USERID;
URN;
```
Response:
If Otp is sent successfully UNIQUEID is returned. UNIQUEID is used in the following Apis.

## Step 2:Make Transaction
Initiate the transaction.

UNIQUEID: returned after calling createOTP api
OTP : OTP received
DEBITACC: debit account
CREDITACC : credit account
IFSC : IFSC of the recieving bank
AMOUNT: Amount to be sent
TXNTYPE: Type of transaction. i.e IMPS,NEFT,RTGS
PAYEENAME: Name of the person recieving 
REMARKS: optional remarks if needed

EndPoint:
```
https://app.gonemo.io:5007/api/TransactionOTP
```
Required Fields:
```
Token in header under "token"

CORPID;
USERID;
URN;
UNIQUEID
OTP 
DEBITACC
CREDITACC 
IFSC
AMOUNT
TXNTYPE
PAYEENAME
```
Response:
UTRNUMBER and REQID is returned if the transaction is successfull. These values and your transactions are stored in the transactions table.

## Transaction Inquiry
Use this api to find out the status of your transaction made.
EndPoint:
```
https://app.gonemo.io:5007/api/TransactionTransactionInquiry
```
Required Fields:
```
Token in header under "token"

REQID
```
Response:
Status of your transactions


## Transaction table
All the credentials of the ICICI account such as CORPID,USERID,URN is stored here. Use the following endpoints to view the data.
> You can have multiple transactionss linked to your single Nemo Account.

Endpoints:

(Send Token)

POST:
> To view Single Transaction
https://app.gonemo.io:5007/api/SingleTransaction
(Send UNIQUEID)

POST:
> To view Single Transaction
https://app.gonemo.io:5007/api/ViewSingleTransaction
(Send UTRNUMBER)

POST:
> To view Single Transaction based on either UNIQUEID or UTRNUMBER
https://app.gonemo.io:5007/api/ViewTransaction
(Send UTRNUMBER or UNIQUEID or both)


POST:
> To enter Transactions value in the transaction table manually
https://app.gonemo.io:5007/api/CreateTransaction

POST:
> To get a statement of all the transactions made in a time period
https://app.gonemo.io:5007/api/Transaction/Statement
(Send CORPID,USERID,FromDate,ToDate)

POST:
> To update a transaction based on id.
https://app.gonemo.io:5007/api/UpdateTransaction/id
(Send CORPID,USERID,FromDate,ToDate)

POST:
> To update a transaction based on UTRNUMBER and UNIQUEID.
https://app.gonemo.io:5007/api/UpdateTransaction
(Send UTRNUMBER or UNIQUEID)





