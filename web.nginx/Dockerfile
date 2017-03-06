#Docker images for centos web server
#Version 0.02
FROM centos
MAINTAINER IsCod "iscodd@gmail.com"

#ENV
ENV REFRESHED_AT 2017-03-05
ENV INSTALL_DIR /usr/local/src/

#update centos system
RUN yum update -y && yum clean all
RUN yum install -y vim && yum install -y wget && yum install -y iproute

#start install nginx
#USER nginx
WORKDIR $INSTALL_DIR
ARG nginxnoarch=http://nginx.org/packages/centos/7/noarch/RPMS/nginx-release-centos-7-0.el7.ngx.noarch.rpm
RUN rpm -ivh $nginxnoarch && yum install -y nginx
RUN nginx

EXPOSE 80
