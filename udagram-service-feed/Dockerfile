FROM node:12.19.0
WORKDIR /usr/src/app
COPY package-lock.json package.json tsconfig.json tslint.json src ./
RUN npm install

COPY src src
RUN npm run tsc
EXPOSE 8080
CMD [ "node", "./www/server.js" ]