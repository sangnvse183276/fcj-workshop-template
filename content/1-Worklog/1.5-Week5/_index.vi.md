---
title: "Worklog Tuần 5"
date: "2025-09-09T19:53:52+07:00"
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 5:

* Kết nối, làm quen với các thành viên trong First Cloud Journey.
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:
| Ngày    | Nhiệm vụ                                                                                                                                                                                                                                                                                                                    | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo                                                                                      |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------------------------------------------------------------------- |
| Thứ Hai | - Sử dụng AWS Storage Gateway: ôn lại tổng quan lab và các trường hợp sử dụng chính (file/volume/tape gateway, hybrid storage, backup và archiving).aws.amazon​ - Hiểu kiến trúc tổng thể của lab (máy ảo on‑premises/EC2 đóng vai trò gateway, S3 là backend storage).                                                     | 13/10/2025   | 13/10/2025      | https://www.youtube.com/watch?v=Je2jPk7HhLQ&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=88            |
| Thứ Ba  | – “Create S3 Bucket” và tạo S3 bucket cần thiết cho lab Storage Gateway.aws.amazon​ - Cấu hình các thiết lập cơ bản: tên bucket, region, mã hóa (nếu cần) và các tag liên quan cho lab.                                                                                                                                     | 14/10/2025   | 14/10/2025      | https://www.youtube.com/watch?v=3vSrTeWroSs&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=86aws.amazon​ |
| Thứ Tư  | – “Create EC2 for Storage Gateway” và khởi tạo EC2 instance sẽ chạy Storage Gateway.000010.awsstudygroup​ - Cấu hình mạng và Security Group để EC2 instance có thể truy cập S3 và được quản lý an toàn (chỉ mở các port cần thiết).                                                                                         | 15/10/2025   | 15/10/2025      | https://www.youtube.com/watch?v=xVrhpe8OpVU&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=87            |
| Thứ Năm | – “Configure AWS Storage Gateway” (index 88) và kích hoạt gateway bằng S3 bucket đã tạo trước đó.aws.amazon​ - Cấu hình loại gateway phù hợp (ví dụ File Gateway hoặc Volume Gateway) theo hướng dẫn lab và kiểm tra trạng thái gateway đã ở trạng thái active.                                                             | 16/10/2025   | 16/10/2025      | https://www.youtube.com/watch?v=Je2jPk7HhLQ&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=88aws.amazon​ |
| Thứ Sáu | “Test Storage Gateway / Access Data” (index 89) và thực hiện các bước kiểm thử trong lab (mount share hoặc volume, đọc/ghi file, kiểm tra dữ liệu trong S3).aws.amazon​ - Viết một ghi chú nội bộ ngắn tóm tắt “Cách AWS Storage Gateway tích hợp workload on‑premises với S3 và khi nào nên dùng trong các dự án thực tế”. | 17/10/2025   | 17/10/2025      | https://www.youtube.com/watch?v=3Zp9GSMO-VI&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=89            |

### Kết quả đạt được tuần 5:

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


