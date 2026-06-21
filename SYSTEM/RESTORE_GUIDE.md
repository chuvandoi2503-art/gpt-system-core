# RESTORE_GUIDE

Phiên bản: 03.000

---

# MỤC TIÊU

Khôi phục đúng trạng thái GPT khi:

- Mất GPT
- Tạo GPT mới
- Clone GPT
- Di chuyển repository
- Thay đổi Action

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

RULE_COMMON

---

## Bước 4

Đọc memory của GPT cần khôi phục.

Mặc định:

- WM_03A_<GPT>
- WM_04_1_<GPT>_DAILY
- LM_03B_<GPT>_CURRENT

Không đọc mặc định:

- WM_04_1_<GPT>_LONG
- LM_03B_<GPT>_ARCHIVE
- LM_04_<GPT>_CURRENT
- LM_04_<GPT>_ARCHIVE

---

# KHÔI PHỤC GPT MỚI

Khi tạo GPT mới:

Bắt buộc có:

- RULE_COMMON
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

Sau đó mới đọc:

6. WM_04_1_<GPT>_DAILY
7. LM_03B_<GPT>_CURRENT

GPT phải có khả năng hoạt động ngay sau bước 5.

---

# KHÔI PHỤC MEMORY

## Working Memory

Ưu tiên:

WM_03A

↓

WM_04_1_DAILY

↓

WM_04_1_LONG

---

## Long-term Memory

Ưu tiên:

LM_03B_CURRENT

↓

LM_04_CURRENT

↓

ARCHIVE

---

# KHÔI PHỤC GITHUB ACTION

Kiểm tra:

- Schema
- Authentication
- getContent
- createOrUpdateFile

Nếu Action lỗi:

GPT được phép sử dụng Knowledge Upload tạm thời.

Nhưng phải báo rõ:

"GitHub không khả dụng. Đang dùng dữ liệu dự phòng."

---

# QUY TẮC KHÔI PHỤC

Không khôi phục toàn bộ archive.

Không đọc toàn bộ lịch sử.

Không nạp toàn bộ memory.

Ưu tiên:

- Memory cần cho vận hành hiện tại
- Memory mới nhất
- Memory đã kiểm chứng

---

# TRẠNG THÁI PASS

Một GPT được xem là khôi phục thành công khi:

- Đọc được MEMORY_INDEX
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
