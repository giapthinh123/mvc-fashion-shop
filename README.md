# BTL_demo_4 - Fashion Shop

Website bán hàng thời trang được xây dựng bằng Java Servlet và JSP.

## Mô tả dự án

BTL_demo_4 là một ứng dụng web thương mại điện tử chuyên bán các sản phẩm thời trang bao gồm:
- Thời trang nam
- Thời trang nữ  
- Thời trang trẻ em

## Công nghệ sử dụng

- **Backend**: Java Servlet, JSP
- **Frontend**: HTML, CSS, JavaScript, Bootstrap 5
- **Database**: MySQL
- **Payment**: VNPay (sandbox)
- **Build Tool**: Maven
- **Java Version**: 24

## Cấu trúc dự án

```
mvc-fashion-shop/
├── src/
│   └── main/
│       ├── java/com/bqa/
│       │   ├── config/         # Cấu hình (VNPay)
│       │   ├── dao/            # Data Access Objects
│       │   ├── model/          # Entity classes
│       │   ├── service/        # Business logic
│       │   ├── servlet/        # Controllers
│       │   │   └── admin/      # Admin controllers
│       │   └── util/           # Utilities (DB connection)
│       └── webapp/
│           ├── admin/          # Admin pages
│           ├── assets/         # CSS, JS, images
│           ├── page/           # Header, footer components
│           ├── WEB-INF/        # Configuration
│           └── *.jsp           # User-facing pages
├── pom.xml                     # Maven configuration
└── README.md
```

## Chức năng chính

### Người dùng (User)
- Đăng ký / Đăng nhập
- Xem danh sách sản phẩm
- Xem chi tiết sản phẩm
- Thêm sản phẩm vào giỏ hàng
- Thanh toán (COD hoặc VNPay)
- Xem lịch sử đơn hàng
- Quản lý thông tin cá nhân

### Quản trị viên (Admin)
- Quản lý sản phẩm (CRUD)
- Quản lý danh mục sản phẩm
- Quản lý người dùng
- Quản lý đơn hàng
- Xem báo cáo thống kê

## Cài đặt và chạy

### Yêu cầu
- JDK 24 hoặc cao hơn
- MySQL 8.0 hoặc cao hơn
- Apache Maven 3.6 hoặc cao hơn
- Apache Tomcat 10 (hoặc server hỗ trợ Jakarta EE 9+)

### Cấu hình Database

1. Tạo database MySQL với tên `btl`:
```sql
CREATE DATABASE btl CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
```

2. Cập nhật thông tin kết nối database trong file `src/main/java/com/bqa/util/DBconn.java`:
```java
String url = "jdbc:mysql://localhost:3306/btl";
String user = "root";
String password = "your_password";
```

### Build và Deploy

1. Clone repository:
```bash
git clone https://github.com/giapthinh123/mvc-fashion-shop.git
cd mvc-fashion-shop
```

2. Build project với Maven:
```bash
mvn clean package
```

3. Deploy file WAR lên Tomcat server hoặc chạy trực tiếp từ IDE

### Chạy với IDE

- **IntelliJ IDEA**: Import project as Maven project, cấu hình Tomcat server và run
- **Eclipse**: Import as Maven project, add to Tomcat server

## Dependencies

| Dependency | Version | Mô tả |
|------------|---------|-------|
| Jakarta Servlet API | 6.1.0 | Servlet specification |
| Jakarta JSTL | 3.0.0 | JSP Standard Tag Library |
| MySQL Connector | 8.0.33 | JDBC driver cho MySQL |
| JUnit Jupiter | 5.11.0 | Testing framework |

## Cổng thanh toán VNPay

Dự án tích hợp sẵn VNPay sandbox để test thanh toán. Cấu hình được lưu trong `VNPayConfig.java`:
- URL thanh toán: sandbox.vnpayment.vn
- Return URL: localhost:8080/BTL_demo_4_war_exploded/checkout/vnpay_return

> **Lưu ý**: Đây là môi trường sandbox, không sử dụng cho production.

## Tính năng nổi bật

- ✅ Giao diện responsive với Bootstrap 5
- ✅ Phân quyền User/Admin
- ✅ Tích hợp thanh toán VNPay
- ✅ Quản lý giỏ hàng
- ✅ Quản lý đơn hàng đầy đủ
- ✅ Phân loại sản phẩm theo danh mục

## Tác giả

- **giapthinh123** - [GitHub Profile](https://github.com/giapthinh123)

## License

Dự án này được phát triển cho mục đích học tập.
