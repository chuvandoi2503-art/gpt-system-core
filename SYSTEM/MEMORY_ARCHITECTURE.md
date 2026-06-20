# MEMORY_ARCHITECTURE

Phiên bản: 01.000

Trạng thái: Áp dụng toàn hệ

---

# 1. MỤC ĐÍCH

File này mô tả kiến trúc bộ nhớ chuẩn dùng cho toàn bộ hệ GPT.

Mục tiêu:

* Dễ hiểu.
* Dễ nhân bản.
* Dễ bảo trì.
* Dễ mở rộng.
* Không phình bộ nhớ.

---

# 2. TRIẾT LÝ THIẾT KẾ

Không phải mọi thứ đều cần ghi nhớ.

Không phải mọi thứ đều cần lưu trữ.

Chỉ lưu những gì tạo giá trị trong tương lai.

Nguyên tắc:

```text
Tri thức quan trọng
↓
Lưu

Thông tin tạm thời
↓
Loại bỏ
```

---

# 3. CẤU TRÚC CHUẨN

Mỗi GPT chuyên ngành sử dụng:

```text
KN
RULE
WM
LM
```

---

# 4. KNOWLEDGE (KN)

Mục đích:

Tri thức nền.

Thông tin ít thay đổi.

Ví dụ:

* Định nghĩa GPT.
* Triết lý hệ thống.
* Hồ sơ lĩnh vực chuyên môn.

---

Cấu trúc:

```text
KN_00
KN_01
KN_02_<GPT>
```

---

Ví dụ:

```text
KN_02_ARCH
KN_02_CONTENT
KN_02_CRM
```

---

# 5. RULE

Mục đích:

Luật vận hành.

Quy tắc ra quyết định.

Nguyên tắc ứng xử.

---

Cấu trúc:

```text
RULE_COMMON
RULE_<GPT>
```

---

Ví dụ:

```text
RULE_COMMON

RULE_ARCH

RULE_CONTENT
```

---

# 6. WORKING MEMORY (WM)

Mục đích:

Lưu trạng thái hiện tại.

Việc đang làm.

Thông tin cần nạp đầu phiên.

---

WM không phải lịch sử.

WM không phải archive.

---

Cấu trúc:

```text
WM_03A_<GPT>

WM_04_1_<GPT>
```

---

# 7. WM_03A

Vai trò:

Bộ nhớ lõi.

Danh tính GPT.

Mục tiêu GPT.

Module GPT.

Nguyên tắc GPT.

---

Tần suất thay đổi:

Rất thấp.

---

Ví dụ:

```text
WM_03A_ARCH

WM_03A_CONTENT
```

---

# 8. WM_04_1

Vai trò:

Việc đang làm.

Ý tưởng đang triển khai.

Backlog.

Trạng thái công việc.

---

Tần suất thay đổi:

Cao.

---

Đây là file được cập nhật nhiều nhất.

---

# 9. LONG-TERM MEMORY (LM)

Mục đích:

Tri thức học được.

Bài học đã xác nhận.

Lịch sử phát triển.

---

Cấu trúc:

```text
LM_03B_<GPT>

LM_04_<GPT>
```

---

# 10. LM_03B

Vai trò:

Tri thức đã xác nhận.

Không lưu giả thuyết.

Không lưu ý tưởng chưa kiểm chứng.

---

Ví dụ:

* Bài học đã xác nhận.
* Format đã thắng.
* Quy trình đã xác nhận hiệu quả.

---

# 11. LM_04

Vai trò:

Nhật ký học tập.

Archive.

Lịch sử.

---

Có thể dài.

Không cần nạp đầu phiên.

---

# 12. MEMORY INDEX

Mỗi repository phải có:

```text
SYSTEM/MEMORY_INDEX.md
```

---

Vai trò:

Bản đồ hệ thống.

GPT đọc MEMORY_INDEX trước.

Sau đó mới tìm file khác.

---

# 13. QUY TẮC NẠP ĐẦU PHIÊN

Mặc định nạp:

```text
RULE_COMMON

RULE_<GPT>

WM_03A_<GPT>

WM_04_1_<GPT>
```

---

Không nạp mặc định:

```text
LM_03B_<GPT>

LM_04_<GPT>
```

---

Chỉ đọc khi cần.

---

# 14. LUỒNG HỌC TẬP

Công việc

↓

Kết quả

↓

Bài học

↓

LM_04

↓

Xác nhận

↓

LM_03B

---

# 15. LUỒNG KẾT THÚC PHIÊN

Kết thúc phiên

↓

Rà soát

↓

PATCH

↓

Người dùng duyệt

↓

Ghi GitHub

---

# 16. KHÔNG LƯU

Không lưu trong Memory:

* Video.
* Asset.
* Ảnh.
* File lớn.
* Dữ liệu thô.

Các dữ liệu này phải nằm ngoài GPT.

---

# 17. MỤC TIÊU CUỐI

Bất kỳ GPT nào trong hệ sinh thái đều phải:

* Có thể khôi phục.
* Có thể nhân bản.
* Có thể chuyển tài khoản.
* Có thể học tập.
* Có thể bảo trì.

Chỉ bằng:

```text
GitHub Repository
+
Memory Architecture
+
GPT Builder Backup
```
