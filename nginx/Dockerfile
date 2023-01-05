FROM nginx:latest
RUN apt update && apt install php-fpm -y
RUN service php7.4-fpm start
RUN ls /run/php
WORKDIR /var/www/html
COPY . .
RUN chmod +x script.sh
RUN mv script.sh /docker-entrypoint.sh
RUN mv default.conf /etc/nginx/conf.d/default.conf
