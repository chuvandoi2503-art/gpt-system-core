# MEMORY_ARCHITECTURE

Phiên bản: 03.000

---

# MỤC TIÊU

Hệ thống bộ nhớ phải:

* Đơn giản
* Dễ nhân bản
* Dễ bảo trì
* Dễ mở rộng
* Không phình vô hạn
* Không tồn đọng patch
* Có thể vận hành nhiều năm

---

# NGUYÊN TẮC

GitHub là nguồn chân lý.

Memory phải phục vụ vận hành.

Không sử dụng một file memory tăng trưởng vô hạn.

Ưu tiên nhiều file nhỏ theo vai trò.

Ưu tiên giảm dữ liệu phải nạp đầu phiên.

---

# CẤU TRÚC MEMORY CHUẨN

## WM_03A

Bộ nhớ lõi GPT.

Lưu:

* Vai trò
* Mục tiêu
* Quy trình vận hành
* Cấu hình hệ thống

Nạp đầu phiên.

---

## WM_04_1

Không sử dụng một file duy nhất.

Sử dụng thư mục:

```
WM_04_1/
```

Bao gồm:

```
WM_04_1_DAILY.md

WM_04_1_LONG.md
```

---

### WM_04_1_DAILY

Mục đích:

Việc đang dở trong ngày hoặc phiên gần nhất.

Quy tắc:

* Nạp đầu phiên.
* Được ghi đè.
* Không archive.
* Không lưu lịch sử dài hạn.

Nếu việc kéo dài nhiều ngày:

Chuyển sang:

```
WM_04_1_LONG.md
```

---

### WM_04_1_LONG

Mục đích:

Việc đang dở dài hạn.

Ví dụ:

* Dự án
* Backlog
* Công việc theo tuần
* Công việc theo tháng
* Công việc theo quý

Quy tắc:

* Không nạp mặc định đầu phiên.
* Chỉ đọc khi cần.
* Khi hoàn thành:

Chuyển sang:

```
LM_04_CURRENT.md
```

hoặc

```
LM_03B_CURRENT.md
```

---

# LONG TERM MEMORY

## LM_03B

Tri thức đã kiểm chứng.

Sử dụng thư mục:

```
LM_03B/
```

---

Bao gồm:

```
LM_03B_CURRENT.md

LM_03B_ARCHIVE_001.md

LM_03B_ARCHIVE_002.md

...
```

---

### LM_03B_CURRENT

Mục đích:

Tri thức mới được xác nhận.

Quy tắc:

* Có thể nạp đầu phiên.
* Chỉ giữ tri thức còn hữu ích trong vận hành gần đây.

Khi:

* Trên 300 dòng

hoặc

* Trên 50 mục tri thức

thì phải tổng hợp.

Tri thức ổn định chuyển sang:

```
LM_03B_ARCHIVE_xxx.md
```

---

### LM_03B_ARCHIVE_xxx

Mục đích:

Lưu tri thức đã ổn định.

Không nạp đầu phiên.

Chỉ đọc khi cần tra cứu.

Quy tắc tạo archive mới:

Không tạo archive mới theo thời gian.

Ưu tiên nhóm theo chủ đề.

Ví dụ:

```
LM_03B_ARCHIVE_001.md
=
Kiến trúc GPT

LM_03B_ARCHIVE_002.md
=
GitHub Memory

LM_03B_ARCHIVE_003.md
=
Content System
```

Chỉ tạo archive mới khi:

* Archive hiện tại vượt khoảng 1000 dòng

hoặc

* Xuất hiện nhóm tri thức mới đủ lớn.

---

## LM_04

Nhật ký học tập.

Sử dụng thư mục:

```
LM_04/
```

---

Bao gồm:

```
LM_04_CURRENT.md

LM_04_ARCHIVE_YYYY_MM.md
```

---

### LM_04_CURRENT

Mục đích:

Lưu lịch sử học tập gần đây.

Quy tắc:

* Không bắt buộc nạp đầu phiên.
* Chỉ đọc khi cần tra cứu.

Khi:

* Quá lớn

hoặc

* Hết tháng

thì chuyển sang archive.

---

### LM_04_ARCHIVE_YYYY_MM

Ví dụ:

```
LM_04_ARCHIVE_2026_06.md

LM_04_ARCHIVE_2026_07.md

LM_04_ARCHIVE_2026_08.md
```

Mục đích:

Lưu lịch sử cũ.

Không nạp đầu phiên.

Chỉ đọc khi cần tra cứu.

---

# KHỞI TẠO PHIÊN CHUẨN

Mặc định chỉ nạp:

```
RULE_COMMON

RULE_<GPT>

WM_03A_<GPT>

WM_04_1_DAILY

LM_03B_CURRENT
```

Không nạp mặc định:

```
WM_04_1_LONG

LM_03B_ARCHIVE

LM_04_CURRENT

LM_04_ARCHIVE
```

Chỉ đọc khi cần.

---

# KẾT THÚC PHIÊN CHUẨN

PATCH phải được phân loại:

```
UPDATE_WM_03A

UPDATE_WM_04_1_DAILY

UPDATE_WM_04_1_LONG

UPDATE_LM_03B_CURRENT

UPDATE_LM_04_CURRENT

DISCARD
```

Sau khi người dùng xác nhận:

Ghi trực tiếp vào file đích.

Không lưu patch tồn đọng.
