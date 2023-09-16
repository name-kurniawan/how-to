## Cara install apache, mariadb, php dan phpmyadmin di Ubuntu adalah sebagai berikut:

1. Install apache2 \
   ` sudo apt-get install apache2 `
2. Install database server mariadb \
   ` sudo apt-get install mariadb-server mariadb-client ` \
   login ke mysql : \
   ` sudo mysql -u root ` \
   di dalam mysql server set password untuk user root \
   ` ALTER USER 'root'@'localhost' IDENTIFIED BY 'MyN3wP4ssw0rd';` \
   ` flush privileges;` \
   `  exit; `
4. install php \
   ` sudo apt-get install php php-mysql libapache2-mod-php php-cli php-cgi php-gd php-fpm `
5. install phpmyadm \
   ` sudo apt install phpmyadmin `
6. Restart apache \
   ` sudo systemctl restart apache2 `
7. Login ke phpmyadmin dengan user root dan pass MyN3wP4ssw0rd \
   ` http://ip-vps/phpmyadmin `
