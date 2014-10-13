vagrant_lamp_php55
==================

Vagrant setup with Apache2, Mysql and php5.5
Just run vagrant up

If webroot can't be reached
===========================

1. vagrant ssh
2. sudo nano /etc/apache2/sites-available/10-default_vhost_80.conf
3. change to: Documentroot to /var/www/web
4. change to: Directory "/var/www/web"
5. change to: AllowOverride All
6. change to: ProxyPassMatch ^/(.*\.php(/.*)?)$ fcgi://127.0.0.1:9000/var/www/web/$1
7. save
8. sudo  /etc/init.d/apache2 restart

Connect to mysql with Sequal Pro
================================

1. connect using ssh
2. MySQL Host: 127.0.0.1
3. Usernaam: root
4. Password: root
5. SSH Host: 192.168.56.101 or configured ip
6. SSH User: Vagrant
7. SSH Key: .../dot/ssh/insecure_private_key
8. SSH Port: 22
