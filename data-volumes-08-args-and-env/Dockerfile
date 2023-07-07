FROM node:14

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

# 변수 지정이라고 보면 될듯
ARG DEFAULT_PORT=80

ENV PORT $DEFAULT_PORT

EXPOSE $PORT

# VOLUME [ "/app/node_modules" ]

CMD [ "npm", "start" ]