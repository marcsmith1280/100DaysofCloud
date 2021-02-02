[placeholder image](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.linkedin.com%2Fcompany%2Famazon-web-services&psig=AOvVaw01ZgBr9w8xXvZsrq11rA4a&ust=1612367276538000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIDRtKjGy-4CFQAAAAAdAAAAABAD)

NEW AWS Free Tier Account

## Introduction

My Free Tier account ended on the 1/31/2021. So with this project I went back and created a new Free Tier account. 

## Prerequisite

My Advice is to take advantage of the Free Tier options as much as you can. Especially during learning/practicing phases of AWS

## Use Case

The purpose of the Free Tier is to allow people to learn about AWS and the different services without accruing large financial charges during the process.
While learning AWS there are different services that cost different amounts. Staying in Free Tier will allow you to use most of the services needed to learn the fundamentals of AWS.

## Cloud Research

Based on my research, one of the best practices to do is after creating your new Free Tier account. You will need to create a new user and give that user progammatic & AWS management Access. 
Doing this will allow you to sign in as this user instead of signing in with Root account. 

### Step 1 — Summary of Step

Create you AWS account using email, phone number, address etc

### Step 2 — Summary of Step

Once account is created and verified you now have access to AWS management console.
Now you need to create a new user and give the use Programmatic and AWS Management access
Next step would be to create group and add a policy of Admin for the group
The best practice suggest that you add the newly created user to the group and remove the indiviaual policies created for the user
Since the group has admin access, the user will inherit those policies once added to the group

### Step 3 — Summary of Step

During this process I also enabled MFA for the user, to be able to authenticate when needed to login
I also edited the password policy to ensure a strict and safe set of rules surrounding passwords.


## ☁️ Cloud Outcome

Additional steps I ended up taking included downloading the AWS CLI to implement with my windows machine. Was able to confirm successful install with the following command: aws --version
I also created a billing policy with a budget of $10 per month. Anytime my usage goes over that amount I will be notified

## Next Steps

As I continue to work on my AWS Security Cert, in the next project I will show how I created an AWS SSO.

## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

[Tweet](https://twitter.com/MarcusS69448454/status/1356648439518552074)