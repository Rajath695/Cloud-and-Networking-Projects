<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Host a Website on Amazon S3

**Project Link:** [View Project](http://nextwork.ai/projects/aws-host-a-website-on-s3)

**Author:**   Rajath Noor  
**Email:**  raj****@gmail.com

---

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Introducing Today's Project!

### Project overview

### Tools and concepts

Services I used were... Key concepts I learnt include...

### Time, challenges, and wins

This project took me approximately 40 mins... The most challenging part was using it first time... It was most rewarding to myself...

---

## How I Set Up an S3 Bucket

### What I did in this step

### How long it took to create the bucket

Creating an S3 bucket took me...5mins

### Region selection

i picked mumbai region because it is the nearest one


### Understanding bucket name uniqueness

S3 bucket names are globally unique! This means...
all account has that

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-host-a-website-on-s3_ba6d42ad)

---

## Upload Website Files to S3

### What I did in this step

In this step, I will add the website files inside the bucket

### Files I uploaded

I uploaded two files to my S3 bucket - they were...
index.html,nextworks.xip folder 

### How the files work together

Both files are necessary for this project as...
because index.html provides the main
and other files shows the other contents 

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-host-a-website-on-s3_a265af88)

---

## Static Website Hosting on S3

### What I did in this step

In this step, I will. configure the s3 bucket for static wehsite hosting

### Understanding website hosting

Website hosting means...
get available in the public internet by owning a private ownership space 

### How I enabled website hosting

To enable website hosting with my S3 bucket, I...static website hosting settings

### Access Control Lists (ACLs)

An ACL is...Access  control List which defines who accesss your S3 bucket files

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-host-a-website-on-s3_c22c54c0)

---

## Bucket Endpoints

### Understanding bucket endpoint URLs

Once static website is enabled, S3 produces a bucket endpoint URL, which is...A bucket website endpoint is just like a regular website URL. It lets people visit your S3 bucket's files as a website

### What I saw when I tested the endpoint

When I first visited the bucket endpoint URL, I saw... The reason for this error was...403 forbidden

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-host-a-website-on-s3_22ce4daf)

---

## Success!

### What I did in this step

In this step, I will... because...make the web files in s3 bucket publcly accessible

### How I resolved the 403 error

To resolve this 403 Forbidden error, I...by access to public acl

![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Bucket Policies

### What I did in this extension

In this project extension I'm about to... I'm doing this so that...
avoid users from deleting incex.html


### Understanding bucket policies

An alternative to ACLs are bucket policies, which are... The benefit of using bucket policies is... while ACLs are useful for...


![Image](http://nextwork.ai/amused_pink_quiet_peafowl/uploads/aws-host-a-website-on-s3_sm2sm2sm)

### What my bucket policy does

My bucket policy... I tested this by... and saw...
avoid delete the specific file for anyone

---

---
