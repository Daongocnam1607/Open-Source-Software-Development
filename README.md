<h2 align="center">
    <a href="https://dainam.edu.vn/vi/khoa-cong-nghe-thong-tin">
    🎓 Faculty of Information Technology (DaiNam University)
    </a>
</h2>
<h2 align="center">
    Open Source Software Development
</h2>
<div align="center">
    <p align="center">
        <img src="docs/logo/aiotlab_logo.png" alt="AIoTLab Logo" width="170"/>
        <img src="docs/logo/fitdnu_logo.png" alt="AIoTLab Logo" width="180"/>
        <img src="docs/logo/dnu_logo.png" alt="DaiNam University Logo" width="200"/>
    </p>

[![AIoTLab](https://img.shields.io/badge/AIoTLab-green?style=for-the-badge)](https://www.facebook.com/DNUAIoTLab)
[![Faculty of Information Technology](https://img.shields.io/badge/Faculty%20of%20Information%20Technology-blue?style=for-the-badge)](https://dainam.edu.vn/vi/khoa-cong-nghe-thong-tin)
[![DaiNam University](https://img.shields.io/badge/DaiNam%20University-orange?style=for-the-badge)](https://dainam.edu.vn)

</div>

## 🚀 1. Các project đã thực hiện dựa trên Platform

Một số project sinh viên đã thực hiện:
- #### [Khoá 17](./docs/projects/K17/README.md)
- #### [Khoá 18]() (Coming soon)
## 📚 2. Bài thực hành Lab01–Lab05

Mỗi bài nằm trên một nhánh riêng, có tài liệu, mã nguồn mẫu và bộ kiểm thử. Chọn bài trong bảng dưới đây hoặc clone riêng nhánh tương ứng. Các TODO là phần sinh viên cần hoàn thiện.

| Bài | Nội dung | Nhánh | Hướng dẫn đầy đủ |
| --- | --- | --- | --- |
| Lab01 | Linux và shell script | [lab1](https://github.com/FIT-DNU/Open-Source-Software-Development/tree/lab1) | [Hướng dẫn Lab01](https://github.com/FIT-DNU/Open-Source-Software-Development/blob/lab1/HUONG_DAN.md) |
| Lab02 | Module PHP kiểm tra điều kiện đăng ký | [lab2](https://github.com/FIT-DNU/Open-Source-Software-Development/tree/lab2) | [Hướng dẫn Lab02](https://github.com/FIT-DNU/Open-Source-Software-Development/blob/lab2/HUONG_DAN.md) |
| Lab03 | Danh sách sự kiện, tìm kiếm và form | [lab3](https://github.com/FIT-DNU/Open-Source-Software-Development/tree/lab3) | [Hướng dẫn Lab03](https://github.com/FIT-DNU/Open-Source-Software-Development/blob/lab3/HUONG_DAN.md) |
| Lab04 | Bản nháp bằng Session và Cookie | [lab4](https://github.com/FIT-DNU/Open-Source-Software-Development/tree/lab4) | [Hướng dẫn Lab04](https://github.com/FIT-DNU/Open-Source-Software-Development/blob/lab4/HUONG_DAN.md) |
| Lab05 | Lưu, truy vấn và thống kê với PostgreSQL | [lab5](https://github.com/FIT-DNU/Open-Source-Software-Development/tree/lab5) | [Hướng dẫn Lab05](https://github.com/FIT-DNU/Open-Source-Software-Development/blob/lab5/HUONG_DAN.md) |

### Chuẩn bị môi trường

Trên Windows, mở **Ubuntu/WSL** để chạy các lệnh Bash bên dưới. Cần PHP **từ 8.1 trở lên** và Git:

```bash
sudo apt update
sudo apt install php-cli git unzip
php -v
git --version
```

Lab01–04 không cần PostgreSQL, Composer hoặc framework. Lab05 cần chuẩn bị thêm PostgreSQL theo mục riêng bên dưới.

### Clone và chạy từng bài

Chạy mỗi nhóm lệnh từ thư mục bạn muốn lưu bài học. Mỗi lệnh clone tạo một thư mục riêng; nếu đã tải bài, chỉ cần vào thư mục `Ma_nguon` của bài đó để chạy lại.

#### Lab01 — Linux và shell script

```bash
git clone --single-branch --branch lab1 https://github.com/FIT-DNU/Open-Source-Software-Development.git lab1
cd lab1/Ma_nguon
bash lab.sh check
bash lab.sh run
```

Mở [http://127.0.0.1:8101](http://127.0.0.1:8101). Bài thực hành gồm script kiểm tra môi trường và quét cú pháp PHP.

#### Lab02 — Module PHP

```bash
git clone --single-branch --branch lab2 https://github.com/FIT-DNU/Open-Source-Software-Development.git lab2
cd lab2/Ma_nguon
bash lab.sh check
bash lab.sh run
```

Kết quả in ngay trong terminal, không cần trình duyệt. Ví dụ mẫu còn chỗ trả `AVAILABLE`.

#### Lab03 — Tìm kiếm và form

```bash
git clone --single-branch --branch lab3 https://github.com/FIT-DNU/Open-Source-Software-Development.git lab3
cd lab3/Ma_nguon
bash lab.sh check
bash lab.sh run
```

Mở [danh sách sự kiện](http://127.0.0.1:8103) hoặc [form đăng ký](http://127.0.0.1:8103/register.php). Form hợp lệ hiển thị `PREVIEW_OK`; chưa lưu Session hoặc CSDL.

#### Lab04 — Session và Cookie

```bash
git clone --single-branch --branch lab4 https://github.com/FIT-DNU/Open-Source-Software-Development.git lab4
cd lab4/Ma_nguon
bash lab.sh check
bash lab.sh run
```

Mở [http://127.0.0.1:8104/register.php](http://127.0.0.1:8104/register.php). Thử nhập, xem lại, sửa, hủy và hoàn tất bản nháp. Hoàn tất hiển thị `SIMULATED_OK`; chưa ghi CSDL.

#### Lab05 — PostgreSQL

```bash
git clone --single-branch --branch lab5 https://github.com/FIT-DNU/Open-Source-Software-Development.git lab5
cd lab5/Ma_nguon
sudo apt install postgresql postgresql-client php-pgsql
sudo service postgresql start
```

**Trước khi chạy ứng dụng**, làm mục [Chuẩn bị riêng cho Lab 05](https://github.com/FIT-DNU/Open-Source-Software-Development/blob/lab5/HUONG_DAN.md): tạo tài khoản và CSDL lab riêng hoặc dùng thông tin giảng viên cấp. Sau đó, tại `lab5/Ma_nguon`:

```bash
bash lab.sh db-config
bash lab.sh check
bash lab.sh sql
```

Nhập thông tin kết nối theo lời nhắc của `db-config`. Khi lệnh `sql` mở cửa sổ PostgreSQL, tạo bảng và kiểm tra dữ liệu mẫu:

```sql
\i database/schema.sql
SELECT id, title FROM events ORDER BY id;
\q
```

Cần thấy 3 sự kiện mẫu. Trở về Bash và chạy:

```bash
bash lab.sh run
```

Mở [http://127.0.0.1:8105/register.php](http://127.0.0.1:8105/register.php). Đăng ký lần đầu trả `CREATED`; cùng email và sự kiện trả `DUPLICATE`. Không đưa thư mục `.local` chứa cấu hình mật khẩu vào Git hoặc bài nộp.

### Kiểm thử và dừng ứng dụng

Với các bài Web, giữ terminal máy chủ mở; nhấn **Ctrl+C** để dừng. Để chạy kiểm thử trong lúc Web hoạt động, mở terminal Ubuntu/WSL thứ hai và vào đúng thư mục `Ma_nguon` của bài:

```bash
bash lab.sh test
bash lab.sh extend
```

- `check`: chỉ kiểm tra môi trường, không xác nhận bài tập hoàn thành.
- `test`: kiểm tra phần mẫu; Lab05 có kiểm thử tích hợp PostgreSQL.
- `extend`: kiểm tra phần tự làm; có thể chưa đạt khi sinh viên chưa hoàn thiện TODO. Không sửa test để bỏ qua lỗi.

Nếu báo `No such file or directory`, kiểm tra `pwd` và `ls`: thư mục hiện tại cần chứa `lab.sh`. Nếu báo `Address already in use`, dừng máy chủ cũ bằng Ctrl+C trước khi chạy lại.
