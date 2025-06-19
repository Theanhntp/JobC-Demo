# 💼 JobC – Nền Tảng Kết Nối Việc Làm Hiện Đại

**JobC** là hệ thống tuyển dụng và tìm việc làm trực tuyến, hỗ trợ các vai trò: **Guest**, **User (Job Seeker)**, **Enterprise (Employer)**, và **Administrator**. Dự án tối ưu hóa trải nghiệm ứng tuyển và tuyển dụng với các tính năng như tạo CV, phỏng vấn video, chat thời gian thực, và quản lý hồ sơ hiệu quả.

---

## 🎯 Mục Tiêu Hệ Thống

- 🔍 **Tìm việc dễ dàng**: Giao diện thân thiện, hỗ trợ tìm kiếm và lọc công việc.
- 📝 **Ứng tuyển thông minh**: Tạo và gửi CV trực tiếp, theo dõi trạng thái ứng tuyển.
- 🧑‍💼 **Quản lý tuyển dụng hiệu quả**: Doanh nghiệp quản lý bài đăng, CV, và phỏng vấn online.
- 🛡️ **Giám sát hệ thống**: Admin kiểm duyệt bài đăng, thống kê, và quản lý tài khoản tập trung.

---

## 🔧 Chức Năng Chính

### 👤 Guest
- Đăng ký tài khoản.
- Tìm kiếm và xem chi tiết công việc.

### 👥 User (Người tìm việc)
- Đăng nhập / Đăng xuất.
- Viết, tải lên, và gửi CV.
- Tìm kiếm và xem chi tiết công việc.
- Bình luận, chỉnh sửa, hoặc xóa bình luận.
- Báo cáo bài đăng vi phạm.
- Chat với admin.
- Tham gia phỏng vấn trực tuyến.
- Xem và chỉnh sửa hồ sơ cá nhân.
- Đổi mật khẩu / Đặt lại mật khẩu.

### 🏢 Enterprise (Nhà tuyển dụng)
- Đăng bài tuyển dụng, chỉnh sửa thông tin công ty.
- Xem và duyệt CV ứng viên.
- Chấp nhận hoặc từ chối ứng viên.
- Chat và phỏng vấn trực tuyến.
- Quản lý danh sách công việc đã đăng.

### 🛠️ Admin (Quản trị viên)
- Duyệt bài đăng tuyển dụng.
- Khóa / mở khóa / xóa tài khoản.
- Xem thống kê bài đăng theo doanh nghiệp.

---

## 🧠 Luồng Nghiệp Vụ Tổng Quát

1. **Guest truy cập**: Xem công việc → Đăng ký tài khoản để trở thành User.
2. **User tìm việc**: Đăng nhập → Viết CV → Gửi ứng tuyển → Theo dõi phản hồi → Tham gia phỏng vấn.
3. **Enterprise tuyển dụng**: Đăng tin → Admin duyệt → Nhận CV → Phỏng vấn → Tuyển dụng.
4. **Admin quản lý**: Kiểm duyệt nội dung → Quản lý người dùng và thống kê dữ liệu.

---

## 🧩 Kiến Trúc Hệ Thống

| **Thành Phần**         | **Công Nghệ**                     |
|-------------------------|-----------------------------------|
| **Frontend**           | JSP, HTML, CSS, Bootstrap 4      |
| **Backend**            | Java Servlet / JSP               |
| **Máy chủ ứng dụng**   | Apache Tomcat 9.x                |
| **Cơ sở dữ liệu**      | MySQL                            |
| **Thư viện JDBC**      | MySQL Connector/J                |
| **Gửi email**          | JavaMail API                     |
| **Chat / Video Call**  | Messenger, WebRTC (giả lập)      |

---

## 📸 Giao Diện Minh Họa

Dưới đây là một số hình ảnh minh họa giao diện của JobC:

| **Tính Năng**            | **Hình Ảnh**                                                                 |
|--------------------------|------------------------------------------------------------------------------|
| **Trang chủ**            | <img src="/IMG/HomePage.png" alt="Home Page" width="300" />                      |
| **Đăng nhập**            | <img src="/IMG/SignUp.png" alt="Login" width="300" />                         |
| **Gửi CV**               | <img src="/IMG/SentCV.png" alt="Write CV" width="300" />                    |
| **Xem CV**               | <img src="/IMG/ViewCV.png" alt="View CV" width="300" />                    |
| **Phỏng vấn video**      | <img src="/IMG/VideoCall.png" alt="Interview" width="300" />                 |
| **Quản lý công việc**    | <img src="/IMG/ViewJob.png" alt="Post Job" width="300" />                   |
| **Quản lý tài khoản**    | <img src="/IMG/LockDelete.png.png" alt="Statistic" width="300" />                 |

---

## 📂 Cấu Trúc Dự Án

```
JobC/
├── build.xml             # File build Ant
├── src/
│   ├── controller/       # Servlet xử lý request
│   ├── model/            # DAO, kết nối DB
│   └── utils/            # Tiện ích: Email, Token, Validate...
├── web/
│   ├── css/              # Giao diện CSS, Bootstrap
│   ├── js/               # Script JS
│   ├── pages/            # Các trang JSP chính
│   └── index.jsp         # Trang chủ
├── WEB-INF/
│   ├── web.xml           # Cấu hình Servlet
│   └── lib/              # Thư viện (JAR)
└── Doc+DB/               # Tài liệu + thiết kế cơ sở dữ liệu
```

---

## ⚙️ Yêu Cầu Hệ Thống

- Java JDK 8 hoặc 11
- Apache Tomcat 9+
- MySQL 5.7+ hoặc 8.x
- NetBeans (tùy chọn, hỗ trợ chạy trực tiếp)
- MySQL Connector/J

---

## 🚀 Khởi Chạy Ứng Dụng

### 1. Thiết lập cơ sở dữ liệu
- Tạo database `jobc` (hoặc tên tương ứng).
- Nhập các bảng theo script trong thư mục `Doc+DB`.
- Cập nhật thông tin kết nối trong `DatabaseInfo.java`.

### 2. Build và deploy ứng dụng

#### Cách 1: Dùng NetBeans
```bash
# Mở project trong NetBeans
# Clean and Build → Run
```

---

## 📑 Ghi Chú
- File `.war` có thể cần đổi tên để dễ truy cập.
- Đảm bảo file `mysql-connector-java.jar` nằm trong thư mục `Tomcat/lib`.
- Tạo tài khoản Admin và Enterprise mẫu để kiểm thử.
- Các tính năng như gửi email và video call cần cấu hình thêm (JavaMail, WebRTC) để hoạt động đầy đủ.
- Hình ảnh trong mục **Giao Diện Minh Họa** hiện là placeholder. Thay thế bằng hình ảnh thực tế của JobC để minh họa tốt hơn.

---

<p align="center">
  <strong>JobC</strong> – Cầu nối giữa ứng viên và nhà tuyển dụng, hiệu quả và hiện đại!
</p>
<p align="center">
  theanhntp@gmail.com
</p>
