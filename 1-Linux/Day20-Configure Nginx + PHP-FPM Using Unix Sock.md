# Day 20: Configure Nginx + PHP-FPM Using Unix Sock


## 🐛Task
The Nautilus application development team is planning to launch a new PHP-based application, which they want to deploy on Nautilus infra in Stratos DC. The development team had a meeting with the production support team and they have shared some requirements regarding the infrastructure. Below are the requirements they shared:



a. Install nginx on app server 3 , configure it to use port 8099 and its document root should be /var/www/html.


b. Install php-fpm version 8.1 on app server 3, it must use the unix socket /var/run/php-fpm/default.sock (create the parent directories if don't exist).


c. Configure php-fpm and nginx to work together.


d. Once configured correctly, you can test the website using curl http://stapp03:8099/index.php command from jump host.

NOTE: We have copied two files, index.php and info.php, under /var/www/html as part of the PHP-based application setup. Please do not modify these files.


## 🛠️Solution

```curl http://stapp03:8099/index.php```

```ssh banner@stapp03```

```sudo su -```

```yum install nginx -y```

```vi /etc/nginx/nginx.conf```

```root : /var/www/html index index.php index.html```

```systemctl restart nginx```

```yum update -y```

```dnf install https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm```

```dnf install https://rpms.remirepo.net/enterprise/remi-release-9.rpm```

```dnf module install php:remi-8.2```

```php -v```

```vi /etc/php-fpm.d/www.conf```

```systemctl restart php-fpm ```

```chown -R nginx:nginx /var/run/php-fpm/default.sock```

```nginx -t```

```curl http://stapp03:8099/index.php```

---
