# Lab 1: Containerization

## 1. Docker command to create and run a container named `dbserver-mysql-nairobi`

Use the `customized-ubuntu:1.0` image to create a container named `dbserver-mysql-nairobi`. The command should map the container’s port 3306 to the host’s port 3309.

```dockerfile
#navigate to the specific folder  
 cd images/ubuntu 
 #build 
 docker build -t customized-ubuntu:1.0.
 # naming container and assigning ports 
 docker run -d --name dbserver-mysql-nairobi -p 3309:3306 customized-ubuntu:1.0 tail -f /dev/null


```

## 2. MySQL Server and MySQL Client Installation in Ubuntu

```shell
Specify your commands here
#enter running container 
docker run -it --name dbserver-mysql-nairobi -p 3309:3306 customized -ubuntu:1.0 bash 

#inside the container 
apt-get update 
apt-get intall -y mysql-server mysql-cient 
#secure mysql and password 
service mysql start 
login to MYSQL
mysql -u root 
change the root password inside the MYSQL shell:

## 3. Login using the MySQL Client and Change the MySQL Root Password

```sql
Specify your commands here
#in sql
ALTER USER 'root'@'loacalhost' IDENTIFIED WITH mysql_native_password BY '5trathmore';
FLUSH PRIVILEGES
exit 
#lab completed well 
