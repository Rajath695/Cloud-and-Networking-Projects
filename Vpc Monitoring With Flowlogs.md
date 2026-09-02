<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# VPC Monitoring with Flow Logs

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-monitoring)

**Author:** Noor Noor  
**Email:** nn0756358@gmail.com

---

## VPC Monitoring with Flow Logs

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-monitoring_3e1e79a1)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is... and it is useful because it has variety of features

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to analyze flow logs

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was little bit difficult

### This project took me...

This project took me 2 houra

---

## In the first part of my project...

### Step 1 - Set up VPCs

In this step, I will Create two VPCs from scratch!


### Step 2 - Launch EC2 instances

In this step, I will Launch an EC2 instance in each VPC, so we can use them to test your VPC peering connection later.

### Step 3 - Set up Logs

Set up a way to track all inbound and outbound network traffic.

Set up a space that stores all of these records.



### Step 4 - Set IAM permissions for Logs

Give VPC Flow Logs the permission to write logs and send them to CloudWatch.

Finish setting up your subnet's flow log.

---

## Multi-VPC Architecture

I started my project by launching two subnets

The CIDR blocks for VPCs 1 and 2 are  10.1.0.0/16,10.2.0.0/16 They have to be unique because they were overlap if they connected to same cidr blcok subnet

### I also launched EC2 instances in each subnet

For the new rule's Type, select All ICMP - IPv4.

For the new rule's Source, select 0.0.0.0/0

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-monitoring_e7fa8775)

---

## Logs

Log class is Standard by default, which means the logs that get created will get accessed or analyzed regularly.

Log groups are
Think of a log group as a big folder in AWS where you keep related logs together. Usually, logs from the same source or application will go into the same log group, BUT logs are also region-specific. This means log data gets created and saved in the region it was created, although you can use CloudWatch dashboards to bring together logs from different regions.



### I also set up a flow log for VPC 1

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-monitoring_e8398869)

---

## IAM Policy and Roles

so VPC Flow Logs doesn't have the permission to write logs and send them to CloudWatch... yet.

I also created an IAM role because
VPC Flow Logs by default don't have the permission to record logs and store them in your CloudWatch log group. This policy makes sure that your VPC can now send log data to your log group!

A custom trust policy is A custom trust policy is specific type of policy! They're different from IAM policies. While IAM policies help you define the actions a user/service can or cannot do, custom trust policies are used to very narrowly define who can use a role.

Here's another way to think about it: using a custom trust policy is like using a special VIP list - only the services you pinpoint in your policy would be allowed to use your role.

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-monitoring_4334d777)

---

## In the second part of my project...

### Step 5 - Ping testing and troubleshooting

In this step, I will Get Instance 1 to send test messages to Instance 2.

### Step 6 - Set up a peering connection

In this step, I will... because...
Aha, so we have a missing link that's causing this connectivity error... did you catch it ahead of time that our network doesn't have a peering connection?

### Step 7 - Analyze flow logs

In this step, I will
Review the flow logs recorded aboout VPC 1's public subnet.

Analyse the flow logs to get some tasty insights 👀

---

## Connectivity troubleshooting

My first ping test between my EC2 instances had no replies, which means there is an connection fault

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-monitoring_99d4ba42)

I could receive ping replies if I ran the ping test using the other instance's public IP address, which means there is an successful connection between sender and reciever

---

## Connectivity troubleshooting

Looking at VPC 1's route table, I identified that the ping test with Instance 2's private address failed because there is no route between those two vpcs

### To solve this, I set up a peering connection between my VPCs

I also updated both VPCs' route tables so that can communicate each others private ranges

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-monitoring_7316a13d)

---

## Connectivity troubleshooting

I received ping replies from Instance 2's private IP address! This means the connection between two vpcs succesfull

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-monitoring_4ec7821f)

---

## Analyzing flow logs

Flow logs tell us about  which traffic blocked or allowed and the packet size

For example, the flow log I've captured tells us the event logs our flow 

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-monitoring_d116818e)

---

## Logs Insights

Logs Insights is To put it simply, CloudWatch Logs Insights is a powerful, interactive log analytics tool within AWS. Its primary purpose is to help you search, analyze, and visualize the log data stored in CloudWatch Logs, allowing you to quickly find insights and troubleshoot operational issues

I ran the query The query "Top 10 byte transfers by source and destination IP addresses" is all about discovering the top 10 biggest data transfers between IP addresses in your network! You'll find out which resources are moving the most data, which uncovers the busiest traffic routes in your network.

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-monitoring_3e1e79a1)

---

---
