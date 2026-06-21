# PATCH_STANDARD

Phiên bản: 03.000

---

# MỤC TIÊU

PATCH là cơ chế trung gian giữa:

```
Hội thoại
↓
Memory
```

PATCH giúp:

* Kiểm tra trước khi ghi
* Giảm ghi nhầm
* Giảm mất dữ liệu
* Giữ người dùng là người quyết định cuối cùng

---

# NGUYÊN TẮC

PATCH không phải bộ nhớ.

PATCH không được lưu tồn đọng.

PATCH chỉ tồn tại trong phiên hiện tại.

Sau khi được duyệt:

```
PATCH
↓
Ghi vào file đích
↓
Kết thúc
```

Không tạo backlog PATCH.

Không tạo thư mục PATCH.

Không lưu PATCH để tổng hợp sau.

---

# QUY TRÌNH KẾT THÚC PHIÊN

Người dùng nói:

```
Kết thúc phiên
```

GPT phải:

```
Rà soát phiên
↓
Tạo PATCH
↓
Chờ duyệt
↓
Ghi GitHub
↓
Hoàn tất
```

---

# PHÂN LOẠI PATCH

## UPDATE_WM_03A

Sử dụng khi:

* Vai trò GPT thay đổi
* Quy trình thay đổi
* Nguyên tắc thay đổi
* Cấu hình hệ thống thay đổi

---

## UPDATE_WM_04_1_DAILY

Sử dụng khi:

* Việc đang dở trong ngày thay đổi

Ghi vào:

```
WM_04_1_DAILY.md
```

File này được phép ghi đè.

---

## UPDATE_WM_04_1_LONG

Sử dụng khi:

* Xuất hiện việc dài hạn mới
* Tiến độ việc dài hạn thay đổi
* Hoàn thành việc dài hạn

Ghi vào:

```
WM_04_1_LONG.md
```

---

## UPDATE_LM_03B_CURRENT

Sử dụng khi:

Xuất hiện tri thức mới đã được kiểm chứng.

Ví dụ:

* Quy tắc mới
* Kiến trúc mới
* Workflow mới
* Bài học đã xác nhận

Không lưu:

* Giả thuyết
* Suy đoán
* Ý tưởng chưa kiểm chứng

---

## UPDATE_LM_04_CURRENT

Sử dụng khi:

Cần lưu lịch sử học tập.

Ví dụ:

* Bài học triển khai
* Lỗi gặp phải
* Kết quả kiểm chứng

---

## DISCARD

Thông tin không lưu.

Ví dụ:

* Trao đổi tạm thời
* Ý tưởng bị loại
* Thảo luận không còn giá trị

---

# QUY TẮC GHI GITHUB

Nếu file đã tồn tại:

GPT phải:

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

Nếu file chưa tồn tại:

GPT phải:

```
Tạo PATCH
↓
Chờ xác nhận
↓
Tạo file mới
```

---

# QUY TẮC TỔNG HỢP MEMORY

Không tổng hợp từ PATCH.

PATCH không phải nguồn chân lý.

Nguồn chân lý là:

```
GitHub Repository
```

Khi cần tổng hợp:

GPT đọc trực tiếp:

```
WM_03A
WM_04_1
LM_03B
LM_04
```

từ GitHub.

---

# QUY TẮC HOÀN TẤT

Sau khi PATCH được ghi vào file đích:

PATCH được xem là hoàn thành.

Không tiếp tục lưu PATCH ở nơi khác.

Không tạo lịch sử PATCH.

Không tạo archive PATCH.
