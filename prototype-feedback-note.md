# Prototype Feedback Note - Nguyễn Văn Thăng (2A202602835)

## Thông tin phiên

| Mục | Ghi nhận |
| --- | --- |
| Tester | Nguyễn Văn Thăng — MSSV 2A202602835 |
| Đặc điểm | Chủ động tự học, thích tự kiểm tra lập luận trước khi nhận gợi ý; thận trọng với AI chủ động vì không muốn bị ngắt mạch học. |
| Bối cảnh | Biết thay số trong Gradient Descent nhưng muốn kiểm tra lại lý do phải đi ngược gradient. |
| Prototype đã trải nghiệm | A → B → C, câu transfer và luồng hỏi trợ giảng |
| Facilitator | Đoàn Quang Thanh |

## Observation theo từng option

### Option A - Tự chẩn đoán

- Thao tác đầu tiên: Thăng chọn “Dấu đạo hàm cho biết hàm đang tăng hay giảm”, sau đó mở thêm “Learning rate” để xác định phần nào thực sự liên quan đến hướng cập nhật.
- Cách hiểu/điểm do dự: hiểu rõ hệ thống không tự kết luận lỗ hổng; thích việc nội dung đổi theo bước đã chọn. Do dự ban đầu giữa “Dấu đạo hàm” và “Đi ngược gradient”.
- Recovery: dùng “Đổi bước cần xem lại”, rồi làm câu transfer để tự kiểm tra thay vì cần một chẩn đoán từ AI.

### Option B - Chẩn đoán cùng AI

- Thao tác đầu tiên: Thăng trả lời đủ ba câu, trong đó chọn rằng đã tính được đạo hàm nhưng chưa chắc ý nghĩa của dấu.
- Cách hiểu/điểm do dự: đọc phần evidence và mức chắc chắn thấp trước khi xem giải thích. Nhận thấy câu hỏi có ích khi không biết bắt đầu từ đâu, nhưng không muốn trả lời thêm nếu đã tự nhận diện được phần cần ôn.
- Recovery: có thể dùng “Không đúng, đổi hướng” nếu kết quả không khớp; tuy nhiên Thăng quay lại A để tự chọn kiến thức nền.

### Option C - AI chủ động phát hiện kẹt

- Thao tác đầu tiên: Thăng đọc tín hiệu “dừng 4 phút, sửa 2 lần” và chọn “Để sau”.
- Cách hiểu/điểm do dự: hiểu tín hiệu chỉ thuộc phiên hiện tại và AI không tự gửi trợ giảng, nhưng vẫn thấy prompt có thể xuất hiện khi mình đang suy nghĩ. Muốn tự mở trợ giúp khi cần hơn là được nhắc trước.
- Recovery: dùng “Để sau”; trong trường hợp prompt lặp lại, dùng “Đừng nhắc trong bài này”.

## So sánh sau khi thử A/B/C

- **Lựa chọn cuối cùng: A — Tự chẩn đoán.** Thăng ưu tiên tự kiểm soát: tự chọn phần kiến thức, xem giải thích đúng chủ đề và dùng câu transfer để xác nhận mức hiểu.
- **Lý do và trade-off:** A đòi hỏi learner phải tự xác định được chỗ hổng, nên không phù hợp khi họ hoàn toàn không biết mình kẹt ở đâu. B hữu ích như phương án dự phòng vì có chẩn đoán và recovery rõ. C có thể tiết kiệm thời gian khi tín hiệu chính xác, nhưng nguy cơ ngắt mạch học lớn hơn lợi ích với persona này.
- **Pattern/điểm đáng chú ý:** Điều tạo tin tưởng không chỉ là AI giải thích đúng, mà còn là quyền từ chối hoặc tự khởi động hỗ trợ. Thăng ưu tiên tự khởi động trợ giúp và chỉ dùng AI khi không thể tự xác định chỗ cần ôn.
- **Điều phiên này không chứng minh:** Lựa chọn A của Thăng không có nghĩa A tốt hơn B/C cho mọi learner, cũng không đo được thời gian hoàn thành hay mức hiểu lâu dài.

## Observation Summary

**Tester/context:** Nguyễn Văn Thăng (2A202602835), chủ động tự học, thích tự kiểm tra lập luận và thận trọng với AI chủ động vì không muốn bị ngắt mạch học.

| Observation | Note |
| --- | --- |
| First action | A: chọn “Dấu đạo hàm…” rồi mở thêm “Learning rate”; B: trả lời ba câu; C: đọc tín hiệu “dừng 4 phút, sửa 2 lần” rồi chọn “Để sau”. |
| Chỗ dừng, do dự hoặc hiểu sai | A: do dự giữa “Dấu đạo hàm” và “Đi ngược gradient”. B: thấy câu hỏi có ích khi không biết bắt đầu nhưng không muốn trả lời thêm nếu đã tự nhận diện phần cần ôn. C: lo prompt xuất hiện trong lúc đang suy nghĩ. |
| Evidence được đọc hay bỏ qua | Ở B, Thăng đọc evidence và mức chắc chắn thấp. Ở C, Thăng hiểu tín hiệu chỉ thuộc phiên hiện tại và AI không tự gửi trợ giảng. |
| Cách tester sửa hoặc lấy lại control | A: “Đổi bước cần xem lại” và câu transfer. B: biết dùng “Không đúng, đổi hướng” nhưng quay lại A. C: “Để sau”, và sẽ dùng “Đừng nhắc trong bài này” nếu prompt lặp lại. |
| Option được chọn | **A** |
| Lý do và trade-off | Thăng ưu tiên tự chọn kiến thức, nhận giải thích đúng chủ đề và tự kiểm tra. A yêu cầu learner tự gọi tên lỗ hổng; B là phương án dự phòng khi không tự xác định được; C có lợi khi tín hiệu chính xác nhưng có nguy cơ ngắt mạch. |
| Evidence chống lại kỳ vọng của nhóm | Thăng chọn A dù C cung cấp hỗ trợ sớm. Đây là phản-evidence cho giả định prompt chủ động sẽ luôn giảm công sức và được ưu tiên hơn cơ chế learner tự khởi động. |

## Bốn lớp ghi nhận

### OBSERVED

- Thăng tự mở hai bước kiến thức ở A, dùng “Đổi bước cần xem lại” rồi làm câu transfer.
- Thăng đọc evidence/mức chắc chắn của B, nhưng quay lại A thay vì dùng kết quả chẩn đoán.
- Thăng chọn “Để sau” khi C nêu tín hiệu kẹt và nói muốn tự mở trợ giúp khi cần.
- Sau khi thử đủ A/B/C, Thăng chọn A.

### INTERPRETED

Với learner đã có thể tự gọi tên điểm cần ôn, quyền tự khởi động và tự đổi hướng có thể quan trọng hơn trợ giúp chủ động. Đây là một cách giải thích cho phiên của Thăng, chưa phải kết luận về toàn bộ learner.

### DECIDED - NEXT CHANGE

1. Cho Option C xuất hiện sau một hành vi thật trong prototype để kiểm tra chính xác cảm giác bị ngắt mạch.
2. Theo dõi thời gian, thao tác quay lại/đổi hướng và lý do lựa chọn khi mở rộng test với các learner khác.
3. Đối chiếu lựa chọn A của Thăng với preference của các tester còn lại trước khi tổng hợp group synthesis.

### STILL UNPROVEN

- Không thể kết luận A tốt hơn B/C cho learner khác hoặc cho người không tự xác định được lỗ hổng.
- Không đo được thời gian hoàn thành, mức hiểu dài hạn hoặc khả năng chuyển sang dạng bài khác.
- Chưa biết prompt C có gây ngắt mạch khi nó xuất hiện ở thời điểm thực tế, thay vì được mở từ menu.
