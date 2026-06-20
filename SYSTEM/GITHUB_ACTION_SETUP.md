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

```text id="p8gq7k"
GPT
↓
GitHub Action
↓
GitHub Repository
```

---

Ví dụ:

```text id="wtkn2f"
GPT Content OS
↓
GitHub Action
↓
gpt-content-director-system
```

---

Ví dụ:

```text id="1lg4w7"
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

```text id="e7zxtg"
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

```text id="09l12n"
Contents
=
Read & Write
```

---

Bắt buộc:

```text id="q6v6ei"
Metadata
=
Read
```

---

Không cần:

```text id="qmb4gg"
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

```text id="cl4o74"
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

```text id="87k0x5"
getContent
```

---

Mục đích:

Đọc file.

---

Action chuẩn:

```text id="4yzfho"
createOrUpdateFile
```

---

Mục đích:

Tạo file.

Cập nhật file.

---

# 8. GETCONTENT

Input:

```text id="w9vwju"
owner

repo

path
```

---

Ví dụ:

```text id="jlwm8e"
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

```text id="kn3x0t"
owner

repo

path

content

message
```

---

Nếu cập nhật file cũ:

Bắt buộc thêm:

```text id="isjlwm"
sha
```

---

# 10. QUY TRÌNH ĐỌC FILE

```text id="04fkkh"
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

```text id="8k7h9m"
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

```text id="b7zz15"
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

```text id="0zbrcu"
MEMORY_INDEX
```

---

Bước 5

Tạo:

```text id="3ykgw3"
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

```text id="80kk8o"
SYSTEM/MEMORY_INDEX.md
```

---

Nếu đọc được:

PASS.

---

Test ghi:

```text id="vgpq1h"
TEST_CREATE_FILE
```

---

Nếu ghi được:

PASS.

---

# 15. XỬ LÝ LỖI THƯỜNG GẶP

Lỗi:

```text id="lcf7xe"
403
```

---

Nguyên nhân:

Token không có quyền.

---

Kiểm tra:

```text id="c7nnrz"
Contents

Read & Write
```

---

Lỗi:

```text id="k3e0km"
Repository not found
```

---

Nguyên nhân:

Sai repo.

Sai quyền.

---

Lỗi:

```text id="t9vuzm"
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
