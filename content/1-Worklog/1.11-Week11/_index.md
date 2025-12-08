---
title: "Week 11 Worklog"
date: "2025-09-09T19:53:52+07:00"
weight: 2
chapter: false
pre: " <b> 1.11. </b> "
---
{{% notice warning %}} 
⚠️ **Note:** The following information is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}}


### Week 11 Objectives:

* Connect and get acquainted with members of First Cloud Journey.
* Understand basic AWS services, how to use the console & CLI.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                                                                    | Start Date | Completion Date | Reference Material                                                 |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ------------------------------------------------------------------ |
| MON | - Set up Cognito User Pool and test sign‑up/sign‑in flow (hosted UI or simple client).- Inspect ID/Access tokens and plan how backend will read user identity and roles.                                                                                | 24/11/2025 | 24/11/2025      | Proposal – Amazon Cognito & Authentication                         |
| TUE | - Create initial DynamoDB table(s) according to Week 1 model and perform simple CRUD tests via Console/CLI.- Validate partition key design with sample data, note potential hot‑partition risks.                                                        | 25/11/2025 | 25/11/2025      | Proposal – DynamoDB usage & data model plan                        |
| WED | - Build minimal POC: API Gateway + a few Lambda functions (e.g. CreateEvent, ListEvents) integrated with DynamoDB.- Test end‑to‑end flow (HTTP request → API Gateway → Lambda → DynamoDB) with sample payloads.                                         | 26/11/2025 | 26/11/2025      | Proposal – Serverless architecture (API Gateway, Lambda, DynamoDB) |
| THU | - Configure EventBridge rule plus Lambda/SES POC for sending reminder emails on a schedule.- Verify SES identities, limits, and send at least one test reminder email successfully.                                                                     | 27/11/2025 | 27/11/2025      | Proposal – EventBridge & SES reminders                             |
| FRI | - Use AWS Pricing Calculator to estimate monthly costs for API Gateway, Lambda, DynamoDB, S3, CloudFront, Amplify, Cognito, SES, EventBridge, CloudWatch.| 28/11/2025 | 28/11/2025      | Proposal – Estimated Infrastructure Cost table                     |


### Week 11 Achievements:

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
