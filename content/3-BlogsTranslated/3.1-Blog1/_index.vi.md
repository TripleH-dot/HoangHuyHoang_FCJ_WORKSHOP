---
title: "Blog 1"
date: "2025-10-02"
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---


# Arctic: Kiểm thử ứng dụng desktop tự động

*bởi Elif Aslan and David Alvarez | vào ngày 10 tháng 5 năm 2025 | trong AWS Java Development, Developer Tools, Java, Open Source, Technical How-to*

---

Nhóm Amazon Corretto cung cấp hơn 75 gói OpenJDK cho nhiều nền tảng và phiên bản Java khác nhau, bao gồm thư viện giao diện người dùng **AWT** và **Swing**. Việc xác thực từng bản phát hành là cần thiết để đảm bảo không gây ra lỗi hồi quy, bởi vì ngay cả những thay đổi nhỏ nhất cũng có thể ảnh hưởng đến cách các phần tử đồ họa được hiển thị.

Việc xác thực các ứng dụng desktop tương tác như một phần của quy trình build tự động là **rất khó**. Các giải pháp tồn tại bị hạn chế về phạm vi và thường yêu cầu các bài kiểm thử phải được viết riêng để hỗ trợ tự động hóa, điều này tốn nhiều thời gian và không thể mở rộng.

> **Arctic** là công cụ giúp tự động hóa việc xác thực các ứng dụng desktop. Nó hỗ trợ các bài kiểm thử **hiện có** (legacy tests) vốn được thiết kế để chạy thủ công mà **không cần chỉnh sửa chúng**.

Arctic hoạt động bằng cách dựa vào hệ điều hành để ghi lại tất cả các sự kiện cần thiết trong quá trình ghi và tái tạo lại chúng trong quá trình phát lại.

Arctic chạy trên Linux, Windows và macOS trên hệ thống x86\_64, và trên Linux cùng macOS trên hệ thống aarch64.

---

## 🚀 Arctic hoạt động như thế nào?

Arctic hoạt động theo cơ chế **so sánh hình ảnh dựa trên bản ghi** (Image-based recording and comparison).

### 1. Chế độ Ghi (Recording Mode)

* Bài kiểm thử được chạy thủ công với Arctic ở **“chế độ ghi”** để thu thập một tập ảnh chụp màn hình cơ bản.
* Tất cả các sự kiện bàn phím và chuột, cùng với ảnh chụp màn hình, sẽ được lưu lại.

### 2. Chế độ Phát lại và So sánh

* Bản ghi được sử dụng để phát lại chuỗi sự kiện bàn phím và chuột gốc, đồng thời ghi lại một tập ảnh chụp màn hình mới.
* Arctic so sánh hai tập ảnh để xác minh rằng chúng giống nhau.

### Hỗ trợ so sánh nâng cao

Một tính năng nổi bật của Arctic là khả năng hỗ trợ các tình huống mà việc **khớp pixel hoàn hảo là không thể**:

* **“Workbench”**: Một cửa sổ được vẽ ở nền, xác định khu vực màn hình mà Arctic sẽ chú ý đến.
* **“Shades”**: Các cửa sổ dùng để che đi những phần không liên quan hoặc có thể xuất hiện ngẫu nhiên.
* Arctic hỗ trợ nhiều cơ chế so sánh hình ảnh khác nhau để phân biệt giữa **dao động nhỏ** (sai lệch màu sắc hoặc pixel) và những khác biệt thực sự đáng kể.

Arctic cũng bao gồm cơ chế để xem lại các so sánh hình ảnh bị lỗi, cho phép người dùng thêm ảnh chụp hiện tại làm các **lựa chọn được phê duyệt** (approved alternatives) để sử dụng cho lần chạy kiểm thử tiếp theo.

### Các tính năng khác của Arctic:

* Bộ so sánh hình ảnh có thể cấu hình để đối chiếu ảnh chụp màn hình.
* Khả năng lưu và khôi phục phiên làm việc.
* Tự động loại bỏ các sự kiện dư thừa trong quá trình phát lại kiểm thử.
* Kiểm soát tốc độ phát lại kiểm thử, cho phép chạy nhanh hơn so với tốc độ ghi ban đầu.
* Ghi log có thể tùy chỉnh.
* Lớp phủ giúp con người dễ dàng xác định sự khác biệt giữa hai hình ảnh.

---

## 🛠️ Hướng dẫn bắt đầu sử dụng Arctic

### 1. Cấu hình & Yêu cầu

* Arctic là một ứng dụng Java, yêu cầu tối thiểu **JDK 11** (khuyến nghị **JDK 21**).
* Cấu hình thông qua hai tệp: `recorder.properties` và `player.properties` trong thư mục làm việc hiện tại.

### 2. Cấu hình môi trường kiểm thử

Vì Arctic dựa vào so sánh pixel, cần duy trì sự ổn định của môi trường để tránh lỗi giả. Các cài đặt cần kiểm soát gồm:

* Hình nền máy tính
* Độ phân giải màn hình
* Giao diện
* Phông chữ được cài đặt

### 3. Tải xuống & Điều khiển

* [Tải Arctic binaries](https://github.com/amazon-corretto/arctic) hoặc [Arctic source code](https://github.com/amazon-corretto/arctic)
* **Phím điều khiển:** Sử dụng tổ hợp phím bổ trợ (`ctrl` hoặc `alt`) để ra lệnh mà không ảnh hưởng đến kiểm thử.
    * Mặc định: `ctrl+alt+z` (Bắt đầu/Dừng ghi) và `ctrl+alt+x` (Chụp ảnh màn hình).

### 4. Ghi một bài kiểm thử

1.  Khởi động Arctic ở **chế độ ghi**: `java -jar arctic-<VERSION>.jar -r`
2.  Định vị cửa sổ **Workbench** (khu vực quan tâm) và **Shade** (khu vực che).
3.  Bắt đầu bài kiểm thử: `java -jar arctic-<VERSION>.jar -c test start <testName> <testCase>`.
4.  Thực hiện thao tác thủ công và **chụp lại ảnh màn hình** khi có thay đổi UI quan trọng.
5.  Dừng ghi. Ảnh chụp và bản ghi được lưu trong thư mục `tests`.

### 5. Phát lại bài kiểm thử

1.  Khởi động Arctic ở **chế độ phát lại**: `java -jar arctic-<VERSION>.jar -p`
2.  Yêu cầu Arctic chạy bài kiểm thử: `java -jar arctic-<VERSION>.jar -c test start <testName> <testCase>`.
3.  Thông báo kết thúc: `java -jar arctic-<VERSION>.jar test finish <testName> <testCase> <result>`

> Nếu `result` là `true` và tất cả ảnh chụp đạt yêu cầu, Arctic sẽ đánh dấu bài kiểm thử là **ok**. Ngược lại, nó sẽ là **thất bại**.

---

## 📊 Kết quả & Xem lại

### Lấy kết quả

Arctic hỗ trợ xuất kết quả dưới các định dạng sau bằng lệnh: `java -jar arctic-<VERSION>.jar <format> save <filename>`

| Định dạng (`<format>`) | Mô tả |
| :--- | :--- |
| `xml` | Báo cáo **JUnit XML** |
| `tap` | **TAP** phiên bản 13 |
| `jtx` | Tệp loại trừ cho **jtHarness** |

### Xem lại so sánh ảnh chụp màn hình

Để xem lại các ảnh chụp bị lỗi trong phiên làm việc hiện tại và thêm chúng làm phương án thay thế hợp lệ, sử dụng lệnh: `java -jar arctic-<VERSION>.jar -c sc all`.

---

## 🔗 Tài nguyên & Đóng góp

Nhóm Amazon Corretto hoan nghênh mọi phản hồi và câu hỏi.

* Truy cập kho lưu trữ GitHub của Arctic: [Arctic github repository](https://github.com/amazon-corretto/arctic) để tìm hiểu thêm và đóng góp.
* **Video Demo:** [https://youtu.be/diA0IPl-bEU](https://youtu.be/diA0IPl-bEU)

---

### Lời cảm ơn

Các dự án mã nguồn mở đã góp phần giúp Arctic trở thành hiện thực:

* jNativeHook
* Apache Commons Configuration
* Google Gson
* Google Guice
* JUnit
* Mockito
* SLF4J
* Lombok
* Checkstyle
* Gradle

---

### Thông tin Tác giả

#### Elif Aslan

Kỹ sư Phần mềm tại AWS, chuyên về các dự án JDK, release engineering, và system design.

#### David Alvarez

Kỹ sư Phát triển Phần mềm tại Amazon hơn mười năm, tập trung vào nhiều khía cạnh khác nhau của OpenJDK. Bạn có thể tìm thấy anh ấy trên GitHub với tên **@alvdavi**.
