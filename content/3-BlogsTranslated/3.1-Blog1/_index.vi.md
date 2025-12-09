---
title: "Blog 1"
date: "2025-09-09T19:53:52+07:00"
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

AWS Marketplace
Mở khóa khả năng AI tạo sinh với DataRobot từ AWS Marketplace
Tác giả: Shun Mao, Luke Shulman, and Nathaniel Daly.
Ngày đăng: 20/12/2024
Chuyên mục:  Amazon Bedrock, Amazon Machine Learning, Amazon SageMaker, Amazon SageMaker Autopilot, Amazon Titan, AWS Marketplace, Generative AI, Intermediate (200) Permalink 

Generative AI đã trở thành chủ đề trung tâm trong lĩnh vực công nghệ kể từ cuối năm 2022. Tuy nhiên, với sự xuất hiện của nhiều mô hình ngôn ngữ lớn (LLM) mới và việc nhận diện các vấn đề như mô hình bịa đặt thông tin (hallucination), giới hạn độ dài ngữ cảnh, kỹ thuật thiết kế prompt (prompt engineering) và chi phí, cộng đồng generative AI đã nhận ra rằng cần bổ sung thêm nhiều tính năng và chức năng để sử dụng LLM một cách an toàn và hiệu quả trong môi trường doanh nghiệp.

Những phức tạp kết hợp này đã khiến các doanh nghiệp và tổ chức gặp khó khăn trong việc nhanh chóng ứng dụng generative AI. Các thách thức bao gồm thiếu chuyên môn và nhân sự về generative AI, không có khuôn khổ để đánh giá các mô hình khác nhau, thiếu cơ chế triển khai mô hình, không biết cách thiết lập các biện pháp bảo vệ và giám sát cho LLM hoặc cách kết hợp AI dự đoán truyền thống với generative AI, và còn nhiều điều khác nữa. Nhìn chung, các doanh nghiệp và tổ chức cần một công cụ hợp nhất có thể giải quyết những thách thức này trong khi yêu cầu ít chuyên môn AI và chi phí hợp lý.

DataRobot, một  AWS Partner và người bán trên AWS Marketplace, cung cấp một giải pháp để giải quyết các thách thức này. DataRobot là một nền tảng vòng đời AI toàn diện cung cấp cả khả năng AI dự đoán và generative với thiết kế low-code/no-code (LCNC) để giúp doanh nghiệp và tổ chức tạo giá trị kinh doanh và thúc đẩy đổi mới với AI nhanh hơn. DataRobot đã đạt được các AWS Competencies về máy học (ML), dữ liệu và phân tích, và dịch vụ tài chính, đồng thời sở hữu Chuyên môn AWS Service Ready cho Amazon SageMaker. DataRobot cung cấp nhiều kiểu triển khai khác nhau, bao gồm SaaS đa khách hàng (multi-tenant) được xây dựng trên AWS, SaaS dành riêng cho một khách hàng (single-tenant), và triển khai trên Amazon VPC (Amazon Virtual Private Cloud) để đáp ứng yêu cầu của các công ty và ngành khác nhau.

Bài viết này sẽ giới thiệu kiến trúc tổng thể của Nền tảng AI của DataRobot và cũng trình bày cách bạn có thể xây dựng một ứng dụng GenAI, từ lựa chọn LLM, kiểm thử prompt và đánh giá mô hình đến Retrieval Augmented Generation (RAG), giám sát LLM và các biện pháp bảo vệ (guardrails). Mọi thứ đã được kết hợp vào một nền tảng AI DataRobot thống nhất với trải nghiệm người dùng được tối ưu hóa.

Tổng quan giải pháp

Nền tảng SaaS của DataRobot được xây dựng hoàn toàn trên AWS với thiết kế Kubernetes hiện đại, cung cấp cho khách hàng các giải pháp AI mạnh mẽ, có khả năng mở rộng và đáng tin cậy. Các dự án AI bắt đầu bằng việc ingest dữ liệu, nơi DataRobot cung cấp các tích hợp an toàn với nhiều nguồn dữ liệu khác nhau, chẳng hạn như Amazon S3, Amazon Athena và Amazon Redshift, cũng như các kho dữ liệu từ nhà cung cấp khác như Snowflake. Sơ đồ sau đây mô tả kiến trúc tổng thể của giải pháp.

Hình 1: Sơ đồ kiến trúc tổng thể của SaaS DataRobot

Đối với AI dự đoán, bạn có thể dùng DataRobot để lưu trữ, xem, biến đổi và phân tích dữ liệu chỉ với một vài cú nhấp chuột và ít kiến thức khoa học dữ liệu. Những khả năng này được hỗ trợ bởi một động cơ xử lý dữ liệu mạnh mẽ. Sau khi chuẩn bị dữ liệu, DataRobot sử dụng năng lực AutoML của mình, chạy các công việc huấn luyện ML song song trên nhiều mô hình ML chất lượng cao đã chọn và toàn bộ các bước xử lý đặc trưng cần thiết một cách tự động. Các mô hình đã huấn luyện được xếp hạng trong một bảng xếp hạng tích hợp (leaderboard) với thông tin chi tiết về từng mô hình, chẳng hạn như độ chính xác, bản đồ tầm quan trọng đặc trưng (feature importance map), đường cong ROC (receiver operating characteristic), công thức xử lý (processing recipes) và giải thích dự đoán. Bạn có thể triển khai các mô hình trong DataRobot hoặc lên các nền tảng khác, chẳng hạn Amazon SageMaker hoặc Snowflake, chỉ trong vài phút sau khi chọn được mô hình tốt nhất.

Đối với generative AI, DataRobot cung cấp một LLM playground — một không gian nơi bạn có thể tạo và tương tác với các blueprint LLM sử dụng các LLM hàng đầu khác nhau, bao gồm Claude của Anthropic trên Amazon Bedrock và các mô hình Amazon Titan. Playground này tích hợp các cơ sở dữ liệu vector được tiền chọn sẵn để cho phép khách hàng xây dựng các ứng dụng chat hoặc RAG (Retrieval Augmented Generation) mà không cần chuyên sâu về ML. Các blueprint LLM khác nhau có thể được tạo và so sánh song song để thử nghiệm prompt. Nhiều chỉ số đánh giá LLM được chọn sẵn và các chỉ số tùy chỉnh có thể được lựa chọn và triển khai để giám sát hiệu suất của LLM — điều rất quan trọng để doanh nghiệp và tổ chức chấp nhận LLM. Sau khi thử nghiệm blueprint LLM và quyết định prompt cùng các chỉ số, khách hàng có thể chuyển blueprint vào triển khai sản xuất.

Đối với cả AI dự đoán và generative AI, DataRobot trang bị các công cụ giám sát cho các mô hình, dễ dàng thiết lập. Nền tảng có thể giám sát nhiều chỉ số được tiền chọn sẵn cũng như các chỉ số do người dùng thiết kế, chẳng hạn như tình trạng dịch vụ, độ trễ, kích thước token, tỷ lệ lỗi và chi phí. Đối với generative AI, DataRobot cung cấp các biện pháp bảo vệ (guardrails) để giúp ngăn chặn tấn công bằng prompt (prompt injection), phân loại cảm xúc và độc hại, phát hiện thông tin nhận dạng cá nhân (PII) và nhiều tính năng khác.

Trong các mục tiếp theo, chúng tôi sẽ trình bày các bước chính về cách bạn có thể dễ dàng xây dựng một ứng dụng AI dự đoán và generative trong DataRobot.

Trong hướng dẫn này, bạn sẽ học cách:

Kết nối dữ liệu trong Amazon S3 và tạo một công thức wrangling để chuẩn bị dữ liệu
Xây dựng một mô hình dự đoán trong DataRobot và triển khai nó lên Amazon SageMaker
Tạo một blueprint LLM kết hợp Claude của Anthropic trên Amazon Bedrock với dữ liệu làm căn cứ (grounding data)
Đánh giá và tối ưu blueprint theo các chỉ số như ROUGE (Recall-Oriented Understudy for Gisting Evaluation), tính trung thực (faithfulness) và độ tự tin (confidence)
Đóng gói blueprint LLM với các biện pháp bảo vệ để duy trì an toàn và hiệu suất
Ra mắt một ứng dụng AI có thể dự đoán NBO và tự động tạo email tiếp cận
Yêu cầu

Trước khi bắt đầu Trước khi bắt đầu, hãy đảm bảo bạn có các điều kiện sau:
Một tài khoản AWS với quyền truy cập vào các mô hình Amazon Bedrock
Một tài khoản DataRobot. DataRobot có thể được mua qua AWS Marketplace. Bạn cũng có thể truy cập trang DataRobot để yêu cầu dùng thử miễn phí.
Hướng dẫn giải pháp: Xây dựng một ứng dụng AI dự đoán và generative được cung cấp năng lực bởi các mô hình Claude của Anthropic trong DataRobot
Trường hợp sử dụng chúng tôi trình bày ở đây là tạo một chiến dịch email Next Best Offer (NBO) với mục tiêu tiếp cận chủ động những khách hàng có khả năng rời bỏ (churn) và cung cấp cho họ một ưu đãi giúp giữ chân họ.
Chúng tôi dùng một mô hình dự đoán để đề xuất NBO cho từng khách hàng và sau đó dùng generative AI để cá nhân hoá email cho từng khách hàng.
Bước 1: Kết nối nguồn dữ liệu trong Amazon S3 
Trong giao diện người dùng DataRobot Workbench, chúng ta có thể bắt đầu một Use Case mới và thêm dữ liệu NBO bằng cách kết nối với một thùng Amazon S3. Dữ liệu NBO được chuẩn bị nội bộ dựa trên bộ dữ liệu khách hàng rời bỏ dịch vụ viễn thông IBM công khai.
Thực hiện thay đổi cho tập dữ liệu này bằng cách thêm một cột văn bản khác có tên "kế hoạch khách hàng" và thay đổi mục tiêu dự đoán từ  Churn Value thành Next Best Offer . Thay đổi này biến dự đoán thành một bài toán phân loại đa lớp. Điều này được rút ra bằng cách áp dụng một số quy tắc kinh doanh thông thường vào mã lý do từ dữ liệu gốc. Đồng thời, chúng ta có thể tạo các cột mới để theo dõi thời gian khách hàng liên hệ với bộ phận chăm sóc khách hàng qua điện thoại, cung cấp một tính năng chính cho dự đoán của chúng ta.
Sử dụng công cụ sắp xếp dữ liệu của DataRobot để tạo công thức sắp xếp dữ liệu với một mẫu dữ liệu, sau đó áp dụng vào toàn bộ tập dữ liệu.

Hình 2: Thêm dữ liệu đầu vào từ Amazon S3 vào Giao diện người dùng DataRobot
Bước 2: Tạo mô hình dự đoán cho NBO
Sau khi hoàn tất việc chuẩn bị dữ liệu, chúng tôi có thể đào tạo một mô hình dự đoán để dự đoán loại ưu đãi nào phù hợp nhất với khách hàng nhằm tránh tình trạng khách hàng rời bỏ dịch vụ. Để thực hiện điều này, chúng tôi thực hiện theo các bước sau:
Trong DataRobot Workbench UI, hãy bắt đầu thử nghiệm để đào tạo mô hình.


Đối với loại đa lớp, hãy chọn Offers làm mục tiêu dự đoán.


Chạy Autopilot Register để huấn luyện một vài mô hình ML. Quá trình huấn luyện sẽ diễn ra tự động với các bước tiền xử lý được thiết kế riêng cho từng mô hình. Tất cả các công thức xử lý có thể được xem trong giao diện người dùng, hiển thị dưới dạng bản thiết kế, để khách hàng có thể xem những gì thực sự diễn ra trước khi huấn luyện mô hình thực tế. Điều này được thể hiện trong ảnh chụp màn hình sau.

Hình 3: Bản thiết kế để mô hình hóa và xử lý công thức nấu ăn
Các công thức này có thể hoàn thành trong vài phút do kích thước nhỏ của các tập dữ liệu được thử nghiệm. Khi triển khai mô hình, bạn có thể triển khai trực tiếp trong DataRobot mà không cần lo lắng về cơ sở hạ tầng nền. Bạn cũng có tùy chọn triển khai mô hình vào Amazon SageMaker chỉ với một cú nhấp chuột, như được hiển thị trong ảnh chụp màn hình sau. Điều này mang lại sự linh hoạt tuyệt vời cho việc lựa chọn cơ sở hạ tầng triển khai.

Hình 4: Triển khai mô hình một cú nhấp chuột của SageMaker trong DataRobot.
Bước 3: Tạo bản thiết kế LLM
Sau khi hoàn tất việc triển khai mô hình dự đoán, chúng tôi có thể xây dựng phần AI tạo sinh của ứng dụng, vốn là một thiết lập RAG. Một số LLM hàng đầu thị trường hiện đã có sẵn trong sân chơi LLM của DataRobot, chẳng hạn như Claude của Anthropic từ Amazon Bedrock và mô hình Amazon Titan, cũng như các mô hình từ các nhà cung cấp khác, mang đến cho khách hàng nhiều lựa chọn tuyệt vời để lựa chọn mô hình phù hợp cho ứng dụng của mình.
1.Điều hướng đến sân chơi LLM từ DataRobot Workbench và tạo bản thiết kế LLM bằng cách chọn mô hình Claude 3 làm LLM từ danh sách thả xuống. Sau khi mô hình được chọn, một số tham số liên quan đến LLM có thể được điều chỉnh để tinh chỉnh kết quả, chẳng hạn như Mã thông báo hoàn thành tối đa, Nhiệt độ và Ngưỡng xác suất lựa chọn Mã thông báo.
2.Trên cùng một trang, cơ sở dữ liệu vector và lời nhắc hệ thống có thể được cấu hình để hoạt động với LLM. Tại thời điểm này, người dùng có thể thử các kết hợp khác nhau của LLM, chiến lược phân đoạn và chiến lược nhắc nhở để có được kết quả tối ưu.
3.Users can build multiple blueprints and compare them against different metrics such as ROUGE, confidence, and faithfulness. The data we used to send to the vector database is a collection of five internal plan documents discussing various details of the cell phone plans.
Ảnh chụp màn hình sau đây hiển thị giao diện người dùng của sân chơi LLM.

Hình 5: Giao diện người dùng sân chơi DataRobot LLM
Bước 4: Thiết lập lan can LLM
1.Sau khi bản thiết kế LLM đã được tạo và thử nghiệm, hãy chọn các hành động của bản thiết kế LLM rồi chọn Gửi đến xưởng mô hình.
2.Trong hội thảo mô hình, hãy điều chỉnh các biến môi trường thời gian chạy khi cần thiết. Phần Đánh giá và Kiểm duyệt chứa các số liệu bạn có thể chọn để đánh giá hiệu suất và độ an toàn của mô hình theo thời gian. DataRobot cung cấp một số số liệu sẵn sàng sử dụng để bắt đầu, chẳng hạn như phát hiện PII, phân tích cảm xúc, độc tính, v.v. Ngoài ra, bạn có thể thiết kế các số liệu tùy chỉnh của riêng mình dựa trên logic kinh doanh riêng.
3.Sau khi hoàn tất mọi cấu hình, bạn có thể kiểm tra mô hình hoặc tạo phiên bản mới. DataRobot khuyến nghị bạn nên kiểm tra trước khi triển khai.
4.Tiếp theo, chọn Đăng ký mô hình, cung cấp chi tiết mô hình hoặc phiên bản đã đăng ký, rồi chọn Đăng ký mô hình một lần nữa để thêm LLM vào Registry. Phiên bản mô hình đã đăng ký sẽ mở ra trong thư mục Mô hình, chứa nút Triển khai để người dùng nhanh chóng triển khai mô hình.

Hình 6: Giao diện người dùng hội thảo mô hình DataRobot

Hình 7: Các số liệu đánh giá LLM có sẵn trong DataRobot
Bước 5: Các tùy chọn triển khai LLM
Tương tự như mô hình dự đoán, bạn có thể triển khai các mô hình LLM của mình trong DataRobot hoặc trên các nền tảng của bên thứ ba khác, chẳng hạn như Amazon SageMaker hoặc Amazon Elastic Kubernetes Service (Amazon EKS). Ở đây, chúng tôi sử dụng triển khai một cú nhấp chuột DataRobot để triển khai mô hình lên Amazon SageMaker. Sau khi triển khai, chúng tôi có thể theo dõi hiệu suất của cả phần tạo và phần dự đoán của ứng dụng. Bạn có thể tạo các số liệu tùy chỉnh như độ trễ, lợi tức đầu tư (ROI) hoặc khả năng đọc, có thể được xem trong cùng một bảng điều khiển, bất kể các mô hình đó được xây dựng trong DataRobot, trên AWS hay ở nơi khác. Điều này được hiển thị trong ảnh chụp màn hình sau.

Hình 8: Bảng thông tin theo dõi số liệu
Bước 6: Lưu trữ ứng dụng trong DataRobot
Với các mô hình dự đoán và tạo được triển khai, chúng ta có thể xây dựng một ứng dụng web bằng cách sử dụng cả hai mô hình và lưu trữ ứng dụng trong DataRobot. DataRobot hỗ trợ lưu trữ các ứng dụng tùy chỉnh trong nhiều khuôn khổ khác nhau, chẳng hạn như Streamlit, Shiny và Flask. Để biết thông tin chi tiết về việc lưu trữ các ứng dụng tùy chỉnh trong DataRobot, vui lòng tham khảo bài viết Tạo ứng dụng tùy chỉnh trong tài liệu DataRobot. Ở đây, chúng tôi sử dụng python để xây dựng một ứng dụng web đơn giản với Streamlit. Giao diện của ứng dụng được hiển thị trong hình 9. Ứng dụng chọn một khách hàng theo tên và dự đoán liệu khách hàng có cần một loại ưu đãi nhất định hay không để tránh tình trạng khách hàng rời bỏ. Kết quả của phần này được lấy từ phản hồi của mô hình dự đoán mà chúng tôi đã triển khai. Nếu xác định khách hàng cần một ưu đãi, ứng dụng sẽ tận dụng mô hình tạo mà chúng tôi đã triển khai trước đó để tạo một chiến dịch email mẫu với ưu đãi được tuyển chọn có chủ đích dựa trên tình huống riêng của khách hàng. Sau đó, nhóm tiếp thị có thể gửi email cho khách hàng.

Hình 9: Ví dụ ứng dụng kết hợp cả AI dự đoán và AI tạo ra
Dọn dẹp
Để dọn dẹp các tài nguyên được tạo trong hướng dẫn này, hãy làm theo các bước sau:


1.Trên bảng điều khiển AWS trong bảng điều khiển SageMaker, hãy xóa các triển khai SageMaker bằng cách xóa các điểm cuối SageMaker và cấu hình điểm cuối.
2.Trong giao diện người dùng DataRobot, hãy xóa tất cả các triển khai DataRobot.
Không có chi phí tiêu thụ bổ sung nào cho sân chơi DataRobot LLM hoặc các thử nghiệm dự đoán.
Kết luận
DataRobot là một nền tảng AI toàn diện giúp các nhóm khai thác giá trị từ AI với tốc độ nhanh hơn. Đối với các công ty và tổ chức có quy mô khác nhau, DataRobot có thể giúp bạn xây dựng và cung cấp các giải pháp AI tổng thể và dự đoán toàn diện cho doanh nghiệp của bạn, mang đến sự lựa chọn, tính linh hoạt và các thành phần hàng đầu. Với sự hợp tác và tích hợp chặt chẽ giữa DataRobot và AWS, khách hàng cũng có thể xây dựng ứng dụng của mình bằng cách kết hợp các khả năng của cả hai. Để bắt đầu với DataRobot, hãy truy cập


AWS Marketplace. Để tìm hiểu thêm các ví dụ về cách DataRobot có thể hỗ trợ bạn trong lĩnh vực AI tổng hợp, hãy tham khảo bản demo DataRobot GenAI Delivered.
Giới thiệu về tác giả




Shun Mao
Shun Mao là kiến ​​trúc sư giải pháp đối tác cấp cao trong nhóm đối tác nhà cung cấp phần mềm độc lập (ISV) về trí tuệ nhân tạo và học máy (AI/ML) tại Amazon Web Services. Ông có nhiều năm kinh nghiệm trong lĩnh vực khoa học dữ liệu, phân tích, AI và điện toán đám mây trên nhiều ngành công nghiệp khác nhau, bao gồm dầu khí và dược phẩm. Tại AWS, ông hỗ trợ các đối tác chiến lược về AI/ML xây dựng các sản phẩm và giải pháp mới lạ nhằm mang lại giá trị kinh doanh cho khách hàng. Ngoài công việc, ông thích câu cá, du lịch và chơi bóng bàn.
Nathaniel Daly
Nathaniel Daly là giám đốc sản phẩm chính tại DataRobot, tập trung vào việc phát triển các giải pháp AI dự đoán và AI tạo sinh. Ông tập trung vào việc mang những tiến bộ trong khoa học dữ liệu đến với người dùng để họ có thể sử dụng giá trị này nhằm giải quyết các vấn đề kinh doanh thực tế.




Luke Shulman
Luke Shulman là nhà khoa học dữ liệu hàng đầu tại DataRobot. Luke có hơn 12 năm kinh nghiệm trong lĩnh vực phân tích dữ liệu và khoa học dữ liệu. Trước khi gia nhập DataRobot, Luke đã lãnh đạo việc triển khai và là giám đốc nhóm quản lý sản phẩm tại Arcadia.io, nền tảng phân tích SaaS chăm sóc sức khỏe hàng đầu, và tại N1Health. Tại DataRobot, Luke đang làm việc với một số công ty nằm trong danh sách Fortune 100 sử dụng DataRobot. Anh cũng là người đóng góp tích cực cho các tiện ích mở rộng DrX cho ứng dụng khách API DataRobot, tập trung vào đánh giá mô hình và tích hợp MLFlow. Là một người đam mê khoa học dữ liệu, Luke cũng đã đóng góp cho các dự án trong hệ sinh thái khoa học dữ liệu bao gồm Bokeh, Altair và Zebras.js.

