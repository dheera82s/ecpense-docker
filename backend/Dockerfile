FROM node:20

RUN groupadd -r expense && useradd -r -m -g expense expense

WORKDIR /opt/backend

COPY package.json .

RUN npm install

COPY *.js .

RUN chown -R expense:expense /opt/backend

USER expense

ENV DB_HOST="mysql"

CMD ["node", "index.js"]