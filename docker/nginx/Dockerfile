FROM alpine:3.11

LABEL maintainer="Janosch Kocsis <jk@coloso.de>"

RUN addgroup -S www \
    && adduser -S -G www www

RUN apk add --update nginx
RUN rm -rf /var/cache/apk/* && rm -rf /tmp/*

ADD nginx.conf /etc/nginx/
ADD symfony.conf /etc/nginx/conf.d/default.conf
RUN echo "upstream php-upstream { server php:9001; }" > /etc/nginx/conf.d/upstream.conf

EXPOSE 80

CMD ["nginx"]