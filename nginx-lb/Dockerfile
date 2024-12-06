FROM nginx:latest

RUN adduser \
    --disabled-password \
    --gecos "" \
    --uid 10014 \
    "choreo"

USER 10014

COPY /data-directory/default.conf /etc/nginx/conf.d/

COPY /data-directory/index.html /usr/share/nginx/html/

EXPOSE 8080

CMD ["nginx", "-g", "daemon off;"]
