
# Bài 3 : Khắc phục sự cố rò rỉ thông tin đăng nhập
## **Báo cáo phân tích (IPO)**

- Xác định Input (Dấu hiệu nhiễm), Process (Các bước xử lý), Output (Hệ thống sạch):
   - **Input** (Dấu hiệu nhận biết nhiễm mã độc):

  - Tài khoản cá nhân  liên tục bị đăng nhập bất thường hoặc bị chiếm quyền kiểm soát mặc dù đã đổi mật khẩu trước đó.

  - Nhận được thông báo đăng nhập từ các thiết bị lạ hoặc địa điểm không rõ nguồn gốc.

   - Các phiên đăng nhập trên trình duyệt bị mất hoặc bị đăng xuất đột ngột; token API của các dịch vụ lập trình (GitHub, AWS, Discord Bot) bị khai thác trái phép.

  - **Process** (Quy trình 4 bước cấp cứu hệ thống):

  - Ngắt kết nối mạng ngay lập tức: Ngắt toàn bộ kết nối Wi-Fi/Ethernet để ngăn chặn mã độc truyền tải dữ liệu đánh cắp về máy chủ của kẻ tấn công.

  - Cách ly thiết bị và sao lưu dữ liệu quan trọng. Không thực hiện các giao dịch nhạy cảm hay nhập mật khẩu mới trên máy tính đang bị nhiễm.

  - Thu hồi quyền truy cập (Revoke Tokens & Sessions): Đăng xuất toàn bộ các phiên làm việc đang hoạt động và thu hồi token API, SSH Keys trên các nền tảng từ một thiết bị hoàn toàn sạch khác.

Xử lý triệt để mã độc: Cài lại hệ điều hành (Format và Clean Install Windows/macOS) hoặc sử dụng phần mềm quét mã độc chuyên sâu để loại bỏ hoàn toàn Infostealer ẩn sâu trong hệ thống.

Output (Hệ thống sạch và an toàn):

Máy tính được làm sạch hoàn toàn, không còn tiến trình độc hại ngầm.

Toàn bộ mật khẩu, token API, session cookie cũ bị vô hiệu hóa; các tài khoản được bảo vệ bằng mật khẩu mới và xác thực hai yếu tố (2FA).