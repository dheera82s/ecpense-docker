#FROM node:20
FROM node:20.18.3-alpine3.21
WORKDIR /opt/backend
COPY package.json .
RUN npm install
COPY *.js .
ENV DB_HOST="mysql"
CMD ["node", "index.js"]