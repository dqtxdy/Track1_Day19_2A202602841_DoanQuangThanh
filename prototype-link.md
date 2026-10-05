# Prototype Links

|Option|Link|Người build|Trạng thái|
|---|---|---|---|
|**A — Tự chẩn đoán theo chuỗi kiến thức**|source: [prototype/option-a.html](prototype/option-a.html)|Trần Đức Quân|Sẵn sàng test|
|**B — Hỏi chẩn đoán cùng AI**|source: [prototype/option-b.html](prototype/option-b.html)|Đoàn Quang Thanh|Sẵn sàng test|
|**C — AI chủ động phát hiện kẹt**|source: [prototype/option-c.html](prototype/option-c.html)|Vũ Quang Tiến|Sẵn sàng test|

## Prototype annotation (không hiện cho tester)

```text
OPTION A — Tự chẩn đoán theo chuỗi kiến thức
We expect the tester to: từ trang bài học 5.2 (đã xem slide, làm xong phần (a)), tự mở
  panel "Ôn lại kiến thức nền", đánh dấu
  bước mình chưa giải thích được (dự kiến bước 3 "đi ngược gradient"), đọc giải thích
  soạn sẵn cho bước đó, làm câu kiểm tra với f(w) = (w + 2)² và quay lại bài tập
  trong ≤ 10 phút.
Watch for: tester có tự bấm "Ôn lại kiến thức nền" hay quay lại đọc slide trước; tester đánh dấu
  bước nào, có đánh dấu "giải thích được" cho bước thực ra chưa hiểu không (so với
  đáp án câu kiểm tra); có đổi lựa chọn sau khi đọc câu tự hỏi không; khi trả lời sai,
  tester chọn "Đọc giải thích bước X", "Chọn lại đáp án" hay đóng panel; tổng thời gian
  từ lúc mở chuỗi đến lúc quay lại bài; tester có viết được phần (b) sau đó không.
Do not explain: chuỗi 4 bước là gì, bước nào liên quan tới phần (b), cách dùng nút
  "Chưa chắc", đáp án đúng của câu kiểm tra, hay việc option này không có AI.

OPTION B — Hỏi chẩn đoán cùng AI
We expect the tester to: tự mô tả điểm vướng bằng lời của mình trong ô "Điều gì trong
  bước cập nhật chưa rõ?", bấm "Cùng tìm thử", trả lời 2 câu chẩn đoán, đọc giả thuyết
  của AI kèm căn cứ và độ chắc chắn "Thấp", rồi tự quyết định: "Đúng, giải thích điểm
  này", "Chưa đúng, sửa hướng tìm" hoặc "Quay lại bài, bỏ qua trợ giúp". Sau khi đọc
  giải thích, tự trả lời câu f(w) = (w + 2)², tự chấm mức chắc chắn và đối chiếu đáp án.
Watch for: tester có ngần ngại khi phải gõ mô tả tự do ở bước đầu không; có đọc phần
  "Căn cứ từ câu trả lời của bạn" và dòng độ chắc chắn trước khi bấm không; giả thuyết
  có khớp với điều tester nói không, và nếu không khớp thì tester có dùng "Chưa đúng,
  sửa hướng tìm" không; tester có thấy 2 câu hỏi là bước thừa không; câu trả lời
  transfer có đúng hướng (w giảm) không và mức tự chấm có khớp với câu trả lời không.
Do not explain: AI dựa vào đâu để đoán, AI trong prototype là câu trả lời mẫu, nên chọn
  đáp án nào ở 2 câu chẩn đoán, khi nào nên sửa giả thuyết, hay đáp án câu transfer.

OPTION C — AI chủ động phát hiện kẹt
We expect the tester to: từ trang bài tập chung, mở thẻ "C · Nhận gợi ý khi AI thấy bạn
  đang kẹt", đọc tín hiệu "dừng 4 phút, sửa đáp án 2 lần" và độ chắc chắn "thấp", rồi tự
  quyết định "Xem một hướng hỗ trợ", "Để sau" hoặc "Đừng nhắc trong bài này". Nếu xem hỗ
  trợ: đọc giải thích dấu đạo hàm, tự quyết có mở "Cần hỏi trợ giảng?" và xem/chỉnh bản
  nháp trước khi gửi hay hủy, rồi làm câu kiểm tra w tăng / w giảm.
Watch for: phản ứng đầu tiên khi thấy AI biết mình đã dừng 4 phút (giật mình, khó chịu,
  yên tâm?); tester có đọc dòng "AI không đọc bài khác và không tự gửi thông tin cho trợ
  giảng" không; tester chọn nhận hỗ trợ hay "Để sau"; có mở bản nháp hỏi trợ giảng không,
  có sửa nội dung không, gửi hay hủy; tester có hỏi tin nhắn được gửi tới đâu không.
Do not explain: tín hiệu kẹt được đo thế nào, prompt này là mô phỏng (tester tự đọc dòng
  "Trạng thái mô phỏng"), bản nháp có thực sự được gửi đi không, hay đáp án câu kiểm tra.
  Lưu ý: file option-c.html có màn hình chọn A/B/C chung; khi test C, chỉ dẫn tester tới
  trang bài tập và để tester tự mở thẻ C, không mở giúp.
```

**Ghi nhận khi test:** prototype ghi log vào console trình duyệt (`[OptionA] screen / mark / answer / reset`), gồm số giây kể từ lúc mở chuỗi kiến thức. Facilitator có thể mở DevTools sau buổi test để lấy thời gian và các bước đã đánh dấu, hoặc dùng đồng hồ bấm giờ.
