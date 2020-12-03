
![placeholder image](https://i.ytimg.com/vi/MK4ZoCs-muo/maxresdefault.jpg)

# AWS Systems Manager

## Introduction

I chose to do this project to show case my skills in configuring an SSM Agent on an EC2 instance. AWS Systems Manager is the service that allows you to view and control your infrastructure in AWS. To end this project I started a session in Session Manager and created a CloudWatch Log group and sent the log files to CloudWatch to monitor who connected to the instance and what work was done. 

## Prerequisite

The knowledge needed to complete this project including understanding of the purpose of AWS Systems Manager. Also how to launch EC2 instance and start the SSM Agent service via CLI. 

## Use Case

- Centralized Access Control using IAM policies
- No Inbound ports need to be open
- Logging and auditing session activity
- One-click access to instances from the console and CLI
- No Need of VPN to connect to instances

## Cloud Research

- One error I experienced was with the .pem file and connecting to my instance. I kept getting an error message "Unprotected private key file". To resolve I needed to locate my .pem file in file explorer.
- Select Properties > Security > Advanced > Disable Inheritance > then remove all full control except for yourself.
- Another issue I ran into was managing the EC2 instance I created in SSM. The created instance would not show available. This was a easy and quick fix. Simply configure an IAM role to SSM access

## Try yourself

### Step 1 — Summary of Step

- Launch an EC2 instance
- Create an IAM role for EC2 instance and SSM full access

### Step 2 — Summary of Step

- Navigate to Sessions Manager
- Select Start Session 
- Test command can be "LS"
- End the Session

### Step 3 — Summary of Step

- Create a Cloud Watch Log Group 
- Navigate to Preferences 
- Select Edit 
- Enable Cloud Watch Logs
- Now All session data will be sent to CloudWatch for detailed monitoring

## ☁️ Cloud Outcome

What I learned was the importance of AWS Systems Manager and how it can be used as a centralized location to make changes to your EC2 Instance. By using Cloudwatch logs you can also see who has start sessions to connect to EC2 instance and what changes were made. 

## Next Steps

Next I will start a project and gain experience using SSM Run Command

## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

[Tweet](https://twitter.com/MarcusS69448454/status/1334319384530137093)
