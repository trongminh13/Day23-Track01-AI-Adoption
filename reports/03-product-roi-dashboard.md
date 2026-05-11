# Product ROI Dashboard — DOMIN-H Family (Finance Mediator)

## 1. Product Summary

**DOMIN-H Family** là nền tảng AI-Mediator (Trọng tài AI) giúp minh bạch hóa tài chính giữa sinh viên và phụ huynh, xóa bỏ sự nghi ngờ và những cuộc tra khảo căng thẳng mỗi khi đến kỳ chu cấp.

Sản phẩm hỗ trợ người dùng:
- **Smart Request:** AI hỗ trợ sinh viên lập kế hoạch chi tiêu, xác thực nhu cầu bằng dữ liệu thị trường (ví dụ: giá sách giáo trình, tiền nhà khu vực).
- **Audit & Verification:** AI dùng OCR quét hóa đơn, tự động đối chiếu để phát hiện hóa đơn giả hoặc chi tiêu sai mục đích.
- **Mediation Report:** Tổng hợp báo cáo "Độ tin cậy" (Trust Score) dựa trên lịch sử chi tiêu thay vì soi xét từng đồng lẻ.
- **Family Harmony:** Giảm ma sát giao tiếp, giúp phụ huynh duyệt chi nhanh gọn dựa trên sự an tâm do AI bảo chứng.

DOMIN-H không thay thế cha mẹ trong việc dạy con quản lý tiền. AI đóng vai trò **Copilot**: thu thập bằng chứng, cảnh báo rủi ro và giải thích. Phụ huynh vẫn là người cầm nút "Duyệt" cuối cùng.

---

## 2. Case Comparison Summary

Nhóm dùng 2 case chính từ OpenAI để rút bài học cho dashboard:

| Trường | Case thành công (Morgan Stanley) | Case cảnh báo (Klarna) |
| :--- | :--- | :--- |
| **Workflow** | AI hỗ trợ advisor truy xuất tri thức nội bộ phục vụ khách hàng. | AI hỗ trợ customer service tiếp nhận chat và xử lý case đơn giản. |
| **Metric mạnh** | Adoption, mức độ sử dụng hằng ngày của advisor. | Volume chat, resolution time, FTE-equivalent. |
| **Hệ quả cho DOMIN-H** | Cần thiết kế "Trust Architecture" (audit log, giải thích lý do) trước khi scale. | Không chỉ đo số hóa đơn đã quét. Phải đo Quality (độ chính xác) và Trust (hòa khí). |

---

## 3. Part A — Adoption Context

| Trường | Trả lời |
| :--- | :--- |
| **Product** | DOMIN-H Family |
| **Người dùng chính** | Sinh viên (User) và Phụ huynh (Payer) |
| **Bối cảnh sử dụng** | Hằng tháng khi sinh viên cần chu cấp và phụ huynh cần kiểm soát chi phí giáo dục. |
| **Mục tiêu vận hành** | Giảm 50% thời gian tra khảo/cãi vã; tăng 30% độ minh bạch tài chính gia đình. |
| **Rào cản ADKAR** | **Desire + Ability + Reinforcement**. |

### 3.1 Phân tích rào cản ADKAR
- **Desire:** Sinh viên sợ bị theo dõi (Spying); Phụ huynh sợ AI "vẽ" thêm chuyện để con xin tiền.
- **Ability:** Người dùng phải biết cách "đọc vị" báo cáo AI để không hiểu lầm con cái.
- **Reinforcement:** Nếu AI báo sai một lần (án oan), cha mẹ sẽ quay lại cách tra khảo thủ công ngay lập tức.

---

## 4. Workflow chính & Guardrails

| # | Workflow | AI làm gì? | Con người kiểm tra ở đâu? | Xử lý khi AI sai |
| :--- | :--- | :--- | :--- | :--- |
| 1 | **Lập Smart Request** | Gợi ý danh mục chi tiêu dựa trên lịch sử và giá thị trường khu vực. | Sinh viên kiểm tra tính thực tế trước khi gửi. | Sinh viên override thủ công; AI ghi log lý do chỉnh sửa. |
| 2 | **Audit Hóa đơn (OCR)** | Quét hóa đơn, phát hiện dấu hiệu chỉnh sửa hoặc giá bất thường. | Phụ huynh xem các cảnh báo Vàng/Đỏ của AI. | Sinh viên gửi thêm ảnh chụp/giải thích; AI rotate key nếu bị hack. |
| 3 | **Mediation Report** | Tổng hợp "Trust Score" tài chính và báo cáo hòa khí gia đình. | Phụ huynh duyệt nhanh dựa trên tóm tắt độ tin cậy. | Phụ huynh override và ghi lỗi; Team dev review prompt hằng tuần. |

---

## 5. ROI Dashboard Metrics

### 5.1 Metric toàn Product

| Layer | Metric | Baseline | Target | Red-team risk | Fix |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Activation** | % SV tạo thành công 1 Smart Request đầu tiên. | 0 | >= 75% | SV tạo request "ảo" để test app. | Chỉ tính khi có ít nhất 1 hóa đơn thật đính kèm. |
| **Trust / Quality** | **AI Error Rate (Tỷ lệ án oan)**. | 0 | <= 1% | SV không báo lỗi khi AI báo cáo có lợi cho mình. | Thực hiện QA Random Sample hằng tuần. |
| **Value** | **Family Harmony Index** (Số giờ giảm tranh cãi). | 5h/tháng | Giảm xuống < 1h/tháng | Tranh cãi chuyển sang chủ đề khác không liên quan tiền. | Khảo sát định tính mức độ "An tâm" của phụ huynh. |

### 5.2 Metric theo Workflow tiêu biểu (Workflow 2: Audit OCR)

| Layer | Metric | Target | Red-team risk | Fix |
| :--- | :--- | :--- | :--- | :--- |
| **Productivity** | Thời gian AI xử lý 1 hóa đơn (OCR). | < 5 giây | OCR nhanh nhưng sai số liệu nhạy cảm. | Thêm bước "Confidence Threshold" (Xác nhận thủ công nếu < 85%). |
| **Quality** | % Hóa đơn bị AI gắn cờ "Đỏ" là đúng sự thật. | >= 90% | AI quá nhạy cảm, gây áp lực lên sinh viên. | Hiệu chỉnh prompt để phân biệt "lỗi định dạng" và "gian lận". |
| **Trust** | % Phụ huynh không cần gọi điện hỏi lại sau khi xem báo cáo. | >= 70% | Phụ huynh vẫn gọi vì thói quen khó bỏ. | Thiết kế UI báo cáo cực kỳ trực quan, dễ hiểu hơn cả lời nói. |

---

## 6. Decision Memo

### 6.1 Khuyến nghị: Continue with Guardrails
DOMIN-H nên tiếp tục phát triển nhưng **tuyệt đối không được "vũ khí hóa" AI**. Phải giữ AI ở vị thế Mediator (Trọng tài) giúp đỡ đôi bên thay vì Spyware (Phần mềm gián điệp).

### 6.2 Metric mạnh nhất: AI Error Rate (Tỷ lệ án oan)
Đây là metric "sống còn". Nếu AI báo cáo sai khiến sinh viên bị mắng oan, hệ sinh thái niềm tin sẽ sụp đổ. Mục tiêu là **0 lỗi nghiêm trọng** lọt qua bước duyệt.

### 6.3 Thay đổi từ V1 sang V2
- **V1:** Đo số lượng hóa đơn quét được.
- **V2:** Đo tỷ lệ "Hòa khí gia đình" và "Tỷ lệ phụ huynh tin tưởng báo cáo AI".

---
