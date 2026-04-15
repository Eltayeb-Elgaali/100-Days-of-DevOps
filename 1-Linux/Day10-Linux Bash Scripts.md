# Day 10: Linux Bash Scripts
## 🐛Task
The production support team of xFusionCorp Industries is working on developing some bash scripts to automate different day to day tasks. One is to create a bash script for taking websites backup. They have a static website running on App Server 1 in Stratos Datacenter, and they need to create a bash script named official_backup.sh which should accomplish the following tasks. (Also remember to place the script under /scripts directory on App Server 1).



a. Create a zip archive named xfusioncorp_official.zip of /var/www/html/official directory.


b. Save the archive in /backup/ on App Server 1. This is a temporary storage, as backups from this location will be cleaned on a weekly basis. Therefore, we also need to save this backup archive on Nautilus Storage Server.


c. Copy the created archive to Nautilus Storage Server server in /backup/ location.


d. Please make sure script won't ask for password while copying the archive file. Additionally, the respective server user (for example, tony in case of App Server 1) must be able to run it.


e. Do not use sudo inside the script.

Note:
The zip package must be installed on given App Server before executing the script. This package is essential for creating the zip archive of the website files. Install it manually outside the script.


## 🛠️Solution
```sudo su -```

```ls -la /scripts```

```ls -la /backup```

```cat /var/www/html/official/index.html```

```grep nologin /etc/passwd```

```id user-name```

```sudo userdel -r user-name```


```vi /scripts/official_backup.sh```

```#!/bin/bash
echo "zip archiving file..."
zip -r /backup/xfusioncorp_official.zip /var/www/html/official
echo "copying zip archive..."
scp /backup/xfusioncorp_official.zip natasha@ststor01:/backup
echo "successfuly copied zip archive into backup server"```


```chmod +x /scripts/official_backup.sh```
```ls -la```


```ssh-keygen -t rsa```
```ssh-copy-id natasha@ststor01```

```ssh natasha@ststor01```
```ls -la /backup```

exit

bash /scripts/official_backup.sh

ssh natasha@ststor01


ls -la /backup

