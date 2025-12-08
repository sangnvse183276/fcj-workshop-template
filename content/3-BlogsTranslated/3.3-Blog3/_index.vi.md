---
title: "Blog 3"
date: "2025-09-09T19:53:52+07:00"
weight: 1
chapter: false
pre: " <b> 3.3. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

Databricks hiện đại hóa dữ liệu y tế trên AWS
Tác giả: Venkat Viswanathan 
Ngày đăng: 13/5/2025
Chuyên mục: Amazon AppFlow, Amazon Bedrock, Amazon EC2, Amazon Kinesis, Amazon Nova, Amazon Simple Storage Service (S3), Amazon Titan, AWS Database Migration Service, AWS Glue, AWS Identity and Access Management (IAM), AWS Key Management Service, AWS Marketplace, AWS PrivateLink, AWS Trainium, Graviton Permalink 

Bài đăng này được đồng viết cùng Rebecca Nissan, Kỹ sư Giải pháp Cấp cao, Chăm sóc Sức khỏe và Khoa học Đời sống, Kỹ thuật Hiện trường, Databricks.

Trong bối cảnh hiện nay, khi dữ liệu y tế trở thành trọng tâm, các tổ chức gặp nhiều thách thức (chẳng hạn như các silo dữ liệu rời rạc) trong hồ sơ sức khỏe điện tử (EHR), hình ảnh y tế và các kho dữ liệu tại chỗ khác. Dữ liệu y tế đang tăng trưởng với tốc độ rất nhanh đến mức một nghiên cứu nhận thấy ngành y tế đang tăng nhanh hơn các lĩnh vực khác và đóng góp khoảng 30% tổng dung lượng dữ liệu toàn cầu hiện nay.

Do đó, các tổ chức cần một nền tảng dữ liệu an toàn và dễ sử dụng để tập trung và tận dụng dữ liệu một cách hiệu quả. Databricks trên Amazon Web Services (AWS) cung cấp một nền tảng dữ liệu và phân tích thống nhất, phá vỡ các silo dữ liệu và tích hợp khả năng kỹ thuật dữ liệu của Databricks với cơ sở hạ tầng đáng tin cậy và an toàn của AWS.

Chúng tôi sẽ lần lượt trình bày cách Databricks và AWS, cùng phối hợp, có thể giúp giải quyết các silo dữ liệu lớn để chuyển đổi chăm sóc bệnh nhân cá nhân hóa thông qua AI tạo sinh và học máy.

Các thách thức của ngành thúc đẩy việc chuyển sang nền tảng dữ liệu hiện đại

Ngành chăm sóc sức khỏe đang thay đổi nhanh chóng trong cách quản lý và sử dụng dữ liệu. Ngành này ngày càng áp dụng các kiến trúc dữ liệu hiện đại để theo kịp bối cảnh thay đổi nhanh chóng.
Hãy cùng khám phá một số thách thức hiện tại của ngành y tế:
Chuyển đổi số trong y tế được thúc đẩy bởi xu hướng dịch từ mô hình trả phí cho dịch vụ (fee-for-service) sang chăm sóc dựa trên giá trị (value-based care — VBC) và thanh toán theo hiệu quả. Lịch sử y tế của bệnh nhân, hình ảnh y tế, dữ liệu từ thiết bị đeo, dữ liệu gen và các dữ liệu nghiên cứu y học khác đóng vai trò then chốt trong việc cải thiện kết quả bệnh nhân. Tuy nhiên, nhu cầu dữ liệu để thực hiện chiến lược VBC vượt quá khả năng của các công nghệ cũ và đòi hỏi hiện đại hóa để đáp ứng nhu cầu kinh doanh.


Các silo dữ liệu tại chỗ dẫn đến việc quản lý hàng petabyte dữ liệu phân tán ở nhiều bộ phận của tổ chức, có thể bị khóa trong các loại dữ liệu y tế khác nhau.


Tương tác cá nhân hóa đòi hỏi tập trung dữ liệu của một bệnh nhân để cho phép y học chính xác dựa trên tiền sử và nhu cầu sức khỏe riêng của bệnh nhân.


Việc ứng dụng các sáng kiến hỗ trợ AI còn chậm cản trở khả năng tận dụng tự động hóa nâng cao trong ghi chép lâm sàng và tăng độ chính xác chẩn đoán thông qua hình ảnh hỗ trợ AI. Việc ứng dụng AI tạo sinh cho các nhiệm vụ hành chính và dự đoán rủi ro bệnh nhân cũng sẽ mang lại lợi ích cho chăm sóc bệnh nhân.
Những yếu tố này thúc đẩy các khách hàng trong lĩnh vực y tế bắt đầu áp dụng các chiến lược dữ liệu hiện đại trên đám mây. Quy mô và tốc độ đổi mới trên đám mây cho phép khách hàng mở rộng tài nguyên khi cần và thu nhỏ khi không cần, dẫn đến hiệu quả chi phí trong lưu trữ và tính toán. Việc hợp nhất các silo dữ liệu cũng giảm trùng lặp dữ liệu — tạo ra một nguồn dữ liệu duy nhất đáng tin cậy.
Databricks cho ngành y tế	

Trong bối cảnh y tế dựa trên dữ liệu hiện nay, các tổ chức cần các giải pháp mạnh mẽ, an toàn và có khả năng mở rộng để biến lượng lớn dữ liệu y tế thành những hiểu biết có thể hành động nhằm cải thiện kết quả cho bệnh nhân. Nền tảng Data Intelligence từ Databricks cách mạng hóa cách các tổ chức sử dụng dữ liệu của họ để nâng cao kết quả điều trị.
Databricks hoạt động như một nền tảng phân tích mở và thống nhất để xây dựng các trường hợp sử dụng dữ liệu hoàn chỉnh trên một "data lakehouse" — một thuật ngữ kết hợp giữa kho dữ liệu và hồ dữ liệu trong cùng một công nghệ. Được sáng lập bởi
những người tạo ra Apache Spark, kiến trúc này tận dụng tính mở rộng của công nghệ đám mây cho lưu trữ, xử lý dữ liệu và AI đồng thời bổ sung cấu trúc, quản trị dữ liệu và trải nghiệm business intelligence của các kho dữ liệu truyền thống.
AWS hợp tác với Databricks để đưa nền tảng lakehouse mạnh mẽ của Databricks cùng với cơ sở hạ tầng toàn diện của AWS. Sự hợp tác này cung cấp cho các tổ chức y tế một môi trường an toàn, có khả năng mở rộng và tuân thủ cho khối lượng công việc dữ liệu quan trọng của họ — tạo điều kiện cho đổi mới nhằm thúc đẩy cải thiện chăm sóc bệnh nhân.
Tại sao nên chọn Databricks trên AWS

Hình 1: Kiến trúc tổng quan của các nguồn dữ liệu và kết quả của Databricks trên AWS

Databricks trên AWS cung cấp một nền tảng để hợp nhất hệ sinh thái các silo dữ liệu đa dạng, bao gồm tất cả dữ liệu EHR, hình ảnh y tế, hệ thống phòng xét nghiệm, chu kỳ doanh thu, dược phẩm, chuỗi cung ứng, hệ thống hỗ trợ quyết định lâm sàng và nhiều nguồn khác. Quyết định chạy Databricks trên AWS là một lựa chọn chiến lược cho các tổ chức y tế, mở khóa giá trị đáng kể. Nó có thể giúp dự đoán khởi phát bệnh trong thời gian thực ở môi trường nội trú, đo lường các chỉ số an toàn bệnh nhân (như gãy xương do ngã). Nó có thể hỗ trợ đóng các khoảng trống chăm sóc bằng các sàng lọc phòng ngừa (giảm thời gian nằm viện và cải thiện kế hoạch điều trị), và tối ưu hóa hiệu suất nhà cung cấp trong các thỏa thuận thanh toán gói, chỉ kể vài ví dụ.
Có một số lợi thế công nghệ thuyết phục khi sử dụng Databricks cùng với AWS.

Sẵn sàng và độ tin cậy
Nền tảng của những lợi thế này nằm ở cơ sở hạ tầng toàn cầu của AWS, cung cấp độ sẵn sàng và khả năng phục hồi cao nhất trong ngành. Databricks trên AWS có mặt ở 13 khu vực AWS và nhiều Vùng Khả dụng (Availability Zones) trong mỗi khu vực. Điều này có nghĩa là các tổ chức y tế có thể triển khai khối lượng công việc Databricks với sự tự tin, đảm bảo tiếp tục hoạt động kinh doanh và đáp ứng các yêu cầu quy định nghiêm ngặt về cư trú dữ liệu và khôi phục thảm họa.
Mang lại sự đơn giản và linh hoạt cho AI tạo sinh
Mang đến cho khách hàng sự đơn giản và linh hoạt cho AI tạo ra

Trong khi Databricks đơn giản hóa kiến trúc bằng lakehouse và tăng tốc mang lại giá trị, AWS cung cấp các công cụ mạnh mẽ và linh hoạt. Chúng cho phép các tổ chức y tế có khả năng chưa từng có để xây dựng nghiên cứu tiên tiến sử dụng AI tạo sinh, hình ảnh y tế, dữ liệu gen, mã hóa y tế tự động, nghiên cứu và phát triển thuốc, và các kế hoạch điều trị cá nhân hóa.

Databricks Mosaic AI Gateway hỗ trợ phục vụ mô hình trên mọi đám mây, bao gồm các mô hình có sẵn trong Amazon Bedrock — dịch vụ cung cấp quyền truy cập vào lựa chọn các mô hình nền tảng hàng đầu qua một API duy nhất. Điều này bao gồm các mô hình Amazon Titan và Amazon Nova cũng như các mô hình từ các công ty AI hàng đầu như Anthropic, AI21 Labs, Meta và nhiều nhà cung cấp khác. Cùng nhau, Mosaic AI Gateway và Amazon Bedrock mang đến cho khách hàng sự linh hoạt và lựa chọn để sử dụng mô hình phù hợp với trường hợp sử dụng của họ, tận dụng phạm vi rộng các mô hình có sẵn trên Amazon Bedrock cùng với các mô hình khác mà Mosaic AI Gateway hỗ trợ.

Databricks Mosaic AI cung cấp kết nối và minh bạch hoàn chỉnh giữa dữ liệu và AI, được hỗ trợ bởi tích hợp gốc với các công cụ quan sát (observability) của Unity Catalog — giúp cải thiện độ chính xác mô hình và giám sát chi phí.

Hơn nữa, tận dụng các chip AWS Trainium và Inferentia cho phép các tổ chức tối ưu cả chi phí huấn luyện và suy luận trong khi duy trì hiệu suất cao.
Tối đa hóa lợi tức đầu tư và tối ưu chi phí.
Tối đa hóa lợi tức đầu tư và tối ưu hóa chi phí
Các tổ chức y tế có thể tận dụng bộ xử lý AWS Graviton, đem lại hiệu suất chi phí tốt hơn tới 40% so với các instance x86 truyền thống. Khả năng sử dụng Amazon EC2 Spot Instances cho các khối lượng công việc Databricks có thể giảm chi phí tính toán tới 90% so với giá on-demand.

Spot Instances trên AWS cung cấp thông báo gián đoạn trước hai phút trước khi bị chấm dứt, giúp khách hàng cân bằng giữa khả năng chống lỗi và tối ưu chi phí. Hiệu quả chi phí này còn mở rộng tới lưu trữ dữ liệu thông qua phân lớp thông minh giữa các lớp lưu trữ của Amazon Simple Storage Service (Amazon S3) và tích hợp với các công cụ quản lý chi phí của AWS. Các tổ chức y tế có thể kiểm soát chi tiêu công nghệ trong khi mở rộng khả năng phân tích của mình.

Việc áp dụng Databricks trên AWS cũng tăng tốc thời gian đi đến cái nhìn chuyên sâu so với việc xây dựng và duy trì một nền tảng phân tích dữ liệu tùy chỉnh. Các giải pháp tùy chỉnh đòi hỏi kỹ sư nền tảng và kiến trúc sư chuyên trách để xây dựng và hỗ trợ các hoạt động vận hành liên tục (chẳng hạn như vá lỗi, tối ưu hóa cụm, và quản lý các pipeline nhúng dữ liệu). Với Databricks trên AWS, các tổ chức có thể tái tập trung chuyên môn nội bộ vào việc khai thác giá trị từ dữ liệu thay vì duy trì kiến trúc dữ liệu phức tạp.

Bảo mật và tuân thủ
Khả năng bảo mật và tuân thủ là tối quan trọng đối với các tổ chức y tế. Tích hợp gốc với các dịch vụ bảo mật của AWS, bao gồm AWS Key Management Service (AWS KMS) cho quản lý khóa mã hóa, AWS PrivateLink cho kết nối mạng an toàn, và AWS Identity and Access Management (IAM) cho kiểm soát truy cập chi tiết, giúp các tổ chức y tế dễ dàng duy trì tuân thủ HIPAA và bảo vệ dữ liệu bệnh nhân nhạy cảm.

Việc nền tảng Databricks hỗ trợ mô hình trách nhiệm chia sẻ của AWS cung cấp sự phân định rõ ràng về nghĩa vụ bảo mật, đơn giản hóa quá trình kiểm toán tuân thủ và quản lý rủi ro.

Đối với khách hàng bắt đầu trên AWS, chúng tôi khuyến nghị khám phá AWS Landing Zone Accelerator (LZA) cho ngành Y tế. Giải pháp mã nguồn mở của AWS này giúp bạn nhanh chóng triển khai nền tảng an toàn phù hợp với các thực hành tốt nhất của AWS, đặc thù cho ngành y tế, để thiết lập nền tảng vững chắc cho thành công.
Sự kết hợp của các lợi thế này khiến Databricks trên AWS trở thành một lựa chọn chiến lược cho các tổ chức y tế. Cho dù là triển khai các sáng kiến y học chính xác, tối ưu hóa thử nghiệm lâm sàng, hay cải thiện hiệu quả vận hành, nền tảng này cung cấp các khả năng kỹ thuật, tính năng bảo mật và lợi ích kinh tế cần thiết để thúc đẩy đổi mới trong chăm sóc sức khỏe.

Mở khóa dữ liệu chăm sóc sức khỏe của bạn với Databricks trên AWS

Hình 2: Kiến trúc tham chiếu Databricks trên AWS cho ngành Y tế

Kiến trúc tham chiếu Databricks trên AWS cho ngành Y tế bắt đầu bằng một vùng hạ cánh an toàn thông qua AWS Landing Zone Accelerator for Healthcare (LZA). Đây là nền tảng để tích hợp các nguồn dữ liệu y tế đa dạng, bao gồm hồ sơ sức khỏe điện tử (EHR), hình ảnh y tế và nghiên cứu bộ gen.
Việc tích hợp dữ liệu được thực hiện thông qua nhiều con đường, bao gồm các công cụ của Databricks như Auto Loader, Lakeflow Connect và Structured Streaming, cũng như các dịch vụ của AWS như AWS Database Migration Service (AWS DMS), Amazon AppFlow, AWS Glue và Amazon Kinesis. Những dịch vụ này cho phép thu thập dữ liệu theo cả chế độ lô (batch) và luồng (streaming) vào data lakehouse.
Dữ liệu được lưu trữ trong lakehouse, được backing bởi Amazon S3. Kiến trúc Medallion của Databricks được sử dụng để chuyển đổi và chăm sóc (curation) dữ liệu. Cuối cùng, dữ liệu đã xử lý có thể tích hợp với nhiều dịch vụ khác, bao gồm Amazon Bedrock, cung cấp truy cập API tới các mô hình nền tảng (foundation models) và mô hình ngôn ngữ lớn (LLM) hàng đầu trong ngành.
Khi bạn đã lọc, làm sạch và bổ sung cả dữ liệu có cấu trúc và không có cấu trúc, bạn có dữ liệu sản xuất — sẵn sàng để cung cấp cho người dùng và ứng dụng hạ nguồn. Khách hàng Databricks có thể tận dụng Delta Sharing, một phương pháp mã nguồn mở để chia sẻ dữ liệu trực tiếp (live data) từ lakehouse của bạn đến bất kỳ nền tảng tính toán, công cụ phân tích hay AI nào mà không cần sao chép.

Các lợi ích chính của Delta Sharing bao gồm khả năng chia sẻ xuyên nền tảng mở (tránh bị khóa nhà cung cấp), khả năng chia sẻ dữ liệu trực tiếp mà không cần nhân bản, và quản trị tập trung với Unity Catalog. Delta Sharing cho phép bạn tích hợp dữ liệu với các công cụ BI và phân tích ưa thích của mình (bao gồm cả Amazon QuickSight). Từ đó, các khách hàng ngành y tế có thể xây dựng báo cáo, trực quan hóa và ứng dụng giúp khai thác những hiểu biết từ dữ liệu trước đây bị khóa trong các silo.
Tóm tắt 
 Sự kết hợp giữa Databricks và AWS đại diện cho một giải pháp mạnh mẽ cho các tổ chức y tế muốn chuyển đổi khả năng phân tích dữ liệu của họ. Chúng tôi đã khám phá cách hợp tác này cung cấp bảo mật, khả năng mở rộng và các năng lực phân tích tinh vi cần thiết để thúc đẩy đổi mới trong y tế, đồng thời duy trì tuân thủ quy định và tối ưu chi phí.
Tương lai của phân tích y tế đã đến, và nó được thúc đẩy bởi Databricks trên AWS. Hãy tham gia cộng đồng ngày càng tăng của các tổ chức y tế đang tận dụng sự kết hợp quyền năng này để cải thiện kết quả cho bệnh nhân, tăng tốc nghiên cứu và mở khóa dữ liệu để thúc đẩy đổi mới.

Kết nối với Databricks hoặc đại diện AWS để xem demo trực tiếp và thảo luận cách chúng tôi có thể hỗ trợ hành trình của bạn tới kiến trúc dữ liệu hiện đại.
Sẵn sàng tăng tốc các sáng kiến dữ liệu của tổ chức y tế bạn? Dưới đây là một vài cách để bắt đầu:
Dùng thử Databricks miễn phí 14 ngày bằng trải nghiệm triển khai đơn giản qua AWS Marketplace
Duyệt các Databricks Healthcare & Life Sciences Solution Accelerators để bắt đầu nhanh cho các trường hợp sử dụng phổ biến
Truy cập AWS for Healthcare & Life Sciences để tìm hiểu thêm về các giải pháp chuyên biệt cho ngành y tế

Venkat Viswanathan
Venkatavaradhan (Venkat) Viswanathan là Kiến trúc sư Giải pháp Cấp cao tại Amazon Web Services. Venkat là Trưởng nhóm Chiến lược Công nghệ về Dữ liệu, AI, ML và Phân tích Nâng cao. Venkat là một doanh nghiệp vừa và nhỏ (SME) toàn cầu của Databricks, hỗ trợ khách hàng AWS thiết kế, xây dựng, bảo mật và tối ưu hóa khối lượng công việc Databricks trên AWS.






Amandip Kaler

202 / 5.000
Amandip Kaler là kiến ​​trúc sư giải pháp chăm sóc sức khỏe tại Amazon Web Services (AWS). Anh có bằng kỹ sư máy tính và hỗ trợ các tổ chức chăm sóc sức khỏe hiện đại hóa và hoàn thành sứ mệnh của họ.


Harrison Holstein
Harrison là Kiến trúc sư Giải pháp Cấp cao, chuyên hỗ trợ các đối tác Nhà cung cấp Phần mềm Độc lập Khu vực Công Toàn cầu của AWS. Anh đã làm việc tại AWS 6 năm và rất tâm huyết với việc hợp tác với các đối tác để cung cấp các giải pháp chung giúp khách hàng hiện đại hóa chiến lược dữ liệu đồng thời duy trì các mục tiêu bảo mật và tuân thủ.


Vaishali Gohel
Vaishali Gohel là Trưởng nhóm Kiến trúc Giải pháp tại Amazon với hơn hai thập kỷ kinh nghiệm trong việc chuyển đổi các tổ chức chăm sóc sức khỏe thông qua các giải pháp công nghệ đám mây tiên tiến. Bà là giám đốc công nghệ chiến lược, chuyên về di chuyển đám mây quy mô lớn và các chiến lược dữ liệu tiên tiến sử dụng AI, ML và AI tạo sinh. Vaishali đảm nhiệm việc liên tục cung cấp các giải pháp thúc đẩy tăng trưởng kinh doanh, nâng cao chất lượng chăm sóc bệnh nhân và cải thiện hiệu quả vận hành.
TAGS: Databricks


