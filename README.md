# Dockerfile

##Dockerfile for images

contains base image and application image

##centos web

###web.nginx

create image
<code>
$ docker build -t="web:nginx" web.nginx/
</code>

create container
<code>
$ docker run -d -p8080:80 --name="web1" -v /data/www:/data/www web:nginx nginx 
</code>

test
<code>
curl 127.0.0.1:8080
</code>


##centos php-fpm

##centos mysql

##centos ipvsadm
