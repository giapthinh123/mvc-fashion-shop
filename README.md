# BTL_demo_4 - Fashion Shop

An e-commerce fashion website built with Java Servlet and JSP.

## Project Description

BTL_demo_4 is an e-commerce web application specializing in fashion products including:
- Men's Fashion
- Women's Fashion
- Kids' Fashion

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

### User Features
- Registration / Login
- Browse product list
- View product details
- Add products to cart
- Checkout (COD or VNPay)
- View order history
- Manage personal information

### Admin Features
- Product management (CRUD)
- Category management
- User management
- Order management
- View statistics reports

## Installation and Running

### Requirements
- JDK 24 or higher
- MySQL 8.0 or higher
- Apache Maven 3.6 or higher
- Apache Tomcat 10 (or a server supporting Jakarta EE 9+)

### Database Configuration

1. Create a MySQL database named `btl`:
```sql
CREATE DATABASE btl CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
```

2. Update the database connection settings in `src/main/java/com/bqa/util/DBconn.java`:
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

3. Deploy the WAR file to a Tomcat server or run directly from your IDE

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

The project includes VNPay sandbox integration for testing payments. Configuration is stored in `VNPayConfig.java`:
- Payment URL: sandbox.vnpayment.vn

> **Note**: This is a sandbox environment and should not be used for production.

## Key Features

- ✅ Responsive UI with Bootstrap 5
- ✅ User/Admin role-based access control
- ✅ VNPay payment integration
- ✅ Shopping cart management
- ✅ Complete order management
- ✅ Product categorization

## Author

- **giapthinh123** - [GitHub Profile](https://github.com/giapthinh123)

## License

This project was developed for educational purposes.
