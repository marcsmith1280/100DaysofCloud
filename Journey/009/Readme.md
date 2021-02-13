
![placeholder image](https://www.google.com/url?sa=i&url=https%3A%2F%2Fmedium.com%2Fweareservian%2Faws-sso-next-evolution-azure-ad-implementation-cee1121f4189&psig=AOvVaw07ab8JbCF1_zI7tmyWEDTb&ust=1613274319020000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCLj136j55e4CFQAAAAAdAAAAABAK)

AWS SSO Configuration

## Introduction

AWS Single-Sign-On makes it easy to centrally manage access to multiple AWS Accounts & business applications.
It provides users with Single-Sign-On access to all their assigned accounts and applications from one location.

## Prerequisite

What you need to understand is the purpose of AWS SSO and why it is being used. 

## Use Case

If you are an Architect or Cloud Engineer, and you want to have user sign into one centralized location where they can access all the corporate apps. Then you will want to use AWS SSO to complete the project. 

## Cloud Research

There is documentation available on AWS website that provides steps on how to enable AWS SSO via console or CLI

## Try yourself

### Step 1 — Summary of Step

Navigate to the AWS console and locate AWS SSO
Enable SSO which will also create an AWS Organization as well by default.

### Step 2 — Summary of Step

Now that AWS SSO is configured
You will need to choose your Identity Source - you can choose either AWS SSO, AD or External Identity Provider

Now you will need to add/configure a user - sample.user
Next you will be prompted to add the user to a new group - PowerUsers

Now that the user/group has been created
You will need to create a Permission Set
Create new policy - Custom Policy
Next, attach an AWS Manage Policy to the new Custom Policy - ex. S3ReadOnlyAccess

Final step is to navigate back to AWS Accounts tab, 
Assign the new user - sample.user 
And new group to the AWS Account

You can now test access using Incognito Mode in Chrome
### Step 3 — Summary of Step

You can also configure AWS SSO from the CLI

Assuming you have already configured your AWS CLI to your machines CLI
Complete Follow the next steps from CLI:

- aws configure sso
You will be prompted to enter the start URL, which can be located from AWS SSO console dashboard
Next you will enter the region which AWS SSO is enabled
Once complete you will be given a URL to navigate to and a verification code to submit
Once code is submited, press ENTER again on CLI and you will be given the Account ID and AWS Region and Role information

Once complete you can run the following command:

aws s3 ls --profile sso
ACCESS GRANTED!
## ☁️ Cloud Outcome

This project resulted in the successful creation and access using AWS SSO
I tried doing this project prior and kept getting an error message when submitting the verfication code from the CLI
Luckily I tried again and this time was successful.


## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

[Tweet](https://twitter.com/MarcusS69448454/status/1360444887204773888)
