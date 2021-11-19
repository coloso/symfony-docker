FROM nginx:alpine

ADD nginx.conf /etc/nginx/
ADD symfony.conf /etc/nginx/conf.d/default.conf

EXPOSE 80

CMD ["nginx"]