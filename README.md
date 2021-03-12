## Remove sudo
1. `sudo -i`

## Home
1. `nano /etc/motd`

## Change language système
1. `dpkg-reconfigure locales`

## Install Curl
1. apt install curl

## Install nodejs V13.x
1. `curl -sL https://deb.nodesource.com/setup_13.x | bash -`
2. `apt-get install -y nodejs`

## Install Git
1. `apt install git`

## Install apache2 & PhpMyAdmin
1. `apt install apache2 php php-json php-mbstring php-zip php-gd php-xml php-curl php-mysql`
2. `wget https://files.phpmyadmin.net/phpMyAdmin/4.9.0.1/ phpMyAdmin-4.9.0.1-all-languages.zip`
3. `unzip phpMyAdmin-4.9.0.1-all-languages.zip -d /opt`
4. `ls -lh /opt`
5. `mv -v /opt/phpMyAdmin-4.9.0.1-all-languages /opt/phpMyAdmin`
6. `chown -Rfv www-data:www-data /opt/phpMyAdmin`
7. `nano /etc/apache2/sites-available/phpmyadmin.conf`
```htlm
<VirtualHost *:9000>
ServerAdmin webmaster@localhost
DocumentRoot /opt/phpMyAdmin
 
<Directory /opt/phpMyAdmin>
Options Indexes FollowSymLinks
AllowOverride none
Require all granted
</Directory>
ErrorLog ${APACHE_LOG_DIR}/error_phpmyadmin.log
CustomLog ${APACHE_LOG_DIR}/access_phpmyadmin.log combined
</VirtualHost>
```
8. `CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';`
5. `GRANT ALL PRIVILEGES ON *.* TO 'admin'@'localhost' WITH GRANT OPTION;`

## Install MariaDB
1. `apt install mariadb-server mariadb-client`
2. `systemctl status mariadb`
3. `systemctl start mariadb`
4. `mysql_secure_installation`
5. `mysql -u (username) -p`
6. `GRANT ALL ON *.* TO 'username'@'localhost' IDENTIFIED BY 'password';`

## Install PhpMyAdmin
1. `sudo apt install phpmyadmin`
2. `sudo systemctl restart apache2`
3. `sudo mysql -p`
4. `CREATE USER 'admin'@'localhost' IDENTIFIED BY 'password';`
5. `GRANT ALL PRIVILEGES ON *.* TO 'admin'@'localhost' WITH GRANT OPTION;`

## Install GTOP
1. `npm install -g gtop`

## Msq Safe Mode
1. etc/init.d/mysql stop
2. mysqld_safe --skip-grant-tables &
3. mysql -u root
4. use mysql;
5. update user set password=PASSWORD("PASSWORD") where user="USERNAME";
6. flush privileges;
7. quit
8. /etc/init.d/mysql stop
9. /etc/init.d/mysql start
