# MEMORY_STRUCTURE_TEMPLATE

Phiên bản: 03.000

---

# MỤC TIÊU

Định nghĩa cấu trúc thư mục memory chuẩn áp dụng cho mọi GPT trong hệ sinh thái.

Mục tiêu:

- Dễ nhân bản
- Dễ bảo trì
- Không phình memory
- Giảm dữ liệu phải nạp đầu phiên
- Dễ tổng hợp
- Dễ archive

---

# CẤU TRÚC CHUẨN

memory/

├── WM_03A/

├── WM_04_1/

├── LM_03B/

└── LM_04/

---

# WM_03A

Bộ nhớ lõi GPT.

Ví dụ:

WM_03A_ARCH - BỘ NHỚ LÕI GPT KIẾN TRÚC SƯ.md

WM_03A_CONTENT - BỘ NHỚ LÕI GPT CONTENT OS.md

Mỗi GPT chỉ có 1 file WM_03A.

---

# WM_04_1

Việc đang dở.

Bao gồm:

WM_04_1_<GPT>_DAILY - VIỆC ĐANG DỞ HÔM NAY GPT <GPT>.md

WM_04_1_<GPT>_LONG - VIỆC ĐANG DỞ DÀI HẠN GPT <GPT>.md

---

## DAILY

Mục đích:

Lưu việc đang làm trong ngày.

Được ghi đè.

Không archive.

Không lưu lịch sử.

---

## LONG

Mục đích:

Lưu:

- backlog
- dự án
- mục tiêu tuần
- mục tiêu tháng
- mục tiêu quý

Không nạp mặc định đầu phiên.

---

# LM_03B

Tri thức đã kiểm chứng.

Bao gồm:

LM_03B_<GPT>_CURRENT - TRI THỨC ĐÃ KIỂM CHỨNG GPT <GPT>.md

LM_03B_<GPT>_ARCHIVE_001 - TRI THỨC LƯU TRỮ GPT <GPT>.md

LM_03B_<GPT>_ARCHIVE_002 - TRI THỨC LƯU TRỮ GPT <GPT>.md

...

---

## CURRENT

Chứa:

- kiến thức mới xác nhận
- workflow mới xác nhận
- bài học mới xác nhận

Có thể nạp đầu phiên.

---

## ARCHIVE

Chứa:

- tri thức ổn định
- tri thức ít thay đổi

Không nạp đầu phiên.

Ưu tiên chia theo chủ đề.

Không ưu tiên chia theo thời gian.

---

# LM_04

Nhật ký học tập.

Bao gồm:

LM_04_<GPT>_CURRENT - NHẬT KÝ HỌC TẬP GPT <GPT>.md

LM_04_<GPT>_ARCHIVE_YYYY_MM - NHẬT KÝ LƯU TRỮ GPT <GPT>.md

---

## CURRENT

Lưu:

- lịch sử học tập gần đây
- lỗi mới phát hiện
- kết quả kiểm chứng gần đây

Không bắt buộc nạp đầu phiên.

---

## ARCHIVE

Lưu lịch sử cũ.

Ví dụ:

LM_04_ARCH_ARCHIVE_2026_06.md

LM_04_ARCH_ARCHIVE_2026_07.md

LM_04_ARCH_ARCHIVE_2026_08.md

Không nạp đầu phiên.

---

# QUY TẮC KHỞI TẠO PHIÊN

Mặc định nạp:

- RULE_COMMON
- RULE_<GPT>
- WM_03A_<GPT>
- WM_04_1_<GPT>_DAILY
- LM_03B_<GPT>_CURRENT

---

Không nạp mặc định:

- WM_04_1_<GPT>_LONG
- LM_03B_<GPT>_ARCHIVE
- LM_04_<GPT>_CURRENT
- LM_04_<GPT>_ARCHIVE

---

# QUY TẮC KẾT THÚC PHIÊN

PATCH được phân loại:

- UPDATE_WM_03A
- UPDATE_WM_04_1_DAILY
- UPDATE_WM_04_1_LONG
- UPDATE_LM_03B_CURRENT
- UPDATE_LM_04_CURRENT
- DISCARD

Sau khi người dùng xác nhận:

Ghi trực tiếp vào file đích.

Không lưu patch tồn đọng.
