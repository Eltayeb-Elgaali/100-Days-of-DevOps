# Day 13: IPtables Installation And Configuration


## 🐛Task
We have one of our websites up and running on our Nautilus infrastructure in Stratos DC. Our security team has raised a concern that right now Apache’s port i.e 8087 is open for all since there is no firewall installed on these hosts. So we have decided to add some security layer for these hosts and after discussions and recommendations we have come up with the following requirements:


1. Install iptables and all its dependencies on each app host.


2. Block incoming port 6400 on all apps for everyone except for LBR host.


3. Make sure the rules remain, even after system reboot.


## 🛠️Solution

```ssh tony@stapp01```

```sudo su -```

```cat /etc/*release*```

```yum install iptables iptables-services -y```

```systemctl enable --now iptables```

```systemctl status iptables```

```iptables -L -n --line-numbers```

```ss -tlun | grep 6400```

```iptables -I INPUT 5 -p tcp --dport 6400 -s stlb01 -j ACCEPT```

```iptables -I INPUT 6 -p tcp --dport 6400 -j DROP```

```iptables -D INPUT 3```

```iptables-save > /etc/sysconfig/iptables``` 

```curl stapp01:6400```

```telnet stapp03 6400```










---
