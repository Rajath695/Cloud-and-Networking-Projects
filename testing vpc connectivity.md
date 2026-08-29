<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Testing VPC Connectivity

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-connectivity)

**Author:** Noor Noor  
**Email:** nn0756358@gmail.com

---

## Testing VPC Connectivity

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-connectivity_8ee57662)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is... and it is useful because...

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to testing connectivity between public and private server

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was most learnable


### This project took me...

This project took me like 1 hour

---

## Connecting to an EC2 Instance

Connectivity means...
EC2 Instance Connect is an alternative way to use SSH - Instance Connect lets you securely connect to your EC2 instances directly using the AWS Management Console. You're still using SSH, but with all the key management handling it for you. This takes away a lot of the complexity of setting up SSH.

My first connectivity test was whether I could connect to...
nextwork public server

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-connectivity_88727bef)

---

## EC2 Instance Connect

I connected to my EC2 instance using EC2 Instance Connect, 
EC2 Instance Connect is a service from AWS that provides a secure, browser-based way to connect to your Linux EC2 instances. It simplifies SSH access by removing the need to manage long-term private key files

My first attempt at getting direct access to my public server resulted in an error, because the security group has not allowed ssh connections

I fixed this error by add a rule to the security group to allow ssh connections to all ipv4 address

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-connectivity_1cbb1b88)

---

## Connectivity Between Servers

Ping is ping is a fundamental network diagnostic tool that tests whether a specific IP address or hostname is reachable over a network, I used ping to test the connectivity between  
public and private ec2 instance

The ping command I ran was ping "nextworks private servers ip"

The first ping returned error  and 100% packet loss
it means theres no connectivity between the two servers

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-connectivity_defghijk)

---

## Troubleshooting Connectivity

I troubleshooted this by
fixing security groups and NACL inbound outbound rules 
to allow ipv4 from public security group

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-connectivity_4a9e8014)

---

## Connectivity to the Internet

Curl is  Just like ping, curl is a tool to test connectivity in a network. Where ping checks if one computer can contact another (and how long messages take to travel back and forwth), curl is used to transfer data to or from a server. That means on top of checking connectivity, you can use curl to grab data from, or upload data into other servers on the internet!



I used curl to test the connectivity between  
curl (Client URL) is a command-line tool for transferring data using network protocols, most commonly HTTP, HTTPS, and FTP. Unlike ping (which tests network connectivity at the IP layer), curl tests application-layer connectivity—meaning it actually talks to the web server software (like Apache, Nginx, or a REST API) running on an instance.

### Ping vs Curl

Ping and curl are different because
ping tests network connectivity at the internet layer (IP/ICMP) , while curl tests application connectivity at the application layer (HTTP/HTTPS), much higher up the network stack.

---

## Connectivity to the Internet

I ran the curl command curl se***.** 

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-networks-connectivity_8ee57662)

---

---
