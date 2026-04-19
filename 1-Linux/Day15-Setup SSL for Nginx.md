# Day 15: Setup SSL for Nginx


## 🐛Task
Create 


## 🛠️Solution

```curl -Ik https://stapp01```

```ssh tony@stapp01```

```sudo su -```

```ls -l /tmp```

```systemctl status nginx```

```yum install nginx -y```

```systemctl start nginx```

```curl -Ik https://stapp01```

```mv /tmp/nautilus.cert /etc/pki/tls/certs```

```mv /tmp/nautilus.key /etc/pki/tls/private```

```ls -l /etc/pki/tls/certs | grep "nautilus.cert"```

```vi /etc/nginx/nginx.conf```

```modify server name: ip address```

```uncomment all settings for TLS enabled server```

```systemctl restart nginx```

```curl -Ik https://stapp01```

```ls -l /usr/share/nginx/html```

```rm -rf /usr/share/nginx/html/index.html```

```vi /usr/share/nginx/html/index.html```

```nginx -t```





---
