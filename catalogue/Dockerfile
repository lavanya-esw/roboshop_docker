FROM node:20.19.5-alpine3.21 AS build
WORKDIR /opt/server
EXPOSE 8080
COPY *.json .
COPY *.js .
RUN npm install
ENV MONGO="true" \
    MONGO_URL="mongodb://mongodb:27017/catalogue"
CMD ["node","server.js"]
