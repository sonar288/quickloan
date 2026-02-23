# 🚀 QuickLoan -- Production-Ready Scalable PHP Web Application on AWS

## 📌 Overview

QuickLoan is a highly available and scalable PHP-based web application
deployed on AWS using modern cloud architecture best practices.

This project demonstrates real-world DevOps implementation including:

-   Custom VPC (Public & Private Subnets)
-   Internet Gateway & NAT Gateway
-   EC2 Deployment (Nginx + PHP 8.2)
-   Amazon RDS (MySQL -- Private Subnet)
-   Application Load Balancer (ALB)
-   Auto Scaling Group (Min: 3 \| Desired: 4 \| Max: 20)
-   Amazon S3 for Static Image Hosting
-   Infrastructure as Code using CloudFormation

------------------------------------------------------------------------

# 📖 Important Note

This repository contains all required source code, configuration files,
and infrastructure templates.

⚠️ However, to fully understand and replicate the complete architecture
end-to-end (including networking setup, scaling configuration, S3
integration, and production best practices), please refer to the
detailed step-by-step blog guide below:

👉 Blog Link:\
https://rahul-sonar.hashnode.dev/quickloan-scalable-php-web-application-on-aws-step-by-step-beginner-guide

The blog provides complete instructions with explanations, screenshots,
and architectural breakdowns to help you recreate the entire project
successfully.

------------------------------------------------------------------------

# 🏗️ Architecture Overview

## 🌍 Deployment Region

-   Region: us-east-1 (N. Virginia)
-   VPC CIDR: 172.20.0.0/16

## 🔁 Traffic Flow

User → Application Load Balancer → EC2 (Auto Scaling Group) → RDS\
User → Amazon S3 (Static Images)

------------------------------------------------------------------------

# 🧰 Tech Stack

-   Frontend: HTML, CSS, JavaScript
-   Backend: PHP 8.2
-   Web Server: Nginx
-   Database: Amazon RDS (MySQL -- db.t3.micro)
-   Static Storage: Amazon S3
-   Load Balancer: Application Load Balancer
-   Scaling: Auto Scaling Group
-   IaC: CloudFormation

------------------------------------------------------------------------

# 📂 Repository Structure

quickloan/ ├── public/ ├── includes/ ├── nginx/ │ └── quickloan.conf ├──
database/ │ └── init.sql ├── infrastructure/ │ └── vpc-ec2.yml └──
README.md

------------------------------------------------------------------------

# 🚀 High-Level Deployment Steps

1.  Clone this repository.
2.  Deploy infrastructure using CloudFormation template.
3.  Launch and configure EC2 with Nginx & PHP.
4.  Configure RDS database.
5.  Deploy application code.
6.  Configure S3 for static image hosting.
7.  Set up ALB and Auto Scaling Group.

For complete detailed commands and explanations, refer to the blog.

------------------------------------------------------------------------
# 🖥️ Demo Screenshots

## 🔹 Application Home Page
![Home Page](img/Home_Page.png)

## 🔹 Form 
![Form](img/form_html_out.png)

## 🔹form submition Success
![Submission Success](img/submit_php.png)

## 🔹 Data Stored in RDS
![Database Output](img/database_store.png)

------------------------------------------------------------------------

# 🛡️ Security Highlights

-   RDS deployed in private subnet
-   No public database access
-   EC2 instances in private subnets
-   Only ALB publicly accessible
-   NAT Gateway for outbound internet access

------------------------------------------------------------------------

# 🎯 Interview Summary

> I deployed a scalable PHP web application on AWS by designing a custom
> VPC with public and private subnets. The application runs on EC2
> instances behind an Application Load Balancer and Auto Scaling Group.
> The database is hosted securely on RDS in a private subnet, and static
> assets are stored in S3 to maintain a stateless architecture.

------------------------------------------------------------------------

# 👨‍💻 Author

Rahul Sonar\
GitHub: https://github.com/sonar288\
Blog: https://rahul-sonar.hashnode.dev
