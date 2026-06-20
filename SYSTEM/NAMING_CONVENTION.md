# NAMING_CONVENTION

Phiên bản: 01.000

Trạng thái: Áp dụng toàn hệ

---

# 1. MỤC ĐÍCH

File này quy định chuẩn đặt tên dùng chung cho toàn bộ hệ GPT.

Mục tiêu:

* Dễ đọc.
* Dễ tìm.
* Dễ nhân bản.
* Dễ mở rộng.
* Dễ viết automation.
* Dễ bảo trì.

---

# 2. NGUYÊN TẮC CHUNG

Tên phải:

* Ngắn.
* Rõ nghĩa.
* Nhất quán.
* Dễ đoán.

---

Không dùng:

* Tên ngẫu nhiên.
* Tên cảm tính.
* Tên không có quy luật.

---

# 3. QUY TẮC THƯ MỤC

Chuẩn:

```text
knowledge/
rules/
memory/
SYSTEM/
```

---

Không dùng:

```text
KNOWLEDGE/
Rule/
Memory/
SystemFolder/
```

---

# 4. QUY TẮC KNOWLEDGE

Chuẩn:

```text
KN_<SO>_<TEN>
```

---

Ví dụ:

```text
KN_00
KN_01
KN_02_ARCH
KN_02_CONTENT
KN_02_CRM
```

---

Ý nghĩa:

KN

=

Knowledge

---

# 5. QUY TẮC RULE

Chuẩn:

```text
RULE_<TEN>
```

---

Ví dụ:

```text
RULE_COMMON

RULE_ARCH

RULE_CONTENT

RULE_CRM
```

---

# 6. QUY TẮC WORKING MEMORY

Chuẩn:

```text
WM_<MA>_<TEN>
```

---

Ví dụ:

```text
WM_03A_ARCH

WM_04_1_ARCH

WM_03A_CONTENT

WM_04_1_CONTENT
```

---

# 7. QUY TẮC LONG-TERM MEMORY

Chuẩn:

```text
LM_<MA>_<TEN>
```

---

Ví dụ:

```text
LM_03B_ARCH

LM_04_ARCH

LM_03B_CONTENT

LM_04_CONTENT
```

---

# 8. QUY TẮC TÊN FILE MEMORY

Cấu trúc chuẩn:

```text
<ID> - <TEN VIET HOA>.md
```

---

Ví dụ:

```text
WM_03A_CONTENT - BO NHO LOI GPT CONTENT OS.md

WM_04_1_CONTENT - TRANG THAI CONG VIEC DANG DO GPT CONTENT OS.md

LM_03B_CONTENT - BO NHO DAI HAN GPT CONTENT OS.md
```

---

Mục tiêu:

ID phục vụ GPT.

Tên Việt hóa phục vụ con người.

---

# 9. QUY TẮC TÊN FILE SYSTEM

Ví dụ:

```text
MEMORY_INDEX.md

MEMORY_ARCHITECTURE.md

NAMING_CONVENTION.md

PATCH_STANDARD.md

GITHUB_WRITE_POLICY.md

RESTORE_GUIDE.md

OPENAPI_SCHEMA.md
```

---

Tên file System:

* Không dấu.
* Viết hoa.
* Dùng dấu gạch dưới.

---

# 10. QUY TẮC REPOSITORY

Chuẩn:

```text
gpt-<ten-he>-system
```

---

Ví dụ:

```text
gpt-architect-system

gpt-content-director-system

gpt-system-core

gpt-crm-system
```

---

# 11. QUY TẮC MÃ GPT

Ví dụ:

```text
ARCH

CONTENT

CRM

SALES

AUTO

KNOWLEDGE
```

---

Mỗi GPT chỉ có một mã chính thức.

---

Không đổi mã giữa chừng.

---

# 12. QUY TẮC PATCH

Chuẩn:

```text
UPDATE_<MUC>
```

---

Ví dụ:

```text
UPDATE_03A

UPDATE_03B

UPDATE_04_1

UPDATE_04_ARCHIVE
```

---

Không dùng:

```text
UPDATE_FILE

FIX_FILE

SAVE_FILE
```

---

# 13. QUY TẮC COMMIT

Ví dụ:

```text
TEST_CREATE_FILE

UPDATE_WM

UPDATE_LM

UPDATE_RULE

UPDATE_KN
```

---

Commit phải phản ánh mục đích.

---

# 14. QUY TẮC TÊN KÊNH NỘI DUNG

Tên hiển thị:

Được phép có dấu.

Ví dụ:

```text
Bồ Đề Việt

Đợi Bồ Đề

Nghề Lá Của Đợi

Nhà Có Maybach

Không Phải Maybach Đâu

Đợi Làm Bố
```

---

Mã nội bộ:

```text
BDV

DBD

NLCD

MAYBACH

KPMBD

DLB
```

---

# 15. QUY TẮC TÊN ASSET

Chuẩn:

```text
YYYY-MM-DD_NHOM_TUKHOA1_TUKHOA2_TUKHOA3
```

---

Ví dụ:

```text
2026-06-20_BDV_HaiLa_GhepLa_DongGoi.mp4

2026-06-20_DLB_GheTreEm_KhongHopTac.mp4

2026-06-20_KPMBD_KhongPhaiMaybachDau.mp4
```

---

Không dùng ID riêng cho asset ở V1.

---

# 16. QUY TẮC MEMORY_INDEX

Memory Index là nguồn ánh xạ chính thức.

Ví dụ:

```text
WM_03A_CONTENT

↓

memory/WM_03A_CONTENT - BO NHO LOI GPT CONTENT OS.md
```

---

GPT không được tự suy đoán path.

GPT phải ưu tiên đọc MEMORY_INDEX.

---

# 17. QUY TẮC CUỐI CÙNG

Nếu có xung đột giữa:

Tên đẹp

và

Tên nhất quán

Ưu tiên:

Tên nhất quán.

Vì hệ thống sẽ tồn tại lâu hơn cảm xúc đặt tên tại một thời điểm.
