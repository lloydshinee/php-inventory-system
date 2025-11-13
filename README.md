
# PHP Simple CRUD Project

This project is a simple web application that demonstrates how to perform CRUD (Create, Read, Update, Delete) operations using PHP and a MySQL database. It's designed for students to learn the basics of web development with these technologies.

## Current Status

The "Read" functionality is already implemented. The main page (`index.php`) displays a list of products from the database.

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

4.  **Create the Database and Table:**
    *   Open your web browser and go to `http://localhost/phpmyadmin/`.
    *   Create a new database. You can name it anything you like, for example, `your_name_db`. Remember this name as you will need to update `database.php` with it.
    *   Select the `lastname_db` database and go to the "SQL" tab.
    *   Run the following SQL query to create the `products` table:

        ```sql
        CREATE TABLE products (
            id INT(6) UNSIGNED AUTO_INCREMENT PRIMARY KEY,
            name VARCHAR(255) NOT NULL,
            price DECIMAL(10, 2) NOT NULL,
            quantity INT(10) NOT NULL,
            reg_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
        );
        ```

5.  **View the Project:**
    *   Open your web browser and navigate to `http://localhost/semblante_site/` (or the name you gave your project folder).
    *   You should see the project running, but with "0 results" since the database is empty.

## Your Task: Implement Full CRUD Functionality

Your main task is to implement the Create, Update, and Delete functionalities.

### 1. Create: Add New Products

*   Create a new PHP file (e.g., `create.php`) with an HTML form to add a new product. The form should have fields for `name`, `price`, and `quantity`.
*   The form should submit the data to a PHP script that inserts the new product into the `products` table.
*   Add a link or button on the `index.php` page to navigate to the "Add Product" page.

### 2. Update: Edit Existing Products

*   On the `index.php` page, add an "Edit" button next to each product.
*   This button should link to a new PHP file (e.g., `edit.php`) and pass the `id` of the product to be edited (e.g., `edit.php?id=1`).
*   The `edit.php` page should:
    *   Fetch the product's current data from the database.
    *   Display a form pre-filled with the product's information.
    *   Allow the user to modify the data and submit the form.
*   The form submission should update the product's record in the database.

### 3. Delete: Remove Products

*   On the `index.php` page, add a "Delete" button next to each product.
*   This button should trigger a PHP script that deletes the corresponding product from the database. You can pass the product `id` to a `delete.php` script (e.g., `delete.php?id=1`).
*   **Important:** For a better user experience, you can use JavaScript to show a confirmation dialog before deleting a product.

## File Structure

*   `index.php`: The main page that displays the list of products (Read).
*   `database.php`: Handles the connection to the MySQL database.
*   `style.css`: Contains the CSS styles for the project.
*   `create.php` (You need to create this)
*   `edit.php` (You need to create this)
*   `delete.php` (You need to create this)

Good luck!
