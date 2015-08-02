# bash
## Reset Mysql Password ubuntu 14.04

* `sudo service mysql stop` --- Stop the mysql
* `sudo mysqld --skip-grant-tables &` --- Start the mysql 
* `mysql -u root mysql` --- login to the mysql
* `UPDATE user SET Password=PASSWORD('new_password') WHERE user='root';` reset the password
* `FLUSH PRIVILEGES; ` --- refresh the mysql 
* `sudo service mysql start` --- Start the mysql

## Create New DB mysql with username password

* `CREATE DATABASE DatabaseName;`
* `CREATE USER user@localhost IDENTIFIED BY 'Password';`
* `GRANT ALL PRIVILEGES ON DatabaseName.* TO user@localhost IDENTIFIED BY 'Password';`

## /casper/vmlinuz: file not found ubuntu boot

I was facing issue with new install on ubuntu 14.04 from USB /casper/vmlinuz: file not found
* `cd /casper &&  cp vmlinuz.efi vmlinuz ` --- we have a file name /casper/vmlinuz.efi which should be vmlinuz and rename was not working in that case so we need to cp of that file and it works

## Convert Text file to pdf file on ubuntu 14.04

*  `sudo apt-get install enscript ghostscript` 
*  `enscript -p output.ps coverletter`
*  `ps2pdf output.ps coverletter.pdf`
