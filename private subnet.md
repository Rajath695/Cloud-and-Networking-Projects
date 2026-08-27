<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Creating a Private Subnet

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-private)

**Author:** Rajath Noor  
**Email:** raj****@gmail.com

---

## Creating a Private Subnet

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-private_afe1fdbd)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is... It is useful because


### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to...
Create a VPC.

Create subnets.

Create an internet gateway.

Create a route table.

Create a security group.

Create a network ACLs.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project is  
very informative and practically approachable

### This project took me...

This project took me like 1 hour

---

## Private vs Public Subnets

The difference between public and private subnets is that.
public subnet is connected to internet gateway and private not connected to internet

Having private subnets are useful because...to protect the important part of a system like database

My private and public subnets cannot have the same
routing table

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-private_afe1fdbd)

---

## A dedicated route table

By default, my private subnet is associated with..
network private route table 

I had to set up a new route table because
i want to create my private subnet to route

My private subnet's dedicated route table only has one inbound and one outbound rule that allows private subnet range ips

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-private_b4b904b5)

---

## A new network ACL

By default, my private subnet is associated with  NextWork Private NACL

I set up a dedicated network ACL for my private subnet because   So while the default ACL is very convenient in allowing all traffic types, we'll create a new custom network ACL to keep our private subnet safe.

My new network ACL has two simple rules 
inbound all deny
outbound all deny

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-private_1ed2cb07)

---

---
