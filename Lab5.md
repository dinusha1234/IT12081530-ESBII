####NAME : K.D.D. Chathurangi

####REG.NO : IT12081530

####SUBJECT : ENTERPRISE STANDARDS AND BEST PRACTICES FOR IT INFRASTRUCTURE

####LAB : 05

#Install OwnCloud 7 on CentOS 7

##Prerequisites:

 * OwnCloud  is based on PHP and database combination, So install PHP, Apache web server and MySQL server on CentOS 7. 

#####yum install httpd php php-mysql mariadb-server mariadb sqlite php-dom php-mbstring php-gd php-pdo wget
![1](https://cloud.githubusercontent.com/assets/13193749/9330706/a6012740-45d8-11e5-9b5f-3c15845f4fd9.png)

![2](https://cloud.githubusercontent.com/assets/13193749/9330699/a5de76e6-45d8-11e5-88a4-5f6ddfb39347.png)

![3](https://cloud.githubusercontent.com/assets/13193749/9330708/a6068cda-45d8-11e5-8735-adf0d69a02a3.png)

* Set SELinux to allow OwnCloud to write the data.

#####setsebool -P httpd_unified 1

* Allow apache in firewall.
#####firewall-cmd --permanent --zone=public --add-service=http
#####firewall-cmd --permanent --zone=public --add-service=https
#####firewall-cmd --reload

![4](https://cloud.githubusercontent.com/assets/13193749/9330711/a617036c-45d8-11e5-9851-a162fde20adb.png)

* Start Apache and MariaDB.

#####systemctl start httpd.service
#####systemctl start mariadb.service

![5](https://cloud.githubusercontent.com/assets/13193749/9330709/a60cde1e-45d8-11e5-8a69-6fb228a42e2f.png)

* Auto start the service at system start-up.

#####systemctl enable httpd.service
#####systemctl enable mariadb.service

![6](https://cloud.githubusercontent.com/assets/13193749/9330710/a6116f24-45d8-11e5-9a1b-86b06b7696e6.png)

##Download and Setup:

* Download ownCloud from official website or enter the fallowing command on terminal.

#####wget https://download.owncloud.org/community/owncloud-7.0.0.tar.bz2

![7](https://cloud.githubusercontent.com/assets/13193749/9330712/a61821de-45d8-11e5-879c-0558e5855f8b.png)

###Extract the archive.

#####tar -jxvf owncloud-7.0.0.tar.bz2 -C /var/www/html/

* Allow the web server to read and write the files on cloud directory.

#####chown -R apache.apache /var/www/html/owncloud/

![8](https://cloud.githubusercontent.com/assets/13193749/9330694/a573d854-45d8-11e5-86a5-d97a826c419f.png)

##Create Database:

 * MariaDB server must be started before creating the database, login to MySQL server.

#####mysql -u root -p

* Create database called “clouddb”

#####create database clouddb;

* Allow “clouddbuser” to access the “clouddb” database on localhost with predefined password

#####grant all on clouddb.* to 'clouddbuser'@'localhost' identified by 'password';


![9](https://cloud.githubusercontent.com/assets/13193749/9330698/a5d948d8-45d8-11e5-8d6b-0974f4c731e8.png)
##Configure Apache server:

While configuring Apache web server, it is recommended that you to enable .htaccess to get a enhanced security features, by default .htaccess is disabled in Apache server. To enable it, open your virtual host file and make AllowOverride is set to All.For example, here i used external config file instead of modifying main file.

#####vi /etc/httpd/conf.d/owncloud.conf

* Add the following.

<IfModule mod_alias.c>
Alias /owncloud /var/www/html/owncloud
< /IfModule>
<Directory “/var/www/html/owncloud”>
Options Indexes FollowSymLinks
AllowOverride All
Order allow,deny
allow from all
</ Directory>


![10](https://cloud.githubusercontent.com/assets/13193749/9330697/a5d8c0fc-45d8-11e5-8608-5f4e287609bd.png)

* Remember to restart all services related to Apache server.

#####systemctl restart httpd.service

![11](https://cloud.githubusercontent.com/assets/13193749/9330701/a5e08f12-45d8-11e5-8c60-83fc17aa51c0.png)

##Configure ownCloud:

Open up web browser, point a URL to http://your-ip-address/owncloud ( http://Your-custom-domain). Browser will automatically take you to ownCloud setup page where it must be configured before going to live. Enter admin user name, password, data folder location and database details. You can choose any one of the database from SQLite or MySQL. If you choose SQLite database, you do not require to enter database details. where as MySQL database requires database user, password and data base name.


![12](https://cloud.githubusercontent.com/assets/13193749/9330695/a5a622e6-45d8-11e5-938e-bf8b53719bab.png)

![13](https://cloud.githubusercontent.com/assets/13193749/9330703/a5f391a2-45d8-11e5-9cd2-c76bcd67588f.png)
* Alternately you can download ownCloud client to upload the files.

![14](https://cloud.githubusercontent.com/assets/13193749/9330705/a5fafec4-45d8-11e5-89f2-efb3bc272753.png)

* Home page will look like this, you can start uploading the contents using upload button

![15](https://cloud.githubusercontent.com/assets/13193749/9330707/a6017c5e-45d8-11e5-9bd4-0f55af1d826f.png)
![16](https://cloud.githubusercontent.com/assets/13193749/9330704/a5f7e234-45d8-11e5-96c5-c529d3a83c45.png)