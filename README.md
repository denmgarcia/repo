# repo

In ubuntu 17, dockerized application with Nginx, Django and Mysql however running this gives an error in database

# mysql_upgrade -u root -p

will fixed an error

Mysql will not allow django to connect on this database, so we have to configure it

$ docker exec -it (name of your docker) bash

Here we will enter mysql inside dockerized mysql

> mysql -u root -p

>GRANT ALL PRIVILEGES ON myproject.* TO 'myprojectuser'@'%';  

>FLUSH PRIVILEGES;

This command allow django to connect to mysql
