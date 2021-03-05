
![placeholder image](https://via.placeholder.com/1200x600)

Path Based Routing in Application Load Balancers

## Introduction

In the previous project I created a Classic Load Balancer.
In this project I chose to create an Application Load Balancer
Alot of the configurations are exactly the same as previous project. 
I reused the same EC2 instances. I will not go over how to setup instances, please refer back to previous project

## Prerequisite

Some important information you want to know is exactly what the purpose of a Load Balancer is and the different types. The type of application being created will dictate which type of load balancer you want to create. 

## Use Case

In this project, I created a Application Load Balancer in front of 2 EC2 instances. Both EC2 instances have nhinx installed on them with one being labeled Server 1 & the other Server 2. Within the EC2 instances I configured 2 index.html files. Inside the first index.html I created a new directory called "images" and the other EC2 instance has a index.html file called "work". By doing this I was able to route traffic based on the path of either \images or \work.

## Cloud Research

3 Types of Load Balancers
-Classic Load Balancer
-Application Load Balancer
-Network Load Balancer

## Try yourself

### Step 1 - Summary of Step

First you want to create the Application Load Balancer
Give it name and select the availability zones

You also must configure a new Target Group
Also register your 2 instances with your Target group

### Step 2 - Summary of Step

Next we must configure new Target Groups
First will be named Images
Please choose Target Type as - Instance

For our next TG 
Second will be named - Work
Please choose Target Type as - IP Address

### Step 3 - Summary of Step

Now we must modify the EC2 Instance Nginx Directory to serve the traffic

SSH into the first instance - Server 1
Follow the next commands
- cd /usr/share/nginx/html
- mkdir images
- cd images 
- nano index.html 
Edit the index.html to read "This is image traffic being served from Server 1"
- ctrl x
- y to save

SSH into the second instance - Server 2
Follow the next commands
- cd /usr/share/nginx/html
- mkdir work
- cd work
- nano index.html 
Edit the index.html to read "This is work traffic being served from Server 2"
- ctrl x
- y to save

You can test each change by copying the specific public IP of Server 1
add \images to confirm message will display

Follow same steps for Server 2
add \work to confirm message will display

### Step 4 - Summary of Step

Next will go back edit the 2 Target Groups we created 

Target Group - Images
Add Server 1 Instance to Registered Targets

Target Group - Work
This TG was configured to IP as Target Type

Copy Private IP address of Server 2
Select Edit on "Work" TG
Add IP as Target, select Register

### Step 5 - Summary of Step

Navigate to Application Load Balancer
In the current and only listener, select view/edit rules
Add new rule:
Condition - select path - add "images
Action - select Forward to - TG images
Select SAVE

Add new rule:
Condition - select path - add "work"
Action - select Forward to - TG work
Select SAVE

Add new rule:
Condition - Requests otherwise not router
Action - select Return fixed response - Response code = 200, 
Add text "Add either \images or \work within the URL"
Select SAVE

Now if you go back and copy DNS name of ALB, 
You can test out your configuration by adding \images or \work to the end of DNS
This will show the desired messages created. 
## ☁️ Cloud Outcome

My Application Load Balancer work like a charm

## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

[Tweet](https://twitter.com/MarcusS69448454/status/1367956442880294912)
