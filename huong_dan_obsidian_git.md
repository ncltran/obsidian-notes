# Hướng dẫn Thiết lập Obsidian Git để Đồng bộ Ghi chú với GitHub

> Ngày tạo: 2025-06-04

## ✅ Mục tiêu

Biến Obsidian thành một hệ thống ghi chú **tự động đồng bộ** và **lưu trữ an toàn** bằng GitHub.

---

## 🧩 Bước 1: Cài Git cho máy tính

1. Tải Git tại: https://git-scm.com/
2. Cài đặt và để mặc định mọi tùy chọn (Next → Next → Finish)
3. Mở Git Bash kiểm tra bằng lệnh:
   ```bash
   git --version
   ```

---

## 📂 Bước 2: Tạo Git Repository trên GitHub

1. Truy cập: https://github.com/new
2. Đặt tên ví dụ: `obsidian-notes`
3. Chọn Public hoặc Private tùy ý → Nhấn "Create repository"

---

## 🔁 Bước 3: Kết nối Vault Obsidian với GitHub

1. Mở thư mục Vault trong máy tính (ví dụ: `D:\Obsidian\Notes`)
2. Chuột phải chọn `Git Bash Here`
3. Gõ lệnh:
   ```bash
   git init
   git remote add origin https://github.com/<tên_user>/<tên_repo>.git
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git push -u origin main
   ```

4. Nếu lỗi “Author identity unknown” thì chạy lệnh:
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "your@email.com"
   ```

---

## 🔌 Bước 4: Cài plugin Obsidian Git

1. Mở Obsidian → `Settings → Community Plugins`
2. Tắt `Safe mode`
3. Nhấn `Browse` → tìm: `Obsidian Git`
4. Nhấn `Install` → `Enable`

---

## ⚙️ Bước 5: Cấu hình plugin Obsidian Git

Vào `Settings → Obsidian Git`, thiết lập:

- ✅ Auto pull on vault open: **Bật**
- ✅ Auto pull interval: **5** phút
- ✅ Auto commit: **Bật**
- ✅ Auto push: **Bật**
- ✅ Auto pull: **Bật**
- 📝 Commit message: `update: {date}`

---

## 🧪 Kiểm tra hoạt động

1. Tạo ghi chú mới trong Obsidian
2. Chờ vài phút hoặc `Ctrl + P` → `Git: Commit and push`
3. Vào GitHub repo kiểm tra file mới

---

## 🎯 Lợi ích

- Tự động backup & đồng bộ giữa các máy
- Có lịch sử ghi chú (quay lại phiên bản cũ)
- Miễn phí, bảo mật, chuyên nghiệp

---

## 🤝 Tác giả hướng dẫn

Trân 

