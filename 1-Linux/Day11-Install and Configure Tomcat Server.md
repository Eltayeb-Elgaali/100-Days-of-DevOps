# Day 11: Install and Configure Tomcat Server


## 🐛Task
The Nautilus application development team recently finished the beta version of one of their Java-based applications, which they are planning to deploy on one of the app servers in Stratos DC. After an internal team meeting, they have decided to use the tomcat application server. Based on the requirements mentioned below complete the task:



a. Install tomcat server on App Server 2.

b. Configure it to run on port 6300.

c. There is a ROOT.war file on Jump host at location /tmp.


Deploy it on this tomcat server and make sure the webpage works directly on base URL i.e curl http://stapp02:6300


## 🛠️Solution

```ls -l /tmp```

```scp /tmp/ROOT.war steve@stapp02:/tmp```

```ssh steve@stapp02```

```ls -la /tmp```

```sudo systemctl status tomcat```

```cat /etc/*release*```

```sudo yum install tomcat -y```

```sudo systemctl status tomcat```

```vi /etc/tomcat/server.xml```

```sudo systemctl restart tomcat```

```curl http://stapp02:3001```

```sudo cp /tmp/ROOT.war /usr/share/tomcat/webapps```

```curl http://stapp02:3001```





---
