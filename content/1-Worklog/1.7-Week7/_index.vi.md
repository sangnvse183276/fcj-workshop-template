---
title: "Worklog Tuần 7"
date: "2025-09-09T19:53:52+07:00"
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 7:

* Kết nối, làm quen với các thành viên trong First Cloud Journey.
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:
| Ngày    | Nhiệm vụ                                                                                                                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | ------------------ |
| Thứ Hai | - Ôn lại AWS Well-Architected Framework: 6 trụ cột và cách chúng liên quan đến bảo mật, độ tin cậy, hiệu năng và tối ưu chi phí.- Lướt lại phần tổng quan các dịch vụ cốt lõi: EC2, S3, IAM, RDS, VPC, Lambda, CloudWatch, CloudFront và map mỗi dịch vụ với các trụ cột tương ứng.        | 27/10/2025   | 27/10/2025      |                    |
| Thứ Ba  | - Kiến trúc an toàn: ôn lại IAM (users, roles, policies), MFA, SCP, mã hóa bằng KMS, TLS/ACM, Security Group so với NACL, WAF, Shield, GuardDuty, Secrets Manager.                                                                                                                         | 28/10/2025   | 28/10/2025      |                    |
| Thứ Tư  | - Kiến trúc có khả năng chịu lỗi: ôn lại Multi-AZ so với Multi-Region, RDS Multi-AZ, các chiến lược DR (backup & restore, pilot light, warm standby, multi-site), Auto Scaling, ELB, Route 53 health check, các pattern backup & restore với S3/Backup.                                    | 29/10/2025   | 29/10/2025      |                    |
| Thứ Năm | - Kiến trúc hiệu năng cao & tối ưu chi phí: ôn lại các cơ chế scale compute (EC2 Auto Scaling, Lambda, Fargate), các tùy chọn lưu trữ (S3/EFS/EBS) và caching; sau đó ôn lại các công cụ cost (Cost Explorer, Budgets, Savings Plans/RI, lifecycle policy, tối ưu NAT, phân tầng lưu trữ). | 30/10/2025   | 30/10/2025      |                    |
| Thứ Sáu | - Đi thi.                                                                                                                                                                                                                                                                                  | 31/10/2025   | 31/10/2025      |                    |

### Kết quả đạt được tuần 7:

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


