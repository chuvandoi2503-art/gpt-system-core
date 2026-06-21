# GITHUB_ACTION_SETUP

Phiên bản: 01.000

Trạng thái: Áp dụng toàn hệ

---

# 1. MỤC ĐÍCH

File này hướng dẫn kết nối GPT với GitHub Repository.

Mục tiêu:

* Đọc Memory.
* Đọc Knowledge.
* Đọc Rule.
* Ghi Memory.
* Ghi Knowledge.
* Ghi Rule.

Thông qua GitHub API.

---

# 2. TRIẾT LÝ

GitHub là nguồn chân lý.

GPT không lưu bộ nhớ dài hạn.

GPT chỉ:

* Đọc.
* Suy luận.
* Đề xuất.
* Cập nhật.

Dữ liệu phải nằm trên GitHub.

---

# 3. KIẾN TRÚC CHUẨN

```
GPT
↓
GitHub Action
↓
GitHub Repository
```

---

Ví dụ:

```
GPT Content OS
↓
GitHub Action
↓
gpt-content-director-system
```

---

Ví dụ:

```
GPT Kiến Trúc Sư
↓
GitHub Action
↓
gpt-architect-system
```

---

# 4. GITHUB TOKEN

Khuyến nghị:

1 token dùng chung toàn hệ.

---

Ví dụ:

Token có quyền:

```
gpt-system-core

gpt-architect-system

gpt-content-director-system
```

---

Mục tiêu:

Đơn giản hóa vận hành.

---

# 5. QUYỀN TOKEN

Bắt buộc:

```
Contents
=
Read & Write
```

---

Bắt buộc:

```
Metadata
=
Read
```

---

Không cần:

```
Administration

Actions

Secrets

Codespaces
```

---

# 6. REPOSITORY ACCESS

Khuyến nghị:

Selected repositories

---

Ví dụ:

```
gpt-system-core

gpt-architect-system

gpt-content-director-system
```

---

Không cần:

All repositories

---

# 7. ACTION CHUẨN

Action chuẩn toàn hệ:

```
getContent
```

---

Mục đích:

Đọc file.

---

Action chuẩn:

```
createOrUpdateFile
```

---

Mục đích:

Tạo file.

Cập nhật file.

---

# 8. GETCONTENT

Input:

```
owner

repo

path
```

---

Ví dụ:

```
owner:
chuvandoi2503-art

repo:
gpt-content-director-system

path:
SYSTEM/MEMORY_INDEX.md
```

---

Output:

Nội dung file.

SHA.

Metadata.

---

# 9. CREATEORUPDATEFILE

Input:

```
owner

repo

path

content

message
```

---

Nếu cập nhật file cũ:

Bắt buộc thêm:

```
sha
```

---

# 10. QUY TRÌNH ĐỌC FILE

```
Người dùng yêu cầu
↓
Đọc MEMORY_INDEX
↓
Xác định path
↓
Đọc file cần thiết
↓
Suy luận
```

---

# 11. QUY TRÌNH SỬA FILE

```
Đọc file
↓
Lấy SHA
↓
Tạo PATCH
↓
Người dùng duyệt
↓
Ghi GitHub
```

---

Không được bỏ qua bước PATCH.

---

# 12. QUY TRÌNH TẠO FILE

```
Tạo nội dung
↓
Hiển thị cho người dùng
↓
Người dùng duyệt
↓
Tạo file mới
```

---

Không cần SHA.

---

# 13. QUY TRÌNH KHỞI TẠO GPT MỚI

Bước 1

Tạo Repository.

---

Bước 2

Kết nối GitHub Action.

---

Bước 3

Import OpenAPI Schema.

---

Bước 4

Tạo:

```
MEMORY_INDEX
```

---

Bước 5

Tạo:

```
Knowledge

Rule

Memory
```

---

Bước 6

Kiểm tra đọc ghi.

---

PASS.

---

# 14. KIỂM TRA KẾT NỐI

Test đọc:

```
SYSTEM/MEMORY_INDEX.md
```

---

Nếu đọc được:

PASS.

---

Test ghi:

```
TEST_CREATE_FILE
```

---

Nếu ghi được:

PASS.

---

# 15. XỬ LÝ LỖI THƯỜNG GẶP

Lỗi:

```
403
```

---

Nguyên nhân:

Token không có quyền.

---

Kiểm tra:

```
Contents

Read & Write
```

---

Lỗi:

```
Repository not found
```

---

Nguyên nhân:

Sai repo.

Sai quyền.

---

Lỗi:

```
Resource not accessible
```

---

Nguyên nhân:

Token chưa được cấp quyền repo.

---

# 16. NGUYÊN TẮC BẢO TRÌ

Schema dùng chung.

Action dùng chung.

Token dùng chung.

Repository tách riêng.

---

Mục tiêu:

Giảm chi phí bảo trì.

---

# 17. QUY TẮC CUỐI CÙNG

Nếu phải lựa chọn giữa:

Tự động hóa nhiều hơn

hoặc

Đơn giản hơn

Ưu tiên:

Đơn giản hơn.

Chỉ tự động hóa khi tạo ra giá trị thực tế.
