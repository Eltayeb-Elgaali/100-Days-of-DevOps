# Day 15: Setup SSL for Nginx


## 🐛Task
The system admins team of xFusionCorp Industries needs to deploy a new application on App Server 1 in Stratos Datacenter. They have some pre-requites to get ready that server for application deployment. Prepare the server as per requirements shared below:



1. Install and configure nginx on App Server 1.


2. On App Server 1 there is a self signed SSL certificate and key present at location /tmp/nautilus.crt and /tmp/nautilus.key. Move them to some appropriate location and deploy the same in Nginx.


3. Create an index.html file with content Welcome! under Nginx document root.


4. For final testing try to access the App Server 1 link (via hostname) from jump host using curl command. For example: curl -Ik https://<app-server-name>/. 


## 🛠️Solution

```curl -Ik https://stapp01```

```ssh tony@stapp01```

```sudo su -```

```ls -l /tmp```

```systemctl status nginx```

```yum install nginx -y```

```systemctl start nginx```

```curl -Ik https://stapp01```

```mv /tmp/nautilus.crt /etc/pki/tls/cert```

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
