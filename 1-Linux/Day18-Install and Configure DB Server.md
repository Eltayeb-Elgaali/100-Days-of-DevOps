# Day 18: Install and Configure DB Server


## 🐛Task

- Install Mariadb server on database server
- Create database
- Create user with password
- Grant user all privileges



## 🛠️Solution

```ssh tony@stap01```

```sudo su -```

```yum install mariadb-server -y```

```systemctl enable mariadb```

```sudo -u root mysql;```

```CREATE DATABASE name;```

```SHOW DATABASES;```

```CREATE USER 'newuser'@'localhost' IDENTIFIED BY 'strong_password';```

```SELECT User, Host FROM mysql.user;```

```GRANT ALL PRIVILEGES ON database_name.* TO 'newuser'@'localhost';```

```SHOW GRANTS FOR 'username'@'localhost';```

---
