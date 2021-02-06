
![placeholder image](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.jscmgroup.com%2Fsecurity-views-blog%2Fmulti-factor-authentication&psig=AOvVaw1wCIvUen1vk1CdXukb5JMb&ust=1612663451881000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCKjAhNqV1O4CFQAAAAAdAAAAABAD)

MFA Protected API Access

## Introduction

I chose to do this project while studying for AWS Security Cert. MFA's are becoming more popular in many differnt ways and fashions. The additional security it adds can help prevent the wrong person from doing things they shouldn't. 

## Prerequisite

Some base knowledge needed to know is that you can grant permissions to users to stop/start EC2 instances. You can also design the policy to ensure the users uses MFA for additional security purposes. 

## Use Case

The use-case is added Security. If you want to an extra layer of security to the users who have access to make changes to your EC2 instances. You should really consider using MFA Protected API Access. 

## Cloud Research

Sample Policy
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Deny",
            "Action": [
                "ec2:StopInstances",
                "ec2:TerminateInstances"
            ],
            "Resource": [
                "*"
            ],
            "Condition": {
                "BoolIfExists": {
                    "aws:MultiFactorAuthPresent": "false"
                }
            }
        }
    ]
}


## Try yourself

To try this project on your own, please use the following steps. 

### Step 1 — Summary of Step

First step is to create a user in IAM
Include Admin Access for the users policy 

### Step 2 — Summary of Step

Next step would be to add an Inline policy to the new user permissions
Copy and paste the above policy and create an policy name 


### Step 3 — Summary of Step

Next navigate to the IAM dashboard and copy the user ARN 
Sign in as the new user role created 

What you will notice is that even signed in as the new user
You still cant stop or start any EC2 instances

This is because you must set MFA for the new user!

### Step 4 - Summary of Step

Navigate to IAM and select the new user
Select Security Credentials and enable MFA 

Using one of many virtual MFA options
Scan your QR code and activate MFA

### Step 5 - Summary of Step

Now you must sign out of new user account 
Once signed out, please sign back in
This time you will be prompted to enter MFA code during login

After successful login using MFA code
The new user role will now be able to stop/start EC2 instances

## ☁️ Cloud Outcome

After completing these steps I was able to successful create a new user and add MFA authentication to the user account
What I learned during my studies was very interesting. During my studies it instructed that you wanted to complete the same function of 
starting and stopping EC2 instances from the CLI that you would need to authenticate for MFA on the CLI as well.
The instructions said to use the get-session-token command!

The interesting part was that I did not configure the CLI with MFA using the get-session-token
Yet I was still able to stop/start the EC2 instances

## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

[Tweet](https://twitter.com/MarcusS69448454/status/1357878465832353792)
