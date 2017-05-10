FROM nginx:alpine

RUN mkdir -p /data/nginx/cache
RUN rm /etc/nginx/conf.d/*
RUN mv /etc/nginx/nginx.conf /etc/nginx/nginx.conf-ori

COPY nginx.conf /etc/nginx/nginx.conf
COPY proxy.conf /etc/nginx/conf.d/

EXPOSE 80

STOPSIGNAL SIGQUIT

CMD ["nginx", "-g", "daemon off;"]
