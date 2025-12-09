---
title: "Week 9 Worklog"
date: "2025-09-09T19:53:52+07:00"
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---
{{% notice warning %}} 
⚠️ **Note:** The following information is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}}


### Week 9 Objectives:

* Connect and get acquainted with members of First Cloud Journey.
* Understand basic AWS services, how to use the console & CLI.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                                                                              | Start Date | Completion Date | Reference Material                                                 |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ------------------------------------------------------------------ |
| MON | - Set up basic Cognito User Pool and test user sign-up/sign-in flow (hosted UI or simple test client).- Verify token structure and how APIs will read user identity/claims.                                                                                       | 10/11/2025 | 10/11/2025      | Proposal – Cognito & Authentication                                |
| TUE | - Create initial DynamoDB table(s) according to Week 1 model and perform simple CRUD tests via AWS Console/CLI.- Validate partition key design with sample workloads and note hot-partition risks.                                                                | 11/11/2025 | 11/11/2025      | Proposal – DynamoDB usage & data model plan                        |
| WED | - Build a minimal POC: API Gateway + 1–2 Lambda functions (e.g. CreateEvent, ListEvents) integrated with DynamoDB.- Test end-to-end flow (HTTP request → API Gateway → Lambda → DynamoDB) using test data.                                                        | 12/11/2025 | 12/11/2025      | Proposal – Serverless architecture (API Gateway, Lambda, DynamoDB) |
| THU | - Configure EventBridge rule + Lambda/SES POC for sending reminder emails on a schedule (simple test rule and template).- Validate SES sending limits and verify sender emails/domains.                                                                           | 13/11/2025 | 13/11/2025      | Proposal – EventBridge & SES reminders                             |
| FRI | - Use AWS Pricing Calculator to estimate monthly cost for key services (API Gateway, Lambda, DynamoDB, S3, CloudFront, Amplify, Cognito, SES, EventBridge, CloudWatch). | 14/11/2025 | 14/11/2025      | Proposal – Estimated Infrastructure Cost table                     |m/> |


### Week 9 Achievements:

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
