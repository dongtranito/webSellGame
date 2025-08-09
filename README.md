# 🎮 WebGame - Hệ thống Bán Game Online

Website bán tài khoản game online được xây dựng bằng Spring Boot.

## 🛠 Công nghệ sử dụng

- **Spring Boot 3.3.5** - Framework chính
- **Spring Security** - Bảo mật 
- **MySQL** - Cơ sở dữ liệu
- **Thymeleaf** - Template engine
- **Maven** - Quản lý dependencies

## ✨ Tính năng chính

### Người dùng
- Đăng ký/đăng nhập (Email + Google OAuth2)
- Duyệt và tìm kiếm game
- Thêm vào giỏ hàng và thanh toán
- Xem lịch sử đơn hàng
- Đánh giá game

### Quản trị viên  
- Quản lý game và tài khoản game
- Quản lý người dùng
- Xem báo cáo đơn hàng

## 🗄 Thiết kế cơ sở dữ liệu

### Các bảng chính:
- **User**: Thông tin người dùng
- **Game**: Thông tin game
- **AccountGame**: Tài khoản game để bán
- **Orders**: Đơn hàng
- **CartGame**: Giỏ hàng
- **Review**: Đánh giá
- **Category**: Danh mục game

## 💰 Hệ thống xử lý đơn hàng

**Phần tôi phát triển:**

### Quy trình mua hàng:
1. Khách hàng chọn game và thêm vào giỏ hàng
2. Xác nhận đơn hàng và tổng tiền
3. Xử lý thanh toán
4. Cập nhật trạng thái tài khoản game (chưa bán → đã bán)
5. Giao hàng (hiển thị thông tin tài khoản game)

### Controllers và Services:
- **BuyController**: Xử lý HTTP requests cho thanh toán
- **BuyService**: Logic nghiệp vụ xử lý đơn hàng

## 🚀 Cài đặt và chạy

### Yêu cầu:
- Java 23+
- Maven 3.6+
- MySQL 8.0+

### Các bước:

1. **Clone repository**
```bash
git clone https://github.com/dongtranito/webSellGame.git
cd webSellGame
```

2. **Cấu hình database**
```sql
CREATE DATABASE webgame;
```

3. **Tạo file .env**
```env
DB_URL=jdbc:mysql://localhost:3306/webgame?useSSL=false
DB_USERNAME=root
DB_PASSWORD=password
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
MAIL_USERNAME=your_email@gmail.com
MAIL_PASSWORD=your_app_password
```

4. **Chạy ứng dụng**
```bash
mvn spring-boot:run
```

Truy cập: `http://localhost:8080`

## 👨‍💻 Đóng góp của tôi

- **Thiết kế cơ sở dữ liệu**: Phân tích yêu cầu và thiết kế các bảng
- **Hệ thống xử lý đơn hàng**: Phát triển toàn bộ quy trình mua hàng và thanh toán
- **Logic nghiệp vụ**: Xử lý trạng thái tài khoản, tính toán tổng tiền, quản lý giỏ hàng
