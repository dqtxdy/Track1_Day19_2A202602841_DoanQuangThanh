# Day 19 - Multiple Prototypes & Human-AI Design

## 1. Thông tin cá nhân & đội ngũ

- **Họ và tên:** Đoàn Quang Thanh
- **MSSV:** 2A202602841
- **Tên nhóm:** Hicarus
- **Case AI nghiên cứu:** Case A — AI Tutor: Diagnostic Refresher

|Họ và tên|MSSV|Vai trò chính Day 19|
|---|---|---|
|Đoàn Quang Thanh|2A202602841|Build Option B, facilitator Feedback 2|
|Vũ Quang Tiến|2A202602872|Build Option C, facilitator Feedback 3|
|Trần Đức Quân|2A202602922|Build Option A, facilitator Feedback 1|

## 2. Hypothesis Problem

> Khi **[situation]**, **[user]** gặp khó khăn trong việc **[job]** vì **[barrier]**, dẫn đến **[consequence]**.

|Thành phần|Nội dung|
|---|---|
|**Situation**|Đang làm bài tập và bị kẹt ở một khái niệm (biết áp dụng công thức nhưng không hiểu vì sao nó đúng)|
|**User**|Learner tự học/làm bài tập môn kỹ thuật|
|**Job**|Hiểu đủ khái niệm đang kẹt để tiếp tục làm bài|
|**Barrier**|Không xác định được chính xác mình đang hổng ở đâu, nên không biết nguồn hay cách giải thích nào phù hợp với trình độ hiện tại|
|**Consequence**|Phải chuyển qua nhiều nguồn, mất 30–45 phút cho việc tìm và chọn lọc thay vì học, và sau đó vẫn không chắc mình đã hiểu khái niệm hay chỉ hiểu đúng ví dụ|

**Hypothesis Problem nhóm chọn:** Khi đang làm bài tập và bị kẹt ở một khái niệm, learner gặp khó khăn trong việc hiểu đủ khái niệm đó để tiếp tục làm bài vì không xác định được chính xác mình đang hổng ở đâu và lời giải thích nào khớp với trình độ hiện tại, dẫn đến việc phải chuyển qua nhiều nguồn, mất 30–45 phút cho việc tìm kiếm thay vì học, và vẫn không chắc mình đã hiểu thật hay chỉ hiểu đúng ví dụ.

### Evidence từ Day 17

|Practice Note|User đã thực sự làm/nói gì?|Điều nhóm đang diễn giải|
|---|---|---|
|Situation|Tuần trước làm bài tập Machine Learning, kẹt ở gradient descent: biết áp dụng công thức nhưng không hiểu vì sao cập nhật parameter theo hướng đó lại giảm loss.|Điểm kẹt nằm ở **bản chất khái niệm**, không phải thao tác tính toán.|
|Workaround|Đọc lại slide → xem lại ví dụ trên lớp → tự thử ví dụ đơn giản → Google → YouTube → ChatGPT (hỏi lại nhiều lần) → tự làm lại bài tương tự.|Learner không thiếu nguồn; họ **chuyển nguồn liên tục** vì không nguồn nào khớp đúng chỗ đang hổng.|
|Vì sao nguồn không giúp|Slide dùng thuật ngữ user chưa hiểu; Google/YouTube phải tự lọc; ChatGPT đôi khi trả lời quá dài, "khiến càng rối".|Vấn đề nằm ở **độ khớp** giữa lời giải thích và trình độ hiện tại.|
|Chi phí|Mất khoảng 30–45 phút. *"Phần tốn thời gian nhất không hẳn là học, mà là tìm đúng tài liệu hoặc đúng cách giải thích."*|Chi phí chính là **tìm kiếm & chọn lọc**.|
|Kết quả|Làm được bài tương tự. *"Nhiều lúc mình cũng không chắc là mình thực sự hiểu hay chỉ hiểu đúng cái ví dụ đó."*|Learner **thiếu tín hiệu để biết mình đã hiểu thật**.|

**Điều vẫn chưa được chứng minh ở thời điểm chốt hypothesis:**

- Tần suất: mới có 1 sự kiện từ 1 learner.
- Nguyên nhân gốc: barrier là do hổng kiến thức nền hay do cách giải thích chưa phù hợp.
- Mức độ nghiêm trọng: 30–45 phút có ảnh hưởng tới deadline, điểm số hay động lực học không.
- Hậu quả của "hiểu nông": chưa có sự kiện cụ thể learner làm được bài tương tự rồi thất bại khi dạng bài thay đổi.

## 3. Three Solution Options

Ba options cùng giải một task: learner bị kẹt ở khái niệm gradient descent cần xác định chỗ hổng và hiểu đủ để quay lại bài. Chúng khác nhau ở **ai khởi động** và **ai chẩn đoán chỗ hổng**. Cả ba kết thúc bằng cùng một câu kiểm tra ở dạng khác, f(w) = (w + 2)², để đo learner hiểu thật hay chỉ hiểu đúng ví dụ.

|Option|Cơ chế hoạt động|Human–AI|
|---|---|---|---|
|**A — Tự chẩn đoán theo chuỗi kiến thức**|Learner tự mở chuỗi 4 bước kiến thức nền soạn sẵn, tự đánh dấu bước chưa chắc, đọc giải thích soạn sẵn cho bước đó; không có AI suy luận.|User initiates · AI *Don't Act*|
|**B — Cùng AI chẩn đoán**|Learner mô tả chỗ vướng; AI hỏi 2–3 câu ngắn, đưa giả thuyết kèm căn cứ và độ chắc chắn; learner xác nhận hoặc sửa trước khi nhận giải thích.|User + AI co-create · AI *Ask*|
|**C — AI chủ động + human escalation**|AI phát hiện tín hiệu kẹt (dừng lâu, sửa đáp án nhiều lần), đề xuất hỗ trợ; learner chấp nhận, để sau hoặc tắt nhắc; có bản nháp câu hỏi gửi trợ giảng để learner xem và sửa trước khi gửi.|AI initiates, user reviews · AI *Act → Ask*|

- **Chi tiết** (parking lot, phần giữ nguyên/khác nhau, distance check, Human–AI Decision Table): [three-option-design-sheet.md](three-option-design-sheet.md)
- **Danh sách link và annotation cho facilitator:** [prototype-link.md](prototype-link.md)

## 4. Đóng góp cụ thể của tôi trong sản phẩm nhóm

- **Chịu trách nhiệm chính Option B:** thiết kế và build micro-prototype [prototype/option-b.html](prototype/option-b.html): learner mô tả chỗ vướng, trả lời ba câu ngắn; AI nêu giả thuyết có căn cứ và độ chắc chắn thấp; learner xác nhận hoặc sửa trước khi xem giải thích, rồi tự kiểm tra bằng câu transfer.
- **Bối cảnh chung cho A/B/C:** dựng trang bài học 5.2 Gradient descent (mục lục khoá học, slide bài giảng, bài tập phần (a)/(b)) và content fixture dùng chung (bài f(w) = (w − 3)², chuỗi 4 bước, câu transfer f(w) = (w + 2)²), để B và C chỉ cần thay phần critical interaction.
- **Human–AI Decision Table:** viết bốn quyết định thiết kế (Expectation, Role & Agency, Evidence & Uncertainty, Control & Recovery), bảng quyết định cho cả A/B/C và phần Feedback & data check trong [three-option-design-sheet.md](three-option-design-sheet.md).
- **Hỗ trợ đồng đội:** viết kịch bản test chung (câu hỏi relevant context, outcome task, observation focus, luật facilitation, thứ tự xoay vòng A-B-C / B-C-A / C-A-B); chuẩn hoá Feedback Note của Thăng và Nam về cùng cấu trúc; tổng hợp 3 phiên vào [group-feedback-synthesis.md](group-feedback-synthesis.md).
- **Kiểm thử:** làm facilitator cho phiên test với Nguyễn Văn Thăng trên cả A, B, C; note chi tiết: [prototype-feedback-note.md](prototype-feedback-note.md).

## 5. Dữ liệu kiểm thử & bài học

### Phiên test tôi dẫn dắt

**Tester:** Nguyễn Văn Thăng (2A202602835), chủ động tự học, thích tự kiểm tra lập luận và thận trọng với AI chủ động vì không muốn bị ngắt mạch học · **Thứ tự:** A → B → C · **Chọn:** **A** · Chi tiết: [prototype-feedback-note.md](prototype-feedback-note.md)

- **A:** chọn “Dấu đạo hàm cho biết hàm đang tăng hay giảm”, rồi mở thêm “Learning rate”; ban đầu do dự giữa bước dấu đạo hàm và bước đi ngược gradient. Dùng “Đổi bước cần xem lại” và câu transfer để tự kiểm tra.
- **B:** trả lời đủ ba câu, cho biết tính được đạo hàm nhưng chưa chắc ý nghĩa của dấu; đọc evidence và độ chắc chắn thấp. Thấy câu hỏi hữu ích khi chưa biết bắt đầu từ đâu, nhưng quay lại A để tự chọn kiến thức.
- **C:** đọc tín hiệu “dừng 4 phút, sửa 2 lần” rồi chọn “Để sau”; hiểu tín hiệu chỉ thuộc phiên hiện tại và AI không tự gửi cho trợ giảng, nhưng lo prompt có thể ngắt lúc đang suy nghĩ.
- **Lựa chọn và trade-off:** chọn A vì muốn tự chọn nội dung, nhận giải thích đúng chủ đề và tự kiểm tra; A vẫn đòi hỏi learner tự xác định được bước cần ôn. Cân nhắc B như phương án dự phòng nếu không tự gọi tên được chỗ hổng.
- **Câu transfer:** note cá nhân ghi tester đã dùng câu transfer để tự kiểm tra; không ghi rõ kết quả đúng/sai.

### Tổng hợp 3 phiên của nhóm

|Feedback|Tester|Thứ tự|Chọn|Lý do chính|
|---|---|---|---|---|
|1 (Quân)|Đặng Văn Thái Anh|A → B → C|**B**|B thu hẹp đúng chỗ vướng mà không phải tự đoán như A, không bị theo dõi như C. [Note](prototype-feedback-note-dang-van-thai-anh.md)|
|2 (Thanh)|Nguyễn Văn Thăng|A → B → C|**A**|Muốn tự chọn kiến thức và tự kiểm tra; B là dự phòng tốt; C có thể ngắt mạch.|
|3 (Tiến)|Bùi Hải Nam|C → A → B|**C**|Được hỗ trợ sớm mà không phải tự gọi tên lỗ hổng hay trả lời câu hỏi.|

**Pattern:**

- Ở C, **cả 3 tester đều lo ngại** bị theo dõi hoặc bị ngắt mạch, và đều đọc tín hiệu trước khi quyết định.
- Ở A, 2/3 tester **do dự giữa "Dấu đạo hàm" và "Đi ngược gradient"**: tự chẩn đoán vẫn khó.
- Mỗi tester chọn một option khác nhau. Thái Anh chọn B ở lượt thứ hai; Thăng chọn A ở lượt đầu; Nam chọn C ở lượt đầu. Vì hai người chọn option test đầu tiên, lựa chọn có thể chịu ảnh hưởng thứ tự; chưa thể tách sở thích khỏi hiệu ứng thứ tự.

Bảng tổng hợp đầy đủ: [group-feedback-synthesis.md](group-feedback-synthesis.md)

### Next Change nhóm chốt

Chọn **Option B — Cùng AI chẩn đoán** làm cơ chế chính, và thêm lối tắt **"Mình biết cần ôn bước nào"** ở màn hình đầu để learner đã biết chỗ hổng bỏ qua câu hỏi chẩn đoán. Lý do: B giải quyết đúng barrier trong Hypothesis Problem, đáp ứng nhu cầu "không phải tự gọi tên lỗ hổng" của người chọn C mà không cần AI tự xuất hiện, và lối tắt giữ quyền tự chọn mà người chọn A cần. Quyết định này không dựa trên số phiếu (chỉ 1/3 tester chọn B).

### Still Unproven

- **Nhánh phục hồi khi AI chẩn đoán sai:** không tester nào gặp chẩn đoán sai ở B, nên chưa biết "Không đúng, đổi hướng" có giúp quay về đúng chỗ hổng không.
- **Learner có chọn đúng giữa lối tắt và câu hỏi chẩn đoán không**, hay sẽ dùng lối tắt rồi chọn sai bước.
- **Thời điểm prompt C xuất hiện:** cả 3 phiên đều mở C từ màn hình chọn phương án, chưa thử lúc AI tự xuất hiện thật.
- **Hiệu quả học:** chưa đo thời gian hoàn thành so với 30–45 phút ở Day 17, chưa đo mức hiểu khi đổi dạng bài.
- **Cỡ mẫu:** chỉ 3 tester; Thái Anh đã quen chủ đề từ buổi phỏng vấn Day 17.

## 6. AI Support Log

- **Công cụ:** Claude Code trong VS Code được ghi nhận cho công việc prototype/lab trước đó; Codex hỗ trợ rà soát và chỉnh README, prototype, feedback notes trong lượt hoàn thiện này.
- **AI hỗ trợ cá nhân:** chuyển cơ chế Option B thành flow và nội dung prototype; diễn đạt Human–AI decisions cho B; chuẩn bị prompt và observation focus; định dạng feedback note dựa trên dữ liệu tester tôi cung cấp; rà sự nhất quán giữa vai trò cá nhân, thứ tự test và các note.
- **Tôi quyết định và cung cấp:** Option B là phần tôi phụ trách; nội dung thật của phiên do tôi dẫn dắt lấy từ `prototype-feedback-note.md` (Nguyễn Văn Thăng, chọn A); chi tiết phiên Đặng Văn Thái Anh do đồng đội Trần Đức Quân dẫn dắt được giữ ở note riêng. Tôi kiểm tra và xác nhận các sửa đổi theo những note đó.
- **Giới hạn:** AI không tham gia các buổi test và không tạo observation/quote thật. Một bộ review giả lập từng được tạo theo yêu cầu để minh họa format; bộ đó được đánh dấu rõ là mẫu luyện tập, không dùng thay feedback thật. Prototype dùng canned output, không kết nối model/API.
- **Sai sót và cách tôi sửa:** AI ban đầu đặt nhầm phiên của Quân vào phần test cá nhân của tôi; tôi chỉ rõ phải theo note của Thăng, sau đó sửa facilitator, tester, lựa chọn và thứ tự. Khi phát hiện thứ tự trong note khác bảng tổng hợp, tôi lấy note cá nhân làm nguồn chi tiết và cập nhật phần tổng hợp để phản ánh khả năng ảnh hưởng của thứ tự. AI cũng phát hiện bản B tích hợp hiển thị lời giải trước khi learner xác nhận; đã thêm bước xác nhận riêng.

Nhật ký chi tiết, gồm mục đích, phạm vi hỗ trợ, kiểm chứng và giới hạn: [ai-support-log.md](ai-support-log.md).
