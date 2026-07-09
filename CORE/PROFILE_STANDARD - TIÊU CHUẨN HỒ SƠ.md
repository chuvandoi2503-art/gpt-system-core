# PROFILE_STANDARD - TIÊU CHUẨN HỒ SƠ

Phiên bản: 04.002

---

# MỤC ĐÍCH

Chuẩn hóa cấu trúc tối thiểu của một Profile.

Profile là hồ sơ sống của một thực thể được phát triển lâu dài.

Ví dụ:

* Thương hiệu
* Dự án
* Hệ giá trị
* Không gian nội dung
* Lĩnh vực nghiên cứu
* Hệ tri thức

---

# VAI TRÒ RUNTIME

PROFILE_STANDARD không phải Runtime Memory.

PROFILE_STANDARD không phải Prompt.

PROFILE_STANDARD không phải Rule vận hành của GPT Engine.

PROFILE_STANDARD được dùng để:

* Thiết kế Profile mới.
* QC Profile hiện có.
* Kiểm tra Profile có đủ cấu trúc tối thiểu không.
* Làm chuẩn chung để nhiều GPT Engine đọc cùng một loại hồ sơ.
* Hỗ trợ tạo Rule đọc Profile cho từng GPT Engine.

Nếu không có PROFILE_STANDARD:

* GPT Engine vẫn có thể chạy.
* Session vẫn có thể chạy.
* Content OS vẫn có thể chạy nếu đã có Profile cụ thể và Rule đọc Profile riêng.
* Nhưng hệ thống thiếu chuẩn chung để nhân bản, QC và mở rộng Profile.

---

# GPT NÀO ĐỌC FILE NÀY

PROFILE_STANDARD được đọc bởi:

* GPT Kiến Trúc Sư
* GPT Content
* GPT Research
* GPT Engine mới cần tương thích với Profile

---

# ĐỌC Ở BƯỚC NÀO

GPT đọc PROFILE_STANDARD khi cần:

* Thiết kế Profile mới.
* Refactor Profile.
* QC Profile.
* Tạo Rule đọc Profile.
* Chẩn đoán lỗi Content OS liên quan đến thiếu dữ liệu Profile.
* Xác định Profile có đủ cấu trúc để vận hành không.

Không cần đọc PROFILE_STANDARD trong mọi phiên runtime nếu Profile và Rule đọc Profile đã ổn định.

---

# ĐỌC ĐỂ LÀM GÌ

GPT đọc PROFILE_STANDARD để hành động:

* Xác định Profile có những phần nào.
* Xác định mỗi phần lưu loại dữ liệu nào.
* Xác định dữ liệu có bị lưu sai vòng đời không.
* Xác định Profile thiếu phần nào.
* Đề xuất tạo hoặc cập nhật PF_xx phù hợp.
* Kiểm tra Profile có đủ phục vụ Content OS không.

GPT không dùng PROFILE_STANDARD để:

* Viết content trực tiếp.
* Thay thế Profile cụ thể.
* Thay thế Research Package.
* Thay thế Rule của GPT Engine.
* Quy định GPT phải đọc phần nào trong một phiên cụ thể.

---

# NGUYÊN TẮC NỀN TẢNG

Profile không phụ thuộc vào một GPT cụ thể.

GPT Engine có thể thay đổi.

Profile vẫn giữ nguyên.

Profile chỉ lưu dữ liệu thuộc về chính thực thể mà nó đại diện.

Profile không lưu:

* Prompt của GPT Engine
* Rule của GPT Engine
* Workflow riêng của GPT Engine
* Memory của GPT Engine
* Kiến thức chỉ phục vụ riêng một GPT

---

# MÔ HÌNH KIẾN TRÚC

Core

↓

GPT Engine

↓

Profile

↓

Session

---

# PROFILE LÀ GÌ

Profile là hồ sơ sống của một thực thể.

Profile cung cấp:

* Danh tính
* Định hướng
* Hệ giá trị
* Bản đồ hiện diện
* Chỉ mục tri thức
* Trạng thái phát triển
* Tài sản tái sử dụng

Profile không hướng dẫn GPT phải đọc gì.

Việc đọc như thế nào thuộc trách nhiệm của GPT Engine.

---

# CẤU TRÚC TỐI THIỂU

Một Profile tối thiểu gồm:

* PF_00 - Mục lục hồ sơ
* PF_01 - Danh tính và hệ giá trị
* PF_02 - Thế giới hiện diện
* PF_03 - Chỉ mục tri thức
* PF_04 - Tiến độ và việc đang mở
* PF_05 - Tài sản tái sử dụng

---

# PF_00 - MỤC LỤC HỒ SƠ

PF_00 là điểm vào của Profile.

PF_00 không chứa tri thức chi tiết.

PF_00 trả lời:

* Profile này là gì.
* Có những phần nào.
* Mỗi phần lưu loại dữ liệu gì.
* File nào chứa loại dữ liệu nào.

Dùng cho:

* Tra cứu nhanh.
* Điều hướng Profile.
* Xác định nơi cần đọc tiếp.

---

# PF_01 - DANH TÍNH VÀ HỆ GIÁ TRỊ

PF_01 lưu phần gần như bất biến.

Bao gồm:

* Mục đích tồn tại.
* Định hướng dài hạn.
* Hệ giá trị.
* Huyết mạch.
* Điều không làm.
* Đối tượng hiện diện.

Dùng cho:

* Giữ nhất quán định hướng.
* Kiểm tra output có lệch bản sắc không.
* Làm nền cho Content OS và Research.

---

# PF_02 - THẾ GIỚI HIỆN DIỆN

PF_02 là bản đồ không gian của Profile.

PF_02 không phải kho tri thức chi tiết.

PF_02 mô tả:

* Profile hiện diện ở đâu.
* Các vùng nội dung chính là gì.
* Các vùng liên hệ với nhau như thế nào.

Dùng cho:

* Xác định phạm vi nội dung.
* Điều hướng chủ đề.
* Phát hiện vùng thiếu dữ liệu.
* Hỗ trợ lập bản đồ Knowledge Gap.

---

# PF_03 - CHỈ MỤC TRI THỨC

PF_03 là chỉ mục tri thức của Profile.

PF_03 không phải kho lưu toàn bộ dữ liệu.

PF_03 trả lời:

* Profile đã có nhóm tri thức nào.
* Nguồn nào đã có.
* Reality Pack nào đã có.
* Research Package nào đã có.
* Khoảng trống tri thức nào đang tồn tại.
* Dữ liệu nằm ở đâu.

Dùng cho:

* Tra cứu.
* Xác định Knowledge Gap.
* Tạo Research Request.
* Gắn Research Package vào đúng vị trí.
* Đề xuất cập nhật Profile.

---

# PF_04 - TIẾN ĐỘ VÀ VIỆC ĐANG MỞ

PF_04 lưu trạng thái hiện tại.

Bao gồm:

* Đang phát triển đến đâu.
* Đang nghiên cứu gì.
* Đang kiểm thử gì.
* Việc nào đang mở.
* Bước tiếp theo là gì.

PF_04 thay đổi thường xuyên.

PF_04 không lưu lịch sử dài hạn.

Dùng cho:

* Tiếp tục phiên sau.
* Xác định việc đang dở.
* Ưu tiên Research Request.
* Đề xuất cập nhật Profile sau phiên.

---

# PF_05 - TÀI SẢN TÁI SỬ DỤNG

PF_05 lưu tài sản có thể dùng lại.

Bao gồm:

* Reality Pack
* Research Package
* Checklist
* Template
* Framework
* Quy trình
* Bộ dữ liệu đã đóng gói
* Mẫu đầu vào
* Mẫu đầu ra

Dùng cho:

* Tái sử dụng tri thức.
* Giảm nghiên cứu lại.
* Hỗ trợ tạo output nhất quán.
* Cung cấp vật liệu cho Content OS.

---

# ÁNH XẠ VỚI CONTENT OS

Content OS cần Profile để:

## 1. Tra cứu

Đọc:

* PF_00
* PF_03
* PF_05 nếu cần tài sản có sẵn

## 2. Xác định Knowledge Gap

Đọc:

* PF_02
* PF_03
* PF_04

## 3. Tạo Research Request

Đọc:

* PF_03
* PF_04

## 4. Sử dụng Research Package

Đọc:

* PF_03
* PF_05

## 5. Đề xuất cập nhật Profile

Đọc:

* PF_03
* PF_04
* PF_05

---

# VÒNG ĐỜI DỮ LIỆU

Mỗi phần có vòng đời khác nhau.

PF_01:

Gần như bất biến.

PF_02:

Thay đổi ít.

PF_03:

Tăng trưởng liên tục.

PF_04:

Thay đổi gần như mỗi phiên.

PF_05:

Tăng trưởng theo tài sản tái sử dụng.

Không lưu sai vòng đời dữ liệu.

---

# NGUYÊN TẮC CẬP NHẬT

Khi có dữ liệu mới:

* Dữ liệu định danh → PF_01
* Dữ liệu bản đồ hiện diện → PF_02
* Dữ liệu chỉ mục tri thức → PF_03
* Việc đang mở → PF_04
* Tài sản tái sử dụng → PF_05

Nếu không xác định được vị trí lưu:

Không cập nhật Profile.

Cần tạo ghi chú kiểm tra trước.

---

# NGUYÊN TẮC MỞ RỘNG

Khi Profile lớn lên:

* Không sửa cấu trúc nếu chưa cần.
* Ưu tiên thêm dữ liệu vào đúng PF_xx.
* Chỉ sửa cấu trúc khi PROFILE_STANDARD được cập nhật trước.
* Sau đó mới cập nhật từng Profile cụ thể.

---

# TIÊU CHUẨN PASS

Một Profile đạt chuẩn tối thiểu khi:

* Có PF_00 đến PF_05.
* Mỗi PF_xx có vai trò rõ.
* Dữ liệu được lưu đúng vòng đời.
* PF_03 đủ để tra cứu và xác định Knowledge Gap.
* PF_04 đủ để tiếp tục phiên sau.
* PF_05 chỉ chứa tài sản có thể tái sử dụng.
* Không trộn Rule GPT Engine vào Profile.
* Không trộn Memory GPT Engine vào Profile.
* Không trộn Prompt vào Profile.

---

# NGUYÊN TẮC CUỐI CÙNG

Profile là hồ sơ của thực thể.

GPT Engine là bên đọc và vận hành.

PROFILE_STANDARD chỉ quy định cấu trúc chuẩn của hồ sơ.

Rule đọc Profile thuộc về từng GPT Engine.
