FROM node:10-alpine

RUN mkdir -p /home/node/app/node_modules

WORKDIR /home/node/app

COPY package*.json ./

#USER node

RUN npm install

COPY . .

EXPOSE 8080

CMD [ "node", "app.js" ]
