# Day 12: Linux Network Services


## 🐛Task
Our monitoring tool has reported an issue in Stratos Datacenter. One of our app servers has an issue, as its Apache service is not reachable on port 5004 (which is the Apache port). The service itself could be down, the firewall could be at fault, or something else could be causing the issue.

Use tools like telnet, netstat, etc. to find and fix the issue. Also make sure Apache is reachable from the jump host without compromising any security settings.

Once fixed, you can test the same using command curl http://stapp01:5004 command from jump host.

Note: Please do not try to alter the existing index.html code, as it will lead to task failure.


## 🛠️Solution

```telnet stapp01 5004```

```ssh tony@stapp01```

```sudo su -```

```sudo systemctl status httpd```

```sudo dnf install net-tools```

```netstat -lntp | grep 5004```

```kill 444```

```netstat -lntp /grep 5004```

```sudo systemctl restart httpd```

```iptables -L -n```

```iptables -L -n -v```

```sudo iptables -A INPUT -p tcp --dport 5004 -j ACCEPT```

```iptables -L -n```

```sudo iptables -D INPUT -p tcp --dport 500 -j ACCEPT```

```sudo iptables -I INPUT 1 -p tcp --dport 5004 -j ACCEPT```

```iptables -L -n```

```telnet stapp01 5003```

```curl http://stapp01:5004```

---
