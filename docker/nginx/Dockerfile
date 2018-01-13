FROM nginx:latest

RUN apt-get update \
# install openssl
  && apt-get install -y --no-install-recommends openssl

# generate certificate
RUN openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/private/nginx-selfsigned.key -out /etc/ssl/certs/nginx-selfsigned.crt -subj "/C=DE/ST=Berlin/L=Berlin/O=Global Security/OU=IT Department/CN=example.com"