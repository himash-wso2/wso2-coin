FROM nginx:latest

COPY /app/nginx.conf /etc/nginx/nginx.conf

COPY /app/index.html /etc/nginx/html/index.html

WORKDIR /app

RUN adduser \
    --disabled-password \
    --gecos "" \
    --uid 10014 \
    "nginxuser"

RUN chown -R nginxuser:nginxuser /app && chmod -R 755 /app && \
        chown -R nginxuser:nginxuser /var/cache/nginx && \
        chown -R nginxuser:nginxuser /var/log/nginx && \
        chown -R nginxuser:nginxuser /etc/nginx/conf.d
RUN touch /var/run/nginx.pid && \
        chown -R nginxuser:nginxuser /var/run/nginx.pid

USER 10014

EXPOSE 8080

CMD ["nginx", "-g", "daemon off;"]
