vagrant_lamp_php55
==================

Vagrant setup with Apache2, Mysql and php5.5
Just run vagrant up

If webroot can't be reached
===========================

1. vagrant ssh
2. sudo nano /etc/apache2/sites-available/10-default_vhost_80.conf
3. change to: Documentroot to /var/www/web
4. change to: <Directory "/var/www/web">
5. change to: ProxyPassMatch ^/(.*\.php(/.*)?)$ fcgi://127.0.0.1:9000/var/www/web/$1
6. save
7. sudo  /etc/init.d/apache2 restart
