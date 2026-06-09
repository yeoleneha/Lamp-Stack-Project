# 🚀 LAMP Stack Deployment on AWS EC2

## 📌 Project Overview

This project demonstrates the deployment and configuration of a LAMP Stack (Linux, Apache, MariaDB, and PHP) on an AWS EC2 instance. The objective of this project is to create a fully functional web server environment capable of hosting dynamic PHP-based web applications.

The LAMP stack is one of the most widely used open-source web application platforms and serves as the foundation for many modern websites and applications.

---

## 🎯 Project Objectives

* Launch and configure an AWS EC2 instance.
* Install and configure Apache Web Server.
* Install and configure MariaDB Database Server.
* Install PHP and integrate it with Apache.
* Verify PHP functionality.
* Host a sample website.
* Understand cloud-based web server deployment.

---

## 🏗️ Architecture Diagram

> Architecture Diagram uploaded in this repository.

Flow:

User Browser
↓
Apache Web Server
↓
PHP Application
↓
MariaDB Database

---

## ✨ Key Features

* Cloud-based deployment using AWS EC2.
* Apache web server configuration.
* MariaDB database integration.
* PHP support for dynamic web pages.
* Secure access through AWS Security Groups.
* Sample website hosting.
* Basic troubleshooting and validation.

---

## 🛠️ Technologies Used

| Technology         | Purpose                |
| ------------------ | ---------------------- |
| AWS EC2            | Virtual Server         |
| Amazon Linux       | Operating System       |
| Apache HTTP Server | Web Server             |
| MariaDB            | Database Server        |
| PHP                | Server-side Scripting  |
| Security Groups    | Network Access Control |

---

## 📋 Prerequisites

Before starting this project:

* AWS Account
* EC2 Instance (Amazon Linux)
* Basic Linux Knowledge
* Internet Connection
* Security Group with required ports open

Required Ports:

| Port | Protocol | Purpose            |
| ---- | -------- | ------------------ |
| 22   | SSH      | Remote Access      |
| 80   | HTTP     | Web Traffic        |
| 443  | HTTPS    | Secure Web Traffic |

---

## ⚙️ Implementation Steps

### Step 1: Launch EC2 Instance

* Login to AWS Console.
* Navigate to EC2 Dashboard.
* Launch Amazon Linux Instance.
* Configure Security Group.
* Allow Ports 22, 80 and 443.

---

### Step 2: Connect to EC2

Connect using EC2 Instance Connect or SSH.

Update the system:

```bash
sudo yum update -y
```

---

### Step 3: Install Apache

```bash
sudo yum install httpd -y
```

Start Apache:

```bash
sudo systemctl start httpd
```

Enable Apache:

```bash
sudo systemctl enable httpd
```

Verify Status:

```bash
sudo systemctl status httpd
```

---

### Step 4: Install MariaDB

```bash
sudo yum install mariadb105-server -y
```

Start MariaDB:

```bash
sudo systemctl start mariadb
```

Enable MariaDB:

```bash
sudo systemctl enable mariadb
```

Verify Status:

```bash
sudo systemctl status mariadb
```

---

### Step 5: Install PHP

```bash
sudo yum install php php-mysqlnd -y
```

Restart Apache:

```bash
sudo systemctl restart httpd
```

---

### Step 6: Verify PHP Installation

Create PHP Test File:

```bash
sudo vi /var/www/html/info.php
```

Add:

```php
<?php
phpinfo();
?>
```

Access:

http://YOUR_PUBLIC_IP/info.php

---

### Step 7: Host Sample Website

Create:

```bash
sudo vi /var/www/html/index.html
```

Add sample HTML content and save.

Access:

http://YOUR_PUBLIC_IP

---

## 📸 Project Screenshots

The repository contains screenshots of:

* EC2 Instance Running
* EC2 Connection
* Security Group Configuration
* Apache Installation
* Apache Running Status
* Apache Webpage
* MariaDB Running Status
* PHP Information Page
* Final Website Output

---

## ✅ Project Outcome

Successfully deployed and configured a complete LAMP Stack environment on AWS EC2.

The web server was able to:

* Serve web pages through Apache.
* Execute PHP scripts.
* Integrate with MariaDB database.
* Host a sample website successfully.

---

## 📚 Learning Outcomes

Through this project, I learned:

* AWS EC2 Management
* Linux Administration
* Apache Configuration
* Database Management using MariaDB
* PHP Integration
* Cloud Infrastructure Basics
* Troubleshooting Web Server Issues

---

## 🚀 Future Enhancements

Possible future improvements:

* Configure HTTPS using SSL/TLS.
* Deploy a WordPress application.
* Integrate automated backups.
* Implement monitoring using AWS CloudWatch.
* Configure Load Balancer.
* Deploy the application using Docker containers.
* Implement CI/CD using Jenkins and GitHub Actions.

