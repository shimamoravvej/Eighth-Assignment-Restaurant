Security Measures
Passwords are hashed using the SHA-256 algorithm (implemented in PasswordHashing.java).

Plaintext passwords are never stored in the database.

Users must confirm their current password before changing it.

💻 JavaFX UI Features
User login and registration

Scrollable order form with quantity selection

Order history view with detailed popups

Profile editor and password update functionality

🔧 Core Functionalities
registerCtrl(username, password, email)
Validates user input and registers new users

login(username, password)
Verifies password by comparing its SHA-256 hash

placeOrder(order, userId, orderDetails)
Saves the complete order to the database

getAllMenuItems()
Dynamically loads the restaurant menu from the database

🧰 Technologies Used
Technology	Purpose
Java 17	Core programming language
JavaFX	User interface development
PostgreSQL	Persistent data storage
JDBC	Database connectivity
Gradle	Build automation and dependency management

🚀 How to Run the Project
Set up PostgreSQL and execute the init.sql file to initialize the database.

Open the project in IntelliJ IDEA or Eclipse.

Run the RestaurantApp.java file located in the UI package.

🧱 Project Architecture
Layers:
Presentation Layer (UI):

Built using JavaFX.

Includes interfaces for login, registration, dashboard, menu viewing, and order submission.

Business Logic Layer:

OrderService.java and UserService.java contain the core business logic (registration, orders, updates, etc.).

Data Access Layer:

DAO classes like MenuItemDatabase.java and DatabaseManager.java handle all database operations via JDBC.

Model Layer:

Includes POJOs such as User.java, MenuItems.java, Orders.java, and OrderDetails.java.

🗃️ Entity Relationship (Database Schema)
Table	Description
users	Stores user credentials and metadata
menu_items	Contains restaurant menu items with name, price, category, and description
orders	Represents order headers with reference to the user
order_details	Stores line items for each individual order