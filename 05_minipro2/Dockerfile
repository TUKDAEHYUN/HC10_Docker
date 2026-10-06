FROM quay.io/centos/centos:stream10

RUN dnf -y install httpd php php-fpm php-cli php-common php-mysqlnd php-opcache \
    && dnf clean all

ADD src.tar /var/www/html
COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh

VOLUME /var/www/html /var/log/httpd
EXPOSE 80

ENTRYPOINT ["/entrypoint.sh"]