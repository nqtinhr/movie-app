FROM node:alpine3.18

WORKDIR /backend

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 5000
CMD [ "node", "index.js" ]
