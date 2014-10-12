FROM centos:centos6
MAINTAINER asola@....co.uk

RUN yum update -y
RUN yum install -y httpd
RUN yum install -y php
RUN yum install -y mysql-server
RUN yum install -y php-mysql
RUN yum install -y git
RUN curl -sS https://getcomposer.org/installer | php
ADD ssh/* /root/.ssh/
RUN git clone git@bitbucket.org:lylessutherland/brightcare.git /var/www/html/
RUN cd /var/www/html; php -e memory_limit=2G /composer.phar install
