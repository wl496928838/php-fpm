# php-fpm
适合中国用的php-fpm

基于官方php-fpm镜像制作，https://hub.docker.com/_/php/

因此版本使用最新的fpm。

# 使用镜像说明

已经安装了 pdo gdi 基本满足功能。

你只需要把代码放进去就好啦。

本仓库里面有php-fpm.conf,php.ini。如果你需要定制配置请下载回来以后。自行修改。


```
# 把本地代码copy进去
COPY ./app /var/www/html/

# 不给权限创建不了文件
RUN chmod -R 777 /var/www/html/*

# 设置php-fpm.conf
COPY php-fpm.conf /usr/local/etc

# 设置php.ini
COPY php.ini /usr/local/etc/php
```
