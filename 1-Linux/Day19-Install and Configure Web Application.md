# Day 19: Install and Configure Web Application.md


## 🐛Task
xFusionCorp Industries is planning to host two static websites on their infra in Stratos Datacenter. The development of these websites is still in-progress, but we want to get the servers ready. Please perform the following steps to accomplish the task:


a. Install httpd package and dependencies on app server 1.


b. Apache should serve on port 3003.


c. There are two website's backups /home/thor/news and /home/thor/demo on jump_host. Set them up on Apache in a way that news should work on the link http://localhost:3003/news/ and demo should work on link http://localhost:3003/demo/ on the mentioned app server.


d. Once configured you should be able to access the website using curl command on the respective app server, i.e curl http://localhost:3003/news/ and curl http://localhost:3003/demo/

## 🛠️Solution

```scp /home/thor/news/index.html tony@stapp01:/tmp```

```ssh tony@stapp01```

```sudo su -```

```yum install httpd```

```sudo systemctl enable httpd```

```vi /etc/httpd/httpd.conf```

```mv /tmp/index.html /var/www/html/apps```

```mv /tmp/index.html /var/www/html/media```

```curl http://localhost:3003/news/```



---
