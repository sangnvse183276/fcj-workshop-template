---
title: "Worklog Tuần 12"
date: "2025-09-09T19:53:52+07:00"
weight: 2
chapter: false
pre: " <b> 1.12 </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 12:

* Kết nối, làm quen với các thành viên trong First Cloud Journey.
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:
| Ngày    | Nhiệm vụ                                                                                                                                                                                                                                                                                            | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo                                                                 |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ---------------------------------------------------------------------------------- |
| Thứ Hai |  Tham gia một sự kiện AWS                             | 01/12/2025   | 01/12/2025      |  |
| Thứ Ba  | - Tinh chỉnh Lambda và DynamoDB: điều chỉnh memory, timeout và concurrency; chọn giữa on‑demand và provisioned RCU/WCU cho các bảng.- Bật CloudWatch metrics và alarm cho lỗi/throttling của Lambda và throttling của DynamoDB.                                                                     | 02/12/2025   | 02/12/2025      | Proposal – Technical Implementation Plan (System Optimization)aws.amazon​          |
| Thứ Tư  | - Tăng cường bảo mật: tinh chỉnh IAM role với nguyên tắc least privilege cho Lambda, EventBridge, SES và DynamoDB.- Bảo vệ API Gateway (Cognito authorizer, throttling) và thiết lập AWS Budgets alerts cho account dự án.                                                                          | 03/12/2025   | 03/12/2025      | Proposal – Risks & Mitigation (cost overrun, failures)aws.amazon​                  |
| Thứ Năm | - Kết nối frontend (ứng dụng host trên Amplify) với backend API: triển khai các trang login/sign‑up, lịch biểu, tạo/sửa event và thiết lập reminder.- Kết nối frontend với Cognito và các endpoint API Gateway, kiểm thử các luồng người dùng cơ bản.                                               | 04/12/2025   | 04/12/2025      | Proposal – AWS Amplify, Key Features & Problem Statement                           |
| Thứ Sáu | - Chạy test tích hợp end‑to‑end: user auth → create/update/delete events → email nhắc việc theo lịch → xem lịch trên nhiều thiết bị/trình duyệt.- Chuẩn bị deliverable cuối (sơ đồ kiến trúc, báo cáo chi phí, demo script, screenshot) và cập nhật worklog với mục “Lessons Learned & Next Steps”. | 05/12/2025   | 05/12/2025      | Proposal – Expected Outcomes & ROI; AWS Well-Architected best practicesaws.amazon​ |

### Kết quả đạt được tuần 12:

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


