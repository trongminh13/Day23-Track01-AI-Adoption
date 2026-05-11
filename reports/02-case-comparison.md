# Case Comparison — Morgan Stanley vs Klarna

## 0. Bài tập cá nhân đang phát triển

| Mục tiêu | Trả lời |
| :--- | :--- |
| **Product chọn phân tích** | **DOMIN-H Family** (AI-Mediator quản lý tài chính sinh viên) |
| **Người dùng chính** | **Phụ huynh có con học đại học xa nhà:** Những người chu cấp tài chính và cần sự an tâm minh bạch. |
| **Mục tiêu dashboard** | Đo lường xem DOMIN-H có thực sự giúp giảm xung đột tài chính, tăng độ tin cậy và minh bạch hay chỉ đơn thuần tạo ra các báo cáo AI khô khan mà không giải quyết được "nỗi lo" của cha mẹ. |

---

## 1. Lý do chọn 2 case

Tớ chọn 2 case nghiên cứu điển hình từ OpenAI để làm "kim chỉ nam" cho DOMIN-H Family:

* **Morgan Stanley — AI Assistant cho Wealth Management:** Đây là case thành công rực rỡ trong việc triển khai AI vào môi trường tài chính rủi ro cao. Bài học lớn nhất ở đây là cách họ xây dựng **"Trust Architecture" (Kiến trúc niềm tin)** để đạt tỷ lệ áp dụng (adoption) tới 98%. Điều này cực kỳ quan trọng với DOMIN-H vì cha mẹ sẽ không giao tiền cho một hệ thống mà họ không tin tưởng tuyệt đối.
* **Klarna — AI Customer Support Assistant:** Đây là case cảnh báo (cautionary tale). Dù đạt được những con số khủng về năng suất (thay thế 700 nhân sự), nhưng đến năm 2025 họ phải điều chỉnh lại vì nhận ra việc quá tập trung vào cắt giảm chi phí và tốc độ có thể làm tổn hại đến chất lượng dịch vụ và niềm tin bền vững.

**Liên hệ với DOMIN-H Family:** Dự án của chúng ta nằm ở giao lộ của Tài chính và Mối quan hệ gia đình. Nếu AI báo cáo sai (hallucinate) khiến sinh viên bị mắng oan, hoặc nếu cha mẹ cảm thấy AI quá "máy móc", ứng dụng sẽ chết ngay lập tức. Dashboard của chúng ta phải học cách cân bằng giữa **Năng suất (Productivity)** và **Niềm tin (Trust)**.

---

## 2. Source bank

| Case | Nguồn | Link | Dùng để làm gì? |
| :--- | :--- | :--- | :--- |
| **Morgan Stanley** | OpenAI Case Study | [openai.com/morgan-stanley](https://openai.com/index/morgan-stanley/) | Dẫn chứng về 98% adoption, bài học về thiết kế cho sự tin tưởng (Trust). |
| **Klarna** | OpenAI & Reuters | [reuters.com/klarna-ai-2025](https://www.reuters.com/business/swedens-klarna-shifts-ai-focus-cost-cuts-growth-2025-09-10/) | Dẫn chứng về việc chuyển trọng tâm từ "cắt giảm chi phí" sang "chất lượng dịch vụ". |
| **Day 23 Ref** | Tài liệu lớp | 05-reference-document.md | Dùng framework: Metrics Ladder và Measurement Trap. |

---

## 3. Case Comparison Table

| Trường | Case thành công (Morgan Stanley) | Case cảnh báo (Klarna) |
| :--- | :--- | :--- |
| **AI Workflow** | Truy xuất tri thức nội bộ, hỗ trợ cố vấn tài chính phục vụ khách hàng. | Tiếp nhận chat, xử lý yêu cầu hỗ trợ khách hàng tự động. |
| **Metric mạnh** | 98% adoption, truy cập tài liệu tăng từ 20% lên 80%. | 2.3 triệu cuộc trò chuyện, thay thế 700 nhân sự, xử lý dưới 2 phút. |
| **Chứng minh được** | AI có thể hoạt động hiệu quả trong môi trường tài chính khắt khe. | AI có thể xử lý khối lượng công việc khổng lồ ở quy mô lớn. |
| **Chưa chứng minh** | Tác động cuối cùng đến sự hài lòng lâu dài của khách hàng (NPS). | Chất lượng cảm xúc và niềm tin bền vững của khách hàng. |
| **Bài học chính** | Phải thiết kế Trust trước khi scale (Eval, Expert feedback). | Không được dừng lại ở metric "Năng suất" và "Tốc độ". |
| **Áp dụng cho DOMIN-H** | Cần cơ chế kiểm soát lỗi (Human-in-the-loop) để bảo vệ sinh viên. | Không chỉ đo số hóa đơn được quét, mà phải đo "Độ an tâm" của cha mẹ. |

---

## 4. Phân tích case 1 — Morgan Stanley

### 4.1 Tại sao đây là case thành công cho DOMIN-H?
Morgan Stanley cho thấy ngay cả trong ngành tài chính bảo thủ nhất, AI vẫn có thể chiếm được lòng tin nếu nó giúp con người làm việc tốt hơn chứ không phải thay thế họ. Với DOMIN-H, AI không thay thế cha mẹ quản lý con cái, mà hỗ trợ họ trở thành những "nhà đầu tư giáo dục" thông thái hơn.

### 4.2 Các Metric mạnh
* **Adoption (98%):** Chứng minh AI đã trở thành một phần của workflow hàng ngày, không còn là "đồ chơi".
* **Knowledge Access (20% -> 80%):** Giải phóng sức mạnh của dữ liệu tĩnh.

### 4.3 Bài học cho Dashboard của DOMIN-H Family
Nhóm nên học cách Morgan Stanley dùng chuyên gia để đánh giá (Eval) kết quả của AI. Trước khi gửi một báo cáo "Red Flag" về chi tiêu của sinh viên, DOMIN-H cần:
* **Cơ chế giải thích:** Tại sao AI coi đây là khoản chi bất thường?
* **Quyền kháng cáo:** Cho phép sinh viên giải thích trước khi phụ huynh nhìn thấy.

---

## 5. Phân tích case 2 — Klarna

### 5.1 Tại sao đây là case cảnh báo cho DOMIN-H?
Klarna ban đầu rất tự hào về việc giảm thời gian xử lý từ 11 phút xuống 2 phút. Nhưng trong quản lý tài chính gia đình, nhanh không có nghĩa là tốt. Nếu AI duyệt chi quá nhanh mà bỏ qua rủi ro, hoặc từ chối quá nhanh gây xung đột, startup của chúng ta sẽ chết vì người dùng mất lòng tin (Trust death).

### 5.2 Các Metric dễ gây hiểu lầm (Measurement Trap)
* **Số lượng hóa đơn AI quét:** Metric này chỉ đo Năng suất, không đo Chất lượng.
* **Số nhân sự tương đương:** DOMIN-H không nhằm thay thế con người, mà là Mediator kết nối con người.

---

## 6. Bài học áp dụng vào Dashboard của DOMIN-H Family

### 6.1 Nguyên tắc 1: Năng suất phải đi kèm Chất lượng
Không chỉ đo "Thời gian duyệt chi giảm", mà phải đo cùng với **"Tỷ lệ khiếu nại từ sinh viên"**. Nếu duyệt nhanh mà sinh viên than phiền vì AI hiểu sai hóa đơn, đó là thất bại.

### 6.2 Nguyên tắc 2: Trust là Metric quan trọng nhất
Học từ Morgan Stanley, tớ đề xuất thêm metric **"Tỷ lệ cha mẹ chấp nhận gợi ý của AI" (AI Suggestion Acceptance Rate)**. Nếu tỷ lệ này thấp, nghĩa là hệ thống của chúng ta đang nói những thứ cha mẹ không tin.

### 6.3 Nguyên tắc 3: Phân tách rủi ro (Risk Segmentation)
Đừng đo trung bình tất cả chi tiêu. Hãy tách ra:
* **Chi tiêu định kỳ (Tiền nhà, học phí):** Ưu tiên Tốc độ.
* **Chi tiêu biến động (Tiệc tùng, mua sắm lớn):** Ưu tiên Minh bạch và Giải trình.

---

## 7. Kết luận cho Dashboard nhóm

Dashboard của DOMIN-H Family sẽ không chỉ là một bảng báo cáo tài chính. Nó phải là một Dashboard về Niềm tin.

| Layer | Metric đề xuất cho DOMIN-H |
| :--- | :--- |
| **Productivity** | Thời gian trung bình từ lúc sinh viên gửi Request đến khi phụ huynh Duyệt chi. |
| **Quality** | Tỷ lệ AI nhận diện đúng danh mục hóa đơn (OCR Accuracy). |
| **Trust** | % sinh viên cảm thấy AI đang "bảo vệ quyền lợi" của mình (qua khảo sát ngắn). |
| **Value** | Số lượng các cuộc tranh cãi về tiền bạc giảm đi hàng tháng (Family Harmony Metric). |

---

## 8. Summary ngắn để đưa vào Dashboard

Tớ chọn Morgan Stanley là case thành công vì nó chứng minh AI có thể scale trong ngành tài chính nếu có hệ thống bảo mật và tin tưởng vững chắc. Ngược lại, Klarna là case cảnh báo để nhắc nhở chúng ta rằng việc quá tập trung vào tốc độ và cắt giảm chi phí có thể làm hỏng mối quan hệ giữa người dùng và sản phẩm. Với DOMIN-H Family, sự thành công không nằm ở số tiền được chuyển, mà ở sự an tâm của cha mẹ và sự tự do minh bạch của sinh viên.

---

## 9. References
* OpenAI. "Morgan Stanley uses AI evals to shape the future of financial services."
* OpenAI. "Klarna's AI assistant does the work of 700 full-time agents."
* Reuters. "Klarna shifts AI focus from cost cuts to growth (2025)."
* Day 23 Course Materials. "Metrics ladder và Measurement Trap."
* DOMIN-H Project Documentation (Jimala).
