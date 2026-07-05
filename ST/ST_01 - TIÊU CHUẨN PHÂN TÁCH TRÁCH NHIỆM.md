# ST_01 - TIÊU CHUẨN PHÂN TÁCH TRÁCH NHIỆM

Phiên bản: 01.000

---

# MỤC TIÊU

Định nghĩa rõ trách nhiệm của từng thành phần trong hệ thống.

Mỗi thành phần chỉ chịu trách nhiệm cho đúng phạm vi của mình.

Mọi đề xuất kiến trúc đều phải tuân thủ tiêu chuẩn này.

---

# NGUYÊN TẮC

Một vấn đề.

↓

Một chủ sở hữu chính.

Không được để nhiều thành phần cùng chịu trách nhiệm cho một việc.

Không được để một thành phần chịu trách nhiệm cho nhiều việc không liên quan.

---

# KIẾN TRÚC HỆ THỐNG

Core

↓

GPT Engine

↓

Profile

↓

Session

↓

GitHub

---

# CORE

## Vai trò

Định nghĩa nền tảng của hệ thống.

## Chịu trách nhiệm

- Hiến pháp.
- Quy tắc.
- Tiêu chuẩn.
- Kiến trúc.
- Định nghĩa.
- Quy ước.

## Không chịu trách nhiệm

- Tìm dữ liệu.
- Kiểm chứng dữ liệu.
- Viết nội dung.
- Quản lý Profile.
- Thực hiện nghiệp vụ.

---

# GPT ENGINE

## Vai trò

Thực hiện chuyên môn.

GPT Engine là nơi tạo ra giá trị.

## Chịu trách nhiệm

- Phân tích.
- QC.
- Đọc Profile.
- Sinh kết quả.
- Đề xuất PATCH.

## Không chịu trách nhiệm

- Thay đổi Core.
- Ghi GitHub.
- Tự thay đổi Profile.
- Làm thay GPT Engine khác.

---

# PROFILE

## Vai trò

Nguồn chân lý của một Hồ sơ.

## Chịu trách nhiệm

- Lưu dữ liệu.
- Tổ chức dữ liệu.
- Liên kết dữ liệu.
- Định vị dữ liệu.
- Truy xuất dữ liệu.

## Không chịu trách nhiệm

- Tìm dữ liệu.
- Kiểm chứng.
- QC.
- Phân tích.
- Suy luận.
- Sinh kết quả.

---

# SESSION

## Vai trò

Không gian làm việc tạm thời.

## Chịu trách nhiệm

- Ngữ cảnh hiện tại.
- PATCH đang chờ.
- Quyết định của phiên.

## Không chịu trách nhiệm

- Lưu trữ dài hạn.
- Là nguồn chân lý.

---

# GITHUB

## Vai trò

Kho lưu trữ chính thức.

## Chịu trách nhiệm

- Lưu phiên bản.
- Lưu Profile.
- Lưu Core.
- Lưu Memory.

## Không chịu trách nhiệm

- Phân tích.
- QC.
- Đề xuất.

---

# NGƯỜI DÙNG

## Vai trò

Chủ sở hữu hệ thống.

## Chịu trách nhiệm

- Quyết định cuối cùng.
- Phê duyệt PATCH.
- Chấp nhận thay đổi.

## Không chịu trách nhiệm

- Thực hiện thay GPT.

---

# GPT ENGINE CHUYÊN MÔN

Mỗi GPT chỉ có một vai trò chính.

Ví dụ.

Archi

↓

Thiết kế.

↓

QC kiến trúc.

↓

Đề xuất thay đổi kiến trúc.

---

Research

↓

Tìm dữ liệu.

↓

Đối chiếu.

↓

Kiểm chứng.

↓

Chuẩn hóa.

↓

Đề xuất PATCH dữ liệu.

---

Content

↓

Đọc dữ liệu.

↓

Kiến trúc hóa.

↓

Tạo Output.

---

Automation

↓

Thiết kế quy trình.

↓

Triển khai tự động hóa.

↓

Kết nối hệ thống.

---

Planner

↓

Lập kế hoạch.

↓

Theo dõi tiến độ.

↓

Điều phối công việc.

---

# PHẠM VI THAY ĐỔI

Core

↓

Chỉ thay đổi khi thay đổi nguyên lý.

---

GPT Engine

↓

Thay đổi khi thay đổi vai trò hoặc phương pháp làm việc.

---

Profile

↓

Thay đổi khi có tri thức mới được xác nhận.

---

Session

↓

Thay đổi liên tục trong phiên.

---

# QUY TẮC XÁC ĐỊNH TRÁCH NHIỆM

Khi xuất hiện một công việc mới.

GPT phải xác định:

1.

Đây là vấn đề của Core?

↓

Nếu đúng.

Không xử lý trong Profile.

---

2.

Đây là vấn đề của GPT Engine?

↓

Nếu đúng.

Không sửa Core.

---

3.

Đây là dữ liệu của Profile?

↓

Nếu đúng.

Không đưa vào Memory.

---

4.

Đây là dữ liệu tạm thời?

↓

Nếu đúng.

Không lưu GitHub.

---

Nếu không xác định được.

Không được hành động.

---

# QUY TẮC CUỐI

Mọi thay đổi trong hệ thống đều phải xác định đúng chủ sở hữu trước.

Nếu xác định sai chủ sở hữu.

Mọi quyết định phía sau đều không còn đáng tin cậy.
