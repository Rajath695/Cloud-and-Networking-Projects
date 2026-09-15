<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# VPC Endpoints

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-endpoints)

**Author:** Noor Noor  
**Email:** nn0756358@gmail.com

---

## VPC Endpoints

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-endpoints_09bcaa8a)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is mean by virtual private cloud

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to... access s3 from endpoint

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was very complex if not configured theproper way

### This project took me...

This project took me like 60min

---

## In the first part of my project...

### Step 1 - Architecture set up

Create a VPC from scratch!

Launch an EC2 instance, which you'll connect to using EC2 Instance Connect later.

Set up an S3 bucket.

### Step 2 - Connect to EC2 instance

 before we create that endpoint... let's see what things are like without endpoint connections in place.

In this step, we're gonna connect to your EC2 instance and try access S3 through the public internet!

### Step 3 - Set up access keys

Give your EC2 instance access to your AWS environment.

### Step 4 - Interact with S3 bucket

Head back to your EC2 instance.

Get your EC2 instance to access your S3 bucket.

---

## Architecture set up

.Create a VPC from scratch!

Launch an EC2 instance, which you'll connect to using EC2 Instance Connect later.

Set up an S3 bucket.

I also set up a s3 bucket and uploaded two files into that

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-endpoints_4334d777)

---

## Access keys

### Credentials

To set up my EC2 instance to interact with my AWS environment, I configured access key ,access secretkey ,aws region,ouputformst

Access keys are  which are what we're learning about now, are credentials for your applications and other servers to log into AWS and talk to your AWS services/resources

The secret access key is like the password that pairs with your access key ID (your username). You need both to access AWS services.

Secret is a key word here - anyone who has it can access your AWS account, so we need to keep this away from anyone else!

### Best practice

Although I'm using access keys in this project, a best practice alternative is to use key pairs.

---

## Connecting to my S3 bucket

The command I ran was. aws s3 ls which is a command used to list the S3 buckets in your account (yup, ls stands for list!).

The terminal responded with lists of s3 contentsThis indicated that the access keys I set up now

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-endpoints_4334d778)

---

## Connecting to my S3 bucket

I also tested the command.aws s3 ls s3://nextwork-vpc-project-noor  which returned. the files inside the s3 bucket

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-endpoints_4334d779)

---

## Uploading objects to S3

To upload a new file to my bucket, I first ran the command. sudo touch /tmp/nextwork.txt This command creates nextwork.txt

The second command I ran was aws s3 cp /tmp/nextwork.txt s3://nextwork-vpc-project-noor 
This command will copy the files into s3 bukcet

The third command I ran was. ~]$ aws s3 ls s3://nextwork-vpc-project-noor which validated that added txt file in there

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-endpoints_3e1e79a2)

---

## In the second part of my project...

### Step 5 - Set up a Gateway

In this step, I will Set up a way for your VPC and S3 to communicate direclty.

### Step 6 - Bucket policies

Limit your S3 bucket access's to only traffic from your endpoint

### Step 7 - Update route tables

In this step, I will Test your VPC endpoint set up.

Troubleshoot a connectivity issue.



### Step 8 - Validate endpoint conection

In this step, I wil

Test your VPC endpoint set up (again).

Restrict your VPC's acccess to your AWS environment.



---

## Setting up a Gateway

I set up an S3 Gateway, which is A Gateway is a type of endpoint used specifically for Amazon S3 and DynamoDB (DynamoDB is an AWS database service).

Gateways work by simply adding a route to your VPC route table that directs traffic bound for S3 or DynamoDB to head straight for the Gateway instead of the internet.

### What are endpoints?

An endpoint in AWS is a service that allows private connections between your VPC and other AWS services without needing the traffic to go over the internet.

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-endpoints_09bcaa8a)

---

## Bucket policies

A bucket policy is a type of IAM policy designed for setting access permissions to an S3 bucket. Using bucket policies, you get to decide who can access the bucket and what actions they can perform with it.

My bucket policy will denies all actions (s3:*) on your S3 bucket and its objects to everyone (Principal: "*")... unless the access is from the VPC endpoint with the ID defined in aws:sourceVpce.

In other words, only traffic coming from your VPC endpoint can get any access to your S3 bucket!

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-endpoints_7316a13d)

---

## Bucket policies

Right after saving my bucket policy, my S3 bucket page showed 'denied access' warnings. This was because
This means any attempt to access your bucket from other sources, including the AWS Management Console, is blocked!

I also had to update my route table because doesn't have a route that directs traffic bound for S3 to your VPC endpoint, traffic from your EC2 instance is actually trying to get to your S3 bucket through the public internet instead.

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-endpoints_4ec7821f)

---

## Route table updates

To update my route table, I modify route table of endpoint 

After updating my public subnet's route table, my terminal could return
[ec2-user@ip-10-0-1-236 ~]$ aws s3 ls s3://nextwork-vpc-project-noor
2026-09-14 12:55:00    2431554 NextWork - Denzel is awesome.png
2026-09-14 12:55:02    2399812 NextWork - Lelo is awesome.png
2026-09-15 11:40:50          0 nextwork.txt
[ec2-user@ip-10-0-1-236 ~]$ 

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-endpoints_d116818e)

---

## Endpoint policies

An endpoint policy is

AWS endpoint policies are resource-based policies attached to VPC endpoints to control access to AWS services. These policies define which AWS principals (users, roles, or accounts) can use the endpoint to access specific services. They do not override identity-based or resource-based policies but work in conjunction with them.

I updated my endpoint's policy by... I could see the effect of this right away, because it will deny in the  policy

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-endpoints_3e1e79a3)

---

---
