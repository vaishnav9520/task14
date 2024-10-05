Sure! Here’s a README template for your task 14 project. You can modify it as needed.

---

# Task 14: Cloud VM Setup and Web Development

## Overview
In this task, I will document the steps taken to set up a free virtual machine (VM) on a cloud platform (AWS/GCP/Azure), deploy a simple HTML page, and configure a PHP and MySQL environment. Screenshots are included to demonstrate each step.

## Steps Taken

### 1. Create a Free VM
- **Cloud Platform**: [Specify AWS/GCP/Azure]
- **Steps**:
  - Sign up for a free cloud account.
  - Navigate to the VM creation section.
  - Select a free tier instance type.
  - Configure the instance (OS, region, etc.).
  - Launch the instance.

### 2. SSH into the Cloud VM
- **Command Used**:
  ```bash
  ssh username@public-ip-address
  ```
- **Screenshot**: ![SSH Screenshot](path/to/your/ssh_screenshot.png)

### 3. Clone the Repository
- **Command**:
  ```bash
  git clone <repo-url>
  ```
- **Notes**: Cloned the repository containing the HTML page from Task 12.

### 4. Copy Files to Apache Web Server
- **Command**:
  ```bash
  sudo cp -r repo-folder/* /var/www/html/
  ```
- **Notes**: Copied all necessary files to the root folder of the Apache web server.

### 5. Start the Apache Web Server
- **Command**:
  ```bash
  sudo systemctl start apache2
  ```
- **Accessing the Web Page**:
  - Open a web browser and navigate to `http://public-ip-address`.
- **Screenshot**: ![Web Page Screenshot](path/to/your/web_page_screenshot.png)

### 6. Install PHP and MySQL
- **Commands**:
  ```bash
  sudo apt update
  sudo apt install php libapache2-mod-php mysql-server
  ```
- **Start MySQL Server**:
  ```bash
  sudo systemctl start mysql
  ```
- **Login to MySQL**:
  ```bash
  mysql -u root -p
  ```
- **Screenshot**: ![MySQL Screenshot](path/to/your/mysql_screenshot.png)

### 7. Create Database, Table, and User
- **Commands**:
  ```sql
  CREATE DATABASE mydatabase;
  CREATE TABLE mytable (id INT AUTO_INCREMENT PRIMARY KEY, username VARCHAR(255), password VARCHAR(255));
  CREATE USER 'myuser'@'localhost' IDENTIFIED BY 'mypassword';
  GRANT ALL PRIVILEGES ON mydatabase.* TO 'myuser'@'localhost';
  FLUSH PRIVILEGES;
  ```
- **Notes**: Successfully created the database and user.

### 8. PHP Files for User Registration
- **Steps**:
  - Created necessary PHP files for user registration.
  - Ensured they save data in the created database table.

### 9. User Login
- **Testing**:
  - Logged in as the user created.
- **Screenshot**: ![Login Screenshot](path/to/your/login_screenshot.png)

### 10. Public IP and Access
- **Public IP**: [Your Public IP]
- **Notes**: The web page is accessible to anyone with the IP address.

## Conclusion
Successfully set up a cloud VM, deployed a web application, and configured a PHP and MySQL environment. The application is publicly accessible, earning the Cloud Dweller badge!

## Files
- [Text File with Steps](path/to/your/steps.txt)
- [Screenshots](path/to/your/screenshots/)

---

Feel free to adjust any sections to better match your project details!
