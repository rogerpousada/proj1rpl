FROM nginx:1.14.0

RUN rm /etc/nginx/conf.d/default.conf
ADD nginx.conf /etc/nginx/
ADD notes.conf /etc/nginx/conf.d/

CMD nginx
