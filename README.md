# phubon-locketgold

Locket Gold full: cấu hình video có âm thanh đến 30 giây, caption, bộ lọc, QR, người xem và lựa chọn gửi cho chính mình.

Bộ cài gọn từ bản Full 1.4.1 đang dùng của Phú Bôn. Ngày hiển thị Gold: **01/11/2005**, múi giờ Việt Nam.

## Link cài Shadowrocket

https://raw.githubusercontent.com/fub0ln/phubon-locketgold/main/PhuBon.module

## Năm tệp trong kho

| Tệp | Vai trò |
| --- | --- |
| `PhuBon.module` | Module để nhập vào Shadowrocket; gọi ba script trong chính kho này. |
| `phubon-gold.js` | Xử lý phản hồi Gold và ngày hiển thị; chỉnh ngày tại `SETTINGS.goldSince`. |
| `phubon-request.js` | Xử lý ETag của yêu cầu Locket để phản hồi có thể được cập nhật. |
| `phubon-full-1.4.js` | Bộ cấu hình Full đang dùng, gồm QR, caption, bộ lọc, video/âm thanh và lựa chọn Chỉ mình tôi. |
| `README.md` | Hướng dẫn cài và quản lý bộ cài. |

## Chuyển từ kho cũ

1. Đóng Locket và tạm chọn DNS **Tự động** để ứng dụng nhận dữ liệu mới.
2. Trong Shadowrocket, tắt module Locket cũ, thêm link cài ở trên và chỉ bật module **Phú Bôn - Locket Gold**.
3. Giữ chứng chỉ Shadowrocket đã cài, bật kết nối rồi mở Locket. Kiểm tra ngày Gold, QR, đăng bài, người xem, video có tiếng và lựa chọn Chỉ mình tôi.
4. Sau khi kiểm tra, đóng Locket, tắt VPN và chọn lại DNS **Phú Bôn – Locket DNS** đã cài. Cấu hình DNS riêng tiếp tục dùng như trước.

Khi đăng riêng tư, kiểm tra người nhận chỉ là chính mình trước khi gửi. Các tên và vị trí nút phụ thuộc phiên bản Locket.

## Đổi ngày hiển thị

Sửa `SETTINGS.goldSince` trong `phubon-gold.js`, dùng dạng `YYYY-MM-DDT00:00:00+07:00`. Sau khi sửa, đổi giá trị `?v=` của đường dẫn script Gold trong `PhuBon.module`, cập nhật module trên điện thoại rồi nạp lại theo trình tự trên.

## Nguồn và giới hạn

Chép từ [phubon-locket tại commit b6451ed](https://github.com/fub0ln/phubon-locket/tree/b6451ed208c479849ab7e9fd75c7bce8d3739745). Ba script được giữ nguyên nội dung; module chỉ đổi tên hiển thị, mô tả và đường dẫn sang kho này. Các ghi nhận tác giả trong bộ caption gốc được giữ lại.

Kho `phubon-locket` được giữ nguyên để lưu các bản trước và các tệp kiểm tra. Bản này chạy độc lập bằng các tệp trong `phubon-locketgold`.

Phần Gold xử lý phản hồi trên thiết bị, không ghi nhận một giao dịch mua với Apple. Các cờ và hạn mức hiển thị không thay đổi quyền mà máy chủ áp dụng; hiệu quả duy trì khi dùng DNS phụ thuộc cơ chế kiểm tra của ứng dụng.
