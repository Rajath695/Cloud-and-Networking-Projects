<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# VPC Peering

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-peering)

**Author:** Noor Noor  
**Email:** nn0756358@gmail.com

---

## VPC Peering

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-peering_88727bef)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is... and it is useful because it shows vpc peering

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to use cloud computing

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was great

### This project took me...

This project took me 1 hour

---

## In the first part of my project...

### Step 1 - Set up my VPC

In this step, I wil Create two VPCs from scratch!

Use the visual VPC resource map to create our VPCs 

### Step 2 - Create a Peering Connection

In this step, I will Set up a connection link between your VPCs.



### Step 3 - Update Route Tables

In this step, I will
Set up a way for traffic coming from VPC 1 to get to VPC 2.

Set up a way for traffic coming from VPC 2 to get to VPC 1.

### Step 4 - Launch EC2 Instances

Wooohooo, now it's time to launch EC2 instances into your architecture!

---

## Multi-VPC Architecture

I started my project by launching create only one subnet

The CIDR blocks for VPCs 1 and 2 are... They have to be unique because Each VPC must have a unique IPv4 CIDR block so the IP addresses of their resources don't overlap. Having overlapping IP addresses could cause routing conflicts and connectivity issues!

### I also launched 2 EC2 instances

I didn't set up key pairs for these EC2 instances as n previous projects, setting up a key pair was a key step for learning how SSH and directly accessing an EC2 instance works.

However, we've also learnt that with EC2 Instance Connect, AWS actually manages a key pair for us! We don't need to manage key pairs ourselves. Since we've already learnt how to set up key pairs twice in the last two projects, we don't need to do it again this time.

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-peering_11111111)

---

## VPC Peering

A VPC peering connection is A VPC peering connection is a direct connection between two VPCs.

VPC peering connections exist to create a secure, private, and direct network link between two

The difference between a Requester and an Accepter in a peering connection is
In VPC peering, the Accepter is the VPC that receives a peering connection request! The Accepter can either accept or decline the invitation. This means the peering connection isn't actually made until the other VPC also agrees to it!
in VPC peering, the Requester is the VPC that initiates a peering connection. As the requester, they will be sending the other VPC an invitation to connect!


![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-peering_1cbb1b88)

---

## Updating route tables

Even if your peering connection has been accepted, traffic in VPC 1 won't know how to get to resources in VPC 2 without a route in your route table! You need to set up a route that directs traffic bound for VPC 2 to the peering connection you've set up.

My VPCs' new routes have a destination of... The routes' target was...
10.1.0.0/16,10.2.0.0/16

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-peering_4a9e8014)

---

## In the second part of my project...

### Step 5 - Use EC2 Instance Connect

Use EC2 Instance Connect to connect to your first EC2 instance.

Fix a connection error!



### Step 6 - Connect to EC2 Instance 1

In this step, I will
Use EC2 Instance Connect to connect to Instance 1 (one more time)!

Fix (another) error.

### Step 7 - Test VPC Peering

In this step, I will Get Instance 1 to send test messages to Instance 2.

Solve connection errors until Instance 2 is able to send messages back.

---

## Troubleshooting Instance Connect

 recommended EC2 Instance Connect because it's the simplest, most secure, and least friction way to get shell access to a Linux instance in that situation:



I was stopped from using EC2 Instance Connect as  
no public ipv4 or ipv6 address assigned

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-peering_7685490c)

---

## Elastic IP addresses

To resolve this error, I set up Elastic IP addresses. Elastic IP addresses are
Elastic IPs are static IPv4 addresses that get allocated to your AWS account, and is yours to delegate to an EC2 instance.

Associating an Elastic IP address resolved the error because Elastic IPs are very popular tools for making sure an application stays available on the internet. Usually, an IP address change means a website's DNS record (i.e. the map that directs users visiting their domain to the right application/server) needs to be updated.

DNS updates take time to propogate across the internet - it can take hours and even days! So without an Elastic IP, a website would be down for its users if an EC2 instance restarts and the engineers have to change a DNS record. With an Elastic IP, the IP address associated with the EC2 instance is always constant - no DNS updates needed!

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-peering_45663498)

---

## Troubleshooting ping issues

To test VPC peering, I ran the command... ping

A successful ping test would validate my VPC peering connection because...  it will show if the connection success or error

I had to update my second EC2 instance's security group I added a new rule that icmp to all

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-peering_7a29d352)

---

---
