---
title: "Blog 2"
date: "2025-10-02"
weight: 1
chapter: false
pre: " <b> 3.2. </b> "
---



# Cách Rocket đơn giản hóa trải nghiệm mua nhà với Amazon Bedrock Agents

*bởi Manali Sapre, Seshidhar Raghupathi, Axel Larsson, và Sajjan AVS | vào ngày 10 tháng 7 năm 2025 | trong Amazon Bedrock Agents, Amazon Bedrock Knowledge Bases, Artificial Intelligence, Customer Solutions, Generative AI, Responsible AI*

---

Rocket Companies là một công ty FinTech có trụ sở tại Detroit với sứ mệnh **“Giúp Mọi Người Có Nhà.”** Sứ mệnh của Rocket mở rộng ra toàn bộ hành trình sở hữu nhà. Rocket đã phát triển bằng cách biến những điều phức tạp trở nên đơn giản, trao quyền cho khách hàng điều hướng hành trình sở hữu nhà thông qua các giải pháp công nghệ trực quan. Bằng cách kết hợp phân tích dữ liệu và **11PB dữ liệu** với tự động hóa tiên tiến, Rocket tăng tốc mọi quy trình từ phê duyệt khoản vay đến dịch vụ hậu mãi.

Cách tiếp cận **đặt khách hàng lên hàng đầu** của Rocket là trung tâm của mọi việc họ làm, kết hợp các công cụ kỹ thuật số có thể tùy chỉnh và hướng dẫn chuyên môn từ các chuyên viên thế chấp giàu kinh nghiệm.

Với sự ra đời của **generative AI**, Rocket nhận ra cơ hội để tiến xa hơn. Mua nhà có thể khiến nhiều người cảm thấy quá tải. Điều này khiến Rocket đặt ra câu hỏi: Làm thế nào chúng tôi có thể cung cấp sự hướng dẫn đáng tin cậy mà khách hàng mong đợi vào bất kỳ thời điểm nào, trên bất kỳ kênh nào?

> Kết quả là **Rocket AI Agent**, một trợ lý hội thoại AI được thiết kế để thay đổi cách khách hàng tương tác với các nền tảng kỹ thuật số của Rocket. Được xây dựng trên **Amazon Bedrock Agents**, Rocket AI Agent kết hợp kiến thức chuyên sâu, hướng dẫn cá nhân hóa và khả năng thực hiện các hành động có ý nghĩa thay mặt khách hàng.

Kể từ khi ra mắt, những khách hàng tương tác với Rocket AI Agent có khả năng hoàn tất khoản vay **cao gấp ba lần** so với những người không sử dụng.

---

## Giới thiệu Rocket AI Agent: Hướng dẫn AI cá nhân hóa cho việc sở hữu nhà

Rocket AI Agent hiện có sẵn trên phần lớn các trang web và ứng dụng di động của Rocket, giúp khách hàng trong quá trình khởi tạo khoản vay, dịch vụ, và trong hệ thống môi giới bên thứ ba (**Rocket Pro**). Rocket AI Agent được thiết kế với mục đích không chỉ để trả lời câu hỏi mà còn mang đến hướng dẫn cá nhân hóa theo thời gian thực và thực hiện hành động khi cần thiết. Nó cung cấp:

* **Hỗ trợ đa ngôn ngữ 24/7** thông qua trang web và dịch vụ di động của Rocket.
* **Nhận thức theo ngữ cảnh** (biết khách hàng đang xem trang nào).
* **Câu trả lời thời gian thực** về các lựa chọn thế chấp, lãi suất, tài liệu, và quy trình.
* **Hành động tự phục vụ có hướng dẫn**, chẳng hạn như điền vào mẫu phê duyệt trước hoặc lên lịch thanh toán.
* Trải nghiệm cá nhân hóa sử dụng **dữ liệu độc quyền** của Rocket và ngữ cảnh người dùng.
* Chuyển tiếp liền mạch đến các chuyên viên **Rocket Mortgage** khi cần hỗ trợ con người.

---

## Amazon Bedrock Agents

**Amazon Bedrock Agents** là một năng lực dựa trên đám mây, được quản lý hoàn toàn, cho phép khách hàng nhanh chóng xây dựng, kiểm thử và mở rộng các ứng dụng AI agentic trên Amazon Web Services (AWS).

Các agent này mở rộng **foundation models (FMs)** bằng cách sử dụng **Reasoning and Acting (ReAct) framework**, cho phép chúng diễn giải ý định của người dùng, lập kế hoạch và thực thi các tác vụ, đồng thời tích hợp liền mạch với dữ liệu và API doanh nghiệp.

> Agent sử dụng FM để phân tích yêu cầu của người dùng, chia nhỏ thành các bước hành động, truy xuất dữ liệu liên quan, và kích hoạt các API ở hạ tầng phía dưới để hoàn thành nhiệm vụ. Điều này cho phép Rocket AI Agent vượt ra ngoài hỗ trợ thụ động và chuyển sang **hỗ trợ chủ động**.

Các khả năng chính của Amazon Bedrock Agents được sử dụng trong Rocket AI Agent bao gồm:

* **Agent instructions**: Đặt mục tiêu và vai trò của agent (ví dụ: chuyên gia dịch vụ thế chấp).
* **Amazon Bedrock Knowledge Bases**: Cung cấp truy xuất thông tin nhanh chóng, chính xác từ Rocket’s Learning Center và các tài liệu nội bộ khác (sử dụng **Amazon Kendra** bên trong).
* **Action group**: Định nghĩa các thao tác an toàn như gửi khách hàng tiềm năng hoặc lên lịch thanh toán mà agent có thể thực hiện thông qua các dịch vụ backend của Rocket.
* **Agent memory**: Khả năng ghi nhớ cho phép Rocket AI Agent duy trì nhận thức ngữ cảnh trong nhiều lượt hội thoại.
* **Amazon Bedrock Guardrails**: Hỗ trợ mục tiêu **AI có trách nhiệm** của Rocket bằng cách đảm bảo agent giữ đúng giới hạn chủ đề phù hợp.

---

## Cách Rocket AI Agent hoạt động: Tổng quan kiến trúc

Rocket AI Agent là một năng lực tập trung được triển khai trên toàn bộ các nền tảng kỹ thuật số của Rocket. Trọng tâm của kiến trúc là một mạng lưới ngày càng mở rộng các **agent chuyên biệt theo lĩnh vực**, hiện có tám agent.

Các yếu tố nền tảng hình thành kiến trúc của Rocket AI Agent:

* **Client initiation**: Khách hàng sử dụng chức năng chat.
* **Rocket AI Agent API**: Cung cấp giao diện API thống nhất cho các agent.
* **Agent routing**: API của AI Agent định tuyến yêu cầu đến đúng agent Amazon Bedrock dựa trên tiêu chí tĩnh hoặc **nhận diện ý định bằng LLM**.
* **Agent processing**: Agent chia nhỏ nhiệm vụ thành các phần, xác định trình tự phù hợp, và thực hiện hành động cùng việc truy xuất kiến thức.
* **Task execution**: Agent sử dụng dữ liệu trong knowledge base của Rocket để tìm thông tin, gửi kết quả cho khách hàng, và thực hiện hành động.
* **Guardrails**: Thực thi các chính sách responsible AI của Rocket.
* **Prompt management**: Giúp Rocket quản lý thư viện prompt và tối ưu hóa cho từng FM cụ thể.

---

## Tác động và kết quả

Kể từ khi ra mắt Rocket AI Agent, Rocket đã chứng kiến những cải thiện mang tính chuyển đổi:

* **Tăng gấp ba lần tỷ lệ chuyển đổi** từ lưu lượng web thành các khoản vay được chốt.
* **Gia tăng hiệu quả vận hành** thông qua chat containment:
    * Giảm **85%** trong việc chuyển tiếp đến bộ phận customer care.
    * Giảm **45%** trong việc chuyển tiếp đến các servicing specialists.
* **Điểm Customer Satisfaction (CSAT) cao hơn**, với **68%** khách hàng đưa ra đánh giá mức độ hài lòng cao.
* **Tăng cường mức độ tương tác** của khách hàng, được thúc đẩy bởi khả năng self-service trực quan.
* **Cá nhân hóa và linh hoạt hơn**, cung cấp khả năng escalate đến banker theo điều kiện của khách hàng.
* **Mở rộng hỗ trợ ngôn ngữ**, bao gồm hỗ trợ **tiếng Tây Ban Nha**.

Rocket AI Agent không chỉ giúp khách hàng dễ dàng hơn mà còn giúp nhân viên Rocket làm việc hiệu quả hơn.

---

## Bài học kinh nghiệm

Trong suốt quá trình phát triển và triển khai, nhóm Rocket đã rút ra nhiều bài học quan trọng:

* **Curate your data carefully**: Chất lượng phản hồi của generative AI liên hệ chặt chẽ với chất lượng và cấu trúc của dữ liệu nguồn.
* **Limit the agent’s scope per task**: Giới hạn phạm vi hoạt động của mỗi agent trong khoảng **3–5 hành động** giúp chúng dễ bảo trì và đạt hiệu suất cao hơn.
* **Prioritize graceful escalation**: Escalation không phải là thất bại, mà là một phần quan trọng của việc xây dựng lòng tin. Rocket triển khai **uncertainty thresholds** để phát hiện khi nào cần chuyển sang hỗ trợ của con người.
* **Expect user behavior to evolve**: Hành vi người dùng trong thực tế luôn thay đổi, đòi hỏi đầu tư vào **observability** và các vòng phản hồi người dùng.
* **Using cross-Region inference from the start**: Kích hoạt **cross-Region inference** ngay từ đầu giúp mang lại hiệu suất mô hình có khả năng mở rộng và độ ổn định cao, tránh các giới hạn Regional service quota trong thời điểm lưu lượng cao.

---

## Tiếp theo: Hướng đến sự hợp tác giữa nhiều agent

Giai đoạn tiếp theo tập trung vào việc mở rộng các khả năng thông qua **sự hợp tác giữa nhiều agent** được hỗ trợ bởi Amazon Bedrock Agents, cho phép Rocket điều phối các agent trên nhiều miền khác nhau và mang đến các trải nghiệm thông minh, **toàn diện (end-to-end experiences)**.

### Lợi ích đối với Rocket

Sự hợp tác giữa nhiều agent đánh dấu một bước tiến mang tính chuyển đổi, tái định nghĩa khái niệm sở hữu nhà.

* **End-to-end personalization**: Nhiều **specialized agents** phối hợp để chia sẻ ngữ cảnh và mang lại các phản hồi thông minh và phù hợp hơn.
* **Back-office integration**: Các agent có thể gọi các secure backend APIs và workflows, tự động hóa một phần hoạt động back-office.
* **Context switching**: Chuyển đổi linh hoạt giữa servicing, origination và refinancing trong cùng một phiên chat.
* **Orchestration**: Xử lý các tác vụ nhiều bước trải rộng trên nhiều bộ phận kinh doanh khác nhau của Rocket.

Đây chính là chương tiếp theo trong sứ mệnh của Rocket: **“Help Everyone Home.”**

---

## Kết luận

**Rocket AI Agent** là một cách tiếp cận hoàn toàn mới đối với việc tương tác với khách hàng. Bằng cách kết hợp **Amazon Bedrock Agents** với dữ liệu độc quyền và hệ thống backend, công ty đã tạo ra một trải nghiệm thông minh hơn, có khả năng mở rộng cao hơn, và mang tính con người hơn, luôn sẵn sàng 24/7.

Để tìm hiểu sâu hơn, bạn có thể khám phá AWS workshop **Unified User Experiences with Hierarchical Multi-Agent Collaboration**.

Rocket đã tóm gọn điều đó một cách đơn giản: “Cùng với AWS, chúng tôi chỉ mới bắt đầu. Mục tiêu của chúng tôi là giúp mọi khách hàng tiến bước với sự tự tin, và cuối cùng, để **Help Everyone Home**.”

---

## Về các tác giả

#### Manali Sapre

Giám đốc cấp cao tại Rocket Mortgage, với hơn 20 năm kinh nghiệm lãnh đạo các sáng kiến công nghệ mang tính chuyển đổi.

#### Seshidhar Raghupathi

Kiến trúc sư phần mềm tại Rocket. Anh là Kỹ sư trưởng tại Rocket, tập trung vào **generative AI** và tự động hóa doanh nghiệp.

#### Venkata Santosh Sajjan Alla

Kiến trúc sư giải pháp cấp cao tại AWS Financial Services, nơi anh dẫn dắt chuyển đổi số dựa trên AI trong ngành FinTech tại Bắc Mỹ.

#### Axel Larsson

Kiến trúc sư giải pháp cấp cao tại AWS, hỗ trợ khách hàng trong lĩnh vực FinTech.
