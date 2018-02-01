FROM node:alpine
ENV node_env production
RUN apk --no-cache add redis git
RUN git clone https://github.com/seejohnrun/haste-server.git /haste-server
WORKDIR /haste-server
RUN npm install --production --silent
EXPOSE 7777
CMD redis-server --daemonize yes && npm start