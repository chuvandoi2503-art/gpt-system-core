# OPENAPI_SCHEMA

Phiên bản: 01.000

Trạng thái: Áp dụng toàn hệ

---

# 1. MỤC ĐÍCH

File này quản lý chuẩn OpenAPI Schema dùng chung cho toàn bộ hệ GPT.

Mục tiêu:

* Một schema dùng cho nhiều GPT.
* Giảm bảo trì.
* Giảm trùng lặp.
* Dễ nhân bản GPT mới.

---

# 2. TRIẾT LÝ

Schema là hạ tầng.

Schema không thuộc GPT nào.

Schema thuộc:

```text
GPT SYSTEM CORE
```

---

GPT chuyên ngành chỉ sử dụng.

Không sở hữu schema.

---

# 3. KIẾN TRÚC

```text
GPT
↓
OpenAPI Schema
↓
GitHub Action
↓
GitHub Repository
```

---

Ví dụ:

```text
GPT Kiến Trúc Sư
↓
Schema chung
↓
GitHub
```

---

Ví dụ:

```text
GPT Content OS
↓
Schema chung
↓
GitHub
```

---

# 4. NGUYÊN TẮC

Một schema.

Nhiều GPT.

Nhiều repository.

---

Không tạo schema riêng cho từng GPT nếu không thật sự cần.

---

# 5. NHỮNG GÌ ĐƯỢC PHÉP THAY ĐỔI

Được phép thay đổi:

* Endpoint.
* Authentication.
* Response format.
* Request format.

---

Nếu thay đổi:

Phải cập nhật toàn hệ.

---

# 6. NHỮNG GÌ KHÔNG NÊN THAY ĐỔI

Không sửa schema vì:

* Một GPT mới.
* Một workflow mới.
* Một use case nhỏ.

---

Schema phải ổn định.

---

# 7. AUTHENTICATION

Chuẩn hiện tại:

```text
Bearer Token
```

---

Token có thể dùng chung toàn hệ.

---

# 8. REPOSITORY

Schema không khóa vào repository cụ thể.

Repository truyền vào lúc gọi API.

---

Ví dụ:

```text
owner

repo

path
```

---

không hardcode.

---

# 9. ACTION CHUẨN

Bắt buộc:

```text
getContent
```

---

Mục đích:

Đọc file.

---

Bắt buộc:

```text
createOrUpdateFile
```

---

Mục đích:

Tạo file.

Cập nhật file.

---

# 10. TƯƠNG THÍCH GPT MỚI

Một GPT mới phải có khả năng:

* Dùng lại schema.
* Dùng lại token.
* Dùng lại action.

---

Không cần tạo schema mới.

---

# 11. QUY TRÌNH CẬP NHẬT

Schema thay đổi

↓

Test

↓

Cập nhật SYSTEM CORE

↓

Cập nhật GPT Builder Backup

↓

Thông báo toàn hệ

---

# 12. QUẢN LÝ PHIÊN BẢN

Ví dụ:

```text
01.000
01.001
01.002
02.000
```

---

Quy tắc:

```text
Sửa nhỏ
=
+0.001

Sửa lớn
=
+1.000
```

---

# 13. KIỂM TRA TƯƠNG THÍCH

Sau khi đổi schema:

Kiểm tra:

* GPT Kiến Trúc Sư
* GPT Content OS
* GPT CRM
* GPT Sales
* GPT Automation

---

PASS toàn bộ mới triển khai.

---

# 14. BACKUP

Schema gốc phải được lưu:

* GPT System Core
* PC cá nhân

---

Không phụ thuộc vào GPT Builder.

---

# 15. MỤC TIÊU DÀI HẠN

Tạo GPT mới trong:

```text
5 phút
```

---

Quy trình:

```text
Tạo GPT

↓

Paste Builder Backup

↓

Import Schema

↓

Kết nối GitHub

↓

PASS
```

---

# 16. QUAN HỆ VỚI GPT_BUILDER_BACKUP

GPT_BUILDER_BACKUP

không chứa schema đầy đủ.

---

Chỉ chứa:

Thông tin vị trí schema.

---

Nguồn chuẩn:

```text
SYSTEM/OPENAPI_SCHEMA.md
```

---

# 17. QUY TẮC CUỐI CÙNG

Nếu phải lựa chọn giữa:

```text
1 schema dùng chung
```

và

```text
N schema riêng lẻ
```

Ưu tiên:

```text
1 schema dùng chung
```

trừ khi có bằng chứng rõ ràng rằng việc tách schema tạo ra giá trị lớn hơn chi phí bảo trì.
