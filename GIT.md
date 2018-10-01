## Git là gì
- [Git là gì và các khái niệm cơ bản trong git](https://blog.duyet.net/2015/04/git-va-cac-khai-niem-co-ban.html)
- [Sổ tay về Git](https://learnxinyminutes.com/docs/vi-vn/git-vi/)

## Đăng ký GitHub
- Để đăng ký bạn chỉ cần có một Email và khai báo theo các bước [Join GitHub](https://github.com/join?source=header) để có một tài khoản GitHub

## Cài đặt Git
- Windows: [Download](https://git-scm.com/download/win)
- Linux: [Download](https://git-scm.com/download/linux)
- Mac: [Download](https://git-scm.com/download/mac)

## Cấu hình Git
Thiết lập thông tin cá nhân cho Git: (Sử dụng Git Bash hoặc Terminal để gõ các lệnh sau) **bắt buộc**
```
git config --global user.name "Ten cua ban"
git config --global user.email "Email cua ban"
```

Trường hợp code trên Windows nhưng môi trường thật chạy trên Linux, cần đảm bảo các file phải có line endings kiểu Unix (LF) để chạy đúng.
```
git config --global core.autocrlf false
git config --global core.safecrlf false
```

Hiển thị các tham số thiết lập Git
```
git config --list
```

## Truy cập GitHub qua SSH key
*Giúp thao tác truy cập đến GitHub dễ dàng hơn với xác thực thông qua mã SSH thay vì nhập username và password thủ công.*
1. Tạo mã xác thực SSH (Sử dụng Git Bash hoặc Terminal để gõ các lệnh sau)
```
ssh-keygen
```
Khi nó hỏi Enter passphrase có thể nhấn Enter để trống cái này. Kết thúc lệnh đó thì trong C:\Users\<User name> sẽ có SSH Key cho bạn
gồm có public key là file id_rsa.pub và private key là file: id_rsa

2. Thiết lập SSH public key cho GitHub
Truy cập trang https://github.com/settings/ssh/new
- Mục Title đặt tên tùy ý
- Mục Key thì copy và paste toàn bộ nội dung file id_rsa.pub vào
- Click button Add SSH key

## Khởi tạo git repository từ thư mục source code có sẵn
Gõ lệnh:
```
cd furbook-username
git init
git remote add origin git@github.com:USERNAME/REPOSITORY.git
```

## Clone git repository từ Git về máy tính cá nhân
Gõ lệnh:
```
git clone git@github.com:USERNAME/REPOSITORY.git
cp .env.example .env
composer install
php artisan key:generate
php artisan migrate
php artisan db:seed
```

## Thay đổi remote URLs
1. Xem remote hiện tại
```
git remote -v
```

2. Thay đổi remote's URL từ HTTPS sang SSH
```
git remote set-url origin git@github.com:USERNAME/REPOSITORY.git
```

## Những điều chú ý khi dùng Git
1. Tạo issue để liệt kê các chức năng cần phát triển. Ví dụ có yêu cầu *"Viết chức năng đăng ký user cho hệ thống"* thì tạo issue là
**"[69] Implement user registration feature"**

2. Tạo nhánh để phát triển/ fix bug các chức năng để không ảnh hưởng tới ứng dụng hiện tại đang chạy. Ví dụ: Issue #69, có yêu cầu:
*"Viết chức năng đăng ký user cho hệ thống"* thì có thể chọn một trong các cách đặt tên nhánh bên dưới:
```
feat/daidv/reg_user
69_reg_user
```

3. Viết nội dung commit có ý nghĩa và liên quan tới công việc đang làm.

Ví dụ: Issue #69, có yêu cầu: *"Viết chức năng đăng ký user cho hệ thống"* thì khi commit nên viết message là:
```
Issue #69 Implement user registration feature
refs dev #69 Implement user registration feature
```
Ví dụ: Issue #70, có yêu cầu: *"Fix bug chức năng đăng ký user cho hệ thống"* thì khi commit nên viết message là:
```
Issue #69 Fix bug implement user registration feature
refs bug #69 Fix bug implement user registration feature
```

## TIP
1. Git là gì?
2. Tại sao nên sử dụng Git?
3. Có mấy cách để clone source code từ Git? Nên sử dụng cách nào?
4. Sự khác nhau giữa Local repository và Remote repository ?
5. Sự khác nhau giữa lệnh git commit và git push ?
6. Sự khác nhau giữa lệnh git fetch và git pull?
7. Conflict là gì, làm sao để tránh bị conflict?
8. Dùng lệnh gì để hủy bỏ source code đã commit nhưng chưa push?
9. File .gitignore dùng để làm gì?
10. Giải thích ngắn gọn về git flow? Phân biệt các nhánh master, develop, features, hotfix, release… ?

## Một số câu lệnh GIT thường dùng
1. Xem tất cả branch
```
git branch -a
```

2. Xem tên branch hiện tại
```
git branch
```

3. Xem trạng thái các file có thay đổi
```
git status
```

4. Cập nhật branch ở trạng thái mới nhất
```
git pull
* Nếu dưới local có một số file đang có sự thay đổi thì nhiều khi ko thể cập nhật được,
hãy hủy bỏ hoặc lưu lại những sự thay đổi đó trước khi git pull
```

5. Checkout một nhánh cụ thể
```
git checkout branchName
```

6. Tạo một nhánh mới và chuyển đến nó
```
git checkout -b newBranch
```

7. Xóa một nhánh
```
git branch -d branchName
* Lưu ý checkout sang branch khác branch cần xóa
```

8. Cách hủy bỏ các file đã add vào trạng thái sẽ commit
```
git reset
```

9. Cách hủy bỏ các file đã commit nhưng chưa push
```
git reset HEAD~1
```

10. Hiện lịch sử tất cả các commit
```
git log
```
