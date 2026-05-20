# ĐIỀU KHIỂN MÁY LẠNH BẰNG GIỌNG NÓI

## 1. Thông tin đề tài và thành viên

- **Tên đề tài:** Điều khiển máy lạnh bằng giọng nói.
- **Sinh viên thực hiện:** Tô Quang Hiếu
- **MSSV:** N23DCCI023
- **Lớp:** D23CQCI01-N

## 2. Mô tả thư mục

Mã nguồn trong kho lưu trữ này là gói WebAssembly lõi được xuất bản từ hệ thống Edge Impulse, bao gồm:

- `browser/`: Chứa mã nguồn phục vụ môi trường trình duyệt web, bao gồm tệp `index.html` (giao diện test tĩnh), mã nhị phân WebAssembly (`.wasm`) và các tệp JavaScript xử lý luồng thuật toán.
- `node/`: Chứa mã nguồn cấu hình để chạy mô hình suy luận trực tiếp trên môi trường Node.js (dành cho các thiết bị như Raspberry Pi hoặc máy chủ cục bộ).

## 3. Các phụ thuộc

Để hệ thống hoạt động chính xác, môi trường triển khai cần đáp ứng các yêu cầu sau:

- **Đối với môi trường Trình duyệt (Browser):** Yêu cầu các trình duyệt web hiện đại (Google Chrome, Microsoft Edge, Firefox, Safari) có hỗ trợ **WebAssembly** và **Web Audio API** để thu thập tín hiệu Microphone.
- **Đối với môi trường Node.js (Tùy chọn):** Yêu cầu cài đặt sẵn Node.js (phiên bản v14.x trở lên).
- **Môi trường máy chủ (Localhost):** Để mở tệp `browser/index.html`, cần có một máy chủ web ảo (như Python http.server, extension Live Server trên VS Code hoặc Web Server for Chrome) do chính sách bảo mật CORS của trình duyệt không cho phép chạy trực tiếp tệp từ ổ cứng (file://).

## 4. Hướng dẫn cài đặt và chạy

### Cách 1: Chạy trực tiếp qua giao diện Web Demo

Đây là cách nhanh nhất để kiểm thử toàn bộ hệ thống (đã bao gồm giao diện người dùng trực quan và code thu tín hiệu Microphone) mà không cần cài đặt môi trường.

1. Truy cập vào đường dẫn Web Demo do Edge Impulse host (hoặc xem trong Phụ lục tiểu luận và cuối file README.md).
2. Nhấn "Allow" để cấp quyền sử dụng Microphone.
3. Đợi trạng thái hiển thị "Listening..." và tiến hành đọc các khẩu lệnh đã huấn luyện ("quang hiếu", "lạnh hơn", "ấm hơn", "tắt").

### Cách 2: Sao chép toàn bộ không gian làm việc

1. Truy cập vào đường dẫn dự án công khai trên nền tảng Edge Impulse được cung cấp trong báo cáo.
2. Điều hướng đến tab Live Classification ở menu bên trái, kích hoạt Microphone để hệ thống thu âm, bóc tách đặc trưng và phân loại trực tiếp trên đám mây của Edge Impulse.
3. Nhấn nút "Clone this project" ở góc phía trên bên phải giao diện. Nền tảng sẽ tự động sao chép nguyên bản 100% toàn bộ không gian làm việc, bộ dữ liệu gốc và các siêu tham số huấn luyện của đề tài sang tài khoản cá nhân một cách độc lập, minh bạch và nhanh chóng.

## 5. Đường Dẫn Truy Cập Dự Án Và Mã Nguồn

**Link dự án Edge Impluse:** https://studio.edgeimpulse.com/public/999199/live
**Link Video demo:** https://drive.google.com/file/d/1QZiPXOtsV_dQ1LbFzVgQZfgQHiukXY3P/view?usp=sharing
**Link giao diện thực nghiệm:** https://smartphone.edgeimpulse.com/classifier.html?
