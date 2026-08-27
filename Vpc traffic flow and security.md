<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# VPC Traffic Flow and Security

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-security)

**Author:** Rajath Noor  
**Email:**  raj***@gmail.com

---

## VPC Traffic Flow and Security

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-security_92b0b0b4)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is... and it is useful because...Amazon Virtual Private Cloud (VPC) is a service that lets you create a logically isolated section of the AWS cloud where you can launch resources in a virtual networ

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to
setup VPC
setup route table
setup Security group
setup Network ACL...

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was so informative.

### This project took me...

This project took me like 1 hour

---

## Route tables

Route tables are...Think of a route table as a GPS for the resources in your subnet. Just like a GPS helps people get to their destination in a city, a route table is a table of rules, called routes, that decide where the data in your network should go.

Routes tables are needed to make a subnet public because...We need no access internet gateway to share resources

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-security_0a07b191)

---

## Route destination and target

Routes are defined by their destination and target, which mean...
Target
The target defines the next step or hop that the packet should take to reach its destination

Destination
The destination in a route table represents the IP address or range of addresses (CIDR block) to which the network traffic is intended to go


The route in my route table that directed internet-bound traffic to my internet gateway had a destination of. 0.0.0.0/0.. and a target of...Network IG

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-security_0a07b191)

---

## Security groups

Security groups are the checkpoints which allows or restric the traffic 

### Inbound vs Outbound rules

Inbound rules are. incoming traffic.. I  configured an inbound rule that  for HTTP that allows any ipv4 address

Outbound rules are... By default, my security group's outbound rule. is default which send all traffic to all protocols

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-security_92b0b0b4)

---

## Network ACLs

Network ACLs are...
Access control lists

Think of Network ACLs as traffic cops stationed at every entry and exit point of your subnet, checking each data packet against a table of ACL rules before allowing them through.



### Security groups vs. network ACLs

The difference between a security group and a network ACL is that

Network ACL: This is like the security checkpoint at the building's main entrance, controlling who can enter or leave the entire building (subnet) .

Security Group: This is like a lock on each individual apartment door (instance), providing more specific, fine-grained control

---

## Default vs Custom Network ACLs

### Similar to security groups, network ACLs use inbound and outbound rules

By default, a network ACL's inbound and outbound rules will...
Rule 100

In contrast, a custom ACL’s inbound and outbound rules are automatically set to...*

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-security_4faeb056)

---

## Tracking VPC Resources

I created additional... Instead of my usual region, I used ap-northeast-3 ... for region and i deployed vpc,Internet Gateway ,Security group....

EC2 Global View is a tool where you can find resources used for All regions... I could even narrow down my search by sorting filters. Without EC2 Global View, you'd have to search resources used each region one by one

Now that I've learnt about EC2 Global View, I'd use it again to...
use for future projects

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-security_b03ea6162)

---

---
