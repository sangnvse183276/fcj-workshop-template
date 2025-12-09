    ---
    title : "Các bước chuẩn bị"
    date :  "2025-09-09T19:53:52+07:00" 
    weight : 2
    chapter : false
    pre : " <b> 5.2. </b> "
    ---

    #### IAM permissions
    Gắn IAM permission policy sau vào tài khoản aws user của bạn để triển khai và dọn dẹp tài nguyên trong workshop này.
    ```
    {
        "Version": "2012-10-17",
        "Statement": [
            {
                "Sid": "VisualEditor0",
                "Effect": "Allow",
                "Action": [
                    "cloudformation:*",
                    "cloudwatch:*",
                    "ec2:AcceptTransitGatewayPeeringAttachment",
                    "ec2:AcceptTransitGatewayVpcAttachment",
                    "ec2:AllocateAddress",
                    "ec2:AssociateAddress",
                    "ec2:AssociateIamInstanceProfile",
                    "ec2:AssociateRouteTable",
                    "ec2:AssociateSubnetCidrBlock",
                    "ec2:AssociateTransitGatewayRouteTable",
                    "ec2:AssociateVpcCidrBlock",
                    "ec2:AttachInternetGateway",
                    "ec2:AttachNetworkInterface",
                    "ec2:AttachVolume",
                    "ec2:AttachVpnGateway",
                    "ec2:AuthorizeSecurityGroupEgress",
                    "ec2:AuthorizeSecurityGroupIngress",
                    "ec2:CreateClientVpnEndpoint",
                    "ec2:CreateClientVpnRoute",
                    "ec2:CreateCustomerGateway",
                    "ec2:CreateDhcpOptions",
                    "ec2:CreateFlowLogs",
                    "ec2:CreateInternetGateway",
                    "ec2:CreateLaunchTemplate",
                    "ec2:CreateNetworkAcl",
                    "ec2:CreateNetworkInterface",
                    "ec2:CreateNetworkInterfacePermission",
                    "ec2:CreateRoute",
                    "ec2:CreateRouteTable",
                    "ec2:CreateSecurityGroup",
                    "ec2:CreateSubnet",
                    "ec2:CreateSubnetCidrReservation",
                    "ec2:CreateTags",
                    "ec2:CreateTransitGateway",
                    "ec2:CreateTransitGatewayPeeringAttachment",
                    "ec2:CreateTransitGatewayPrefixListReference",
                    "ec2:CreateTransitGatewayRoute",
                    "ec2:CreateTransitGatewayRouteTable",
                    "ec2:CreateTransitGatewayVpcAttachment",
                    "ec2:CreateVpc",
                    "ec2:CreateVpcEndpoint",
                    "ec2:CreateVpcEndpointConnectionNotification",
                    "ec2:CreateVpcEndpointServiceConfiguration",
                    "ec2:CreateVpnConnection",
                    "ec2:CreateVpnConnectionRoute",
                    "ec2:CreateVpnGateway",
                    "ec2:DeleteCustomerGateway",
                    "ec2:DeleteFlowLogs",
                    "ec2:DeleteInternetGateway",
                    "ec2:DeleteNetworkInterface",
                    "ec2:DeleteNetworkInterfacePermission",
                    "ec2:DeleteRoute",
                    "ec2:DeleteRouteTable",
                    "ec2:DeleteSecurityGroup",
                    "ec2:DeleteSubnet",
                    "ec2:DeleteSubnetCidrReservation",
                    "ec2:DeleteTags",
                    "ec2:DeleteTransitGateway",
                    "ec2:DeleteTransitGatewayPeeringAttachment",
                    "ec2:DeleteTransitGatewayPrefixListReference",
                    "ec2:DeleteTransitGatewayRoute",
                    "ec2:DeleteTransitGatewayRouteTable",
                    "ec2:DeleteTransitGatewayVpcAttachment",
                    "ec2:DeleteVpc",
                    "ec2:DeleteVpcEndpoints",
                    "ec2:DeleteVpcEndpointServiceConfigurations",
                    "ec2:DeleteVpnConnection",
                    "ec2:DeleteVpnConnectionRoute",
                    "ec2:Describe*",
                    "ec2:DetachInternetGateway",
                    "ec2:DisassociateAddress",
                    "ec2:DisassociateRouteTable",
                    "ec2:GetLaunchTemplateData",
                    "ec2:GetTransitGatewayAttachmentPropagations",
                    "ec2:ModifyInstanceAttribute",
                    "ec2:ModifySecurityGroupRules",
                    "ec2:ModifyTransitGatewayVpcAttachment",
                    "ec2:ModifyVpcAttribute",
                    "ec2:ModifyVpcEndpoint",
                    "ec2:ReleaseAddress",
                    "ec2:ReplaceRoute",
                    "ec2:RevokeSecurityGroupEgress",
                    "ec2:RevokeSecurityGroupIngress",
                    "ec2:RunInstances",
                    "ec2:StartInstances",
                    "ec2:StopInstances",
                    "ec2:UpdateSecurityGroupRuleDescriptionsEgress",
                    "ec2:UpdateSecurityGroupRuleDescriptionsIngress",
                    "iam:AddRoleToInstanceProfile",
                    "iam:AttachRolePolicy",
                    "iam:CreateInstanceProfile",
                    "iam:CreatePolicy",
                    "iam:CreateRole",
                    "iam:DeleteInstanceProfile",
                    "iam:DeletePolicy",
                    "iam:DeleteRole",
                    "iam:DeleteRolePolicy",
                    "iam:DetachRolePolicy",
                    "iam:GetInstanceProfile",
                    "iam:GetPolicy",
                    "iam:GetRole",
                    "iam:GetRolePolicy",
                    "iam:ListPolicyVersions",
                    "iam:ListRoles",
                    "iam:PassRole",
                    "iam:PutRolePolicy",
                    "iam:RemoveRoleFromInstanceProfile",
                    "lambda:CreateFunction",
                    "lambda:DeleteFunction",
                    "lambda:DeleteLayerVersion",
                    "lambda:GetFunction",
                    "lambda:GetLayerVersion",
                    "lambda:InvokeFunction",
                    "lambda:PublishLayerVersion",
                    "logs:CreateLogGroup",
                    "logs:DeleteLogGroup",
                    "logs:DescribeLogGroups",
                    "logs:PutRetentionPolicy",
                    "route53:ChangeTagsForResource",
                    "route53:CreateHealthCheck",
                    "route53:CreateHostedZone",
                    "route53:CreateTrafficPolicy",
                    "route53:DeleteHostedZone",
                    "route53:DisassociateVPCFromHostedZone",
                    "route53:GetHostedZone",
                    "route53:ListHostedZones",
                    "route53domains:ListDomains",
                    "route53domains:ListOperations",
                    "route53domains:ListTagsForDomain",
                    "route53resolver:AssociateResolverEndpointIpAddress",
                    "route53resolver:AssociateResolverRule",
                    "route53resolver:CreateResolverEndpoint",
                    "route53resolver:CreateResolverRule",
                    "route53resolver:DeleteResolverEndpoint",
                    "route53resolver:DeleteResolverRule",
                    "route53resolver:DisassociateResolverEndpointIpAddress",
                    "route53resolver:DisassociateResolverRule",
                    "route53resolver:GetResolverEndpoint",
                    "route53resolver:GetResolverRule",
                    "route53resolver:ListResolverEndpointIpAddresses",
                    "route53resolver:ListResolverEndpoints",
                    "route53resolver:ListResolverRuleAssociations",
                    "route53resolver:ListResolverRules",
                    "route53resolver:ListTagsForResource",
                    "route53resolver:UpdateResolverEndpoint",
                    "route53resolver:UpdateResolverRule",
                    "s3:AbortMultipartUpload",
                    "s3:CreateBucket",
                    "s3:DeleteBucket",
                    "s3:DeleteObject",
                    "s3:GetAccountPublicAccessBlock",
                    "s3:GetBucketAcl",
                    "s3:GetBucketOwnershipControls",
                    "s3:GetBucketPolicy",
                    "s3:GetBucketPolicyStatus",
                    "s3:GetBucketPublicAccessBlock",
                    "s3:GetObject",
                    "s3:GetObjectVersion",
                    "s3:GetBucketVersioning",
                    "s3:ListAccessPoints",
                    "s3:ListAccessPointsForObjectLambda",
                    "s3:ListAllMyBuckets",
                    "s3:ListBucket",
                    "s3:ListBucketMultipartUploads",
                    "s3:ListBucketVersions",
                    "s3:ListJobs",
                    "s3:ListMultipartUploadParts",
                    "s3:ListMultiRegionAccessPoints",
                    "s3:ListStorageLensConfigurations",
                    "s3:PutAccountPublicAccessBlock",
                    "s3:PutBucketAcl",
                    "s3:PutBucketPolicy",
                    "s3:PutBucketPublicAccessBlock",
                    "s3:PutObject",
                    "secretsmanager:CreateSecret",
                    "secretsmanager:DeleteSecret",
                    "secretsmanager:DescribeSecret",
                    "secretsmanager:GetSecretValue",
                    "secretsmanager:ListSecrets",
                    "secretsmanager:ListSecretVersionIds",
                    "secretsmanager:PutResourcePolicy",
                    "secretsmanager:TagResource",
                    "secretsmanager:UpdateSecret",
                    "sns:ListTopics",
                    "ssm:DescribeInstanceProperties",
                    "ssm:DescribeSessions",
                    "ssm:GetConnectionStatus",
                    "ssm:GetParameters",
                    "ssm:ListAssociations",
                    "ssm:ResumeSession",
                    "ssm:StartSession",
                    "ssm:TerminateSession"
                ],
                "Resource": "*"
            }
        ]
    }

    ```

    #### Khởi tạo tài nguyên bằng CloudFormation

    Trong lab này, chúng ta sẽ dùng N.Virginia region (us-east-1).

    Để chuẩn bị cho môi trường làm workshop, chúng ta deploy CloudFormation template sau (click link): [PrivateLinkWorkshop ](https://us-east-1.console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/quickcreate?templateURL=https://s3.us-east-1.amazonaws.com/reinvent-endpoints-builders-session/Nested.yaml&stackName=PLCloudSetup). Để nguyên các lựa chọn mặc định.

    ![create stack](/images/5-Workshop/5.2-Prerequisite/create-stack1.png)

    + Lựa chọn 2 mục acknowledgement 
    + Chọn Create stack

    ![create stack](/images/5-Workshop/5.2-Prerequisite/create-stack2.png)

    Quá trình triển khai CloudFormation cần khoảng 15 phút để hoàn thành.

    ![complete](/images/5-Workshop/5.2-Prerequisite/complete.png)

    + 2 VPCs đã được tạo

    ![vpcs](/images/5-Workshop/5.2-Prerequisite/vpcs.png)

    + 3 EC2s đã được tạo

    ![EC2](/images/5-Workshop/5.2-Prerequisite/ec2.png)```md
---
title : "Các bước chuẩn bị"
date : "2025-09-09T19:53:52+07:00"
weight : 2
chapter : false
pre : " <b> 5.2. </b> "
---

#### IAM permissions

Để triển khai và dọn dẹp toàn bộ tài nguyên của Aurora Time, bạn nên làm việc dưới **một IAM user/role chuyên cho lab** với quyền đủ dùng cho các dịch vụ serverless sau: Lambda, API Gateway, DynamoDB, EventBridge, SES, Cognito, S3, CloudFront, Amplify, CloudWatch và IAM (PassRole cho Lambda). Các quyền này tương đương một role dùng cho workshop serverless web app trên AWS.[web:111]

Nếu không dùng quyền AdministratorAccess, bạn có thể tạo một IAM policy tuỳ chỉnh với các nhóm quyền chính:

- `lambda:*` cho việc tạo/xoá/cập nhật hàm Lambda và xem log.  
- `apigateway:*` cho việc tạo REST API, stage và deployment.  
- `dynamodb:*` cho việc tạo bảng và CRUD dữ liệu lab.  
- `events:*` và `ses:*` cho EventBridge rule/Scheduler và gửi email nhắc việc.  
- `cognito-idp:*` cho Cognito User Pool, `amplify:*`, `s3:*`, `cloudfront:*` cho frontend, và một số quyền `cloudwatch:*`, `logs:*` để theo dõi hệ thống.[web:282][web:259]

Ví dụ, bạn có thể tạo một policy tên **AuroraTimeWorkshopPolicy**, gán cho IAM user/role dùng riêng cho workshop này, sau khi kết thúc có thể detach hoặc xoá role để giảm rủi ro bảo mật.

---

#### Cấu hình region và công cụ dòng lệnh

Trong workshop này, bạn nên chọn **một region cố định** cho toàn bộ tài nguyên, ví dụ:

- `ap-southeast-1` (Singapore) hoặc  
- `us-east-1` (N. Virginia)

Điều này giúp các dịch vụ như Lambda, API Gateway, DynamoDB, Cognito, EventBridge và SES hoạt động cùng vùng, giảm độ trễ và đơn giản hoá cấu hình.[web:111]

Các bước chuẩn bị:

1. Cài đặt **AWS CLI** trên máy cá nhân và chạy `aws configure` để thiết lập Access key, Secret key và region mặc định trùng với region bạn chọn cho Aurora Time.  
2. Đảm bảo bạn đã cài sẵn **Node.js** (hoặc runtime bạn dùng cho Lambda) và một trình quản lý mã nguồn (Git) để làm việc với mã frontend/back‑end.

---

#### Chuẩn bị dịch vụ nền tảng cho Aurora Time

Trước khi vào các bài lab chi tiết, bạn nên kiểm tra nhanh các dịch vụ cốt lõi:

+ **SES**:  
  - Vào Amazon SES trong region đã chọn, verify ít nhất một địa chỉ email gửi, và (nếu còn ở sandbox) verify luôn email nhận.  
  - Điều này cần thiết để gửi được email nhắc việc bằng EventBridge + SES.[web:259][web:289]

+ **Cognito**:  
  - Tạo sẵn (hoặc lên kế hoạch tạo) một **User Pool** cho Aurora Time, dùng để đăng ký/đăng nhập người dùng và phát hành JWT cho API Gateway.  
  - Bạn sẽ cấu hình chi tiết trong phần security & authentication sau, nhưng ở bước chuẩn bị nên quyết định luôn naming convention (ví dụ: `aurora-time-user-pool`).[web:295]

+ **Amplify & S3/CloudFront**:  
  - Chuẩn bị sẵn một Git repository chứa mã frontend (React, Vue, v.v.).  
  - Đảm bảo bạn có quyền tạo Amplify App để deploy frontend tĩnh lên S3 và phân phối bằng CloudFront theo hướng dẫn của AWS cho serverless web app.[web:111][web:283]

Sau khi hoàn thành các bước trên, bạn đã sẵn sàng bắt đầu các phần tiếp theo của workshop Aurora Time: thiết kế mô hình DynamoDB, triển khai Lambda + API Gateway, cấu hình EventBridge/SES cho reminders và kết nối frontend qua Amplify.
```