# Day 1: Linux User Setup with Non-Interactive Shell


## 🐛Task
Create a user with non-interactive shell for your organization on a specific server.


## 🛠️Solution

```ssh user@server-name```

```sudo useradd -m -s /usr/sbin/nologin user-name```

```cat /etc/passwd```

```sudo su user-name```

```grep nologin /etc/passwd```

```id user-name```

```sudo userdel -r user-name```




---

