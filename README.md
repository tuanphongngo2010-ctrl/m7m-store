# M7M STUDIO – WEBSITE ĐẶT HÀNG & KHẢO SÁT MÓC KHÓA IN 3D

> **Slogan:** "Break Limits – Create Beyond"  
> **Dành riêng cho:** Học sinh THPT Mạc Đĩnh Chi & Các bạn trẻ yêu thích phụ kiện in 3D cá nhân hóa.

---

## 🌟 TÍNH NĂNG NỔI BẬT

1. **Giao diện hiện đại & trẻ trung:**
   - Thiết kế chuẩn Gen Z với tông màu năng động (Indigo - Violet - Cyan), hiển thị tối ưu 100% trên cả Điện thoại di động và Máy tính.
   - Header nhận diện thương hiệu, banner hot trend, nút bấm mượt mà.

2. **Cẩm nang so sánh 2 loại nhựa in 3D:**
   - **Nhựa PLA (Sinh học):** Màu tươi sáng, siêu nhẹ, nét chữ chuẩn, thân thiện môi trường, chịu nhiệt 55-60°C (cho balo, túi tote, góc học tập).
   - **Nhựa PETG (Kỹ thuật):** Chịu lực dẻo dai, chống va đập, kháng nước 100%, chịu nhiệt 75-80°C (cho chìa khóa xe máy/xe đạp điện đi mưa nắng).

3. **Danh mục sản phẩm niêm yết rõ ràng:**
   - Móc khóa Clicky "MDC" (Blue Switch cơ học bấm xả stress): **50.000 VNĐ**
   - Móc khóa thẻ tên "Mạc Đĩnh Chi" (Chữ nổi 3D đa sắc): **40.000 VNĐ**
   - Móc khóa Custom in tên / icon theo yêu cầu: **45.000 VNĐ**

4. **Form đặt hàng & Khảo sát chuẩn Form KTPL / Google Form:**
   - Tích chọn bắt buộc **"Đã đọc và đồng ý với chính sách đổi trả"**.
   - Họ và tên, Lớp, Tên trường THPT, Số điện thoại / Zalo, Địa chỉ nhận hàng (hoặc nhận trực tiếp tại cổng trường MDC).
   - Chọn số lượng từng loại (nếu không mua điền 0), ô nhập nội dung in riêng cho mẫu custom.
   - Chọn chất liệu nhựa (Radio PLA / PETG), chọn loại khoen (khoen tròn inox, móc càng cua, dây bi), chọn tông màu phối.
   - Tính tổng tiền và tổng số lượng theo thời gian thực (Live Price Calculation).
   - Đánh giá sao (1-5 sao) & câu hỏi khảo sát nhu cầu sản phẩm tiếp theo.
   - Hiệu ứng pháo hoa chúc mừng (Confetti) & Modal tóm tắt thông tin đơn hàng sau khi gửi.

5. **Accordion chính sách minh bạch:**
   - Hỗ trợ đổi mới 1-1 hoặc hoàn tiền trong **3 – 7 ngày**.
   - Quy định trường hợp được đổi trả, không áp dụng đổi trả, điều kiện video unbox liền mạch và quy trình giải quyết trong **24 giờ**.
   - Hướng dẫn chi tiết cách bảo quản móc khóa PLA và PETG.

6. **Trang Quản Trị (Admin Portal) Đầy Đủ & Bảo Mật:**
   - Đăng nhập bảo vệ bằng mật khẩu: **`M7M2026`**.
   - Thống kê thời gian thực (KPI): Tổng số đơn, Tổng doanh thu dự kiến, Tỷ lệ chất liệu PLA vs PETG, Điểm đánh giá trung bình.
   - Tìm kiếm đơn hàng theo tên, SĐT, lớp/trường; bộ lọc theo chất liệu và trạng thái (Chờ xác nhận, Đang in 3D, Đang giao, Đã hoàn thành, Đã hủy).
   - Đổi trạng thái đơn hàng trực tiếp trên bảng.
   - Xem chi tiết từng đơn hàng, xóa đơn, thêm đơn hàng mẫu thử nghiệm.
   - **Xuất dữ liệu 1-click:**
     * **Xuất file Excel (.xlsx):** Đầy đủ các cột chuẩn hóa tiếng Việt có dấu, định dạng đẹp mắt với thư viện SheetJS.
     * **Xuất file CSV:** Lưu trữ nhanh.
   - **Tích hợp Webhook Google Sheets:** Cho phép cấu hình Google Apps Script Webhook để tự động đẩy dữ liệu sang Google Sheets.

---

## 🚀 HƯỚNG DẪN MỞ VÀ SỬ DỤNG TRANG WEB

1. **Mở trực tiếp trên máy tính:**
   - Nhấp đúp vào file `index.html` trong thư mục này để mở ngay trên trình duyệt (Chrome, Edge, Cốc Cốc, Safari...).
   - Không cần cài đặt Node.js hay phần mềm phụ trợ.

2. **Cách truy cập trang Quản Trị (Admin):**
   - Bấm vào nút **"Quản Trị"** ở góc trên thanh Menu (Header) hoặc cuối chân trang (Footer).
   - Nhập mật khẩu: **`M7M2026`** -> Bấm **Đăng Nhập**.

3. **Hướng dẫn kết nối Google Sheets (Tùy chọn nâng cao):**
   Nếu bạn muốn mỗi khi khách gửi đơn hàng, dữ liệu tự động ghi vào 1 dòng trong Google Sheets:
   - Mở Google Sheets mới -> Chọn **Tiện ích mở rộng** (Extensions) -> **Apps Script**.
   - Dán đoạn code sau vào:
   ```javascript
   function doPost(e) {
     var sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
     var data = JSON.parse(e.postData.contents);
     
     // Thêm dòng mới vào Google Sheets
     sheet.appendRow([
       data.id,
       data.createdAt,
       data.fullName,
       data.phone,
       data.studentClass,
       data.schoolName,
       data.shippingAddress,
       data.qtyClicky,
       data.qtyClassic,
       data.qtyCustom,
       data.customText,
       data.material,
       data.keyringType,
       data.preferredColor,
       data.totalQty,
       data.totalPrice,
       data.orderNote,
       data.surveyRating,
       data.surveyFeedback,
       data.status
     ]);
     
     return ContentService.createTextOutput("Success").setMimeType(ContentService.MimeType.TEXT);
   }
   ```
   - Bấm **Triển khai** (Deploy) -> **Tùy chọn triển khai mới** (New Deployment) -> Chọn loại **Ứng dụng web** (Web app) -> Ai có quyền truy cập: **Bất kỳ ai (Anyone)**.
   - Sao chép liên kết URL Webhook nhận được.
   - Mở Admin Dashboard trên web M7M -> Dán URL vào ô **"Kết Nối Google Sheets Webhook"** -> Bấm **Lưu**. Xong!
