# 📱 Group 9 - Hệ Thống Quản Lý Lý Lịch Thiết Bị & Bảo Trì Nhà Máy

Chào mừng bạn đến với kho lưu trữ mã nguồn của **Group 9**. Dự án **Hệ Thống Quản Lý Lý Lịch Thiết Bị & Bảo Trì Nhà Máy** là ứng dụng di động được phát triển bằng **Flutter & Dart** nhằm hỗ trợ theo dõi hồ sơ thiết bị, lịch trình bảo trì định kỳ, ghi nhận sự cố và quản lý vận hành thiết bị trong môi trường nhà máy / xí nghiệp.

---

## 👥 Danh Sách Thành Viên & Phân Công Nhiệm Vụ

| STT | Họ và Tên | Mã Sinh Viên | Vai Trò | Nhiệm Vụ Phụ Trách |
| :---: | :--- | :---: | :---: | :--- |
| 1 | **Phạm Văn Hùng** | **2351170598** | Thành viên / Core Dev | Cấu hình dự án, kiến trúc ứng dụng & kết nối chức năng cốt lõi |
| 2 | **Trịnh Trung Kiên** | **2251172396** | Thành viên / Frontend | Thiết kế UI/UX, màn hình danh mục & hồ sơ lý lịch thiết bị |
| 3 | **Đỗ Việt Tiến** | **2251243452** | Thành viên / Frontend | Thiết kế giao diện lập lịch bảo dưỡng & báo cáo sự cố |
| 4 | **Cao Đức Đạo** | **2351170581** | Thành viên / Backend | Quản lý cơ sở dữ liệu thiết bị, tích hợp API hệ thống |
| 5 | **Trương Tuấn Hải** | **2351170590** | Thành viên / QA | Kiểm thử chức năng (Testing), viết tài liệu & kiểm soát PR |

---

## 🛠️ Công Nghệ & Môi Trường Phát Triển

- **Framework:** [Flutter](https://flutter.dev/) (phiên bản 3.x trở lên)
- **Ngôn ngữ:** [Dart](https://dart.dev/)
- **IDE khuyên dùng:** VS Code / Android Studio (đã cài extension Flutter & Dart)
- **Hệ thống Quản lý Phiên bản:** Git & GitHub

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
1. Khởi chạy thiết bị ảo (Android Emulator) hoặc kết nối thiết bị thật (bật USB Debugging).
2. Chạy lệnh:
   ```bash
   flutter run
   ```
   *(Hoặc trong VS Code: nhấn phím `F5` / chọn `Run Without Debugging`)*

---

## 🌿 Quy Trình Nhánh & Đóng Góp Mã Nguồn (Git Workflow)

Nhóm áp dụng quy trình Git Flow để làm việc nhóm hiệu quả và kiểm soát chất lượng code:

1. **Nhánh chính (`main`):**
   - Chứa mã nguồn ổn định, đã qua kiểm thử và sẵn sàng báo cáo.
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
