```sh
# base image
FROM centos

MAINTAINER iwe7 admin@meepo.com.cn

RUN yum install -y wget

RUN wget http://mirrors.linuxeye.com/oneinstack-full.tar.gz && tar xzf oneinstack-full.tar.gz && ./oneinstack/install.sh --nginx_option 1 --apache_option 1 --php_option 5 --phpcache_option 1 --php_extensions zendguardloader,ioncube,imagick,gmagick --phpmyadmin  --db_option 2 --dbinstallmethod 1 --dbrootpwd oneinstack --pureftpd  --redis  --memcached  --iptables  --reboot

```
