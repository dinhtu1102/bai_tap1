# Môn: Phát triển ứng dụng với mã nguồn mở-TEE0421
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

* Kết quả chạy được:

<img width="501" height="301" alt="image" src="https://github.com/user-attachments/assets/e10a6097-ca1d-4d1f-9226-0d7d926cf9a3" />

<img width="1870" height="1033" alt="image" src="https://github.com/user-attachments/assets/c5993e58-9dfd-4097-ab1e-5aceeb62acd1" />

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

# F Gỡ lỗi:
1 nếu có lỗi xẩy ra trong quá trình triển khai docker compose up -d

Kiểm tra nhanh: docker compose ps giúp biết container nào đang chạy xem log, ví dụ: docker logs mynginx docker logs myapi

<img width="1080" height="140" alt="image" src="https://github.com/user-attachments/assets/381ef9cd-593f-4ab8-b57e-1369ad005008" />

2 Thêm healthcheck cho myapi trong file docker-compose.yml

healthcheck:

  test: ["CMD", "curl", "-f", "http://localhost:9630"]

<img width="1101" height="124" alt="image" src="https://github.com/user-attachments/assets/3c23f535-e7cd-49c4-aa17-a5795b327521" />

3 giới hạn resource cho một service: (tránh việc 1 service chiếm quá nhiều ram)

deploy:

  resources:
  
    limits:
    
      memory: 512M

<img width="1073" height="148" alt="image" src="https://github.com/user-attachments/assets/808e13df-b4ea-4769-aafa-4f887e664255" />

sử dụng lệnh: docker compose stats để quan sát lượng ram sử dụng bởi mỗi service

Đầu tiên, bạn cần tạo file để thiết lập các thông số Healthcheck và giới hạn tài nguyên.

<img width="1103" height="604" alt="image" src="https://github.com/user-attachments/assets/14f33b8f-0ea6-4962-9f96-ca18afcbc26f" />

<img width="1090" height="281" alt="image" src="https://github.com/user-attachments/assets/55734925-1b30-4dc8-beb8-d9690a4a6363" />

<img width="1084" height="208" alt="image" src="https://github.com/user-attachments/assets/a836ead7-7cba-4b20-96d7-e9a830e419cc" />

* Kết quả đạt được

<img width="1862" height="908" alt="image" src="https://github.com/user-attachments/assets/b11004d0-fa1f-4749-8164-2bbe240edc2f" />

# G. Triển khai ứng dụng đến End-user

1 Trong Cloudflare: Tạo tunnel (đường hầm), chọn loại triển khai cho docker

<img width="1879" height="906" alt="image" src="https://github.com/user-attachments/assets/5ecf21c9-e553-4f3c-9b7d-ca5433c85e46" />

<img width="1866" height="874" alt="image" src="https://github.com/user-attachments/assets/e77a9321-315a-4e92-bcc2-d71c1df1cae0" />

<img width="1786" height="897" alt="image" src="https://github.com/user-attachments/assets/8599f293-7b55-44a7-9da7-76f99eefcca6" />

<img width="1839" height="838" alt="image" src="https://github.com/user-attachments/assets/a8b872ba-65c5-4a00-815a-e0669e052fa8" />

<img width="1845" height="775" alt="image" src="https://github.com/user-attachments/assets/0e9db438-c5dc-43d1-be3b-4f06124c4378" />

<img width="1860" height="943" alt="image" src="https://github.com/user-attachments/assets/2580f4c3-521b-413a-bd43-b20c968b864d" />

<img width="1875" height="932" alt="image" src="https://github.com/user-attachments/assets/3b26e2c3-6af2-4397-8230-90740c23a3ae" />

2 Convert lệnh docker run ... sang dạng docker compose

<img width="1108" height="202" alt="image" src="https://github.com/user-attachments/assets/f9586756-b75e-45d0-b027-f00b0634082c" />

3 Khai báo kết quả convert vào trong file docker-compose.yml

4 Chạy lại docker compose

5 Public ứng dụng bằng cách thêm 1 router trỏ tới container đang chạy trong docker, dữ liệu sẽ đi qua tunnel, url dạng sub-domain

6 Kiểm tra url sub-domain đã hoạt động public cho mọi end-user

<img width="1369" height="1024" alt="image" src="https://github.com/user-attachments/assets/3162727d-79b3-41dd-9236-bf15df49a5cd" />

<img width="1335" height="1002" alt="image" src="https://github.com/user-attachments/assets/b55e1f84-8a29-4e6b-92d8-c89420b8fb16" />

<img width="1309" height="987" alt="image" src="https://github.com/user-attachments/assets/ef381e0d-f52e-4f7c-96fc-384b58dca5c4" />

* cloudflared tunnel login
  
<img width="1234" height="1014" alt="image" src="https://github.com/user-attachments/assets/c17f62cd-66e3-41f4-aa07-b11b5b86e1b6" />

* bấm AU

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/dcda3830-c587-4c4c-adf2-f36f31a507e2" />

* sinh file .cem

<img width="1236" height="1014" alt="image" src="https://github.com/user-attachments/assets/0771cf63-15fa-4ae5-a894-f379903ed58d" />

* cloudflared tunnel create my-tunnel

<img width="1235" height="1021" alt="image" src="https://github.com/user-attachments/assets/15d839a1-eda0-459d-84a6-0950ac24da72" />

* bước tiếp: Tạo config ( tạo router ) nano ~/.cloudflared/config.yml

tunnel: YOUR_TUNNEL_ID

credentials-file: /home/admin/.cloudflared/a8dbc3de-1f8f-48c8-b881-52a1c844f0e7.json

ingress:

  - hostname: iot.dinhtu.id.vn
    
    service: http://localhost:80
    
  - service: http_status:404

<img width="1103" height="648" alt="image" src="https://github.com/user-attachments/assets/0508264d-b05b-49a5-bec5-ee112fe0ff7e" />

* Bước tiếp: Tạo DNS cloudflared tunnel route dns my-tunnel abc.yourdomain.id.vn

* Bước tiếp: Tạo DNS cloudflared tunnel route dns my-tunnel abc.yourdomain.id.vn

<img width="1520" height="1011" alt="image" src="https://github.com/user-attachments/assets/d59af264-ef9d-4aaa-96ab-ff317532ef5d" />

<img width="1449" height="941" alt="image" src="https://github.com/user-attachments/assets/db1e7e97-3375-4da5-b591-9f653a8e8797" />

<img width="1454" height="963" alt="image" src="https://github.com/user-attachments/assets/60aca56b-2a11-4d3d-b40f-37dbaee8ce16" />

* Chỉnh sửa lại nodered.

<img width="1108" height="857" alt="image" src="https://github.com/user-attachments/assets/b8147974-277b-4998-acd3-a5106ec11b09" />

* Kết quả :

<img width="1822" height="969" alt="image" src="https://github.com/user-attachments/assets/6fae9daa-adb6-46fa-bd87-9c15b08335b6" />

<img width="1832" height="965" alt="image" src="https://github.com/user-attachments/assets/cf75edd6-bb83-4d73-88b2-f6405b7e5e3c" />

myapp/
├── docker-compose.yml
├── nginx/
│   └── nginx.conf
├── myweb/
│   └── index.html
└── nodered/ (sẽ tự sinh dữ liệu)
│   └── (có nhiều file tự sinh)
│   └── settings.js (file này cần edit để bắt nodered login)

1 docker-compose.yml

Lệnh kiểm tra: nano ~/myapp/docker-compose.yml

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/b8919494-a716-42cf-b643-2e73f776968c" />

2 Nginx.conf

Lệnh kiểm tra: nano ~/myapp/nginx/nginx.conf

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/64bbcc8f-75f6-4d33-82ed-5c8170490a58" />

3 index.html

Lệnh kiểm tra: nano ~/myapp/myweb/index.html

<img width="1862" height="1070" alt="image" src="https://github.com/user-attachments/assets/fc7afb72-73a5-457d-a5b9-d1dc6de59f91" />

4 nodered :

<img width="1108" height="857" alt="image" src="https://github.com/user-attachments/assets/4f2ce323-9484-4d6b-a6a9-e1e69aaa3897" />

# G. Câu hỏi về bài làm?

Đây là phần giải đáp chi tiết cho các câu hỏi về hệ thống IoT của Tú. Những kiến thức này rất quan trọng để Tú bảo vệ đồ án của mình trước các thầy cô nhé.

1. Tại sao phải dùng Nginx làm Reverse Proxy mà không trỏ thẳng Tunnel vào Node-RED?
Quản lý tập trung: Nginx đóng vai trò là "người điều phối". Nó có thể nhận yêu cầu từ domain rồi chia ra: cái nào vào trang Web (HTML), cái nào vào API (Node-RED). Nếu trỏ thẳng vào Node-RED, Tú sẽ khó tích hợp thêm các ứng dụng khác (như Flask API, Database dashboard) trên cùng một tên miền.

Bảo mật: Nginx ẩn đi các thông tin kỹ thuật của Node-RED, giúp chặn bớt các cuộc tấn công trực tiếp vào cổng dịch vụ.

Hiệu năng: Nginx xử lý các file tĩnh (HTML, CSS, JS) cực nhanh, giúp giảm tải cho Node-RED để Node-RED chỉ tập trung xử lý logic IoT.

2. Sự khác biệt giữa việc Mount file và Mount thư mục trong Docker?
Mount file: Ánh xạ một file cụ thể (ví dụ: nginx.conf). Chỉ file đó được đồng bộ. Nếu Tú xóa file ở máy ngoài, container có thể gặp lỗi không tìm thấy cấu hình.

Mount thư mục: Ánh xạ cả một "kho chứa" (ví dụ: ./nodered). Tất cả file cũ, file mới phát sinh bên trong đều được đồng bộ.

Đặc biệt: Node-RED cần mount thư mục để nó tự sinh ra các file cài đặt, thư viện và flows mà không bị mất khi container khởi động lại.

3. Nếu thay đổi file index.html ở máy Ubuntu, nội dung web có thay đổi ngay không? Tại sao?
Có thay đổi ngay.

Tại sao: Vì Tú đã dùng tính năng Volume Binding trong Docker. File index.html ở máy Ubuntu và trong container thực chất là một. Khi Tú lưu file bằng nano, Nginx trong container sẽ thấy nội dung mới ngay lập tức. Tú chỉ cần F5 trình duyệt là xong.

4. Restart: always và restart: unless-stopped để làm gì?
Restart: always: Container sẽ luôn tự khởi động lại nếu bị lỗi hoặc nếu máy ảo Ubuntu bị tắt đi bật lại.

Restart: unless-stopped: Tương tự như always, nhưng nếu Tú chủ động dùng lệnh docker stop để tắt nó đi, nó sẽ không tự bật lại cho đến khi Tú ra lệnh start. Điều này giúp tránh việc container tự bật lên ngoài ý muốn khi Tú đang bảo trì hệ thống.

5. Khai báo dùng chung 1 network và lợi ích?
Cách khai báo: Khai báo một tên network ở cuối file (phần networks:) và gán tên đó vào từng service.

Lợi ích: * DNS nội bộ: Các container gọi nhau bằng Tên service (ví dụ: http://nodered:1880) thay vì dùng IP. IP có thể thay đổi, nhưng tên service thì cố định.

Bảo mật: Chỉ các container trong cùng network mới thấy nhau, cô lập với các ứng dụng khác bên ngoài.

Sửa đổi file mẫu:

YAML
services:
  nodered:
    # ... cấu hình
    networks:
      - iot_net
  my_nginx:
    # ... cấu hình
    networks:
      - iot_net

networks:
  iot_net:
    driver: bridge
6. Cloudflare Token vào .env và .gitignore?
Cách làm: Tạo file .env ghi: CF_TOKEN=mã_token_của_tú. Trong docker-compose.yml sửa thành: token: ${CF_TOKEN}. Sau đó thêm dòng .env vào file .gitignore.

Tại sao quan trọng: Token là "chìa khóa" vào hệ thống của Tú. Nếu Tú push Token lên GitHub (mã nguồn mở), ai cũng có thể điều hướng tên miền của Tú về máy của họ hoặc tấn công vào mạng nội bộ của Tú. .env giúp tách biệt giữa Mã nguồn và Dữ liệu nhạy cảm.

7. Tại sao nên thêm hậu tố :ro khi mount file cấu hình Nginx?
:ro (Read-Only): Nghĩa là "Chỉ đọc".

Lý do: Đảm bảo container Nginx không thể vô tình sửa đổi hoặc xóa file cấu hình gốc trên máy Ubuntu của Tú. Điều này giúp hệ thống ổn định và bảo mật hơn, tránh việc một lỗ hổng trong container làm hỏng dữ liệu máy chủ.

8. Khi dùng Cloudflare Tunnel: có cần thiết phải mở cổng nữa không?
Không cần thiết.

Giải thích: Cloudflare Tunnel thiết lập một kết nối "đi ra" (outbound) từ máy ảo đến Cloudflare. Vì nó tự mở đường từ bên trong ra, nên Tú không cần mở cổng 80, 443 hay 1880 trên router hoặc tường lửa (UFW) của máy ảo nữa. Đây chính là ưu điểm lớn nhất về bảo mật của Tunnel.




