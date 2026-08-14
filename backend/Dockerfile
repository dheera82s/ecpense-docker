FROM node:20-alpine

RUN addgroup -S expense && adduser -S expense -G expense

WORKDIR /opt/backend

COPY package*.json ./

RUN npm install --omit=dev && npm cache clean --force

COPY *.js ./

RUN chown -R expense:expense /opt/backend

USER expense

ENV DB_HOST="mysql"

CMD ["node", "index.js"]