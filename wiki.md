Nội dung đã thực hiện:

Tìm hiểu tổng quan về Laravel Framework, một framework PHP mã nguồn mở, mạnh mẽ và phổ biến trong phát triển web hiện đại.

Phân tích ưu điểm của Laravel:

Cấu trúc MVC rõ ràng, dễ bảo trì.

Hệ thống Routing, Middleware, và Blade Template tiện lợi.

Hỗ trợ ORM (Eloquent) giúp thao tác CSDL dễ dàng.

Tích hợp sẵn Authentication, Validation, Migration, giảm công sức lập trình.

So sánh Laravel với các framework PHP khác (như CodeIgniter, Symfony) để thấy rõ lợi thế về cú pháp và cộng đồng hỗ trợ.

Kết quả:
✔️ Nắm vững khái niệm, vai trò và các tính năng nổi bật của Laravel trong lập trình web.
✔️ Chuẩn bị nền tảng lý thuyết cho các bước cài đặt và xây dựng ứng dụng ở module tiếp theo.

🔹 1.7 Cài đặt môi trường phát triển Laravel

Nội dung đã thực hiện:

Cài đặt các công cụ cần thiết:

XAMPP / Laragon – để chạy server PHP và MySQL.

Composer – trình quản lý thư viện PHP.

Node.js + NPM – để quản lý gói frontend.

Cài đặt Laravel bằng lệnh:

composer create-project laravel/laravel example-app


Kiểm tra hoạt động ứng dụng với lệnh:

php artisan serve


→ Truy cập địa chỉ http://127.0.0.1:8000 thành công.

Kết quả:
✔️ Môi trường Laravel hoạt động ổn định.
✔️ Mỗi thành viên trong nhóm đều thiết lập thành công môi trường phát triển trên máy cá nhân.

🔹 1.8 Cấu trúc code Laravel

Nội dung đã thực hiện:

Tìm hiểu cấu trúc thư mục chính của một dự án Laravel:

app/ – chứa code chính của ứng dụng (Models, Http, Console, …)

routes/ – định nghĩa các route web, API, console.

resources/ – chứa file view (Blade), CSS, JS.

database/ – chứa migration, seeders, factories.

public/ – nơi đặt file tĩnh (CSS, JS, ảnh).

config/ – các file cấu hình hệ thống.

Phân tích luồng xử lý request trong Laravel:
Route → Controller → Model → View

Thực hành tạo một route đơn giản hiển thị “Hello Laravel!” để minh họa hoạt động.

Kết quả:
✔️ Hiểu rõ cấu trúc thư mục và vai trò của từng phần trong framework Laravel.
✔️ Thành thạo thao tác cơ bản với route và view.
