# Day 18: Install and Configure DB Server


## 🐛Task



## 🛠️Solution

```ssh tony@stap01```

```sudo su -```

```yum install php php-opcache php-cli php-gd php-curl php-mysqlnd```

```yum install httpd -y```

```yum install mariadb-server mariadb -y```

```systemctl enable mariadb```

```systemctl restart mariadb```

```vi /etc/httpd/conf/httpd.conf``` change listen port then ```systemctl restart httpd```

```sudo -u root mysql;```

```craete database xxx;```

```show databases;```

```create user database-user with password 'xxx';```

```show databases;```

```GRANT ALL PRIVILEGES ON database.* TO 'username'@'%' IDENTIFIED BY 'password';```

```SELECT USER FROM,HOST FROM mysql.user;```

```SHOW GRANTS;```

```show databases;```

---
