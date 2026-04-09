<img width="1082" height="234" alt="image" src="https://github.com/user-attachments/assets/a4d910bf-d9a5-4874-a72a-cf5cb78acf08" /># Môn: Phát triển ứng dụng với mã nguồn mở-TEE0421
# Họ tên : Nguyễn Đình Tú
# Lớp: 58KTPM
# MSSV: K225480106067
# bai_tap1
# A. Đăng ký tên miền xịn cho cá nhân:

1 Đăng ký domain xịn (có thể dùng của mắt bão, tên miền *.id.vn đang miễn phí cho mọi công dân việt nam <= 23 tuổi, *.io.vn : giá 30k vnđ/năm)

* Trang web đang ký tên miền.
 
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

* kết lối thành công

<img width="1292" height="966" alt="image" src="https://github.com/user-attachments/assets/a7dc98dc-5434-488d-b29e-ef09260020e3" />

Sử dụng một trong các công cụ để giả lập: HyperV (có sẵn của windows), VirutualBox (Miễn phí), VM_Ware (bản quyền)

Download file iso để cài đặt.

Cấu hình mạng trong Ubuntu (và công cụ giả lập) để cho phép truy cập SSH vào Ubuntu từ cmd của windows

Ví dụ:

để ssh tới ubuntu ở ip 192.168.100.123, user là admin thì mở CMD trên windows,

<img width="767" height="519" alt="image" src="https://github.com/user-attachments/assets/dbfa711d-2b2a-4761-a801-29c70141d4ad" />

gõ lệnh: ssh dinhtu@172.20.164.62

<img width="1019" height="659" alt="image" src="https://github.com/user-attachments/assets/e415cf65-6141-4914-86ca-95558e710462" />

hệ thống sẽ yêu cầu nhập password (chú ý : password sẽ không hiện ra)

sau khi login thành công sẽ thấy màn hình chào hỏi của ubuntu

Tìm hiểu các lệnh cơ bản của ubuntu

Các lệnh cần tìm hiểu:

Liệt kê các file trong thư mục: ls

<img width="875" height="113" alt="image" src="https://github.com/user-attachments/assets/494f1e93-5580-453b-b4a7-c12d93bd4af3" />

Tạo thư mục: mkdir nameFolder

<img width="1003" height="101" alt="image" src="https://github.com/user-attachments/assets/831b1ede-3157-4a83-b3e7-16b807a86dee" />

Chuyển thư mục làm việc: cd path


Copy file: cp file_nguồn path/file_đích

Thay đổi quyền thao tác file: sudo chmod xxx filename

Edit file: sudo nano tenfile

CTRL+o : lưu nội dung sau khi edit

CTRL+x : thoát edit file

<img width="1104" height="634" alt="image" src="https://github.com/user-attachments/assets/d5690195-23b5-40d0-ae8d-7089c860bf93" />

Xem ip của máy ubuntu: ip -4 addr

<img width="1176" height="747" alt="image" src="https://github.com/user-attachments/assets/c0b09f04-4a39-4be2-9a40-ec2823d915bc" />

Cài đặt docker cho Ubuntu

<img width="1096" height="526" alt="image" src="https://github.com/user-attachments/assets/da8edaf6-8918-4dda-bced-a21af0ddc75c" />

Kiểm tra phiên bản docker vừa cài đặt, kiểm tra phiên bản của docker compose

<img width="499" height="95" alt="image" src="https://github.com/user-attachments/assets/4ccd0288-55fb-44fa-bb64-6f974d0f67a3" />

Cấu hình để docker chạy mà không cần tiền tố sudo

<img width="690" height="313" alt="image" src="https://github.com/user-attachments/assets/03ae4ed7-dd26-4179-8856-ae0201c8fa18" />

Tìm hiểu tập lệnh của docker và docker compose

Đảm bảo tường lửa trên Ubuntu đã cho phép các cổng 80, 1880, 9630 (Lệnh: sudo ufw allow ...)

<img width="581" height="220" alt="image" src="https://github.com/user-attachments/assets/03c179c6-2427-4571-9573-0320b743ce40" />

4 Nhập 2 dòng namespace của cloudflare vào trong trang quản lý DNS record của tên miền đăng ký (vd trên mắt bão)

<img width="1519" height="730" alt="image" src="https://github.com/user-attachments/assets/1690768f-bc11-4001-97f4-afadc9939476" />

# C. Cấu hình docker compose:

1 Tạo thư mục: ~/myapp

 <img width="737" height="420" alt="image" src="https://github.com/user-attachments/assets/25549202-650f-416d-b84a-6bd89ebc6c2b" />

2 Chuyển vào trong thư mục ~/myapp

<img width="413" height="76" alt="image" src="https://github.com/user-attachments/assets/cace6e16-757b-4ed2-b813-91cf0a2adc92" />

3 Tạo thư mục: ./myweb

4 Tạo file ./myweb/index.html (với nội dung là thông tin cá nhân của em)

  nano myweb/index.html

<img width="1099" height="633" alt="image" src="https://github.com/user-attachments/assets/0c74c472-3ec6-40f9-91d2-1459a8e105fc" />

5 Tạo file docker-compose.yml để nó sẽ có các dịch vụ sau:

<img width="1100" height="638" alt="image" src="https://github.com/user-attachments/assets/4ec06d3a-4a43-4f11-bc9f-5d3ba1a1ac0e" />

Khai báo sử dụng nodered/node-red, cổng 1880, dữ liệu nằm tại thư mục ./nodered

Khai báo sử dụng nginx, cổng 80, cấu hình trong file ./nginx/nginx.conf

<img width="1101" height="638" alt="image" src="https://github.com/user-attachments/assets/9e649fa5-5f4f-4a69-ba74-c4ee26a23507" />

Mount thư mục ./myweb thành thư mục /myweb trong nginx

Mount file ./nginx/nginx.conf vào file /etc/nginx/nginx.conf trong nginx

6 Edit file ./nginx/nginx.conf để:

Cấu hình web server cổng 80

<img width="1103" height="630" alt="image" src="https://github.com/user-attachments/assets/3f082457-1320-4943-9ead-a4e7f539db0e" />

server_name là sub-domain (sub-domain tuỳ ý của em)

<img width="1918" height="841" alt="image" src="https://github.com/user-attachments/assets/dfe9d65e-b49f-45eb-ba12-90589c533bbe" />

location / trỏ tới root là thư mục /myweb

<img width="1095" height="704" alt="image" src="https://github.com/user-attachments/assets/f98b1e57-f5e8-43ff-afa3-2c9400a67c02" />

location /api dùng proxy_pass trỏ tới 1 (hoặc nhiều) node http_in của nodered

<img width="1877" height="909" alt="image" src="https://github.com/user-attachments/assets/328528c4-dc39-4e51-8fd3-f3723eef2b0e" />

<img width="1127" height="758" alt="image" src="https://github.com/user-attachments/assets/543647a4-f331-4505-9541-478354874e9d" />

7 Edit file ./nodered/settings.js để nodered bắt buộc đăng nhập

<img width="1097" height="638" alt="image" src="https://github.com/user-attachments/assets/d9f3173a-e17a-4e49-aee8-1f65af91416a" />

Chạy docker-compose lần đầu để Node-RED tự sinh file cấu hình trong thư mục ./nodered, sau đó mới tiến hành sửa settings.js và restart lại container

<img width="1904" height="996" alt="image" src="https://github.com/user-attachments/assets/bbf703ea-ff17-444d-8c83-20331e161699" />

<img width="1910" height="973" alt="image" src="https://github.com/user-attachments/assets/b0e58396-b22f-4a14-81ec-066595f62d38" />

# D. (Bonus - không bắt buộc)

1 tạo thư mục ./myapi

<img width="1051" height="369" alt="image" src="https://github.com/user-attachments/assets/723efade-b829-41a6-a470-4ac1497ca0ab" />

2 tạo file ./myapi/app.py sử dụng Python + Flask để làm gì đó funny

<img width="878" height="102" alt="image" src="https://github.com/user-attachments/assets/c48c9b04-e30a-472e-85ac-ce148dc13b42" />

<img width="1103" height="699" alt="image" src="https://github.com/user-attachments/assets/744f7139-649e-42e4-80a2-1237793e1d89" />

3 tạo file ./myapi/requirements.txt chứa các thư viện mà app.py sử dụng (theo như app.py ví dụ thì requirements.txt chỉ cần có nội dung: flask)

<img width="1061" height="165" alt="image" src="https://github.com/user-attachments/assets/ee88125d-6fe0-458b-b985-8441fffb5f88" />

4 tạo file ./myapi/Dockerfile để khai báo sử dụng Python 3.9 slim

    Sử dụng phiên bản Python nhẹ (alpine) để giảm dung lượng image
 
   FROM python:3.9-slim
  
    Thiết lập thư mục làm việc bên trong container
 
   WORKDIR /app

    Sao chép file requirements vào và cài đặt thư viện
   COPY requirements.txt .
   RUN pip install --no-cache-dir -r requirements.txt

    Sao chép toàn bộ mã nguồn vào container
   COPY . .

    Thông báo container sẽ chạy ở cổng 9630
   EXPOSE 9630

    Lệnh khởi chạy ứng dụng
   CMD ["python", "app.py"]

<img width="1100" height="692" alt="image" src="https://github.com/user-attachments/assets/555dfff0-98da-4d0e-a5de-92475e0bdf15" />
 
5 Sửa đổi docker-compose để sử dụng myapp (xem phần tham khảo ở dưới)

<img width="1097" height="667" alt="image" src="https://github.com/user-attachments/assets/fa6dc340-ae05-4352-bbf0-594fd85a58c0" />

6 Sửa đổi nginx/nginx.conf để /api trỏ tới service myapp cổng 9630

<img width="1081" height="430" alt="image" src="https://github.com/user-attachments/assets/51788628-863d-436b-bdb2-d8fa6ff4d6aa" />

<img width="1111" height="699" alt="image" src="https://github.com/user-attachments/assets/a2f6be52-77a1-4ed5-a7c1-2ac180833f9e" />

# E. Triển khai (level test) ứng dụng

1 Chuyển vào trong thư mục ~/myapp

2 Gõ lệnh để docker compose chạy: sẽ run tất cả các service khai báo trong file docker-compose.yml

Lợi ích: Chỉ cần docker-compose up -d là toàn bộ hệ thống (Web + Node-RED + Tunnel) tự chạy,

<img width="1108" height="842" alt="image" src="https://github.com/user-attachments/assets/51b7d78e-4e15-4124-800a-d322f8e770c4" />

3 Kiểm tra các container đang chạy trong docker, nếu có cái nào bị restart cần tìm lỗi rồi edit lại docker-compose.yml

<img width="1082" height="234" alt="image" src="https://github.com/user-attachments/assets/1fd3b097-3ebd-4187-8b6b-9b273e29daaa" />

4 Kiểm tra kiểm thử các service đang chạy độc lập thông qua ip và port của nó: ví dụ mở trình duyệt ip_ubuntu:1880 để check nodered đã chạy chưa

 Truy cập http://172.20.164.62 -> Ra trang web cá nhân.

 <img width="908" height="595" alt="image" src="https://github.com/user-attachments/assets/46ae65e9-5db6-40a9-8b07-626a7ab01bf2" />

 Truy cập http://172.20.164.62/api/ -> Ra nội dung JSON của Flask.

 <img width="1243" height="448" alt="image" src="https://github.com/user-attachments/assets/12e82b83-fcb3-4bc1-b0de-06535221fa28" />

 Truy cập http://172.20.164.62:1880 -> Ra bảng đăng nhập bảo mật của Node-RED.

 <img width="1908" height="967" alt="image" src="https://github.com/user-attachments/assets/bfbc837a-bb3e-468e-9b93-a0dd22c79990" />

5 Sử dụng nodered: kéo nodered http_in , http_response, function : để tạo api get đơn giản (dùng cho /api proxy_pass của nginx)

<img width="1377" height="769" alt="image" src="https://github.com/user-attachments/assets/15e8d05f-d883-4066-a17b-294336f6ea59" />

<img width="1159" height="431" alt="image" src="https://github.com/user-attachments/assets/4efbd37e-a083-4eb4-bff2-40ff4bf5aef9" />

6 Sửa file ./myweb/index.html : thêm code html+js để sử dụng được api đã khai báo proxy_pass (thực ra là sử dụng nodered http_in hoặc sử dụng service myapi)

<img width="1099" height="696" alt="image" src="https://github.com/user-attachments/assets/336c34f9-5803-498e-ad0a-5195fb940e04" />

<img width="1872" height="958" alt="image" src="https://github.com/user-attachments/assets/cb3bfc7d-3c7a-4fe5-82ce-a5fd0f9fd566" />
