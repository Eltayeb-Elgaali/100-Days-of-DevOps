# Day 3: Secure Root SSH Access


## 🐛Task
Disable all app server SSH root access.


## 🛠️Solution

```vi /etc/ssh/sshd_config```

```Set PermitRootLogin to no```

```sudo systemctl restart sshd```






---
