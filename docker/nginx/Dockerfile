FROM alpine:3.12

LABEL maintainer="Janosch Kocsis <jk@coloso.de>"

RUN addgroup -S www-data \
    && adduser -S -G www-data www-data

RUN apk add --update nginx
RUN rm -rf /var/cache/apk/* && rm -rf /tmp/*

ADD nginx.conf /etc/nginx/
ADD symfony.conf /etc/nginx/conf.d/default.conf
RUN echo "upstream php-upstream { server php:9000; }" > /etc/nginx/conf.d/upstream.conf

EXPOSE 80

CMD ["nginx"]