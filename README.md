# BTL_demo_4 - Fashion Shop

A fashion e-commerce website built with Java Servlet and JSP.

## Project Description

BTL_demo_4 is an e-commerce web application specializing in fashion products including:
- Men's fashion
- Women's fashion
- Children's fashion

## Technologies Used

- **Backend**: Java Servlet, JSP
- **Frontend**: HTML, CSS, JavaScript, Bootstrap 5
- **Database**: MySQL
- **Payment**: VNPay (sandbox)
- **Build Tool**: Maven
- **Java Version**: 24

## Project Structure

```
mvc-fashion-shop/
├── src/
│   └── main/
│       ├── java/com/bqa/
│       │   ├── config/         # Configuration (VNPay)
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

## Main Features

### User
- Register / Login
- View product list
- View product details
- Add products to cart
- Checkout (COD or VNPay)
- View order history
- Manage personal information

### Administrator (Admin)
- Product management (CRUD)
- Product category management
- User management
- Order management
- View statistical reports

## Installation and Running

### Requirements
- JDK 24 or higher
- MySQL 8.0 or higher
- Apache Maven 3.6 or higher
- Apache Tomcat 10 (or server supporting Jakarta EE 9+)

### Database Configuration

1. Create a MySQL database named `btl`:
```sql
CREATE DATABASE btl CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
```

2. Update the database connection information in `src/main/java/com/bqa/util/DBconn.java`:
```java
String url = "jdbc:mysql://localhost:3306/btl";
String user = "root";
String password = "your_password";
```

### Build and Deploy

1. Clone the repository:
```bash
git clone https://github.com/giapthinh123/mvc-fashion-shop.git
cd mvc-fashion-shop
```

2. Build the project with Maven:
```bash
mvn clean package
```

3. Deploy the WAR file to Tomcat server or run directly from IDE

### Running with IDE

- **IntelliJ IDEA**: Import project as Maven project, configure Tomcat server and run
- **Eclipse**: Import as Maven project, add to Tomcat server

## Dependencies

| Dependency | Version | Description |
|------------|---------|-------------|
| Jakarta Servlet API | 6.1.0 | Servlet specification |
| Jakarta JSTL | 3.0.0 | JSP Standard Tag Library |
| MySQL Connector | 8.0.33 | JDBC driver for MySQL |
| JUnit Jupiter | 5.11.0 | Testing framework |

## VNPay Payment Gateway

The project integrates VNPay sandbox for payment testing. Configuration is stored in `VNPayConfig.java`:
- Payment URL: sandbox.vnpayment.vn

> **Note**: This is a sandbox environment, not for production use.

## Key Features

- ✅ Responsive interface with Bootstrap 5
- ✅ User/Admin role authorization
- ✅ VNPay payment integration
- ✅ Shopping cart management
- ✅ Complete order management
- ✅ Product categorization by category

## Author

- **giapthinh123** - [GitHub Profile](https://github.com/giapthinh123)

## License

This project was developed for educational purposes.
