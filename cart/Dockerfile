FROM node:20.19.5-alpine3.21
WORKDIR /opt/server
EXPOSE 8080
COPY *.json .
COPY *.js .
RUN npm install
ENV REDIS_HOST="redis" \
    CATALOGUE_HOST="catalogue" \
    CATALOGUE_PORT="8080"
CMD ["node","server.js"]