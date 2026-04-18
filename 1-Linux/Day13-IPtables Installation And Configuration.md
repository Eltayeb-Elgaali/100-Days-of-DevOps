# Day 13: IPtables Installation And Configuration


## 🐛Task
We have one of our websites up and running on our Nautilus infrastructure in Stratos DC. Our security team has raised a concern that right now Apache’s port i.e 8087 is open for all since there is no firewall installed on these hosts. So we have decided to add some security layer for these hosts and after discussions and recommendations we have come up with the following requirements:


1. Install iptables and all its dependencies on each app host.


2. Block incoming port 8087 on all apps for everyone except for LBR host.


3. Make sure the rules remain, even after system reboot.


## 🛠️Solution

```ssh tony@stapp01```

```sudo su -```

```cat /etc/*release*```

```yum install iptables-service -y```

```iptables -L -n```

```ss -tlun | grep 5000```

```systemctl iptables enable```

```systemctl iptables start```

```iptables --help```

```iptables -A INPUT -p tcp --dport 5000 -s stlb01 -j ACCEPT```

```iptables -A INPUT -p tcp --dport 5000 -s -j DROP```

```curl stapp01:5000```

```telnet stapp03 5000```

```yum install telnet -y```

```ssh loki@stlb01```

```iptables -L INPUT --line-numbers -n -v```

```iptables -D INPUT 5```

```service iptable save```

```systemctl iptables restart```

---
