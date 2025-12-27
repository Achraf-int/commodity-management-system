# Commodity Information Management System (CMS)

A professional Java Desktop application built with Java Swing, JDBC, and MySQL.

## Project Structure
- `com.cms.model`: Contains the `Product` entity class.
- `com.cms.dao`: Contains `ProductDAO` for database CRUD operations.
- `com.cms.service`: Contains `ProductService` for business logic and validation.
- `com.cms.ui`: Contains `MainFrame`, the graphical user interface built with Swing.
- `com.cms.util`: Contains `DBConnection` for managing MySQL connections.

## Features
- **Create**: Add new products with name, price, quantity, and category.
- **Read**: View all products in a dynamic table.
- **Update**: Modify existing product details by selecting a row.
- **Delete**: Remove products from the database.
- **Search**: Filter products by name.

## How it Works
1. **Database Layer**: The `DBConnection` class uses JDBC to connect to the MySQL database `cms_db`.
2. **Data Access**: `ProductDAO` executes SQL queries (INSERT, SELECT, UPDATE, DELETE) using `PreparedStatement` to prevent SQL injection.
3. **Service Layer**: `ProductService` handles basic validation before passing data to the DAO.
4. **UI Layer**: `MainFrame` provides a user-friendly interface. It uses `JTable` to display data and `JTextField` for input. Event listeners on buttons trigger service methods and refresh the UI.

## Setup Instructions
1. Run the provided `db_setup.sql` in your MySQL server to create the database and table.
2. Ensure you have the MySQL JDBC Driver (`mysql-connector-java`) in your classpath.
3. Update the credentials in `com.cms.util.DBConnection` if necessary.
4. Run `com.cms.ui.MainFrame` to start the application.

## 📁 Project Structure

model    -> Product entity
dao      -> Database access (JDBC CRUD operations)
service  -> Business logic
ui       -> Java Swing user interface
util     -> Database connection

