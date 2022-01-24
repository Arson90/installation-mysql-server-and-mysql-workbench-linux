# installation-mysql-server-and-mysql-workbench-linux
## Index
* [Installation MySQL Server on Linux](#installation-mysql-server-on-linux)
* [Installation MySQL Workbench on Linux](#installation-mysql-workbench-on-linux)
* [Uninstall MySQL Workbench](#uninstall-mysql-workbench)
* [Troubleshooting](#troubleshooting)

## Installation MySQL Server on Linux
### Step by step
```
sudo apt-get update
```
```
sudo apt-get install mysql-server
```
```
systemctl is-active mysql
```
```
systemctl is-enabled mysql
```
```
sudo mysql_secure_installation
```
```
mysql -u root -p
```
## Installation MySQL Workbench on Linux
### Step by step
* download apt-repository - https://dev.mysql.com/downloads/repo/apt/
```
sudo apt install ./file from the link above
```
```
sudo apt update
```
```
sudo apt-get install mysql-workbench-community
```
```
mysql-workbench
```
## Uninstall MySQL Workbench
### Step by step
```
sudo systemctl stop mysql
```
```
sudo apt purge mysql-server mysql-client mysql-common mysql-server-core-* mysql-client-core-*
```
```
sudo rm -rf /etc/mysql /var/lib/mysql /var/log/mysql
```
```
sudo apt autoremove
```
```
sudo apt autoclean
```
## Troubleshooting
* IF YOU HAVE A PROBLEM TO ACCESS TO MySQL IN TERMINAL USE COMMANDS BELOW:
```
mysql -u root
```
```
ALTER USER 'root'@'localhost'IDENTIFIED WITH mysql_native_password BY 'you_super_password';
```
* IF YOU HAVE A PROBLEM WITH SETTING PASSWORD YOU CAN USE COMMANDS BELOW:
```
mysql -u root -p
```
Below command shows requirement concer the PASSWORD:
```
SHOW VARIABLES LIKE 'validate_password%'; 
```
You can change them, for example:
```
SET GLOBAL validate_password.length = 6;
SET GLOBAL validate_password.number_count = 0;
```
* IF YOU HAVE A PROBLEM WITH PASSWORD IN MYSQL_WORKBRENCH AND I CANNOT LOGIN, USE COMMAND BELOW:
```
sudo apt-get install gnome-keyring
```
