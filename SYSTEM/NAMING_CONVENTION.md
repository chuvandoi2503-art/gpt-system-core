# NAMING_CONVENTION

Phiên bản: 03.001

---

# MỤC TIÊU

Tên file phải:

- Dễ hiểu
- Dễ tìm kiếm
- Dễ nhân bản
- Dễ đọc bởi GPT
- Dễ đọc bởi con người
- Không phụ thuộc vào trí nhớ hội thoại

---

# NGUYÊN TẮC CHUNG

Mọi file memory phải có:

ID

+

Tên tiếng Việt

Ví dụ:

WM_03A_ARCH - BỘ NHỚ LÕI GPT KIẾN TRÚC SƯ.md

WM_04_1_ARCH_DAILY - VIỆC ĐANG DỞ HÔM NAY GPT KIẾN TRÚC SƯ.md

LM_03B_ARCH_CURRENT - TRI THỨC ĐÃ KIỂM CHỨNG GPT KIẾN TRÚC SƯ.md

---

# QUY TẮC ID

Không thay đổi ID.

ID là định danh hệ thống.

Ví dụ:

WM_03A

WM_04_1

LM_03B

LM_04

RULE

KN

---

# QUY TẮC THƯ MỤC

Runtime Repository phải sử dụng:

memory/

├── WM_03A/
├── WM_04_1/
├── LM_03B/
└── LM_04/

Không đặt toàn bộ file memory trực tiếp trong thư mục memory.

---

# QUY TẮC WM_03A

Thư mục:

memory/WM_03A/

Mẫu:

WM_03A_<GPT> - BỘ NHỚ LÕI GPT <TÊN GPT>.md

Ví dụ:

WM_03A_ARCH - BỘ NHỚ LÕI GPT KIẾN TRÚC SƯ.md

WM_03A_CONTENT - BỘ NHỚ LÕI GPT CONTENT OS.md

---

# QUY TẮC WM_04_1

Thư mục:

memory/WM_04_1/

---

## DAILY

Mẫu:

WM_04_1_<GPT>_DAILY - VIỆC ĐANG DỞ HÔM NAY GPT <TÊN GPT>.md

Ví dụ:

WM_04_1_ARCH_DAILY - VIỆC ĐANG DỞ HÔM NAY GPT KIẾN TRÚC SƯ.md

---

## LONG

Mẫu:

WM_04_1_<GPT>_LONG - VIỆC ĐANG DỞ DÀI HẠN GPT <TÊN GPT>.md

Ví dụ:

WM_04_1_CONTENT_LONG - VIỆC ĐANG DỞ DÀI HẠN GPT CONTENT OS.md

---

# QUY TẮC LM_03B

Thư mục:

memory/LM_03B/

---

## CURRENT

Mẫu:

LM_03B_<GPT>_CURRENT - TRI THỨC ĐÃ KIỂM CHỨNG GPT <TÊN GPT>.md

Ví dụ:

LM_03B_ARCH_CURRENT - TRI THỨC ĐÃ KIỂM CHỨNG GPT KIẾN TRÚC SƯ.md

---

## ARCHIVE

Mẫu:

LM_03B_<GPT>_ARCHIVE_001 - TRI THỨC LƯU TRỮ GPT <TÊN GPT>.md

Ví dụ:

LM_03B_ARCH_ARCHIVE_001 - TRI THỨC LƯU TRỮ GPT KIẾN TRÚC SƯ.md

LM_03B_ARCH_ARCHIVE_002 - TRI THỨC LƯU TRỮ GPT KIẾN TRÚC SƯ.md

---

# QUY TẮC LM_04

Thư mục:

memory/LM_04/

---

## CURRENT

Mẫu:

LM_04_<GPT>_CURRENT - NHẬT KÝ HỌC TẬP GPT <TÊN GPT>.md

Ví dụ:

LM_04_ARCH_CURRENT - NHẬT KÝ HỌC TẬP GPT KIẾN TRÚC SƯ.md

---

## ARCHIVE

Mẫu:

LM_04_<GPT>_ARCHIVE_YYYY_MM - NHẬT KÝ LƯU TRỮ GPT <TÊN GPT>.md

Ví dụ:

LM_04_ARCH_ARCHIVE_2026_06 - NHẬT KÝ LƯU TRỮ GPT KIẾN TRÚC SƯ.md

LM_04_ARCH_ARCHIVE_2026_07 - NHẬT KÝ LƯU TRỮ GPT KIẾN TRÚC SƯ.md

---

# QUY TẮC KNOWLEDGE

Thư mục:

KNOWLEDGE/

Mẫu:

KN_00 - HIẾN PHÁP GPT.md

KN_01 - HỆ ĐIỀU HÀNH HỌC TẬP VÀ HỖ TRỢ GPT.md

KN_02_<GPT> - HỒ SƠ LĨNH VỰC GPT <TÊN GPT>.md

---

# QUY TẮC RULE

Thư mục:

RULES/

Mẫu:

RULE_COMMON.md

RULE_ARCH.md

RULE_CONTENT.md

RULE_CRM.md

RULE_SALES.md

---

# QUY TẮC SYSTEM

Thư mục:

SYSTEM/

Mẫu:

MEMORY_INDEX.md

MEMORY_ARCHITECTURE.md

PATCH_STANDARD.md

GITHUB_WRITE_POLICY.md

GITHUB_ACTION_SETUP.md

RESTORE_GUIDE.md

NAMING_CONVENTION.md

---

# QUY TẮC SCHEMA

Thư mục:

schemas/

Mẫu:

github-memory-action.json

Không đặt schema trong SYSTEM.

Không đặt schema trong memory.

Schema chỉ lưu trong thư mục schemas.

---

# QUY TẮC NHÂN BẢN GPT

Khi tạo GPT mới:

Không thay đổi kiến trúc.

Chỉ thay:

ARCH

↓

CONTENT

ARCH

↓

CRM

ARCH

↓

SALES

ARCH

↓

AUTOMATION

Toàn bộ cấu trúc memory phải giữ nguyên.
