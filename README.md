# 📱 Group 9 - Hệ Thống Quản Lý Lý Lịch Thiết Bị & Bảo Trì Nhà Máy

Chào mừng bạn đến với kho lưu trữ mã nguồn của **Group 9**. Dự án **Hệ Thống Quản Lý Lý Lịch Thiết Bị & Bảo Trì Nhà Máy** là giải pháp toàn diện hỗ trợ theo dõi hồ sơ thiết bị, lịch trình bảo trì định kỳ, ghi nhận và xử lý sự cố tức thì trong môi trường nhà máy / phân xưởng sản xuất.

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

## 🛠️ Công Nghệ Sử Dụng (Technology Stack)

### 1. Mobile Application (Core App)
- **Framework:** [Flutter](https://flutter.dev/) (Dart) — Phát triển ứng dụng di động đa nền tảng (Android / iOS).
- **State Management:** Riverpod.
- **QR Code Scanner:** `mobile_scanner` (decode mã QR thiết bị trong < 1.5s).
- **Digital Signature:** `signature` Canvas SDK (xuất ảnh chữ ký xác nhận bảo trì định dạng PNG).
- **Image Storage & CDN:** Cloudflare (Cloudflare R2 Storage / Cloudflare Images).
- **Offline Storage & Sync:** SQLite (`sqflite`) lưu trữ Local Queue khi mất mạng, tự động đồng bộ dữ liệu khi có kết nối trở lại.

### 2. Backend & Infrastructure
- **BaaS Platform:** [Supabase](https://supabase.com/) / Firebase (PostgreSQL / Firestore NoSQL).
- **Cloud Storage:** Cloudflare R2 / Firebase Storage lưu trữ ảnh hiện trường sự cố và ảnh chữ ký.
- **Security:** Row-Level Security (RLS) / Security Rules phân quyền theo từng phân xưởng (`workshop_id`).
- **Realtime & Cloud Functions:** Database Triggers, Cloud Functions.
- **Push Notification:** Firebase Cloud Messaging (FCM) thông báo sự cố tức thì đến kỹ thuật viên.

### 3. Web Mobile Demo
- **Framework:** Next.js 16 (App Router) + TypeScript + Tailwind CSS v4 + shadcn/ui (dùng cho bản trải nghiệm giao diện Web di động tại thư mục `ui/`).

---

## 🚀 Hướng Dẫn Cài Đặt Và Chạy Ứng Dụng (Installation & Setup Guide)

### 4.1. Chạy Ứng Dụng Di Động Flutter (Flutter Mobile App)

**Yêu cầu tiền đề:**
- [Flutter SDK](https://docs.flutter.dev/get-started/install) (≥ 3.19.0)
- Android Studio / Xcode / VS Code (đã cài extension Flutter & Dart)
- Thiết bị thật hoặc Emulator / Simulator (Android / iOS)

**Các bước thực hiện:**
```bash
# 1. Di chuyển vào thư mục dự án Flutter gốc
cd project

# 2. Tải các gói thư viện phụ thuộc (Dependencies)
flutter pub get

# 3. Kiểm tra thiết bị sẵn sàng
flutter devices

# 4. Chạy ứng dụng trên thiết bị di động
flutter run
```

---

### 4.2. Chạy Bản Trải Nghiệm Giao Diện Web Mobile (Next.js Demo)

**Yêu cầu tiền đề:**
- Node.js (≥ 18.x)
- npm (≥ 9.x)

**Các bước thực hiện:**
```bash
# 1. Di chuyển vào thư mục giao diện UI
cd ui

# 2. Cài đặt các gói npm
npm install

# 3. Khởi động Server phát triển (Dev Server)
npm run dev
```
> Trình duyệt tự động mở tại đường dẫn: `http://localhost:3000`

---

## 📚 Tài Liệu Thiết Kế Chi Tiết (Project Documentation)

- **Tóm tắt Quản lý Dự án:** `overview.md`
- **Đặc tả Thiết kế SAD (System Architecture Document):** `system_design.md`
- **Thiết kế CSDL & Tập lệnh SQL:** `database_schema.md`
- **Thiết kế Giao diện UI/UX:** `design.md`

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
