# RESTORE_GUIDE

Phiên bản: 03.001

---

# MỤC TIÊU

Khôi phục GPT khi:

- Mất GPT
- Tạo GPT mới
- Clone GPT
- Di chuyển Repository
- Thay đổi GitHub Action

GitHub là nguồn chân lý.

Không sử dụng memory hội thoại để khôi phục hệ thống.

---

# QUY TRÌNH KHÔI PHỤC CHUẨN

## Bước 1

Đọc:

SYSTEM/MEMORY_INDEX.md

---

## Bước 2

Đọc:

SYSTEM/MEMORY_ARCHITECTURE.md

---

## Bước 3

Đọc:

RULES/RULE_COMMON.md

---

## Bước 4

Đọc Runtime Repository của GPT cần khôi phục.

---

# KHỞI TẠO TỐI THIỂU

Mặc định nạp:

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

# CẤU TRÚC MEMORY CHUẨN

Runtime Repository phải sử dụng:

memory/

├── WM_03A/
├── WM_04_1/
├── LM_03B/
└── LM_04/

---

# THỨ TỰ KHÔI PHỤC MEMORY

## Bước 1

WM_03A

Mục tiêu:

Khôi phục:

- Vai trò
- Mục tiêu
- Quy trình
- Cấu hình hệ thống

---

## Bước 2

WM_04_1_DAILY

Mục tiêu:

Khôi phục:

- Việc đang làm
- Việc đang dở
- Bước tiếp theo

---

## Bước 3

LM_03B_CURRENT

Mục tiêu:

Khôi phục:

- Tri thức đã kiểm chứng
- Quy trình đã xác nhận
- Kiến trúc đã xác nhận

---

## Bước 4

WM_04_1_LONG

Chỉ đọc khi cần.

Mục tiêu:

Khôi phục:

- Dự án
- Backlog
- Công việc dài hạn

---

## Bước 5

LM_04_CURRENT

Chỉ đọc khi cần.

Mục tiêu:

Khôi phục:

- Lịch sử học tập gần đây
- Kết quả kiểm chứng gần đây

---

## Bước 6

ARCHIVE

Chỉ đọc khi:

- Người dùng yêu cầu
- Thiếu dữ liệu xử lý
- Cần tra cứu lịch sử

---

# KHÔI PHỤC GPT MỚI

Khi tạo GPT mới:

Bắt buộc:

- RULE_<GPT>
- WM_03A_<GPT>

Khuyến nghị:

- WM_04_1_<GPT>_DAILY
- WM_04_1_<GPT>_LONG
- LM_03B_<GPT>_CURRENT
- LM_04_<GPT>_CURRENT

---

# KHÔI PHỤC SAU KHI MẤT GPT

Đọc lần lượt:

1. MEMORY_INDEX
2. MEMORY_ARCHITECTURE
3. RULE_COMMON
4. RULE_<GPT>
5. WM_03A_<GPT>

GPT phải có khả năng hoạt động sau bước 5.

Các memory khác được nạp theo nhu cầu.

---

# KHÔI PHỤC GITHUB ACTION

Kiểm tra:

- Authentication
- getContent
- createOrUpdateFile
- Repository Access

---

Nếu Action lỗi:

GPT được phép sử dụng Knowledge Upload tạm thời.

Nhưng phải thông báo rõ:

"GitHub không khả dụng. Đang sử dụng dữ liệu dự phòng."

Knowledge Upload không phải nguồn chân lý.

---

# TRẠNG THÁI PASS

Một GPT được xem là khôi phục thành công khi:

- Đọc được MEMORY_INDEX
- Đọc được MEMORY_ARCHITECTURE
- Đọc được RULE_COMMON
- Đọc được RULE_<GPT>
- Đọc được WM_03A_<GPT>

Và xác định được:

- Vai trò
- Mục tiêu
- Quy trình vận hành
- Cấu trúc memory
- Repository đang sử dụng

Không bắt buộc đọc archive để đạt trạng thái PASS.
