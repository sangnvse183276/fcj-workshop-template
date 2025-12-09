---
title: "Worklog Tuần 10"
date: "2025-09-09T19:53:52+07:00"
weight: 2
chapter: false
pre: " <b> 1.10. </b> "
---



### Mục tiêu tuần 10:

* Kết nối, làm quen với các thành viên trong First Cloud Journey.
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:
| Ngày    | Nhiệm vụ                                                                                                                                                                                                                               | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo                                           |
| ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------------------------ |
| Thứ Hai | - Tinh chỉnh yêu cầu nghiệp vụ và user story cho Aurora Time (lịch biểu, nhắc nhở, xác thực, thông báo email). - Xác định các yêu cầu phi chức năng: khả năng mở rộng, tính sẵn sàng, độ trễ và ràng buộc chi phí.                     | 17/11/2025   | 17/11/2025      | Proposal – Executive Summary, Problem Statement              |
| Thứ Ba  | - Thiết kế kiến trúc serverless mức cao: API Gateway, Lambda, DynamoDB, EventBridge, SES, Cognito, Amplify, S3/CloudFront. - Vẽ/cập nhật sơ đồ kiến trúc dựa trên proposal.                                                            | 18/11/2025   | 18/11/2025      | Proposal – Solution Architecture & AWS Services Used         |
| Thứ Tư  | - Mô hình dữ liệu DynamoDB: thiết kế bảng, partition key và sort key cho users, events, schedules và reminders. - Ghi lại các pattern truy cập (tạo/cập nhật/xóa event, liệt kê theo ngày/người dùng, truy vấn các reminders sắp tới). | 19/11/2025   | 19/11/2025      | Proposal – Technical Implementation Plan (DynamoDB modeling) |
| Thứ Năm | - Tham gia sự kiện.                                                                                                                                                                                                                    | 20/11/2025   | 20/11/2025      |                                                              |
| Thứ Sáu | - Phác thảo thiết kế bảo mật & xác thực: Cognito user pool, luồng xác thực, JWT với API Gateway authorizer, các rule phân quyền cơ bản. - Viết “Architecture Design v1” (tài liệu ngắn) và chia sẻ với mentor/team để nhận phản hồi.   | 21/11/2025   | 21/11/2025      | Proposal – Cognito, Security, ROI & Risks sections           |
### Kết quả đạt được tuần 10:

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


