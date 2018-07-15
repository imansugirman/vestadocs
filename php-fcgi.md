### How to enable PHP-FCGI support on a RHEL or CentOS
* This tutorial is created for servers with less than 1Gb of ram avaialbe. On "medium" servers installation is fully automatic.
1. Install fcgid apache module
``` bash
apt-get install libapache2-mod-fcgid
a2enmod fcgid
```
2. Download fcgid template

``` bash
cd /usr/local/vesta/data/templates/web
wget http://c.vestacp.com/0.9.8/ubuntu/fcgid/apache2.tar.gz
tar -xzvf apache2.tar.gz
rm -f apache2.tar.gz
```
3. Create new package or set phpfcgid as apache template in the existing package
4. Add new user and assing him package with phpfcgid template
5. Add new domain and check the result
