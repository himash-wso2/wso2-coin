FROM nginx:alpine

RUN adduser \
    --disabled-password \
    --gecos "" \
    --uid 10014 \
    "choreo"

USER 10014

COPY index.html /usr/share/nginx/html/

EXPOSE 8080

CMD ["nginx", "-g", "daemon off;"]
