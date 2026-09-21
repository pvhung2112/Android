# 📱 Group 9 - Dự Án Phát Triển Ứng Dụng Di Động Android

Chào mừng bạn đến với kho lưu trữ mã nguồn của **Group 9**. Dự án này được phát triển trong khuôn khổ môn học Lập trình Thiết bị Di động (Android).

---

## 👥 Danh Sách Thành Viên & Phân Công Nhiệm Vụ

| STT | Họ và Tên | Mã Sinh Viên | Vai Trò | Nhiệm Vụ Phụ Trách | GitHub Username |
| :---: | :--- | :---: | :---: | :--- | :--- |
| 1 | **Phạm Văn Hùng** | *Điền MSSV* | **Team Leader / Core Dev** | Quản lý dự án, thiết lập repo, kiến trúc ứng dụng & merge PR | [@pvhung2112](https://github.com/pvhung2112) |
| 2 | *Thành viên 2* | *Điền MSSV* | Frontend Dev | Thiết kế Layout XML, UI/UX, xử lý giao diện người dùng | [@username2](https://github.com/) |
| 3 | *Thành viên 3* | *Điền MSSV* | Backend / Database | Xây dựng cơ sở dữ liệu (Room / SQLite), API Integration | [@username3](https://github.com/) |
| 4 | *Thành viên 4* | *Điền MSSV* | Tester / QA | Viết tài liệu kiểm thử, Test chức năng, Review PR | [@username4](https://github.com/) |

---

## 🛠️ Công Nghệ & Môi Trường Phát Triển

- **Ngôn ngữ lập trình:** Java / Kotlin
- **IDE khuyên dùng:** Android Studio (phiên bản Iguana / Jellyfish trở lên)
- **Hệ thống Build:** Gradle (Kotlin DSL hoặc Groovy DSL)
- **Target SDK:** 34 | **Min SDK:** 24
- **Quản lý phiên bản:** Git & GitHub

---

## 🚀 Hướng Dẫn Cài Đặt & Chạy Dự Án

### 1. Yêu cầu tiên quyết
- Cài đặt [Android Studio](https://developer.android.com/studio) và JDK 17+.
- Đã cấu hình biến môi trường `ANDROID_HOME`.

### 2. Clone mã nguồn về máy
Mở terminal / CMD / Git Bash và chạy lệnh:
```bash
git clone https://github.com/pvhung2112/Android.git
cd Android
```

### 3. Mở dự án trên Android Studio
1. Khởi động Android Studio.
2. Chọn **Open** -> Điều hướng đến thư mục dự án vừa clone.
3. Chờ Android Studio đồng bộ các dependency qua Gradle (`Gradle Sync`).

### 4. Chạy ứng dụng
1. Khởi chạy thiết bị ảo (Android Emulator) hoặc kết nối thiết bị thật (bật chế độ *USB Debugging*).
2. Nhấn nút **Run** (biểu tượng ▶️ màu xanh) hoặc tổ hợp phím `Shift + F10` để build và cài đặt ứng dụng.

---

## 🌿 Quy Trình Nhánh & Đóng Góp Mã Nguồn (Git Workflow)

Để đảm bảo chất lượng mã nguồn và tránh xung đột code khi làm việc nhóm, nhóm áp dụng quy trình Git Flow như sau:

1. **Nhánh chính (`main`):**
   - Chỉ chứa code ổn định, đã qua kiểm thử và sẵn sàng phát hành.
   - **Không được phép commit trực tiếp lên `main`**.

2. **Nhánh phát triển (`develop`):**
   - Nhánh tập hợp code từ các tính năng đang phát triển.

3. **Nhánh tính năng (`feature/...` hoặc `bugfix/...`):**
   - Mỗi thành viên khi làm tính năng mới sẽ tách nhánh từ `develop`:
     ```bash
     git checkout develop
     git pull origin develop
     git checkout -b feature/ten-tinh-nang
     ```

4. **Tạo Pull Request (PR):**
   - Sau khi hoàn thành và commit code:
     ```bash
     git push origin feature/ten-tinh-nang
     ```
   - Lên GitHub tạo Pull Request từ nhánh `feature/ten-tinh-nang` vào nhánh `develop` (hoặc `main`).
   - Cần ít nhất **1 thành viên khác review** code trước khi được phép Merge.
