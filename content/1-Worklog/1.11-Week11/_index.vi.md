---
title: "Worklog Tuần 11"
date: "2025-09-09T19:53:52+07:00"
weight: 2
chapter: false
pre: " <b> 1.11. </b> "
---



### Mục tiêu tuần 11:

* Kết nối, làm quen với các thành viên trong First Cloud Journey.
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:
| Ngày    | Nhiệm vụ                                                                                                                                                                                                             | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo                                                 |
| ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------------------------------ |
| Thứ Hai | - Thiết lập Cognito User Pool và kiểm thử luồng sign‑up/sign‑in (hosted UI hoặc client đơn giản). - Kiểm tra ID/Access token và lên kế hoạch cách backend sẽ đọc danh tính và vai trò (roles) của người dùng.        | 24/11/2025   | 24/11/2025      | Proposal – Amazon Cognito & Authentication                         |
| Thứ Ba  | - Tạo bảng DynamoDB ban đầu theo mô hình Tuần 1 và thực hiện các test CRUD đơn giản qua Console/CLI. - Xác thực thiết kế partition key với dữ liệu mẫu, ghi chú các rủi ro hot partition tiềm ẩn.                    | 25/11/2025   | 25/11/2025      | Proposal – DynamoDB usage & data model plan                        |
| Thứ Tư  | - Xây dựng POC tối thiểu: API Gateway + một vài Lambda function (ví dụ CreateEvent, ListEvents) tích hợp với DynamoDB. - Kiểm thử luồng end‑to‑end (HTTP request → API Gateway → Lambda → DynamoDB) với payload mẫu. | 26/11/2025   | 26/11/2025      | Proposal – Serverless architecture (API Gateway, Lambda, DynamoDB) |
| Thứ Năm | - Cấu hình EventBridge rule cùng với Lambda/SES POC để gửi email nhắc việc theo lịch. - Xác minh danh tính SES, giới hạn gửi và gửi thành công ít nhất một email nhắc việc test.                                     | 27/11/2025   | 27/11/2025      | Proposal – EventBridge & SES reminders                             |
| Thứ Sáu | - Sử dụng AWS Pricing Calculator để ước tính chi phí hàng tháng cho API Gateway, Lambda, DynamoDB, S3, CloudFront, Amplify, Cognito, SES, EventBridge, CloudWatch.                                                   | 28/11/2025   | 28/11/2025      | Proposal – Estimated Infrastructure Cost table                     |
### Kết quả đạt được tuần 11:

* Hiểu AWS là gì và nắm được các nhóm dịch vụ cơ bản: 
  * Compute
  * Storage
  * Networking 
  * Database
  * ...

* Đã tạo và cấu hình AWS Free Tier account thành công.

* Làm quen với AWS Management Console và biết cách tìm, truy cập, sử dụng dịch vụ từ giao diện web.

* Cài đặt và cấu hình AWS CLI trên máy tính bao gồm:
  * Access Key
  * Secret Key
  * Region mặc định
  * ...

* Sử dụng AWS CLI để thực hiện các thao tác cơ bản như:

  * Kiểm tra thông tin tài khoản & cấu hình
  * Lấy danh sách region
  * Xem dịch vụ EC2
  * Tạo và quản lý key pair
  * Kiểm tra thông tin dịch vụ đang chạy
  * ...

* Có khả năng kết nối giữa giao diện web và CLI để quản lý tài nguyên AWS song song.
* ...


