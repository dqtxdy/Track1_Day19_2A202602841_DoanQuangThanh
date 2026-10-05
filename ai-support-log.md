# AI Support Log — Đoàn Quang Thanh (Option B)

## 1. Công cụ và phạm vi

- **Codex:** hỗ trợ rà soát, chỉnh nội dung README, prototype và feedback notes trong lượt hoàn thiện này.
- Log này ghi phần tôi sử dụng AI cho Option B và cho việc hoàn thiện phần cá nhân; 

## 2. AI đã hỗ trợ việc gì

| Công việc | AI hỗ trợ | Phần tôi chịu trách nhiệm |
| --- | --- | --- |
| Thiết kế Option B | Phát triển flow learner mô tả chỗ vướng → trả lời câu hỏi ngắn → xem giả thuyết, căn cứ và uncertainty → xác nhận/sửa → xem giải thích và làm transfer. | Chọn Option B theo phân công nhóm; quyết định learner phải có quyền xác nhận hoặc sửa trước khi nhận giải thích. |
| Prototype B | Soạn HTML/CSS/JS cho prototype dùng canned output và tinh chỉnh copy, nhánh chẩn đoán, recovery, câu transfer. | Xác định nội dung học, fixture, cơ chế tương tác và giới hạn prototype; không dùng API/model thật. |
| Human–AI Design và test setup | Giúp tổ chức Expectation, Role & Agency, Evidence & Uncertainty, Control & Recovery; diễn đạt prompt test, task và observation focus. | Rà lại để khớp với Option B và flow A/B/C dùng chung. |
| Feedback/README | Sắp xếp note do tôi cung cấp thành các lớp OBSERVED, INTERPRETED, NEXT CHANGE, STILL UNPROVEN; rà tên tester, facilitator, lựa chọn và thứ tự. | Đối chiếu với `prototype-feedback-note.md`; xác nhận phiên tôi dẫn dắt là Nguyễn Văn Thăng, chọn A, thứ tự A → B → C. |
| Rà prototype nhóm | Phát hiện B trong trang A/B/C hiện lời giải ngay sau gợi ý; đề xuất và thêm trạng thái xác nhận riêng trước khi mở giải thích. | Quyết định giữ agency của Option B: tester xác nhận gợi ý trước khi xem lời giải. |

Các prompt dưới đây là **tóm tắt nội dung yêu cầu**, không phải transcript nguyên văn:

- “Rà repo và giúp hoàn thiện phần Option B theo lab; giữ cùng problem, task và fixture với A/C.”
- “Làm prototype B rõ hơn về cách AI suy luận, căn cứ, độ chắc chắn, quyền sửa và đường quay lại.”
- “Đọc note gốc và sửa phần phiên test cá nhân cho đúng người, facilitator, thứ tự và lựa chọn.”
- “Tách dữ liệu mẫu giả lập khỏi feedback thật và ghi rõ giới hạn.”

## 3. Cách kiểm chứng và giới hạn

- Dữ liệu tester thật trong README được đối chiếu với `prototype-feedback-note.md` (Nguyễn Văn Thăng) và chi tiết phiên Thái Anh do người dùng cung cấp, được ghi riêng tại `prototype-feedback-note-dang-van-thai-anh.md`.
- AI không tham gia facilitation, không quan sát tester và không tạo dữ liệu cho các phiên thật. Các hành vi, lựa chọn và câu nói trong feedback thật đến từ note của người dùng/nhóm; phần thiếu trong note không được lấp bằng quote hoặc hành vi bịa thêm.
- Prototype dùng canned output để thử luồng tương tác. Nó không kiểm chứng chất lượng chẩn đoán của một model AI.
- Một bộ review giả lập từng được tạo theo yêu cầu để minh họa cách hoàn thành đủ ba Feedback Notes và Group Synthesis. Bộ đó được gắn nhãn giả lập, tách khỏi dữ liệu thật và không được dùng làm evidence nộp bài.
- Các chỉnh sửa prototype trong log này chưa được xác nhận bằng buổi test mới; không xem đó là validation.

## 4. Sai sót AI và cách tôi sửa

1. **Gán nhầm phiên test của đồng đội vào phần cá nhân.** Bản README trước ghi phiên Đặng Văn Thái Anh do Trần Đức Quân dẫn dắt như phiên tôi dẫn dắt. Tôi yêu cầu đối chiếu `prototype-feedback-note.md`; README hiện ghi đúng phiên Nguyễn Văn Thăng do tôi dẫn dắt, chọn A.
2. **Thứ tự test không nhất quán giữa các note.** Note chi tiết của Thăng ghi A → B → C, trong khi bảng tổng hợp cũ ghi B → C → A. Tôi lấy note cá nhân làm nguồn chi tiết, cập nhật thứ tự liên quan và ghi rõ trong synthesis rằng thứ tự chưa counterbalance đầy đủ.
3. **Bản đầu của trang nhóm không chờ user xác nhận.** AI phát hiện và sửa flow để gợi ý/căn cứ tách khỏi lời giải; learner có lựa chọn xác nhận, quay lại sửa câu trả lời hoặc bỏ qua.
4. **Ví dụ giả lập có thể bị nhầm với kết quả thật.** Tôi yêu cầu ghi nhãn rõ dữ liệu tổng hợp là sample; README và feedback notes thật không dùng các hành vi/lời nói đó.

## 5. Kết quả

- README cá nhân ghi Option B và đúng phiên tester tôi dẫn dắt.
- `prototype-feedback-note.md` vẫn là nguồn chi tiết cho phiên Nguyễn Văn Thăng; phiên Đặng Văn Thái Anh có note riêng.
- Prototype B thể hiện uncertainty, xác nhận của learner, sửa hướng và recovery.
- Phản hồi thật và sample giả lập được phân biệt rõ.
