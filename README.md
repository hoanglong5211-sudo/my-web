# Quản Lý Sản Xuất Cửa Nhôm Kính

Web quản lý đơn hàng và tiến độ sản xuất cho xưởng cửa nhôm kính. Dữ liệu được đồng bộ thời gian thực qua Firebase Firestore (collection `orders`), mọi người cùng mở web sẽ thấy cập nhật ngay.

## Tính năng

- **Đơn hàng nhiều hạng mục**: loại sản phẩm (cửa đi, cửa sổ, cửa lùa, vách kính...), hệ nhôm (Xingfa, Việt Pháp, PMA...), loại kính, kích thước Rộng × Cao (mm), số lượng, đơn giá/m².
- **Tự động tính** diện tích (m²), thành tiền, tổng đơn, tiền cọc và số còn phải thu.
- **Bảng công đoạn**: Đo đạc - Thiết kế → Cắt nhôm → Gia công - Lắp ráp → Lắp kính → Lắp đặt → Hoàn thành. Có nút chuyển tới/lùi và lưu lịch sử thời gian từng công đoạn.
- **Cảnh báo trễ hạn** khi quá ngày giao mà chưa hoàn thành.
- **Thống kê**: tổng đơn, đơn đang sản xuất, đơn trễ hạn, diện tích đang sản xuất, tổng giá trị, công nợ.
- **Tìm kiếm** theo mã đơn, tên khách, SĐT, địa chỉ; lọc đơn trễ hạn.
- **In lệnh sản xuất** cho xưởng (kèm ước tính chiều dài nhôm khung bao và ô ký tên).

## Sử dụng

Mở `index.html` trên trình duyệt hoặc deploy lên GitHub Pages / Firebase Hosting.

Firestore Rules cần cho phép đọc/ghi collection `orders`. Lưu ý: nếu rules đang mở cho tất cả mọi người, bất kỳ ai có link đều sửa/xóa được dữ liệu. Nên bật Firebase Authentication khi dùng thật.
