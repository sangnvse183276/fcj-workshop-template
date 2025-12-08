---
title: "Worklog Tuần 9"
date: "2025-09-09T19:53:52+07:00"
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 9:

* Kết nối, làm quen với các thành viên trong First Cloud Journey.
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:
| Ngày    | Nhiệm vụ                                                                                                                                                                                                                                                                         | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo                                                 |
| ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------------------------------ |
| Thứ Hai | - Thiết lập Cognito User Pool cơ bản và kiểm thử luồng user sign-up/sign-in (hosted UI hoặc client test đơn giản). - Xác minh cấu trúc token và cách API sẽ đọc danh tính/claims của người dùng.                                                                                 | 10/11/2025   | 10/11/2025      | Proposal – Cognito & Authentication                                |
| Thứ Ba  | - Tạo bảng DynamoDB ban đầu theo mô hình của Tuần 1 và thực hiện các test CRUD đơn giản qua AWS Console/CLI. - Xác thực thiết kế partition key với workload mẫu và ghi chú rủi ro hot partition.                                                                                 | 11/11/2025   | 11/11/2025      | Proposal – DynamoDB usage & data model plan                        |
| Thứ Tư  | - Xây dựng POC tối thiểu: API Gateway + 1–2 Lambda function (ví dụ CreateEvent, ListEvents) tích hợp với DynamoDB. - Kiểm thử luồng end-to-end (HTTP request → API Gateway → Lambda → DynamoDB) với dữ liệu test.                                                                | 12/11/2025   | 12/11/2025      | Proposal – Serverless architecture (API Gateway, Lambda, DynamoDB) |
| Thứ Năm | - Cấu hình EventBridge rule + Lambda/SES POC để gửi email nhắc việc theo lịch (rule và template test đơn giản). - Kiểm tra giới hạn gửi của SES và xác minh email/tên miền gửi.                                                                                                  | 13/11/2025   | 13/11/2025      | Proposal – EventBridge & SES reminders                             |
| Thứ Sáu | - Dùng AWS Pricing Calculator để ước tính chi phí hàng tháng cho các dịch vụ chính (API Gateway, Lambda, DynamoDB, S3, CloudFront, Amplify, Cognito, SES, EventBridge, CloudWatch). - So sánh ước tính với khoảng 16–50 USD/tháng trong proposal và điều chỉnh giả định nếu cần. | 14/11/2025   | 14/11/2025      | Proposal – Estimated Infrastructure Cost table                     |


### Kết quả đạt được tuần 9:

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


