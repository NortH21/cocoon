FROM nginx:alpine

RUN apk add --no-cache certbot certbot-nginx

RUN echo "0	0	*	*	*	/usr/bin/certbot renew --quiet" >> /etc/crontabs/root

#COPY ./config/default.conf /etc/nginx/conf.d/default.conf
#COPY ./config/nginx.conf /etc/nginx/nginx.conf

EXPOSE 80/tcp 443/tcp

CMD ["sh", "-c", "crond && nginx -g 'daemon off;'"]

