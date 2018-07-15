#### ClamAV Installation Ubuntu

``` bash
apt-get install clamav-daemon
wget http://c.vestacp.com/0.9.8/ubuntu/clamd.conf -O /etc/clamav/clamd.conf
gpasswd -a clamav mail
gpasswd -a clamav Debian-exim
freshclam
update-rc.d clamav-daemon defaults
service clamav-daemon restart
```
#### SpamAssassin Installation Ubuntu

``` bash
apt-get install spamassassin
update-rc.d spamassassin defaults
sed -i "s/ENABLED=0/ENABLED=1/" /etc/default/spamassassin
service spamassassin restart
```
#### Exim Configuration
``` bash
sed -i "s/^#SPAMASSASSIN/SPAMASSASSIN/g" /etc/exim4/exim4.conf.template
sed -i "s/^#CLAMD/CLAMD/g" /etc/exim4/exim4.conf.template
sed -i "s/^#SPAM_SCORE/SPAM_SCORE/g" /etc/exim4/exim4.conf.template
service exim4 restart
```
#### Vesta Configuration
``` bash
sed -i "s/ANTIVIRUS.*/ANTIVIRUS_SYSTEM='clamav-daemon'/" /usr/local/vesta/conf/vesta.conf
sed -i "s/ANTISPAM.*/ANTISPAM_SYSTEM='spamassassin'/" /usr/local/vesta/conf/vesta.conf
```
