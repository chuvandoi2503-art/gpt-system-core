# MEMORY_ARCHITECTURE

Phiên bản: 03.001

---

# MỤC TIÊU

Hệ thống memory phải:

- Đơn giản
- Dễ nhân bản
- Dễ bảo trì
- Dễ mở rộng
- Không phình vô hạn
- Không tồn đọng patch
- Có thể vận hành nhiều năm

---

# NGUYÊN TẮC

GitHub là nguồn chân lý.

Memory phải phục vụ vận hành.

Không sử dụng một file memory tăng trưởng vô hạn.

Ưu tiên thư mục rõ vai trò.

Ưu tiên nhiều file nhỏ theo chức năng.

Ưu tiên giảm dữ liệu phải nạp đầu phiên.

---

# CẤU TRÚC THƯ MỤC CHUẨN

Mọi Runtime Repository phải sử dụng:

memory/

├── WM_03A/
├── WM_04_1/
├── LM_03B/
└── LM_04/

---

# WM_03A

Bộ nhớ lõi GPT.

Mỗi GPT chỉ có một file WM_03A.

Ví dụ:

memory/WM_03A/

- WM_03A_ARCH - BỘ NHỚ LÕI GPT KIẾN TRÚC SƯ.md
- WM_03A_CONTENT - BỘ NHỚ LÕI GPT CONTENT OS.md

---

## Vai trò

Lưu:

- Vai trò
- Mục tiêu
- Quy trình vận hành
- Cấu hình hệ thống
- Triết lý hoạt động

---

## Quy tắc

- Nạp đầu phiên
- Kích thước nhỏ
- Chỉ thay đổi khi hệ thống thay đổi

---

# WM_04_1

Việc đang dở.

Sử dụng thư mục:

memory/WM_04_1/

---

## WM_04_1_DAILY

Ví dụ:

- WM_04_1_ARCH_DAILY - VIỆC ĐANG DỞ HÔM NAY GPT KIẾN TRÚC SƯ.md

---

### Vai trò

Lưu:

- Việc đang làm hôm nay
- Việc đang dở phiên gần nhất
- Bước tiếp theo cần thực hiện

---

### Quy tắc

- Nạp đầu phiên
- Được ghi đè
- Không archive
- Không lưu lịch sử
- Không lưu tri thức
- Không lưu backlog dài hạn

Nếu việc kéo dài nhiều ngày:

Chuyển sang:

WM_04_1_LONG

---

## WM_04_1_LONG

Ví dụ:

- WM_04_1_ARCH_LONG - VIỆC ĐANG DỞ DÀI HẠN GPT KIẾN TRÚC SƯ.md

---

### Vai trò

Lưu:

- Dự án
- Backlog
- Công việc tuần
- Công việc tháng
- Công việc quý

---

### Quy tắc

- Không nạp mặc định đầu phiên
- Chỉ đọc khi cần
- Không lưu tri thức
- Không lưu nhật ký

Khi hoàn thành:

- Chuyển sang LM_04_CURRENT

hoặc

- Chuyển sang LM_03B_CURRENT

Khi không còn giá trị:

- DISCARD

---

# LM_03B

Tri thức đã kiểm chứng.

Sử dụng thư mục:

memory/LM_03B/

---

## LM_03B_CURRENT

Ví dụ:

- LM_03B_ARCH_CURRENT - TRI THỨC ĐÃ KIỂM CHỨNG GPT KIẾN TRÚC SƯ.md

---

### Vai trò

Lưu:

- Kiến thức đã xác nhận
- Workflow đã xác nhận
- Quy trình đã xác nhận
- Bài học đã xác nhận

---

### Quy tắc

Không lưu:

- Ý tưởng
- Giả thuyết
- Suy đoán

Có thể nạp đầu phiên.

---

### Ngưỡng tổng hợp

Khi:

- Trên 300 dòng

hoặc

- Trên 50 mục tri thức

thì phải:

- Tổng hợp
- Rút gọn
- Chuyển tri thức ổn định sang Archive

---

## LM_03B_ARCHIVE

Ví dụ:

- LM_03B_ARCH_ARCHIVE_001 - TRI THỨC LƯU TRỮ GPT KIẾN TRÚC SƯ.md
- LM_03B_ARCH_ARCHIVE_002 - TRI THỨC LƯU TRỮ GPT KIẾN TRÚC SƯ.md

---

### Vai trò

Lưu tri thức ổn định.

---

### Quy tắc

- Không nạp đầu phiên
- Chỉ đọc khi tra cứu

Không chia theo thời gian.

Ưu tiên chia theo chủ đề.

Ví dụ:

Archive 001

- Kiến trúc GPT

Archive 002

- GitHub Memory

Archive 003

- Content System

---

### Tạo Archive mới

Chỉ tạo archive mới khi:

- Archive hiện tại vượt khoảng 1000 dòng

hoặc

- Xuất hiện nhóm tri thức mới đủ lớn

---

# LM_04

Nhật ký học tập.

Sử dụng thư mục:

memory/LM_04/

---

## LM_04_CURRENT

Ví dụ:

- LM_04_ARCH_CURRENT - NHẬT KÝ HỌC TẬP GPT KIẾN TRÚC SƯ.md

---

### Vai trò

Lưu:

- Bài học gần đây
- Kết quả kiểm chứng
- Lịch sử học tập gần đây

---

### Quy tắc

- Không bắt buộc nạp đầu phiên
- Chỉ đọc khi cần tra cứu

Khi quá lớn:

Chuyển sang Archive.

---

## LM_04_ARCHIVE

Ví dụ:

- LM_04_ARCH_ARCHIVE_2026_06 - NHẬT KÝ LƯU TRỮ GPT KIẾN TRÚC SƯ.md
- LM_04_ARCH_ARCHIVE_2026_07 - NHẬT KÝ LƯU TRỮ GPT KIẾN TRÚC SƯ.md

---

### Vai trò

Lưu lịch sử cũ.

---

### Quy tắc

- Không nạp đầu phiên
- Chỉ đọc khi tra cứu

Chia theo thời gian.

Định dạng:

LM_04_<GPT>_ARCHIVE_YYYY_MM

---

# KHỞI TẠO PHIÊN CHUẨN

Mặc định chỉ nạp:

- RULE_COMMON
- RULE_<GPT>
- WM_03A_<GPT>
- WM_04_1_<GPT>_DAILY
- LM_03B_<GPT>_CURRENT

---

Không nạp mặc định:

- WM_04_1_<GPT>_LONG
- LM_03B_<GPT>_ARCHIVE
- LM_04_<GPT>_CURRENT
- LM_04_<GPT>_ARCHIVE

---

Chỉ đọc khi:

- Người dùng yêu cầu
- Thiếu dữ liệu xử lý
- Cần tra cứu lịch sử

---

# KẾT THÚC PHIÊN CHUẨN

PATCH phải được phân loại:

- UPDATE_WM_03A
- UPDATE_WM_04_1_DAILY
- UPDATE_WM_04_1_LONG
- UPDATE_LM_03B_CURRENT
- UPDATE_LM_04_CURRENT
- DISCARD

---

Sau khi người dùng xác nhận:

Ghi trực tiếp vào file đích.

Không lưu patch tồn đọng.

---

# QUY TẮC CUỐI CÙNG

Không để một file memory trở thành nơi chứa mọi thứ.

Nếu file bắt đầu phình:

- Kiểm tra lại vai trò file
- Tổng hợp nếu cần
- Archive nếu cần
- Giữ đúng kiến trúc memory

Memory tốt là memory giúp GPT vận hành nhẹ hơn, không phải memory lưu nhiều hơn.
