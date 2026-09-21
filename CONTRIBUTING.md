# 📋 Quy Định Đóng Góp & Quy Trình Pull Request (Group 9)

Tài liệu này hướng dẫn các thành viên trong **Group 9** cách phối hợp làm việc và tạo Pull Request (PR) chuẩn trên kho lưu trữ.

---

## 1. Quy Tắc Đặt Tên Nhánh (Branch Naming)

Khi nhận một nhiệm vụ mới, thành viên tạo nhánh mới từ nhánh `develop`:
- Nhánh tính năng: `feature/<ten-tinh-nang>` (Ví dụ: `feature/login-ui`, `feature/sqlite-db`)
- Nhánh sửa lỗi: `bugfix/<ten-loi>` (Ví dụ: `bugfix/crash-on-backpress`)
- Nhánh tài liệu: `docs/<noi-dung>` (Ví dụ: `docs/update-readme`)

```bash
git checkout develop
git pull origin develop
git checkout -b feature/login-ui
```

---

## 2. Quy Chuẩn Commit Message

Sử dụng tiền tố rõ ràng theo chuẩn Conventional Commits:
- `feat:` Thêm tính năng mới
- `fix:` Sửa lỗi
- `docs:` Chỉnh sửa tài liệu, README
- `style:` Định dạng code, giao diện XML
- `refactor:` Tái cấu trúc code mà không đổi logic
- `chore:` Cấu hình Gradle, thư viện

Ví dụ: `git commit -m "feat: thiet ke man hinh dang nhap XML"`

---

## 3. Quy Trình Tạo & Duyệt Pull Request (PR)

1. **Đẩy nhánh lên GitHub:**
   ```bash
   git push origin feature/login-ui
   ```
2. **Tạo Pull Request trên GitHub:**
   - Base branch: `develop` (hoặc `main`)
   - Compare branch: `feature/<ten-tinh-nang>`
   - Đặt tiêu đề rõ ràng: `[Feature] Thiết kế màn hình đăng nhập`
   - Ghi mô tả: Tóm tắt những gì đã làm, ảnh chụp màn hình (nếu có).
3. **Review và Hợp nhất (Merge):**
   - Tag ít nhất **1 thành viên khác** để review code.
   - Khi không còn lỗi và code đã được phê duyệt (Approve), tiến hành **Squash and merge** hoặc **Merge pull request**.
