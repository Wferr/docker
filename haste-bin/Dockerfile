FROM node:alpine
ENV NODE_ENV production
RUN apk --no-cache add memcached
RUN apk --no-cache --virtual download-dependencies add git
RUN git clone https://github.com/seejohnrun/haste-server.git /haste-server
RUN apk del download-dependencies
WORKDIR /haste-server
RUN npm install --production --silent
EXPOSE 7777
CMD npm start
