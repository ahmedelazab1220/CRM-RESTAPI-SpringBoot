# CRM Web Application

This CRM (Customer Relationship Management) application is built using Spring Boot MVC, Spring Data Jpa, MySQL, and Java 21. The application provides a comprehensive solution for managing customer (Post , delete , get). 


# Prerequisites

Before installing the CRM application, ensure the following :

- Java 21 is installed on your machine.
- MySQL database is set up and running.
- Obtain valid MySQL connection details (URL, username, password).
- Use Postman to testing http://localhost:8081/api/customers

# Installation

To install and run the CRM application, follow these steps :

- Clone the repository from GitHub.
- Configure the MySQL database connection details in the `application.properties` file:

```

# (JDBC Properties - ) connect MySQL Database System To Java

spring.datasource.url=jdbc:mysql://localhost:3306/your_database_name?useSSL=false
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.jpa.hibernate.ddl-auto=update

# server port run app on it
# you can change this port , it's up to you
server.port=8081

```

Replace `your_username` and `your_password` with your MySQL database credentials.

Create this DataBase in MySQL Workbench or From Terminal.

![Database](https://github.com/ahmedelazab1220/CRM-RESTAPI-SpringBoot/assets/105994948/2be3574a-5716-47c2-9420-cb7b74b17732)

you can use this script in MySQL Workbench

```

drop database if exists `customer_management`;

create database if not exists  `customer_management`;

use `customer_management`;

drop table if exists `customer`;

create table `customer`(
   `id` int(11) NOT NULL AUTO_INCREMENT,
   `first_name` varchar(45) DEFAULT NULL,
   `last_name` varchar(45) DEFAULT NULL,
   `email` varchar(45) NOT NULL UNIQUE,
   PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=latin1;

INSERT INTO `customer` (`first_name`, `last_name`, `email`) VALUES
('John', 'Doe', 'johndoe@gmail.com'),
('Jane', 'Smith', 'janesmith1@gmail.com'),
('Alice', 'Johnson', 'alice_johnson@gmail.com'),
('Bob', 'Brown', 'bob.brown@gmail.com'),
('Emma', 'Davis', 'emma.davis@gmail.com');

```

# Postman

- you can use PostMan to test and determine any method you want (Post , Delete , Get).

Thank You.
