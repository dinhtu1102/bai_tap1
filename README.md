# Môn: Phát triển ứng dụng với mã nguồn mở-TEE0421
# Họ tên : Nguyễn Đình Tú
# Lớp: 58KTPM
# MSSV: K225480106067
# bai_tap1
# A. Đăng ký tên miền xịn cho cá nhân:
1 Đăng ký domain xịn (có thể dùng của mắt bão, tên miền *.id.vn đang miễn phí cho mọi công dân việt nam <= 23 tuổi, *.io.vn : giá 30k vnđ/năm)
* Trang web đang ký tên miền.
* 
<img width="1849" height="984" alt="image" src="https://github.com/user-attachments/assets/92f7ad94-8fa1-4592-8da5-fa671e569241" />

* Tài khoản đã đăng ký thành công.

<img width="1849" height="905" alt="image" src="https://github.com/user-attachments/assets/4af29e27-ec63-4566-8994-cba4baa7a908" />

2 Đăng ký tài khoản cloudflare

<img width="1872" height="918" alt="image" src="https://github.com/user-attachments/assets/0ac8fff7-64fb-4e95-ab58-be943818807c" />

3 Thêm domain đã đăng ký vào trong cloudflare : Nhận 2 dòng namespace

<img width="1868" height="899" alt="image" src="https://github.com/user-attachments/assets/f728b1e0-fabe-4f2e-aa09-46f71a6614a4" />

<img width="1861" height="910" alt="image" src="https://github.com/user-attachments/assets/98851681-f892-40c5-a97e-07b9e0b8f0ee" />

<img width="1858" height="906" alt="image" src="https://github.com/user-attachments/assets/4216557b-0f70-4ac5-b8d3-08a17a76c0e5" />

* giao diện cloudflare

<img width="1859" height="914" alt="image" src="https://github.com/user-attachments/assets/ee30fa24-dce1-4d93-9468-927e2bfb78d0" />

* đặt tên domin

<img width="1865" height="882" alt="image" src="https://github.com/user-attachments/assets/be229604-a027-4c6c-ba11-4aba08a7cdeb" />

<img width="1854" height="896" alt="image" src="https://github.com/user-attachments/assets/39cea8be-5a0e-48b1-918b-bfeaf832e21b" />

* cài đặt namepace thành công

<img width="1639" height="778" alt="image" src="https://github.com/user-attachments/assets/c704b836-d91b-4a48-aece-b8bb7ccd272e" />

# B. Cài đặt Ubuntu + Docker

Cài đặt hệ điều hành Ubuntu 24.04.4 LTS

* cài đặt ubuntu

<img width="1859" height="885" alt="Screenshot 2026-04-08 214355" src="https://github.com/user-attachments/assets/5990a8d4-8847-4b8c-a353-bb411933c5c1" />

* cài đặt ubuntu trên hyper-V

<img width="1187" height="679" alt="image" src="https://github.com/user-attachments/assets/529fbe6f-16a8-43b7-8e53-7023d1c59f85" />

* giao diên maysb ảo

<img width="1304" height="993" alt="image" src="https://github.com/user-attachments/assets/0b2a7870-ab86-41a9-b7ca-b773227dc60b" />

<img width="1337" height="1001" alt="image" src="https://github.com/user-attachments/assets/b0b527ae-7578-4672-b6ca-09c7a463914d" />

<img width="1306" height="952" alt="image" src="https://github.com/user-attachments/assets/18a9e28f-48b3-46c9-acce-9df492a90663" />

<img width="1315" height="990" alt="image" src="https://github.com/user-attachments/assets/00e940ec-90c8-4027-adda-d6bf8c63bbf4" />


* cài đặt docker

<img width="1377" height="763" alt="image" src="https://github.com/user-attachments/assets/5a90384c-a3ef-479f-9ee8-3f181fb1b741" />

* kết lối thành công

<img width="1292" height="966" alt="image" src="https://github.com/user-attachments/assets/a7dc98dc-5434-488d-b29e-ef09260020e3" />

Sử dụng một trong các công cụ để giả lập: HyperV (có sẵn của windows), VirutualBox (Miễn phí), VM_Ware (bản quyền)

Download file iso để cài đặt.

Cấu hình mạng trong Ubuntu (và công cụ giả lập) để cho phép truy cập SSH vào Ubuntu từ cmd của windows

Ví dụ:

để ssh tới ubuntu ở ip 192.168.100.123, user là admin thì mở CMD trên windows,
gõ lệnh: ssh admin@192.168.100.123
hệ thống sẽ yêu cầu nhập password (chú ý : password sẽ không hiện ra)
sau khi login thành công sẽ thấy màn hình chào hỏi của ubuntu
Tìm hiểu các lệnh cơ bản của ubuntu
Các lệnh cần tìm hiểu:

Liệt kê các file trong thư mục: ls
Tạo thư mục: mkdir nameFolder
Chuyển thư mục làm việc: cd path
Copy file: cp file_nguồn path/file_đích
Thay đổi quyền thao tác file: sudo chmod xxx filename
Edit file: sudo nano tenfile
CTRL+o : lưu nội dung sau khi edit
CTRL+x : thoát edit file
Xem ip của máy ubuntu: ip -4 addr
Cài đặt docker cho Ubuntu
Kiểm tra phiên bản docker vừa cài đặt, kiểm tra phiên bản của docker compose
Cấu hình để docker chạy mà không cần tiền tố sudo
Tìm hiểu tập lệnh của docker và docker compose
Đảm bảo tường lửa trên Ubuntu đã cho phép các cổng 80, 1880, 9630 (Lệnh: sudo ufw allow ...)
4 Nhập 2 dòng namespace của cloudflare vào trong trang quản lý DNS record của tên miền đăng ký (vd trên mắt bão)

<img width="1639" height="778" alt="image" src="https://github.com/user-attachments/assets/c704b836-d91b-4a48-aece-b8bb7ccd272e" />

* cài đặt namepace thành công

<img width="1842" height="863" alt="image" src="https://github.com/user-attachments/assets/8da41247-bd3e-4398-9eea-12e3d1b45c1a" />

