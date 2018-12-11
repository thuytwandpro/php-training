|--- app/
│      |--- Console
│      |--- Exceptions
│      |--- Http
│      │   |--- Controllers/
│                          |--Auth
│                          |--Controller.php
│      │   |--- Middleware
│      │   └──  Kernel.php
│      |--- Providers
|      └--- User.php
|--- bootstrap/
|--- config/
|--- database/
|--- public/
|          |--- ...
|          |--- index.php
|--- resources/
|             |--- assets
|             |--- lang
|             |--- views
|--- routes/
|          |--- api.php
|          |--- console.php
|          |--- web.php
|--- storage/
|--- tests/
|--- vendor/
|--- .env
|--- .env.example
|--- .gitattributes
|--- .gitignore
|--- artisan
|--- composer.json
|--- composer.lock
|--- package.json
|--- phpunit.xml
|--- readme.md
|--- server.php

## Có 3 thư mục chính là app, public và vendor
- `app/`: Thư mục này chứa các file của ứng dụng, chúng ta sẽ làm việc chủ yếu trên thư mục này.
   + `Console`: Chứa các tập tin định nghĩa các câu lệnh trên artisan.
   + `Exception`:  Chứa các tập tin quản lý, điều hướng lỗi.
   + `Http`
     + `Controllers/` : Chứa các controllers của project.
     + `Middleware/`:  Chứa các tập tin lọc và ngăn chặn các requests.
     + `Kernel.php`:  Cấu hình, định nghĩa Middleware.
     + `Providers`: là nơi chứa các class đăng ký (register) các ServiceProvider.
     + User.php: Là model User mà Laravel tự tạo sẵn cho chúng ta.
- `bootstrap`: chứa file app.php, autoload.php là 2 file thiết lập cơ bản để bắt đầu chạy ứng dụng và file cấu hình nạp class tự động. Ngoài ra trong này còn có thư mục cache (dùng để chứa các file cache tối ưu hóa hiệu suất chạy của ứng dụng).
- `config/`: Chứa mọi tập tin cấu hình của Laravel.
- `database/`: Bên trong chứa các folder factories, migration và seed cơ sỡ dữ liệu của ứng dụng. 
   + `migrations`: Chứa các tập tin định nghĩa, khởi tạo và sửa bảng.
   + `seeds`: Chứa các tập tin định nghĩa dữ liệu insert (thêm) vào trong database.
   + `factories`: Chứa các tập tin định nghĩa các cột bảng dữ liệu để tạo ra các dữ liệu ảo.
- `public`: Các file tĩnh như file HTML, CSS, Javascript hay ảnh sẽ được đưa vào thư mục này.
  + index.php: Đây là tệp tin root của Laraver
- `resources`: nơi chứa các template views, asset và các file ngôn ngữ.
- `routes`: Chứa các tập tin định nghĩa các router, xử lý điều hướng router bao gồm: web, api và console
- `storage`: Chứa các tập tin hệ thống cache, session, ...
- `tests`: chứa các file test case kiểm thử của ứng dụng.
- `vendor`: Thư mục này chứa các thư viện và core framework được tải về bởi Composer, ta không nên động chạm hay sửa chưa gì trong thư mục này.

## Ngoài ra, chúng ta cần quan tâm tới các file sau:
- .env: Là tập tin cấu hình chính của laravel như key app, database.
- .env.example: Tệp tin cấu hình mẫu của laravel.
- .gitattributes và .gitignore Git (phần mềm để quản lý sự thay đổi của source code) sử dụng 2 file này để định nghĩa thuộc tính và danh sách các file không theo dõi.
- composer.json: File này chứa danh sách các dependencies (thư viện, framework) sử dụng trong app. Khi bạn chạy câu lệnh composer install hoặc composer update thì file này sẽ là cơ sở để xác định phiên bản nào cần tải về của các thư viện, framework được liệt kê trong file này.
- composer.lock: File này chứa thông tin log lại khi Composer cài đặt hoặc update các dependencies.
- package.json: Tập tin cấu hình của nodejs (chứa các package cần dùng cho projects).
- phpunit.xml: Là tập tin xml của phpunit dùng để testing project.
- server.php: Là tập tin để artisan trỏ đến tạo server khi gõ lệnh `php artisan serve`.
- artisan: File này được dùng để thực thi các lệnh CLI (command line interface) để hỗ trợ phát triển ứng dụng.
