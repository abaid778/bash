# bash
## Reset Mysql Password
* `sudo service mysql stop` --- Stop the mysql
* `sudo mysqld --skip-grant-tables &` --- Start the mysql 
* `mysql -u root mysql` --- login to the mysql
* `UPDATE user SET Password=PASSWORD('new_password') WHERE user='root';` reset the password
* `FLUSH PRIVILEGES; ` --- refresh the mysql 
* `sudo service mysql start` --- Start the mysql
