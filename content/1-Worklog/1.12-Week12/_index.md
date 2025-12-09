---
title: "Week 12 Worklog"
date: "2025-09-09T19:53:52+07:00"
weight: 2
chapter: false
pre: " <b> 1.12. </b> "
---
{{% notice warning %}} 
⚠️ **Note:** The following information is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}}


### Week 12 Objectives:

* Connect and get acquainted with members of First Cloud Journey.
* Understand basic AWS services, how to use the console & CLI.

### Tasks to be carried out this week:
Dưới đây là **3 tuần** Aurora Time project theo đúng format Day/Task/Start Date/Completion Date/Reference Material:

***

## Week 1 – Research & Architecture Design

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ----- | ---------- | ---------------- | ------------------ |
| MON | - Refine business requirements and user stories for Aurora Time (scheduling, reminders, authentication, email notifications).<br>- Define non‑functional requirements: scalability, availability, latency, and cost constraints. | dd/mm/2025 | dd/mm/2025 | Proposal – Executive Summary, Problem Statement |
| TUE | - Design high-level serverless architecture: API Gateway, Lambda, DynamoDB, EventBridge, SES, Cognito, Amplify, S3/CloudFront.<br>- Draw/update the architecture diagram based on the proposal. | dd/mm/2025 | dd/mm/2025 | Proposal – Solution Architecture & AWS Services Used |
| WED | - DynamoDB data modeling: design tables, partition key and sort key for users, events, schedules, and reminders.<br>- Document access patterns (create/update/delete event, list by date/user, query upcoming reminders). | dd/mm/2025 | dd/mm/2025 | Proposal – Technical Implementation Plan (DynamoDB modeling) |
| THU | - Define API contract: list all REST endpoints with methods, request/response schemas, and error patterns.<br>- Map each endpoint to specific Lambda functions and required IAM permissions. | dd/mm/2025 | dd/mm/2025 | Proposal – AWS Lambda, API Gateway, DynamoDB roles |
| FRI | - Draft security & authentication design: Cognito user pools, auth flow, JWT with API Gateway authorizer, basic authorization rules.<br>- Write "Architecture Design v1" (short document) and share with mentor/team for feedback. | dd/mm/2025 | dd/mm/2025 | Proposal – Cognito, Security, ROI & Risks sections |

***

## Week 2 – POC, Backend & Cost Estimation

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ----- | ---------- | ---------------- | ------------------ |
| MON | - Set up Cognito User Pool and test sign‑up/sign‑in flow (hosted UI or simple client).<br>- Inspect ID/Access tokens and plan how backend will read user identity and roles. | dd/mm/2025 | dd/mm/2025 | Proposal – Amazon Cognito & Authentication |
| TUE | - Create initial DynamoDB table(s) according to Week 1 model and perform simple CRUD tests via Console/CLI.<br>- Validate partition key design with sample data, note potential hot‑partition risks. | dd/mm/2025 | dd/mm/2025 | Proposal – DynamoDB usage & data model plan |
| WED | - Build minimal POC: API Gateway + a few Lambda functions (e.g. `CreateEvent`, `ListEvents`) integrated with DynamoDB.<br>- Test end‑to‑end flow (HTTP request → API Gateway → Lambda → DynamoDB) with sample payloads. | dd/mm/2025 | dd/mm/2025 | Proposal – Serverless architecture (API Gateway, Lambda, DynamoDB) |
| THU | - Configure EventBridge rule plus Lambda/SES POC for sending reminder emails on a schedule.<br>- Verify SES identities, limits, and send at least one test reminder email successfully. | dd/mm/2025 | dd/mm/2025 | Proposal – EventBridge & SES reminders |
| FRI | - Use AWS Pricing Calculator to estimate monthly costs for API Gateway, Lambda, DynamoDB, S3, CloudFront, Amplify, Cognito, SES, EventBridge, CloudWatch.<br>- Compare with proposal's estimated range ($16–$50/month) and adjust assumptions if necessary. | dd/mm/2025 | dd/mm/2025 | Proposal – Estimated Infrastructure Cost table |

***

## Week 3 – Optimization, Frontend & Finalization

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ----- | ---------- | ---------------- | ------------------ |
| MON | - Attend an AWS event . | 01/12/2025 | 01/12/2025 |  |
| TUE | - Tune Lambda and DynamoDB: adjust memory, timeout, and concurrency; choose on‑demand vs provisioned RCU/WCU for tables.<br>- Enable CloudWatch metrics and alarms for Lambda errors/throttling and DynamoDB throttling. | 02/11/2025 | 02/11/2025 | Proposal – Technical Implementation Plan (System Optimization)[1] |
| WED | - Harden security: refine IAM roles with least privilege for Lambda, EventBridge, SES, and DynamoDB.<br>- Secure API Gateway (Cognito authorizer, throttling) and set AWS Budgets alerts for the project account. | 03/11/2025 | 03/11/2025 | Proposal – Risks & Mitigation (cost overrun, failures)[1] |
| THU | - Connect frontend (Amplify‑hosted app) to backend APIs: implement pages for login/sign‑up, schedule view, create/edit events, and reminder settings.<br>- Wire frontend to Cognito and API Gateway endpoints and test basic user flows. | 04/11/2025 | 04/11/2025 | Proposal – AWS Amplify, Key Features & Problem Statement |
| FRI | - Run integrated end‑to‑end testing: user auth → create/update/delete events → scheduled reminder emails → view schedules across devices/browsers.<br>- Prepare final deliverables (architecture diagram, cost report, demo script, screenshots) and update worklog with "Lessons Learned & Next Steps". | 06/11/2025 | 07/11/2025 | Proposal – Expected Outcomes & ROI; AWS Well-Architected best practices[1] |

[1](https://aws.amazon.com/architecture/well-architected/)

### Week 12 Achievements:

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
