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
Nội dung đã thực hiện:

Tìm hiểu Routing trong Laravel – cơ chế giúp ánh xạ các URL tới logic xử lý cụ thể.

Phân biệt các loại route:

GET, POST, PUT, DELETE, PATCH, …

Thực hành tạo route cơ bản trong file routes/web.php:

Route::get('/', function () {
    return 'Chào mừng đến với Laravel!';
});


Thực hành route có tham số:

Route::get('/user/{id}', function ($id) {
    return "User ID: " . $id;
});


Sử dụng Route name và route group để quản lý code tốt hơn.

Kết quả:
✔️ Hiểu rõ khái niệm, cấu trúc và cách hoạt động của Route trong Laravel.
✔️ Tạo được các route cơ bản và route động, tổ chức nhóm route logic hợp lý.

🔹 2.2 Controllers

Nội dung đã thực hiện:

Tìm hiểu Controller trong Laravel – lớp trung gian xử lý logic giữa Route và View.

Thực hành tạo Controller bằng lệnh Artisan:

php artisan make:controller PageController


Định nghĩa hàm trong Controller, ví dụ:

class PageController extends Controller {
    public function home() {
        return view('home');
    }
}


Kết nối Controller với Route:

Route::get('/home', [PageController::class, 'home']);


Thực hành thêm: tạo Controller tài nguyên (Resource Controller) để xử lý CRUD tự động:

php artisan make:controller ProductController --resource


Kết quả:
✔️ Hiểu rõ vai trò của Controller trong mô hình MVC.
✔️ Thành thạo cách tạo và sử dụng Controller để xử lý logic cho ứng dụng web.

🔹 2.3 View

Nội dung đã thực hiện:

Tìm hiểu View trong Laravel – phần giao diện hiển thị cho người dùng.

Thực hành tạo view bằng Blade template trong thư mục resources/views/.
Ví dụ: file home.blade.php

<!DOCTYPE html>
<html>
<head>
    <title>Trang chủ</title>
</head>
<body>
    <h1>Chào mừng đến với Laravel!</h1>
</body>
</html>


Truyền dữ liệu từ Controller sang View:

public function home() {
    $name = "Nguyễn Văn A";
    return view('home', compact('name'));
}


Trong file home.blade.php:

<h2>Xin chào, {{ $name }}</h2>


Sử dụng Blade directives như:

@if, @foreach, @include, @extends, @section, @yield để tái sử dụng layout.

Kết quả:
✔️ Biết cách tạo, tổ chức và kết nối View với Controller.
✔️ Thành thạo cú pháp Blade Template và tái sử dụng giao diện hiệu quả.
Nội dung đã thực hiện:

Tìm hiểu hệ thống quản lý cơ sở dữ liệu (CSDL) trong Laravel.

Cấu hình kết nối cơ sở dữ liệu trong file .env:

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel_db
DB_USERNAME=root
DB_PASSWORD=


Kiểm tra kết nối và tạo mới database bằng lệnh Artisan:

php artisan migrate


Hiểu rõ cơ chế ORM (Object-Relational Mapping) giúp Laravel làm việc với dữ liệu mà không cần viết câu lệnh SQL trực tiếp.

Kết quả:
✔️ Đã kết nối thành công Laravel với MySQL thông qua file cấu hình .env.
✔️ Sẵn sàng cho việc tạo bảng và thao tác dữ liệu bằng Migration & Eloquent ORM.

🔹 2.4.1 Migration

Nội dung đã thực hiện:

Migration là công cụ giúp quản lý cấu trúc CSDL bằng code.

Thực hành tạo Migration bằng lệnh:

php artisan make:migration create_products_table


Chỉnh sửa file migration trong thư mục database/migrations:

public function up(): void
{
    Schema::create('products', function (Blueprint $table) {
        $table->id();
        $table->string('name');
        $table->integer('price');
        $table->text('description')->nullable();
        $table->timestamps();
    });
}


Chạy migration để tạo bảng:

php artisan migrate


Tìm hiểu thêm các lệnh quản lý migration:

php artisan migrate:rollback (quay lại phiên bản trước)

php artisan migrate:refresh (làm mới toàn bộ bảng)

Kết quả:
✔️ Hiểu rõ vai trò của Migration trong việc kiểm soát phiên bản CSDL.
✔️ Tạo được bảng và quản lý thay đổi cấu trúc CSDL bằng công cụ dòng lệnh Artisan.

🔹 2.4.2 Eloquent ORM

Nội dung đã thực hiện:

Eloquent ORM là hệ thống ánh xạ đối tượng giúp làm việc với CSDL theo hướng đối tượng thay vì viết SQL.

Tạo Model tương ứng với bảng products:

php artisan make:model Product


Sử dụng Model để thao tác dữ liệu:

// Thêm dữ liệu
$product = new Product();
$product->name = 'Laptop ASUS';
$product->price = 15000000;
$product->description = 'Hiệu năng cao, thiết kế đẹp';
$product->save();

// Lấy tất cả dữ liệu
$products = Product::all();

// Tìm kiếm theo ID
$item = Product::find(1);

// Cập nhật dữ liệu
$item->price = 16000000;
$item->save();

// Xóa dữ liệu
$item->delete();


Tìm hiểu thêm về Query Builder và Relationship (quan hệ giữa các bảng: One-to-Many, Many-to-Many).

Kết quả:
✔️ Hiểu cách sử dụng Eloquent ORM để thêm, sửa, xóa, truy xuất dữ liệu từ CSDL.
✔️ Thực hành thành công các thao tác CRUD cơ bản thông qua Model.
