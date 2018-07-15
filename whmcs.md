### How to install WHMCS module

1. Locate whmcs installation directory on your server
2. Create vesta directory in the modules/server subdirectory
3. Download php module

##### Example

``` bash
cd /home/user/web/billing-site.ltd/public_html/modules/server
mkdir vesta
wget http://c.vestacp.com/0.9.8/rhel/whmcs-module.php -O vesta.php
```
The WHMCS plugin allows to manage servers running Vesta Control Panel. You can automatically create delete or suspend user accounts. Users are able to change passwords and manage their web/mail/dns domains.
