Project 1: Deploy a Static Portfolio Website Using Amazon S3

Project Overview

This project demonstrates the deployment of a static personal portfolio website using Amazon S3 Static Website Hosting.

The portfolio website is stored in an Amazon S3 bucket and made publicly accessible through the S3 website endpoint. The project demonstrates cloud storage, static website hosting, bucket permissions, and public object access.

Objectives

Learn how to host a static website using Amazon S3.

Understand cloud storage and static website hosting.

Configure S3 bucket permissions.

Configure an S3 static website endpoint.

Deploy a personal portfolio website in the AWS cloud.

Gain practical hands-on experience with AWS deployment.

Technologies Used

HTML

CSS

JavaScript

Amazon S3

Git

GitHub

AWS Configuration

Configuration

Value

AWS Service

Amazon S3

Bucket Name

personalportfolio2026

AWS Region

US East (Ohio) - us-east-2

Hosting Type

Bucket hosting

Static Website Hosting

Enabled

Index Document

index.html

Error Document

404.html

Project Structure

portfolio-aws-s3/
│
├── images/
│   └── portfolio images
│
├── screenshots/
│   ├── AWS-01-bucket-permissions.png
│   ├── AWS-02-uploaded-files.png
│   ├── AWS-03-index-object.png
│   └── AWS-04-bucket-policy.png
│
├── index.html
├── style.css
├── script.js
├── 404.html
└── README.md

Deployment Steps

1. Create an S3 Bucket

Created an S3 bucket with the following name:

personalportfolio2026

The bucket was created in:

US East (Ohio)
us-east-2

2. Upload Website Files

The portfolio website files were uploaded to the S3 bucket.

Important files include:

index.html
404.html
style.css
script.js
images/

3. Enable Static Website Hosting

Static website hosting was enabled from:

S3
→ Bucket
→ Properties
→ Static website hosting

The following configuration was used:

Index document: index.html
Error document: 404.html

4. Configure Public Access

For the S3 website endpoint approach, public access blocking was configured so that the bucket policy could provide public read access to the website objects.

5. Configure Bucket Policy

The following bucket policy was configured:

{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::personalportfolio2026/*"
    }
  ]
}

6. Verify Website

The S3 website endpoint was used to verify that the portfolio website is accessible online.

Live Website URL

http://personalportfolio2026.s3-website.us-east-2.amazonaws.com

Make sure this URL opens successfully before submitting the project.

GitHub Repository

Add your GitHub repository URL here:

YOUR_GITHUB_REPOSITORY_URL

Example:

https://github.com/YOUR_USERNAME/portfolio-aws-s3

Screenshots

1. S3 Bucket Permissions

This screenshot shows that Block all public access is Off and the bucket policy is configured.



2. Uploaded Website Files

This screenshot shows the website files stored inside the S3 bucket.



3. index.html Object

This screenshot shows the index.html object and its S3 object details.



4. Bucket Policy

This screenshot shows the bucket policy used to allow public s3:GetObject access.



Important Concepts Learned

Amazon S3

Amazon S3 is an object storage service used to store and retrieve data as objects inside buckets.

Static Website Hosting

S3 can serve static website files such as:

HTML
CSS
JavaScript
Images

Bucket Policy

A bucket policy is a JSON-based resource policy that controls access to objects stored in an S3 bucket.

In this project:

Principal: *
Action: s3:GetObject

allows public users to read the website objects.

Block Public Access

S3 Block Public Access provides protection against public access configurations.

For this learning project, it was configured so that the public-read bucket policy required by the S3 website endpoint could take effect.

Verification Checklist

S3 bucket created

Website files uploaded

index.html uploaded

404.html uploaded

Static website hosting enabled

Index document configured

Error document configured

Bucket policy configured

Website opens successfully

GitHub repository created

Source code pushed to GitHub

README added

Screenshots added

GitHub repository URL verified

Live website URL verified

Conclusion

The static portfolio website was successfully configured for deployment using Amazon S3 Static Website Hosting. The project demonstrates the practical use of S3 buckets, static website hosting, object permissions, bucket policies, and public website endpoints.

The completed project provides hands-on experience with deploying a real static website on AWS.
