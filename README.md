## Install nodejs V13.x
1. `curl -sL https://deb.nodesource.com/setup_13.x | bash -`
2. `apt-get install -y nodejs`

## Install PhpMyAdmin
1. `sudo apt install phpmyadmin`
2. `sudo systemctl restart apache2`
3. `sudo mysql -p`
4. `CREATE USER 'admin'@'localhost' IDENTIFIED BY 'password';`
5. `GRANT ALL PRIVILEGES ON *.* TO 'admin'@'localhost' WITH GRANT OPTION;`
