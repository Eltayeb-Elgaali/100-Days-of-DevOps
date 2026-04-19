# Day 14: Linux Process Troubleshooting


## 🐛Task
The production support team of xFusionCorp Industries has deployed some of the latest monitoring tools to keep an eye on every service, application, etc. running on the systems. One of the monitoring systems reported about Apache service unavailability on one of the app servers in Stratos DC.


Identify the faulty app host and fix the issue. Make sure Apache service is up and running on all app hosts. They might not have hosted any code yet on these servers, so you don't need to worry if Apache isn't serving any pages. Just make sure the service is up and running. Also, make sure Apache is running on port 3002 on all app servers.


## 🛠️Solution

```ssh tony@stapp01```

```sudo su -```

```systemctl status httpd```

```ss -tlpn | grep 3002```

```kill 2738```

```systemctl restart httpd```

```curl stapp01:3002```




---
