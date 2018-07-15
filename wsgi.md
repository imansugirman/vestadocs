### How to enable WSGI support on a Debian or Ubuntu
#### 1. Install wsgi apache module

``` bash
apt-get install libapache2-mod-wsgi
a2enmod wsgi
```
#### 2. Download wsgi template
``` bash
cd /usr/local/vesta/data/templates/web
wget http://c.vestacp.com/0.9.8/ubuntu/wsgi/apache2.tar.gz
tar -xzvf apache2.tar.gz
rm -f apache2.tar.gz
```

#### 3. Create new package or set wsgi as apache template in the existing package
#### 4. Add new user and assing him package with wsgi template
#### 5. Add new domain and check the result
