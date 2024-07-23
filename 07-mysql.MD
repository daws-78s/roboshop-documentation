### MySQL
Developer has chosen the database MySQL. Hence, we are trying to install it up and configure it.

CentOS-8 Comes with MySQL 8 Version by default, However our application needs MySQL 5.7. So lets disable MySQL 8 version.


```
dnf install mysql-server -y
```

Start MySQL Service

```
systemctl enable mysqld
```
```
systemctl start mysqld
```

Next, We need to change the default root password in order to start using the database service. Use password RoboShop@1 or any other as per your choice.

```
mysql_secure_installation --set-root-pass RoboShop@1
```

You can check the new password working or not using the following command in MySQL.

```
mysql -uroot -pRoboShop@1
```