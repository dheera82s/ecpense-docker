FROM node:20
RUN addgroup -S expense && adduser -S expense -G expense
RUN mkdir /opt/backend
RUN chown -R expense:expense /opt/backend
USER expense
WORKDIR /opt/backend
COPY package.json .
RUN npm install
COPY *.js .
ENV DB_HOST="mysql"
CMD ["node", "index.js"]