---
title: "Blog 2"
date: "2025-09-09T19:53:52+07:00"
weight: 1
chapter: false
pre: " <b> 3.2. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

Những người vô gia cư có được nơi trú ẩn, chứng minh danh tính của họ bằng giải pháp Kiip do AWS cung cấp
Tác giả:Noah Harlan and Jessie Metcalf
Ngày đăng:03/11/2023
Chuyên mục: Amazon Bedrock, Amazon Chime, Amazon Cognito, Amazon Simple Storage Service (S3), AWS Key Management Service, AWS Lambda, AWS Marketplace, Customer Solutions, Nonprofit, Public Sector, State or Local Government Permalink 

Noah Harlan, bên trái, và các đồng nghiệp của Kiip tại sự kiện Homeless Connect Day ở Los Angeles.

Quyền tiếp cận các tài liệu quan trọng vừa là một khó khăn vừa là điều cần thiết đối với các cộng đồng dễ bị tổn thương và có nguy cơ. Đối với những người vô gia cư, việc “sẵn sàng về giấy tờ” là yếu tố then chốt để tránh bị trì hoãn hoặc bị từ chối tiếp cận các quyền lợi và dịch vụ họ cần. Đối với một cá nhân ở Los Angeles gần đây, điều đó quyết định sự khác biệt giữa có một chỗ nằm an toàn trong một nơi trú ẩn và bị tạm giữ bởi cảnh sát.

Vấn đề tiếp cận tài liệu và gánh nặng hành chính liên quan phổ biến đến mức các nhà nghiên cứu y tế công cộng đã công bố các bài báo về tác động bất lợi của việc thiếu giấy tờ tùy thân đối với những người đang trải nghiệm tình trạng vô gia cư. Thẻ An sinh Xã hội (Social Security card), giấy khai sinh và giấy chứng nhận khuyết tật là những thứ thiết yếu để tiếp cận dịch vụ và nộp đơn xin nhà ở. Nếu không có giấy tờ đầy đủ, người vô gia cư phải đối mặt với rào cản lớn đối với sự ổn định và cơ hội. Tuy nhiên, các công nghệ và công cụ mới đang giải quyết những vấn đề này đồng thời hỗ trợ các tổ chức phục vụ những cộng đồng dễ bị tổn thương. Một giải pháp sáng tạo gọi là Kiip, được hỗ trợ bởi Amazon Web Services (AWS), tiếp cận vấn đề này theo cách độc đáo bằng cách trao quyền cho cá nhân trong việc truy cập và kiểm soát các tài liệu quan trọng của chính họ.

Trao quyền cho cá nhân sở hữu dữ liệu của chính mình


Bắt đầu từ tháng 7 năm 2023, hàng trăm nhân viên tại Homeless Outreach Program Integrated Care System (HOPICS) đã bắt đầu sử dụng Kiip để lưu trữ tài liệu, hoàn tất các mẫu đơn và đơn xin, và đơn giản hóa liên lạc với khách hàng đến. Họ đặt mục tiêu cung cấp cho mọi người đến trung tâm quyền truy cập vào tài liệu của chính họ dù họ đi đâu. Như một khách hàng đã nhận ra, bạn không bao giờ biết khi nào một tài liệu quan trọng sẽ cần đến vào lúc then chốt.
Vào tháng 8 vừa qua, cảnh sát đã tạm giữ một cư dân ở một nơi trú ẩn do HOPICS vì là nghi phạm trong một vụ án. Cơ quan chức năng biết tên nghi phạm và người này trùng mô tả nhưng không có giấy tờ tùy thân. Không thể chứng minh mình không phải thủ phạm, người đó sắp bị đưa vào trại tạm giữ. Đang định bị còng tay, người này nhớ ra tài khoản Kiip của họ. Họ giải thích với cảnh sát rằng HOPICS đã tạo cho họ một tài khoản lưu trữ tất cả giấy tờ nhận dạng khi họ mới vào nơi trú ẩn.
Mở điện thoại, họ đã cung cấp được bản sao giấy tờ tùy thân, thẻ An sinh Xã hội, và thậm chí một bản sao đầy đủ đã ký của các mẫu tiếp nhận với nhân viên phụ trách hồ sơ của HOPICS — người đã thiết lập họ với Kiip. Khi danh tính được xác minh, cảnh sát đã thả người đó.
Tương tác này có vẻ nhỏ nhưng đối với ai đó trong cộng đồng dễ bị tổn thương, nó có thể thay đổi cuộc đời. Nếu người này vẫn bị tạm giữ, họ có thể mất giường trong nơi trú ẩn, buộc phải bắt đầu lại hành trình tìm nơi ở lâu dài.
“Khi chúng tôi tạo Kiip, chúng tôi tin rằng giúp người ta truy cập vào thông tin của chính họ sẽ không chỉ cải thiện quy trình tiếp cận quyền lợi và dịch vụ mà còn giúp họ trong nhiều nhu cầu khác ngoài bất kỳ tương tác nào,” said Noah Harlan, Nhà sáng lập kiêm Giám đốc điều hành Kiip. “Chúng tôi xây dựng Kiip để giúp cá nhân vượt qua gánh nặng hành chính khi xin quyền lợi và dịch vụ, đồng thời giảm bớt gánh nặng nhận thức nặng nề đặt lên các cộng đồng dễ bị tổn thương. Chúng tôi rất vui khi thấy nó đã giúp hàng trăm người nộp đơn xin quyền lợi, và việc biết rằng một người có thể tự giúp mình trong một tình huống có thể rất nghiêm trọng không liên quan đến các đơn xin của họ đã chứng minh rằng mô hình này hoạt động cho cả cá nhân và cộng đồng.”
Sử dụng công nghệ để cải thiện dịch vụ xã hội
HOPICS là một trong năm điều phối viên nhà ở cho Quận Los Angeles, tập trung vào Nam Los Angeles. Với gần 500 nhân viên, HOPICS cung cấp đa dạng dịch vụ bao gồm nơi trú ẩn cho cá nhân và gia đình, các trung tâm tiếp cận, đội tiếp cận cộng đồng, và các đội điều hướng cộng đồng cung cấp nhà ở, chăm sóc sức khỏe hành vi và hỗ trợ tái hòa nhập trong toàn khu vực. HOPICS được thành lập bởi Mike Neely 35 năm trước, khi ông là một cựu chiến binh vô gia cư ngủ trên Skid Row. Neely đã vận dụng trải nghiệm sống của mình để trở thành một nhà tổ chức cộng đồng, cuối cùng khởi động chương trình thử nghiệm với một khoản tài trợ 50.000 đô la. Từ khởi đầu đó, HOPICS đã giúp hàng nghìn cá nhân.
“Sự hợp tác của chúng tôi với Kiip đang thay đổi cách người dân ở Los Angeles tương tác với hệ thống phản ứng đối với người vô gia cư bằng cách trao quyền cho cá nhân một nguồn tài nguyên để lưu trữ các tài liệu quan trọng nhất một cách an toàn,” said Ben Kay, Giám đốc phụ trách Truy cập và Phân loại của HOPICS.
Kiip là một nền tảng phần mềm dưới dạng dịch vụ (SaaS) gốc đám mây tận dụng nhiều tính năng hàng đầu của AWS bao gồm điện toán serverless qua AWS Lambda, lưu trữ bảo mật có khả năng mở rộng với Amazon Simple Storage Service (Amazon S3) và AWS Key Management Service (AWS KMS), và Amazon Cognito cho quản lý định danh. Kiip tuân thủ HIPAA và là một giải pháp có khả năng mở rộng đảm bảo mọi tính năng đều có sẵn bất cứ khi nào và ở đâu cần thiết. Kiip sử dụng một số công cụ tiên tiến nhất của AWS, bao gồm Amazon Chime cho chat đa bên an toàn và Amazon Bedrock AI cho việc thẩm định (introspection) và phân loại tài liệu bằng mô hình ngôn ngữ lớn (LLM) riêng tư và an toàn.
Kiip, phối hợp với HOPICS và được hỗ trợ bởi AWS, cho phép những người vô gia cư lưu giữ, quản lý và chia sẻ an toàn các bản sao tài liệu quan trọng của họ. Giải pháp này cũng cung cấp cho các tổ chức cộng đồng, cơ quan và nhà cung cấp dịch vụ các tính năng chat đa bên an toàn, trao đổi tài liệu, điền mẫu và chữ ký điện tử có giá trị pháp lý cùng các giới thiệu (referrals). Giá trị cốt lõi của Kiip đối với khách hàng là các nhà cung cấp dịch vụ là cải thiện quy trình nộp đơn xin dịch vụ. Nó sử dụng phương thức “giải quyết vấn đề” đẩy thông tin, quyền truy cập và kiểm soát trở lại cho chính các cá nhân bằng cách làm cho các tài liệu cần thiết trở nên có thể truy cập và chia sẻ được. Việc đảo ngược mô hình cổng thông tin truyền thống này trao quyền cho cá nhân vượt ra ngoài mối quan hệ chỉ với nhà cung cấp dịch vụ của họ.
Kể từ khi ra mắt vào tháng 7 năm 2023 cùng HOPICS, Kiip đã phục vụ hơn 800 khách hàng và lưu trữ an toàn hơn 3.500 tài liệu quan trọng — bao gồm hơn 1.000 đơn xin.
Tác động rộng lớn hơn
Kiip đang cách mạng hóa cách một cộng đồng tiếp cận vấn đề vô gia cư và các thách thức liên quan. Nó trao quyền cho cá nhân, cải thiện hiệu quả cho nhà cung cấp dịch vụ, và đóng góp đáng kể vào cuộc chiến chấm dứt tình trạng vô gia cư. Khi đối mặt với vấn đề phức tạp này, những giải pháp như Kiip mang lại hy vọng và hỗ trợ thực tiễn cho những người cần giúp đỡ. Với các tổ chức như HOPICS dẫn đầu, có những công cụ mới trao quyền cho tương lai tốt hơn, nơi vô gia cư trở nên hiếm và tạm thời.
Có trên AWS Marketplace
Các tổ chức thuộc khu vực công cần cân bằng giữa các nghĩa vụ quy định và tuân thủ rộng lớn với các chiến lược mua sắm hiệu quả về chi phí. AWS Marketplace giúp đơn giản hóa và hợp lý hóa việc mua sắm cho các tổ chức khu vực công, cho phép họ dành ngân sách để thực hiện sứ mệnh hơn là cho chi phí hành chính. Tìm hiểu thêm về Kiip trên AWS Marketplace và đọc thêm các bài đăng blog về cách đám mây giúp các cộng đồng ngăn ngừa và chống lại bất ổn về nhà ở.
Bạn có phải là một tổ chức phi lợi nhuận muốn tìm hiểu thêm về cách điện toán đám mây có thể tăng tốc sứ mệnh của bạn? Bạn có câu hỏi về cách AWS có thể giúp cơ quan chính phủ của bạn cung cấp dịch vụ đổi mới cho người dân không? Hãy liên hệ với đội Ngành Công (Public Sector) của AWS.
Đọc các câu chuyện liên quan trên AWS Public Sector Blog:
Cung cấp nhanh quỹ hỗ trợ chủ nhà cho những người cần bằng đám mây
Giúp chính quyền địa phương giải quyết khủng hoảng nhà ở bằng đám mây
Sử dụng đám mây để đưa trợ cấp thuê nhà nhanh chóng đến những người cần
Sử dụng đám mây để tích hợp dữ liệu vô gia cư với các dịch vụ chăm sóc toàn diện cho cá nhân


TAGS: AWS for nonprofits, AWS Public Sector, customer story, homelessness, state and local government




Noah Harlan
Noah Harlan là Nhà sáng lập và Giám đốc điều hành của Kiip, PBC. Noah có gần hai thập kỷ kinh nghiệm xây dựng và lãnh đạo các tổ chức kỹ thuật số. Noah là Đồng sáng lập và Trưởng bộ phận Sản phẩm của Breadcrumb POS (được bán cho Groupon vào năm 2012) và đồng sáng lập và lãnh đạo Two Bulls, một công ty tư vấn sản phẩm kỹ thuật số toàn cầu hàng đầu (được bán cho Dept/Carlyle Group vào năm 2022). Noah cũng là Giám đốc của EdgeX Foundry và AllSeen Alliance, hai tập đoàn nguồn mở trực thuộc Linux Foundation, nơi ông đồng sáng lập và AllSeen Alliance nơi ông giữ chức chủ tịch. Noah đang trong nhiệm kỳ thứ hai với tư cách là thành viên được bầu của Hội đồng Giáo dục Cộng đồng cho Quận 1 tại Thành phố New York. Noah có bằng Khoa học Máy tính từ Cao đẳng Williams và đã nhận được Giải Emmy cho công trình nghiên cứu của mình về Tương tác Kỹ thuật số Tiên tiến.


Jessie Metcalf
Jessie Metcalf dẫn dắt các hoạt động chuyển đổi dữ liệu và số hóa cho nhóm chính quyền địa phương và tiểu bang của Amazon Web Services (AWS). Trong vai trò này, cô làm việc với những nhà lãnh đạo mong muốn khai thác tối đa dữ liệu họ có – những nhà lãnh đạo luôn tò mò và quyết tâm tìm hiểu cách họ thực sự tác động đến tất cả chúng ta bằng những chương trình nào để họ có thể tập trung vào việc cải thiện trải nghiệm đó.
