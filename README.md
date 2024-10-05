Creating a good README file for your GitHub repository is essential for conveying the purpose of your project and guiding users through the steps to replicate or use it. Here's a structured template you can follow to create a comprehensive README file for your web application deployment project:

# Web Application Deployment on Cloud VM

## Overview
This repository contains the steps and scripts to deploy a web application on a cloud Virtual Machine (VM) using Apache, PHP, and MariaDB. It includes the configuration of the server, database setup, and user registration functionality.

## Table of Contents
1. [Prerequisites](#prerequisites)
2. [Deployment Steps](#deployment-steps)
3. [Accessing the Web Application](#accessing-the-web-application)
4. [Database Structure](#database-structure)
5. [User Registration Functionality](#user-registration-functionality)
6. [Screenshots](#screenshots)
7. [Conclusion](#conclusion)

## Prerequisites
- A cloud VM (AWS EC2 instance recommended)
- SSH key pair for secure access
- Basic knowledge of Linux commands

## Deployment Steps

### Step 1: Log in to Cloud VM
- Opened Kali Linux terminal and logged into the cloud VM via SSH.
- Command:
  ```bash
  sudo ssh -i Documents/cloudkey.pem ec2-user@34.230.49.137
Step 2: Clone Repository
Cloned the repository from GitHub:
git clone https://github.com/AbhiramT21/webapp
Step 3: Copy Files to Apache Root Folder
Copied the cloned files to the Apache root folder:
sudo cp -r /home/ec2-user/webapp/cloudweb /var/www/html
Step 4: Start Apache Web Server
Installed and started the Apache web server:
sudo yum install httpd
sudo systemctl start httpd
Step 5: Configure Security Groups
Updated AWS instance Security Groups to allow HTTP and HTTPS traffic.
Step 6: Access Web Page
Accessed the deployed web page via a local web browser.
Step 7: Install PHP and MariaDB
Installed PHP:
sudo yum install php
Installed MariaDB Server:
sudo yum install mariadb105-server
Step 8: Start MariaDB Server
Started the MariaDB server and logged in:
sudo systemctl start mariadb
mysql -u root
Step 9: Create Database, Table, and User
Created a database and table:
CREATE DATABASE register;
USE register;
CREATE TABLE registration (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100),
    phone_number VARCHAR(15),
    password VARCHAR(255)
);
Step 10: Create User Registration Files
Developed PHP files for user registration and data handling.
Step 11: Log In as Created User
Demonstrated logging in with user credentials and data storage.
Step 12: Verify Accessibility
Verified accessibility using the public IP address: 44.211.206.95.
Database Structure
The database contains the following structure:

Database: register
Table: registration
Fields:
id: Unique identifier for each user.
name: User's full name.
email: User's email address.
phone_number: User's phone number.
password: User's hashed password.
User Registration Functionality
The application allows users to register with their name, email, phone number, and password. The data is securely stored in the MariaDB database.

Screenshots
Include screenshots demonstrating each step of the process here.

SSH Login: Screenshot-1
Repository Cloning: Screenshot-2
Copying Files: Screenshot-3
Starting Apache: Screenshot-4
Accessing Web Page: Screenshot-5
Creating Database: Screenshot-9
Creating Table: Screenshot-10
Conclusion
This document outlines the steps taken to successfully deploy a web application on a cloud VM. The application features user registration with data stored securely in a MariaDB database.

Feel free to contribute to this repository or reach out for any questions.


### Tips for Customization:
- **Personalize the Overview**: Add a brief description of the purpose of your web application and any specific technologies or frameworks used.
- **Add More Screenshots**: Include any additional relevant screenshots that could help visualize the steps taken.
- **Links to Documentation**: Consider linking to relevant documentation for Apache, PHP, or MariaDB for further reading.
- **Markdown Formatting**: Use proper Markdown formatting for code snippets, links, and images.

This template will help provide clear instructions and information about your project, making it easier for others to understand and use.
