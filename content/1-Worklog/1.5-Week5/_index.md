---
title: "Week 5 Worklog"
date: "2025-09-09T19:53:52+07:00"
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---



### Week 5 Objectives:

* Connect and get acquainted with members of First Cloud Journey.
* Understand basic AWS services, how to use the console & CLI.

### Tasks to be carried out this week:
Dưới đây là **Week 5** cho module *Using AWS Storage Gateway* (4 video bạn gửi), theo đúng format các tuần trước. Nội dung tập trung vào S3 bucket, EC2 host cho Storage Gateway, cấu hình Storage Gateway và test truy cập.

***

## Week 5 – Worklog (AWS Storage Gateway)
Dưới đây là **Week 5** cho module *Using AWS Storage Gateway* (4 video bạn gửi), theo đúng format các tuần trước. Nội dung tập trung vào S3 bucket, EC2 host cho Storage Gateway, cấu hình Storage Gateway và test truy cập.

***

## Week 5 – Worklog (AWS Storage Gateway)
Dưới đây là **Week 5** cho module *Using AWS Storage Gateway* (4 video bạn gửi), theo đúng format các tuần trước. Nội dung tập trung vào S3 bucket, EC2 host cho Storage Gateway, cấu hình Storage Gateway và test truy cập.

***

## Week 5 – Worklog (AWS Storage Gateway)

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ----- | ---------- | ---------------- | ------------------ |
| MON | - Using AWS Storage Gateway: review the lab overview and main use cases (file/volume/tape gateway, hybrid storage, backup and archiving).[1] <br>- Understand the overall lab architecture (on‑premises VM/EC2 acting as gateway, S3 as backend storage). | 13/10/2025 | 13/10/2025 | https://www.youtube.com/watch?v=Je2jPk7HhLQ&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=88|
| TUE | – Create S3 Bucket” and create the S3 bucket required for the Storage Gateway lab.[2] <br>- Configure basic settings: bucket name, region, encryption (if required), and relevant tags for the lab. | 14/10/2025 | 14/10/2025 | https://www.youtube.com/watch?v=3vSrTeWroSs&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=86[2]|
| WED | – Create EC2 for Storage Gateway” and provision the EC2 instance that will run the Storage Gateway.[3] <br>- Configure networking and Security Groups so the EC2 instance can reach S3 and be managed securely (only required ports allowed). | 15/10/2025 | 15/10/2025 | https://www.youtube.com/watch?v=xVrhpe8OpVU&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=87 |
| THU |– Configure AWS Storage Gateway” (index 88) and activate the gateway using the S3 bucket created earlier.[1] <br>- Configure the appropriate gateway type (for example File or Volume Gateway) according to the lab guide and verify that the gateway status is active. | 16/10/2025 | 16/10/2025 | https://www.youtube.com/watch?v=Je2jPk7HhLQ&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=88[1] |
| FRI |  Test Storage Gateway / Access Data” (index 89) and perform the lab tests (mount share or volume, read/write files, verify data in S3).[1] <br>- Write a short internal note summarizing “How AWS Storage Gateway integrates on‑premises workloads with S3 and when to use it in real projects”. | 17/10/2025 | 17/10/2025 | https://www.youtube.com/watch?v=3Zp9GSMO-VI&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=89 |

[1](https://awsstudygroup.com)
[2](https://www.youtube.com/watch?v=3vSrTeWroSs&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=86)
[3](https://www.youtube.com/watch?v=xVrhpe8OpVU&list=P)


### Week 5 Achievements:

* Understood what AWS is and mastered the basic service groups: 
  * Compute
  * Storage
  * Networking 
  * Database
  * ...

* Successfully created and configured an AWS Free Tier account.

* Became familiar with the AWS Management Console and learned how to find, access, and use services via the web interface.

* Installed and configured AWS CLI on the computer, including:
  * Access Key
  * Secret Key
  * Default Region
  * ...

* Used AWS CLI to perform basic operations such as:

  * Check account & configuration information
  * Retrieve the list of regions
  * View EC2 service
  * Create and manage key pairs
  * Check information about running services
  * ...

* Acquired the ability to connect between the web interface and CLI to manage AWS resources in parallel.
* ...
