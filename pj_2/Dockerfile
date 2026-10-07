FROM nginx:alpine

RUN apk add --no-cache git

RUN rm -rf /usr/share/nginx/html/*

RUN git clone https://github.com/anlbora/SnakeGame---JavaScript.git /tmp/game && \
    cp /tmp/game/index.html /usr/share/nginx/html/ && \
    cp /tmp/game/script.js /usr/share/nginx/html/ && \
    cp /tmp/game/style.css /usr/share/nginx/html/ && \
    rm -rf /tmp/game

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
