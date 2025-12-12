FROM node:18-alpine

RUN apk add --no-cache python3 py3-pip make g++ bash

WORKDIR /app

COPY package.json package-lock.json ./

RUN npm install

COPY . .

RUN npm run build

EXPOSE 1337

CMD ["npm", "run", "start"]