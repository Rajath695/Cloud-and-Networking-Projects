<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Access S3 from a VPC

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-s3)

**Author:** Rajath Noor  
**Email:** raj**8@gmail.com

---

## Access S3 from a VPC

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-s3_3e1e79a2)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is... and it is useful because they will give free tier to get trained to platform

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to. access s3 bucket from vpc

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was more informative 

### This project took me...

This project took me 60 minutes

---

## In the first part of my project...

### Step 1 - Architecture set up

Create a VPC from scratch!

Launch an EC2 instance into your VPC.

### Step 2 - Connect to my EC2 instance

In this step, I will  Connect directly to your EC2 instance.

### Step 3 - Set up access keys

In this step, I will.Give your EC2 instance access to your AWS environment.

---

## Architecture set up

I started my project by launching nextwork vpc and EC@ instance

I also set up s3 bucket with two files uploaded

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-s3_4334d777)

---

## Running CLI commands

There is a special software called the AWS CLI (Command Line Interface) that you install and run on your computer to control AWS services directly from the command line i.e. your terminal! You can install this in your local computer too, and all EC2 instances come with it already installed.



The first command I ran was aws s3 ls

The second command I ran was aws configure  This command is used to configure credentials

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-s3_e7fa8776)

---

## Access keys

### Credentials

The aws configure command is the setup and authentication command for the AWS Command Line Interface (CLI)

Access keys are An access key ID is a part of a credential!

Your credentials are made up of a username and password; think of the access key ID as the username.

You don't automatically have one, but you can create access keys IDs through AWS IAM.



The secret access key is like the password that pairs with your access key ID (your username). You need both to access AWS services.

### Best practice

Although I'm using access keys in this project, a best practice alternative is to use key pairs


---

## In the second part of my project...

### Step 4 - Set up an S3 bucket

In this step, I will Launch a bucket in Amazon S3.

### Step 5 - Connecting to my S3 bucket

In this step, I will Head back to your EC2 instance.

Get your EC2 instance to interact with your S3 bucket.

---

## Connecting to my S3 bucket

The first command I ran was aws s3 ls

When I ran the command... again, the terminal responded with... This indicated...2026-09-04 13:47:07 nextwork-vpc-project-noor-963348789655-ap-south-1-an

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-s3_4334d778)

---

## Connecting to my S3 bucket

Another CLI command I ran was aws s3 ls s3://nextwork-vpc-project-noor-963348789655-ap-south-1-an

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-s3_4334d779)

---

## Uploading objects to S3

To upload a new file to my bucket, I first ran the command. sudo touch /tmp/test.txt This command creates a test.txt file

The second command I ran was aws s3 cp /tmp/test.txt s3://nextwork-vpc-project-noor
This command will copy the files inside to the s3 bucket

The third command I ran was aws s3 ls s3://nextwork-vpc-project-noor
 which validated that files inside the s3 bucket

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-s3_3e1e79a2)

---

---
