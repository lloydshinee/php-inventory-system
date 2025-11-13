# PHP Simple CRUD Project with Database Relationships

This project is a simple web application that demonstrates how to perform CRUD (Create, Read, Update, Delete) operations using PHP and a MySQL database. It's designed for students to learn the basics of web development with these technologies, including how to use foreign keys and joins to manage related data.

## Current Status

The "Read" functionality is already implemented for a single `products` table. The main page (`index.php`) displays a list of products from the database. Your task is to expand the database schema, implement full CRUD functionality, and use joins to display related data.

## Technologies Used

*   **PHP:** Server-side scripting language.
*   **MySQL:** Relational database management system (via XAMPP/MariaDB).
*   **HTML/CSS:** For the structure and styling of the web pages.
*   **XAMPP:** A local server environment that includes Apache and MySQL.

## Project Setup

To run this project on your local machine, follow these steps:

1.  **Install XAMPP:** If you don't have it already, download and install XAMPP from the [official website](https://www.apachefriends.org/index.html).

2.  **Place Project Files:**
    *   Navigate to your XAMPP installation directory.
    *   Place the entire project folder inside the `htdocs` directory (e.g., `C:\xampp\htdocs\your-project-folder`).

3.  **Start Apache and MySQL:**
    *   Open the XAMPP Control Panel.
    *   Start the "Apache" and "MySQL" modules.

4.  **Create the Database and Tables:**
    *   Open your web browser and go to `http://localhost/phpmyadmin/`.
    *   Create a new database. You can name it anything you like, for example, `your_name_db`. Remember this name as you will need to update `database.php` with it.
    *   Inside your new database, you will need to create the following tables: `categories`, `products`, `customers`, `orders`, and `order_items`.
    *   You will need to define the columns for each table and set up the relationships between them using foreign keys.

5.  **View the Project:**
    *   Open your web browser and navigate to `http://localhost/semblante_site/` (or the name you gave your project folder).
    *   You should see the project running, but with "0 results" since the database is empty.

## Your Task: Implement Full CRUD Functionality and Joins

Your main task is to implement the Create, Update, and Delete functionalities for the new tables and use `JOIN` clauses to display related data.

### 1. Manage Categories and Products (CRUD)

*   **Create:**
    *   Create a form to add new categories.
    *   Create a form to add new products, including a dropdown to select the product's category.
*   **Read:**
    *   On the `index.php` page, modify the query to use a `JOIN` to display the category name next to each product.
*   **Update:**
    *   Create a form to edit existing products, including their category.
*   **Delete:**
    *   Implement functionality to delete products.

### 2. Manage Customers and Orders

*   **Create:**
    *   Create a form to add new customers.
    *   Create a simple interface to create a new order for a customer, allowing them to select one or more products. This will involve inserting records into the `orders` and `order_items` tables.
*   **Read:**
    *   Create a page to display a list of all orders.
    *   For each order, display the customer's name and the total number of items. Use a `JOIN` to get the customer's name.
    *   Create a page to view the details of a single order, listing all the products in that order, their quantities, and prices. This will require `JOIN` operations across `orders`, `order_items`, and `products`.

## File Structure

*   `index.php`: The main page that displays the list of products (Read).
*   `database.php`: Handles the connection to the MySQL database.
*   `style.css`: Contains the CSS styles for the project.
*   You will need to create new files for the additional CRUD functionalities (e.g., `add_product.php`, `edit_product.php`, `manage_categories.php`, `view_orders.php`, etc.).

Good luck!
