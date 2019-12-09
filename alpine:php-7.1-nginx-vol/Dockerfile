FROM 'telkomindonesia/alpine:php-7.1-nginx'
MAINTAINER Donny Rhomanzah <donnyrhomanzah@gmail.com>

# install htop for debuging process
USER root

RUN apk --no-cache add htop nmap iputils

COPY ./etc/nginx/nginx.conf /etc/nginx/nginx.conf 
COPY ./etc/nginx/conf.d/default.conf /etc/nginx/conf.d/default.conf

WORKDIR /var/www/data/html
VOLUME /var/www/data/html


USER user
EXPOSE 8080