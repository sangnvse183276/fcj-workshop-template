---
title: "Week 8 Worklog"
date: "2025-09-09T19:53:52+07:00"
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---


### Week 8 Objectives:

* Connect and get acquainted with members of First Cloud Journey.
* Understand basic AWS services, how to use the console & CLI.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                                                                  | Start Date | Completion Date | Reference Material                                           |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ------------------------------------------------------------ |
| MON | - Refine business requirements and user stories for Aurora Time (scheduling, reminders, authentication, email notifications).- Define non-functional requirements: scalability, availability, latency, cost constraints.                              | 03/11/2025 | 03/11/2025      | Proposal document (Executive Summary, Problem Statement)     |
| TUE | - Design high-level serverless architecture: API Gateway + Lambda + DynamoDB + EventBridge + SES + Cognito + Amplify + S3/CloudFront.- Draw architecture diagram and align with the “Solution Architecture” section of the proposal.                  | 04/11/2025 | 04/11/2025      | Proposal – Solution Architecture & AWS Services Used         |
| WED | - DynamoDB data modeling: design tables/PK/SK for users, events, schedules, reminder rules (consider access patterns: list events, create/update/delete, query by date/user).- Document partition key/sort key choices and expected RCU/WCU patterns. | 05/11/2025 | 05/11/2025      | Proposal – Technical Implementation Plan (DynamoDB modeling) |
| THU | - Define API contract for backend: list all REST endpoints (e.g. /events, /events/{id}, /reminders) with methods, request/response schema, error codes.- Map each endpoint to Lambda functions and identify required IAM permissions.                 | 06/11/2025 | 06/11/2025      | Proposal – AWS Lambda, API Gateway, DynamoDB roles           |
| FRI | - Attend an AWS event | 07/11/2025 | 07/11/2025      |         |
### Week 8 Achievements:

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
