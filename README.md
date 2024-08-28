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





const http = require('http');
const hostname = '0.0.0.0';
const port = 3000;

const server = http.createServer((reg, res) => {
res.statusCode = 200;
res.setHeader ('Content-Type', 'text/plain');
res.end ('Hello, World!\n');
});

server.listen(port, hostname, () => {
console.log('Server running at http://${hostnone}:${port}/');
});
