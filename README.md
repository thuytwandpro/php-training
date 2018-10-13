## Cài đặt môi trường

- [XAMPP](https://www.apachefriends.org/download.html) version mới nhất
- [Composer](https://getcomposer.org/download/)
- [PHPStorm](https://www.jetbrains.com/phpstorm/download/) hoặc [Sublime text](https://www.sublimetext.com/3)
- [MySQL Workbench](https://dev.mysql.com/downloads/workbench/)
- [GIT](https://git-scm.com/downloads)

Chi tiết về GIT xem tại [đây](https://github.com/php-iviettech/php-training/blob/master/GIT.md)

## Giáo trình học Laravel
Laravel 5 Essentials

## Hướng dẫn cài đặt laravel với composer
https://laravel.com/docs/5.6/installation

## Trang tài liệu chính thức của laravel framewok
https://laravel.com/docs/5.6

## Tìm hiểu về cấu hình máy ảo laravel homestead
https://laravel.com/docs/5.6/homestead

## Laravel và các lệnh thường dùng
1. Xem version của laravel
```
php artisan --version
```
2. Copy file .env
```
cp .env.example .env
```
3. Chạy trình cài đặt các gói thư viện
```
composer install
```
4. Tạo mã key cho Laravel app
```
php artisan key:generate
```
5. Tạo bảng cơ sở dữ liệu
```
php artisan migrate
```
6. Rollback cơ sở dữ liệu
```
php artisan migrate:rollback
```
7. Rollback cơ sở dữ liệu và tạo lại cơ sở dữ liệu
```
php artisan migrate:refresh
```
8. Tạo dữ liệu mẫu
```
php artisan db:seed
```
9. Đổi namespace
```
php artisan app:name YourNamespace
```
10.  Tạo model và migration
```
php artisan make:model User --migration
```
11. Tạo lại DB và seed
```
php artisan migrate:refresh --seed
```
12. Xem danh sách tất cả các route có hiệu lực
```
php artisan route:list
```
13. Lệnh tạo ứng dụng laravel
```
composer create-project laravel/laravel --prefer-dist "ten app"
```
14. Xem tất cả các lệnh tạo file được laravel hỗ trợ
```
php artisan make
```

## PHPStorm bật show line bumber
Editor > General > Appearance > Show line number

## PHPStorm tắt auto format code khi paste source
Editor > General > Smart Keys

## PHPStorm chuyển CRLF => LF
Editor > Code Style > Line separator
