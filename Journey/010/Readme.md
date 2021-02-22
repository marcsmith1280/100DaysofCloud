
![placeholder image](https://docs.aws.amazon.com/kms/latest/developerguide/images/decrypt.png)

Create a new CMK in KMS and encrypt an object
## Introduction

In this project I will be show casing skills in creating a new Customer Master Key in Key Management Service in AWS. After creating 
the key I will upload a new object to a bucket in S3 and encrypt it with the new key.

## Prerequisite

Some base knowledge you will want to know is what the CMK and KMS services are in detail. As well as an understanding the importance of encrypting objects uploaded to S3. 

## Cloud Research

This project became pretty simple once I understood how the CMK work in AWS. In a previous project I already had created a new user: sample.user

## Try yourself

### Step 1 — Summary of Step

The first step requires you to create a new CMK in the Key Management Service in AWS. 
You will be require to create a key alias and description, for ease of reference. 
Next you must define a Key Administrator, who will have full permission of key
Finally, assign what user will use the key to encrypt.

### Step 2 — Summary of Step

In the next step we will create a new S3 Bucket.
My bucket name was sample-kms.

### Step 3 — Summary of Step

Finally once the bucket is created we will upload a new object to the bucket
We will use the new CMK key to encrypt the newly uploaded S3 object

Project Complete

## ☁️ Cloud Outcome

During this project I learned how to create CMK and assign them to specific users in AWS
During the creation of my S3 bucket I enabled default encryption with the new CMK
So technically I did not need to encrypt during upload because the S3 bucket was already encrypted
Furthermore, I did still encrypt the new object with the new key just for the experience 

## Social Proof

[Tweet](https://twitter.com/MarcusS69448454/status/1363671973704966144)
