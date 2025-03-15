FROM node:lts

ENV NODE_OPTIONS=--openssl-legacy-provider

RUN npm i -g git http-server && \
    git clone https://github.com/jsonwebtoken/jsonwebtoken.github.io.git

WORKDIR /jsonwebtoken.github.io

RUN  npm install && ./node_modules/.bin/grunt build

CMD http-server /jsonwebtoken.github.io/dist/extension/

EXPOSE 8080