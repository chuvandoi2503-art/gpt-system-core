# MEMORY_INDEX

Phiên bản: 03.000

---

# MỤC ĐÍCH

Memory Index là điểm vào duy nhất của hệ thống memory.

GPT phải đọc file này trước khi truy cập memory.

Không được hardcode path memory ngoài các cấu hình hệ thống đã được xác nhận.

---

# SYSTEM

## RULE_COMMON

Path:

```
SYSTEM/RULE_COMMON.md
```

Mô tả:

Quy tắc vận hành chung cho toàn bộ GPT.

---

## MEMORY_ARCHITECTURE

Path:

```
SYSTEM/MEMORY_ARCHITECTURE.md
```

Mô tả:

Kiến trúc memory chuẩn của toàn hệ.

---

## GITHUB_WRITE_POLICY

Path:

```
SYSTEM/GITHUB_WRITE_POLICY.md
```

Mô tả:

Quy tắc ghi GitHub.

---

## PATCH_STANDARD

Path:

```
SYSTEM/PATCH_STANDARD.md
```

Mô tả:

Chuẩn PATCH.

---

## NAMING_CONVENTION

Path:

```
SYSTEM/NAMING_CONVENTION.md
```

Mô tả:

Quy tắc đặt tên.

---

# MEMORY STRUCTURE STANDARD

Mọi GPT phải sử dụng cấu trúc:

```
WM_03A/

WM_04_1/

LM_03B/

LM_04/
```

---

## WM_03A

Bộ nhớ lõi GPT.

Ví dụ:

```
WM_03A_ARCH.md

WM_03A_CONTENT.md
```

---

## WM_04_1

Việc đang dở.

Bao gồm:

```
WM_04_1_DAILY.md

WM_04_1_LONG.md
```

---

## LM_03B

Tri thức đã kiểm chứng.

Bao gồm:

```
LM_03B_CURRENT.md

LM_03B_ARCHIVE_001.md

LM_03B_ARCHIVE_002.md
```

---

## LM_04

Nhật ký học tập.

Bao gồm:

```
LM_04_CURRENT.md

LM_04_ARCHIVE_YYYY_MM.md
```

---

# QUY TẮC KHỞI TẠO PHIÊN CHUẨN

Mặc định nạp:

```
RULE_COMMON

RULE_<GPT>

WM_03A_<GPT>

WM_04_1_DAILY

LM_03B_CURRENT
```

---

Không nạp mặc định:

```
WM_04_1_LONG

LM_03B_ARCHIVE

LM_04_CURRENT

LM_04_ARCHIVE
```

---

Chỉ đọc khi:

* Người dùng yêu cầu
* Thiếu dữ liệu xử lý
* Cần tra cứu lịch sử

```
```
