
---
title: Wordpress with LNMP
layout: post
tags:
  - wordpress
category: it
---

# install lnmp
screen -S lnmp
wget -c http://soft.vpser.net/lnmp/lnmp1.4.tar.gz && tar zxf lnmp1.4.tar.gz && cd lnmp1.4 && ./install.sh
vim /usr/local/php/etc/php.ini
enable scandir
force https
chattr +i /home/wwwroot/blog.daos.win/.user.ini
return 301 https://blog.daos.win$request_uri;

# download wordpress
cd /home/wwwroot/
wget https://cn.wordpress.org/wordpress-4.9.1-zh_CN.zip
unzip wordpress-4.9.1-zh_CN.zip
chown -R www:www blog.daos.win

# mysql
mysql -u root -p
CREATE DATABASE wordpress; 
GRANT ALL PRIVILEGES ON wordpress.* TO "username"@"localhost"
    -> IDENTIFIED BY "password";
FLUSH PRIVILEGES;
exit