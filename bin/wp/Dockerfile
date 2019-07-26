#wordpress
FROM wordpress:5.2.2-php7.2-apache

RUN apt-get update && apt-get install acl -y

COPY setuser.sh /var/www/html

RUN chmod +x /var/www/html/setuser.sh

# hacking into wordpress entry file 
# and adding my script right before the exit
RUN sed -i '/^exec "\$@"/i sh /var/www/html/setuser.sh' /usr/local/bin/docker-entrypoint.sh

WORKDIR /var/www/html/


 