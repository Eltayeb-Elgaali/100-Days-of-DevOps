# Day 9: MariaDB Troubleshooting


## 🐛Task
There is a critical issue going on with the Nautilus application in Stratos DC. The production support team identified that the application is unable to connect to the database. After digging into the issue, the team found that mariadb service is down on the database server.



Look into the issue and fix the same.


## 🛠️Solution

```ssh peter@stdb01```

```sudo systemctl status mariadb```

```sudo systemctl restart mariadb```

```journalctl -xe | grep mariadb ```

```ls -ld /var/lib/mysql```

```sudo chown mysql:mysql mysql```

```sudo systemctl restart mariadb```

```sudo systemctl status mariadb```






---
