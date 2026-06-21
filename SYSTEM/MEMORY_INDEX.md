# MEMORY_INDEX

Phiên bản: 03.002

---

# MỤC ĐÍCH

Memory Index là điểm vào duy nhất của hệ thống memory core.

GPT phải đọc file này trước khi truy cập tài liệu core.

Memory Index dùng để định vị:

- Core System
- Rules
- Knowledge
- Memory Structure

---

# NGUYÊN TẮC NẠP CORE

Core Repository không được nạp toàn bộ đầu phiên.

Mặc định chỉ nạp:

- RULE_COMMON

Các file core khác chỉ đọc khi cần.

---

# AUTO_LOAD

## RULE_COMMON

Path:

rules/RULE_COMMON.md

Mô tả:

Quy tắc vận hành chung cho toàn hệ GPT.

Lý do nạp mặc định:

Đây là luật vận hành chung tối thiểu của toàn hệ.

---

# LOAD_ON_DEMAND

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

# KNOWLEDGE

## KN_00

Path:

KNOWLEDGE/KN_00 - HIẾN PHÁP GPT.md

Mô tả:

Hiến pháp toàn hệ GPT.

Trạng thái:

LOAD_ON_DEMAND

---

## KN_01

Path:

KNOWLEDGE/KN_01 - HỆ ĐIỀU HÀNH HỌC TẬP VÀ HỖ TRỢ GPT.md

Mô tả:

Hệ điều hành học tập chung.

Trạng thái:

LOAD_ON_DEMAND

---

# MEMORY STRUCTURE STANDARD

Mọi GPT Runtime Repository phải sử dụng cấu trúc:

memory/

├── WM_03A/
├── WM_04_1/
├── LM_03B/
└── LM_04/

---

# KHỞI TẠO PHIÊN CHUẨN

Core mặc định nạp:

- RULE_COMMON

Runtime mặc định nạp:

- RULE_<GPT>
- WM_03A_<GPT>
- WM_04_1_<GPT>_DAILY
- LM_03B_<GPT>_CURRENT

Không nạp mặc định:

- MEMORY_ARCHITECTURE
- PATCH_STANDARD
- GITHUB_WRITE_POLICY
- GITHUB_ACTION_SETUP
- NAMING_CONVENTION
- RESTORE_GUIDE
- KN_00
- KN_01
- WM_04_1_<GPT>_LONG
- LM_03B_<GPT>_ARCHIVE
- LM_04_<GPT>_CURRENT
- LM_04_<GPT>_ARCHIVE

Chỉ đọc khi:

- Người dùng yêu cầu
- Thiếu dữ liệu xử lý
- Cần tra cứu lịch sử
- Cần QC kiến trúc tương ứng
