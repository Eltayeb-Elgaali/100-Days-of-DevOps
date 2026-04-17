# Day 12: Linux Network Services


## 🐛Task
Create a user with non-interactive shell for your organization on a specific server.


## 🛠️Solution

```telnet stapp01 5003```

```ssh tony@stapp01```

```sudo su -```

```sudo systemctl status httpd```

```netstat -lntp | grep 5003```

```kill 444```

```netstat -lntp /grep 5003```

```sudo systemctl restart httpd```

```iptables -L -n```

```iptables -L -n -v```

```sudo iptables -A INPUT -p tcp --dport 5003 -j ACCEPT```

```iptables -L -n```

```sudo iptables -D INPUT -p tcp --dport 5003 -j ACCEPT```

```sudo iptables -I INPUT 1 -p tcp --dport 5003 -j ACCEPT```

```iptables -L -n```

```telnet stapp01 5003```

---
