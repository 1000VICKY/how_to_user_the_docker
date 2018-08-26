FROM centos:latest

# 作成したユーザの情報
MAINTAINER Admin <admin@admin.com>

RUN rpm -Uvh http://dev.mysql.com/get/mysql57-community-release-el7-7.noarch.rpm
RUN yum -y install mysql-community-server mysql mysql-devel
RUN yum -y install httpd httpd-devel php php-devel php-pdo php-mysql php-gd php-openssl which
RUN yum -y remove mariadb-libs && rm -rf /var/lib/mysql
EXPOSE 80

#CMD ["/usr/sbin/httpd", "-DFOREGROUND"]
ENTRYPOINT ["/usr/sbin/httpd", "-DFOREGROUND"]
