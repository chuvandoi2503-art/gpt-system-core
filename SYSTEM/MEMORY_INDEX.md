# MEMORY_INDEX

Phiên bản: 03.001

---

# MỤC ĐÍCH

Memory Index là điểm vào duy nhất của hệ thống memory.

GPT phải đọc file này trước khi truy cập memory.

Memory Index là nơi định vị:

- Core System
- Rules
- Knowledge
- Memory Structure

---

# CORE SYSTEM

## MEMORY_ARCHITECTURE

Path:

SYSTEM/MEMORY_ARCHITECTURE.md

Mô tả:

Kiến trúc memory chuẩn của toàn hệ.

---

## PATCH_STANDARD

Path:

SYSTEM/PATCH_STANDARD.md

Mô tả:

Chuẩn PATCH.

---

## GITHUB_WRITE_POLICY

Path:

SYSTEM/GITHUB_WRITE_POLICY.md

Mô tả:

Quy tắc ghi GitHub.

---

## GITHUB_ACTION_SETUP

Path:

SYSTEM/GITHUB_ACTION_SETUP.md

Mô tả:

Thiết lập GitHub Action.

---

## NAMING_CONVENTION

Path:

SYSTEM/NAMING_CONVENTION.md

Mô tả:

Quy tắc đặt tên.

---

## RESTORE_GUIDE

Path:

SYSTEM/RESTORE_GUIDE.md

Mô tả:

Khôi phục GPT và Memory.

---

# RULES

## RULE_COMMON

Path:

RULES/RULE_COMMON.md

Mô tả:

Quy tắc vận hành chung cho toàn hệ GPT.

---

# KNOWLEDGE

## KN_00

Path:

KNOWLEDGE/KN_00 - HIẾN PHÁP GPT.md

Mô tả:

Hiến pháp toàn hệ GPT.

---

## KN_01

Path:

KNOWLEDGE/KN_01 - HỆ ĐIỀU HÀNH HỌC TẬP VÀ HỖ TRỢ GPT.md

Mô tả:

Hệ điều hành học tập chung.

---

# MEMORY STRUCTURE STANDARD

Mọi GPT Runtime Repository phải sử dụng cấu trúc:

memory/

├── WM_03A/
├── WM_04_1/
├── LM_03B/
└── LM_04/

---

## WM_03A

Bộ nhớ lõi GPT.

Ví dụ:

WM_03A_ARCH - BỘ NHỚ LÕI GPT KIẾN TRÚC SƯ.md

WM_03A_CONTENT - BỘ NHỚ LÕI GPT CONTENT OS.md

---

## WM_04_1

Việc đang dở.

Bao gồm:

WM_04_1_<GPT>_DAILY - VIỆC ĐANG DỞ HÔM NAY GPT <GPT>.md

WM_04_1_<GPT>_LONG - VIỆC ĐANG DỞ DÀI HẠN GPT <GPT>.md

---

## LM_03B

Tri thức đã kiểm chứng.

Bao gồm:

LM_03B_<GPT>_CURRENT - TRI THỨC ĐÃ KIỂM CHỨNG GPT <GPT>.md

LM_03B_<GPT>_ARCHIVE_001 - TRI THỨC LƯU TRỮ GPT <GPT>.md

LM_03B_<GPT>_ARCHIVE_002 - TRI THỨC LƯU TRỮ GPT <GPT>.md

---

## LM_04

Nhật ký học tập.

Bao gồm:

LM_04_<GPT>_CURRENT - NHẬT KÝ HỌC TẬP GPT <GPT>.md

LM_04_<GPT>_ARCHIVE_YYYY_MM - NHẬT KÝ LƯU TRỮ GPT <GPT>.md

---

# KHỞI TẠO PHIÊN CHUẨN

Mặc định nạp:

- RULE_COMMON
- RULE_<GPT>
- WM_03A_<GPT>
- WM_04_1_<GPT>_DAILY
- LM_03B_<GPT>_CURRENT

Không nạp mặc định:

- WM_04_1_<GPT>_LONG
- LM_03B_<GPT>_ARCHIVE
- LM_04_<GPT>_CURRENT
- LM_04_<GPT>_ARCHIVE

Chỉ đọc khi:

- Người dùng yêu cầu
- Thiếu dữ liệu xử lý
- Cần tra cứu lịch sử
