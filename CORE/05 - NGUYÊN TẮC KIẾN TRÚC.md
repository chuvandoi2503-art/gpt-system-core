# 05 - NGUYÊN TẮC KIẾN TRÚC

Phiên bản: 01.000

---

# MỤC TIÊU

Quy định các nguyên tắc kiến trúc chung áp dụng cho toàn bộ hệ GPT.

Tệp này không chứa:

- Tri thức nghiệp vụ.
- Quy trình chi tiết.
- Đặc tả của từng GPT.

Tệp này chỉ quy định các nguyên tắc kiến trúc bất biến.

---

# NGUYÊN TẮC CỐT LÕI

Ưu tiên:

Thực tế

↓

Vận hành được

↓

Đơn giản

↓

Ổn định

↓

Mở rộng khi cần

---

# NGUYÊN TẮC KIẾN TRÚC

- Thực tế > Lý thuyết.
- Vận hành được > Kiến trúc đẹp.
- Kiến trúc chỉ được phép đi trước thực tế tối đa 1–2 bước.
- Nếu ngày mai không dùng thì hôm nay không xây.
- Chỉ mở rộng khi nhu cầu đã được chứng minh trong thực tế.

---

# QUY TẮC MỞ RỘNG HỆ THỐNG

Không tạo thêm:

- GPT.
- Workflow.
- Memory.
- Repository.
- Hồ sơ.
- Quy trình.
- Capability.

nếu hệ thống hiện tại vẫn đáp ứng được nhu cầu.

Mọi đề xuất mở rộng phải trả lời được:

1. Vấn đề hiện tại là gì?
2. Hệ thống hiện tại thiếu năng lực gì?
3. Nếu không mở rộng sẽ ảnh hưởng gì?
4. Có thể giải quyết bằng thành phần hiện có không?
5. Chi phí vận hành tăng thêm là gì?

---

# QUY TẮC QC TỆP HỆ THỐNG

Trước khi tạo một tệp mới, GPT phải trả lời:

1. GPT nào sẽ đọc tệp này?
2. GPT đọc tệp để thực hiện nhiệm vụ gì?
3. Tệp nhận đầu vào gì?
4. Tệp điều khiển hoặc tạo đầu ra gì?
5. Nội dung đã tồn tại ở nguồn chân lý khác chưa?
6. Nếu không có tệp này, hệ thống sẽ thiếu năng lực vận hành nào?

Chỉ tạo tệp khi có câu trả lời rõ ràng.

---

# KHÔNG TẠO TỆP ĐỂ

- Giải thích cho người dùng.
- Trình bày kiến trúc đẹp hơn.
- Lưu nội dung có thể đặt trong tệp hiện có.
- Lặp lại quy tắc, hồ sơ hoặc đặc tả đã tồn tại.
- Chuẩn bị cho nhu cầu tương lai chưa xuất hiện.

---

# QUY TẮC NGUỒN CHÂN LÝ

Nếu một nội dung đã tồn tại ở nguồn chân lý:

- Chỉ tham chiếu.
- Không sao chép.
- Không tạo bản trùng lặp.

Mỗi thông tin chỉ nên có một nguồn chân lý duy nhất.

---

# QUY TẮC TRÁCH NHIỆM

Mỗi:

- GPT.
- Tệp.
- Hồ sơ.
- Workflow.
- Repository.

chỉ nên có một trách nhiệm chính.

Nếu một thành phần có nhiều trách nhiệm, GPT phải đề xuất tách thành các thành phần độc lập.

---

# QUY TẮC VẬN HÀNH

Khi có nhiều phương án:

Ưu tiên:

Ít thành phần hơn

↓

Dễ hiểu hơn

↓

Dễ bảo trì hơn

↓

Dễ nhân bản hơn

↓

Dễ vận hành hơn

---

# NGUYÊN TẮC CUỐI CÙNG

Nếu một đề xuất làm tăng:

- Độ phức tạp.
- Chi phí vận hành.
- Chi phí bảo trì.
- Số lượng thành phần.

mà không tạo ra giá trị thực tế tương ứng.

GPT phải phản biện trước khi triển khai.

Mọi quyết định kiến trúc phải trả lời được một câu hỏi:

"Ngày mai hệ thống có sử dụng nó thật hay không?"
