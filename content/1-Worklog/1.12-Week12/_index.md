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
