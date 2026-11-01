# Lãnh đạo Thế giới

Website tĩnh tra cứu **chức vụ** và **quê quán** của quan chức, lãnh đạo các quốc gia. Giai đoạn đầu: **Việt Nam** (Bộ Chính trị khóa XIV, Ban Bí thư, Nhà nước, Chính phủ và lãnh đạo Quốc hội nhiệm kỳ 2026–2031).

## Tính năng
- Tìm kiếm không dấu theo tên, chức vụ, quê quán
- Lọc theo cơ quan (Bộ Chính trị, Ban Bí thư, Nhà nước, Chính phủ, Quốc hội, Tư pháp) và theo tỉnh/thành
- Thống kê lãnh đạo theo quê quán
- Quê quán hiển thị kèm tỉnh/thành cũ trước sáp nhập 2025 (trường `oldProvince`)
- Quiz trắc nghiệm (`quiz.html`): quê quán, tỉnh cũ, chức vụ, "ai là ai", đồng hương
- Giao diện sáng/tối, dùng tốt trên điện thoại

## Cấu trúc
```
index.html      # giao diện
data/vn.js      # dữ liệu Việt Nam
```

## Thêm quốc gia mới
1. Tạo `data/<mã>.js` theo mẫu `data/vn.js` (`window.LEADERS.<mã> = {...}`).
2. Thêm `<script src="data/<mã>.js"></script>` vào `index.html`.
3. Đặt `ready: true` cho quốc gia đó trong mảng `COUNTRIES`.

## Nguyên tắc dữ liệu
- Chỉ ghi thông tin công khai từ nguồn chính thống (báo Đảng, Cổng TTĐT Chính phủ, báo chí lớn); danh sách nguồn ở cuối trang.
- Trường nào chưa xác minh được thì để trống (hiển thị “Chưa cập nhật”), không điền theo suy đoán.
- Quê quán ghi theo đơn vị hành chính sau sắp xếp năm 2025.

Chạy thử: mở trực tiếp `index.html` hoặc `python3 -m http.server`.
