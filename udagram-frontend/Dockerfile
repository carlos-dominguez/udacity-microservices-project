FROM node:12.19.0
WORKDIR /usr/src/app
RUN npm install -g ionic

COPY package.json package-lock.json ./
RUN npm install

COPY . .
RUN ionic build
EXPOSE 8100
CMD [ "ionic", "serve" ]