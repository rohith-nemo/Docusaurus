---
id: doc10
title: Run the website
sidebar_label: Run Locally
---

Githuh Repo of Nemo-be [Repository](https://github.com/gonemo-io/nemo-be).

## Steps to Run Nemo-be Locally

Prerequisites
-node.js
-MySql

Step 1:-install sequelize
```
npm install --save sequelize
```
step 2:- run command
```
npm install
```
this will run and install required packages

step 3:-navigate to .config file and write the MYSQL database credentials

step 4:- run command
```
sequelize db:migrate
```
this will run the migrations and create all the required tables to the database 

step 5:- run command
```
npm start
```
this will start the server
```
docker build -t gonemo-be:latest 
docker run -d -p 4007:4007 --env-file ./.env.list gonemo-be:latest
```