<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Website Delivery with CloudFront

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-cloudfront)

**Author:** Mark Isaac  
**Email:** markisaac695@gmail.com

---

## Website Delivery with CloudFront

---

## Introducing Today's Project!

In this project, I will demonstrate Three tier arch. I'm doing this project to learn about how can a website including frontend , backend and database comunciate each other to represent  abeautiful website wit low latency 

### Tools and concepts

### Project reflection

---

## Set Up S3 and Website Files

I started the project by creating an S3 bucket to store our files. I can't use CloudFront for this task because CloudFront is not a storage service 

The three files that make up my website are index.html, which act as main entry point for my website containg all attributed and elements ,style.css which act as responsie and colorful part of the website (colors,design etc) and script.js, which act as brain of the website have all function that user my interact with

I validated that my website files work by opnening each file and saw the code of the . and for index.html it open in  my vrowser

![Image](http://learn.nextwork.org/vibrant_pink_mysterious_chico/uploads/aws-networks-cloudfront_qgo7wcd3)

---

## Exploring Amazon CloudFront

Amazon CloudFront is a content delivery network, which means it speeds up the distriobution of your statc files. Businesses and developers use CloudFront because it imporves performances and ensure a low latency connection

To use Amazon CloudFront, you set up distributions, which are like settings or instructions to my CDN. I set up a distribution for my CDN so that it knows what do if my file requsted not in cached. The origin is like the warehouse of your data in my case it is S3 bucket that itr acts as my warehouse

My CloudFront distribution's default root object is index.html . This means when someone visits my url they will see the content my webpage

![Image](http://learn.nextwork.org/vibrant_pink_mysterious_chico/uploads/aws-networks-cloudfront_qgo7wcdt)

---

## Handling Access Issues

When I tried visiting my distributed website, I ran into an access denied error because i didnt give my CDN permission to access S3 bucket files

To resolve the error, I set up origin access control (OAC). OAC is like a sepcial user that says "hey the S3 bucket stays private and inaccessible to the world, but CloudFront is allowed to access the files.”

![Image](http://learn.nextwork.org/vibrant_pink_mysterious_chico/uploads/aws-networks-cloudfront_egrhntyu)

---

## Updating S3 Permissions

Once I set up my OAC, I still needed to update my bucket policy because its objects are still private to anyone including cloudfront

Creating an OAC automatically gives me a policy I could copy, which grants me access to paste in S3 bucket policy to accees it

![Image](http://learn.nextwork.org/vibrant_pink_mysterious_chico/uploads/aws-networks-cloudfront_eg98ntyu)

---

## S3 vs CloudFront for Hosting

---

## S3 vs CloudFront Load Times

---

---
