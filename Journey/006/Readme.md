
![placeholder image](https://lh3.googleusercontent.com/Fs8_7Txz3oUMeVrdZoRilOnSfZj60sIodrrVj4hT7q0eNAgdJwEupW0jMYE_jbZQ4Wa0PQ=s152)

AWS Cleanup

## Introduction

In this project, I simply cleaned up my AWS account. Free Tier was ending. 

## Prerequisite

Learning how to prevent future charges once Free Tier expires

## Use Case

While having fun building in AWS, time will fly by. Before you are aware your getting the emails that the Free Tier will be ending. To avoid accruing charges, make sure you follow these steps.

## Cloud Research

- ✍️ Document your trial and errors. Share what you tried to learn and understand about the cloud topic or while completing micro-project.
- 🖼️ Show as many screenshot as possible so others can experience in your cloud research.

## Try yourself

✍️ Add a mini tutorial to encourage the reader to get started learning something new about the cloud.

### Step 1 — Summary of Step

Identify the resources that are generating charges

### Step 1 — Summary of Step

Delete, shutdown, or terminate resources that may be generating charges

### Step 3 — Summary of Step

Proactively monitor your usage to be sure that you dont exceed the free tier offering.

## ☁️ Cloud Outcome

For my account I needed to terminate all EC2 instances in the different AZ I was using. 
I also deleted all S3 buckets that were saved.
One area where I ran into trouble was with deleting buckets associated with Elastic Bean Stalk
When I would try to delete them I kept getting a error message "Access Denied"
To fix, I went into the the bucket policy and changed the explict "Deny" to "Allow"
Once done I was able to successfully delete all buckets with no issues

## Next Steps

Next I was create a new Free Tier account and began to create roles and practice AWS

## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

[Tweet](https://twitter.com/MarcusS69448454/status/1356378815229030401)
