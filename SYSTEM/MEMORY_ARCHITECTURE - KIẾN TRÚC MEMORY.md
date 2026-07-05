# MEMORY_ARCHITECTURE

Phiên bản: 04.001

---

# MỤC TIÊU

Hệ thống memory phải:

- Đơn giản
- Dễ nhân bản
- Dễ bảo trì
- Dễ mở rộng
- Không phình vô hạn
- Không tồn đọng patch
- Có thể vận hành nhiều năm
- Tách rõ GPT Engine và Profile

---

# NGUYÊN TẮC NỀN TẢNG

GitHub là nguồn chân lý.

Memory hội thoại không phải nguồn chân lý.

Knowledge Upload không phải nguồn chân lý.

GPT Engine không lưu cứng tri thức riêng của từng Profile.

Profile là nguồn chân lý cho một hồ sơ, thương hiệu, dự án, hệ giá trị hoặc không gian vận hành cụ thể.

Nhiều GPT Engine có thể cùng đọc một Profile.

---

# MÔ HÌNH KIẾN TRÚC CHUẨN

Hệ thống vận hành theo mô hình:

Core

↓

GPT Engine

↓

Profile

↓

Session

---

## Core

Core là luật chung toàn hệ.

Core chứa:

- RULE_COMMON
- MEMORY_ARCHITECTURE
- MEMORY_INDEX
- PATCH_STANDARD
- NAMING_CONVENTION
- GITHUB_WRITE_POLICY
- GITHUB_ACTION_SETUP
- RESTORE_GUIDE

Core không chứa tri thức riêng của một Profile.

---

## GPT Engine

GPT Engine là động cơ vận hành.

Ví dụ:

- GPT Kiến Trúc Sư
- GPT Content OS
- GPT Research
- GPT CRM
- GPT Sales
- GPT Automation

GPT Engine lưu:

- Vai trò
- Quy trình vận hành
- Luật chuyên ngành
- Memory vận hành của chính GPT
- Tri thức đã kiểm chứng về cách GPT hoạt động

GPT Engine không lưu:

- Bản sắc riêng của Profile
- Hệ giá trị riêng của Profile
- Tri thức riêng của Profile
- Trạng thái triển khai riêng của Profile

---

## Profile

Profile là hồ sơ sống của một hệ cụ thể.

Profile có thể đại diện cho:

- Một thương hiệu
- Một dự án
- Một hệ giá trị
- Một không gian nội dung
- Một lĩnh vực người dùng muốn nuôi lớn lâu dài

Profile lưu:

- Danh tính
- Mục đích tồn tại
- Định hướng thương hiệu
- Hệ giá trị
- Huyết mạch
- Thế giới hiện diện
- Tri thức riêng
- Trạng thái triển khai
- Tài sản tái sử dụng

Profile là nơi lớn lên theo thời gian.

---

## Session

Session là phiên làm việc hiện tại.

Session lưu:

- Việc đang làm
- Bối cảnh tạm thời
- Quyết định trong phiên
- PATCH đang chờ duyệt

Session không phải nguồn chân lý dài hạn.

---

# CẤU TRÚC MEMORY GPT ENGINE

Mọi Runtime Repository của GPT Engine phải sử dụng:

memory/

├── WM_03A/

├── WM_04_1/

├── LM_03B/

└── LM_04/

---

# WM_03A

Bộ nhớ lõi GPT.

Mỗi GPT chỉ có một file WM_03A.

Ví dụ:

memory/WM_03A/

- WM_03A_ARCH - BỘ NHỚ LÕI GPT KIẾN TRÚC SƯ.md
- WM_03A_CONTENT - BỘ NHỚ LÕI GPT CONTENT OS.md

---

## Vai trò

Lưu:

- Vai trò GPT
- Mục tiêu GPT
- Quy trình vận hành GPT
- Triết lý hoạt động GPT
- Cấu hình vận hành của GPT Engine

Không lưu:

- Tri thức riêng của Profile
- Trạng thái riêng của Profile
- Hệ giá trị riêng của Profile

---

## Quy tắc

- Nạp đầu phiên
- Kích thước nhỏ
- Chỉ thay đổi khi GPT Engine thay đổi

---

# WM_04_1

Việc đang dở của GPT Engine.

Sử dụng thư mục:

memory/WM_04_1/

---

## WM_04_1_DAILY

Lưu:

- Việc đang làm hôm nay
- Việc đang dở phiên gần nhất
- Bước tiếp theo cần thực hiện của GPT Engine

Quy tắc:

- Nạp đầu phiên
- Được ghi đè
- Không archive
- Không lưu lịch sử
- Không lưu tri thức
- Không lưu backlog dài hạn
- Không lưu trạng thái riêng của Profile nếu trạng thái đó thuộc Profile

Nếu việc kéo dài nhiều ngày:

Chuyển sang:

WM_04_1_LONG

---

## WM_04_1_LONG

Lưu:

- Dự án dài hạn của GPT Engine
- Backlog dài hạn của GPT Engine
- Công việc tuần / tháng / quý của GPT Engine

Quy tắc:

- Không nạp mặc định đầu phiên
- Chỉ đọc khi cần
- Không lưu tri thức
- Không lưu nhật ký

Khi hoàn thành:

- Chuyển sang LM_04_CURRENT

hoặc

- Chuyển sang LM_03B_CURRENT

Khi không còn giá trị:

- DISCARD

---

# LM_03B

Tri thức đã kiểm chứng của GPT Engine.

Sử dụng thư mục:

memory/LM_03B/

---

## LM_03B_CURRENT

Lưu:

- Kiến thức đã xác nhận về GPT Engine
- Workflow đã xác nhận
- Quy trình đã xác nhận
- Kiến trúc đã xác nhận
- Bài học đã xác nhận

Không lưu:

- Ý tưởng
- Giả thuyết
- Suy đoán
- Tri thức riêng của Profile

Có thể nạp đầu phiên.

---

## Ngưỡng tổng hợp

Khi:

- Trên 300 dòng

hoặc

- Trên 50 mục tri thức

thì phải:

- Tổng hợp
- Rút gọn
- Chuyển tri thức ổn định sang Archive

---

## LM_03B_ARCHIVE

Lưu tri thức ổn định của GPT Engine.

Quy tắc:

- Không nạp đầu phiên
- Chỉ đọc khi tra cứu
- Không chia theo thời gian
- Ưu tiên chia theo chủ đề

---

# LM_04

Nhật ký học tập của GPT Engine.

Sử dụng thư mục:

memory/LM_04/

---

## LM_04_CURRENT

Lưu:

- Bài học gần đây
- Kết quả kiểm chứng
- Lịch sử học tập gần đây của GPT Engine

Không bắt buộc nạp đầu phiên.

Chỉ đọc khi cần tra cứu.

---

## LM_04_ARCHIVE

Lưu lịch sử cũ của GPT Engine.

Quy tắc:

- Không nạp đầu phiên
- Chỉ đọc khi tra cứu
- Chia theo thời gian

Định dạng:

LM_04_<GPT>_ARCHIVE_YYYY_MM

---

# CẤU TRÚC PROFILE CHUẨN

Profile được lưu ngoài memory của GPT Engine.

Thư mục chuẩn:

profiles/

├── _TEMPLATE/

└── <PROFILE_ID>/

---

Mỗi Profile tối thiểu gồm:

profiles/<PROFILE_ID>/

├── PF_00_<PROFILE_ID> - HỒ SƠ TỔNG QUAN.md

├── PF_01_<PROFILE_ID> - DANH TÍNH VÀ HỆ GIÁ TRỊ.md

├── PF_02_<PROFILE_ID> - THẾ GIỚI HIỆN DIỆN.md

├── PF_03_<PROFILE_ID> - CHỈ MỤC TRI THỨC.md

├── PF_04_<PROFILE_ID> - TRẠNG THÁI HIỆN TẠI.md

└── PF_05_<PROFILE_ID> - TÀI SẢN TÁI SỬ DỤNG.md

---

# PF_00 - HỒ SƠ TỔNG QUAN

Mục đích:

Là điểm vào chính của Profile.

Lưu:

- Profile ID
- Tên Profile
- Mục đích tồn tại
- Repository / thư mục liên quan
- Các file con của Profile
- Quy trình nạp Profile

---

# PF_01 - DANH TÍNH VÀ HỆ GIÁ TRỊ

Lưu phần gần như bất biến của Profile:

- Định hướng
- Thương hiệu muốn trở thành
- Hệ giá trị
- Huyết mạch
- Điều không làm
- Đối tượng hiện diện
- Nguyên tắc nền tảng

File này thay đổi rất ít.

---

# PF_02 - THẾ GIỚI HIỆN DIỆN

Lưu bản đồ hiện diện của Profile:

- Vùng đời sống
- Nhánh chủ đề
- Thùng tri thức
- Mối liên hệ giữa các nhánh
- Nhánh đang ưu tiên

WORLD không phải kho tri thức.

WORLD là bản đồ để GPT Engine định tuyến.

---

# PF_03 - CHỈ MỤC TRI THỨC

Lưu chỉ mục tri thức của Profile:

- Nhóm tri thức đã có
- Dữ liệu đời sống
- Dữ liệu đã kiểm chứng
- Gói đầu vào cho Content
- Nguồn đã dùng
- Khoảng trống tri thức

PF_03 không bắt buộc lưu toàn bộ nội dung tri thức.

PF_03 ưu tiên làm chỉ mục để truy xuất.

---

# PF_04 - TRẠNG THÁI HIỆN TẠI

Lưu trạng thái động của Profile:

- Đang triển khai
- Đang kiểm thử
- Đang nghiên cứu
- Câu hỏi đang mở
- Việc cần tiếp tục
- Ghi chú phiên gần nhất

PF_04 có thể cập nhật thường xuyên.

---

# PF_05 - TÀI SẢN TÁI SỬ DỤNG

Lưu tài sản của Profile:

- Khung nội dung
- Checklist
- Quy trình
- Mẫu output
- Prompt phụ trợ
- Bộ dữ liệu đầu vào đã đóng gói

PF_05 không lưu việc đang dở hằng ngày.

---

# KHỞI TẠO PHIÊN CHUẨN CỦA GPT ENGINE

Mặc định nạp:

- RULE_COMMON
- RULE_<GPT>
- WM_03A_<GPT>
- WM_04_1_<GPT>_DAILY
- LM_03B_<GPT>_CURRENT

Không nạp mặc định:

- WM_04_1_<GPT>_LONG
- LM_03B_<GPT>_ARCHIVE
- LM_04_<GPT>_CURRENT
- LM_04_<GPT>_ARCHIVE

---

# KHỞI TẠO PHIÊN CÓ PROFILE

Khi người dùng yêu cầu làm việc với một Profile, GPT phải:

Đọc GPT Engine

↓

Xác định PROFILE_ID

↓

Đọc PF_00

↓

Đọc PF_01

↓

Đọc PF_02

↓

Đọc PF_04

↓

Chỉ đọc PF_03 hoặc PF_05 khi công việc yêu cầu

---

# NGUYÊN TẮC NẠP PROFILE

Không nạp toàn bộ Profile nếu không cần.

Mặc định chỉ nạp:

- PF_00
- PF_01
- PF_02
- PF_04

Nạp theo nhu cầu:

- PF_03
- PF_05
- Dữ liệu chi tiết
- Gói đầu vào
- Archive của Profile nếu có

---

# KẾT THÚC PHIÊN CHUẨN

PATCH phải được phân loại:

## Thuộc GPT Engine

- UPDATE_WM_03A
- UPDATE_WM_04_1_DAILY
- UPDATE_WM_04_1_LONG
- UPDATE_LM_03B_CURRENT
- UPDATE_LM_04_CURRENT

## Thuộc Profile

- UPDATE_PROFILE_PF_00
- UPDATE_PROFILE_PF_01
- UPDATE_PROFILE_PF_02
- UPDATE_PROFILE_PF_03
- UPDATE_PROFILE_PF_04
- UPDATE_PROFILE_PF_05

## Không lưu

- DISCARD

---

# QUY TẮC PHÂN LOẠI CUỐI PHIÊN

Nếu nội dung thay đổi cách GPT vận hành:

Lưu vào GPT Engine.

Nếu nội dung thay đổi danh tính, hệ giá trị, thế giới, tri thức, trạng thái hoặc tài sản của một Profile:

Lưu vào Profile.

Nếu nội dung chỉ là trao đổi tạm thời, suy đoán, ý tưởng chưa kiểm chứng hoặc không phục vụ vận hành tương lai:

DISCARD.

Nếu chưa đủ cơ sở phân loại:

Đánh dấu cần QC, không tự ghi.

---

# QUY TẮC CUỐI CÙNG

Không để memory GPT chứa tri thức riêng của Profile.

Không để Profile chứa quy trình vận hành riêng của GPT Engine nếu quy trình đó dùng chung cho nhiều Profile.

Không để một file trở thành nơi chứa mọi thứ.

Memory tốt là memory giúp GPT vận hành nhẹ hơn.

Profile tốt là Profile giúp nhiều GPT Engine cùng hiểu đúng một thực thể sống.
