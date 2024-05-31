# Library Management System

## Introduction
This Library Management System is a web-based application designed to manage and automate the operations of a library. It is built using PHP for the server-side scripting and MySQL for the database management. This system helps in managing books, users (members), and transactions efficiently.

## Features
- **Admin Panel**: For managing books, users, and viewing transaction history.
- **User Panel**: For viewing available books, borrowing books, and viewing borrowing history.
- **Book Management**: Add, update, delete, and search books.
- **User Management**: Add, update, delete, and search users.
- **Transaction Management**: Record book borrowing and returns.
- **Login System**: Separate login for admin and users.
- **Responsive Design**: Accessible from both desktop and mobile devices.

## Requirements
- **Server**: Apache or any other web server supporting PHP.
- **PHP**: Version 7.0 or higher.
- **Database**: MySQL 5.6 or higher.
- **Browser**: Modern web browser (Chrome, Firefox, Safari, etc.).

## Installation
1. **Download and Extract**
   - Download the project files and extract them to your web server's root directory (e.g., `htdocs` for XAMPP, `www` for WAMP).

2. **Database Setup**
   - Create a MySQL database for the system.
   - Import the `library.sql` file located in the `database` directory into your database.

   ```sql
   CREATE DATABASE library_db;
   USE library_db;
   SOURCE /path/to/library.sql;
   ```

3. **Configuration**
   - Open the `config.php` file in the `includes` directory.
   - Update the database configuration settings with your MySQL database credentials.

   ```php
   <?php
   // Database configuration
   define('DB_SERVER', 'localhost');
   define('DB_USERNAME', 'root');
   define('DB_PASSWORD', '');
   define('DB_NAME', 'library_db');

   // Attempt to connect to MySQL database
   $link = mysqli_connect(DB_SERVER, DB_USERNAME, DB_PASSWORD, DB_NAME);

   // Check connection
   if($link === false){
       die("ERROR: Could not connect. " . mysqli_connect_error());
   }
   ?>
   ```

4. **Access the System**
   - Open your web browser and navigate to `http://localhost/library-management-system`.
   - Login using the following credentials:
     - Admin: `admin` / `admin123`
     - User: `user` / `user123`

## Directory Structure
```
library-management-system/
├── assets/
│   ├── css/
│   ├── js/
│   └── images/
├── includes/
│   ├── config.php
│   ├── functions.php
│   └── header.php
├── admin/
│   ├── add_book.php
│   ├── add_user.php
│   ├── dashboard.php
│   ├── edit_book.php
│   ├── edit_user.php
│   ├── view_books.php
│   └── view_users.php
├── user/
│   ├── dashboard.php
│   ├── borrow_book.php
│   ├── return_book.php
│   └── view_books.php
├── database/
│   └── library.sql
├── index.php
├── login.php
└── logout.php
```

## Usage
1. **Admin Operations**
   - Login to the admin panel to add, edit, and delete books and users.
   - View the list of all books and users.
   - Monitor book borrow and return transactions.

2. **User Operations**
   - Login to the user panel to view available books.
   - Borrow and return books.
   - View borrowing history.

## Contributing
Contributions are welcome! Please fork this repository and submit a pull request with your improvements.

## License
This project is licensed under the MIT License.

## Contact
For any questions or suggestions, please contact [your email].

---

This README file provides the necessary steps to set up and use the Library Management System. Make sure to follow each step carefully to ensure the system functions correctly. Enjoy managing your library with ease!
