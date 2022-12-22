
# Xây dựng ứng dụng trên AWS cho phép tạo Database và cung cấp api để thêm, xóa, sửa trên Database

## Các tính năng chính

- Thêm, xóa table DynamoDB
- Tương tác dữ liệu của table trực tiếp trên web
- Tương tác dữ liệu của table thông qua API được cung cấp


## Công nghệ sử dụng 

**Client:** Html, Css3, Bootstrap, JS

**Server:** PHP, AWS Lambda, AWS SQS, AWS EC2

**Database:** DynamoDB


## Thành viên tham gia Project

- Vũ Mạnh Cường - 20110449 - 20110449@student.hcmute.edu.vn
- Nguyễn Như Sâm - 20110557 - 20110557@student.hcmute.edu.vn
- Trần Đức Long - 20110058 - 20110058@student.hcmute.edu.vn


## Cách Chạy Project ở Local (video hướng dẫn + text hướng dẫn):
### Bước 1: Chuẩn bị môi trường
+ Vào LearnLab--> start lab --> Aws Detail -->   AWS CLI --> show  copy bảng credentials
+ vào thư mục C:\Users\tên máy\ .aws\credentials
+ past AWS CLI vừa copy file credentials 
- Tải và cài đặt XAMPP và Git
### Bước 2: Cấu hình lại đồ án
- git clone https://github.com/cr49/ProjectDetai11.git vào thư mục htdocs của XAMPP 
#### Tạo API bằng SQS
- vào AWS Tạo các SQS và Lamda theo file Lamda.txt
- Copy URL các SQS vừa tạo và past vào file lib/tables.php trong thư mục project để thay thế các URL của SQS
#### Tạo API bằng API Gateway
- Vào AWS tạo các Lamda function theo API.txt

### Bước 3: Chạy
- Mở XAMPP và start Apache
- mở trình duyệt http://localhost/ProjectDetai11

## Cách Deploy project EC2 (video hướng dẫn + text hướng dẫn):
- Tạo EC2 với hệ điều hành window, mở port http và alltraffic
- Tạo Elastic IP kết nối đến EC2
- Connect EC2 bằng remote Desktop Connection
- Trên window của EC2 vào Window Security --> Firewall & network protection --> Windows Defender Firewall Properties --> tag Public Profile --> Allow Inbound connections --> Apply--> ok
- Dowload XAMPP và GIT
- mở git bash trong thư mục htdocs của XAMPP vừa tải về và git clone https://github.com/cr49/ProjectDetai11.git
- Copy .aws của local máy tính và past vào c/user/Administrator của máy window EC2
- mở XAMPP start apache và mở trình duyệt vào http://<ip máy EC2>/ProjectDetai11
=> Deploy thành công
