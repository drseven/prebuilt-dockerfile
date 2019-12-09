FROM 'telkomindonesia/alpine:php-7.1-nginx'
MAINTAINER Donny Rhomanzah <donnyrhomanzah@gmail.com>

# install htop for debuging process
USER root

RUN apk --no-cache add htop nmap

COPY ./etc/nginx/nginx.conf /etc/nginx/nginx.conf 
COPY ./etc/nginx/conf.d/default.conf /etc/nginx/conf.d/default.conf
WORKDIR /var/www/data/html

RUN adduser -S app -G root

USER app
EXPOSE 8080


# # Set Labels Used in OpenShift to Describe the Builder Images
# LABEL release=1 \
#       vendor="Alpine" \
#       summary="Virtual Machine (VM) like container platform with Nginx 1.12.2 & PHP 7.1" \
#       maintainer="Donny Rhomanzah <donnyrhomanzah@gmail.com>" \
#       io.k8s.description="Alpine (3.x) with Nginx 1.12.2 & PHP 7.1" \
#       io.k8s.display-name="Alpine (3.x) with Nginx 1.12.2 & PHP 7.1" \
#       io.openshift.tags="builder,alpine,nginx,php" \
#       io.openshift.expose-services="80:http,443:https" \
#       io.openshift.non-scalable="false"