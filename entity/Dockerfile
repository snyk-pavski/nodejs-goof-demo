FROM nginx:stable-alpine3.19-slim@sha256:154e108059468bed12d676c3c446e4767db24d6099f09e92918d28e052960bf4
COPY ./nginx/nginx.conf /etc/nginx/nginx.conf
COPY ./nginx/sites-enabled /etc/nginx/sites-enabled
RUN mkdir -p /etc/pki/nginx/certs
RUN mkdir -p /etc/pki/nginx/private
RUN echo "$NGINX_SERVER_CERTIFICATE" > /etc/pki/nginx/certs/logserver.example.com.crt
RUN echo "$NGINX_PRIVATE_KEY_SECRET" > /etc/pki/nginx/private/logserver.example.com.key
