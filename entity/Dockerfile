FROM nginx:stable-alpine3.19-slim
COPY ./nginx/nginx.conf /etc/nginx/nginx.conf
COPY ./nginx/sites-enabled /etc/nginx/sites-enabled
RUN mkdir -p /etc/pki/nginx/certs
RUN mkdir -p /etc/pki/nginx/private
RUN echo "$NGINX_SERVER_CERTIFICATE" > /etc/pki/nginx/certs/logserver.example.com.crt
RUN echo "$NGINX_PRIVATE_KEY_SECRET" > /etc/pki/nginx/private/logserver.example.com.key
