# php-fpm
适合中国用的php-fpm

# 使用镜像说明

时区已经设置好了

```
# 把本地代码copy进去
COPY ./app /var/www/html/

# 不给权限创建不了文件
RUN chmod -R 777 /var/www/html/*

```
