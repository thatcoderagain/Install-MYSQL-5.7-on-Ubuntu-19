# Install MYSQL 5.7 on ubuntu 19.04 or 19.10 

### Before proceeding download all the packages into the system.


### Make sure no other version of MySQL is installed already if installed then remove completely. Then execute the following commands.

```
sudo apt-get autoclean && sudo apt-get clean && sudo apt-get update

sudo service mysql stop

sudo apt remove mysql-server mysql-server-8.0 mysql-server-core-8.0 mysql-client-8.0 mysql-client-core-8.0

sudo rm -rf /var/lib/mysql

sudo apt-get install -f

sudo dpkg -i libmysqlclient20_5.7.28-1ubuntu19.04_amd64.deb libmysqlclient-dev_5.7.28-1ubuntu19.04_amd64.deb libmysqld-dev_5.7.28-1ubuntu19.04_amd64.deb mysql-client_5.7.28-1ubuntu19.04_amd64.deb mysql-common_5.7.28-1ubuntu19.04_amd64.deb mysql-community-client_5.7.28-1ubuntu19.04_amd64.deb mysql-community-server_5.7.28-1ubuntu19.04_amd64.deb mysql-community-source_5.7.28-1ubuntu19.04_amd64.deb mysql-community-test_5.7.28-1ubuntu19.04_amd64.deb mysql-server_5.7.28-1ubuntu19.04_amd64.deb

sudo apt-get install -f

sudo service mysql status

sudo mysql_secure_installation

sudo mysql
```

# After the installation execute the following command to hold the package from automatic upgrade
```
sudo apt-mark hold libmysqlclient-dev
sudo apt-mark hold mysql-client
sudo apt-mark hold mysql-common
sudo apt-mark hold mysql-server
sudo apt list --upgradable
sudo apt upgrade
```
