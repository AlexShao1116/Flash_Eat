# 🍔 Reggie Take-Out 🍟

Reggie Take-Out is a web application designed to streamline food ordering and management processes. This project combines a robust backend with a dynamic frontend, delivering a seamless experience for both customers and administrators. 🚀

## ✨ Features

### 🛠️ Backend:
- 🔒 User Authentication and Authorization
- 👨‍💻 Employee Management
- 🍱 Food and Category Management
- 📦 Order Processing and Tracking

### 🌟 Frontend:
- 🖥️ User-Friendly Interfaces for Customers and Administrators
- 📋 Dynamic Food Menus
- ⚡ Real-Time Order Updates

## 🛠️ Technology Stack

### Backend:
- **Language**: Java ☕
- **Framework**: Spring Boot 🌱
- **Build Tool**: Maven 🛠️
- **Database**: MySQL 🗄️

### Frontend:
- **Framework**: Vue.js 🖌️
- **Styling**: CSS 🎨, Element-UI 💡
- **Build Tool**: Webpack 📦

## 📂 Project Structure

```
reggie_take_out
|-- pom.xml                 # Maven configuration
|-- src/
    |-- main/java/          # Java source files
        |-- com/itheima/reggie/
            |-- ReggieApplication.java  # Entry point of the application
            |-- common/                # Common utility classes and constants
            |-- config/                # Configuration files
            |-- controller/            # Controllers for handling HTTP requests
            |-- dto/                   # Data Transfer Objects
            |-- entity/                # Entity classes representing database tables
            |-- filter/                # Servlet filters for request processing
            |-- mapper/                # Data Access Objects (DAO) or Mapper interfaces
            |-- service/               # Business logic interfaces and implementations
            |-- utils/                 # Utility classes
    |-- main/resources/
        |-- application.yml            # Backend configuration
        |-- backend/                   # Backend-related frontend assets
        |-- front/                     # Frontend user-facing assets
    |-- test/java/                     # Test files
```

## 📄 Java Files and Their Usage

### 🚀 `ReggieApplication.java`
- **Usage**: The main entry point of the Spring Boot application. It bootstraps and starts the application.

### 📦 `common` Package:
- **`BaseContext.java`**: Provides thread-local storage for storing and retrieving user-related data.
- **`CustomException.java`**: Defines custom exceptions used in the application.
- **`GlobalExceptionHandler.java`**: Handles exceptions globally and provides standardized error responses.
- **`JacksonObjectMapper.java`**: Configures Jackson for JSON serialization and deserialization.
- **`MyMetaObjecthandler.java`**: Automatically populates fields like `createTime` and `updateTime` during database operations.
- **`R.java`**: Defines standard response structures for API responses.

### ⚙️ `config` Package:
- **`MybatisPlusConfig.java`**: Configures MyBatis Plus for ORM features.
- **`WebMvcConfig.java`**: Configures CORS, static resource handlers, and argument resolvers.

### 🧑‍💼 `controller` Package:
- **Various Controllers**: Handle HTTP requests for specific modules:
  - `EmployeeController.java`: 👨‍💼 Employee management (e.g., login, creation).
  - `CategoryController.java`: 🗂️ Category management for dishes and set meals.
  - `DishController.java`: 🍛 Manages dishes, including flavors.
  - `OrderController.java`: 📦 Handles customer orders.
  - `SetmealController.java`: 🍱 Manages set meals and their associated dishes.
  - `ShoppingCartController.java`: 🛒 Handles shopping cart operations.

### 📊 `dto` Package:
- **`DishDto.java`**: Encapsulates dish data with related flavors.
- **`SetmealDto.java`**: Encapsulates set meal data with related dishes.

### 📋 `entity` Package:
- Represents database tables, including:
  - `Employee.java`: 👨‍💼 Employee details.
  - `Dish.java`: 🍛 Dish details.
  - `Orders.java`: 🧾 Order details.
  - `Setmeal.java`: 🍱 Set meal details.

### 🔍 `filter` Package:
- **`LoginCheckFilter.java`**: Intercepts requests to check for user authentication.

### 🗄️ `mapper` Package:
- Provides database interaction methods for each module:
  - `EmployeeMapper.java`: Handles employee database operations.
  - `CategoryMapper.java`: Handles category database operations.
  - `OrderMapper.java`: Handles order database operations.

### 🧠 `service` Package:
- Business logic interfaces and implementations:
  - `EmployeeService.java`: 👨‍💼 Employee-related operations.
  - `OrderService.java`: 📦 Order processing.
  - `SetmealService.java`: 🍱 Set meal management.

### 🛠️ `utils` Package:
- **`SMSUtils.java`**: Provides methods for sending SMS notifications.
- **`ValidateCodeUtils.java`**: Generates validation codes for authentication.

### 🧪 Test Files:
- **`UploadFileTest.java`**: Tests for file upload functionality.

## 🔧 Techniques Used

1. **Spring Boot Framework** 🌱:
   - Simplifies Java-based web application development.
   - Provides REST API support with @RestController.

2. **Maven for Dependency Management** 🛠️:
   - Automates project build and manages dependencies efficiently.

3. **MyBatis Plus** 🗄️:
   - Simplifies database interactions with MySQL.

4. **Vue.js for Frontend Development** 🎨:
   - Enables a reactive, component-based UI.
   - Integrates with Element-UI for pre-designed components.

5. **Servlet Filters** 🔍:
   - Enhances security by intercepting and validating requests.

6. **AJAX and API Integration** ⚡:
   - Facilitates dynamic data exchange between frontend and backend.

7. **Layered Architecture** 🏗️:
   - Organizes the codebase into layers (Controller, Service, DAO, Entity) for maintainability.

## 🛠️ Setup Instructions

### Prerequisites:
- Java Development Kit (JDK) 8+ ☕
- Maven 🛠️
- Node.js and npm (for frontend if necessary) 🌐
- MySQL database server 🗄️

### Steps:
1. Clone the repository:
   ```
   git clone <repository_url>
   ```
2. Navigate to the project directory:
   ```
   cd reggie_take_out
   ```
3. Configure the database in `application.yml`.
4. Build the project:
   ```
   mvn clean install
   ```
5. Run the application:
   ```
   java -jar target/<project-jar-file>.jar
   ```
6. Access the application:
   - Backend: `http://localhost:<port>`
   - Frontend: Open the `index.html` files in `src/main/resources/backend` or `front`.

## 🌟 Usage

### Backend:
- Access REST APIs for managing employees, categories, orders, etc.

### Frontend:
- Open the provided HTML files for the administrator and customer interfaces.

## 🤝 Contributors
- (Add contributors' names or roles here)

## 📜 License

This project is licensed under the [MIT License](LICENSE).

## 🚀 Future Work

- Integration of real-time notifications.
- Mobile responsiveness for frontend interfaces.
- Expanded reporting and analytics for administrators.

