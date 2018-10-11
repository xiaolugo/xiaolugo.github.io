---
title: 搭建wordpress
layout: post
tags:
  - wordpress
category: it
---
# install lnmp
```bash
screen -S lnmp
wget -c http://soft.vpser.net/lnmp/lnmp1.4.tar.gz && tar zxf lnmp1.4.tar.gz && cd lnmp1.4 && ./install.sh
vim /usr/local/php/etc/php.ini
enable scandir
chattr +i /home/wwwroot/blog.daos.win/.user.ini
return 301 https://blog.daos.win$request_uri;
```
# download wordpress
```bash
cd /home/wwwroot/
wget http://wordpress.org/latest.tar.gz
tar -xzvf latest.tar.gz
chown -R www:www wordpress
```
# mysql
```bash
mysql -u root -p
CREATE DATABASE wordpress; 
GRANT ALL PRIVILEGES ON wordpress.* TO "username"@"localhost"
    
    -> IDENTIFIED BY "password";
FLUSH PRIVILEGES;
exit
```
