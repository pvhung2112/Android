# 📱 Group 9 - Dự Án Phát Triển Ứng Dụng Với Flutter

Chào mừng bạn đến với kho lưu trữ mã nguồn của **Group 9**. Dự án này được phát triển bằng **Flutter & Dart** trong khuôn khổ môn học Phát triển Ứng dụng Di động.

---

## 👥 Danh Sách Thành Viên & Phân Công Nhiệm Vụ

| STT | Họ và Tên | Mã Sinh Viên | Vai Trò | Nhiệm Vụ Phụ Trách | GitHub Username |
| :---: | :--- | :---: | :---: | :--- | :--- |
| 1 | **Phạm Văn Hùng** | *Điền MSSV* | **Team Leader / Core Dev** | Quản lý dự án, cấu hình hệ thống, kiến trúc ứng dụng & merge PR | [@pvhung2112](https://github.com/pvhung2112) |
| 2 | *Thành viên 2* | *Điền MSSV* | Frontend Dev | Thiết kế UI/UX Widgets, Xử lý giao diện màn hình Flutter | [@username2](https://github.com/) |
| 3 | *Thành viên 3* | *Điền MSSV* | Backend / State Management | Quản lý trạng thái (Provider/Bloc), Tích hợp REST API / Firebase | [@username3](https://github.com/) |
| 4 | *Thành viên 4* | *Điền MSSV* | Tester / QA | Viết tài liệu kiểm thử, Test chức năng trên thiết bị/máy ảo, Review PR | [@username4](https://github.com/) |

---

## 🛠️ Công Nghệ & Môi Trường Phát Triển

- **Framework:** [Flutter](https://flutter.dev/) (phiên bản 3.x trở lên)
- **Ngôn ngữ:** [Dart](https://dart.dev/)
- **IDE khuyên dùng:** VS Code / Android Studio (đã cài extension Flutter & Dart)
- **Quản lý phiên bản:** Git & GitHub

---

## 🚀 Hướng Dẫn Cài Đặt & Chạy Dự Án

### 1. Yêu cầu tiên quyết
- Đã cài đặt [Flutter SDK](https://docs.flutter.dev/get-started/install) và cấu hình biến môi trường PATH.
- Đã cài đặt VS Code hoặc Android Studio.
- Đã kiểm tra môi trường bằng lệnh:
  ```bash
  flutter doctor
  ```

### 2. Clone mã nguồn về máy
Mở terminal / CMD / Git Bash và chạy lệnh:
```bash
git clone https://github.com/pvhung2112/Android.git
cd Android
```

### 3. Cài đặt các gói phụ thuộc (Dependencies)
```bash
flutter pub get
```

### 4. Chạy ứng dụng
1. Khởi chạy thiết bị ảo (Android Emulator / iOS Simulator) hoặc kết nối thiết bị thật (bật USB Debugging).
2. Chạy lệnh:
   ```bash
   flutter run
   ```
   *(Hoặc trong VS Code: nhấn phím `F5` / chọn `Run Without Debugging`)*

---

## 🌿 Quy Trình Nhánh & Đóng Góp Mã Nguồn (Git Workflow)

Nhóm áp dụng quy trình Git Flow để làm việc nhóm hiệu quả và tránh xung đột code:

1. **Nhánh chính (`main`):**
   - Chỉ chứa code hoàn chỉnh, đã kiểm thử và sẵn sàng báo cáo/phát hành.
   - **Không commit trực tiếp lên `main`**.

2. **Nhánh phát triển (`develop`):**
   - Nhánh tích hợp các tính năng mới từ các thành viên.

3. **Nhánh tính năng (`feature/...` hoặc `bugfix/...`):**
   - Mỗi thành viên khi làm tính năng mới sẽ tách nhánh từ `develop`:
     ```bash
     git checkout develop
     git pull origin develop
     git checkout -b feature/ten-tinh-nang
     ```

4. **Tạo Pull Request (PR):**
   - Đẩy nhánh tính năng lên GitHub:
     ```bash
     git push origin feature/ten-tinh-nang
     ```
   - Tạo Pull Request từ nhánh `feature/...` vào nhánh `develop` (hoặc `main`).
   - Cần ít nhất **1 thành viên khác review** code trước khi được phép Merge.
