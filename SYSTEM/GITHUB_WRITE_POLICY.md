# GITHUB_WRITE_POLICY

Phiên bản: 03.000

---

# MỤC TIÊU

GitHub là nguồn chân lý của hệ thống.

Không sử dụng memory hội thoại làm nguồn chân lý.

Không sử dụng Knowledge Upload làm nguồn chân lý.

Mọi thay đổi memory phải đi qua GitHub.

---

# NGUYÊN TẮC

Ưu tiên:

```text id="k9cc5j"
GitHub
↓
Memory
↓
GPT
```

Không ưu tiên:

```text id="6qblvp"
GPT
↓
Memory
↓
GitHub
```

---

# QUY TẮC ĐỌC

Khi đọc file đã tồn tại:

GPT phải đọc từ GitHub.

Không được tự suy luận nội dung file.

Không được giả định nội dung file.

---

# QUY TẮC GHI

Nếu file đã tồn tại:

Bắt buộc:

```text id="quc2ii"
Bước 1
Đọc file

↓

Bước 2
Lấy SHA

↓

Bước 3
Tạo PATCH

↓

Bước 4
Chờ xác nhận

↓

Bước 5
Ghi GitHub
```

---

Nếu file chưa tồn tại:

```text id="h8wlgp"
Bước 1
Tạo PATCH

↓

Bước 2
Chờ xác nhận

↓

Bước 3
Tạo file mới
```

---

# QUY TẮC MEMORY

Không ghi trực tiếp từ hội thoại vào memory.

Mọi cập nhật phải đi qua:

```text id="h6v7zl"
PATCH
↓
Xác nhận
↓
GitHub
```

---

# QUY TẮC WORKING MEMORY

## WM_04_1_DAILY

Cho phép:

* Ghi đè
* Thay thế toàn bộ nội dung

Mục đích:

Lưu việc đang dở trong ngày.

Không lưu lịch sử.

---

## WM_04_1_LONG

Cho phép:

* Thêm
* Sửa
* Xóa

Mục đích:

Lưu việc đang dở dài hạn.

---

# QUY TẮC LONG TERM MEMORY

## LM_03B_CURRENT

Chỉ lưu:

* Tri thức đã kiểm chứng
* Quy trình đã xác nhận
* Kiến trúc đã xác nhận

Không lưu:

* Ý tưởng
* Giả thuyết
* Suy đoán

---

## LM_03B_ARCHIVE

Chỉ dùng để lưu trữ.

Không nạp mặc định đầu phiên.

---

## LM_04_CURRENT

Lưu:

* Nhật ký học tập gần đây
* Kết quả kiểm chứng
* Bài học vận hành

---

## LM_04_ARCHIVE

Lưu:

* Lịch sử cũ
* Nhật ký cũ

Không nạp mặc định đầu phiên.

---

# QUY TẮC TỔNG HỢP

Khi CURRENT quá lớn:

GPT phải đề xuất:

```text id="k9rrrk"
Tổng hợp
↓
Rút gọn
↓
Chuyển archive
```

Không được để CURRENT tăng trưởng vô hạn.

---

# QUY TẮC ARCHIVE

## LM_03B_ARCHIVE

Đánh số:

```text id="h48bkr"
LM_03B_ARCHIVE_001.md

LM_03B_ARCHIVE_002.md

LM_03B_ARCHIVE_003.md
```

Nguyên tắc:

Ưu tiên chia theo chủ đề.

Không ưu tiên chia theo thời gian.

---

## LM_04_ARCHIVE

Đặt tên:

```text id="46mlr6"
LM_04_ARCHIVE_YYYY_MM.md
```

Ví dụ:

```text id="4k6sl1"
LM_04_ARCHIVE_2026_06.md

LM_04_ARCHIVE_2026_07.md

LM_04_ARCHIVE_2026_08.md
```

Nguyên tắc:

Chia theo thời gian.

---

# QUY TẮC HOÀN TẤT

Sau khi GitHub ghi thành công:

PATCH được xem là hoàn tất.

Không lưu PATCH.

Không tạo lịch sử PATCH.

Không tạo thư mục PATCH.

GitHub Repository là nguồn chân lý duy nhất.
