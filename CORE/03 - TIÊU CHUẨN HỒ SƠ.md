# 03 - TIÊU CHUẨN HỒ SƠ

Phiên bản: 01.001

---

# MỤC ĐÍCH

Quy định cấu trúc tối thiểu của một Hồ sơ.

Hồ sơ là nơi lưu trữ tri thức dài hạn của một lĩnh vực, dự án, thương hiệu hoặc thực thể cần phát triển lâu dài.

---

# VAI TRÒ RUNTIME

File này được GPT đọc khi cần:

* Tạo Hồ sơ mới.
* QC Hồ sơ hiện có.
* Xác định Hồ sơ có đủ cấu trúc tối thiểu không.
* Đề xuất cập nhật Hồ sơ.
* Phân biệt dữ liệu nào nên lưu vào phần nào.

File này không dùng để:

* Viết nội dung trực tiếp.
* Thay thế Memory.
* Thay thế Rule của GPT.
* Quy định workflow riêng của GPT.

---

# NGUYÊN TẮC

Một Hồ sơ chỉ phục vụ một lĩnh vực hoặc một thực thể.

Không trộn nhiều lĩnh vực vào cùng một Hồ sơ.

Không lưu dữ liệu tạm thời vào Hồ sơ.

Không lưu suy đoán chưa xác nhận vào Hồ sơ.

---

# CẤU TRÚC TỐI THIỂU

Một Hồ sơ tối thiểu gồm 5 phần:

* 01 - Danh tính
* 02 - Hệ giá trị
* 03 - Tri thức
* 04 - Tiến độ
* 05 - Patch

---

# 01 - DANH TÍNH

Lưu thông tin định danh của Hồ sơ.

Trả lời:

* Hồ sơ này là gì?
* Tên là gì?
* Mục tiêu là gì?
* Phạm vi là gì?

Dùng để xác định Hồ sơ đang đại diện cho thực thể nào.

---

# 02 - HỆ GIÁ TRỊ

Lưu các nguyên tắc gần như không thay đổi.

Trả lời:

* Hồ sơ muốn trở thành điều gì?
* Giá trị cốt lõi là gì?
* Điều gì không được làm?
* Điều gì phải được giữ ổn định?

Dùng để kiểm tra các đề xuất có lệch định hướng không.

---

# 03 - TRI THỨC

Lưu tri thức đã được xác nhận.

Bao gồm:

* Kiến thức nền.
* Dữ liệu đã kiểm chứng.
* Tài sản dùng lâu dài.
* Nguồn tham chiếu đã được chấp nhận.

Không lưu:

* Ý tưởng tạm thời.
* Giả thuyết chưa xác nhận.
* Nội dung đang tranh luận.
* Ghi chú phiên làm việc.

---

# 04 - TIẾN ĐỘ

Lưu trạng thái hiện tại của Hồ sơ.

Bao gồm:

* Đang ở giai đoạn nào.
* Đang triển khai gì.
* Đang kiểm chứng gì.
* Việc nào đang mở.
* Bước tiếp theo là gì.

Đây là phần thay đổi thường xuyên.

Không dùng để lưu lịch sử dài hạn.

---

# 05 - PATCH

Lưu các thay đổi đã được người dùng xác nhận.

Bao gồm:

* Nội dung cập nhật.
* Lý do cập nhật.
* Phần bị ảnh hưởng.
* Thời điểm hoặc phiên cập nhật nếu cần.

Patch chỉ ghi thay đổi đã xác nhận.

Không ghi suy đoán vào Patch.

---

# NGUYÊN TẮC CẬP NHẬT

Khi có dữ liệu mới:

* Dữ liệu định danh → 01
* Dữ liệu giá trị / nguyên tắc → 02
* Tri thức đã xác nhận → 03
* Việc đang mở → 04
* Thay đổi đã xác nhận → 05

Nếu chưa rõ dữ liệu thuộc phần nào:

Không cập nhật Hồ sơ.

Tạo ghi chú cần kiểm tra trước.

---

# TIÊU CHUẨN PASS

Một Hồ sơ đạt chuẩn tối thiểu khi:

* Có đủ 5 phần.
* Mỗi phần có vai trò rõ.
* Tri thức mới chỉ được đưa vào Hồ sơ khi đã QC.
* Dữ liệu được lưu đúng vòng đời.
* Không trộn Memory của GPT vào Hồ sơ.
* Không trộn Rule của GPT vào Hồ sơ.
* Không trộn nội dung tạm thời vào Hồ sơ.

---

# NGUYÊN TẮC CUỐI CÙNG

Hồ sơ chỉ lưu và tổ chức tri thức.

Hồ sơ không quyết định GPT phải sử dụng tri thức như thế nào.

Đó là trách nhiệm của từng GPT.
