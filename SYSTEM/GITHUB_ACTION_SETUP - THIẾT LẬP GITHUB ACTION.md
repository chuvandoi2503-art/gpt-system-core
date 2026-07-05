# GITHUB_ACTION_SETUP

Phiên bản: 03.001

---

# MỤC TIÊU

Thiết lập kết nối GitHub chuẩn cho toàn bộ hệ GPT.

GitHub là nguồn chân lý.

GPT đọc và ghi memory thông qua GitHub Action.

Không phụ thuộc vào Knowledge Upload.

---

# ACTION CHUẨN

Hệ thống sử dụng:

- getContent
- createOrUpdateFile

---

# YÊU CẦU TỐI THIỂU

Action phải hỗ trợ:

## Đọc file

```
getContent(
 owner,
 repo,
 path
)
```

Trả về:

```
content
sha
```

---

## Ghi file

```
createOrUpdateFile(
 owner,
 repo,
 path,
 content,
 sha,
 branch
)
```

---

# REPOSITORY CORE

Repository chuẩn:

```
gpt-system-core
```

Vai trò:

- RULE_COMMON
- MEMORY_ARCHITECTURE
- MEMORY_INDEX
- PATCH_STANDARD
- NAMING_CONVENTION
- GITHUB_WRITE_POLICY
- RESTORE_GUIDE
- GITHUB_ACTION_SETUP

---

# REPOSITORY GPT

Mỗi GPT có repository riêng.

Ví dụ:

- gpt-architect-system
- gpt-content-director-system
- gpt-crm-system
- gpt-sales-system

Repository GPT chứa:

- RULE_<GPT>
- WM_03A
- WM_04_1
- LM_03B
- LM_04
- KN_02

---

# QUY TẮC KHỞI TẠO PHIÊN

GPT phải đọc:

## Core Repository

```
SYSTEM/MEMORY_INDEX.md
```

Từ đó xác định:

- RULE_COMMON
- MEMORY_ARCHITECTURE

---

## Runtime Repository

Đọc theo quy trình riêng của GPT.

Ví dụ GPT Content:

- RULE_CONTENT
- WM_03A_CONTENT
- WM_04_1_CONTENT_DAILY
- LM_03B_CONTENT_CURRENT

---

# AUTHENTICATION

Khuyến nghị:

GitHub Fine-Grained Personal Access Token

---

Quyền tối thiểu:

```
Contents
Read and Write
```

```
Metadata
Read
```

---

# KIỂM TRA ACTION

## Test đọc

Đọc:

```
SYSTEM/MEMORY_INDEX.md
```

PASS khi:

- Đọc được file
- Nhận được SHA
- Nhận được content

---

## Test ghi

Tạo:

```
TEST_CREATE_FILE.md
```

PASS khi:

- File được tạo
- GitHub trả kết quả thành công

---

## Test cập nhật

Đọc file

↓

Lấy SHA

↓

Cập nhật nội dung

↓

Ghi lại file

PASS khi:

- SHA mới được tạo
- Nội dung được cập nhật

---

# QUY TẮC GHI MEMORY

GPT không được ghi memory nếu:

- Chưa đọc file
- Chưa lấy SHA
- Chưa có PATCH
- Chưa có xác nhận người dùng

---

# QUY TẮC GHI FILE ĐÃ TỒN TẠI

Bắt buộc:

```
Đọc file
↓
Lấy SHA
↓
Tạo PATCH
↓
Chờ xác nhận
↓
Ghi GitHub
```

---

# QUY TẮC TẠO FILE MỚI

Bắt buộc:

```
Tạo PATCH
↓
Chờ xác nhận
↓
Tạo file mới
```

Không được tự tạo file memory khi chưa có xác nhận.

---

# QUY TẮC KHỞI TẠO GPT MỚI

Trước khi vận hành memory thật:

Bắt buộc PASS:

- getContent
- createOrUpdateFile

---

# QUY TẮC DỰ PHÒNG

Nếu GitHub Action lỗi:

GPT được phép sử dụng Knowledge Upload tạm thời.

Nhưng phải thông báo rõ:

```
GitHub không khả dụng.
Đang sử dụng dữ liệu dự phòng.
```

Knowledge Upload không được xem là nguồn chân lý.

---

# QUY TẮC XUẤT FILE .MD

Khi người dùng yêu cầu:

```
1 trả lời = 1 file .md
```

GPT phải xuất Markdown thuần.

Không sử dụng:

- :::writing
- text id=
- UI block của ChatGPT
- Metadata nội bộ của ChatGPT

Nội dung phải có thể:

```
Copy
↓
Paste vào GitHub
↓
Commit ngay
```

không cần dọn dẹp lại.

---

# TRẠNG THÁI PASS

Hệ GitHub Action được xem là PASS khi:

- Đọc được Core Repository
- Đọc được Runtime Repository
- Tạo file mới thành công
- Cập nhật file thành công
- Trả về SHA chính xác
- GPT có thể khởi tạo phiên hoàn toàn từ GitHub
