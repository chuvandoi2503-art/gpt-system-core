# PATCH_STANDARD

Phiên bản: 03.001

---

# MỤC TIÊU

PATCH là cơ chế trung gian giữa:

Hội thoại

↓

Memory

↓

GitHub

PATCH giúp:

- Kiểm tra trước khi ghi
- Giảm ghi nhầm
- Giảm mất dữ liệu
- Giữ người dùng là người quyết định cuối cùng

---

# NGUYÊN TẮC

PATCH không phải bộ nhớ.

PATCH không phải nguồn chân lý.

PATCH không được lưu tồn đọng.

PATCH chỉ tồn tại trong phiên hiện tại.

Sau khi được xác nhận:

PATCH

↓

Ghi GitHub

↓

Hoàn tất

Không tạo thư mục PATCH.

Không tạo lịch sử PATCH.

Không tạo PATCH Archive.

---

# QUY TRÌNH KẾT THÚC PHIÊN

Khi người dùng yêu cầu:

Kết thúc phiên

GPT phải:

Rà soát phiên

↓

Tạo PATCH

↓

Phân loại PATCH

↓

Chờ xác nhận

↓

Ghi GitHub

↓

Hoàn tất

---

# PHÂN LOẠI PATCH

## UPDATE_WM_03A

Sử dụng khi:

- Vai trò GPT thay đổi
- Mục tiêu thay đổi
- Quy trình thay đổi
- Kiến trúc thay đổi
- Cấu hình hệ thống thay đổi

Ghi vào:

WM_03A

---

## UPDATE_WM_04_1_DAILY

Sử dụng khi:

- Việc đang dở hôm nay thay đổi

Ghi vào:

memory/WM_04_1/

WM_04_1_<GPT>_DAILY

---

## UPDATE_WM_04_1_LONG

Sử dụng khi:

- Xuất hiện dự án mới
- Xuất hiện backlog mới
- Tiến độ dự án thay đổi
- Công việc dài hạn thay đổi
- Công việc dài hạn hoàn thành

Ghi vào:

memory/WM_04_1/

WM_04_1_<GPT>_LONG

---

## UPDATE_LM_03B_CURRENT

Sử dụng khi:

Xuất hiện tri thức đã kiểm chứng.

Ví dụ:

- Kiến trúc mới
- Quy trình mới
- Workflow mới
- Bài học đã xác nhận

Không lưu:

- Ý tưởng
- Giả thuyết
- Suy đoán

Ghi vào:

memory/LM_03B/

LM_03B_<GPT>_CURRENT

---

## UPDATE_LM_04_CURRENT

Sử dụng khi:

Cần lưu lịch sử học tập.

Ví dụ:

- Kết quả kiểm chứng
- Lỗi phát hiện
- Bài học vận hành
- Kinh nghiệm triển khai

Ghi vào:

memory/LM_04/

LM_04_<GPT>_CURRENT

---

## DISCARD

Thông tin không lưu.

Ví dụ:

- Trao đổi tạm thời
- Ý tưởng bị loại
- Thảo luận không còn giá trị
- Nội dung không cần cho vận hành tương lai

---

# QUY TẮC GHI FILE ĐÃ TỒN TẠI

Bắt buộc:

Đọc file

↓

Lấy SHA

↓

Tạo PATCH

↓

Chờ xác nhận

↓

Ghi GitHub

---

# QUY TẮC TẠO FILE MỚI

Bắt buộc:

Tạo PATCH

↓

Chờ xác nhận

↓

Tạo file mới

Không được tự tạo file memory khi chưa có xác nhận.

---

# QUY TẮC TỔNG HỢP MEMORY

Không tổng hợp từ PATCH.

PATCH không phải nguồn chân lý.

Nguồn chân lý là:

GitHub Repository

Khi cần tổng hợp:

GPT phải đọc trực tiếp từ GitHub.

---

# QUY TẮC CHUYỂN MEMORY

## WM_04_1_DAILY

Nếu việc kéo dài nhiều ngày:

WM_04_1_DAILY

↓

WM_04_1_LONG

---

## WM_04_1_LONG

Khi hoàn thành:

WM_04_1_LONG

↓

LM_04_CURRENT

hoặc

↓

LM_03B_CURRENT

---

## LM_03B_CURRENT

Khi quá lớn:

LM_03B_CURRENT

↓

Tổng hợp

↓

LM_03B_ARCHIVE

---

## LM_04_CURRENT

Khi quá lớn hoặc hết tháng:

LM_04_CURRENT

↓

LM_04_ARCHIVE_YYYY_MM

---

# QUY TẮC HOÀN TẤT

Sau khi PATCH được ghi thành công:

PATCH được xem là hoàn tất.

Không lưu PATCH.

Không tạo lịch sử PATCH.

Không tạo archive PATCH.

GitHub là nguồn chân lý duy nhất.
