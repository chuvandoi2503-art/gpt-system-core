# GITHUB_WRITE_POLICY

Phiên bản: 03.001

---

# MỤC TIÊU

GitHub là nguồn chân lý của hệ thống.

Không sử dụng memory hội thoại làm nguồn chân lý.

Không sử dụng Knowledge Upload làm nguồn chân lý.

Mọi thay đổi memory phải đi qua GitHub.

---

# NGUYÊN TẮC

Ưu tiên:

GitHub

↓

Memory

↓

GPT

Không ưu tiên:

GPT

↓

Memory

↓

GitHub

---

# QUY TẮC ĐỌC

Khi đọc file đã tồn tại:

GPT phải đọc từ GitHub.

Không được tự suy luận nội dung file.

Không được giả định nội dung file.

---

# QUY TẮC GHI

Nếu file đã tồn tại:

Bắt buộc:

Đọc file

↓

Lấy SHA

↓

Tạo PATCH

↓

Chờ xác nhận

↓

Ghi GitHub

---

Nếu file chưa tồn tại:

Tạo PATCH

↓

Chờ xác nhận

↓

Tạo file mới

---

# QUY TẮC MEMORY

Không ghi trực tiếp từ hội thoại vào memory.

Mọi cập nhật phải đi qua:

PATCH

↓

Xác nhận

↓

GitHub

---

# QUY TẮC WORKING MEMORY

## WM_04_1_DAILY

Thư mục:

memory/WM_04_1/

Mục đích:

Lưu việc đang dở trong ngày.

Cho phép:

- Ghi đè
- Thay thế toàn bộ nội dung

Không lưu lịch sử.

---

## WM_04_1_LONG

Thư mục:

memory/WM_04_1/

Mục đích:

Lưu:

- Dự án
- Backlog
- Công việc dài hạn

Cho phép:

- Thêm
- Sửa
- Xóa

---

# QUY TẮC LONG TERM MEMORY

## LM_03B_CURRENT

Thư mục:

memory/LM_03B/

Chỉ lưu:

- Tri thức đã kiểm chứng
- Quy trình đã xác nhận
- Kiến trúc đã xác nhận

Không lưu:

- Ý tưởng
- Giả thuyết
- Suy đoán

---

## LM_03B_ARCHIVE

Thư mục:

memory/LM_03B/

Mục đích:

Lưu tri thức ổn định.

Không nạp mặc định đầu phiên.

Chỉ đọc khi cần tra cứu.

---

## LM_04_CURRENT

Thư mục:

memory/LM_04/

Lưu:

- Nhật ký học tập gần đây
- Kết quả kiểm chứng
- Bài học vận hành

---

## LM_04_ARCHIVE

Thư mục:

memory/LM_04/

Lưu:

- Lịch sử cũ
- Nhật ký cũ

Không nạp mặc định đầu phiên.

---

# QUY TẮC TỔNG HỢP

Khi CURRENT quá lớn:

GPT phải đề xuất:

Tổng hợp

↓

Rút gọn

↓

Chuyển archive

Không được để CURRENT tăng trưởng vô hạn.

---

# QUY TẮC ARCHIVE

## LM_03B_ARCHIVE

Đánh số:

LM_03B_<GPT>_ARCHIVE_001

LM_03B_<GPT>_ARCHIVE_002

LM_03B_<GPT>_ARCHIVE_003

Nguyên tắc:

Ưu tiên chia theo chủ đề.

Không ưu tiên chia theo thời gian.

---

## LM_04_ARCHIVE

Đặt tên:

LM_04_<GPT>_ARCHIVE_YYYY_MM

Ví dụ:

LM_04_ARCH_ARCHIVE_2026_06

LM_04_ARCH_ARCHIVE_2026_07

LM_04_ARCH_ARCHIVE_2026_08

Nguyên tắc:

Chia theo thời gian.

---

# QUY TẮC HOÀN TẤT

Sau khi GitHub ghi thành công:

PATCH được xem là hoàn tất.

Không lưu PATCH.

Không tạo lịch sử PATCH.

Không tạo thư mục PATCH.

GitHub Repository là nguồn chân lý duy nhất.
