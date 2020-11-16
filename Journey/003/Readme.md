**Add a cover photo like:**
![placeholder image](https://www.securitymagazine.com/ext/resources/SEC/2017/April/SEC0417-testing-feat-slide_900px.jpg?1489683576)

# AWS Security 

## Introduction

The purpose of this project was to experiment with how AWS GuardDuty actually works. I was able to successfully enable AWS GuardDuty and also created a demo list of IP addresses to add to the Trusted IP list. I also generated some sample findings to view and inspect what the details would look like in the real world. Finally I created a suppression rule to suppress some common but necessary findings that are not high level threats

## Prerequisite

To pass the AWS Security Specialist Certification, one must understand how GuardDuty works and its purpose. 

## Use Case

AWS Guard Duty is a threat intelligence service by AWS which monitors for malicious behavior to help customers protect their AWS workloads.

## Try yourself

To begin working with AWS GuardDuty, you must first enable the service to be activated. Pricing varies depending on quantity of AWS CloudTrail, VPC Flow Logs and DNS logs events being analyzed

### Step 1 — Summary of Step

Login to AWS console and search for AWS GuardDuty. Enable the GuardDuty Service

### Step 2 — Summary of Step

-Navigate to lists. 
-On your personal PC created a txt file and add a sample IP address. 
-Create a demo S3 bucket and upload your IP address txt file to S3. 
-Next on List page, select Add a trusted IP list and create name, add the location of file from S3 and select the format. Finally select ADD LIST
### Step 3 — Summary of Step

-On Findings tab, select Suppress Findings
-Type the name of the findings you wish to suppress and add description. Select Save

## ☁️ Cloud Outcome

From completing this project I learned how to Add trusted IP addresses to GuardDuty. GuardDuty does not generate findings for IP address on trusted IP lists.

## Next Steps

With my next project I will focus on learning how to enable GuardDuty across all AWS accounts. To centralize the dashboard.

## Social Proof

[Tweet](https://twitter.com/MarcusS69448454/status/1328475993212903425ink)
