# 왜관선교교회 웹사이트 · Waegwan Mission Church website

Trang web tĩnh (không cần build). / 정적 웹사이트(빌드 불필요).

```
index.html            ← toàn bộ trang web / 웹사이트 전체
sermon/current.html   ← BÀI GIẢNG TUẦN NÀY / 이번 주 강단 말씀  (thay file này mỗi tuần)
vercel.json           ← cấu hình Vercel / Vercel 설정
```

## 1. Đưa lên GitHub và Vercel (làm một lần)
1. GitHub → **New repository** (ví dụ `waegwan-church`) → **Add file → Upload files**,
   kéo thả `index.html`, `vercel.json`, `README.md` và thư mục `sermon` → **Commit changes**.
2. vercel.com → **Add New… → Project** → chọn repository vừa tạo → **Import**.
3. Framework Preset: **Other**. Build Command: để trống. Output Directory: để trống (hoặc `.`). → **Deploy**.
4. Vài chục giây sau bạn nhận địa chỉ dạng `ten-du-an.vercel.app`.
   Muốn tên miền riêng: Project → Settings → Domains.

## 2. Cập nhật bài giảng mỗi tuần (không cần sửa mã)
1. Tạo file bài giảng mới như mọi tuần (file `이번주강단말씀.html`).
2. GitHub → vào thư mục **sermon** → **Add file → Upload files**.
3. Tải file mới lên với tên **`current.html`** (đổi tên file trước khi tải) → **Commit changes**.
   - Cùng tên với file cũ nên file cũ được thay thế.
   - Nếu để nguyên tên `이번주강단말씀.html`, hãy xóa `current.html` cũ để tránh nhầm
     (trang ưu tiên `current.html`, sau đó mới tìm `이번주강단말씀.html`).
4. Vercel tự triển khai lại (30–60 giây). Mở trang web → mục **Bài giảng** tự hiện bài mới:
   tiêu đề, dàn ý, 9 ngôn ngữ và câu Kinh Thánh bấm xem được.
   Khách đang mở trang chỉ cần tải lại trang (F5).

Mẹo: muốn lưu bài cũ, hãy chép bản cũ vào `sermon/archive/2026-11-08.html` trước khi thay.

## 3. Giới hạn cần biết
- Trang bài giảng tuần hỗ trợ: ko, en, vi, zh, ja, km, id, si, bn. Khi khách chọn tiếng **Nepal**, mục này hiện tiếng Anh.
- Địa chỉ câu chỉ có số chương (ví dụ 행 13장) mà file không kèm nội dung sẽ hiện "đang chuẩn bị".
- Nếu file mới bị lỗi hoặc không tải được, trang tự dùng bản bài giảng đã đóng gói sẵn trong index.html (không bị trống).
