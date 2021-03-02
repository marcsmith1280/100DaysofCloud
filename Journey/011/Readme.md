
![placeholder image](https://www.google.com/url?sa=i&url=http%3A%2F%2Fwww.davidromerotrejo.com%2F2017%2F12%2Faws-elastic-load-balancing.html%3Fm%3D1&psig=AOvVaw0taPN4bbYq49sNMriJM1qM&ust=1614807124361000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCICU97_Hku8CFQAAAAAdAAAAABAD)

Classic Load Balancer 

## Introduction

In this project I demonstrated the ability to configure a Classic Load Balancer in AWS.

## Prerequisite

Some important information you want to know is exactly what the purpose of a Load Balancer is and the different types. The type of application being created will dictate which type of load balancer you want to create. 

## Use Case

In this project, I created a classic load balancer in front of 2 EC2 instances. Both EC2 instances have nhinx installed on them with one being labeled Server 1 & the other Server 2. 
The Classic load balance allowed me to divert an equal 50% of the traffic spreading the work evenly between EC2 instances. This will increase availablity of applications and websites for users.

## Cloud Research

3 Types of Load Balancers
-Classic Load Balancer
-Application Load Balancer
-Network Load Balancer

Classic Load Balancers were the old generations and are recommended if you still have instance in EC2 classic. If not, it’s recommended to move to Application/Network Load Balancer.


## Try yourself

By now you should already know how to launch instances in EC2. 
I'll also show the commands used to connect to EC2 instance via CLI and install nginx via CLI
### Step 1 — Summary of Step

First you must launch your EC2 instances
*Always stay in Free Tier*
You can launch 2 directly from Instance Details screen
Always choose the correct security group.

### Step 2 — Summary of Step

Now that you have launched your EC2 instances 
Create your application Load Balancer.
Configure your Security Group
You can leave Health settings as default for demo.
Finally add your 2 EC2 instances you created earlier.


### Step 3 — Summary of Step

By adding your 2 EC2 instances you have now created your Load Balancer
Remember the EC2 instances have not been configured to run any apps YET!

SSH into one of your instances
Use the follow commands to install nginx:
- sudo su -
- yum -y install nginx
- sudo amazon-linux-extras install nginx1
- systemctl start  nginx

That will install and start the service.
*Run these steps on both EC2 instances*

### Step 4 - Summary of Step

Now to see how the load balancers works follow along.

-Navigate to the IP address if each instance, you will see NGINX site
-While SSH into the instance type following command

CLI
- cd /usr/share/nginx/html
- ls 
- nano index.html 

You have now navigated to the HTML file for the NGINX site and can change the name from NGINX to Server 1. 
*Do the same steps for both instances naming one Server 1 & the other Server 2.

Once complete you can navigate to the Classic Load Balancer DNS name.
Copy and paste it in your browser. 
Each time you refresh the browser it will send you to either Server 1 or Server 2.

This is how Classic Load Balancers sends equal traffic to the the instances behind them, helping keep applications and websites highly available. 

## ☁️ Cloud Outcome

My Classic Load Balancer configuration worked like a charm. 

## Next Steps

In the next project I will configure an application Load balancer and go over its benefits.

## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

[Tweet](https://twitter.com/MarcusS69448454/status/1366864706871431174)
