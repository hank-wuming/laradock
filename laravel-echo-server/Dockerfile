FROM node:argon
 
# Create app directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app
 
# Install app dependencies
COPY package.json /usr/src/app/
RUN npm install
 
# Bundle app source
COPY laravel-echo-server.json /usr/src/app/laravel-echo-server.json

RUN mkdir -p /usr/src/app/ssl
COPY ssl.crt /usr/src/app/ssl/ssl.crt
COPY ssl.key /usr/src/app/ssl/ssl.key

EXPOSE 3000
CMD [ "npm", "start" ]
