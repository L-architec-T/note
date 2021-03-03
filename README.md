## Remove sudo
1. `sudo -i`

## Install nodejs V13.x
1. `curl -sL https://deb.nodesource.com/setup_13.x | bash -`
2. `apt-get install -y nodejs`

## Install MariaDb
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
