FROM alpine:3.8

LABEL maintainer="Janosch Kocsis <jk@coloso.de>"

RUN apk add --update nginx
RUN rm -rf /var/cache/apk/* && rm -rf /tmp/*

ADD nginx.conf /etc/nginx/
ADD nginx.conf /etc/nginx/conf.d/upstream.conf
ADD symfony.conf /etc/nginx/conf.d/default.conf

RUN echo "upstream php-upstream { server php:9001; }" > /etc/nginx/conf.d/upstream.conf

RUN adduser -D -g '' -G www-data www-data

CMD ["nginx"]

EXPOSE 80