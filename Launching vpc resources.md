<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Launching VPC Resources

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-ec2)

**Author:** Noor Noor  
**Email:** nn0756358@gmail.com

---

## Launching VPC Resources

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-ec2_8ee57662)

---

## Introducing Today's Project!

### What is Amazon VPC?

, Amazon Virtual Private Cloud (VPC) is a service that lets you provision a logically isolated section of the AWS Cloud where you can launch resources in a virtual network that you define

### How I used Amazon VPC in this project

I used Amazon VPC to...Launch private vpc resources

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was  it was very easier 

### This project took me...

This project took me like 20 minutes

---

## Setting Up Direct VM Access

Directly accessing a virtual machine means

For a typical Linux instance, this means connecting via SSH (Secure Shell) on port 22. For a Windows instance, it means connecting via RDP (Remote Desktop Protocol) on port 3389.

This is different from "accessing" an application hosted on the instance (like visiting a website on port 80 or 443). Direct access is about managing the server itself—running commands, installing software, editing configuration files, or troubleshooting issues.

### SSH is a key method for directly accessing a VM

SSH traffic means...
Secure shell

we use for this secure access to a remote machine. When you connect to the instance, SSH verifies you possess the correct private key corresponding to the public key on the server, ensuring only authorized users can access the instance. 

### To enable direct access, I set up key pairs

The key pair type determines the algorithm used for generating the key pair's cryptographic keys

A private key's file format means... My private key's file format was .pem

No matter which format your private key uses, one thing remains critical: AWS does not store your private key. You download it once when you create the key pair. If you lose it, you cannot get it back—you'll need to create a new key pair and replace it on your running instances

---

## Launching a public server

Start your response with 'I had to change my EC2 instance's networking settings by selecting networking vpc and public subnet

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-ec2_88727bef)

---

## Launching a private server

My private server has its own dedicated security group because...

Choosing the NextWork Public Security Group as the source means only resources that are part of the NextWork Public Security Group can communicate with your instance. This restricts access to a much smaller group of trusted resources, rather than allowing potentially any IP address on the internet (0.0.0.0/0) to access your instance. A great move for securing a private subnet!

My private server's security group's source is. SSH

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-ec2_4a9e8014)

---

## Speeding up VPC creation

I used an alternative way to set up an Amazon VPC! This time, I find more steps while creating this

A VPC resource map is. A VPC resource map is a visual tool within the AWS Management Console that shows all the components of your Virtual Private Cloud and how they connect . It turns your VPC's configuration into an interactive diagram to help you understand your network architecture, verify configurations, and spot potential issue

My new VPC has a CIDR block of... It is possible for my new VPC to have the same IPv4 CIDR block as my existing VPC because...

our new VPC can have the same IPv4 CIDR block as a "NextWork" (another) VPC because there is no global requirement for IP ranges to be unique across different AWS accounts or regions. Each VPC operates as an isolated network, so overlapping private IP addresses are technically permitted as long as the networks are not connected.

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-ec2_1cbb1b88)

---

## Speeding up VPC creation

### Tips for using the VPC resource map

When determining the number of public subnets in my VPC, I only had two options:..0,1

A NAT gateway (Network Address Translation gateway) is a managed AWS service that allows instances in a private subnet to connect to the internet or other networks, while preventing the internet from initiating connections to those instances. It acts as a bridge between your private resources and the outside world

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-ec2_8ee57662)

---

---
