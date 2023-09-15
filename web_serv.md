## Cara install apache, mariadb, php dan phpmyadmin di Ubuntu adalah sebagai berikut:

1. Install apache2 \
   ` sudo apt-get install apache2 `
2. Install database server mariadb \
   ` sudo apt-get install mariadb-server mariadb-client `
   ` sudo mysql -u root `
   di dalam mysql server set password untuk user root \
   ` ALTER USER 'root'@'localhost' IDENTIFIED BY 'MyN3wP4ssw0rd';` \
   ` flush privileges;` \
   `  exit; `
3. install php \
   ` sudo apt-get install php php-mysql libapache2-mod-php php-cli php-cgi php-gd `
4. install phpmyadm \
   ` sudo apt install phpmyadmin `
5. Restart apache \
   ` sudo systemctl restart apache2 `
6. Login ke phpmyadmin dengan user root dan pass MyN3wP4ssw0rd \
   ` http://ip-vps/phpmyadmin `
