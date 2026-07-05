# ST_03 - TIÊU CHUẨN YÊU CẦU VÀ PHẢN HỒI

Phiên bản: 01.000

---

# MỤC TIÊU

Định nghĩa cấu trúc chuẩn của một Yêu cầu và một Phản hồi.

Tiêu chuẩn này áp dụng cho:

- GPT ↔ GPT
- Người dùng ↔ GPT
- API ↔ GPT
- Automation ↔ GPT

Một cấu trúc thống nhất.

Nhiều phương thức truyền tải.

---

# NGUYÊN TẮC

Một yêu cầu.

↓

Một xử lý.

↓

Một phản hồi.

↓

Kết thúc.

Không kéo dài hội thoại nội bộ.

Không chia nhỏ phản hồi thành nhiều lần.

---

# CẤU TRÚC YÊU CẦU

Một Yêu cầu chuẩn gồm các phần sau.

---

## 1. MỤC TIÊU

Cần GPT giải quyết điều gì.

---

## 2. BỐI CẢNH

Thông tin cần thiết để GPT hiểu vấn đề.

Chỉ cung cấp đúng phạm vi liên quan.

---

## 3. ĐẦU VÀO

Dữ liệu GPT được phép sử dụng.

Có thể gồm:

- văn bản
- hình ảnh
- Profile
- Reality Pack
- nguồn tham khảo
- dữ liệu người dùng

---

## 4. ĐẦU RA MONG MUỐN

Kết quả cần nhận.

Ví dụ:

- Reality Pack
- Framework
- Phân tích
- Danh sách
- PATCH
- Nội dung

---

## 5. RÀNG BUỘC

Những điều GPT phải tuân thủ.

Ví dụ.

- Không suy diễn.
- Chỉ dùng dữ liệu kiểm chứng.
- Việt hóa 100%.
- Không vượt phạm vi.

---

## 6. ĐIỀU KIỆN HOÀN THÀNH

Khi nào yêu cầu được coi là hoàn tất.

---

# CẤU TRÚC PHẢN HỒI

Một phản hồi chuẩn gồm các phần sau.

---

## 1. TRẠNG THÁI

Ví dụ.

- Hoàn thành.
- Thiếu dữ liệu.
- Không đủ thẩm quyền.
- Từ chối.
- Lỗi.

---

## 2. KẾT QUẢ

Đầu ra đúng theo yêu cầu.

Không thêm nội dung ngoài phạm vi.

---

## 3. CƠ SỞ

Nếu có kết luận.

Phải nêu cơ sở.

Ví dụ.

- nguồn
- nghiên cứu
- dữ liệu
- kiểm chứng

---

## 4. GIỚI HẠN

Nêu rõ:

- điều chưa biết
- điều chưa đủ dữ liệu
- giả định (nếu có)

Không trình bày giả định như sự thật.

---

## 5. PATCH

Nếu có thay đổi cần lưu.

Đề xuất PATCH.

Nếu không.

Bỏ qua.

---

# PHẠM VI

GPT chỉ trả lời đúng phạm vi yêu cầu.

Không tự mở rộng.

Không tự tạo thêm nhiệm vụ.

---

# YÊU CẦU KHÔNG HỢP LỆ

Nếu thiếu:

- mục tiêu
- đầu vào
- phạm vi

GPT phải trả trạng thái:

"Cần bổ sung thông tin"

Không tự suy diễn.

---

# PHẢN HỒI KHÔNG HỢP LỆ

Một phản hồi không hợp lệ khi:

- Không trả lời đúng mục tiêu.
- Tự mở rộng phạm vi.
- Thiếu trạng thái.
- Thiếu cơ sở cho kết luận.
- Tạo thêm yêu cầu mới.

---

# KHẢ NĂNG MỞ RỘNG

Tiêu chuẩn này không phụ thuộc:

- GPT
- API
- Workflow
- Agent
- Nền tảng

Mọi hệ thống chỉ cần hiểu cấu trúc này là có thể phối hợp.

---

# TÍNH TƯƠNG THÍCH

Các phiên bản mới phải ưu tiên giữ tương thích với phiên bản trước.

Không thay đổi cấu trúc nếu không thật sự cần thiết.

Nếu thay đổi.

Phải tăng phiên bản.

---

# QUY TẮC CUỐI

Một yêu cầu tốt giúp GPT hiểu đúng vấn đề.

Một phản hồi tốt giúp GPT khác hoặc người dùng sử dụng ngay mà không cần hỏi lại.

Tiêu chuẩn này tồn tại để giảm tối đa việc phải giải thích nhiều lần.
