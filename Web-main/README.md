﻿# My Laravel Project
 #Sprint 3 : 09/09/2025
#Module 2 : Building Web Applications with Laravel

Nội dung chính: Routing, Controllers, Views, Database Migrations, Eloquent ORM, Middleware, Authentication, Blade Templating System.

#User Story 5: Routing in Laravel

Route: Định nghĩa URL và liên kết với hành động xử lý (callback hoặc controller method).

Hỗ trợ nhiều HTTP methods: GET, POST, …

Giúp tổ chức ứng dụng theo mô hình MVC rõ ràng và có cấu trúc.

Trong khóa học sẽ học cách:

Định nghĩa route đơn giản (closure hoặc view).

Truyền tham số động vào route.

Gắn route với controller method.

Tạo route có tên để tiện generate URL.

#User Story 6: Controllers in Laravel

Controller: Lớp trung gian xử lý request → gọi logic nghiệp vụ (model/service) → trả về view hoặc dữ liệu (JSON, redirect).

Có thể tổ chức theo:

Multi-action controller (nhiều action trong một controller).

Resource controller (chuẩn RESTful).

Best practices:

Giữ controller nhẹ (thin controller).

Đưa logic phức tạp vào service/lớp riêng để dễ test & bảo trì.

Tích hợp với middleware, authorization, validation để tăng tính bảo mật và kiểm soát request.

#User Story 7: Views in Laravel

View: Nơi hiển thị dữ liệu cho người dùng (thường là file Blade).

Controller truyền dữ liệu từ backend sang View.

Blade Template Engine giúp:

Tái sử dụng layout.

Sử dụng directive tiện lợi.

In biến an toàn & dễ quản lý giao diện.

