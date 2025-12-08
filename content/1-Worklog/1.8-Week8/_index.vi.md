---
title: "Worklog Tuần 8"
date: "2025-09-09T19:53:52+07:00"
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 8:

* Kết nối, làm quen với các thành viên trong First Cloud Journey.
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:
| Ngày    | Nhiệm vụ                                                                                                                                                                                                                                                          | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo                                          |
| ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------------------------- |
| Thứ Hai | - Tinh chỉnh yêu cầu nghiệp vụ và user story cho Aurora Time (lịch biểu, nhắc nhở, xác thực, thông báo email). - Xác định yêu cầu phi chức năng: khả năng mở rộng, tính sẵn sàng, độ trễ, ràng buộc chi phí.                                                      | 03/11/2025   | 03/11/2025      | Tài liệu đề xuất (Executive Summary, Problem Statement)     |
| Thứ Ba  | - Thiết kế kiến trúc serverless mức cao: API Gateway + Lambda + DynamoDB + EventBridge + SES + Cognito + Amplify + S3/CloudFront. - Vẽ sơ đồ kiến trúc và căn chỉnh với phần “Solution Architecture” của bản đề xuất.                                             | 04/11/2025   | 04/11/2025      | Đề xuất – Solution Architecture & AWS Services Used         |
| Thứ Tư  | - Mô hình dữ liệu DynamoDB: thiết kế bảng/PK/SK cho users, events, schedules, reminder rules (cân nhắc các pattern truy cập: liệt kê sự kiện, tạo/cập nhật/xóa, truy vấn theo ngày/người dùng). - Ghi lại lựa chọn partition key/sort key và mẫu RCU/WCU kỳ vọng. | 05/11/2025   | 05/11/2025      | Đề xuất – Technical Implementation Plan (DynamoDB modeling) |
| Thứ Năm | - Định nghĩa hợp đồng API cho backend: liệt kê mọi REST endpoint (ví dụ: /events, /events/{id}, /reminders) kèm phương thức, schema request/response, mã lỗi. - Ánh xạ từng endpoint sang các hàm Lambda và xác định quyền IAM cần thiết.                         | 06/11/2025   | 06/11/2025      | Đề xuất – AWS Lambda, API Gateway, DynamoDB roles           |
| Thứ Sáu | - Phác thảo thiết kế bảo mật và xác thực: Cognito user pool, luồng đăng nhập, sử dụng JWT, tích hợp với API Gateway authorizer. - Tóm tắt quyết định thiết kế thành tài liệu “Architecture Design v1” (PDF/Markdown) để mentor review.                            | 07/11/2025   | 07/11/2025      | Đề xuất – các phần Cognito, Security, ROI & Risks           |

### Kết quả đạt được tuần 8:

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


