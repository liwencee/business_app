i craeted hypothetical front end and backend with a dockerfile
FROM node:10-alpine

WORKDIR /home/node/app

COPY package*.json ./

USER node

RUN npm install

COPY . .

EXPOSE 8080

CMD [ "node", "app.js" ]

then create a docker ignore file with gitignore file to help store most file associated with those files
