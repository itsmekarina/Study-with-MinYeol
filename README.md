# Study with MinYeol

🌐 **Mở website:** [Study with MinYeol](https://itsmekarina.github.io/Study-with-MinYeol/)

Sổ tay ngoại ngữ cá nhân để lưu từ vựng, cụm từ, câu và đoạn trích từ truyện, phim, video hoặc bài học; sau đó ôn tập và tìm lại theo ngữ cảnh.

## Tính năng

- Lưu từ, cụm từ, collocation, câu và đoạn văn cùng nghĩa, ví dụ, ghi chú, chủ đề và trạng thái ôn tập.
- Ghi lại nguồn, tên truyện/phim, tập hoặc chương và URL đang đọc/xem.
- Tìm từ trong kho và xem các câu, ví dụ, đoạn trích liên quan.
- Gộp nội dung trùng, tránh lưu lặp câu/đoạn và ngữ cảnh của từ.
- Tùy chọn tự tách các từ đơn còn thiếu từ câu tiếng Anh đã lưu.
- Gợi ý tên truyện/phim đã dùng; xem danh sách nguồn đọc và thống kê từ/câu đã lưu.
- Đồng bộ dữ liệu qua Google Apps Script và Google Sheets; hỗ trợ sao lưu JSON lên Google Drive khi backend đã bật tính năng sao lưu.
- Giao diện dùng được trên điện thoại và máy tính.

## Mở ứng dụng

Đây là website tĩnh, không cần cài gói hay chạy bước build. Mở `index.html` trực tiếp hoặc triển khai repository bằng GitHub Pages/hosting tĩnh.

## Kết nối Google Apps Script

Ứng dụng cần một Apps Script Web App tương thích API v6 để đồng bộ dữ liệu. Mã backend `Code.gs` được quản lý và triển khai riêng, không nằm trong repository này.

1. Dán mã backend v6 vào dự án Google Apps Script của bạn và kiểm tra Spreadsheet ID.
2. Triển khai dưới dạng **Web app**; chọn tài khoản thực thi phù hợp và cấp quyền truy cập cần thiết.
3. Trong ứng dụng, mở **Cài đặt**. Bản web hiện có URL triển khai mặc định; chỉ nhập URL riêng nếu đang dùng deployment khác.
4. Nếu đã đặt `SECRET` trong `Code.gs`, nhập cùng mã bảo vệ trong phần Cài đặt.
5. Kiểm tra kết nối và lưu thử một mục. Backend cũ có thể báo cần triển khai phiên bản v6 mới.

Khi sửa `Code.gs`, hãy tạo deployment version mới trong Apps Script. URL Web App thường giữ nguyên khi cập nhật deployment hiện có.

> Bảo mật: không commit Spreadsheet ID, mã bảo vệ hoặc dữ liệu cá nhân vào repository công khai. Hãy đặt `SECRET` trong backend và cấu hình cùng mã đó trong ứng dụng nếu cần giới hạn ghi dữ liệu. Không chia sẻ quyền truy cập Google Sheet rộng hơn mức cần thiết.

## Dữ liệu

- Website giữ bản dữ liệu cục bộ trong trình duyệt để dùng và đồng bộ.
- Apps Script có thể lưu từ vựng, hoạt động học tập, dữ liệu IELTS/liên kết và các câu/đoạn Khám phá vào Google Sheets theo cấu hình backend.
- Sao lưu Drive cần quyền Drive và trigger sao lưu đã được thiết lập trong Apps Script.

## Công nghệ

HTML, CSS và JavaScript thuần; Google Apps Script và Google Sheets là backend tùy chọn.
