1. Install Apache Web Server \
  ` sudo apt install apache2 `\

2. Install PHP \
  ` sudo apt install php libapache2-mod-php php-mbstring php-xmlrpc php-soap php-gd php-xml php-cli php-zip php-bcmath php-tokenizer php-json php-pear `
    
3. Install a Database Manager \
 `  sudo apt install mariadb-server `\
 `  sudo mysql_secure_installation `\
 `  Remove anonymous users? [Y/n] y `\
 `  Disallow root login remotely? [Y/n] n `\
 `  Remove test database and access to it? [Y/n] y `\
 `  Reload privilege tables now? [Y/n] y ` 

4. Install Composer \
 `  curl -sS https://getcomposer.org/installer | php `\
 `  sudo mv composer.phar /usr/local/bin/composer `\
 `  sudo chmod +x /usr/local/bin/composer `

5. Install Laravel on Ubuntu Using Composer \
 `  cd /var/www/applikasi ` \
 `  composer update `

6. Using Laravel to Deploy an Application \
 `  sudo mv example /var/www/html/ `\
 `  sudo chgrp -R www-data /var/www/html/example/ `\
 `  sudo chmod -R 775 /var/www/html/example/storage `\
 `  cd /etc/apache2/sites-available `\
 `  sudo nano laravel_project.conf `\

 ```
       <VirtualHost *:80> 
          ServerName thedomain.com 
          ServerAdmin webmaster@thedomain.com 
          DocumentRoot /var/www/html/example/public 
          <Directory /var/www/html/example> 
             AllowOverride All 
          </Directory> 
          ErrorLog ${APACHE_LOG_DIR}/error.log 
          CustomLog ${APACHE_LOG_DIR}/access.log combined 
       </VirtualHost> 
```
    sudo a2dissite 000-default.conf
    Afterwards, enable the new virtual host:

    sudo a2ensite laravel_project

    Enable the Apache rewrite module, and finally, restart the Apache service
    sudo a2enmod rewrite
    sudo systemctl restart apache2
