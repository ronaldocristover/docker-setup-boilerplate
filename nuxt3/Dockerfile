FROM node:16-alpine

RUN mkdir -p /src/app
WORKDIR /src/app

COPY package*.json ./
RUN npm install

COPY . .

RUN npm run build

COPY . .

EXPOSE 3000

CMD [ "node", ".output/server/index.mjs" ]